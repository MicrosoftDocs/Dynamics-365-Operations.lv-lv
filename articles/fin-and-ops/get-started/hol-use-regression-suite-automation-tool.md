---
title: Regression Suite Automation Tool lietošanas apmācība
description: Šajā tēmā ir parādīts, kā izmantot Regression Suite Automation Tool (RSAT). Tajā ir aprakstīti dažādi līdzekļi un sniegti piemēri, kuros izmantota papildu skriptēšana.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 8f3cd6a27ba0e09e48c0562aff46791228bb46b5
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703856"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool lietošanas apmācība

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Izmantojiet interneta pārlūka rīkus, lai lejupielādētu un saglabātu šo lapu PDF formātā. 

Šajā apmācībā ir aprakstīti daži Regression Suite Automation Tool (RSAT) papildu līdzekļi, ietverta demonstrācijas piešķire un aprakstīta stratēģija un galvenās mācību tēmas.

## <a name="features-of-rsattask-recorder"></a>RSAT/uzdevumu reģistrētāja līdzekļi

### <a name="validate-a-field-value"></a>Lauka vērtības validēšana

Informāciju par šo līdzekli skatiet tēmā [Jauna uzdevuma ieraksta izveide ar validēšanas funkciju](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).

### <a name="saved-variable"></a>Saglabāts mainīgais

Informāciju par šo līdzekli skatiet tēmā [Esoša uzdevuma ieraksta modificēšana, lai izveidotu saglabātu mainīgo](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).

### <a name="derived-test-case"></a>Atvasināts testa gadījums

1. Atveriet Regression Suite Automation Tool (RSAT) un atlasiet abus testa gadījumus, ko izveidojāt, izpildot tēmā [Regression Suite Automation Tool iestatīšana un instalēšana](./hol-set-up-regression-suite-automation-tool.md) norādītās darbības.
2. Atlasiet **Jauns \> Izveidot atvasināto testa gadījumu**.

    ![Jauna atvasinātā testa gadījuma komandas izveide izvēlnē Jauns](./media/use_rsa_tool_01.png)

3. Tiek parādīts ziņojums, ka atvasinātais testa gadījums tiks izveidots katram pašreizējā testu kopā atlasītajam testa gadījumam un ka katram atvasinātajam testa gadījumam tiks izveidota sava Excel parametru faila kopija. Atlasiet **Labi**.

    > [!NOTE]
    > Palaižot atvasināto testa gadījumu, tiek izmantots tā pamata testa gadījuma uzdevuma ieraksts un atvasinātā testa gadījuma Excel parametru faila kopija. Šādā veidā varat palaist vienu un to pašu testu ar dažādiem parametriem bez nepieciešamības uzturēt vairāk par vienu uzdevuma ierakstu. Atvasinātajam testa gadījumam nav jāietilpst tajā pašā testu kopā, kurā ietilpst tā pamata testa gadījums.

    ![Ziņojuma lodziņš](./media/use_rsa_tool_02.png)

    Tiek izveidoti divi papildu atvasinātie testa gadījumi, un tiek atlasīta šo atvasināto testa gadījumu izvēles rūtiņa **Atvasināts?**.

    ![Izveidotie atvasinātie testa gadījumi](./media/use_rsa_tool_03.png)

    Pakalpojumā Azure DevOps tiek automātiski izveidots atvasinātais testa gadījums. Tas ir testa gadījuma **Izveidot jaunu preci** pakārtotais vienums un ir atzīmēts ar īpašu atslēgvārdu: **RSAT:DerivedTestSteps**. Šie testa gadījumi arī tiek automātiski pievienoti testa plānam pakalpojumā Azure DevOps.

    ![RSAT:DerivedTestSteps atslēgvārds](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > Ja kāda iemesla dēļ izveidotie atvasinātie testa gadījumi nav pareizā secībā, dodieties uz Azure DevOps un pārkārtojiet testa gadījumus testu komplektā, lai RSAT varētu tos palaist pareizā secībā.

4. Atlasiet atvasinātos testa gadījumus un pēc tam atlasiet **Rediģēt**, lai atvērtu atbilstošos Excel parametru failus.
5. Rediģējiet šos Excel parametru failus tādā pašā veidā, kā rediģējāt pamata failus. Citiem vārdiem sakot, pārliecinieties, ka preces ID ir iestatīts tā, lai tas tiktu ģenerēts automātiski. Turklāt pārliecinieties, ka saglabātais mainīgais tiek kopēts atbilstošajos laukos.
6. Abu Excel parametru failu cilnē **Vispārīgi** atjauniniet lauka **Uzņēmums** vērtību uz **USSI**, lai atvasinātie testa gadījumi tiktu izpildīti attiecībā pret citu juridisko personu, nevis to, kas norādīta pamata testa gadījumam. Lai palaistu testa gadījumus attiecībā pret noteiktu lietotāju (vai lomu, kas saistīta ar noteiktu lietotāju), varat atjaunināt lauka **Testa lietotājs** vērtību.
7. Atlasiet **Palaist**un pārliecinieties, ka prece ir izveidota gan USMF juridiskajai personai, gan USSI juridiskajai personai.

### <a name="validate-notifications"></a>Paziņojumu validēšana

Šo funkciju var izmantot, lai pārbaudītu, vai darbība ir notikusi. Piemēram, kad tiek izveidots un pēc tam sākts ražošanas pasūtījums, Microsoft Dynamics 365 for Finance and Operations parāda ziņojumu “Ražošana — Sākums”, lai informētu, ka ražošanas pasūtījums ir sākts.

![Paziņojums Ražošana — Sākums](./media/use_rsa_tool_05.png)

Šo ziņojumu varat validēt ar RSAT, ievadot ziņojuma tekstu atbilstošā ieraksta Excel parametru faila cilnē **MessageValidation**.

![Ziņojuma validēšanas cilne](./media/use_rsa_tool_06.png)

Pēc testa gadījuma palaišanas ziņojums Excel parametru failā tiek salīdzināts ar ziņojumu, kas tiek parādīts programmā Finance and Operations. Ja ziņojumi nesakrīt, testa gadījums ir nesekmīgs.

> [!NOTE]
> Excel parametru faila cilnē **MessageValidation** varat ievadīt vairāk nekā vienu ziņojumu. Ziņojumi var būt arī kļūdu vai brīdinājuma ziņojumi, nevis informācijas ziņojumi.

### <a name="validate-values-by-using-operators"></a>Vērtību validēšana, izmantojot operatorus

Iepriekšējās RSAT versijās bija iespējams validēt vērtības tikai tad, ja kontroles vērtība bija vienāda ar paredzēto vērtību. Jaunais līdzeklis ļauj validēt mainīgo, kas nav vienāds ar, ir mazāks par vai ir lielāks par norādīto vērtību.

- Lai izmantotu šo līdzekli, atveriet failu **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**, kas atrodas RSAT instalācijas mapē (piemēram, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), un mainiet tālāk norādītā elementa vērtību no **false** uz **true**.

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    Excel parametru failā tiek parādīts jauns laiks **Operators**.

    > [!NOTE]
    > Ja izmantojat vecāku RSAT versiju, ir jāģenerē jauni Excel parametru faili.

    ![Lauks Operators](./media/use_rsa_tool_07.png)

Tālāk norādītajā piemērā ir parādīts, kā varat izmantot šo līdzekli, lai pārbaudītu, vai rīcībā esošo krājumu daudzums ir vairāk nekā 0 (nulle).

1. Demonstrācijas datos uzņēmumā **USMF** izveidojiet uzdevuma ierakstu, kurā ir tālāk norādītās darbības.

    1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
    2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka **Krājuma numurs**, izmantojot vērtību **1000**.
    3. Atlasiet **Rīcībā esošie krājumi**.
    4. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka **Vieta**, izmantojot vērtību **1**.
    5. Sarakstā atzīmējiet atlasīto rindu.
    6. Pārbaudiet, vai lauka **Pieejamā kopsumma** vērtība ir **411.0000000000000000**.

2. Saglabājiet uzdevuma ierakstu BPM bibliotēkā pakalpojumā LCS un sinhronizējiet ar Azure DevOps.
3. Pievienojiet testa gadījumu testa plānam un ielādējiet testa gadījumu RSAT.
4. Atveriet Excel parametru failu. Cilnē **InventOnhandItem** ir redzama sadaļa **Validēt InventOnhandItem**, kurā ietverts lauks **Operators**.

    ![Lauks Operators](./media/use_rsa_tool_08.png)

5. Lai pārbaudītu, vai rīcībā esošie krājumi vienmēr būs lielāki par 0, mainiet lauka **Vērtība** vērtību no **411** uz **0** un lauka **Operators** vērtību no vienādības zīmes (**=**) uz zīmi “lielāks par” (**\>**).

    ![Nomainītas lauku Vērtība un Operators vērtības](./media/use_rsa_tool_09.png)

6. Saglabājiet un aizveriet Excel parametru failu.
7. Atlasiet **Augšupielādēt**, lai saglabātu izmaiņas, kuras veicāt Excel parametru failā, pakalpojumā Azure DevOps.

Ja tagad lauka **Pieejamā kopsumma** vērtība norādītajam vienumam krājumā ir lielāka par 0 (nulli), testi būs sekmīgi neatkarīgi no faktiskās rīcībā esošo krājumu vērtības.

### <a name="generator-logs"></a>Ģeneratora žurnāli

Šis līdzeklis izveido mapi, kurā atrodas palaisto testa gadījumu žurnāli.

- Lai izmantotu šo līdzekli, atveriet failu **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**, kas atrodas RSAT instalācijas mapē (piemēram, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), un mainiet tālāk norādītā elementa vērtību no **false** uz **true**.

    ```
    <add key="LogGeneration" value="false" />
    ```

Kad testa gadījumi ir izpildīti, žurnāla failus varat atrast sadaļā **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.

![Mape GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> Ja testa gadījumi pastāvēja, pirms mainījāt vērtību failā .config, šiem testa gadījumiem žurnāli netiks ģenerēti, kamēr netiks ģenerēti jauni testa izpildes faili.
> 
> ![Komanda Izveidot tikai teksta izpildes failus izvēlnē Jauns](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>Momentuzņēmums

Šis līdzeklis uzņem to darbību ekrānuzņēmumus, kas tika izpildītas uzdevuma reģistrēšanas laikā.

- Lai izmantotu šo līdzekli, atveriet failu **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**, kas atrodas RSAT instalācijas mapē (piemēram, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), un mainiet tālāk norādītā elementa vērtību no **false** uz **true**.

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Sadaļā **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** tiek izveidota atsevišķa mape katram izpildītajam testa gadījumam.

![Testa gadījuma momentuzņēmuma mape](./media/use_rsa_tool_12.png)

Katrā no šīm mapēm varat atrast to darbību momentuzņēmumus, kas tika veiktas, kamēr tika izpildīti testa gadījumi.

![Momentuzņēmumu faili](./media/use_rsa_tool_13.png)

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

![Demonstrācijas scenārija plūsma](./media/use_rsa_tool_14.png)

Tālāk redzamajā attēlā ir parādīti šī scenārija biznesa procesi RSAT.

![Demonstrācijas scenārija biznesa procesi](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Stratēģija — galvenās mācību tēmas

### <a name="data"></a>Dati

- Pārliecinieties, ka jums ir reprezentatīvi datu apjomi (ražošanas/zelta konfigurācijas datu kopija un migrētie dati).
- Kad ģenerējat jaunus datus, izmantojot uzdevuma reģistrētāju, izveidojiet testa nosaukumus, kas nekonfliktē ar esošiem nosaukumiem (piemēram, izmantojiet prefiksu **RSATxxx**).
- Izmantojiet Azure punkta laikā atjaunošanu, lai atkārtoti palaistu testus vidēs, kas nav 1. līmeņa vides.
- Lai ģenerētu unikālu kombināciju, varat izmantot Excel funkcijas **RANDOM** un **NOW**, tomēr būs jāiegulda ievērojamas pūles. Tālāk ir minēts piemērs.

    ```
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

### <a name="command-line"></a>Komandrinda

RSAT var izsaukt no **komandu uzvednes** loga.

> [!NOTE]
> Pārbaudiet, vai vides mainīgajam **TestRoot** ir iestatīts RSAT instalācijas ceļš. (Operētājsistēmā Microsoft Windows atveriet **Vadības panelis**, atlasiet **Sistēma un drošība \> Sistēma \> Sistēmas papildiestatījumi** un pēc tam atlasiet **Vides mainīgie**.)

1. Atveriet **komandu uzvednes** logu kā administrators.
2. Palaidiet rīku no instalācijas direktorija.

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Attēlojiet visas komandas saraksta veidā.

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a>Windows PowerShell piemēri

#### <a name="run-a-test-case-in-a-loop"></a>Testa gadījuma palaišana ciklā

Jums ir testa skripts, ar kuru tiek izveidots jauns debitors. Izmantojot skriptēšanu, šo testa gadījumu var palaist ciklā, pirms katra atkārtojuma izpildes randomizējot tālāk norādītos datus.

- Debitora ID
- Debitora nosaukums
- Debitora adrese

Klienta ID formāts vienmēr būs *ATCUS\<numurs\>*, kur \<numurs\> ir vērtība no **000000001** līdz **999999999**.

Šajā piemērā izmantots viens parametrs **start**, lai definētu pirmo izmantoto numuru. Tiek izmantots otrs parametrs **nr**, lai definētu izveidojamo debitoru skaitu. Katram atkārtojumam parametri Excel parametru failā tiek mainīti, izmantojot funkciju UpdateCustomer. Pēc tam RSAT komandrinda tiek izsaukta funkcijā RunTestCase.

Atveriet Microsoft Windows PowerShell integrētās skriptēšanas vidi (ISE) administratora režīmā un ielīmējiet tālāk norādīto kodu logā ar nosaukumu **Untitled1.ps1**.

```
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
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>No Microsoft Dynamics 365 datiem atkarīga skripta palaišana

Tālāk norādītajā piemērā izmantots atvērta datu protokola (OData) izsaukums, lai atrastu pirkšanas pasūtījuma statusu. Ja statuss nav **iekļauts rēķinā**, varat, piemēram, izsaukt RSAT testa gadījumu, kas iegrāmato rēķinu.

```
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
