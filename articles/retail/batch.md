<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="batch.md" target-language="lv-LV">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>batch.e70006.4456fc3d5bc4547fa8211642b11ca6df455fa187.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4456fc3d5bc4547fa8211642b11ca6df455fa187</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\batch.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Improved handling of batch-tracked items</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Uzlabota pēc partijas izsekoto krājumu apstrāde</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the improvements that have been made to the handling of batches for batch-tracked items during the Retail statement posting process.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šajā tēmā ir aprakstīti uzlabojumi, kas ieviesti pēc partijas izsekoto krājumu apstrādē, kura tiek veikta mazumtirdzniecības pārskata grāmatošanas procesa laikā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Improved handling of batch-tracked items</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Uzlabota pēc partijas izsekoto krājumu apstrāde</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Microsoft Dynamics 365 for Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pārdošanas laikā Microsoft Dynamics 365 for Retail pārdošanas punktā (POS) nevar tvert partijas numurus pēc partijas izsekotajiem krājumiem.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tomēr attiecībā uz noteiktām konfigurācijām, ja galvenajā birojā pārdošana tiek grāmatota, izmantojot debitoru pasūtījumus vai grāmatojot pārskatu, sistēma Microsoft Dynamics sagaida, ka pastāv derīgi pēc partijas izsekoto krājumu partijas numuri un ka tie tiks izmantoti rēķinu izrakstīšanas procesā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ja precēm ir pieejami derīgi partijas numuri, tiek izmantots pārskatu grāmatošanas laikā veiktais debitora pasūtījumu rēķinu un pārdošanas pasūtījumu rēķinu izrakstīšanas process.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Citādi debitora pasūtījumu rēķinu izrakstīšanas procesu nevar grāmatot, un POS lietotājs saņem kļūdas ziņojumu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Statement posting then goes into an error state.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pēc tam pārskatu grāmatošanas procesam tiek aktivizēts kļūdas stāvoklis.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This error state occurs even when negative inventory has been turned on for the products.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šis kļūdas stāvoklis rodas pat tad, ja precēm ir iespējoti negatīvi krājumi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Improvements that have been made in Microsoft Dynamics for Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ieviešot uzlabojumus Microsoft Dynamics for Retail 10.0.4 un jaunākās versijās, tika nodrošināts: ja pēc partijas izsekotiem krājumiem ir iespējoti negatīvie krājumi un krājuma daudzums ir 0 (nulle) vai nav pieejams partijas numurs, šiem krājumiem netiek bloķēta debitora pasūtījuma rēķinu un pārdošanas pasūtījuma rēķinu izrakstīšana pārskata grāmatošanas procesa laikā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ja partijas numuri nav pieejami, jaunā funkcionalitāte pārdošanas rindām izmanto noklusējuma partijas ID.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To define the default batch ID that is used for customer orders, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Order<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lai definētu debitora pasūtījumiem izmantojamo noklusējuma partijas ID, kopsavilkuma cilnes <bpt id="p3">**</bpt>Pasūtījums<ept id="p3">**</ept> lapas <bpt id="p1">**</bpt>Mazumtirdzniecības parametri<ept id="p1">**</ept> cilnē <bpt id="p2">**</bpt>Debitoru pasūtījumi<ept id="p2">**</ept> iestatiet vērtību laukā <bpt id="p4">**</bpt>Noklusējuma partijas ID<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To define the default batch ID that is used for sales order invoicing through statement posting, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Posting<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Inventory update<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Lai definētu pārskatu grāmatošanas laikā pārdošanas pasūtījumu rēķinos izmantojamo noklusējuma partijas ID, kopsavilkuma cilnes <bpt id="p3">**</bpt>Krājumu atjaunināšana<ept id="p3">**</ept> lapas <bpt id="p1">**</bpt>Mazumtirdzniecības parametri<ept id="p1">**</ept> cilnē <bpt id="p2">**</bpt>Grāmatošana<ept id="p2">**</ept> iestatiet vērtību laukā <bpt id="p4">**</bpt>Noklusējuma partijas ID<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šī funkcionalitāte ir pieejama tikai tad, ja attiecīgajai veikala noliktavai un krājumiem ir iespējoti papildu noliktavas procesi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Turpmākajos laidienos šī funkcionalitāte tiks atbalstīta arī tad, ja netiks izmantots papildu noliktavas pārvaldības process.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>