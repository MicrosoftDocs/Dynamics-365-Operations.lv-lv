<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="custom-fields-mobile.md" target-language="lv-LV">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>custom-fields-mobile.2a9e5e.4343c875da05641c57b7784bf52f1c814dd26d20.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4343c875da05641c57b7784bf52f1c814dd26d20</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>19859d8566a8c7840066b2c10c6b08b67f1b83f4</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/04/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\project-management\custom-fields-mobile.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit logoport:updated-at="2019-06-09T12:41:30Z" xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source><target logoport:matchpercent="0" state="translated">Pielāgotu lauku ieviešana Microsoft Dynamics 365 Project Timesheet mobilajai programmai operētājsistēmā iOS un Android</target>
        </trans-unit>
        <trans-unit logoport:updated-at="2019-06-09T12:42:23Z" xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šajā tēmā ir aprakstīti parastās metodes paplašinājumu izmantošanai, lai ieviestu pielāgotus laukus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Pielāgotu lauku ieviešana Microsoft Dynamics 365 Project Timesheet mobilajai programmai operētājsistēmā iOS un Android</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Šajā tēmā ir aprakstīti parastās metodes paplašinājumu izmantošanai, lai ieviestu pielāgotus laukus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The following topics are covered:</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">Ir aprakstītas tālāk norādītās tēmas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The various data types that the custom field framework supports</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dažādie datu tipi, ko atbalsta pielāgoto lauku struktūra</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kā darba laika uzskaites tabulu ierakstos rādīt tikai lasāmus vai rediģējamus laukus un kā datu bāzē saglabāt lietotāja norādītas vērtības.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>How to show read-only fields on the timesheet header</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kā darba laika uzskaites tabulas virsrakstā rādīt tikai lasāmus laukus</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>How to integrate other custom business logic to enter default values in fields and do additional validation</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kā integrēt citu pielāgoto biznesa loģiku, lai laukos ievadītu noklusējuma vērtības un veiktu papildu validēšanu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Audience</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Mērķauditorija</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šī tēma ir paredzēta izstrādātājiem, kas savus pielāgotos laukus integrē Microsoft Dynamics 365 Project Timesheet mobilajā programmā, kura ir pieejama operētājsistēmai Apple iOS un Google Android.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The assumption is that readers are familiar with X++ development and project timesheet functionality.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tiek pieņemts, ka lasītāji pārzina X++ izstrādes un projektu darba laika uzskaites tabulu funkcionalitāti.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Data contract – TSTimesheetCustomField X++ class</source><target logoport:matchpercent="0" state="translated">Datu līgums – TSTimesheetCustomField X++ klase</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> class is the X++ data contract class that represents information about a custom field for timesheet functionality.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> klase ir X++ datu līguma klase, kas pārstāv informāciju par pielāgotu lauku darba laika uzskaites tabulas funkcionalitātei.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pielāgoto lauku objektu saraksti tiek nodoti gan TSTimesheetDetails datu līgumam, gan TSTimesheetEntry datu līgumam, lai pielāgotus laukus rādītu mobilajā programmā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> - The timesheet header contract.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> — darba laika uzskaites tabulas virsraksta līgums.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> - The timesheet transaction contract.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> — darba laika uzskaites tabulas transakcijas līgums.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Groups of these objects that have the same project information and <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> value constitute a line.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šo objektu grupas, kam ir vienāda projekta informācija un vērtība <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept>, veido vienu rindu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>fieldBaseType (Types)</source><target logoport:matchpercent="0" state="translated">fieldBaseType (tipi)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> property on the <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> object determines the type of the field that appears in the app.</source><target logoport:matchpercent="0" state="translated">Rekvizīts <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> objektā <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> nosaka programmā rādītā lauka tipu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The following <bpt id="p1">**</bpt>Types<ept id="p1">**</ept> values that are supported.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tiek atbalstītas tālāk norādītās vērtības <bpt id="p1">**</bpt>Tipi<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Types value</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match">Vērtības Tipi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Type</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Tips</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Notes</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Piezīmes</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>0</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>String (and Enum)</source><target logoport:matchpercent="0" state="translated">Virkne (un Uzskaitījums)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The field appears as a text field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šis lauks izskatās kā teksta lauks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>1</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Integer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Vesels skaitlis</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The value is shown as a number without decimal places.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vērtība tiek rādīta kā skaitlis bez cipariem aiz komata.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>2</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Real</source>
        <target logoport:matchpercent="0" state="translated">Real</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The value is shown as a number that has decimal places.</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Vērtība tiek rādīta kā skaitlis ar cipariem aiz komata.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To show the real value as a currency in the app, use the <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept> property.</source><target logoport:matchpercent="0" state="translated">Lai reālo skaitļu vērtības programmā radītu kā valūtu, izmantojiet rekvizītu <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>You can use the <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> property to set the number of decimal places that are shown.</source><target logoport:matchpercent="0" state="translated">Varat arī izmantot rekvizītu <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept>, lai iestatītu, cik cipari aiz komata tiek rādīti.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>3</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Date</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Datums</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Date formats are determined by the user's <bpt id="p1">**</bpt>Date, times, and number format<ept id="p1">**</ept> setting that is specified under <bpt id="p2">**</bpt>Language and country/region preference<ept id="p2">**</ept> in <bpt id="p3">**</bpt>User options<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Datuma formātus nosaka lietotāja iestatījums <bpt id="p1">**</bpt>Datumu, laiku un skaitļu formāts<ept id="p1">**</ept>, kas ir norādīts iestatījumā <bpt id="p2">**</bpt>Valodas un valsts/reģiona preferences<ept id="p2">**</ept>, sadaļā <bpt id="p3">**</bpt>Lietotāja opcijas<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>4</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">4.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Boolean</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Būla</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>15</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>GUID</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">GUID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>16</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">16</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Int64</source><target logoport:matchpercent="0" state="translated">Int64</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property isn't provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, a free-text field is provided to the user.</source><target logoport:matchpercent="0" state="translated">Ja objektā <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> nav norādīts rekvizīts <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept>, lietotājam tiek nodrošināts brīva teksta lauks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> property can be used to set the maximum string length that users can enter.</source><target logoport:matchpercent="0" state="translated">Var izmantot rekvizītu <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept>, lai iestatītu maksimālo virknes garumu, kādu lietotāji var ievadīt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property is provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, those list elements are the only values that users can select by using option buttons (radio buttons).</source><target logoport:matchpercent="0" state="translated">Ja objektā <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> ir norādīts rekvizīts <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept>, šie saraksta elementi ir vienīgās vērtības, ko lietotāji var atlasīt, izmantojot opciju pogas (radiopogas).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In this case, the string field can act as an enum value for the purpose of user entry.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tādā gadījumā virknes lauks lietotāja ievades nolūkos var darboties kā uzskaitījuma vērtība.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="0" state="translated">Lai šo vērtību datu bāzē saglabātu kā uzskaitījumu, manuāli kartējiet virknes vērtību atpakaļ uz uzskaitījuma vērtību, pirms to saglabājat datu bāzē, izmantojot komandķēdi (piemēru skatiet tālāk šajā tēmā, sadaļā “Komandķēdes lietošana klasei TSTimesheetEntryService, lai darba laika uzskaites tabulas ierakstu no programmas saglabātu atpakaļ datu bāzē”).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>fieldExtendedType (TSCustomFieldExtendedType)</source><target logoport:matchpercent="0" state="translated">fieldExtendedType (TSCustomFieldExtendedType)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>You can use this property to format real values as currency.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šo rekvizītu varat izmantot, lai reālu skaitļu vērtības formatētu kā valūtu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This approach is applicable only when the <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> value is <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated">Šī pieeja ir piemērojama tikai tad, ja vienuma <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> vērtība ir <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – No formatting is applied.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> — netiek lietots nekāds formatējums.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> – Format the value as currency.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Valūta<ept id="p1">**</ept> — formatēt vērtību kā valūtu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>When currency formatting is active, the <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> field can be used pass the currency code that should be shown in the app.</source><target logoport:matchpercent="0" state="translated">Kad ir aktīvs valūtas formatējums, var izmantot lauku <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept>, lai nodotu valūtas kodu, kas ir jārāda programmā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The value is a read-only value.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šī vērtība ir tikai lasāma vērtība.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> field contains the money amount that should be saved to the database.</source><target logoport:matchpercent="0" state="translated">Laukā <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> ir naudas summa, kas ir jāsaglabā datu bāzē.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>fieldSection (TSCustomFieldSection)</source><target logoport:matchpercent="0" state="translated">fieldSection (TSCustomFieldSection)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You can use this property specify where the custom field should appear in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šo rekvizītu varat izmantot, lai norādītu, kur šis pielāgotais lauks ir jārāda programmā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> – The field will appear in the <bpt id="p2">**</bpt>View more details<ept id="p2">**</ept> section in the app.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldSection::Virsraksts<ept id="p1">**</ept> — šis lauks programmā tiek rādīts sadaļā <bpt id="p2">**</bpt>Skatīt vairāk informācijas<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>These fields are always read-only.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Šie lauki vienmēr ir tikai lasāmi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> – The field will appear after all the out-of-box line fields on timesheet entries.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldSection::Rinda<ept id="p1">**</ept> — šis lauks tiek rādīts pēc visiem darba laika uzskaites tabulu ierakstu standarta komplektācijas rindu laukiem.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>These fields can be either editable or read-only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šie lauki var būt rediģējami vai tikai lasāmi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>fieldName (FieldNameShort)</source><target logoport:matchpercent="0" state="translated">fieldName (FieldNameShort)</target>
        </trans-unit>
        <trans-unit logoport:updated-at="2019-06-09T13:25:56Z" xml:space="preserve" translate="yes" id="165">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šis rekvizīts norāda lauku, kad programmas nodrošinātās vērtības tiek saglabātas atpakaļ datu bāzē.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>tableName (TableNameShort)</source><target logoport:matchpercent="0" state="translated">tableName (TableNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Šis rekvizīts norāda lauku, kad programmas nodrošinātās vērtības tiek saglabātas atpakaļ datu bāzē.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>isEditable (NoYes)</source><target logoport:matchpercent="0" state="translated">isEditable (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be editable by users.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Iestatiet šo rekvizītu uz <bpt id="p1">**</bpt>Jā<ept id="p1">**</ept>, lai norādītu, ka darba laika uzskaites tabulas ieraksta sadaļā esošo lauku lietotājiem ir jāvar rediģēt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Set the property to <bpt id="p1">**</bpt>No<ept id="p1">**</ept> to make the field read-only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Iestatiet šo rekvizītu uz <bpt id="p1">**</bpt>Nē<ept id="p1">**</ept>, lai lauku padarītu par tikai lasāmu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>isMandatory (NoYes)</source><target logoport:matchpercent="0" state="translated">isMandatory (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be mandatory.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Iestatiet šo rekvizītu uz <bpt id="p1">**</bpt>Jā<ept id="p1">**</ept>, lai norādītu, ka darba laika uzskaites tabulas ieraksta sadaļā esošajam laukam ir jābūt obligātam.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>label (str)</source><target logoport:matchpercent="0" state="translated">label (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This property specifies the label that is shown next the field in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šis rekvizīts norāda etiķeti, kas programmā tiek rādīta blakus šim laukam.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>stringOptions (List of Strings)</source><target logoport:matchpercent="0" state="translated">stringOptions (virkņu saraksts)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This property is applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šis rekvizīts ir piemērojams tikai tad, ja vienums <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> ir iestatīts uz <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>If <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ja ir iestatīts vienums <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept>, ar virknēm šajā sarakstā tiek norādītas virkņu vērtības, kas ir pieejamas atlasei, izmantojot opciju pogas (radiopogas).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ja nav norādīta neviena virkne, ir atļauta brīvā teksta ievadīšana virknes laukā (piemēru skatiet tālāk šajā tēmā, sadaļā “Komandķēdes lietošana klasei TSTimesheetEntryService, lai darba laika uzskaites tabulas ierakstu no programmas saglabātu atpakaļ datu bāzē”).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>stringLength (int)</source><target logoport:matchpercent="0" state="translated">stringLength (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This property specifies the maximum length for a string field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šis rekvizīts norāda virknes lauka maksimālo garumu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Tas ir piemērojams tikai tad, ja vienums <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> ir iestatīts uz <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>numberOfDecimals (int)</source><target logoport:matchpercent="0" state="translated">numberOfDecimals (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This property specifies the number of decimal places that are shown for a real field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šis rekvizīts norāda ciparu skaitu aiz komata, kas tiek rādīti reāla skaitļa laukam.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Tas ir piemērojams tikai tad, ja vienums <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> ir iestatīts uz <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>orderSequence (int)</source><target logoport:matchpercent="0" state="translated">orderSequence (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šis rekvizīts kontrolē secību, kādā programmā tiek rādīti pielāgoti lauki, ja ir norādīti vairāki pielāgoti lauki.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Fields that have lower numbers are shown first.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vispirms tiek rādīti lauki, kuru skaitļi ir mazāki.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>booleanValue (boolean)</source><target logoport:matchpercent="0" state="translated">booleanValue (boolean)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>For fields of the <bpt id="p1">**</bpt>Boolean<ept id="p1">**</ept> type, this property passes the Boolean value of the field between the server and the app.</source><target logoport:matchpercent="0" state="translated">Laukiem, kuru tips ir <bpt id="p1">**</bpt>Būla<ept id="p1">**</ept>, šis rekvizīts nodod lauka Būla vērtību starp serveri un programmu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>guidValue (guid)</source><target logoport:matchpercent="0" state="translated">guidValue (guid)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For fields of the <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match">Laukiem, kuru tips ir <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept>, šis rekvizīts nodod lauka globāli unikālā identifikatora (GUID) vērtību starp serveri un programmu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>int64Value (int64)</source><target logoport:matchpercent="0" state="translated">int64Value (int64)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>For fields of the <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> type, this property passes the int64 value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Laukiem, kuru tips ir <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept>, šis rekvizīts nodod lauka int64 vērtību starp serveri un programmu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>intValue (int)</source><target logoport:matchpercent="0" state="translated">intValue (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For fields of the <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> type, this property passes the int value of the field between the server and the app.</source><target logoport:matchpercent="92" state="translated" state-qualifier="fuzzy-match">Laukiem, kuru tips ir <bpt id="p1">**</bpt>Int<ept id="p1">**</ept>, šis rekvizīts nodod lauka int vērtību starp serveri un programmu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>realValue (real)</source><target logoport:matchpercent="0" state="translated">realValue (real)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>For fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type, this property passes the real value of the field between the server and the app .</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Laukiem, kuru tips ir <bpt id="p1">**</bpt>Real<ept id="p1">**</ept>, šis rekvizīts nodod lauka reālā skaitļa vērtību starp serveri un programmu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>stringValue (str)</source><target logoport:matchpercent="0" state="translated">stringValue (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>For fields of the <bpt id="p1">**</bpt>String<ept id="p1">**</ept> type, this property passes the string value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Laukiem, kuru tips ir <bpt id="p1">**</bpt>String<ept id="p1">**</ept>, šis rekvizīts nodod lauka virknes vērtību starp serveri un programmu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>It's also used for fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type that are formatted as currency.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tas tiek izmantots arī laukiem ar tipu <bpt id="p1">**</bpt>Real<ept id="p1">**</ept>, kuri ir formatēti kā valūta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>For those fields, the property is used to pass the currency code to the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šiem laukiem šis rekvizīts tiek izmantots, lai valūtas kodu nodotu programmai.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>dateValue (date)</source><target logoport:matchpercent="0" state="translated">dateValue (date)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>For fields of the <bpt id="p1">**</bpt>Date<ept id="p1">**</ept> type, this property passes the date value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Laukiem, kuru tips ir <bpt id="p1">**</bpt>Datums<ept id="p1">**</ept>, šis rekvizīts nodod lauka datuma vērtību starp serveri un programmu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Show and save a custom field in the timesheet entry section</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pielāgotu lauku rādīšana un saglabāšana darba laika uzskaites tabulas ieraksta sadaļā</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Below is a screenshot from the mobile app of a timesheet entry creation.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tālāk ir ekrānuzņēmums no laika uzskaites tabulas ieraksta izveides mobilās lietotnes.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tajā ir redzami standarta komplektācijā esošie lauki un pielāgots lauks sadaļā “Laika ievade” ar nosaukumu “Testa virkne”, kuram jau ir iestatīta uzskaitījuma vērtība “Otrā opcija”.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Test string custom field in the app</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Testa virknes pielāgotais lauks programmā</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tālāk ir ekrānuzņēmums no mobilās lietotnes lietotājam, kas atlasa vienu no uzskaitījuma opcijām, kuras ir pieejamas pielāgotajam laukam “Testa virkne”.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The two options are "First option" and "Second option" shown as radio buttons.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Abas opcijas ir “Pirmā opcija” un “Otrā opcija” un tiek rādītas kā radiopogas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The second option is currently selected.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pašlaik ir atlasīta otrā opcija.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Option buttons (radio buttons) for the Test string custom field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Opciju pogas (radiopogas) testa virknes pielāgotajam laukam</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Extend the TSTimesheetLine table so that it has a custom field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tabulas TSTimesheetLine paplašināšana, lai tai būtu pielāgots lauks</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tipiskos scenārijos darba laika uzskaites tabulas ieraksta sadaļas pielāgotā lauka dati visticamāk tiks saglabāti tabulā TSTimesheetLine.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Taču var izmantot citas tabulas, ja datus var izgūt, pamatojoties uz nodrošināto TSTimesheetTrans ierakstu, vai ja tam nav konkrēta ieraksta konteksta (piemēram, ja projekta parametros šis lauks ir iestatīts kā tikai lasāms).</target>
        </trans-unit>
        <trans-unit logoport:updated-at="2019-06-09T13:59:31Z" xml:space="preserve" translate="yes" id="215">
          <source>Note that custom fields don't have to have any backing database records.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ņemiet vērā, ka pielāgotajiem laukiem pamatā nav datu bāzes ieraksti.</target>
        </trans-unit>
        <trans-unit logoport:updated-at="2019-06-09T13:59:43Z" xml:space="preserve" translate="yes" id="216">
          <source>They can be dynamically generated based on X++ logic.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tos var dinamiski ģenerēt, pamatojoties uz X++ loģiku.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šī pieeja var būt noderīga tikai lasāmos scenārijos (dinamiski ģenerētu pielāgotu lauku vērtību piemēru skatiet sadaļā “Komandķēdes lietošana klasē TSTimesheetDetails, metodē buildCustomFieldListForHeader, lai aizpildītu darba laika uzskaites tabulas informāciju”.)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Below is a screenshot from Visual Studio of the Application Object Tree.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tālāk ir ekrānuzņēmums no programmas objektu koka Visual Studio.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tajā ir redzams TSTimesheetLine tabulas paplašinājumu ar lauku TestLineString, kas ir pievienots kā pielāgots lauks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Line string</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Rindas virkne</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Komandķēdes lietošana klases TSTimesheetSettings metodei buildCustomFieldList, lai darba laika uzskaites tabulas ieraksta sadaļā rādītu kādu lauku</target>
        </trans-unit>
        <trans-unit logoport:updated-at="2019-06-09T14:06:51Z" xml:space="preserve" translate="yes" id="222">
          <source>This code controls the display settings for the field in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šis kods kontrolē programmas lauka rādīšanas iestatījumus.</target>
        </trans-unit>
        <trans-unit logoport:updated-at="2019-06-09T14:07:20Z" xml:space="preserve" translate="yes" id="223">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tas kontrolē, piemēram, lauka tipu, etiķeti, vai lauks ir obligāts un kurā sadaļā šis lauks tiek rādīts.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The following example shows a string field on time entries.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Nākamajā piemērā ir parādīts virknes lauks laika ierakstos.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>This field has two options, <bpt id="p1">**</bpt>First option<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Second option<ept id="p2">**</ept>, that are available via option buttons (radio buttons).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šim laukam ir divas opcijas, <bpt id="p1">**</bpt>Pirmā opcija<ept id="p1">**</ept> un <bpt id="p2">**</bpt>Otrā opcija<ept id="p2">**</ept>, un tās ir pieejamas, izmantojot opciju pogas (radiopogas).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The field in the app is associated with the <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept> field that is added to the TSTimesheetLine table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šis lauks programmā ir saistīts ar lauku <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept>, kas ir pievienots tabulai TSTimesheetLine.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Note the use of the <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept> method to simplify the initialization of the custom field properties: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept>, and <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</source><target logoport:matchpercent="0" state="translated">Ņemiet vērā metodes <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept> lietošanu, lai vienkāršotu inicializēšanu pielāgotajiem lauku rekvizītiem: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept> un <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>You can also set these parameters manually, as you prefer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šos parametrus varat iestatīt arī manuāli, ja vēlaties.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Komandķēdes lietošana klases TSTimesheetEntry metodei buildCustomFieldListForEntry, lai darba laika uzskaites tabulas ierakstā ievadītu vērtības</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> method is used to enter values on the saved timesheet lines in the mobile app.</source><target logoport:matchpercent="0" state="translated">Metode <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> tiek lietota, lai ievadītu vērtības mobilajā programmā saglabātajās darba laika uzskaites tabulas rindās.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>It takes a TSTimesheetTrans record as a parameter.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šī metode kā parametru izmanto ierakstu TSTimesheetTrans.</target>
        </trans-unit>
        <trans-unit logoport:updated-at="2019-06-09T14:14:57Z" xml:space="preserve" translate="yes" id="232">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Laukus no šī ieraksta var izmantot, lai programmā aizpildītu pielāgotā lauka vērtību.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Komandķēdes lietošana klasei TSTimesheetEntryService, lai darba laika uzskaites tabulas ierakstu no programmas saglabātu atpakaļ datu bāzē</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>To save a custom field back to the database in typical usage, you must extend multiple methods:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lai pielāgotu lauku saglabātu atpakaļ datu bāzē tipiskā lietojumā, jums ir jāpaplašina vairākas metodes.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>The <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Metode <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> tiek lietota, lai noteiktu, vai lietotājs ir mainījis rindas ierakstu programmā un vai tas ir jāsaglabā datu bāzē.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>If performance isn't a concern, this method can be simplified so that it always returns <bpt id="p1">**</bpt>true<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ja nav jāraizējas par veiktspēju, šo metodi var vienkāršot, lai tā vienmēr atgrieztu vērtību <bpt id="p1">**</bpt>true<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> and <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</source><target logoport:matchpercent="0" state="translated">Metodi <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> un <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> var paplašināt tā, lai tās ievadītu vērtības TSTimesheetLine datu bāzes ierakstā no nodrošinātā TSTimesheetEntry datu līguma ieraksta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Nākamajā piemērā pievērsiet uzmanību tam, kā kartēšana starp datu bāzes lauku un ieraksta lauku tiek manuāli veikta, izmantojot X++ kodu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> method can also be extended if the custom field that is mapped to the <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> object must write back to the TSTimesheetLineweek database table.</source><target logoport:matchpercent="0" state="translated">Metodi <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> var arī paplašināt, ja pielāgotajam laukam, kas ir kartēts uz <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> objektu, būtu jāraksta atpakaļ uz TSTimesheetLineweek datu bāzes tabulu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The following example saves the <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> or <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> value that the user selects to the database as a raw string value.</source><target logoport:matchpercent="0" state="translated">Nākamajā piemērā lietotāja atlasītā vērtība <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> vai <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> tiek saglabāta datu bāzē kā neapstrādātas virknes vērtība.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>If the database field is a field of the <bpt id="p1">**</bpt>Enum<ept id="p1">**</ept> type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ja datu bāzes lauks ir lauks ar tipu <bpt id="p1">**</bpt>Uzskaitījums<ept id="p1">**</ept>, šīs vērtības var manuāli kartēt uz uzskaitījuma vērtību un pēc tam saglabāt datu bāzes tabulas uzskaitījuma laukā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Show a custom field in the timesheet header section</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Pielāgotu lauku rādīšana darba laika uzskaites tabulas virsraksta sadaļā</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Below is a screenshot from the mobile app of a user viewing a timesheet.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Tālāk ir ekrānuzņēmums no mobilās lietotnes lietotājam, kurš apskata darba laika uzskaites tabulu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The "More information" button has been selected in the upper-right corner to show the "View more details" option.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Augšējā labajā stūrī ir atlasīta poga “Papildinformācija”, lai rādītu opciju “Skatīt vairāk informācijas”.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>View more details command</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Komanda Skatīt vairāk informācijas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Below is a screenshot from the mobile app showing the “More” section of a timesheet.</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Tālāk ir ekrānuzņēmums no mobilās lietotnes, kur ir redzama darba laika uzskaites tabulas sadaļa “Vairāk”.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Darba laika uzskaites tabulas virsraksta sadaļai ir pievienots pielāgots lauks ar nosaukumu “Šīs darba laika uzskaites tabulas lietojuma koeficients (aprēķināts pielāgots lauks)”.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>A read-only value of "0.667" is set on the custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pielāgotajā laukā ir iestatīta tikai lasāma vērtība “0,667”.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>More section</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Sadaļa Vairāk</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Extend the TSTimesheetTable table so that it has a custom field</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">Tabulas TSTimesheetTable paplašināšana, lai tai būtu pielāgots lauks</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Tipiskos scenārijos virsraksta sadaļas pielāgotā lauka dati visticamāk tiks izgūti no tabulas TSTimesheetHeader.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match">Taču var izmantot citas tabulas, ja datus var izgūt, pamatojoties uz nodrošināto TSTimesheetTable ierakstu, vai ja tam nav konkrēta ieraksta konteksta (piemēram, ja projekta parametros šis lauks ir iestatīts kā tikai lasāms).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Note that custom fields don't have to have any backing database records.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Ņemiet vērā, ka pielāgotajiem laukiem pamatā nav datu bāzes ieraksti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>They can be dynamically generated based on X++ logic.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Tos var dinamiski ģenerēt, pamatojoties uz X++ loģiku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>The example that follows shows this approach.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šī pieeja ir parādīta nākamajā piemērā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Fields in the header section are always read-only in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Programmā lauki virsraksta sadaļā vienmēr ir tikai lasāmi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Komandķēdes lietošana klases TSTimesheetSettings metodei buildCustomFieldList, lai virsraksta sadaļā rādītu kādu lauku</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>This code controls the display settings for the field in the app.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Šis kods kontrolē programmas lauka rādīšanas iestatījumus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Tas kontrolē, piemēram, lauka tipu, etiķeti, vai lauks ir obligāts un kurā sadaļā šis lauks tiek rādīts.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The following example shows a computed value in the header section in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Nākamajā piemērā ir parādīta aprēķināta vērtība programmas virsraksta sadaļā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Komandķēdes lietošana klases TSTimesheetDetails metodei buildCustomFieldListForHeader, lai aizpildītu darba laika uzskaites tabulas informāciju</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> method is used to fill in the timesheet header details in the mobile app.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match">Metode <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> tiek lietota, lai mobilajā programmā aizpildītu darba laika uzskaites tabulas virsraksta informāciju.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>It takes a TSTimesheetTable record as a parameter.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Šī metode kā parametru izmanto ierakstu TSTimesheetTable.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Laukus no šī ieraksta var izmantot, lai programmā aizpildītu pielāgotā lauka vērtību.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The following example doesn't read any values from the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Nākamajā piemērā no datu bāzes netiek nolasītas nekādas vērtības.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Instead, it uses X++ logic to generate a computed value that is then shown in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tā vietā tiek izmantota X++ loģika, lai ģenerētu aprēķinātu vērtību, kura pēc tam tiek rādīta programmā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Other configurability/extensibility opportunities</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Citas konfigurēšanas/paplašināšanas iespējas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Adding additional validation for the app</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Papildu validēšanas pievienošana programmai</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Existing logic for timesheet functionality at the database level will still work as expected.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pastāvošā darba laika uzskaites tabulas funkcionalitātes loģika datu bāzes līmenī joprojām darbosies paredzētajā veidā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>To interrupt the completion of save or submit operations and show a specific error message, you can add <bpt id="p1">**</bpt>throw error("message to user")<ept id="p1">**</ept> to the code via a chain of command extension.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lai pārtrauktu saglabāšanas vai iesniegšanas operāciju pabeigšanu un parādītu konkrētu kļūdas ziņojumu, varat kodam pievienot <bpt id="p1">**</bpt>throw error("ziņojums lietotājam")<ept id="p1">**</ept>, izmantojot komandķēdes paplašinājumu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Here are three examples of useful extensible methods:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tālāk ir trīs noderīgu paplašināmu metožu piemēri.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>If <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> on the TSTimesheetLine table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during a save operation for a timesheet line, an error message is shown in the mobile app.</source><target logoport:matchpercent="0" state="translated">Ja <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> tabulā TSTimesheetLine atgriež <bpt id="p2">**</bpt>false<ept id="p2">**</ept> kādas darba laika uzskaites tabulas rindas saglabāšanas operācijas laikā, mobilajā programmā tiek parādīta kļūda.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>If <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> on the TSTimesheetTable table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during timesheet submission in the app, an error message is shown to the user.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Ja <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> tabulā TSTimesheetTable atgriež <bpt id="p2">**</bpt>false<ept id="p2">**</ept> laikā, kad darba laika uzskaites tabula tiek iesniegta programmā, lietotājam tiek parādīta kļūda.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Logic that fills in fields (for example, <bpt id="p1">**</bpt>Line Property<ept id="p1">**</ept>) during the <bpt id="p2">**</bpt>insert<ept id="p2">**</ept> method on the TSTimesheetLine table will still run.</source><target logoport:matchpercent="0" state="translated">Joprojām darbosies loģika, kas aizpilda laukus (piemēram, <bpt id="p1">**</bpt>Rindas rekvizīts<ept id="p1">**</ept>) tabulai TSTimesheetLine metodes <bpt id="p2">**</bpt>ievietot<ept id="p2">**</ept> laikā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Hiding and marking out-of-box fields as read-only via configuration</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Standarta komplektācijā ietverto lauku slēpšana un atzīmēšana kā tikai lasāmus, izmantojot konfigurāciju</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">No projekta parametriem standarta komplektācijā ietvertos laukus mobilajā programmā varat padarīt par tikai lasāmiem vai paslēptiem.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Set the options in the <bpt id="p1">**</bpt>Mobile timesheets<ept id="p1">**</ept> section on the <bpt id="p2">**</bpt>Timesheet<ept id="p2">**</ept> tab of the <bpt id="p3">**</bpt>Project management and accounting parameters<ept id="p3">**</ept> page.</source><target logoport:matchpercent="0" state="translated">Iestatiet opcijas lapas <bpt id="p3">**</bpt>Projektu vadības un uzskaites parametri<ept id="p3">**</ept> cilnes <bpt id="p2">**</bpt>Darba laika uzskaites tabula<ept id="p2">**</ept> sadaļā <bpt id="p1">**</bpt>Mobilās darba laika uzskaites tabulas<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Project parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Projektu parametri</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Changing the activities that are available for selection via extensions</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tādu aktivitāšu maiņa, kuras ir pieejamas atlasīšanai, izmantojot paplašinājumus</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The activities that are available for selection for a project are filled in via the <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="0" state="translated">Aktivitātes, kas projektam ir pieejamas atlasīšanai, tiek aizpildītas, izmantojot metodi <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> un <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> klasē <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Varat izmantot komandķēdi, lai mainītu šo uzvedību un padarītu to atbilstošu jūsu biznesa scenārijam attiecība uz aktivitātēm, kas ir pieejamas atlasīšanai kādam noteiktam projektam.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Entering a default project category on timesheet entries</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Noklusējuma projekta kategorijas ievadīšana darba laika uzskaites tabulu ierakstos</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Entry of a default project category on timesheet entries occurs at three levels.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Noklusējuma projekta kategorijas ievadīšana darba laika uzskaites tabulu ierakstos notiek trīs līmeņos.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lai sasniegtu vēlamo uzvedību, varat izmantot komandķēdi, lai paplašinātu šo uzvedību jebkurā līmenī vai visos šajos līmeņos.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>The following hierarchy is used:</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Tiek izmantota tālāk aprakstītā hierarhija.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The app tries to put the default category from the project resource.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Programma mēģina ievietot noklusējuma kategoriju no projekta resursa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>This default category is set in the <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="0" state="translated">Šī noklusējuma kategorija ir iestatīta metodē <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> un <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept>, klasē <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ja noklusējuma kategorija nav norādīta projekta resursa līmenī, programma mēģina to izgūt no projekta aktivitātes.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>This default category is set in the <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="0" state="translated">Šī noklusējuma kategorija ir iestatīta metodē <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept>, klasē <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Ja noklusējuma kategorija nav norādīta projekta aktivitātes līmenī, noklusējuma kategorija tiek ņemta no projekta parametriem.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>This default category is set in the <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Šī noklusējuma kategorija ir iestatīta metodē <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept>, klasē <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept>.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>