<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="trace-execution-er-troubleshoot-perf.md" target-language="lv-LV">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>trace-execution-er-troubleshoot-perf.773b92.aa71db2752889bc905c22bab1cf2fa46d7ee07c7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>aa71db2752889bc905c22bab1cf2fa46d7ee07c7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>67d00b95952faf0db580d341249d4e50be59119c</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\trace-execution-er-troubleshoot-perf.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Trace execution of ER format to troubleshoot performance issues</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER formāta izpildes izsekošana, lai novērstu veiktspējas problēmas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to use the performance trace feature in Electronic reporting (ER) to troubleshoot performance issues.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šajā tēmā ir sniegta informācija par to, kā izmantot veiktspējas izsekošanas līdzekli elektronisko pārskatu veidošanā (ER), lai novērstu veiktspējas problēmas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Trace the execution of ER formats to troubleshoot performance issues</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">ER formātu izpildes izsekošana, lai novērstu veiktspējas problēmas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Elektronisko pārskatu veidošanas (ER) konfigurāciju izstrādes procesa ietvaros, lai izveidotu elektroniskus dokumentus, nosakiet metodi, kas tiek izmantota, lai iegūtu datus no Microsoft Dynamics 365 for Finance and Operations un ievadītu tos ģenerētajā izvadē.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER veiktspējas izsekošanas līdzeklis palīdz ievērojami samazināt laiku un izmaksas, kas saistītas ar ER formāta izpildes informācijas vākšanu un tās izmantošanu, lai novērstu veiktspējas problēmas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šajā apmācībā ir sniegti norādījumi par to, kā informāciju par izpildīto ER formātu veiktspējas izsekošanu programmā Finance and Operations var izmantot, lai palīdzētu uzlabot veiktspēju.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Priekšnosacījumi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To complete the examples in this tutorial, you must have the following access:</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Lai izpildītu šajā apmācībā aprakstītos piemērus, jums ir nepieciešama tālāk norādītā piekļuve.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Access to Finance and Operations for one of the following roles:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Piekļuve programmai Finance and Operations vienai no šīm lomām:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Elektroniskā pārskata izstrādātājs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Elektronisko pārskatu veidošanas funkcionālais konsultants</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Sistēmas administrators</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Piekļuve Regulatory Configuration Services (RCS) instancei, kas ir nodrošināta tam pašam nomniekam, kuram nodrošināta Finance and Operations instance, vienai no šādām lomām:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Elektroniskā pārskata izstrādātājs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Elektronisko pārskatu veidošanas funkcionālais konsultants</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Sistēmas administrators</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You must also download and locally store the following files.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Nepieciešams arī lejupielādēt un lokāli saglabāt tālāk norādītos failus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>File</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Fails</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Content</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Saturs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Performance trace model.version.1</source><target logoport:matchpercent="0" state="translated">Veiktspējas izsekošanas modelis.versija.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">[</bpt>Sample ER data model configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>Parauga ER datu modeļa konfigurācija<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Performance trace metadata.version.1</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Veiktspējas izsekošanas metadati.versija.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">[</bpt>Sample ER metadata configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>Parauga ER metadatu konfigurācija<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Performance trace mapping.version.1.1</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Veiktspējas izsekošanas kartējums.versija.1.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt>Sample ER model mapping configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>Parauga ER modeļa kartējuma konfigurācija<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Performance trace format.version.1.1</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Veiktspējas izsekošanas formāts.versija.1.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt>Sample ER format configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>Parauga ER formāta konfigurācija<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Configure ER parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Konfigurēt ER parametrus</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Katra ER veiktspējas izsekošana, kas tiek ģenerēta programmā Finance and Operations, tiek saglabāta kā izpildes žurnāla ieraksta pielikums.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The Document management (DM) framework of Finance and Operations is used to manage these attachments.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šo pielikumu pārvaldībai tiek izmantota programmas Finance and Operations dokumentu pārvaldības (Document Management — DM) struktūras.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vispirms ir jākonfigurē ER parametri, lai norādītu DM dokumenta tipu, kas jāizmanto veiktspējas izsekošanas pievienošanai.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In Finance and Operation, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Programmā Finance and Operations, darbvietā <bpt id="p1">**</bpt>Elektronisko pārskatu veidošana<ept id="p1">**</ept> atlasiet <bpt id="p2">**</bpt>Elektronisko pārskatu veidošanas parametri<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pēc tam lapas <bpt id="p1">**</bpt>Elektronisko pārskatu veidošanas parametri<ept id="p1">**</ept> cilnes <bpt id="p2">**</bpt>Pielikumi<ept id="p2">**</ept> laukā <bpt id="p3">**</bpt>Citi<ept id="p3">**</ept> atlasiet DM dokumenta tipu, kas tiks izmantots veiktspējas izsekošanai.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lapa Elektronisko pārskatu veidošanas parametri programmā Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lai DM dokumenta tips būtu pieejams uzmeklēšanas laukā <bpt id="p1">**</bpt>Citi<ept id="p1">**</ept>, tas ir jākonfigurē lapā <bpt id="p2">**</bpt>Dokumentu tipi<ept id="p2">**</ept> (<bpt id="p3">**</bpt>Organizācijas administrēšana <ph id="ph1">\&gt;</ph> Dokumentu pārvaldība <ph id="ph2">\&gt;</ph> Dokumentu tipi<ept id="p3">**</ept>) šādā veidā:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Klase:<ept id="p1">**</ept> Pievienot failu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Grupa:<ept id="p1">**</ept> Fails</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Document types page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lapa Dokumentu tipi programmā Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atlasītajam dokumenta tipam jābūt pieejamam ikvienā pašreizējās Finance and Operations instances uzņēmumā, jo DM pielikumi attiecas tikai uz konkrētu uzņēmumu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Configure RCS parameters</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">RCS parametru konfigurēšana</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER veiktspējas izsekošana, kas tiek ģenerēta programmā Finance and Operations, tiks importēta RCS analīzes veikšanai, izmantojot ER formāta noformētāju un ER kartēšanas noformētāju.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tā kā ER veiktspējas izsekošana tiek uzglabāta kā izpildes žurnāla ieraksta pielikums, kas ir saistīts ar ER formātu, RCS parametri ir jākonfigurē iepriekš, lai norādītu DM dokumenta tipu, kas jāizmanto veiktspējas izsekošanas pievienošanai.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the instance of RCS that has been provisioned for your company, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tādā RCS instancē, kas nodrošināta jūsu uzņēmumam, darbvietā <bpt id="p1">**</bpt>Elektronisko pārskatu veidošana<ept id="p1">**</ept> atlasiet <bpt id="p2">**</bpt>Elektronisko pārskatu veidošanas parametri.<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Pēc tam lapas <bpt id="p1">**</bpt>Elektronisko pārskatu veidošanas parametri<ept id="p1">**</ept> cilnes <bpt id="p2">**</bpt>Pielikumi<ept id="p2">**</ept> laukā <bpt id="p3">**</bpt>Citi<ept id="p3">**</ept> atlasiet DM dokumenta tipu, kas tiks izmantots veiktspējas izsekošanai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Electronic reporting parameters page in RCS</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">Lapa Elektronisko pārskatu veidošanas parametri pakalpojumā RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Lai DM dokumenta tips būtu pieejams uzmeklēšanas laukā <bpt id="p1">**</bpt>Citi<ept id="p1">**</ept>, tas ir jākonfigurē lapā <bpt id="p2">**</bpt>Dokumentu tipi<ept id="p2">**</ept> (<bpt id="p3">**</bpt>Organizācijas administrēšana <ph id="ph1">\&gt;</ph> Dokumentu pārvaldība <ph id="ph2">\&gt;</ph> Dokumentu tipi<ept id="p3">**</ept>) šādā veidā:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>Klase:<ept id="p1">**</ept> Pievienot failu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>Grupa:<ept id="p1">**</ept> Fails</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Design an ER solution</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">ER risinājuma izstrāde</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pieņemsim, ka esat sācis izstrādāt jaunu ER risinājumu, lai ģenerētu jaunu pārskatu, kurā parādītas kreditoru darbības.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Currently, you can find the transactions for a selected vendor on the <bpt id="p1">**</bpt>Vendor transactions<ept id="p1">**</ept> page (go to <bpt id="p2">**</bpt>Account payable <ph id="ph1">\&gt;</ph> Vendors <ph id="ph2">\&gt;</ph> All vendors<ept id="p2">**</ept>, select a vendor, and then, on the Action Pane, on the <bpt id="p3">**</bpt>Vendor<ept id="p3">**</ept> tab, in the <bpt id="p4">**</bpt>Transactions<ept id="p4">**</ept> group, select <bpt id="p5">**</bpt>Transactions<ept id="p5">**</ept>).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pašlaik varat atrast atlasītā kreditora transakcijas lapā <bpt id="p1">**</bpt>Kreditoru transakcijas<ept id="p1">**</ept> (pārejiet uz <bpt id="p2">**</bpt>Parādi kreditoriem <ph id="ph1">\&gt;</ph> Kreditori <ph id="ph2">\&gt;</ph> Visi kreditori<ept id="p2">**</ept>, atlasiet kreditoru un pēc tam darbību rūtī, cilnē <bpt id="p3">**</bpt>Kreditors<ept id="p3">**</ept>, grupā <bpt id="p4">**</bpt>Transakcijas<ept id="p4">**</ept> atlasiet vienumu <bpt id="p5">**</bpt>Transakcijas<ept id="p5">**</ept>).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>However, you want to have all vendor transaction at the same time in one electronic document in XML format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tomēr ir nepieciešams, lai visas kreditoru transakcijas vienlaicīgi būtu vienā elektroniskajā dokumentā XML formātā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šis risinājums sastāv no vairākām ER konfigurācijām, kas ietver nepieciešamo datu modeli, metadatus, modeļa kartējumu un formāta komponentus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Sign in to the instance of RCS that has been provisioned for your company.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Piesakieties RCS instancē, kas nodrošināta jūsu uzņēmumam.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In this tutorial, you will create and modify configurations for the <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept> sample company.</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">Šajā apmācībā jūs izveidosit un modificēsit nepieciešamās konfigurācijas parauga uzņēmumam <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Therefore, make sure that this configuration provider has been added to RCS and selected as active.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tādēļ pārliecinieties, ka šis konfigurācijas nodrošinātājs ir pievienots RCS un atlasīts kā aktīvs.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For instructions, see the <bpt id="p1">[</bpt>Create configuration providers and mark them as active<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept> procedure.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Norādījumus skatiet procedūrā <bpt id="p1">[</bpt>Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Darbvietā <bpt id="p1">**</bpt>Elektroniskie pārskati<ept id="p1">**</ept> atlasiet elementu <bpt id="p2">**</bpt>Pārskatu veidošanas konfigurācijas<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lapā <bpt id="p1">**</bpt>Konfigurācijas<ept id="p1">**</ept> importējiet ER konfigurācijas, kuras lejupielādējāt kā priekšnosacījumu pakalpojumā RCS, šādā secībā: datu modelis, metadati, modeļa kartējums, formāts.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For each configuration, follow these steps:</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Katrai konfigurācijai rīkojieties šādi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Exchange <ph id="ph1">\&gt;</ph> Load from XML file<ept id="p1">**</ept>.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Darbību rūtī atlasiet <bpt id="p1">**</bpt>Mainīt <ph id="ph1">\&gt;</ph> Ielādēt no XML faila<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the appropriate file for the required ER configuration in XML format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atlasiet <bpt id="p1">**</bpt>Pārlūkot<ept id="p1">**</ept>, lai atlasītu atbilstošu failu nepieciešamajai ER konfigurācijai XML formātā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Atlasiet <bpt id="p1">**</bpt>Labi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Configurations page in RCS</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Lapa Konfigurācijas pakalpojumā RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Run the ER solution to trace execution</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Palaidiet ER risinājumu, lai izsekotu izpildi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Assume that you've finished designing the first version of the ER solution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pieņemsim, ka esat pabeidzis izstrādāt ER risinājuma pirmo versiju.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>You now want to test it in your Finance and Operations instance and analyze execution performance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tagad vēlaties to pārbaudīt savā FInance and Operations instancē un analizēt izpildes veiktspēju.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import an ER configuration from RCS into Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>ER konfigurācijas importēšana no pakalpojuma RCS programmā Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Sign in to your Finance and Operations instance.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Pierakstieties savā Finance and Operations instancē.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šīs apmācības ietvaros importēsit konfigurācijas no savas RCS instances (kur izstrādājat ER komponentus) savā Finance and Operations instancē (kur tos testējat un izmantojat).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Therefore, you must make sure that all the required artifacts have been prepared.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tāpēc ir jāpārliecinās, ka ir sagatavoti visi vajadzīgie artefakti.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>For instructions, see the <bpt id="p1">[</bpt>Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept> procedure.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Norādījumus skatiet procedūrā <bpt id="p1">[</bpt>Importēt elektronisko pārskatu (ER) konfigurācijas no Regulatory Configuration Services (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Follow these steps to import the configurations from RCS into Finance and Operations:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Veiciet šādas darbības, lai importētu konfigurācijas no RCS programmā Finance and Operations.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, on the tile for the <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept> configuration provider, select <bpt id="p3">**</bpt>Repositories<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Darbvietā <bpt id="p1">**</bpt>Elektronisko pārskatu veidošana<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept> konfigurācijas nodrošinātāja elementā atlasiet <bpt id="p3">**</bpt>Repozitoriji<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>On the <bpt id="p1">**</bpt>Configuration repository<ept id="p1">**</ept> page, select the repository of the <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> type, and then select <bpt id="p3">**</bpt>Open<ept id="p3">**</ept>.</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match">Lapā <bpt id="p1">**</bpt>Konfigurācijas repozitorijs<ept id="p1">**</ept> atlasiet repozitoriju ar tipu <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> un pēc tam atlasiet <bpt id="p3">**</bpt>Atvērt<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> FastTab, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kopsavilkuma cilnē <bpt id="p1">**</bpt>Konfigurācijas<ept id="p1">**</ept> atlasiet konfigurāciju <bpt id="p2">**</bpt>Veiktspējas izsekošanas formāts<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>On the <bpt id="p1">**</bpt>Versions<ept id="p1">**</ept> FastTab, select version <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> of the selected configuration, and then select <bpt id="p3">**</bpt>Import<ept id="p3">**</ept>.</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Kopsavilkuma cilnē <bpt id="p1">**</bpt>Versijas<ept id="p1">**</ept> atlasiet atlasītās konfigurācijas versiju <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> un pēc tam atlasiet <bpt id="p3">**</bpt>Importēt<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Configuration repository page in Finance and Operations</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">Lapa Konfigurācijas repozitorijs programmā Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Datu modeļa un modeļa kartējuma konfigurāciju atbilstošās versijas automātiski tiek importētas kā priekšnosacījumi importētajai ER formāta konfigurācijai.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Turn on the ER performance trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER veiktspējas izsekošanas ieslēgšana</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Risinājumā Finance and Operations dodieties uz sadaļu <bpt id="p1">**</bpt>Organizācijas administrēšana <ph id="ph1">\&gt;</ph> Elektronisko pārskatu veidošana <ph id="ph2">\&gt;</ph> Konfigurācijas<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Lapas <bpt id="p1">**</bpt>Konfigurācijas<ept id="p1">**</ept> darbību rūtī, cilnē <bpt id="p2">**</bpt>Konfigurācijas<ept id="p2">**</ept>, grupā <bpt id="p3">**</bpt>Papildu iestatījumi<ept id="p3">**</ept> atlasiet vienumu <bpt id="p4">**</bpt>Lietotāja parametri<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, follow these steps:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dialoglodziņa <bpt id="p1">**</bpt>Lietotāja parametri<ept id="p1">**</ept> sadaļā <bpt id="p2">**</bpt>Izpildes izsekošana<ept id="p2">**</ept> rīkojieties šādi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Debug trace format<ept id="p2">**</ept> to start to collect the details of ER format execution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Laukā <bpt id="p1">**</bpt>Izpildes izsekošanas formāts<ept id="p1">**</ept> atlasiet vienumu <bpt id="p2">**</bpt>Atkļūdot izsekošanas formātu<ept id="p2">**</ept>, lai sāktu apkopot informāciju par ER formāta izpildi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atlasot šo vērtību, veiktspējas izsekošana apkopos informāciju par laiku, kas tiek patērēts šādām darbībām:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Running each data source in the model mapping that is called to get data</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Katra datu avota palaišana modeļa kartējumā, kas tiek izsaukts datu iegūšanai</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Processing each format item to enter data in the output that is generated</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Katra formāta vienuma apstrāde, lai ievadītu datus ģenerētajā izvadē</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You use the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lauku <bpt id="p1">**</bpt>Izpildes izsekošanas formāts<ept id="p1">**</ept> izmanto, lai norādītu ģenerētās veiktspējas izsekošanas formātu, kurā tiek uzglabāta izpildes informācijas ER formāta un kartēšanas elementiem.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>By selecting <bpt id="p1">**</bpt>Debug trace format<ept id="p1">**</ept> as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atlasot kā vērtību <bpt id="p1">**</bpt>Atkļūdot izsekošanas formātu<ept id="p1">**</ept>, varēsit analizēt izsekošanas saturu ER operāciju noformētājā un skatīt ER formāta vai kartēšanas elementus, kas minēti izsekošanā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Set the following options to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to collect specific details of the execution of the ER model mapping and ER format components:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Iestatiet tālāk minētajām opcijām vienumu <bpt id="p1">**</bpt>Jā<ept id="p1">**</ept>, lai apkopotu noteiktu informāciju par ER modeļa kartējuma un ER formāta komponentu izpildi:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Collect query statistics<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect the following information:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Apkopot vaicājumu statistiku<ept id="p1">**</ept> — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota šāda informācija:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The number of database calls that were made by data sources</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Datu avotu veikto datu bāzes izsaukumu skaits</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The number of duplicate calls to the database</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Datu bāzes dublētu izsaukumu skaits</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Details of the SQL statements that were used to make database calls</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Informācija par SQL priekšrakstiem, kas izmantoti datu bāzes izsaukumu veikšanai</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Trace access of caching<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Izsekot kešdarbes piekļuvi<ept id="p1">**</ept> — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota informācija par ER modeļa kartējuma kešatmiņas izmantošanu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source><bpt id="p1">**</bpt>Trace data access<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Izsekot datu piekļuvi<ept id="p1">**</ept> — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota informācija par datu bāzes izsaukumu skaitu izpildītajiem datu avotiem, kas atbilst tipam “ierakstu saraksts”.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">**</bpt>Trace list enumeration<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Izsekot saraksta uzskaitījumu<ept id="p1">**</ept> — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota informācija par ierakstu skaitu, kas pieprasīti no datu avotiem, kuri atbilst tipam “ierakstu saraksts”.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The parameters in the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box are specific to the user and the current company.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Parametri dialoglodziņā <bpt id="p1">**</bpt>Lietotāja parametri<ept id="p1">**</ept> dialoglodziņā ir raksturīgi lietotājam un pašreizējam uzņēmumam.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>User parameters dialog box in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dialoglodziņš Lietotāja parametri programmā Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Run the ER format</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>ER formāta palaišana</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>In Finance and Operations, select the <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept> company.</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match">Programmā Finance and Operations atlasiet uzņēmumu <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Dodieties uz <bpt id="p1">**</bpt>Organizācijas administrēšana <ph id="ph1">\&gt;</ph> Elektronisko pārskatu veidošana <ph id="ph2">\&gt;</ph> Konfigurācijas<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> item.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Lapā <bpt id="p1">**</bpt>Konfigurācijas<ept id="p1">**</ept>, konfigurāciju kokā atlasiet vienumu <bpt id="p2">**</bpt>Veiktspējas izsekošanas formāts<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Run<ept id="p1">**</ept>.</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Darbību rūtī atlasiet <bpt id="p1">**</bpt>Palaist<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Notice that the file that is generated presents information about 265 transactions for six vendors.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ņemiet vērā, ka ģenerētajā failā ir ietverta informācija par 265 transakcijām sešiem kreditoriem.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Review the execution trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Izpildes izsekošanas pārskatīšana</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Eksportēt ģenerēto izsekošanu no programmas Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Veiktspējas izsekošana ir atdalīta no avota ER formāta, un to var serializēt ārējā zip failā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configuration debug logs<ept id="p1">**</ept>.</source><target logoport:matchpercent="88" state="translated" state-qualifier="fuzzy-match">Risinājumā Finance and Operations dodieties uz sadaļu <bpt id="p1">**</bpt>Organizācijas administrēšana <ph id="ph1">\&gt;</ph> Elektronisko pārskatu veidošana <ph id="ph2">\&gt;</ph> Konfigurācijas atkļūdošanas žurnāli<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Electronic reporting run logs<ept id="p1">**</ept> page, in the left pane, in the <bpt id="p2">**</bpt>Configuration name<ept id="p2">**</ept> field, select <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> to find the log records that have been generated by the execution of the <bpt id="p4">**</bpt>Performance trace format<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lapā <bpt id="p1">**</bpt>Elektronisko pārskatu palaišanas žurnāli<ept id="p1">**</ept>, kreisajā rūtī, laukā <bpt id="p2">**</bpt>Konfigurācijas nosaukums<ept id="p2">**</ept> atlasiet <bpt id="p3">**</bpt>Veiktspējas izsekošanas formāts<ept id="p3">**</ept>, lai atrastu žurnāla ierakstus, kas ģenerēti, izpildot konfigurāciju <bpt id="p4">**</bpt>Veiktspējas izsekošanas formāts<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Select the <bpt id="p1">**</bpt>Attachments<ept id="p1">**</ept> button (the paper clip symbol) in the upper-right corner of the page, or press <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept>.</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Atlasiet pogu <bpt id="p1">**</bpt>Pielikumi<ept id="p1">**</ept> (papīra saspraudes simbols) lapas augšējā labajā stūrī vai nospiediet <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Attachments button on the Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Poga Pielikumi lapā Elektronisko pārskatu palaišanas žurnāli programmā Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>On the <bpt id="p1">**</bpt>Attachments for Electronic reporting run logs<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Open<ept id="p2">**</ept> to get the performance trace as a zip file and store it locally.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lapas <bpt id="p1">**</bpt>Elektronisko pārskatu palaišanas žurnālu pielikumi<ept id="p1">**</ept> darbību rūtī atlasiet <bpt id="p2">**</bpt>Atvērt<ept id="p2">**</ept>, lai iegūtu veiktspējas izsekošanu kā zip failu un saglabātu to lokāli.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Attachments for Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Lapa Elektronisko pārskatu palaišanas žurnālu pielikumi programmā Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The trace that is generated has a reference to the source ER report via a unique report identifier in <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> format only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ģenerētajai izsekošanai ir atsauce uz avota ER pārskatu, izmantojot unikālu pārskata identifikatoru tikai <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> formātā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The version numbering of the format isn't considered.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Formāta versijas numerācija netiek ņemta vērā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ņemiet vērā, ka saistība starp veiktspējas izsekošanu, kas ir ģenerēta izpildītajam ER formātam, un ER modeļa kartējumu ir balstīta uz izmantoto saknes deskriptoru un kopējo datu modeli.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>The version numbering of the format and model mapping isn't considered.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Formāta un modeļa kartējuma versijas numerācija netiek ņemta vērā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The setting of the <bpt id="p1">**</bpt>Default for model mapping<ept id="p1">**</ept> flag for the model mapping also isn't considered.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Modeļa kartējuma karodziņa <bpt id="p1">**</bpt>Modeļa kartējuma noklusējums<ept id="p1">**</ept> iestatījums arī netiek ņemts vērā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import the generated trace into RCS</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Importēt ģenerēto izsekošanu RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>In RCS, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match">Pakalpojuma RCS darbvietā <bpt id="p1">**</bpt>Elektroniskie pārskati<ept id="p1">**</ept> atlasiet elementu <bpt id="p2">**</bpt>Pārskatu veidošanas konfigurācijas<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, expand the <bpt id="p2">**</bpt>Performance trace model<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lapā <bpt id="p1">**</bpt>Konfigurācijas<ept id="p1">**</ept>, konfigurāciju kokā izvērsiet vienumu <bpt id="p2">**</bpt>Veiktspējas izsekošanas modelis<ept id="p2">**</ept> un atlasiet vienumu <bpt id="p3">**</bpt>Veiktspējas izsekošanas formāts<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Darbību rūtī atlasiet <bpt id="p1">**</bpt>Noformētājs<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>On the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Lapā <bpt id="p1">**</bpt>Formāta noformētājs<ept id="p1">**</ept>, darbību rūtī atlasiet <bpt id="p2">**</bpt>Veiktspējas izsekošana<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>In the <bpt id="p1">**</bpt>Performance trace result settings<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>Import performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dialoglodziņā <bpt id="p1">**</bpt>Veiktspējas izsekošanas rezultātu iestatījumi<ept id="p1">**</ept> atlasiet <bpt id="p2">**</bpt>Importēt veiktspējas izsekošanu<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the zip file that you exported from Finance and Operations earlier.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atlasiet <bpt id="p1">**</bpt>Pārlūkot<ept id="p1">**</ept>, lai atlasītu zip failu, ko iepriekš eksportējāt no programmas Finance and Operations.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Atlasiet <bpt id="p1">**</bpt>Labi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Performance trace result settings dialog box in RCS</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dialoglodziņš Veiktspējas izsekošanas rezultātu iestatījumi pakalpojumā RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use the performance trace for analysis in RCS – Format execution</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — formāta izpilde</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>In RCS, on the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Expand/collapse<ept id="p2">**</ept> to expand the content of all format items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pakalpojumā RCS, lapā <bpt id="p1">**</bpt>Formāta noformētājs<ept id="p1">**</ept> atlasiet <bpt id="p2">**</bpt>Izvērst/sakļaut<ept id="p2">**</ept>, lai izvērstu visu formāta vienumu saturu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Notice that additional information is shown for some items of the current format:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ņemiet vērā, ka dažiem pašreizējā formāta vienumiem tiek rādīta papildu informācija:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>The actual time that was spent entering data in the generated output by using the format item</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Faktiskais laiks, kas patērēts, ievadot datus ģenerētajā izvadē, izmantojot formāta vienumu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The same time expressed as a percentage of the total time that was spent generating the whole output</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tas pats laiks, kas izteikts procentos no kopējā laika, kurš patērēts, ģenerējot visu izvadi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Format designer page in RCS</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Formāta noformētāja lapa pakalpojumā RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Close <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Aizveriet lapu <bpt id="p1">**</bpt>Formāta noformētājs<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — modeļa kartējums</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> item.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Pakalpojuma RCS lapā <bpt id="p1">**</bpt>Konfigurācijas<ept id="p1">**</ept>, konfigurāciju kokā atlasiet vienumu <bpt id="p2">**</bpt>Veiktspējas izsekošanas kartējums<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="85" state="translated" state-qualifier="leveraged-inherited">Darbību rūtī atlasiet <bpt id="p1">**</bpt>Noformētājs<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Atlasiet <bpt id="p1">**</bpt>Noformētājs<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>On the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Lapā <bpt id="p1">**</bpt>Modeļa kartējuma noformētājs<ept id="p1">**</ept>, darbību rūtī atlasiet <bpt id="p2">**</bpt>Veiktspējas izsekošana<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Select the trace that you imported earlier.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atlasiet iepriekš importēto izsekošanu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Atlasiet <bpt id="p1">**</bpt>Labi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Notice that new information becomes available for some data source items of the current model mapping:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ņemiet vērā, ka kļūst pieejama jauna informācija par dažiem pašreizējā modeļa kartējuma datu avota vienumiem:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The actual time that was spent getting data by using the data source</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Faktiskais laiks, kas patērēts, iegūstot datus, izmantojot datu avotu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The same time expressed as a percentage of the total time that was spent running the whole model mapping</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Tas pats laiks, kas izteikts procentos no kopējā laika, kurš patērēts, palaižot visu modeļa kartējumu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source is run.</source><target logoport:matchpercent="0" state="translated">Ņemiet vērā, ka ER jūs informē par to, ka pašreizējais modeļa kartējums dublē datu bāzes pieprasījumus, kamēr tiek izpildīts VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum datu avots.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šāda dublēšana notiek tāpēc, ka kreditoru transakciju saraksts tiek izsaukts divas reizes katram atkārtotajam kreditora ierakstam:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>One call is made to enter details of each transaction in the data model, based on configured bindings.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Viens izsaukums tiek veikts, lai ievadītu informāciju par katru transakciju datu modelī, pamatojoties uz konfigurētajiem saistījumiem.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>One call is made to enter the calculated number of transactions per vendor in the data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Viens izsaukums tiek veikts, lai ievadītu aprēķināto transakciju skaitu katram kreditoram datu modelī.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Message about duplicate database requests on the Model mapping designer page in RCS</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ziņojums par datu bāzes pieprasījumu dublikātiem lapā Modeļa kartējuma noformētājs pakalpojumā RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vērtība <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> norāda, ka VendTrans tabula tika izsaukta 530 reizes, lai atgrieztu ierakstu no šīs tabulas uz VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum datu avotu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vērtība <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> norāda, ka VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum datu avots tika izsaukts 530 reizes, lai atgrieztu ierakstu no šī datu avota un ievadītu tā informāciju datu modelī.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>We recommend that you use caching for the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ieteicams izmantot kešdarbi VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum datu avotam, lai samazinātu izsaukumu skaitu, kas veikti, lai iegūtu informāciju par 265 transakcijām un palīdzētu uzlabot modeļa kartējuma veiktspēju.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tas arī var būt noderīgi, lai samazinātu LedgerTransTypeList datu avotam veikto izsaukumu skaitu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>This data source is used to associate each value of the <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> enumeration with its label.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šis datu avots tiek izmantots, lai katru <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> uzskaitījuma vērtību saistītu ar tā etiķeti.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Izmantojot šo datu avotu, varat atrast atbilstošu etiķeti un ievadīt to katras kreditora transakcijas datu modelī.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>The current number of calls to this data source (9,027) is quite high for 265 transactions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pašreizējais izsaukumu skaits šim datu avotam (9027) ir diezgan liels 265 transakcijām.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Model mapping designer page in RCS, showing 9,027 calls to the data source</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lapa Modeļa kartējuma noformētājs pakalpojumā RCS, kurā norādīti 9027 izsaukumi uz datu avotu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Improve the model mapping based on information from the execution trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Modeļa kartējuma uzlabošana, pamatojoties uz informāciju no izpildes izsekošanas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Modify the logic of the model mapping</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Modeļa kartējuma loģikas modificēšana</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Follow these steps to use caching, to help prevent duplicate calls to the database:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Veiciet šīs darbības, lai izmantotu kešdarbi, lai palīdzētu novērst dublētus izsaukumus datu bāzē.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>In RCS, on the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Data sources<ept id="p2">**</ept> pane, select the <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pakalpojuma RCS lapā <bpt id="p1">**</bpt>Modeļa kartējuma noformētājs<ept id="p1">**</ept>, rūtī <bpt id="p2">**</bpt>Datu avoti<ept id="p2">**</ept> atlasiet vienumu <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atlasiet <bpt id="p1">**</bpt>Kešatmiņa<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Expand the <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept> item, expand the list of one-to-many relations for the VendTable data source (the <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p2">**</ept> item), and select the <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Izvērsiet vienumu <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept>, izvērsiet “viens pret daudziem” relāciju sarakstu VendTable datu avotam (vienums <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Relācijas<ept id="p2">**</ept>) un atlasiet vienumu <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Atlasiet <bpt id="p1">**</bpt>Kešatmiņa<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Caching setup to help prevent duplicate calls</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kešdarbes iestatīšana, lai palīdzētu novērst dublētus izsaukumus</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Veiciet šīs darbības, lai LedgerTransTypeList datu avotu iekļautu VendTable datu avota tvērumā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>In the <bpt id="p1">**</bpt>Data source types<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>Functions<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Calculated field<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Rūtī <bpt id="p1">**</bpt>Datu avota tipi<ept id="p1">**</ept> izvērsiet vienumu <bpt id="p2">**</bpt>Funkcijas<ept id="p2">**</ept> un atlasiet vienumu <bpt id="p3">**</bpt>Aprēķinātais lauks<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, select the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Rūtī <bpt id="p1">**</bpt>Datu avoti<ept id="p1">**</ept> atlasiet vienumu <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Select <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Atlasiet <bpt id="p1">**</bpt>Pievienot<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept>.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Laukā <bpt id="p1">**</bpt>Nosaukums<ept id="p1">**</ept> ievadiet <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match">Atlasiet <bpt id="p1">**</bpt>Rediģēt formulu<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept>.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match">Laukā <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> ievadiet <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Atlasiet <bpt id="p1">**</bpt>Saglabāt<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Aizveriet lapu <bpt id="p1">**</bpt>Formulas redaktors<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Labi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Follow these steps to do caching of the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> field:</source><target logoport:matchpercent="0" state="translated">Veiciet šīs darbības, lai veiktu lauka <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> kešdarbi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Select the <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept> item.</source><target logoport:matchpercent="0" state="translated">Atlasiet vienumu <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Atlasiet <bpt id="p1">**</bpt>Kešatmiņa<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Select the <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> item.</source><target logoport:matchpercent="0" state="translated">Atlasiet vienumu <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Atlasiet <bpt id="p1">**</bpt>Kešatmiņa<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Caching setup for the $TransType field</source><target logoport:matchpercent="0" state="translated">Kešdarbes iestatīšana laukam $TransType</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Follow these steps to change the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> field so that it starts to use the cached <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept> field:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Veiciet šīs darbības, lai mainītu lauku <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept>, lai tas sāktu izmantot kešoto lauku <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item, expand the <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p3">**</ept> item, expand the <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> item, and select the <bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Rūtī <bpt id="p1">**</bpt>Datu avoti<ept id="p1">**</ept> izvērsiet vienumu <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept>, izvērsiet vienumu <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Relācijas<ept id="p3">**</ept>, izvērsiet vienumu <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> un atlasiet vienumu <bpt id="p5">**</bpt>VendTable.VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Select <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Atlasiet <bpt id="p1">**</bpt>Rediģēt<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Atlasiet <bpt id="p1">**</bpt>Rediģēt formulu<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, find the following expression:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Laukā <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> atrodiet šādu izteiksmi:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</source><target logoport:matchpercent="0" state="translated">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter the following expression:</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Laukā <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> ievadiet šādu izteiksmi:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</source><target logoport:matchpercent="0" state="translated">FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Atlasiet <bpt id="p1">**</bpt>Saglabāt<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Aizveriet lapu <bpt id="p1">**</bpt>Formulas redaktors<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Atlasiet <bpt id="p1">**</bpt>Labi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Atlasiet <bpt id="p1">**</bpt>Saglabāt<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Close the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Aizveriet lapu <bpt id="p1">**</bpt>Modeļa kartējuma noformētājs<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Close the <bpt id="p1">**</bpt>Model mappings<ept id="p1">**</ept> page.</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match">Aizveriet lapu <bpt id="p1">**</bpt>Modeļa kartējumi<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Complete the modified version of the ER model mapping</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER modeļa kartējuma modificētās versijas pabeigšana</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Versions<ept id="p2">**</ept> FastTab, select version <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> of the <bpt id="p4">**</bpt>Performance trace mapping<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pakalpojuma RCS lapā <bpt id="p1">**</bpt>Konfigurācijas<ept id="p1">**</ept>, kopsavilkuma cilnē <bpt id="p2">**</bpt>Versijas<ept id="p2">**</ept> atlasiet konfigurācijas <bpt id="p4">**</bpt>Veiktspējas izsekošanas kartējums<ept id="p4">**</ept> versiju <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Select <bpt id="p1">**</bpt>Change status<ept id="p1">**</ept>.</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match">Atlasiet <bpt id="p1">**</bpt>Mainīt statusu<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Select <bpt id="p1">**</bpt>Complete<ept id="p1">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Atlasiet <bpt id="p1">**</bpt>Pabeigt<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Import the modified ER model mapping configuration from RCS into Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Modificētās ER modeļa kartējuma konfigurācijas importēšana no RCS programmā Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import an ER configuration from RCS into Finance and Operations<ept id="p1">](#import-configuration)</ept> section earlier in this topic to import version 1.2 of the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> configuration into Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atkārtojiet šīs tēmas iepriekšējā sadaļā <bpt id="p1">[</bpt>ER konfigurācijas importēšana no pakalpojuma RCS programmā Finance and Operations<ept id="p1">](#import-configuration)</ept> minētās darbības, lai importētu konfigurācijas <bpt id="p2">**</bpt>Veiktspējas izsekošanas kartējums<ept id="p2">**</ept> versiju 1.2 programmā Finance and Operations.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Run the modified ER solution to trace execution</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Modificētā ER risinājuma palaišana, lai izsekotu izpildi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Run the ER format</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">ER formāta palaišana</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atkārtojiet šīs tēmas iepriekšējā sadaļā <bpt id="p1">[</bpt>ER formāta palaišana<ept id="p1">](#run-format)</ept> minētās darbības, lai ģenerētu jaunu veiktspējas izsekošanu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Review the execution trace</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Izpildes izsekošanas pārskatīšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Eksportēt ģenerēto izsekošanu no programmas Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Export the generated trace from Finance and Operations<ept id="p1">](#export-trace)</ept> section earlier in this topic to save a new performance trace locally.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atkārtojiet šīs tēmas iepriekšējā sadaļā <bpt id="p1">[</bpt>Eksportēt ģenerēto izsekošanu no programmas Finance and Operations<ept id="p1">](#export-trace)</ept> minētās darbības, lai saglabātu jaunu veiktspējas izsekošanu lokāli.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Import the generated trace into RCS</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Importēt ģenerēto izsekošanu RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import the generated trace into RCS<ept id="p1">](#import-trace)</ept> section earlier in this topic to import the new performance trace into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atkārtojiet šīs tēmas iepriekšējā sadaļā <bpt id="p1">[</bpt>Importēt ģenerēto izsekošanu RCS<ept id="p1">](#import-trace)</ept> minētās darbības, lai importētu jauno veiktspējas izsekošanu pakalpojumā RCS.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — modeļa kartējums</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Use the performance trace for analysis in RCS – Model mapping<ept id="p1">](#use-trace)</ept> section earlier in this topic to analyze the latest performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atkārtojiet šīs tēmas iepriekšējā sadaļā <bpt id="p1">[</bpt>Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — modeļa kartējums<ept id="p1">](#use-trace)</ept> minētās darbības, lai analizētu jaunāko veiktspējas izsekošanu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ņemiet vērā, ka korekcijas, kuras veicāt modeļa kartējumam, likvidēja datu bāzes vaicājumu dublikātus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>The number of calls to database tables and data sources for this model mapping has been also reduced.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Datu bāzu tabulu un datu avotu izsaukumu skaits šim modeļa kartējumam arī ir samazināts.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Therefore, the performance of the whole ER solution has improved.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tādēļ ir uzlabojusies ER risinājuma kopējā veiktspēja.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Trace information for the VendTable data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Izsekot informāciju par VendTable datu avotu lapā Modeļa kartējuma noformētājs pakalpojumā RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>In the trace information, the value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> for the VendTable data source indicates that this data source was called 12 times.</source><target logoport:matchpercent="0" state="translated">Izsekošanas informācijā VendTable datu avota vērtība <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> norāda, ka šis datu avots tika izsaukts 12 reizes.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that six calls were translated to database calls to the VendTable table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vērtība <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> norāda, ka seši izsaukumi tika pārveidoti par datu bāzes izsaukumiem uz VendTable tabulu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vērtība <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> norāda, ka ieraksti, kas tika ienesti no datu bāzes, tika kešoti, un seši citi izsaukumi tika apstrādāti, izmantojot kešatmiņu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ņemiet vērā, ka LedgerTransTypeList datu avota izsaukumu skaits ir samazināts no 9027 līdz 240.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Trace information for the LedgerTransTypeList data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Izsekot informāciju par LedgerTransTypeList datu avotu lapā Modeļa kartējuma noformētājs pakalpojumā RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Review the execution trace in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pārskatīt izpildes izsekošanu programmā Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Papildus pakalpojumam RCS dažas Finance and Operations versijas var nodrošināt ER struktūras noformētāja iespējas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>These versions of Finance and Operations have an <bpt id="p1">**</bpt>Enable design mode<ept id="p1">**</ept> option that can be turned on.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šīm Finance and Operations versijām ir opcija <bpt id="p1">**</bpt>Iespējot noformēšanas režīmu<ept id="p1">**</ept>, ko var ieslēgt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>You can find this option on the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept> page, which you can open from the <bpt id="p3">**</bpt>Electronic reporting<ept id="p3">**</ept> workspace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šo opciju var atrast lapas <bpt id="p2">**</bpt>Elektronisko pārskatu veidošanas parametri<ept id="p2">**</ept> cilnē <bpt id="p1">**</bpt>Vispārīgi<ept id="p1">**</ept>, kuru varat atvērt, izmantojot darbvietu <bpt id="p3">**</bpt>Elektronisko pārskatu veidošana<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Enable design mode option on the Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Opcija Iespējot noformēšanas režīmu lapā Elektronisko pārskatu veidošanas parametri programmā Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ja izmantojat vienu no šīm Finance and Operations versijām, varat analizēt ģenerēto veiktspējas izsekošanu informāciju tieši programmā Finance and Operations.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>You don't have to export them from Finance and Operation and import them into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tās nav jāeksportē no Finance and Operations un jāimportē pakalpojumā RCS.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Review the execution trace by using external tools</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pārskatīt izpildes izsekošanu, izmantojot ārējos rīkus</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Configure user parameters</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Konfigurēt lietotāja parametrus</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="72" state="translated" state-qualifier="leveraged-inherited">Risinājumā Finance and Operations dodieties uz sadaļu <bpt id="p1">**</bpt>Organizācijas administrēšana <ph id="ph1">\&gt;</ph> Elektronisko pārskatu veidošana <ph id="ph2">\&gt;</ph> Konfigurācijas<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="72" state="translated" state-qualifier="leveraged-inherited">Lapas <bpt id="p1">**</bpt>Konfigurācijas<ept id="p1">**</ept> darbību rūtī, cilnē <bpt id="p2">**</bpt>Konfigurācijas<ept id="p2">**</ept>, grupā <bpt id="p3">**</bpt>Papildu iestatījumi<ept id="p3">**</ept> atlasiet vienumu <bpt id="p4">**</bpt>Lietotāja parametri<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, in the <bpt id="p3">**</bpt>Execution trace format<ept id="p3">**</ept> field, select <bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dialoglodziņā <bpt id="p1">**</bpt>Lietotāja parametri<ept id="p1">**</ept>, sadaļā <bpt id="p2">**</bpt>Izpildes izsekošana<ept id="p2">**</ept>, laukā <bpt id="p3">**</bpt>Izpildes izsekošanas formāts<ept id="p3">**</ept> atlasiet <bpt id="p4">**</bpt>PerfView XML.<ept id="p4">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Run the ER format</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">ER formāta palaišana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Atkārtojiet šīs tēmas iepriekšējā sadaļā <bpt id="p1">[</bpt>ER formāta palaišana<ept id="p1">](#run-format)</ept> minētās darbības, lai ģenerētu jaunu veiktspējas izsekošanu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Notice that the web browser offers a zip file for download.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ņemiet vērā, ka tīmekļa pārlūkprogramma piedāvā lejupielādēt zip failu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>This file contains the performance trace in PerfView format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šis fails satur veiktspējas izsekošanu PerfView formātā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pēc tam varat izmantot PerfView veiktspējas analīzes rīku, lai analizētu ER formāta izpildes informāciju.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>