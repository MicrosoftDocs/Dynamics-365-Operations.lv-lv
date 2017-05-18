---
title: "Formulas veidotājs elektronisko atskaišu veidošanā"
description: "Šajā tēmā ir paskaidrots, kā elektronisko pārskatu veidošanā (Electronic reporting — ER) lietot formulas veidotāju. Kad veidojat formātu noteiktam ER elektroniskajam dokumentam, datu pārveidošanai varat lietot Microsoft Excel stila formulas, lai izpildītu attiecīgā dokumenta izpildes un formatējuma prasības. Tiek atbalstītas dažādu veidu funkcijas — teksta, datuma un laika, matemātiski loģiskās, informācijas, datu tipa pārveidošanas un citas (biznesa jomai specifiskas funkcijas)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 335a0d7ca466028e8b157cb4e04df7d0f4880e73
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="formula-designer-in-electronic-reporting"></a>Formulas veidotājs elektronisko atskaišu veidošanā

[!include[banner](../includes/banner.md)]


Šajā tēmā ir paskaidrots, kā elektronisko pārskatu veidošanā (Electronic reporting — ER) lietot formulas veidotāju. Kad veidojat formātu noteiktam ER elektroniskajam dokumentam, datu pārveidošanai varat lietot Microsoft Excel stila formulas, lai izpildītu attiecīgā dokumenta izpildes un formatējuma prasības. Tiek atbalstītas dažādu veidu funkcijas — teksta, datuma un laika, matemātiski loģiskās, informācijas, datu tipa pārveidošanas un citas (biznesa jomai specifiskas funkcijas).

<a name="formula-designer-overview"></a>Pārskats par formulas veidotāju
-------------------------

Elektronisko atskaišu veidošana (Electronic Reporting — ER) atbalsta formulas veidotāju. Tāpēc veidošanas laikā varat konfigurēt izteiksmes, kuras var izmantot šādu uzdevumu izpildes laikā:

-   Datu pārveidošana tādiem datiem, kas ir saņemti no Microsoft Dynamics 365 for Operations datu bāzes un kas ir jāaizpilda ER datu modelī, kuru ir paredzēts lietot kā datu avotu ER formātiem (filtrēšana, grupēšana, datu tipa pārveidošana un citas darbības).
-   Datu formatēšana tādiem datiem, kas ir jāsūta uz ģenerēto elektronisko dokumentu saskaņā ar noteikta ER formāta izkārtojumu un nosacījumiem (saskaņā ar pieprasīto valodu vai kultūru, kodējumu un citām prasībām).
-   Elektronisko dokumentu ģenerēšanas procesa kontrolēšana (noteiktu formāta elementu izvades iespējošana/atspējošana atkarībā no datu apstrādes, dokumenta izveides pārtraukšana, ziņojumu sūtīšana lietotājiem un citas darbības).

Formulas veidotāja lapu var atvērt, veicot kādu no tālāk uzskaitītajām darbībām.

-   Datu avota elementus saistīt ar datu modeļa komponentiem.
-   Datu avota elementus saistīt ar formāta komponentiem.
-   Pabeigt aprēķināto lauku uzturēšanu kā daļu no datu avotiem.
-   Definēt redzamības nosacījumus lietotāja ievades parametriem.
-   Formatēt formāta transformācijas.
-   Definēt formāta komponentu iespējošanas nosacījumus.
-   Definēt failu nosaukumus formāta komponentiem FILE.
-   Definēt nosacījumus procesa kontroles pārbaudēm.
-   Definēt ziņojumu tekstu procesa kontroles pārbaudēm.

## <a name="designing-er-formulas"></a>ER formulu veidošana
### <a name="data-binding"></a>Datu saistīšana

ER formulas veidotāju var izmantot, lai definētu izteiksmi, kas pārveido no datu avotiem saņemtos datus, lai izpildes laikā šos datus varētu aizpildīt datu patērētājā:

-   No Dynamics 365 for Operations datu avotiem un izpildes laika parametriem uz ER datu modeli.
-   No ER datu modeļa uz ER formātu.
-   No Dynamics 365 for Operations datu avotiem un izpildes laika parametriem uz ER formātu.

Nākamajā attēlā ir parādīts šī tipa izteiksmes noformējums. Šajā piemērā izteiksme atgriež Dynamics 365 for Operations tabulas **Intrastat** lauka **Intrastat.AmountMST** vērtību pēc tam, kad šī vērtība ir noapaļota līdz diviem cipariem aiz komata. [![picture-expression-binding](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) Tālāk esošajā attēlā ir redzams, kā var izmantot šāda veida izteiksmi. Šajā piemērā izstrādātās izteiksmes rezultāts tiek ievadīts datu modeļa **Nodokļu pārskatu veidošanas modelis** komponentā **Transaction.InvoicedAmount**. [![picture-expression-binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) Izpildes laikā izstrādātā formula **ROUND (Intrastat.AmountMST, 2)** noapaļo katra tabulas **Intrastat** ieraksta lauka **AmountMST** vērtību līdz diviem cipariem aiz komata un ievada noapaļoto vērtību datu modeļa **Nodokļu pārskatu veidošana** komponentā **Transaction.InvoicedAmount**.

### <a name="data-formatting"></a>Datu formatēšana

ER formulas veidotāju var izmantot, lai definētu izteiksmi, kas formatē no datu avotiem saņemtos datus, lai šos datus varētu nosūtīt kā daļu no ģenerētā elektroniskā dokumenta. Ja jums ir formatēšana, kas ir jālieto kā tipisks nosacījums, kuru ir nepieciešams atkārtoti izmantot kādam formātam, tad formāta konfigurācijā šo formatēšanu varat vienu reizi ieviest kā nosauktu transformēšanu, kurai ir formatēšanas izteiksme. Pēc tam šo nosaukto transformēšanu var saistīt ar daudziem formāta komponentiem, kuriem ir nepieciešams formatēt izvadi atbilstoši izveidotajai izteiksmei. Nākamajā attēlā ir parādīts šī tipa transformēšanas noformējums. Šajā piemērā transformēšana **TrimmedString** saņem ienākošos datus ar datu tipu **String** un apcērp sākuma un beigu atstarpes, kad atgriež virknes vērtību. [![picture-transformation-design](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) Tālāk esošajā attēlā ir redzams, kā var lietot šāda veida transformēšanu. Šajā piemērā vairāki formāta komponenti, kas sūta tekstu kā izvadi uz ģenerēto elektronisko dokumentu, izpildes laikā atsaucas uz transformēšanu **TrimmedString** pēc nosaukuma. [![picture-transformation-usage](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) Ja formāta komponentos ir atsauce uz transformāciju **TrimmedString ** (piemēram, komponentā **partyName** iepriekšējā attēlā), kā izvade uz ģenerēto dokumentu tiek nosūtīts teksts. Teksts neietver sākuma un noslēdzošās atstarpes. Ja jums ir formatējums, kas ir jālieto atsevišķi, šo formatējumu varat ieviest kā noteikta formāta komponenta saistīšanas atsevišķu izteiksmi. Nākamajā attēlā ir parādīta šī tipa izteiksme. Šajā piemērā formāta komponents **partyType** tiek saistīts ar datu avotu, izmantojot izteiksmi, kas ienākošos datus no lauka **Model.Company.RegistrationType** datu avotā pārveido par tekstu, kurš rakstīts ar lielajiem burtiem, un šo teksta izvadi sūta uz elektronisko dokumentu. [![picture-binding-with-formula](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Apstrādes plūsmas kontrole

ER formulas veidotāju var izmantot, lai definētu izteiksmes, kas kontrolē dokumentu ģenerēšanas procesa plūsmu. Jūs varat:

-   Definējiet nosacījumus, kas nosaka, kad ir jāaptur dokumenta veidošanas process.
-   Norādiet izteiksmes, kas izveido ziņojumus lietotājam par apturētiem procesiem vai parāda izpildes žurnāla ziņojumus par pārskata ģenerēšanas procesa turpināšanu.
-   Norādiet ģenerēto dokumentu failu nosaukumus un to izveidošanas kontroles nosacījumus.

Katrs apstrādes plūsmas kontroles noteikums ir paredzēts kā atsevišķa pārbaude. Nākamajā attēlā ir parādīta šī tipa pārbaude. Šeit ir šajā piemērā lietotās konfigurācijas skaidrojums:

-   Pārbaude tiek novērtēta, kad ģenerētajā XML failā tiek izveidots mezgls **INSTAT**.
-   Ja transakciju saraksts ir tukšs, pārbaude aptur izpildes procesu un atgriež uzrakstu **FALSE**.
-   Pārbaude atgriež kļūdas ziņojumu, kas ietver etiķetes SYS70894 tekstu lietotāja vēlamajā valodā.

[![picture-validation](./media/picture-validation.jpg)](./media/picture-validation.jpg) ER formulas veidotāju var arī izmantot, lai norādītu ģenerētā elektroniskā dokumenta faila nosaukumu un kontrolētu faila izveides procesu. Nākamajā attēlā ir parādīts šī tipa procesa plūsmas kontroles noformējums. Šeit ir šajā piemērā lietotās konfigurācijas skaidrojums:

-   Ierakstu saraksts no datu avota **model.Intrastat** tiek sadalīts partijās, un katra no tām ietver līdz 1000 ierakstus.
-   Izvade izveido zip failu, kas katrai izveidotajai partijai satur vienu failu XML formātā.
-   Izteiksme atgriež faila nosaukumu ģenerētajiem elektroniskajiem dokumentiem, savienojot faila nosaukumu un faila paplašinājumu. Otrajai partijai un visām turpmākajām partijām faila nosaukums kā sufiksu ietver partijas ID.
-   Izteiksme iespējo (atgriežot vērtību **TRUE**) procesu faila izveidošanai partijām, kuras ietver vismaz vienu ierakstu.

[![picture-file-control](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Pamata sintakse

ER izteiksmes var saturēt jebkuru vai visus no šādiem elementiem:

-   Konstantes
-   Operatori
-   Atsauces
-   Ceļi
-   Funkcijas

#### <a name="constants"></a>Konstantes

Kad veidojat izteiksmes, varat lietot teksta un skaitļu konstantes (vērtības, kas netiek aprēķinātas). Piemēram, izteiksmē **VALUE ("100") + 20** tiek izmantota skaitliskas vērtības konstante 20 un virknes vērtības konstante “100” un tā atgriež skaitlisku vērtību **120**. ER formulas veidotājs atbalsta atsoļa sekvences, kas nozīmē, ka varat norādīt, kura izteiksmes virkne ir jāapstrādā citādi. Piemēram, izteiksme **"Ļevs Tolstojs ""Karš un miers"" 1. sējums"** atgriež šādu teksta virkni: **Ļevs Tolstojs "Karš un miers" 1. sējums**.

#### <a name="operators"></a>Operatori

Nākamajā tabulā ir parādīti aritmētiskie operatori, ko varat izmantot, lai veiktu pamata matemātiskās darbības, piemēram, saskaitīšanu, atņemšanu, dalīšanu un reizināšanu.

| Operators | Nozīme              | Paraugs |
|----------|----------------------|---------|
| +        | Papildinājums             | 1+2     |
| -        | Atņemšana Negācija | 5-2 -1  |
| \*       | Reizināšana       | 7\*8    |
| /        | Nodaļa             | 9/3     |

Nākamajā tabulā ir parādīti salīdzināšanas operatori, kas tiek atbalstīti un ko varat izmantot, lai salīdzinātu divas vērtības.

| Operators | Nozīme                  | Paraugs    |
|----------|--------------------------|------------|
| =        | Vienāds                    | X=Y        |
| &gt;     | Lielāks nekā             | X&gt;Y     |
| &lt;     | Mazāks nekā                | X&lt;Y     |
| &gt;=    | Lielāks vai vienāds ar | X&gt;=Y    |
| &lt;=    | Mazāks vai vienāds ar    | X&lt;=Y    |
| &lt;&gt; | Nav vienāds ar             | X&lt;&gt;Y |

Turklāt rakstzīmi & varat izmantot kā teksta konkatenācijas operatoru, lai vienu vai vairākas teksta virknes savirknētu jeb savienotu vienā teksta daļā.

| Operators | Nozīme     | Paraugs                                        |
|----------|-------------|------------------------------------------------|
| &        | Savienot | "Nav ko drukāt" & ": " & "nav atrasts neviens ieraksts" |

#### <a name="operator-precedence"></a>Operatoru prioritātes

Ir svarīgi, kādā secībā tiek vērtētas saliktas izteiksmes daļas. Piemēram, izteiksmes **1 + 4 / 2** rezultāts atšķiras atkarībā no tā, vai pirmā tiek izpildīta saskaitīšana vai dalīšana. Varat izmantot iekavas, lai skaidri definētu, kā izteiksme tiek novērtēta. Piemēram, lai norādītu, ka vispirms ir jāveic saskaitīšanas operācija, iepriekšējo izteiksmi varat pārveidot uz **(1 + 4) / 2**. Ja nav skaidri definēta operāciju secība, kādā izteiksme ir jāizpilda, tad darbības ir atkarīgas no atbalstītajiem operatoriem piešķirtās noklusējuma prioritāšu secības. Nākamajā tabulā ir parādīti operatori un katram piešķirtā prioritāte. Operatori, kuru prioritāte ir augstāka (piemēram, 7), tiek vērtēti pirms operatoriem, kuriem ir zemāka prioritāte (piemēram, 1).

| Prioritāšu secība | Operatori      | Sintakse                                                   |
|------------|----------------|----------------------------------------------------------|
| 7.          | Grupēšana       | ( … )                                                    |
| 6.          | Piekļuve elementam  | … . …                                                    |
| 5.          | Funkcijas izsaukums  | … ( … )                                                  |
| 4.          | Reizināšana un dalīšana | … \* … … / …                                             |
| 3.          | Piedeva       | … + … … - …                                              |
| 2.          | Salīdzinājums     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1.          | Atdalīšana     | … , …                                                    |

Vienā rindā esošiem operatoriem ir vienāda prioritāte. Ja kādā izteiksmē ir ietverti vairāki no šiem operatoriem, izteiksme tiek vērtēta no kreisās puses uz labo. Piemēram, izteiksme **1 + 6 / 2 \* 3 &gt; 5** atgriež vērtību **patiess**. Ieteicams izmantot iekavas, lai izteiksmēm skaidri norādītu vēlamo vērtēšanas secību, tā izteiksmes padarot vieglāk salasāmas un uzturamas.

#### <a name="references"></a>Atsauces

Visus pašreizējā ER komponenta (modeļa vai formāta) datu avotus, kas ir pieejami izteiksmes veidošanas laikā, var izmantot kā nosauktas atsauces. Piemēram, pašreizējais ER datu modelis ietver datu avotu **ReportingDate**, kurš atgriež vērtību ar datu tipu **DATETIME**. Lai pareizi formatētu šo vērtību ģenerētajā dokumentā, varat izteiksmē ietvert atsauci uz datu avotu šādā veidā: **DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")**. Pirms visām ar atsauci norādītā datu avota nosaukumā esošajām rakstzīmēm, kas nav alfabēta burti, ir jāievieto vienpēdiņa ('). Ja ar atsauci norādītā datu avota nosaukumā ir vismaz viens simbols, kas nav alfabēta burts (piemēram, interpunkcijas zīmes vai citi rakstības simboli), nosaukums ir jāietver vienpēdiņās. Daži piemēri:

-   Uz datu avotu **Today's date & time** jūsu ER izteiksmē ir jāatsaucas šādi: **'Today''s date & time'**
-   Uz metodi **name()** datu avotam **Customers** jūsu ER izteiksmē ir jāatsaucas šādi: **Customers.'name()'**

#### <a name="path"></a>Ceļš

Ja izteiksme atsaucas uz kādu strukturētu datu avotu, ceļa definīciju varat izmantot, lai atlasītu konkrētu šī datu avota primitīvo elementu. Punkta rakstzīme (.) tiek lietota, lai atdalītu atsevišķus strukturēta datu avota elementus. Piemēram, pašreizējais ER datu modelis ietver datu avotu **InvoiceTransactions**, kurš atgriež ierakstu sarakstu. Ieraksta**InvoiceTransactions** struktūra ietver laukus **AmountDebit** un **AmountCredit**, kuri atgriež skaitliskas vērtības. Tādēļ varat izveidot šādu izteiksmi, lai aprēķinātu rēķinā iekļauto summu: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>Funkcijas

Nākamajā sadaļā ir aprakstītas funkcijas, kuras var izmantot ER izteiksmēs. Visus izteiksmes konteksta datu avotus (pašreizējo ER datu modeli vai ER formātu), kā arī visas konstantes var izmantot kā parametrus funkciju izsaukšanai saskaņā ar funkciju izsaukšanas argumentu sarakstu. Piemēram, pašreizējais ER datu modelis ietver datu avotu **InvoiceTransactions**, kurš atgriež ierakstu sarakstu. Ieraksta**InvoiceTransactions** struktūra ietver laukus **AmountDebit** un **AmountCredit**, kuri atgriež skaitliskas vērtības. Tāpēc, lai aprēķinātu rēķinā iekļauto sumu, varat izveidot šādu izteiksmi, kas lieto iebūvēto ER noapaļošanas funkciju: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>Atbalstītās funkcijas
Nākamajās tabulās ir aprakstītas datu manipulācijas funkcijas, kuras var izmantot, lai izveidotu ER datu modeļus un ER atskaites. Šis funkciju saraksts nav fiksēts, un izstrādātāji to var pagarināt. Lai redzētu sarakstu ar funkcijām, kuras varat izmantot, piekļūstiet funkciju rūtij ER formulas veidotājā.

### <a name="date-and-time-functions"></a>Datuma un laika funkcijas

| Funkcija                                   | Apraksts                                                                                                                                                                                                                                                                                                                                                      | Piemērs                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS (datums un laiks, dienas)                   | Norādītajai datuma un laika vērtībai pieskaitiet norādīto dienu skaitu.                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW(), 7)** atgriež datumu un laiku septiņas dienas uz priekšu.                                                                                                                                                                                                                            |
| DATETODATETIME (datums)                      | Norādīto datuma vērtību pārveidojiet par datuma un laika vērtību.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. 'getCurrentDate()')** atgriež pašreizējās Dynamics 365 for Operations sesijas datumu 12.24.2015. formātā **12/24/2015 12:00:00 AM**. Šajā piemērā **CompInfo** ir ER datu avots ar tipu **Dynamics 365 for Operations/Table**, kas atsaucas uz tabulu CompanyInfo. |
| NOW ()                                     | Pašreizējā Dynamics 365 for Operations programmas servera datumu un laiku atgrieziet kā datuma un laika vērtību.                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | Pašreizējā Dynamics 365 for Operations programmas servera datumu atgrieziet kā datuma vērtību.                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | Atgrieziet datuma vērtību **null**.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | Atgrieziet datuma un laika vērtību **null**.                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT (datums un laiks, formāts)          | Norādīto datuma un laika vērtību pārveidojiet par virkni norādītajā formātā. (Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)                                                                        | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** pašreizējo Dynamics 365 for Operations programmas servera datumu, 12/24/2015, atgriež kā **"24-12-2015"**, atbilstoši norādītajam pielāgotajam formātam.                                                                                                          |
| DATETIMEFORMAT (datums un laiks, formāts, kultūra) | Norādīto datuma un laika vērtību pārveidojiet par virkni norādītajā formātā un atbilstoši norādītajai [kultūrai](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** pašreizējo Dynamics 365 for Operations programmas servera datumu, 12/24/2015, atgriež kā **"24.12.2015"**, atbilstoši atlasītajai vācu kultūrai.                                                                                                             |
| SESSIONTODAY ()                            | Pašreizējās Dynamics 365 for Operations sesijas datumu atgriež kā datuma vērtību.                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | Pašreizējās Dynamics 365 for Operations sesijas datumu un laiku atgriež kā datuma un laika vērtību.                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT (datums, formāts)                  | Atgriež datuma virknes attēlojumu, izmantojot norādīto formātu.                                                                                                                                                                                                                                                                                                    | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** pašreizējās Dynamics 365 for Operations sesijas datumu 12/24/2015 atgriež kā “**24-12-2015**” atbilstoši norādītajam pielāgotajam formātam.                                                                                                                      |
| DATEFORMAT (datums, formāts, kultūra)         | Norādīto datuma vērtību pārveidojiet par virkni norādītajā formātā un atbilstoši norādītajai [kultūrai](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)     | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** pašreizējās Dynamics 365 for Operations sesijas datumu 12/24/2015 atgriež kā **“24.12.2015”** atbilstoši atlasītajai vācu kultūrai.                                                                                                                       |

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
<th>Piemērs</th>
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
<td>Nākamajā piemērā datu avots <strong>Lines</strong> tiek izveidots kā ierakstu saraksts, kurš sastāv no trīs ierakstiem, un tas tiek sadalīts divās partijās — katrā no partijām ir līdz diviem ierakstiem. <a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a> Tālāk ir norādīts izstrādātā formāta izkārtojums, kurā ir izveidotas saites ar datu avotu <strong>Lines</strong>, lai ģenerētu izvades XML formāta failu, kurā ir ietverti atsevišķi mezgli atbilstoši katrai paketei un tajā ietvertajiem ierakstiem. <a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a> Tālāk ir norādīts izstrādātā formāta izpildes rezultāts. <a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (1. ieraksts [, 2. ieraksts, ...])</td>
<td>Atgriezt jaunu sarakstu, kas tiek izveidots no norādītajiem argumentiem.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> atgriež tukšu ierakstu, kur lauku saraksts satur visus laukus no ierakstu sarakstiem <strong>MainData</strong> un <strong>OtherData</strong>.</td>
</tr>
<tr class="even">
<td>LISTJOIN (1. saraksts, 2. saraksts, ...)</td>
<td>Atgriezt savienotu sarakstu, kas tiek izveidots no norādīto argumentu sarakstiem.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> atgriež sešu ierakstu sarakstu, kurā viens datu tipa <strong>STRING</strong> lauks satur atsevišķus burtus.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (saraksts)</td>
<td>Atgriezt vērtību <strong>TRUE</strong>, ja norādītajā sarakstā nav neviena elementa. Pretējā gadījumā atgriezt vērtību <strong>FALSE</strong>.</td>
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
<td>Atgriezt jaunu izplātu sarakstu, kas atspoguļo visus elementus, kuri atbilst norādītajam ceļam. Šis ceļš ir jādefinē kā derīgs datu avota ceļš uz datu avota elementu, kuram ir ierakstu saraksta datu tips. Ceļam uz virkni, datumu un citiem datu elementiem ER izteiksmju veidotājā noformēšanas laikā ir jāizraisa kļūda.</td>
<td>Ja kā satura avotu (DS) ievadāt <strong>SPLIT(&quot;abcdef&quot; , 2)</strong>, funkcija <strong>COUNT( ALLITEMS (DS.Value))</strong> atgriež vērtību <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (saraksts [, 1. izteiksme, 2. izteiksme, …])</td>
<td>Atgriezt norādīto sarakstu, kas ir sakārtots atbilstoši norādītajiem argumentiem, kurus var definēt kā izteiksmes.</td>
<td>Kad parametrs <strong>Vendor</strong>(Kreditors) ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, tad<strong>ORDERBY (Vendors, Vendors.'name()')</strong> atgriež sarakstu ar kreditoriem, kuri ir sakārtoti augošā secībā pēc nosaukuma.</td>
</tr>
<tr class="even">
<td>REVERSE (saraksts)</td>
<td>Atgriezt norādīto sarakstu apgrieztā kārtošanas secībā.</td>
<td>Kad parametrs <strong>Vendor</strong>(Kreditors) ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, tad <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong> atgriež sarakstu ar kreditoriem, kuri ir sakārtoti dilstošā secībā pēc nosaukuma.</td>
</tr>
<tr class="odd">
<td>WHERE (saraksts, nosacījums)</td>
<td>Atgriezt norādīto sarakstu, kas ir filtrēts atbilstoši norādītajam nosacījumam. Atšķirībā no funkcijas <strong>FILTER</strong>, norādītais nosacījums tiek lietots attiecībā uz atmiņā esošu sarakstu.</td>
<td>Ja parametrs <strong>Vendor</strong> ir konfigurēts kā ER datu avots ar atsauci uz tabulu VendTable, funkcija <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> atgriež kreditoru grupā 40 ietverto kreditoru sarakstu.</td>
</tr>
<tr class="even">
<td>ENUMERATE (saraksts)</td>
<td>Atgriezt jaunu sarakstu, kas sastāv no norādītā saraksta uzskaitījuma ierakstiem un parāda šādus elementus:
<ul>
<li>Norādītā saraksta ieraksti kā parasti saraksti (komponents <strong>Value</strong>)</li>
<li>Pašreizējā ieraksta indekss (komponents <strong>Number</strong>)</li>
</ul></td>
<td>Nākamajā piemērā datu avots <strong>Enumerated</strong> tiek izveidots kā uzskaitījuma kreditoru ierakstu saraksts no datu avota <strong>Vendors</strong>, kurš atsaucas uz tabulu <strong>VendTable</strong>. <a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>Šeit ir formāts, kur datu saistījumi tiek izveidoti, lai ģenerētu izvadi XML formātā, kas atsevišķus kreditorus attēlo kā uzskaitījuma zarus. <a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a> Tālāk ir norādīts izstrādātā formāta izpildes rezultāts. <a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (saraksts)</td>
<td>Atgriezt ierakstu skaitu norādītajā sarakstā, ja šis saraksts nav tukšs. Pretējā gadījumā atgriezt vērtību <strong>0</strong> (nulle).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> atgriež vērtību <strong>2</strong>, jo funkcija <strong>SPLIT</strong> izveido sarakstu, kas sastāv no diviem ierakstiem.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (ceļš)</td>
<td>Atgriež ierakstu sarakstu, kas izveidots no argumenta ar vienu no tālāk uzskaitītajiem tipiem.
<ul>
<li>Modeļa uzskaitījums</li>
<li>Formāta uzskaitījums</li>
<li>Konteiners</li>
</ul>
Izveidotais saraksts sastāvēs no ierakstiem ar šādiem laukiem:
<ul>
<li>Vārds, uzvārds</li>
<li>Etiķete</li>
<li>apraksts</li>
</ul>
Lauki Etiķete un Apraksts atgriezīsies pie izpildes laika vērtībām, pamatojoties uz formāta valodas iestatījumiem.</td>
<td>Nākamajā piemērā ir parādīts datu modelī ieviests uzskaitījums. <a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>Nākamajā piemērā ir redzams tālāk norādītais.
<ul>
<li>Modeļa uzskaitījums ievietots pārskatā kā datu avots.</li>
<li>ER izteiksme, izveidota ar mērķi lietot modeļa uzskaitījumu kā šīs funkcijas parametru.</li>
<li>Datu avots ar ierakstu saraksta tipu, ievietots pārskatā, izmantojot izveidoto ER izteiksmi.</li>
</ul>
<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> Tālāk esošajā piemērā ir redzami ER formāta elementi, kas ir saistīti ar ierakstu saraksta tipa datu avotu, kurš ir izveidots, izmantojot funkciju LISTOFFIELDS.<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>Tālāk ir norādīts izstrādātā formāta izpildes rezultāts.<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>Piezīme.</strong> ER formāta izvadē etiķešu un aprakstu tulkotais teksts tiek nodrošināts saskaņā ar valodas iestatījumiem, kas ir konfigurēti formāta vecākelementiem FILE un FOLDER.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (saraksts, lauka nosaukums, norobežotājs)</td>
<td>Atgriež savirknētu vērtību virkni laukam no saraksta, atdalot elementus ar atlasīto norobežotāju.</td>
<td>Ja kā datu avotu SD ievadījāt SPLIT(“abc” , 1), izteiksme STRINGJOIN (DS, DS.Value, “:”) atgriež “a:b:c”</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (saraksts, robežvērtība, ierobežojumu avots)</td>
<td>Attiecīgo sarakstu sadala jaunā apakšsarakstu sarakstā un atgriež rezultātu ierakstu saraksta saturā. Robežvērtības parametrs norāda ierobežojuma vērtību sākotnējā saraksta sadalīšanai. Ierobežojuma avota parametrs norāda soli, par kādu kopsumma tiek palielināta. Ierobežojums netiek lietots atsevišķam elementam attiecīgajā sarakstā, ja ierobežojuma avots pārsniedz definēto ierobežojumu.</td>
<td>Nākamajā piemērā ir redzams parauga formāts, izmantojot datu avotus. <a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>Tālāk ir redzams formāta izpildes rezultāts, kurā ir ietverts nekārtots preču saraksts.<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>Tālāk esošajā piemērā ir redzams tas pats formāts, kas ir pielāgots preču saraksta rādīšanai pa partijām, vienā partijā ietverot preces, kuru kopējais svars nepārsniedz ierobežojumu 9.<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>Tālāk ir redzams pielāgotā formāta izpildes rezultāts. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a><strong>Piezīme.</strong> Ierobežojums netiek lietots pēdējam sākotnējā saraksta elementam, jo tā ierobežojuma avota (svara) vērtība (11) pārsniedz noteikto ierobežojumu (9). Lai pārskata ģenerēšanas laikā ignorētu (izlaistu) apakšsarakstus (ja nepieciešams), izmantojiet funkciju <strong>WHERE</strong> vai <strong>Enabled</strong>.</td>
</tr>
<tr class="odd">
<td>FILTER (saraksts, nosacījums)</td>
<td>Atgriež doto sarakstu, kas ar vaicājuma modificēšanu ir filtrēts pēc norādītā nosacījuma. Atšķirībā no funkcijas <strong>WHERE</strong>, norādītais nosacījums tiek lietots datu bāzes līmenī attiecībā uz visiem ER datu avotiem ar tipu Tabulas ieraksti.</td>
<td>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;) atgriež tikai to kreditoru sarakstu, kuri ir ietverti kreditoru grupā “40”, ja parametrs <strong>Vendor</strong> ir konfigurēts kā ER datu avots ar atsauci uz tabulu <strong>VendTable</strong></td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Loģiskas funkcijas

| Funkcija                                                                                | apraksts                                                                                                                                                                                                                                                                     | Paraugs                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CASE (izteiksme, 1. opcija, 1. rezultāts \[, 2. opcija, 2. rezultāts\] ... \[, noklusējuma rezultāts\]) | Norādītās izteiksmes vērtību novērtēt pret norādītajām alternatīvajām opcijām. Atgriezt tās opcijas rezultātu, kas ir vienāda ar izteiksmes vērtību. Pretējā gadījumā atgriezt pēc izvēles ievadīto noklusējuma rezultātu (pēdējais parametrs, kura priekšā neatrodas opcija). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** atgriež virkni **"WINTER"**, ja pašreizējās Dynamics 365 for Operations sesijas datums ir diapazonā no oktobra līdz decembrim. Pretējā gadījumā šī izteiksme atgriež tukšu virkni. |
| IF (nosacījums, 1. vērtība, 2. vērtība)                                                        | Atgriezt norādīto 1. vērtību, ja attiecīgais nosacījums tiek izpildīts. Pretējā gadījumā tiek atgriezta 2. vērtība. Ja 1. vērtība un 2. vērtība ir ieraksti vai ierakstu saraksti, rezultātā ir ietverti tikai tie lauki, kas ir iekļauti abos sarakstos.                                                                     | **IF (1=2, "nosacījums tiek izpildīts", "nosacījums netiek izpildīts")** atgriež virkni **"nosacījums netiek izpildīts"**.                                                                                                                                                      |
| NOT (nosacījums)                                                                         | Atgriezt norādītā nosacījuma pretējo loģisko vērtību.                                                                                                                                                                                                                   | **NOT (TRUE)** atgriež **FALSE**.                                                                                                                                                                                                                            |
| AND (1. nosacījums\[, 2. nosacījums, ...\])                                                 | Atgriež **TRUE**, ja *visi *norādītie nosacījumi ir patiesi. Pretējā gadījumā atgriezt vērtību **FALSE**.                                                                                                                                                                                            | **AND (1=1, "a"="a")** atgriež **TRUE**. **AND (1=2, "a"="a")** atgriež **FALSE**.                                                                                                                                                                           |
| OR (1. nosacījums\[, 2. nosacījums, ...\])                                                  | Atgriež **FALSE**, ja *visi *norādītie nosacījumi ir aplami. Atgriež **TRUE**, ja *kāds *no norādītajiem nosacījumiem ir patiess.                                                                                                                                                                 | **OR (1=2, "a"="a")** atgriež **TRUE**.                                                                                                                                                                                                                      |

### <a name="mathematical-functions"></a>Matemātiskās funkcijas

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funkcija</th>
<th>Apraksts</th>
<th>Piemērs</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ABS (skaitlis)</td>
<td>Atgriezt norādītā skaitļa absolūto vērtību (skaitli bez tā zīmes).</td>
<td><strong>ABS (-1)</strong> atgriež <strong>1</strong>.</td>
</tr>
<tr class="even">
<td>POWER (skaitlis, pakāpe)</td>
<td>Atgriezt rezultātu norādītā pozitīvā skaitļa kāpināšanai norādītajā pakāpē.</td>
<td><strong>POWER (10, 2)</strong> atgriež <strong>100</strong>.</td>
</tr>
<tr class="odd">
<td>NUMBERVALUE (virkne, decimāldaļu atdalītājs, ciparu grupēšanas atdalītājs)</td>
<td>Norādīto virkni pārveidot par skaitli. Norādītais simbols tiek lietots, lai decimāldaļskaitlim veselo skaitli atdalītu no daļskaitļiem, kā arī tiek lietots norādītais tūkstošu atdalītājs.</td>
<td><strong>NUMBERVALUE(&quot;1 234,56&quot;, &quot;,&quot;, &quot; &quot;)</strong> atgriež vērtību <strong>1234,56</strong>.</td>
</tr>
<tr class="even">
<td>VALUE (vērtība)</td>
<td>Norādīto virkni pārveidot par skaitli. Komati un punkta rakstzīmes (.) tiek uzskatīti par decimāldaļu atdalītājiem, un sākuma defise (-) tiek lietota kā mīnusa zīme. Parādīt izņēmumu, ja norādītajā virknē tiek konstatētas citas rakstzīmes, kas nav skaitļi.</td>
<td><strong>VALUE (&quot;1 234,56&quot;)</strong> rada izņēmumu.</td>
</tr>
<tr class="odd">
<td>ROUND (skaitlis, cipari aiz komata)</td>
<td>Atgriezt norādīto skaitli, kas ir noapaļots līdz norādītajam ciparu skaitam aiz komata:
<ul>
<li>Ja norādītais ciparu skaits aiz komata ir lielāks par 0 (nulle), tad norādītais skaitlis tiek noapaļots līdz norādītajam ciparu skaitam aiz komata.</li>
<li>Ja norādītais ciparu skaits aiz komata ir 0 (nulle), tad norādītais skaitlis tiek noapaļots tuvākajam veselajam skaitlim.</li>
<li>Ja norādītais ciparu skaits aiz komata ir mazāks par 0 (nulle), tad norādītais skaitlis tiek noapaļots līdz cipariem, kas atrodas pa kreisi no komata.</li>
</ul></td>
<td><strong>ROUND (1200.767, 2)</strong> noapaļo līdz diviem cipariem aiz komata un atgriež <strong>1200.77</strong>. <strong>ROUND (1200.767, -3)</strong> noapaļo līdz tuvākajam 1,000 reizinājumam un atgriež <strong>1000</strong>.</td>
</tr>
<tr class="even">
<td>ROUNDDOWN (skaitlis, cipari aiz komata)</td>
<td>Atgriezt norādīto skaitli, kas ir noapaļots uz leju (nulles virzienā) līdz norādītajam ciparu skaitam aiz komata. <strong>Piezīme.</strong> Šī funkcija darbojas līdzīgi funkcijai <strong>ROUND</strong>, bet attiecīgo skaitli tā vienmēr noapaļo uz leju.</td>
<td><strong>ROUNDDOWN (1200.767, 2)</strong> noapaļo uz leju līdz diviem cipariem aiz komata un atgriež <strong>1200.76</strong>. <strong>ROUNDDOWN (1700.767, -3)</strong> noapaļo uz leju līdz tuvākajam 1,000 reizinājumam un atgriež <strong>1000</strong>.</td>
</tr>
<tr class="odd">
<td>ROUNDUP (skaitlis, cipari aiz komata)</td>
<td>Atgriezt norādīto skaitli, kas ir noapaļots uz augšu (prom no nulles) līdz norādītajam ciparu skaitam aiz komata. <strong>Piezīme.</strong> Šī funkcija darbojas līdzīgi funkcijai <strong>ROUND</strong>, bet attiecīgo skaitli tā vienmēr noapaļo uz augšu.</td>
<td><strong>ROUNDUP (1200.763, 2)</strong> noapaļo uz augšu līdz diviem cipariem aiz komata un atgriež <strong>1200.77</strong>. <strong>ROUNDUP (1200.767, -3)</strong> noapaļo uz augšu līdz tuvākajam 1,000 reizinājumam un atgriež <strong>2000</strong>.</td>
</tr>
</tbody>
</table>

### <a name="record-functions"></a>Ieraksta funkcijas

| Funkcija             | Apraksts                                                                                                                                                                                                                                     | Piemērs                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (saraksts) | Atgriezt ierakstu **null**, kam ir tāda pati struktūra kā norādītajam ierakstu sarakstam vai ierakstam. **Piezīme.**Šī funkcija ir novecojusi. Tās vietā lietojiet **EMPTYRECORD**.                                                                                  | **NULLCONTAINER (SPLIT ("abc", 1))** atgriež jaunu tukšu ierakstu, kam ir tāda pati struktūra kā sarakstam, ko atgrieza funkcija **SPLIT**. |
| EMPTYRECORD (ieraksts) | Atgriezt ierakstu **null**, kam ir tāda pati struktūra kā norādītajam ierakstu sarakstam vai ierakstam. **Piezīme.** Ieraksts **Null** tiek lietots, ja visu lauku vērtības ir tukšas (**0** \[nulle\] skaitliskas vērtības laikam, tukša vērtība virknes laukam utt.). | **EMPTYRECORD (SPLIT ("abc", 1))** atgriež jaunu tukšu ierakstu, kam ir tāda pati struktūra kā sarakstam, ko atgrieza funkcija **SPLIT**.   |

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
<th>Apraksts</th>
<th>Piemērs</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER (virkne)</td>
<td>Atgriezt norādīto virkni, kas pārveidota par lielajiem burtiem.</td>
<td><strong>UPPER(&quot;Paraugs&quot;)</strong> atgriež <strong>&quot;PARAUGS&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (virkne)</td>
<td>Atgriezt norādīto virkni, kas pārveidota par mazajiem burtiem.</td>
<td><strong>LOWER (&quot;Paraugs&quot;)</strong> atgriež <strong>&quot;paraugs&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>LEFT (virkne, rakstzīmju skaits)</td>
<td>Atgriezt noteikto rakstzīmju skaitu no norādītās virknes sākuma.</td>
<td><strong>LEFT (&quot;Paraugs&quot;, 3)</strong> atgriež <strong>&quot;Par&quot;</strong>.</td>
</tr>
<tr class="even">
<td>RIGHT (virkne, rakstzīmju skaits)</td>
<td>Atgriezt noteikto rakstzīmju skaitu no norādītās virknes beigām.</td>
<td><strong>RIGHT (&quot;Paraugs&quot;, 3)</strong> atgriež <strong>&quot;ugs&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>MID (virkne, sākuma pozīcija, rakstzīmju skaits)</td>
<td>Atgriezt noteikto rakstzīmju skaitu no norādītās virknes, sākot norādītajā pozīcijā.</td>
<td><strong>MID (&quot;Paraugs&quot;, 2, 3)</strong> atgriež <strong>&quot;ara&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LEN (virkne)</td>
<td>Atgriezt norādītajā virknē esošo rakstzīmju skaitu.</td>
<td><strong>LEN (&quot;Paraugs&quot;)</strong> atgriež <strong>6</strong>.</td>
</tr>
<tr class="odd">
<td>CHAR (skaitlis)</td>
<td>Atgriezt rakstzīmju virkni, uz ko atsaucas norādītais unikoda skaitlis.</td>
<td><strong>CHAR (255)</strong> atgriež <strong>&quot;ÿ&quot;</strong>. <strong>Piezīme:</strong> atgrieztā virkne ir atkarīga kodējuma, kas ir atlasīts vecākelementa formāta elementā FILE. Atbalstīto kodējumu saraksts ir atrodams tēmā <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodējuma klase</a>.</td>
</tr>
<tr class="even">
<td>CONCATENATE (1. virkne [, 2. virkne, …])</td>
<td>Atgriezt visas norādītās tekstu virknes, kas ir savienotas vienā virknē.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> atgriež <strong>&quot;abcdef&quot;</strong>. <strong>Piezīme.</strong> Arī izmantojot izteiksmi <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong>, tiek atgriezta vērtība <strong>&quot;abcdef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TRANSLATE (virkne, raksts, aizstājējs)</td>
<td>Atgriezt norādīto virkni, kurā visi norādītajā raksta virknē esošie rakstzīmju gadījumi tiek aizstādi ar rakstzīmēm, kas atrodas norādītās aizstāšanas virknes atbilstošajā pozīcijā.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> aizstāj burtus <strong>&quot;cd&quot;</strong> ar virkni <strong>&quot;GH&quot;</strong> un atgriež <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (virkne, raksts, aizstājējs, parastas izteiksmes karodziņš)</td>
<td>Ja norādītās parastās izteiksme karogs ir <strong>true</strong>, atgriezt norādīto virkni, kas ir modificēta, lietojot šai funkcijai kā raksta argumentu norādīto parasto izteiksmi. Šī izteiksme tiek izmantota, lai atrastu rakstzīmes, kas ir jāaizstāj. Norādītā aizstāšanas argumenta rakstzīmes tiek izmantotas, lai aizstātu atrastās rakstzīmes. Ja norādītās parastās izteiksmes karogs ir <strong>false</strong>, šī funkcija darbojas kā <strong>TRANSLATE</strong>.</td>
<td>  <strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> lieto parastu izteiksmi, kas noņem visus simbolus, kuri nav skaitļi, un atgriež <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> aizstāj burtus <strong>&quot;cd&quot;</strong> ar virkni <strong>&quot;GH&quot;</strong> un atgriež <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (ievade)</td>
<td>Atgriezt norādīto ievadi, kas ir pārveidota par teksta virkni, kura ir formatēta atbilstoši pašreizējāsDynamics 365 for Operations instances servera lokalizācijas iestatījumiem. Vērtībām ar tipu <strong>real</strong> šīs virknes pārveidošana ir ierobežota līdz diviem cipariem aiz komata.</td>
<td>Ja ir norādīta Dynamics 365 for Operations instances servera lokalizācija <strong>EN-US</strong>, funkcija <strong>TEXT (NOW ())</strong> atgriež pašreizējās Dynamics 365 for Operations sesijas datumu 12.17.2015. kā teksta virkni <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEXT (1/3)</strong> atgriež <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (1. virkne, 2. virkne[, 3. virkne, ...])</td>
<td>Atgriezt norādīto virkni, kas ir formatēta, visus <strong>%N</strong> gadījumus aizstājot ar <em>n</em>-to argumentu. Argumenti ir virknes. Ja nav norādīts parametra arguments, šis parametrs virknē tiek atgriezts kā <strong>&quot;%N&quot;</strong>. Vērtībām ar tipu <strong>real</strong> šīs virknes pārveidošana ir ierobežota līdz diviem cipariem aiz komata.</td>
<td>Šajā piemērā datu avots <strong>PaymentModel</strong> atgriež sarakstu ar debitoru ierakstiem, izmantojot komponentu <strong>Customer</strong>, un apstrādāšanas datuma vērtību, izmantojot lauku <strong>ProcessingDate</strong>. <a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a> ER formātā, kas ir izstrādāts, lai ģenerētu elektronisku failu noteiktiem debitoriem, kā datu avots ir atlasīts elements <strong>PaymentModel</strong>, un tas kontrolē procesa plūsmu. Izņēmums lietotājiem tiek parādīts, kad atlasītais debitors tiek apturēts datumam, kad atskaite tiek apstrādāta. Šāda tipa apstrādes kontrolei izveidotā formulā var izmantot šādus resursus:
<ul>
<li>Dynamics 365 for Operations etiķete SYS70894, kurā ir šāds teksts:
<ul>
<li><strong>Valodai EN-US:</strong> &quot;Nothing to print&quot;</li>
<li><strong>Valodai DE:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Dynamics 365 for Operations etiķete SYS18389, kurā ir šāds teksts:
<ul>
<li><strong>Valodai EN-US:</strong> &quot;Customer %1 is stopped for %2.&quot;</li>
<li><strong>Valodai DE:</strong> &quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
Tālāk ir norādīta izstrādājamā formula. FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;)) Ja 2015. gada 17. decembrī tiek apstrādāta atskaite par debitoru <strong>Litware Retail customer</strong>, izmantojot kultūru <strong>EN-US</strong> un valodu <strong>EN-US</strong>, šī formula atgriež tālāk norādīto tekstu, kas var tikt parādīts lietotajam kā izņēmuma ziņojums. &quot;Nothing to print. Customer Litware Retail is stopped for 12/17/2015.&quot; Ja 2015. gada 17. decembrī tiek apstrādāta tā pati atskaite par debitoru <strong> Litware Retail customer</strong>, izmantojot kultūru <strong>DE</strong> un valodu <strong>DE</strong>, šī formula atgriež tālāk norādīto tekstu, kurā tiek izmantots cits datuma formāts. &quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot; <strong>Piezīme. </strong>ER formulās etiķetēm tiek lietota šāda sintakse:
<ul>
<li><strong>Etiķetēm no Dynamics 365 for Operations resursiem:</strong> <strong>@&quot;X&quot;</strong>, kur X ir etiķetes ID lietojumprogrammas objektu kokā (AOT)</li>
<li><strong>Etiķetēm, kas ir ietvertas ER konfigurācijās:</strong> <strong>@&quot;ER_LABEL:X&quot;</strong>, kur X ir etiķetes ID ER konfigurācijā</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (skaitlis, formāts)</td>
<td>Atgriezt norādītā skaitļa virknes attēlojumu norādītajā formātā. (Informāciju par atbalstītajiem formātiem skatiet šeit: <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standarta</a> un <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">pielāgotie</a>.) Formāta numuriem izmantotā kultūra ir atkarīga no šīs funkcijas izpildes konteksta.</td>
<td>Kultūrai EN-US <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> atgriež <strong>&quot;45.00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> atgriež <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (skaitlis, valoda, valūta, drukas valūtas nosaukuma karogs, cipari aiz komata)</td>
<td>Atgriež vārdos izteiktu (konvertētu) skaitli kā teksta virknes definētajā valodā. Valodas kods nav obligāts: ja tas ir definēts kā tukša virkne, tā vietā tiek lietots darbinātais konteksta valodas kods (definēts ģenerēšanas mapei vai failam). Valūtas kods nav obligāts. Ja tas ir definēts kā tukša virkne, tiek ņemta uzņēmuma valūta. Ievērojiet, parametrs <strong>Drukāt valūtas nosaukumu</strong> un parametrs <strong>Cipari aiz komata</strong> tiek analizēti tikai šādiem valodu kodiem: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, <strong>RU</strong>. Ievērojiet, parametrs <strong>Drukāt valūtas nosaukumu</strong> tiek analizēts tikai tiem Dynamics 365 for Operations uzņēmumiem, kuru valsts konteksts atbalsta valūtas locījumus.</td>
<td>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2) atgriež “One Thousand Two Hundred Thirty Four and 56” NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0) atgriež “Sto dwadzieścia” NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2) atgriež “Сто двадцать евро 21 евроцент”</td>
</tr>
<tr class="odd">
<td>PADLEFT (virkne, garums, papildināšanas rakstzīmes)</td>
<td>Atgriež noteikta garuma virkni, kurā pašreizējās virknes sākumā ir ievadītas norādītās rakstzīmes.</td>
<td>PADLEFT (“1234”, 10, “ “) atgriež teksta virkni “      1234”</td>
</tr>
</tbody>
</table>

### <a name="data-collection-functions"></a>Datu apkopošanas funkcijas

Funkcija

Apraksts

Paraugs

FORMATELEMENTNAME ()

Tiek atgriezts pašreizējā formāta elementa nosaukums. Atgriež tukšu virkni, ja pašreizējo failu karogs **Apkopot izvades informāciju** ir izslēgts.

Lai uzzinātu papildinformāciju par šo funkciju lietojumu, skatiet uzdevuma ceļvedi **ER Lietot formāta izvades datus uzskaitei un summēšanai** (daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**).

SUMIFS (galvenā virkne summēšanai, kritēriju 1. diapazona virkne, kritēriju 1. vērtības virkne \[, kritēriju 2. diapazona virkne, kritēriju 2. vērtības virkne, …\])

Atgriež zaru vērtību summu (ar nosaukumu, kas definēts kā atslēga) no XML, kas ir savākts šī formāta izpildes laikā un apmierina ievadītos nosacījumus (diapazona un vērtības pārus). Atgriež nulles vērtību, ja pašreizējo failu karogs **Apkopot izvades informāciju**ir izslēgts.

SUMIF (atslēgu virkne summēšanai, kritēriju diapazona virkne, kritēriju vērtību virkne)

Atgriež zaru vērtību summu (ar nosaukumu, kas definēts kā atslēga) no XML, kas ir savākts šī formāta izpildes laikā un apmierina ievadīto nosacījumu (diapazonu un vērtību). Atgriež nulles vērtību, ja pašreizējo failu karogs **Apkopot izvades informāciju** ir izslēgts.

COUNTIFS (kritēriju 1. diapazona virkne, kritēriju 1. vērtības virkne \[, kritēriju 2. diapazona virkne, kritēriju 2. vērtības virkne, …\])

Atgriež zaru skaitu no XML, kas ir savākts šī formāta izpildes laikā un apmierina ievadītos nosacījumus (diapazona un vērtības pārus). Atgriež nulles vērtību, ja pašreizējo failu karogs **Apkopot izvades informāciju** ir izslēgts.

COUNTIF (kritēriju diapazona virkne, kritēriju vērtību virkne)

Atgriež zaru skaitu no XML, kas ir savākts šī formāta izpildes laikā un apmierina ievadīto nosacījumu (diapazonu un vērtību). Atgriež nulles vērtību, ja pašreizējo failu karogs **Apkopot izvades informāciju** ir izslēgts.

COLLECTEDLIST (kritēriju 1. diapazona virkne, kritēriju 1. vērtības virkne \[, kritēriju 2. diapazona virkne, kritēriju 2. vērtības virkne, …\])

Atgriež zaru vērtību sarakstu no XML, kas ir savākts šī formāta izpildes laikā un apmierina ievadītos nosacījumus (diapazonu un vērtību). Atgriež tukšu sarakstu, ja pašreizējo failu karogs **Apkopot izvades informāciju**ir izslēgts.

### <a name="other-business-domainspecific-functions"></a>Citas (biznesa jomai specifiskas) funkcijas

| Funkcija                                                                         | apraksts                                                                                                                                                                                                                                                        | Piemērs                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (summa, avota valūta, mērķa valūta, datums, uzņēmums)        | Norādīto naudas summu no avota valūtas konvertēt mērķa valūtā, izmantojot norādītā Dynamics 365 for Operations uzņēmuma iestatījumus norādītajā datumā.                                                                            | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** atgriež viena eiro ekvivalentu ASV dolāros pašreizējās sesijas datumā, balstoties uz uzņēmuma DEMF iestatījumiem.                                                                                                                                  |
| ROUNDAMOUNT (skaitlis, cipari aiz komata, noapaļošanas kārtula)                                       | Norādīto summu noapaļot atbilstoši norādītajai noapaļošanas kārtulai un norādītajam ciparu skaitam aiz komata. **Piezīme.** Noapaļošanas kārtula ir jānorāda kā Dynamics 365 for Operations uzskaitījums **RoundOffType**.                          | Ja ir iestatīta parametra **model.RoundOff** vērtība ****Downward****, funkcija **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** atgriež vērtību **1000.78**. Ja parametrs **model.RoundOff** ir iestatīts uz **Normal** vai uz **Rounding-up**, tad **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** atgriež vērtību **1000.79**. |
| CURCredRef (cipari)                                                              | Atgriezt kreditora atsauci, pamatojoties uz norādītā rēķina numura cipariem.                                                                                                                                                                                  | **CURCredRef ("VEND-200002")** atgriež **"2200002"**.                                                                                                                                                                                                                                                         |
| MOD\_97 (cipari)                                                                 | Atgriezt kreditora atsauci kā MOD97 izteiksmi, pamatojoties uz norādītā rēķina numura cipariem.                                                                                                                                                            | **MOD\_97 ("VEND-200002")** atgriež **"20000285"**.                                                                                                                                                                                                                                                           |
| ISOCredRef (cipari)                                                              | Atgriezt ISO kreditora atsauci, pamatojoties uz norādītā rēķina numura cipariem un burtiem. **Piezīme.**Lai izslēgtu alfabētu simbolus, kas nesader ar ISO, šo ievades parametru ir nepieciešams tulkot, pirms to nodod šai funkcijai. | **ISOCredRef ("VEND-200002")** atgriež **"RF23VEND-200002"**.                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (virkne, skaitlis)                                  | Iegūt papildu finanšu dimensijas ID. Dimensijas šajā virknē tiek attēlotas kā ar komatiem atdalīti ID. Numuri šajā virknē definē pieprasītās dimensijas sērijas kodu.                                                                            | CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3) atgriež “CC”                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Atgriež kodu uzņēmumam, kurā lietotājs ir pieteicies pašlaik.                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                               |
| CH\_BANK\_MOD\_10 (cipari)                                                       | Atgriež kreditora atsauci kā MOD10 izteiksmi, pamatojoties uz norādīto rēķina numuru.                                                                                                                                                                      | CH\_BANK\_MOD\_10 ("VEND-200002") atgriež 3                                                                                                                                                                                                                                                                   |
| FA\_SUM (pamatlīdzekļa kods, vērtības modeļa kods, sākuma datums, beigu datums)               | Atgriež sagatavoto perioda pamatlīdzekļu summu datu konteineru.                                                                                                                                                                                         | FA\_SUM ("COMP-000001", “Current”, Date1, Date2) atgriež sagatavoto datu konteineru pamatlīdzeklim “COMP-000001” ar vērtības modeli “Current” par periodu no Date1 līdz Date2.                                                                                                                        |
| FA\_BALANCE (pamatlīdzekļa kods, vērtības modeļa kods, pārskata gads, pārskata datums) | Atgriež sagatavoto pamatlīdzekļa bilanču datu konteineru. Pārskata gads ir jānorāda kā Dynamics 365 for Operations uzskaitījuma **AssetYear** vērtība.                                                                                           | FA\_SUM ("COMP-000001", “Current”, AxEnumAssetYear.ThisYear, SESSIONTODAY ()) atgriež sagatavoto datu konteineru no bilancēm pamatlīdzeklim “COMP-000001” ar vērtības modeli “Current” pašreizējā Dynamics 365 for Operations sesijas datumā.                                                                |

### <a name="functions-list-extension"></a>Funkciju saraksta paplašināšana

ER jums ļauj paplašināt funkciju sarakstu, kuras tiek lietotas ER izteiksmēs. Ir nepieciešamas dažas tehniskas pūles. Papildinformāciju skatiet rakstā [Elektronisko atskaišu veidošanas funkciju saraksta paplašināšana](general-electronic-reporting-formulas-list-extension.md).

<a name="see-also"></a>Skatiet arī
--------

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Paplašināt elektronisko pārskatu veidošanas (ER) funkciju sarakstu](general-electronic-reporting-formulas-list-extension.md)




