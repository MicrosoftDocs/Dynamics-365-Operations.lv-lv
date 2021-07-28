---
title: Regression Suite Automation Tool apmācība
description: Šajā tēmā ir parādīts, kā izmantot Regression Suite Automation Tool (RSAT). Tajā ir aprakstīti dažādi līdzekļi un sniegti piemēri, kuros izmantota papildu skriptēšana.
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: d932a0c10df72dbadcc65d7ef78eb8ad05645bd5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357522"
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

2. Saglabājiet uzdevuma reģistrēšanu kā **izstrādāja ierakstu** un pievienojiet to testa gadījumam Azure Devops.
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

- Lai izmantotu šo līdzekli, atveriet failu **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**, kas atrodas RSAT instalācijas mapē (piemēram, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), un mainiet tālāk norādītā elementa vērtību no **false** uz **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Kad tiek palaists testa gadījums, RSAT ģenerēs soļu momentuzņēmumus (attēlus) pārbaudes gadījumu atskaņošanas mapē darba direktorijā. Ja tiek izmantota vecāka RSAT versija, attēli tiek saglabāti **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, tiek izveidota atsevišķa mape katram testa gadījumam, kas tiek palaists.

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
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Rāda palīdzību par visām pieejamām komandām un to parametriem.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Neobligāti parametri

`command`: Kur ``[command]`` ir viena no tālāk norādītajām komandām.

#### <a name="about"></a>par programmu

Rāda pašreizējo versiju.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Notīra ekrānu.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>lejupielādēt

Lejupielādē pielikumus norādītajam testa gadījumam izvades direktorijā.
Varat izmantot ``list`` komandu, lai iegūtu visus pieejamos pārbaudes gadījumus. Izmantojiet jebkuru vērtību no pirmās kolonnas kā **test_case_id** parametru.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a>lejupielāde: obligātie parametri

+ `test_case_id`: Parāda testa gadījuma ID.
+ `output_dir`: Attēlo izvades direktoriju. Direktorijam ir jāpastāv.

##### <a name="download-examples"></a>lejupielāde: piemēri

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a>rediģēt

Ļauj atvērt parametru failu Excel programmā un to rediģēt.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>rediģēt: obligātie parametri

+ `excel_file`: Ir jāietver pilns ceļš uz esošu Excel failu.

##### <a name="edit-examples"></a>rediģēt: piemēri

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>ģenerēt

Ģenerē pārbaudes izpildi un parametru failus norādītajam testa gadījumam izvades direktorijā. Varat izmantot ``list`` komandu, lai iegūtu visus pieejamos pārbaudes gadījumus. Izmantojiet jebkuru vērtību no pirmās kolonnas kā **test_case_id** parametru.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a>ģenerēt: nepieciešamos parametrus

+ `test_case_id`: Parāda testa gadījuma ID.
+ `output_dir`: Attēlo izvades direktoriju. Direktorijam ir jāpastāv.

##### <a name="generate-examples"></a>ģenerēt: piemēri

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a>generatederived

Ģenerē jaunu testa gadījumu, kas iegūts no norādītā testa gadījuma. Varat izmantot ``list`` komandu, lai iegūtu visus pieejamos pārbaudes gadījumus. Izmantojiet jebkuru vērtību no pirmās kolonnas kā **test_case_id** parametru.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a>generatederived: nepieciešamos parametrus

+ `parent_test_case_id`: Parāda vecāka pārbaudes gadījuma ID.
+ `test_plan_id`: Parāda testa plāna ID.
+ `test_suite_id`: Parāda testa komplekta ID.

##### <a name="generatederived-examples"></a>generatederived: piemēri

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Ģenerē tikai pārbaudes izpildes failu norādītajam testa gadījumam izvades direktorijā. Varat izmantot ``list`` komandu, lai iegūtu visus pieejamos pārbaudes gadījumus. Izmantojiet jebkuru vērtību no pirmās kolonnas kā **test_case_id** parametru.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a>generatesonly: nepieciešamos parametrus

+ `test_case_id`: Parāda testa gadījuma ID.
+ `output_dir`: Attēlo izvades direktoriju. Direktorijam ir jāpastāv.

##### <a name="generatetestonly-examples"></a>generatesonly: piemēri

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a>generatetestsuite

Ģenerē visus testa gadījumus norādītajam komplektam izvades direktorijā. Varat izmantot ``listtestsuitenames`` komandu, lai iegūtu visus pieejamos pārbaudes komplektus. Izmantojiet jebkuru vērtību no pirmās kolonnas kā **test_suite_name** parametru.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: nepieciešamos parametrus

+ `test_suite_name`: Parāda testa komplekta nosaukumu.
+ `output_dir`: Attēlo izvades direktoriju. Direktorijam ir jāpastāv.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: piemēri

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a>palīdzība

Identisks ar [?](#section) komanda.

#### <a name="list"></a>sarakstā

Uzskaita visus pieejamos pārbaudes gadījumus.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Uzskaita visus pieejamos pārbaudes plānus.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Uzskaita testa gadījumus norādītajam testu komplektam. Varat izmantot ``listtestsuitenames`` komandu, lai iegūtu visus pieejamos pārbaudes komplektus. Izmantojiet jebkuru vērtību no pirmās kolonnas kā **suite_name** parametru.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: nepieciešamie parametrus

+ `suite_name`: Nepieciešamā komplekta nosaukums.

##### <a name="listtestsuite-examples"></a>listtestsuite: piemēri

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Uzskaita visus pieejamos pārbaudes komplektus.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>atskaņošana

Atskaņo pārbaudes gadījumu, izmantojot Excel failu.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a>atskaņošana: obligātie parametri

+ `excel_file`: Pilns ceļš uz Excel failu. Failam ir jāpastāv.

##### <a name="playback-examples"></a>atskaņošana: piemēri

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Vienlaicīgi atskaņo vairākus pārbaudes gadījumus. Varat izmantot ``list`` komandu, lai iegūtu visus pieejamos pārbaudes gadījumus. Izmantojiet jebkuru vērtību no pirmās kolonnas kā **test_case_id** parametru.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: obligātie parametri

+ `test_case_id1`: Esošā testa gadījuma ID.
+ `test_case_id2`: Esošā testa gadījuma ID.
+ `test_case_idN`: Esošā testa gadījuma ID.

##### <a name="playbackbyid-examples"></a>playbackbyid: piemēri

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Vienlaicīgi atskaņo daudzus pārbaudes gadījumus, izmantojot Excel failus.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a>playbackbymany: obligātie parametri

+ `excel_file1`: Pilns ceļš uz Excel failu. Failam ir jāpastāv.
+ `excel_file2`: Pilns ceļš uz Excel failu. Failam ir jāpastāv.
+ `excel_fileN`: Pilns ceļš uz Excel failu. Failam ir jāpastāv.

##### <a name="playbackmany-examples"></a>playbackmany: piemēri

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Atskaņo visus testa gadījumus no norādītā testu komplekta.
Varat izmantot ``listtestsuitenames`` komandu, lai iegūtu visus pieejamos pārbaudes komplektus. Izmantojiet jebkuru vērtību no pirmās kolonnas kā **suite_name** parametru.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: obligātie parametri

+ `suite_name`: Nepieciešamā komplekta nosaukums.

##### <a name="playbacksuite-examples"></a>playbacksuite: piemēri

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a>iziet

Aizver programmu.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a>augšupielādēt

Augšupielādē visus failus, kas pieder norādītajam pārbaudes komplektam vai pārbaudes gadījumiem.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a>augšupielāde: obligātie parametri

+ `suite_name`: Augšupielādēs visus failus, kas pieder norādītajam pārbaudes komplektam.
+ `testcase_id`: Augšupielādēs visus failus, kas pieder norādītajam pārbaudes gadījumam(-iem).

##### <a name="upload-examples"></a>augšupielāde: piemēri

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Augšupielādē vienīgi to ieraksta failu, kas pieder norādītajiem pārbaudes gadījumiem.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: obligātie parametri

+ `testcase_id`: Augšupielādē ieraksta failu, kas pieder norādītajiem pārbaudes gadījumiem.

##### <a name="uploadrecording-examples"></a>uploadrecording: piemēri

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>lietojums

Tiek rādīti divi veidi, kā izsaukt šo programmu: viens izmanto noklusējuma iestatījumu failu, otrs nodrošina iestatījumu failu.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

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

```xpp
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