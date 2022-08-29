---
title: Regression Suite Automation Tool apmācība
description: Šajā rakstā ir parādīts, kā izmantot regresīcijas komplekta automatizācijas rīku (RSAT). Tajā ir aprakstīti dažādi līdzekļi un sniegti piemēri, kuros izmantota papildu skriptēšana.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: a270398ddebef0f47a2c31b0ffb022e3df6489c7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277410"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool apmācība

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Izmantojiet interneta pārlūka rīkus, lai lejupielādētu un saglabātu šo lapu PDF formātā.

Šajā apmācībā ir aprakstīti daži Regression Suite Automation Tool (RSAT) papildu līdzekļi, ietverta demonstrācijas piešķire un aprakstīta stratēģija un galvenās mācību tēmas.

## <a name="notable-features-of-rsat-and-task-recorder"></a>Ievērojami RSAT un uzdevumu reģistrētāja līdzekļi

### <a name="validate-a-field-value"></a>Lauka vērtības validēšana

RSAT ļauj iekļaut pārbaudes soļus jūsu pārbaudes gadījumā, lai validētu paredzētās vērtības. Lai iegūtu vairāk informācijas par šo līdzekli, skatiet rakstu [Pārbaudīt paredzētās vērtības](rsat-validate-expected.md).

Tālāk norādītajā piemērā ir parādīts, kā varat izmantot šo līdzekli, lai pārbaudītu, vai rīcībā esošo krājumu daudzums ir vairāk nekā 0 (nulle).

1. Demonstrācijas datos uzņēmumā **USMF** izveidojiet uzdevuma ierakstu, kurā ir tālāk norādītās darbības.

    1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
    2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka **Krājuma numurs**, izmantojot vērtību **1000**.
    3. Atlasiet **Rīcībā esošie krājumi**.
    4. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka **Vieta**, izmantojot vērtību **1**.
    5. Sarakstā atzīmējiet atlasīto rindu.
    6. Pārbaudiet, vai lauka **Pieejamā kopsumma** vērtība ir **411.0000000000000000**.

2. Saglabājiet uzdevuma ierakstu kā izstrādātāja **ierakstu** un pievienojiet to testa gadījumam Azure DevOps.
3. Pievienojiet testa gadījumu testa plānam un ielādējiet testa gadījumu RSAT.
4. Atveriet Excel parametra failu un dodieties uz cilni **TestCaseSteps**.
5. Lai pārbaudītu, vai rīcībā esošie krājumi vienmēr būs vairāk par **0**, dodieties uz soli **Pārbaudīt kopējo pieejamo** un mainiet tā vērtību no **411** uz **0**. Mainiet **Operatora** lauka vērtību no vienādības zīmes (**=**) uz lielāku par zīmi (**\>**).
6. Saglabājiet un aizveriet Excel parametru failu.
7. Atlasiet **Augšupielādēt**, lai saglabātu izmaiņas, kuras veicāt Excel parametru failā, pakalpojumā Azure DevOps.

Ja tagad lauka **Pieejamā kopsumma** vērtība norādītajam vienumam krājumā ir lielāka par 0 (nulli), testi būs sekmīgi neatkarīgi no faktiskās rīcībā esošo krājumu vērtības.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Saglabātie mainīgie un testa gadījumu ķēde

Viens no RSAT svarīgākajiem līdzekļiem ir testa gadījumu savienošana ķēdē, tas ir, iespēja nodot testa mainīgos citiem testiem. Lai iegūtu papildinformāciju, skatiet rakstu [Mainīgo kopēšana uz ķēdes testa gadījumiem](rsat-chain-test-cases.md).

### <a name="derived-test-case"></a>Atvasināts testa gadījums

RSAT ļauj izmantot vienu un to pašu uzdevuma reģistrēšanu ar vairākiem pārbaudes gadījumiem, iespējojot uzdevumu darbināt ar atšķirīgām datu konfigurācijām. Papildinformācijai skatiet rakstu [Iegūtie testa gadījumi](rsat-derived-test-cases.md).

### <a name="validate-notifications-and-messages"></a>Pārbaudīt paziņojumus un ziņas

Šo funkciju var izmantot, lai pārbaudītu, vai darbība ir notikusi. Piemēram, kad tiek izveidots un pēc tam sākts ražošanas pasūtījums, programma parāda ziņojumu “Ražošana — Sākums”, lai informētu, ka ražošanas pasūtījums ir sākts.

![Paziņojums Ražošana — Sākums.](./media/use_rsa_tool_05.png)

Šo ziņojumu varat validēt ar RSAT, ievadot ziņojuma tekstu atbilstošā ieraksta Excel parametru faila cilnē **MessageValidation**.

![Ziņojuma validēšanas cilne.](./media/use_rsa_tool_06.png)

Pēc testa gadījuma palaišanas ziņojums Excel parametru failā tiek salīdzināts ar ziņojumu, kas tiek parādīts programmā. Ja ziņojumi nesakrīt, testa gadījums ir nesekmīgs.

> [!NOTE]
> Excel parametru faila cilnē **MessageValidation** varat ievadīt vairāk nekā vienu ziņojumu. Ziņojumi var būt arī kļūdu vai brīdinājuma ziņojumi, nevis informācijas ziņojumi.

### <a name="snapshot"></a>Momentuzņēmums

Šis līdzeklis uzņem to darbību ekrānuzņēmumus, kas tika izpildītas uzdevuma reģistrēšanas laikā. Tas ir noderīgs audita vai atkļūdošanas nolūkiem.

- Lai izmantotu šo līdzekli, atveriet failu **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**, kas atrodas RSAT instalācijas mapē (piemēram, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), un mainiet tālāk norādītā elementa vērtību no **aplams** uz **patiess**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- Lai izmantotu šo līdzekli RSAT darbības laikā, ko palaida CLI (piemēram, Azure DevOps), atveriet failu **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config**, kas atrodas RSAT instalācijas mapē (piemēram, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), un mainiet tālāk norādītā elementa vērtību no **aplams** uz **patiess**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Palaižot pārbaudes gadījumus, RSAT izveido soļu momentuzņēmumus (attēlus) un saglabā tos darba direktorijā esošo pārbaudes gadījumu mapē. Atskaņošanas mapē tiek izveidota atsevišķa apakšmape ar nosaukumu **StepSnapshots**. Mape satur momentuzņēmumus palaistiem pārbaudes gadījumiem.

## <a name="assignment"></a>Piešķire

### <a name="scenario"></a>Scenārijs

1. Preču noformētājs izveido jaunu izlaisto preci.
2. Ražošanas pārvaldnieks uzsāk ražošanas pasūtījumu, lai palielinātu krājumu līmeni līdz diviem gabaliem.
3. Ražošana sāk un beidz ražošanas pasūtījumu un pārbauda, vai rīcībā esošais daudzums ir divi gabali.
4. Pārdošanas grupa saņem četru jaunās preces gabalu pasūtījumu. Tāpēc pārdošanas grupa atjaunina neto vajadzības, izmantojot dinamisko plānu. Papildu noslodze nav pieejama, tādēļ noklusētā pasūtījuma politika ir iestatīta uz “pirkt, nevis izgatavot”. Tādēļ tiek izveidots plānotais pirkšanas pasūtījums.
5. Pircējs pievieno kreditoru, apstiprina plānoto pirkšanas pasūtījumu un pēc tam apstiprina pirkšanas pasūtījumu.
6. Kad nopirktās preces nonāk veikalā, veikala operators meklē saistīto pirkšanas pasūtījumu un saņem preces. Tagad pasūtījums ir pabeigts, tādēļ preces var tikt izdotas un iepakotas, salīdzinot ar pārdošanas pasūtījumu.
7. Finance iegrāmato pirkšanas rēķinu un pārdošanas rēķinu.

Tālāk redzamajā attēlā ir parādīta šī scenārija plūsma.

![Demonstrācijas scenārija plūsma.](./media/use_rsa_tool_14.png)

Sekojošajā attēlā redzama biznesa procesu hierarhija šim scenārijam LCS biznesa procesu modelētājā.

![Demonstrācijas scenārija biznesa procesi.](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Stratēģija — galvenās mācību tēmas

### <a name="data"></a>Dati

- Pārliecinieties, ka jums ir reprezentatīvi datu apjomi (ražošanas/zelta konfigurācijas datu kopija un migrētie dati).
- Kad ģenerējat jaunus datus, izmantojot uzdevuma reģistrētāju, izveidojiet testa nosaukumus, kas nekonfliktē ar esošiem nosaukumiem (piemēram, izmantojiet prefiksu **RSATxxx**).
- Izmantojiet Azure punkta laikā atjaunošanu, lai atkārtoti palaistu testus vidēs, kas nav 1. līmeņa vides.
- Lai ģenerētu unikālu kombināciju, varat izmantot Excel funkcijas **RANDOM** un **NOW**, tomēr būs jāiegulda ievērojamas pūles. Tālāk ir minēts piemērs.

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>Uzdevumu reģistrētājs

- Pirms ierakstīšanas sākšanas definējiet scenārijus. Labi pārvaldītam projektam ir iepriekš definēti testa scenāriji. Lai izveidotu testa gadījumu, apsveriet, cik prognozējams ir šo testa scenāriju rezultāts.
- Sadaliet ierakstus, ja tos izpilda dažādas lomas vai ja pirms nākamās darbības ir gaidīšanas laiks vai ārējs notikums.
- Neatlasiet vērtības sarakstos. Tā vietā izmantojiet teksta formātus, piemēram, **FIFO**, **AudioRM** un **SiteWH**. Atlasot sarakstā, tiek ierakstīta vērtības pozīcija sarakstā, nevis pati vērtība. Ja šim sarakstam tiek pievienoti krājumi, vērtības pozīcija var mainīties. Tādēļ ierakstam tiks izmantots cits parametrs, un var tikt ietekmēta pārējā scenārija daļa.
- Ņemiet vērā, ka var būt vairāki lietotāji. Piemēram, nepieņemiet, ka jaunizveidotais pārdošanas pasūtījums vienmēr tiks atlasīts automātiski. Tā vietā vienmēr izmantojiet filtru, lai atrastu pareizo pasūtījumu.
- Tikko izveidotas preces nosaukuma saglabāšanai izmantojiet uzdevumu ierakstītāja kopēšanas funkciju, lai varētu to izmantot savienotos testa gadījumos.
- Lietojiet uzdevumu ierakstītāja funkciju Validēt, lai iestatītu kontrolpunktus, kas pārbauda, vai darbības ir pareizi izpildītas.

### <a name="rsat"></a>RSAT

- Lai palaistu testu citā uzņēmumā, varat nomainīt uzņēmumu Excel parametru faila cilnē **Vispārīgi**. Pārliecinieties, ka iestatījumi un dati nesen atlasītajā uzņēmumā ir pieejami.
- Varat mainīt testa lietotāju Excel parametru faila cilnē **Vispārīgi**. Norādiet tā lietotāja e-pasta ID, kurš izpildīs testa gadījumu. Šādā veidā testu var izpildīt, izmantojot norādītā lietotāja drošības atļaujas.
- Lai nogaidītu pirms testa sākšanas, varat noteikt pauzi Excel parametru faila cilnē **Vispārīgi**. Šo pauzi var izmantot pakešuzdevumā (piemēram, ja darbplūsma ir jāizpilda, pirms var izpildīt nākamo darbību.)

## <a name="advanced-scripting"></a>Papildu skriptēšana

### <a name="cli"></a>CLI

RSAT var izsaukt no **Komandu uzvednes** vai **PowerShell** loga.

> [!NOTE]
> Pārbaudiet, vai vides mainīgajam **TestRoot** ir iestatīts RSAT instalācijas ceļš. (Operētājsistēmā Microsoft Windows atveriet **Vadības panelis**, atlasiet **Sistēma un drošība \> Sistēma \> Sistēmas papildiestatījumi** un pēc tam atlasiet **Vides mainīgie**.)

1. Atveriet **Komandu uzvednes** vai **PowerShell** logu kā administrators.
2. Dodieties uz RSAT instalācijas direktoriju.

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Attēlojiet visas komandas saraksta veidā.

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Uzskaita visas komandas vai parāda palīdzību noteiktai komandai kopā ar pieejamajiem parametriem.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Neobligāti parametri

`command`: kur ``[command]`` ir viena no komandām iepriekšējā sarakstā.

#### <a name="about"></a>par programmu

Parāda instalētā RSAT versiju.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Notīra ekrānu.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>lejupielādēt

Lejupielādē pielikumus (ierakstīšanas, izpildes un parametru failus) norādītajam testa gadījumam no Azure DevOps izvades direktorijas. Varat izmantot komandu, ``list`` lai iegūtu visus pieejamos testa gadījumus, un izmantot jebkuru vērtību no pirmās kolonnas kā **test_case_id parametru**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>lejupielāde: izvēles pārslēgšanās

+ `/retry[=seconds]`: Ja ir norādīta šī pārslēgšanās un gadījumu pārbaudes gadījumus bloķē citas RSAT instances, lejupielādes process gaidīs norādīto sekunžu skaitu un tad mēģinās vēlreiz. Noklusējuma sekunžu \[vērtība\] ir 120 sekundes. Bez šī pārslēgšanas, nekavējoties tiks atcelts process, ja testa gadījumi ir bloķēti.

##### <a name="download-required-parameters"></a>lejupielāde: obligātie parametri

+ `test_case_id`: Parāda testa gadījuma ID.

##### <a name="download-optional-parameters"></a>lejupielāde: izvēles parametri

+ `output_dir`: attēlo izvades darba direktoriju. Direktorijam ir jāpastāv. Ja nav norādīts šis parametrs, tiks lietots darba direktorijs no iestatījumiem.

##### <a name="download-examples"></a>lejupielāde: piemēri

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>Lejupielādes darbības

Lejupielādē pielikumus (ierakstīšanas, izpildes un parametru failus) visiem testa gadījumiem norādītajā testu komplektā no Azure DevOps izvades direktorijas. Varat izmantot komandu ``listtestsuitenames``, lai iegūtu visu pieejamo testa darbību un izmantot jebkuru vērtību kā test_suite_name **parametru**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>lejupielādes: neobligātie pārslēgšanās

+ `/retry[=seconds]`: Ja ir norādīta šī pārslēgšanās un gadījumu pārbaudes gadījumus bloķē citas RSAT instances, lejupielādes process gaidīs norādīto sekunžu skaitu un tad mēģinās vēlreiz. Noklusējuma sekunžu \[vērtība\] ir 120 sekundes. Bez šī pārslēgšanas, nekavējoties tiks atcelts process, ja testa gadījumi ir bloķēti.
+ `/byid`: šis pārslēgšanās norāda, ka vēlamais testa komplekts ir identificēts pēc Azure DevOps tā ID, nevis testa komplekta nosaukuma.

##### <a name="downloadsuite-required-parameters"></a>Lejupielādes laiks: obligātie parametri

+ `test_suite_name`: Parāda testa komplekta nosaukumu. Šis parametrs ir nepieciešams, ja nav norādīts **/byid slēdzis**. Šis nosaukums ir testa Azure DevOps komplekta nosaukums.
+ `test_suite_id`: Parāda testa komplekta ID. Šis parametrs ir nepieciešams, ja ir norādīta /byid **pārslēgšanās**. Šis ID ir testa komplekta Azure DevOps ID.

##### <a name="downloadsuite-optional-parameters"></a>downloadlejupielādē: neobligātie parametri

+ `output_dir`: attēlo izvades darba direktoriju. Direktorijam ir jāpastāv. Ja nav norādīts šis parametrs, tiks lietots darba direktorijs no iestatījumiem.

##### <a name="downloadsuite-examples"></a>Downloadlejupielādē — piemēri

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>rediģēt

Ļauj atvērt parametru failu Excel programmā un to rediģēt.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>rediģēt: obligātie parametri

+ `excel_file`: Ir jāietver pilns ceļš uz esošu Excel failu.

##### <a name="edit-examples"></a>rediģēt: piemēri

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>ģenerēt

Ģenerē pārbaudes izpildi un parametru failus norādītajam testa gadījumam izvades direktorijā. Varat izmantot ``list`` komandu, lai iegūtu visus pieejamos pārbaudes gadījumus. Izmantojiet jebkuru vērtību no pirmās kolonnas kā **test_case_id** parametru.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>ģenerēt: izvēles pārslēgšanās

+ `/retry[=seconds]`: ja ir norādīts šis slēdzis un gadījumu pārbaudes gadījumus bloķē citas RSAT instances, ģenerēšanas process gaidīs norādīto sekunžu skaitu un pēc tam izmēģinās vairāk laika. Noklusējuma sekunžu \[vērtība\] ir 120 sekundes. Bez šī pārslēgšanas, nekavējoties tiks atcelts process, ja testa gadījumi ir bloķēti.
+ `/dllonly`: ģenerēt tikai testa izpildes failus. Neģenerēt Excel parametru failu.
+ `/keepcustomexcel`: jauniniet esošo parametru failu. Reģenerēt arī izpildes failus.

##### <a name="generate-required-parameters"></a>ģenerēt: nepieciešamos parametrus

+ `test_case_id`: Parāda testa gadījuma ID.

##### <a name="generate-optional-parameters"></a>ģenerēt: izvēles parametrus

+ `output_dir`: attēlo izvades darba direktoriju. Direktorijam ir jāpastāv. Ja nav norādīts šis parametrs, tiks lietots darba direktorijs no iestatījumiem.

##### <a name="generate-examples"></a>ģenerēt: piemēri

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

Ģenerē jaunu atvasinātā testa gadījumu (atvasinātā testa gadījums) no sniegtā testa gadījuma. Jaunais testa gadījums tiek pievienots arī norādītajam testa komplektam. Varat izmantot komandu, ``list`` lai iegūtu visus pieejamos testa gadījumus, un izmantot jebkuru vērtību no pirmās kolonnas kā **test_case_id parametru**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>ģenerēts: neobligātie pārslēdzēji

+ `/retry[=seconds]`: ja ir norādīts šis slēdzis un gadījumu pārbaudes gadījumus bloķē citas RSAT instances, ģenerēšanas process gaidīs norādīto sekunžu skaitu un pēc tam izmēģinās vairāk laika. Noklusējuma sekunžu \[vērtība\] ir 120 sekundes. Bez šī pārslēgšanas, nekavējoties tiks atcelts process, ja testa gadījumi ir bloķēti.

##### <a name="generatederived-required-parameters"></a>generatederived: nepieciešamos parametrus

+ `parent_test_case_id`: Parāda vecāka pārbaudes gadījuma ID.
+ `test_plan_id`: Parāda testa plāna ID.
+ `test_suite_id`: Parāda testa komplekta ID.

##### <a name="generatederived-examples"></a>generatederived: piemēri

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Ģenerē tikai testa izpildes failus norādītajam testa gadījumam. Tas neģenerē Excel parametru failu. Faili tiek ģenerēti norādītajā izvades direktorijā. Varat izmantot komandu, ``list`` lai iegūtu visus pieejamos testa gadījumus, un izmantot jebkuru vērtību no pirmās kolonnas kā **test_case_id parametru**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>ģenerēti: neobligātie pārslēdzēji

+ `/retry[=seconds]`: ja ir norādīts šis slēdzis un gadījumu pārbaudes gadījumus bloķē citas RSAT instances, ģenerēšanas process gaidīs norādīto sekunžu skaitu un pēc tam izmēģinās vairāk laika. Noklusējuma sekunžu \[vērtība\] ir 120 sekundes. Bez šī pārslēgšanas, nekavējoties tiks atcelts process, ja testa gadījumi ir bloķēti.

##### <a name="generatetestonly-required-parameters"></a>generatesonly: nepieciešamos parametrus

+ `test_case_id`: Parāda testa gadījuma ID.

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: izvēles parametri

+ `output_dir`: attēlo izvades darba direktoriju. Direktorijam ir jāpastāv. Ja nav norādīts šis parametrs, tiks lietots darba direktorijs no iestatījumiem.

##### <a name="generatetestonly-examples"></a>generatesonly: piemēri

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

Ģenerē testa automatizācijas failus visiem testa gadījumiem norādītajā testu komplektā. Varat izmantot komandu ``listtestsuitenames``, lai iegūtu visu pieejamo testa darbību un izmantot jebkuru vērtību kā test_suite_name **parametru**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>Generatetest pārskata: neobligātie pārslēdzēji

+ `/retry[=seconds]`: ja ir norādīts šis slēdzis un gadījumu pārbaudes gadījumus bloķē citas RSAT instances, ģenerēšanas process gaidīs norādīto sekunžu skaitu un pēc tam izmēģinās vairāk laika. Noklusējuma sekunžu \[vērtība\] ir 120 sekundes. Bez šī pārslēgšanas, nekavējoties tiks atcelts process, ja testa gadījumi ir bloķēti.
+ `/dllonly`: ģenerēt tikai testa izpildes failus. Neģenerēt Excel parametru failu.
+ `/keepcustomexcel`: jaunināt esošo parametru failu. Reģenerēt arī izpildes failus.
+ `/byid`: šis pārslēgšanās norāda, ka vēlamais testa komplekts ir identificēts pēc Azure DevOps tā ID, nevis testa komplekta nosaukuma.

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: nepieciešamos parametrus

+ `test_suite_name`: Parāda testa komplekta nosaukumu. Šis parametrs ir nepieciešams, ja nav norādīts **/byid slēdzis**. Šis nosaukums ir testa Azure DevOps komplekta nosaukums.
+ `test_suite_id`: Parāda testa komplekta ID. Šis parametrs ir nepieciešams, ja ir norādīta /byid **pārslēgšanās**. Šis ID ir testa komplekta Azure DevOps ID.

##### <a name="generatetestsuite-optional-parameters"></a>Generatetest pārskata: neobligātie parametri

+ `output_dir`: attēlo izvades darba direktoriju. Direktorijam ir jāpastāv. Ja nav norādīts šis parametrs, tiks lietots darba direktorijs no iestatījumiem.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: piemēri

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>palīdzība

Identisks ar [?](#section) komanda.

#### <a name="list"></a>saraksts

Uzskaita visus pieejamos testa gadījumus pašreizējā pārbaudes plānā.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Uzskaita visus pieejamos pārbaudes plānus.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Uzskaita testa gadījumus norādītajam testu komplektam. Varat izmantot komandu ``listtestsuitenames``, lai iegūtu visu pieejamo testa darbību, un izmantot jebkuru vērtību no saraksta kā **suite_name parametru**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: nepieciešamie parametrus

+ `test_suite_name`: nepieciešamā komplekta nosaukums.

##### <a name="listtestsuite-examples"></a>listtestsuite: piemēri

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestbilibyid

Uzskaita testa gadījumus norādītajam testu komplektam.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestbilibyid: obligātie parametri

+ `test_suite_id`: nepieciešamā komplekta ID.

##### <a name="listtestsuitebyid-examples"></a>listtestbilibyid: piemēri

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Uzskaita visus pieejamos testa uzdevumu šajā pārbaudes plānā.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>atskaņošana

Atgriežas testa gadījums, kas ir saistīts ar norādīto Excel parametru failu. Šī komanda izmanto esošos lokālās automatizācijas failus un nelejupielādē failus Azure DevOps no. Šī komanda netiek atbalstīta POS Commerce pārbaudes gadījumiem.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>: izvēles pārslēgšanās

+ `/retry[=seconds]`: Ja ir norādīts šis slēdzis un gadījumu pārbaudes gadījumus bloķē citas RSAT instances, failu process gaidīs norādīto sekunžu skaitu un pēc tam izmēģinās vēl vienu reizi. Noklusējuma sekunžu \[vērtība\] ir 120 sekundes. Bez šī pārslēgšanas, nekavējoties tiks atcelts process, ja testa gadījumi ir bloķēti.
+ `/comments[="comment"]`: sniegt pielāgotu informācijas virkni, kas tiks ietverta laukā **Komentāri** kopsavilkuma un testa rezultātu lapās testa Azure DevOps gadījuma izpildes laikā.

##### <a name="playback-required-parameters"></a>atskaņošana: obligātie parametri

+ `excel_parameter_file`: Excel parametru faila pilns ceļš. Failam ir jāpastāv.

##### <a name="playback-examples"></a>atskaņošana: piemēri

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Vienlaicīgi tiek atgūti vairāki testa gadījumi. Testa gadījumi tiek identificēti pēc to ID. Šī komanda lejupielādēs failus no Azure DevOps. Varat izmantot komandu ``list``, lai iegūtu visus pieejamos testa gadījumus, un izmantot jebkuru vērtību no pirmās kolonnas kā test_case_id **parametru**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>Tikai <a0/&; neobligātie pārslēdzēji

+ `/retry[=seconds]`: Ja ir norādīts šis slēdzis un gadījumu pārbaudes gadījumus bloķē citas RSAT instances, failu process gaidīs norādīto sekunžu skaitu un pēc tam izmēģinās vēl vienu reizi. Noklusējuma sekunžu \[vērtība\] ir 120 sekundes. Bez šī pārslēgšanas, nekavējoties tiks atcelts process, ja testa gadījumi ir bloķēti.
+ `/comments[="comment"]`: sniegt pielāgotu informācijas virkni, kas tiks ietverta laukā **Komentāri** kopsavilkuma un testa rezultātu lapās testa Azure DevOps gadījuma izpildes laikā.

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: obligātie parametri

+ `test_case_id1`: esoša testa gadījuma ID.
+ `test_case_id2`: esoša testa gadījuma ID.
+ `test_case_idN`: esoša testa gadījuma ID.

##### <a name="playbackbyid-examples"></a>playbackbyid: piemēri

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Vienlaicīgi tiek atgūti daudzi testa gadījumi. Testa gadījumi tiek identificēti ar Excel parametru failiem. Šī komanda izmanto esošos lokālās automatizācijas failus un nelejupielādē failus Azure DevOps no.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>d. <a0/&; neobligātie pārslēdzēji

+ `/retry[=seconds]`: Ja ir norādīts šis slēdzis un gadījumu pārbaudes gadījumus bloķē citas RSAT instances, failu process gaidīs norādīto sekunžu skaitu un pēc tam izmēģinās vēl vienu reizi. Noklusējuma sekunžu \[vērtība\] ir 120 sekundes. Bez šī pārslēgšanas, nekavējoties tiks atcelts process, ja testa gadījumi ir bloķēti.
+ `/comments[="comment"]`: sniegt pielāgotu informācijas virkni, kas tiks ietverta laukā **Komentāri** kopsavilkuma un testa rezultātu lapās testa Azure DevOps gadījuma izpildes laikā.

##### <a name="playbackmany-required-parameters"></a>playbackbymany: obligātie parametri

+ `excel_parameter_file1`: Excel parametru faila pilns ceļš. Failam ir jāpastāv.
+ `excel_parameter_file2`: Excel parametru faila pilns ceļš. Failam ir jāpastāv.
+ `excel_parameter_fileN`: Excel parametru faila pilns ceļš. Failam ir jāpastāv.

##### <a name="playbackmany-examples"></a>playbackmany: piemēri

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Atbalsta visus testa gadījumus no vienas vai vairākām norādītām pārbaudes lietām. Ja ir norādīta lokālā pārslēgšanās, lokālie pielikumi tiks izmantoti iestatījumu saglabāšanai. Pretējā gadījumā pielikumi tiks lejupielādēti no Azure DevOps. Varat izmantot komandu ``listtestsuitenames``, lai iegūtu visu pieejamo testa darbību, un izmantot jebkuru vērtību no pirmās kolonnas kā **suite_name parametru**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>Paralē — neobligātie pārslēdzēji

+ `/updatedriver`: Ja ir norādīta šī pārslēgšanās, interneta pārlūkprogrammas webdrivers tiks atjaunināts pēc vajadzības pirms procesa sākšanas.
+ `/local`: šis pārslēgšanās norāda, ka tāpēc tāpēc, ka tā vietā, lai lejupielādētu failus no, ir jāizmanto lokālie pielikumi Azure DevOps.
+ `/retry[=seconds]`: Ja ir norādīts šis slēdzis un gadījumu pārbaudes gadījumus bloķē citas RSAT instances, failu process gaidīs norādīto sekunžu skaitu un pēc tam izmēģinās vēl vienu reizi. Noklusējuma sekunžu \[vērtība\] ir 120 sekundes. Bez šī pārslēgšanas, nekavējoties tiks atcelts process, ja testa gadījumi ir bloķēti.
+ `/comments[="comment"]`: sniegt pielāgotu informācijas virkni, kas tiks ietverta laukā **Komentāri** kopsavilkuma un testa rezultātu lapās testa Azure DevOps gadījuma izpildes laikā.
+ `/byid`: šis pārslēgšanās norāda, ka vēlamais testa komplekts ir identificēts pēc Azure DevOps tā ID, nevis testa komplekta nosaukuma.

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: obligātie parametri

+ `test_suite_name1`: Parāda testa komplekta nosaukumu. Šis parametrs ir nepieciešams, ja nav norādīts **/byid slēdzis**. Šis nosaukums ir testa Azure DevOps komplekta nosaukums.
+ `test_suite_nameN`: Parāda testa komplekta nosaukumu. Šis parametrs ir nepieciešams, ja nav norādīts **/byid slēdzis**. Šis nosaukums ir testa Azure DevOps komplekta nosaukums.
+ `test_suite_id1`: Parāda testa komplekta ID. Šis parametrs ir nepieciešams, ja ir norādīta /byid **pārslēgšanās**. Šis IR testa komplekta Azure DevOps ID.
+ `test_suite_idN`: Parāda testa komplekta ID. Šis parametrs ir nepieciešams, ja ir norādīta /byid **pārslēgšanās**. Šis IR testa komplekta Azure DevOps ID.

##### <a name="playbacksuite-examples"></a>playbacksuite: piemēri

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>Administratora id

Darbina visus testa gadījumus norādītajā testu Azure DevOps komplektā.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>Paralērs <a0/&a1>neobligātie pārslēgšanās<a

+ `/retry[=seconds]`: Ja ir norādīts šis slēdzis un gadījumu pārbaudes gadījumus bloķē citas RSAT instances, failu process gaidīs norādīto sekunžu skaitu un pēc tam izmēģinās vēl vienu reizi. Noklusējuma sekunžu \[vērtība\] ir 120 sekundes. Bez šī pārslēgšanas, nekavējoties tiks atcelts process, ja testa gadījumi ir bloķēti.
+ `/comments[="comment"]`: sniegt pielāgotu informācijas virkni, kas tiks ietverta laukā **Komentāri** kopsavilkuma un testa rezultātu lapās testa Azure DevOps gadījuma izpildes laikā.
+ `/byid`: šis pārslēgšanās norāda, ka vēlamais testa komplekts ir identificēts pēc Azure DevOps tā ID, nevis testa komplekta nosaukuma.

##### <a name="playbacksuitebyid-required-parameters"></a>Parametrs <a0/&;

+ `test_suite_id`: attēlo testa komplekta ID, kurā tas pastāv Azure DevOps.

##### <a name="playbacksuitebyid-examples"></a>Paralērs <a0/&t. t.i.

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>iziet

Aizver programmu. Šī komanda ir noderīga tikai tad, ja lietojumprogrammas darbojas interaktīvā režīmā.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>nomeš.: piemēri

`quit`

#### <a name="upload"></a>augšupielādēt

Augšupielādē pielikuma failus (Ierakstīšana, Izpilde un Parametru faili), kas pieder norādītajam testa komplektam vai testa gadījumiem Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>augšupielāde: obligātie parametri

+ `test_suite_name`: tiks augšupielādēti visi faili, kas pieder norādītajam testa komplektam.
+ `test_case_id1`: rāda pirmā testa gadījuma ID, kas ir jāielādē. Izmantojiet šo parametru tikai tad, ja nav norādīts testa komplekta nosaukums.
+ `test_case_idN`: norāda pēdējā testa gadījuma ID, kas ir jāielādē. Izmantojiet šo parametru tikai tad, ja nav norādīts testa komplekta nosaukums.

##### <a name="upload-examples"></a>augšupielāde: piemēri

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Augšupielādē tikai ieraksta failu, kas pieder vienam vai vairākiem noteiktais testa gadījumus Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: obligātie parametri

+ `test_case_id1`: parāda pirmā testa gadījuma ID ierakstam, kas ir jāielādē Azure DevOps.
+ `test_case_idN`: attēlo pēdējo testa gadījuma ID ierakstam, kas ir jāielādē Azure DevOps.

##### <a name="uploadrecording-examples"></a>uploadrecording: piemēri

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>lietojums

Parāda trīs šīs lietojumprogrammas lietošanas režīmus.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

Lietojumprogrammas interaktīvā darbība:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

Palaiž programmu, norādot komandu:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

Tiek palaista programma, norādot iestatījumu failu:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

### <a name="windows-powershell-examples"></a>Windows PowerShell piemēri

#### <a name="run-a-test-case-in-a-loop"></a>Testa gadījuma palaišana ciklā

Jums ir testa skripts, ar kuru tiek izveidots jauns debitors. Izmantojot skriptēšanu, šo testa gadījumu var palaist ciklā, pirms katra atkārtojuma izpildes randomizējot tālāk norādītos datus.

- Debitora ID
- Debitora nosaukums
- Debitora adrese

Klienta ID formāts vienmēr būs formātā *ATCUS\<number\>*, kur \<number\> ir vērtība no **000000001** līdz **999999999**.

Šajā piemērā izmantots viens parametrs **start**, lai definētu pirmo izmantoto numuru. Tiek izmantots otrs parametrs **nr**, lai definētu izveidojamo debitoru skaitu. Katram atkārtojumam parametri Excel parametru failā tiek mainīti, izmantojot funkciju UpdateCustomer. Pēc tam RSAT komandrinda tiek izsaukta funkcijā RunTestCase.

Atveriet Microsoft Windows PowerShell integrētās skriptēšanas vidi (ISE) administratora režīmā un ielīmējiet tālāk norādīto kodu logā ar nosaukumu **Untitled1.ps1**.

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>No Microsoft Dynamics 365 datiem atkarīga skripta palaišana

Tālāk norādītajā piemērā izmantots atvērta datu protokola (OData) izsaukums, lai atrastu pirkšanas pasūtījuma statusu. Ja statuss nav **iekļauts rēķinā**, varat, piemēram, izsaukt RSAT testa gadījumu, kas iegrāmato rēķinu.

```powershell
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
