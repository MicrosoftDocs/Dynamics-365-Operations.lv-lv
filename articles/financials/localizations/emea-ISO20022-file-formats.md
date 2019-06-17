<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="emea-ISO20022-file-formats.md" target-language="lv-LV">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>emea-ISO20022-file-formats.35e138.d91e937c62d4d498e67d753e39676514835f4161.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d91e937c62d4d498e67d753e39676514835f4161</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\localizations\emea-ISO20022-file-formats.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>ISO20022 files import</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISO20022 failu importēšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to import payment files of the ISO 20022 camt.054 and pain.002 formats into Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā tēmā ir paskaidrots, kā programmā Microsoft Dynamics 365 for Finance and Operations importēt ISO 20022 camt.054 un pain.002 formāta maksājumu failus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Import ISO20022 files</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISO20022 failu importēšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>You can import payment files that have the following formats:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varat importēt maksājumu failus, kas ir tālāk norādītajos formātos.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source><bpt id="p1">**</bpt>ISO20022 camt.054 credit advice<ept id="p1">**</ept> – Import incoming payments from a file in this format into the Customer payment journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISO20022 camt.054 kredīta izziņa<ept id="p1">**</ept> – importējiet ienākošos maksājumus no šī formāta faila debitoru maksājumu žurnālā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source><bpt id="p1">**</bpt>ISO20022 pain.002 status return<ept id="p1">**</ept> and <bpt id="p2">**</bpt>ISO20022 camt.054 debit advice<ept id="p2">**</ept> – Import return files in these formats into the AP Payment transfer journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISO20022 pain.002 atgrieztais statuss<ept id="p1">**</ept> un <bpt id="p2">**</bpt>ISO20022 camt.054 debeta izziņa<ept id="p2">**</ept> — importējiet atgriešanas failus šajos formātos kreditoru maksājumu pārsūtījumu žurnālā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites for importing the camt.054 credit advice file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Priekšnosacījumi camt.054 kredīta izziņas faila importēšanai</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You must complete the following prerequisites to import bank notification messages in the camt.054.001.002 format into the Customer payment journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai bankas paziņojumus camt.054.001.002 formātā varētu importēt debitoru maksājumu žurnālā, jums ir jāizpilda tālāk norādītie priekšnosacījumi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Import the <bpt id="p1">**</bpt>ISO20022 camt.054<ept id="p1">**</ept> Electronic reporting (ER) configuration from Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Importējiet <bpt id="p1">**</bpt>ISO20022 camt.054<ept id="p1">**</ept> formāta elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurāciju no portāla Microsoft Dynamics Lifecycle Services (LCS).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Then, on the <bpt id="p1">**</bpt>Customer method of payment<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Import format configuration<ept id="p2">**</ept> field, select that configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pēc tam lapas <bpt id="p1">**</bpt>Debitora maksāšanas metode<ept id="p1">**</ept> laukā <bpt id="p2">**</bpt>Importēt formāta konfigurāciju<ept id="p2">**</ept> atlasiet šo konfigurāciju.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For more information, see <bpt id="p1">[</bpt>File formats for methods of payment<ept id="p1">](emea-select-file-formats-for-the-method-of-payments.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Papildinformāciju skatiet rakstā <bpt id="p1">[</bpt>Maksāšanas metožu failu formāti<ept id="p1">](emea-select-file-formats-for-the-method-of-payments.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>On the <bpt id="p1">**</bpt>All customers<ept id="p1">**</ept> page, enter a name and organization number for each customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lapā <bpt id="p1">**</bpt>Visi debitori<ept id="p1">**</ept> ievadiet katra debitora nosaukumu un organizācijas numuru.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>On the <bpt id="p1">**</bpt>Customer bank account<ept id="p1">**</ept> page, set up a customer bank account record by entering the following information: IBAN or bank account number, and SWIFT code or routing number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lapā <bpt id="p1">**</bpt>Debitora bankas konts<ept id="p1">**</ept> iestatiet debitora bankas konta ierakstu, ievadot šādu informāciju: IBAN vai bankas konta numurs un SWIFT kods vai reģistrācijas numurs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>On the <bpt id="p1">**</bpt>Bank accounts<ept id="p1">**</ept> page, set up legal entity bank accounts by entering the following information: IBAN or bank account number, SWIFT code or routing number, currency, and address.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lapā <bpt id="p1">**</bpt>Bankas konti<ept id="p1">**</ept> iestatiet juridiskās personas bankas kontus, ievadot šādu informāciju: IBAN vai bankas konta numurs un SWIFT kods vai reģistrācijas numurs, valūta un adrese.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If you plan to use Advanced bank reconciliation, on the <bpt id="p1">**</bpt>Reconciliation<ept id="p1">**</ept> FastTab, set the <bpt id="p2">**</bpt>Advanced bank reconciliation<ept id="p2">**</ept> option to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja plānojat izmantot opciju Detalizēta bankas darbību saskaņošana, kopsavilkuma cilnē <bpt id="p1">**</bpt>Saskaņošana<ept id="p1">**</ept> opciju <bpt id="p2">**</bpt>Detalizēta bankas darbību saskaņošana<ept id="p2">**</ept> iestatiet uz <bpt id="p3">**</bpt>Jā<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>If you plan to reconcile unposted imported payments, set the <bpt id="p1">**</bpt>Use bank statements as confirmation of electronic payments<ept id="p1">**</ept> option to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja plānojat saskaņot negrāmatotos importētos maksājumus, opciju <bpt id="p1">**</bpt>Lietot bankas izrakstus kā elektronisko maksājumu apstiprinājumu<ept id="p1">**</ept> iestatiet uz <bpt id="p2">**</bpt>Jā<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Optional: On the <bpt id="p1">**</bpt>Transaction code mapping<ept id="p1">**</ept> page, set up the mapping between bank transaction codes in the file and bank transaction types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Neobligāti: lapā <bpt id="p1">**</bpt>Transakciju kodu kartēšana<ept id="p1">**</ept> iestatiet kartēšanu starp bankas transakciju kodiem failā un bankas transakciju tipiem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>If the file contains transaction charges that you want to post together with the incoming payment, create a payment fee on the <bpt id="p1">**</bpt>Customer payment fee<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja fails satur transakciju maksas, ko vēlaties grāmatot kopā ar ienākošo maksājumu, izveidojiet komisijas maksu lapā <bpt id="p1">**</bpt>Debitoru komisijas maksas<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Then, on the <bpt id="p1">**</bpt>Methods of payment<ept id="p1">**</ept> page, associate the payment fee with the bank account in the payment fee setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pēc tam lapā <bpt id="p1">**</bpt>Maksāšanas metodes<ept id="p1">**</ept> saistiet komisijas maksu ar bankas kontu komisijas maksu iestatījumos.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>If ESR payments will be imported and will contain ISR references (applicable for legal entities in Switzerland), complete the following setup:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja ESR maksājumi tiks importēti un saturēs ISR atsauces (attiecas uz juridiskajām personām Šveicē), veiciet tālāk norādītos iestatījumus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In the <bpt id="p1">**</bpt>Customer payments, account lengths<ept id="p1">**</ept> field, enter the length of the customer code that is used in ISR references or for automatic identification of the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Laukā <bpt id="p1">**</bpt>Debitoru maksājumi, kontu garumi<ept id="p1">**</ept> ievadiet garumu debitora kodam, kas tiek izmantots ISR atsaucēs vai automātiskai debitora identifikācijai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Make sure that the customer number and invoice number (number sequences) contain only digits.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārliecinieties, vai debitora numurs un rēķina numurs (numuru sērijas) satur tikai ciparus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>They must contain no other characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tajos nedrīkst būt ietvertas citas rakstzīmes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The invoice number must not have leading zeros.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rēķina numurs nedrīkst sākties ar nullēm.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Enter the ESR, BESR, and routing number for the legal entity bank account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ievadiet ESR, BESR un reģistrācijas numuru juridiskās personas bankas kontam.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For more information, see <bpt id="p1">[</bpt>legacy ESR feature<ept id="p1">](emea-che-esr-customer-payments-import.md)</ept>, because similar settings are required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Papildinformāciju skatiet rakstā <bpt id="p1">[</bpt>Mantojuma ESR līdzeklis<ept id="p1">](emea-che-esr-customer-payments-import.md)</ept>, jo tajā ir nepieciešami līdzīgi iestatījumi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Import the camt.054 credit advice file into the Customer payment journal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">camt.054 kredīta izziņas faila importēšana debitoru maksājumu žurnālā</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>On the <bpt id="p1">**</bpt>Customer payment journal lines<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Functions<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>Import payments<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lapā <bpt id="p1">**</bpt>Debitoru maksājumu žurnāla rindas<ept id="p1">**</ept> noklikšķiniet uz <bpt id="p2">**</bpt>Funkcijas<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>Importēt maksājumus<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Select the method of payment that has the required settings for the ISO20022 camt.054 format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Atlasiet maksāšanas metodi, kam ir ISO20022 camt.054 formātam nepieciešamie iestatījumi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Specify the required parameters and the path of the file, and then click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Norādiet nepieciešamos parametrus un faila ceļu un pēc tam noklikšķiniet uz <bpt id="p1">**</bpt>Labi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The file is imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fails tiek importēts.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Prerequisites for importing files in the pain.002 status return and camt.054 debit advice formats into the AP Payment transfer journal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Priekšnosacījumi failu importēšanai pain.002 atgrieztā statusa un camt.054 debeta izziņas formātos kreditoru maksājumu pārsūtījumu žurnālā</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>You must complete the following prerequisites to import bank messages in the following ISO20022 formats to the <bpt id="p1">**</bpt>Vendor payment transfer<ept id="p1">**</ept> page: pain.002.001.003 status return messages and camt.054.001.002 debit advice.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai bankas ziņojumus importētu šādos ISO20022 formātos lapā <bpt id="p1">**</bpt>Kreditoru maksājumu pārsūtīšana<ept id="p1">**</ept>: pain.002.001.003 atgrieztā statusa ziņojumi un camt.054.001.002 debeta izziņa, ir jāizpilda tālāk norādītie priekšnosacījumi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Import the <bpt id="p1">**</bpt>ISO20022 camt.054<ept id="p1">**</ept> and <bpt id="p2">**</bpt>ISO20022 pain.002<ept id="p2">**</ept> ER configurations from LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Importējiet <bpt id="p1">**</bpt>ISO20022 camt.054<ept id="p1">**</ept> un <bpt id="p2">**</bpt>ISO20022 pain.002<ept id="p2">**</ept> ER konfigurācijas no LCS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>On the <bpt id="p1">**</bpt>Vendor method of payment<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Return format configuration<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Return format secondary configuration<ept id="p3">**</ept> fields, select the ER configurations that you imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lapas <bpt id="p1">**</bpt>Kreditora maksāšanas metode<ept id="p1">**</ept> laukos <bpt id="p2">**</bpt>Atgriešanas formāta konfigurācija<ept id="p2">**</ept> un <bpt id="p3">**</bpt>Atgriešanas formāta sekundārā konfigurācija<ept id="p3">**</ept> atlasiet ER konfigurācijas, ko importējāt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>You will have to activate the generic electronic return format for the selected method of payment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jums būs jāaktivizē vispārīgais elektroniskās atgriešanas formāts atlasītajai maksāšanas metodei.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>On the <bpt id="p1">**</bpt>Return format status mapping<ept id="p1">**</ept> page, set up the mapping of status codes between pain.002 statuses and Vendor payment journal statuses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lapā <bpt id="p1">**</bpt>Atgriešanas formāta statusa kartēšana<ept id="p1">**</ept> iestatiet statusa kodu kartējumu starp pain.002 statusiem un kreditoru maksājumu žurnāla statusiem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Here is an example of a status setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tālāk ir sniegts statusa iestatījumu piemērs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Return status</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Atgrieztais statuss</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Payment status</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maksājuma statuss</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>RJCT</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RJCT</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Rejected</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Noraidījis</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>ACCP</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ACCP</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Accepted</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pieņemts</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>ACSP</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ACSP</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Received</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Saņemts</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>On the <bpt id="p1">**</bpt>Return format error codes<ept id="p1">**</ept> page, set up pain.002 error codes and descriptions in accordance with external ISO20022 status reason codes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lapā <bpt id="p1">**</bpt>Atgriešanas formāta kļūdu kodi<ept id="p1">**</ept> iestatiet pain.002 kļūdu kodus un aprakstus saskaņā ar ārējā ISO20022 statusa iemesla kodiem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Here is an example of part of an error code setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tālāk ir sniegts piemērs ar daļu no kļūdas koda iestatījuma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kods</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nosaukums</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>AC01</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AC01</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>IncorrectAccountNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IncorrectAccountNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>AC02</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AC02</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>InvalidDebtorAccountNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InvalidDebtorAccountNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>AC03</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AC03</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>InvalidCreditorAccountNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InvalidCreditorAccountNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>AC04</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AC04</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>ClosedAccountNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ClosedAccountNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>AC05</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AC05</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>ClosedDebtorAccountNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ClosedDebtorAccountNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>AC06</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AC06</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>BlockedAccount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BlockedAccount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>If the camt.054 file contains transaction charges that you want to post together with the incoming payment, create a payment fee on the <bpt id="p1">**</bpt>Vendor payment fee<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja camt.054 fails satur transakciju maksas, ko vēlaties grāmatot kopā ar ienākošo maksājumu, izveidojiet komisijas maksu lapā <bpt id="p1">**</bpt>Kreditoru komisijas maksas<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Then, on the <bpt id="p1">**</bpt>Methods of payment<ept id="p1">**</ept> page, associate the payment fee with the bank account in the payment fee setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pēc tam lapā <bpt id="p1">**</bpt>Maksāšanas metodes<ept id="p1">**</ept> saistiet komisijas maksu ar bankas kontu komisijas maksu iestatījumos.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Import the pain.002 status return or camt.054 debit advice files into the Vendor payment journal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">pain.002 atgrieztā statusa vai camt.054 debeta izziņas failu importēšana kreditoru maksājumu žurnālā</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Open the <bpt id="p1">**</bpt>Payment transfers<ept id="p1">**</ept> page in Accounts Payable menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Izvēlnē Kreditori atveriet lapu <bpt id="p1">**</bpt>Maksājumu pārsūtījumi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>On the <bpt id="p1">**</bpt>Payment transfers<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Return file - vendor<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lapā <bpt id="p1">**</bpt>Maksājumu pārsūtījumi<ept id="p1">**</ept> noklikšķiniet uz <bpt id="p2">**</bpt>Ievades fails — kreditors<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Select the method of payment that has the required settings for ISO20022 files, and then click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Atlasiet maksāšanas metodi, kam ir ISO20022 failiem nepieciešamie iestatījumi, un pēc tam noklikšķiniet uz <bpt id="p1">**</bpt>Labi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Select the file format that you plan to import, and then click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Atlasiet faila formātu, ko plānojat importēt, un pēc tam noklikšķiniet uz <bpt id="p1">**</bpt>Labi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Specify the required parameters and the path of the file, and then click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Norādiet nepieciešamos parametrus un faila ceļu un pēc tam noklikšķiniet uz <bpt id="p1">**</bpt>Labi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>If you're importing the pain.002 file, the status of vendor payment lines is updated, based the information in the imported file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja importējat pain.002 failu, tiek atjaunināts kreditora maksājumu rindu statuss, pamatojoties uz importētā faila informāciju.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>If you're importing the camt.054 file, you should specify the following additional parameters:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja importējat camt.054 failu, jums ir jānorāda tālāk norādītie papildu parametri.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">**</bpt>Fee ID<ept id="p1">**</ept> – Enter the Fee ID which will define new payment fee lines, which will be created on the Vendor payment journal line if a charge amount is present in the camt.054 file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Maksas ID<ept id="p1">**</ept> — ievadiet maksas ID, kas definēs jaunās komisijas maksas rindas, kuras tiks izveidotas kreditoru maksājumu žurnāla rindā, ja camt.054 failā būs maksas summa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">**</bpt>New journal name<ept id="p1">**</ept> and <bpt id="p2">**</bpt>New journal description<ept id="p2">**</ept> – Enter the name and description of the journal that processed transactions will be transferred to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Jauna žurnāla nosaukums<ept id="p1">**</ept> un <bpt id="p2">**</bpt>Jauna žurnāla apraksts<ept id="p2">**</ept> — ievadiet tā žurnāla nosaukumu un aprakstu, uz kuru tiks pārsūtītas apstrādātās transakcijas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>After the transfer, new voucher numbers should be assigned in the new journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pēc pārsūtīšanas jaunajā žurnālā ir jāpiešķir jauni dokumentu numuri.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source><bpt id="p1">**</bpt>Import direct debit transactions<ept id="p1">**</ept> – Set this option to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> if outgoing direct debits must be imported into the Vendor payment journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Importēt tiešā debeta transakcijas<ept id="p1">**</ept> — iestatiet šo opciju uz <bpt id="p2">**</bpt>Jā<ept id="p2">**</ept>, ja izejošie tiešie debeti ir jāimportē kreditoru maksājumu žurnālā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source><bpt id="p1">**</bpt>Journal name<ept id="p1">**</ept> – Define a new journal name for the imported direct debit transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Žurnāla nosaukums<ept id="p1">**</ept> — definējiet jaunu žurnāla nosaukumu importētajām tiešā debeta transakcijām.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source><bpt id="p1">**</bpt>Settle transactions<ept id="p1">**</ept> – Set this option to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> if imported vendor payments must be settled with invoices that are found in the system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Transakciju nosegšana<ept id="p1">**</ept> — iestatiet šo opciju uz <bpt id="p2">**</bpt>Jā<ept id="p2">**</ept>, ja importētie kreditoru maksājumi ir jānosedz ar rēķiniem, kas ir atrasti sistēmā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>You can view the imported information on the <bpt id="p1">**</bpt>Payment transfers<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Importēto informāciju var skatīt lapā <bpt id="p1">**</bpt>Maksājumu pārsūtījumi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Additional details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Papildu informācija</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>When you import a format configuration from LCS, you import the whole configuration tree which means that the Model and Model mapping configurations are included.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Importējot formāta konfigurāciju no LCS, tiek importēts viss konfigurācijas koks, un tas nozīmē, ka ir iekļauts modelis un modeļa kartēšana konfigurācijas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>In the Payment model starting from version 8, the mappings are located in separate ER configurations in the solution tree (Payment model mapping 1611, Payment model mapping to destination ISO20022, etc).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sākot no 8. versijas, maksājumu modelī kartējumi atrodas risinājumu kokā atsevišķās ER konfigurācijās (maksājumu modeļa kartējums 1611, maksājumu modeļa kartējums līdz galamērķim ISO20022 utt.).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>There are many different payment formats under one model (Payment model), thus separate mapping handling is a key for easy solution maintenance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Atsevišķā modelī ir daudz dažādu maksājuma formātu (maksājuma modelis), tādējādi kartējumu apstrāde ir galvenais nosacījums vienkāršai risinājuma uzturēšanai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>For example, consider this scenario: you use ISO20022 payments to generate credit transfer files and then you import the return messages from the bank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Piemērs. Jūs izmantojat ISO20022 maksājumus, lai ģenerētu kredīta pārskaitījuma failus, un pēc tam importējat atbildes ziņojumus no bankas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>In this scenario, you should use the following configurations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šādā scenārijā jums būtu jāizmanto šādas konfigurācijas:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source><bpt id="p1">**</bpt>Payment model<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Maksājuma modelis<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source><bpt id="p1">**</bpt>Payment model mapping 1611<ept id="p1">**</ept> – this mapping will be used to generate the export file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Maksājumu modeļa kartējums 1611<ept id="p1">**</ept> — šis kartējums tiks lietots, lai ģenerētu eksporta failu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source><bpt id="p1">**</bpt>Payment model mapping to destination ISO20022<ept id="p1">**</ept> – this configuration includes all mappings which will be used to import the data (“to destination” mapping direction)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Maksājumu modeļa kartējums līdz galamērķim ISO20022<ept id="p1">**</ept> — šajā konfigurācijā ir iekļauti visi kartējumi, kas tiks izmantoti datu importēšanai (kartējuma virziens: "uz galamērķi")</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>ISO20022 Credit transfer<ept id="p1">**</ept> – this configuration includes a format component that is responsible for export file generation (pain.001) based on the Payment model mapping 1611, as well as a format to model mapping component which will be used together with Payment model mapping to destination ISO20022 to register exported payments in the system for further import purposes (import in CustVendProcessedPayments technical table)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISO20022 kredīta pārskaitījums<ept id="p1">**</ept> — šajā konfigurācijā ir iekļauts formāta komponents, kas ir atbildīgs par eksporta faila ģenerēšana (pain.001), pamatojoties uz maksājumu modeļa kartējumu 1611, kā arī formāta-modeļa kartējuma komponents, kas tiks izmantots kopā ar maksājumu modeļa kartējumu līdz galamērķim ISO20022, lai reģistrētu eksportētos maksājumus sistēmā turpmākas importēšanas vajadzībām (importēšana tehniskajā tabulā CustVendProcessedPayments)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>ISO20022 Credit transfer (CE)<ept id="p1">**</ept>, where CE correspond to country extension – derived format to the ISO20022 Credit transfer with the same structure and with certain country-specific differences</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISO20022 pārskaitījums (CE)<ept id="p1">**</ept>, kur CE atbilst valsts paplašinājumam — ISO20022 kredīta pārskaitījuma atvasināts formāts ar tādu pašu struktūru un konkrētajai valstij raksturīgam atšķirībām</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Pain.002<ept id="p1">**</ept> – this format will be used together with the Payment model mapping to destination ISO20022 in order to import the pain.002 file into vendor payments transfers journal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Pain.002<ept id="p1">**</ept> — šis formāts tiks izmantots kopā ar maksājumu modeļa kartējumu līdz galamērķim ISO20022, lai importētu failu pain.002 kreditoru maksājumu pārskaitījumu žurnālu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source><bpt id="p1">**</bpt>Camt.054<ept id="p1">**</ept> – this format will be used together with the Payment model mapping to destination ISO20022 to import the camt.054 file into vendor payments transfers journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Camt.054<ept id="p1">**</ept> — šis formāts tiks izmantots kopā ar maksājumu modeļa kartējumu līdz galamērķim ISO20022, lai importētu failu camt.054 kreditoru maksājumu pārskaitījumu žurnālu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The same format configuration will be used in customer payments import functionality, but the different mapping will be used in the Payment model mapping to destination ISO20022 configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tāda pati formātu konfigurācija tiks izmantota debitoru maksājumu importēšanas funkcionalitātē, tomēr atšķirīgs kartējums tiks izmantots maksājumu modeļa kartējumā līdz galamērķa ISO20022 konfigurācijai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>For more information about Electronic reporting, refer to <bpt id="p1">[</bpt>Electronic reporting overview<ept id="p1">](../../dev-itpro/analytics/general-electronic-reporting.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Plašāku informāciju par elektronisko pārskatu veidošanu skatiet šeit: <bpt id="p1">[</bpt>Elektronisko pārskatu veidošanas apskats<ept id="p1">](../../dev-itpro/analytics/general-electronic-reporting.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Papildu resursi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source><bpt id="p1">[</bpt>Create and export vendor payments using ISO20022 payment format<ept id="p1">](./tasks/create-export-vendor-payments-iso20022-payment-format.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Kreditoru maksājumu izveide un eksportēšana, izmantojot maksājumu formātu ISO20022<ept id="p1">](./tasks/create-export-vendor-payments-iso20022-payment-format.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">[</bpt>Import ISO20022 credit transfer configuration<ept id="p1">](./tasks/import-iso20022-credit-transfer-configuration.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>ISO20022 pārvietošanai kredītā konfigurācijas importēšana<ept id="p1">](./tasks/import-iso20022-credit-transfer-configuration.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source><bpt id="p1">[</bpt>Import ISO20022 direct debit configuration<ept id="p1">](./tasks/import-iso20022-direct-debit-configuration.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>ISO20022 tiešā debeta konfigurācijas importēšana<ept id="p1">](./tasks/import-iso20022-direct-debit-configuration.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">[</bpt>Set up company bank accounts for ISO20022 credit transfers<ept id="p1">](./tasks/set-up-company-bank-accounts-iso20022-credit-transfers.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Uzņēmuma bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem<ept id="p1">](./tasks/set-up-company-bank-accounts-iso20022-credit-transfers.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">[</bpt>Set up company bank accounts for ISO20022 direct debits<ept id="p1">](./tasks/set-up-company-bank-accounts-iso20022-direct-debits.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Uzņēmuma bankas kontu iestatīšana ISO20022 tiešajiem debetiem<ept id="p1">](./tasks/set-up-company-bank-accounts-iso20022-direct-debits.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">[</bpt>Set up customers and customer bank accounts for ISO20022 direct debits<ept id="p1">](./tasks/set-up-bank-accounts-iso20022-direct-debits.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Debitoru un debitoru bankas kontu iestatīšana ISO20022 tiešajiem debetiem<ept id="p1">](./tasks/set-up-bank-accounts-iso20022-direct-debits.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source><bpt id="p1">[</bpt>Set up method of payment for ISO20022 credit transfer<ept id="p1">](./tasks/set-up-method-payment-iso20022-credit-transfer.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Maksājuma metodes iestatīšana ISO20022 pārvietošanai kredītā<ept id="p1">](./tasks/set-up-method-payment-iso20022-credit-transfer.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">[</bpt>Set up method of payment for ISO20022 direct debit<ept id="p1">](./tasks/setup-method-payment-iso20022-direct-debit.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Maksājumu metodes iestatīšana ISO20022 tiešajam debetam<ept id="p1">](./tasks/setup-method-payment-iso20022-direct-debit.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source><bpt id="p1">[</bpt>Set up vendors and vendor bank accounts for ISO20022 credit transfers<ept id="p1">](./tasks/set-up-vendor-iso20022-credit-transfers.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Kreditoru un kreditoru bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem<ept id="p1">](./tasks/set-up-vendor-iso20022-credit-transfers.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>