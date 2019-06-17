<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="set-up-manage-images-retail-mpos.md" target-language="lv-LV">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>set-up-manage-images-retail-mpos.3cc4ad.c256569135a00ea98a5c059b9dd12a07a000ee6a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>c256569135a00ea98a5c059b9dd12a07a000ee6a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\set-up-manage-images-retail-mpos.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Set up and manage images for Retail Modern POS (MPOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Programmai Retail Modern POS (MPOS) paredzēto attēlu iestatīšana un pārvaldība</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article explains the steps that are involved in setting up and managing images for the various entities that appear in Retail Modern POS (MPOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā rakstā ir paskaidrotas dažādo programmā Retail Modern POS (MPOS) redzamo elementu attēlu iestatīšanas un pārvaldības darbības.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Set up and manage images for Retail Modern POS (MPOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Programmai Retail Modern POS (MPOS) paredzēto attēlu iestatīšana un pārvaldība</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article explains the steps that are involved in setting up and managing images for the various entities that appear in Retail Modern POS (MPOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā rakstā ir paskaidrotas dažādo programmā Retail Modern POS (MPOS) redzamo elementu attēlu iestatīšanas un pārvaldības darbības.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Setting up the media base URL and defining media templates to configure the format for image URLs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Multivides bāzes vietrāža URL iestatīšana un multivides veidņu definēšana, lai konfigurētu attēlu vietrāžu URL formātu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The images that appear in Retail Modern POS (MPOS) must be hosted externally, outside Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Programmā Retail Modern POS (MPOS) redzamie attēli ir jāvieso ārēji, ārpus programmas Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Typically, they are hosted in a content management system, content delivery network (CDN), or media server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Parasti tie ir izvietoti satura vadības sistēmā, satura piegādes tīklā (CDN) vai multivides serverī.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>MPOS then fetches and displays the images for the appropriate entities, such as products and catalogs, by accessing the target URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pēc tam MPOS ienes un parāda atbilstošo elementu, piemēram, preču un katalogu, attēlus, piekļūstot mērķa vietrādim URL.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>To fetch these externally hosted images, MPOS requires the correct URL format for the images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai ienestu šos ārējos attēlus, MPOS nepieciešams pareizs attēlu vietrāža URL formāts.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can configure the required URL format for the images by setting up the <bpt id="p1">**</bpt>Media base URL<ept id="p1">**</ept> value in the channel profile and using the <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept> functionality for each entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nepieciešamo attēlu vietrāžu URL formātu var konfigurēt, iestatot vērtību <bpt id="p1">**</bpt>Multivides bāzes vietrādis URL<ept id="p1">**</ept> kanāla profilā un izmantojot funkciju <bpt id="p2">**</bpt>Definēt multivides veidni<ept id="p2">**</ept> katram elementam.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can also overwrite the standard URL format for a subset of entities by using the <bpt id="p1">**</bpt>Edit in Excel<ept id="p1">**</ept> functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varat arī pārrakstīt elementu apakškopas standarta vietrāža URL formātu, izmantojot funkciju <bpt id="p1">**</bpt>Rediģēt programmā Excel<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In the current version of Dynamics 365 for Retail, you can no longer set up the URL format by using the <bpt id="p1">**</bpt>Image<ept id="p1">**</ept> attribute XML for MPOS in the <bpt id="p2">**</bpt>Default<ept id="p2">**</ept> attribute group for entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pašreizējā Dynamics 365 for Retail versijā vairs nevar iestatīt vietrāža URL formātu, izmantojot atribūta <bpt id="p1">**</bpt>Attēls<ept id="p1">**</ept> vērtību XML MPOS elementu atribūtu grupā <bpt id="p2">**</bpt>Noklusējuma<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If you're familiar with Microsoft Dynamics AX 2012 R3 and are now using the current version of Dynamics 365 for Retail, make sure that you always use the new <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> functionality to set up images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja pārzināt programmu Microsoft Dynamics AX 2012 R3 un tagad lietojat pašreizējoDynamics 365 for Retail versiju, attēlu iestatīšanai vienmēr izmantojat jauno funkcionalitāti <bpt id="p1">**</bpt>Definēt multivides veidni<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Don't use or modify the <bpt id="p1">**</bpt>Image<ept id="p1">**</ept> attribute in the <bpt id="p2">**</bpt>Default<ept id="p2">**</ept> attribute group for any entities, including products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Neizmantojiet un nemainiet atribūtu <bpt id="p1">**</bpt>Attēls<ept id="p1">**</ept> elementiem, tostarp precēm, atribūtu grupā <bpt id="p2">**</bpt>Noklusējuma<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Changes that you make directly in the <bpt id="p1">**</bpt>Default<ept id="p1">**</ept> attribute group for images won't be reflected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Izmaiņas, ko veicat attēlos tieši atribūtu grupā <bpt id="p1">**</bpt>Noklusējuma<ept id="p1">**</ept>, netiks atspoguļotas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>This option will be disabled in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šī opcija būs atspējota nākamajos laidienos.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In the following procedures, images are set up for the Catalog entity as an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nākamajās procedūrās, kā piemērs, attēli tiek iestatīti elementam Katalogs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>These procedures will help guarantee that the correct image destination path is set implicitly for all catalog images that use a common path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šīs procedūras palīdzēs nodrošināt, ka visiem kataloga attēliem, kas izmanto kopīgo ceļu, netieši iestatīts pareizais attēlu mērķa ceļš.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>For example, if you've set up a media server or CDN externally, and want the images to appear in MPOS for a given store, the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> functionality helps you the set the path where MPOS can look up and retrieve the images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Piemēram, ja ir ārēji iestatīts multivides serveris vai CDN, un vēlaties, lai attēli parādītos MPOS konkrētajam veikalam, funkcija <bpt id="p1">**</bpt>Definēt multivides veidni<ept id="p1">**</ept> palīdz iestatīt ceļu, kur MPOS var uzmeklēt un iegūt attēlus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For this demo data example, the media server is deployed on the Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā demonstrācijas datu piemērā multivides serveris ir izvietots mazumtirdzniecības serverī.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>However, you can have it anywhere outside Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Taču tas var atrasties jebkurā vietā ārpus programmas Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Set up the media base URL for a channel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Multivides bāzes vietrāža URL iestatīšana kanālam</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Open the Dynamics 365 for Retail HQ portal.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Atveriet Dynamics 365 for Retail HQ portālu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Channel profiles<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Mazumtirdzniecība<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Kanāla iestatīšana<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Kanāla profili<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Navigation<ept id="p1">](./media/channel-profile1.png)](./media/channel-profile1.png)</ept></source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Navigācija<ept id="p1">](./media/channel-profile1.png)](./media/channel-profile1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In the channel profile that your store uses for MPOS, update the <bpt id="p1">**</bpt>Media base URL<ept id="p1">**</ept> field with the base URL of your media server or CDN.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kanāla profilā, ko jūsu veikals izmanto MPOS, atjauniniet lauku <bpt id="p1">**</bpt>Multivides bāzes vietrādis URL<ept id="p1">**</ept>, norādot sava multivides servera vai CDN pamata vietrādi URL.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The base URL is the first part of the URL that is shared by all image folders of different entities.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Bāzes vietrādis URL ir pirmā URL vietrāža daļa, kas ir kopīga visām dažādu elementu attēlu mapēm.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Channel profiles page<ept id="p1">](./media/channel-profile2.png)](./media/channel-profile2.png)</ept></source><target logoport:matchpercent="0" state="translated"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Lapa Kanāla profili<ept id="p1">](./media/channel-profile2.png)](./media/channel-profile2.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Define the media template for an entity</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Elementa multivides veidnes definēšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Catalog management<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Catalog images<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Mazumtirdzniecība<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Kataloga pārvaldība<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Kataloga attēli<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>On the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> page, on the Action Pane, click <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lapā <bpt id="p1">**</bpt>Kataloga attēli<ept id="p1">**</ept> darbību rūtī noklikšķiniet uz <bpt id="p2">**</bpt>Definēt multivides veidni<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Entity<ept id="p2">**</ept> field, <bpt id="p3">**</bpt>Catalog<ept id="p3">**</ept> should be selected by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dialoglodziņā <bpt id="p1">**</bpt>Definēt multivides veidni<ept id="p1">**</ept> laukā <bpt id="p2">**</bpt>Elements<ept id="p2">**</ept> jābūt pēc noklusējuma atlasītai vērtībai <bpt id="p3">**</bpt>Katalogs<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>On the <bpt id="p1">**</bpt>Media path<ept id="p1">**</ept> FastTab, enter the remaining path of the image location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kopsavilkuma cilnē <bpt id="p1">**</bpt>Multivides ceļš<ept id="p1">**</ept> ievadiet atlikušo attēla atrašanās vietas ceļu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The media path supports <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> as a variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Multivides ceļš atbalsta <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> kā mainīgo.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>For example, for the demo data, you can create a <bpt id="p1">**</bpt>Catalogs<ept id="p1">**</ept> folder for all catalog images under the media base URL for your media server (<ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer`</ph>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Piemēram, demonstrācijas datiem varat izveidot mapi <bpt id="p1">**</bpt>Katalogi<ept id="p1">**</ept> visiem kataloga attēliem, kas atrodas jūsu multivides servera multivides bāzes vietrādī URL (<ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer`</ph>).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>You can then have a folder for each language, such as en-US or fr-FR, and copy the appropriate images under each folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tad jums var būt mape katrai valodai, piemēram, en-US vai fr-FR, un varat kopēt atbilstošos attēlus zem katras mapes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If you don't have different images for the various languages, you can omit the <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> variable from your folder structure and point directly to the Catalogs folder that contains the catalog images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja jums nav dažādu attēlu dažādām valodām, var izlaist mainīto <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> mapes struktūrā un norādīt tieši uz mapi Katalogi, kurā atrodas kataloga attēli.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The current version of Dynamics 365 for Retail supports the <bpt id="p1">**</bpt>{LanguageId}<ept id="p1">**</ept> token for Catalog, Product, and Category entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pašreizējā Dynamics 365 for Retail versija atbalsta marķiera <bpt id="p1">**</bpt>{LanguageId}<ept id="p1">**</ept> izmantošanu elementiem Katalogs, Prece un Kategorija.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>(The <bpt id="p1">**</bpt>{LanguageID}<ept id="p1">**</ept> token isn't supported for Customer and Worker entities, according to the existing standard that has been effective since Microsoft Dynamics AX 6.x.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Saskaņā ar esošo standartu, kas ir spēkā, sākot ar versiju Microsoft Dynamics AX 6.x., netiek atbalstīta marķiera <bpt id="p1">**</bpt>{LanguageID}<ept id="p1">**</ept> izmantošana elementiem Debitors un Nodarbinātais.)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>For images, the file name format is hard-coded to the catalog name and can't be changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Attēlu faila nosaukuma formāts ir stingri kodēts uz kataloga nosaukumu un to nevar mainīt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Therefore, rename your images so that they have appropriate catalog names, to help guarantee that MPOS handles them correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tāpēc pārdēvējiet attēlus tā, lai tiem būtu atbilstoši kataloga nosaukumi, lai palīdzētu nodrošināt, ka MPOS tos apstrādā pareizi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In the <bpt id="p1">**</bpt>File Extension<ept id="p1">**</ept> field, select the expected file name extension, depending on the type of images that you have.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Laukā <bpt id="p1">**</bpt>Faila paplašinājums<ept id="p1">**</ept> atlasiet paredzēto faila nosaukuma paplašinājumu, atkarībā no jūsu attēlu tipa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>For example, for the demo data, the catalog images are set to the .jpg extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Piemēram, demonstrācijas datos kataloga attēli ir iestatīti uz paplašinājumu .jpg.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>(The image files are also renamed so that they have catalog names.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Attēlu faili tiek pārdēvēti arī tā, lai tiem būtu kataloga nosaukumi.)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Labi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To validate that the media template for images has been saved correctly, on the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept> again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai apstiprinātu, ka multivides veidnes attēliem ir pareizi saglabātas lapā <bpt id="p1">**</bpt>Kataloga attēli<ept id="p1">**</ept> vēlreiz noklikšķiniet uz <bpt id="p2">**</bpt>Definēt multivides veidni<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To validate the template without closing the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box, you can use the <bpt id="p2">**</bpt>Generate Image URLs for Excel<ept id="p2">**</ept> FastTab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai apstiprinātu veidni, neaizverot dialoglodziņu <bpt id="p1">**</bpt>Definēt multivides veidni<ept id="p1">**</ept> var izmantot kopsavilkuma cilni <bpt id="p2">**</bpt>Ģenerēt attēlu vietrāžus URL programmai Excel<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Check the appearance of the image URL, and verify that the URL complies with the template standard that was mentioned earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārbaudiet attēla vietrāža URL izskatu un, vai vietrādis URL atbilst veidnes standartam, kas minēts iepriekš.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box has now set the image path implicitly for all catalog images that use this common URL path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dialoglodziņā <bpt id="p1">**</bpt>Definēt multivides veidni<ept id="p1">**</ept> tagad netieši iestatīts attēla ceļš visiem kataloga attēliem, kuros tiek izmantots šis kopējais vietrāža URL ceļš.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>This URL path applies to all catalog images unless they are overwritten.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šis vietrāža URL ceļš attiecas uz visiem kataloga attēliem, ja vien tie netiek pārrakstīti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The first part of the image path is taken from the media base URL that you defined in the channel profile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pirmā attēla ceļa daļa tiek ņemta no multivides bāzes vietrāža URL, ko definējāt kanāla profilā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The remaining part of the path is taken from the path that you defined in the media template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Atlikusī ceļa daļa tiek ņemta no ceļa, ko definējāt multivides veidnē.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The two parts are concatenated to provide the full URL of the image location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Divas daļas tiek apvienotas, lai sniegtu pilnu attēla atrašanās vietas vietrādi URL.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>For example, a catalog in the demo data is named Fabrikam Base Catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Piemēram, kataloga nosaukums demonstrācijas datos ir Fabrikam Base Catalog.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Therefore, the image name must be Fabrikam Base Catalog.jpg so that it uses the catalog name and the .jpg file name extension that is configured in the template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tāpēc attēla nosaukumam ir jābūt Fabrikam Base Catalog.jpg, lai tiktu izmantots kataloga nosaukums un. jpg faila nosaukuma paplašinājums, kas ir konfigurēts veidnē.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>In this case, after concatenation, the URL will be <ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šādā gadījumā pēc savienošanas vietrādis URL būs <ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg`</ph>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Run the synchronization jobs to push the new template to the channel database, so that MPOS can use the template to access the images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Izpildiet sinhronizēšanas darbus, lai virzītu jaunu veidni uz kanāla datu bāzi, lai MPOS varētu izmantot veidni, lai piekļūtu attēliem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>To update the media template for catalog images on the channel side, be sure to run <bpt id="p1">**</bpt>Catalog Job 1150<ept id="p1">**</ept> from <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Lai atjauninātu multivides veidni kataloga attēliem kanāla pusē, noteikti izpildiet darbību <bpt id="p1">**</bpt>Kataloga darbs 1150<ept id="p1">**</ept> sadaļā <bpt id="p2">**</bpt>Mazumtirdzniecības IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Sadales grafiks<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Define media template dialog box<ept id="p1">](./media/catalog1.png)](./media/catalog1.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Dialoglodziņš Definēt multivides veidni<ept id="p1">](./media/catalog1.png)](./media/catalog1.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Previewing an image from the entity level</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Attēlu priekšskatīšana no elementa līmeņa</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>From the page for the entity item in HQ, you can preview the image that uses the image URL that is derived from the media template.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">No HQ elementa krājuma lapas var priekšskatīt attēlu, kurā izmantots attēla vietrādis URL, kas tiek atvasināts no multivides veidnes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>For this example, go to the appropriate catalog, and then, on the Action Pane, click <bpt id="p1">**</bpt>Media<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Images<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā piemērā dodieties uz atbilstošo katalogu un pēc tam darbību rūtī noklikšķiniet uz <bpt id="p1">**</bpt>Multivide<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Attēli<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Use the drop-down list to select different stores that might have different channel profiles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Izmantojiet nolaižamo sarakstu, lai atlasītu dažādus veikalus, kuriem varētu būt dažādi kanāla profili.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>To edit or remove the implicit media template, you must return to the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box for the <bpt id="p2">**</bpt>Catalog images<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai rediģētu vai noņemtu netiešu multivides veidni, jums ir jāatgriežas dialoglodziņā <bpt id="p1">**</bpt>Definēt multivides veidni<ept id="p1">**</ept>, kas attiecas uz lapu <bpt id="p2">**</bpt>Kataloga attēli<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>You can use the <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Remove<ept id="p2">**</ept> buttons to manually change the path that is based on the implicit template and used for a specific image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Var izmantot pogas <bpt id="p1">**</bpt>Pievienot<ept id="p1">**</ept> un <bpt id="p2">**</bpt>Noņemt<ept id="p2">**</ept>, lai manuāli mainītu ceļu, kas ir balstīts uz netiešo veidni un lietots noteiktam attēlam.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>For more information, see the <bpt id="p1">[</bpt>Overwriting the media template for entity items<ept id="p1">](#overwriting-the-media-template-for-entity-items)</ept> section later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Papildinformāciju skatiet sadaļā <bpt id="p1">[</bpt>Elementu krājumu multivides veidnes pārrakstīšana<ept id="p1">](#overwriting-the-media-template-for-entity-items)</ept> tālāk šajā rakstā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>After you've finished previewing an image and making any changes that you require, start the MPOS instance for the appropriate store, and see whether the catalog images are shown.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kad esat pabeidzis attēla priekšskatīšanu un veicis jebkādas nepieciešamās izmaiņas, palaidiet atbilstošā veikala MPOS instanci un skatiet, vai tiek parādīti kataloga attēli.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Images dialog box<ept id="p1">](./media/catalog4.png)](./media/catalog4.png)</ept></source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Dialoglodziņš Attēli<ept id="p1">](./media/catalog4.png)](./media/catalog4.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>You can use the same procedure for all the five entities that are supported: Worker, Customer, Catalog, Category, and Products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Varat izmantot tādu pašu procedūru visiem pieciem elementiem, kas tiek atbalstīti: Darbinieks, Debitors, Katalogs, Kategorija un Preces.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>"Catalog Products" (products that are set at the catalog level) and "Channel Products" (products that are set at the channel level) use the media template that is set for the Products entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"Kataloga preces" (preces, kas iestatītas kataloga līmenī) un "Kanāla preces" (preces, kas iestatītas kanāla līmenī) izmanto multivides veidni, kas ir iestatīta elementam Preces.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>For the Products media template, you can select the number of product images to show per product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preču multivides veidnei var atlasīt vairākus preču attēlus, lai tos parādītu katrai precei.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>You can also set the default image for a given product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jūs varat arī iestatīt noklusējuma attēlu konkrētai precei.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>In this way, you can prevent blank images in MPOS and help to control which image is used as the default image for a product item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šādā veidā varat novērst tukšus attēlus MPOS un palīdzēt kontrolēt, kurš attēls tiek izmantots kā noklusējuma attēls produkta krājumam.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the following example, each product has five images, and the first image is set as the default image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā piemērā, katrai precei ir pieci attēli un pirmais attēls ir iestatīts kā noklusējuma attēls.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Variant products are treated the same way as master products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preču varianti tiek apstrādāti tāpat, kā pamata preces.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The file name of the image file should be based on the product number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Attēla faila nosaukumam ir jābalstās uz preces numuru.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Some characters are also escaped while the file name is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dažas rakstzīmes arī tiek pārslēgtas, kamēr faila nosaukums tiek ģenerēts.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Therefore, it's a good to verify the file name by using the <bpt id="p1">**</bpt>Generate Image URLs for Excel<ept id="p1">**</ept> section.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Tāpēc būtu labi pārbaudīt faila nosaukumu, izmantojot sadaļu <bpt id="p1">**</bpt>Ģenerēt attēlu vietrāžus URL programmai Excel<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Define media template dialog box<ept id="p1">](./media/prods.png)](./media/prods.png)</ept></source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Dialoglodziņš Definēt multivides veidni<ept id="p1">](./media/prods.png)](./media/prods.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Synchronization jobs to send a media template to the channel side</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Sinhronizēšanas darbi, lai nosūtītu multivides veidni uz kanāla pusi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>For all the five supported entities (Worker, Customer, Catalog, Category, and Products), whenever you update the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog to set up an image, make sure that you run the Catalog job (1150) from <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visiem pieciem atbalstītajiem elementiem (Darbinieks, Debitors, Katalogs, Kategorija un Preces) ikreiz, kad jūs atjaunināt dialoglodziņu <bpt id="p1">**</bpt>Definēt multivides veidni<ept id="p1">**</ept>, lai iestatītu attēlu, pārliecinieties, ka izpildāt Kataloga darbu (1150) no <bpt id="p2">**</bpt>Mazumtirdzniecības IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Sadales grafiks<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This job will enable the updated media template to be synced to the channel and used by MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šis darbs aktivizēs atjaunotās multivides veidnes sinhronizāciju ar kanālu un ļaus MPOS to izmantot.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Run the Catalog job (1150) after you make any of the following changes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Palaidiet Kataloga darbu (1150), ja veicāt kādu no šādām izmaiņām:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>You update the Catalog image media template from <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jūs atjaunināt Kataloga attēla multivides veidni no <bpt id="p1">**</bpt>Kataloga attēli<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Definēt multivides veidni<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>You update the Employee image media template from <bpt id="p1">**</bpt>Employee images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jūs atjaunināt Darbinieka attēla multivides veidni no <bpt id="p1">**</bpt>Darbinieka attēli<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Definēt multivides veidni<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>You update the Customer image media template from <bpt id="p1">**</bpt>Customer image<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jūs atjaunināt Debitora attēla multivides veidni no <bpt id="p1">**</bpt>Debitora attēls<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Definēt multivides veidni<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>You update the Product image media template from <bpt id="p1">**</bpt>Product images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jūs atjaunināt Preces attēla multivides veidni no <bpt id="p1">**</bpt>Preces attēli<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Definēt multivides veidni<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You update the Category image media template from <bpt id="p1">**</bpt>Category images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jūs atjaunināt Kategorijas attēla multivides veidni no <bpt id="p1">**</bpt>Kategorijas attēli<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Definēt multivides veidni<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>You must also publish the channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jums ir arī jāpublicē kanāls.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Overwriting the media template for entity items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Elementa krājumu multivides veidnes pārrakstīšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>As you learned in the previous section, the media template for a given entity supports only one common path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kā minēts iepriekšējā sadaļā, noteiktā elementa multivides veidne atbalsta tikai vienu kopīgu ceļu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>This path is based on the media base URL that is configured and the media path that is defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šis ceļš ir balstīts uz konfigurēto multivides pamata vietrādi URL un definēto multivides ceļu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>However, in many cases, a retailer wants to be able to use images from different sources for a subset of items in an entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tomēr daudzos gadījumos mazumtirdzniecības veikals vēlas, lai krājumu apakškopai elementā varētu izmantot attēlus no dažādiem avotiem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>For example, a store uses the self-hosted media server for one set of catalog images but uses CDN URLs for another set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Piemēram, veikals izmanto pašviesotu multivides serveri vienai kataloga attēlu kopai un CDN vietrāžus URL citai kopai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>To overwrite image URLs that are based on a media template for entity images at the entity level, you can use the Edit in Excel and Manual edit functionality from the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai pārrakstītu attēla vietrādi URL elementa attēlu multivides veidnē elementa līmenī, varat izmantot funkciju Rediģēt programmā Excel un funkciju Manuāli rediģēt lapā <bpt id="p1">**</bpt>Priekšskatījums<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Overwrite by using Edit in Excel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārrakstīšana, izmantojot funkciju Rediģēt programmā Excel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Catalog management<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Catalog images<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Mazumtirdzniecība<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Kataloga pārvaldība<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Kataloga attēli<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>On the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lapā <bpt id="p1">**</bpt>Kataloga attēli<ept id="p1">**</ept> noklikšķiniet uz <bpt id="p2">**</bpt>Definēt multivides veidni<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>In the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Entity<ept id="p2">**</ept> field, <bpt id="p3">**</bpt>Catalog<ept id="p3">**</ept> should be selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dialoglodziņā <bpt id="p1">**</bpt>Definēt multivides veidni<ept id="p1">**</ept> laukā <bpt id="p2">**</bpt>Elements<ept id="p2">**</ept> jāatlasa <bpt id="p3">**</bpt>Katalogs<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>On the <bpt id="p1">**</bpt>Media path<ept id="p1">**</ept> FastTab, notice the image location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kopsavilkuma cilnē <bpt id="p1">**</bpt>Multivides ceļš<ept id="p1">**</ept> ņemiet vērā attēla atrašanās vietu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>On the <bpt id="p1">**</bpt>Generate Image URLs for Excel<ept id="p1">**</ept> FastTab, click <bpt id="p2">**</bpt>Generate<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kopsavilkuma cilnē <bpt id="p1">**</bpt>Ģenerēt attēlu vietrāžus URL programmai Excel<ept id="p1">**</ept> noklikšķiniet uz <bpt id="p2">**</bpt>Ģenerēt<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Whenever the media template is changed, you must click <bpt id="p1">**</bpt>Generate<ept id="p1">**</ept> before you can use the Edit in Excel functionality.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kad multivides veidne tiek mainīta, jums jānoklikšķina uz <bpt id="p1">**</bpt>Ģenerēt<ept id="p1">**</ept> pirms varat izmantot funkciju Rediģēt programmā Excel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Generate Image URLs for Excel FastTab<ept id="p1">](./media/excel1.jpg)](./media/excel1.jpg)</ept></source><target logoport:matchpercent="0" state="translated"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Kopsavilkuma cilne Ģenerēt attēlu vietrāžus URL programmai Excel<ept id="p1">](./media/excel1.jpg)](./media/excel1.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>You now see a preview of the image URLs that were generated based on the last saved media template.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Tagad ir redzams attēla vietrāžu URL priekšskatījums, kas tika ģenerēti, pamatojoties uz pēdējo saglabāto multivides veidni.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Generate Image URLs for Excel FastTab after Generate is selected<ept id="p1">](./media/excel2.png)](./media/excel2.png)</ept></source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Kopsavilkuma cilne Ģenerēt attēlu vietrāžus URL programmai Excel pēc vienuma Ģenerēt atlasīšanas<ept id="p1">](./media/excel2.png)](./media/excel2.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>The URLs that are generated for Excel use the path and conventions of the media template that is defined.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Vietrāžos URL, kas tiek ģenerēti programmai Excel, tiek izmantots ceļš un definētās multivides veidnes noteikumi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>These conventions include the conventions for file names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šie noteikumi ietver failu nosaukumu veidošanas noteikumus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>The expectation is that you've set up the physical images outside Dynamics 365 for Retail, and the images can be retrieved from the URLs that are derived from the media template that you defined earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tiek sagaidīts, ka fizisko attēli ir iestatīti ārpus programmas Dynamics 365 for Retail un attēlus var izgūt, izmantojot vietrāžus URL, kas ir atvasināti no iepriekš definētās multivides veidnes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>You can overwrite these derived URLs by using the Edit in Excel functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šos atvasinātos vietrāžus URL var pārrakstīt, izmantojot funkciju Rediģēt programmā Excel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Click <bpt id="p1">**</bpt>Edit in Excel<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Rediģēt programmā Excel<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>After the Microsoft Excel worksheet is opened, click <bpt id="p1">**</bpt>Enable edit<ept id="p1">**</ept> when you're prompted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad ir atvērta Microsoft Excel darblapa un tiek parādīta attiecīga uzvedne, noklikšķiniet uz <bpt id="p1">**</bpt>Iespējot rediģēšanu<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>When you're prompted, click <bpt id="p1">**</bpt>Trust this add-in<ept id="p1">**</ept> in the right pane, and wait for the add-in to complete the installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad tiek parādīta uzvedne, noklikšķiniet uz <bpt id="p1">**</bpt>Uzticēties šai pievienojumprogrammai<ept id="p1">**</ept> labajā rūtī un uzgaidiet, kamēr pievienojumprogramma tiek instalēta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Trust this add-in<ept id="p1">](./media/excel4.jpg)](./media/excel4.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Uzticēties šai pievienojumprogrammai<ept id="p1">](./media/excel4.jpg)](./media/excel4.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>If you're prompted to sign in, enter the credentials that you used to sign in to HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja tiek piedāvāts pierakstīties, ievadiet akreditācijas datus, ko izmantojat, lai pierakstītos HQ.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Sign-in prompt<ept id="p1">](./media/excel5.png)](./media/excel5.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Pierakstīšanās uzvedne<ept id="p1">](./media/excel5.png)](./media/excel5.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>After you sign in, you should be able to see the list of image URLs for the various catalog entries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad esat pierakstījies, vajadzētu būt redzamam attēlu vietrāžu URL sarakstam dažādiem kataloga ierakstiem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>You edit, add, and remove the image URLs for various entity items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rediģējiet, pievienojiet vai noņemiet attēlu vietrāžus URL dažādiem elementu krājumiem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>For all entities except Products, you can overwrite the image URLs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visiem elementiem, izņemot Preces, attēla vietrādi URL var pārrakstīt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Modify the existing image URL, so that it uses the new destination URL of the image, and update the file name with the new file name for the image file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modificējiet esošo attēla vietrādi URL, lai tas izmantotu jaunu attēla galamērķa vietrādi URL un atjauninātu faila nosaukumu ar jaunu šī attēla faila nosaukumu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The file name must be unique to help guarantee that the record is unique.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Faila nosaukumam ir jābūt unikālam, lai palīdzētu nodrošināt, ka ieraksts ir unikāls.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Overwrite the image URLs in Excel<ept id="p1">](./media/excel6.jpg)](./media/excel6.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Attēla vietrāžu URL pārrakstīšana programmā Excel<ept id="p1">](./media/excel6.jpg)](./media/excel6.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>When you overwrite image URLs for Products entities by using the Edit in Excel functionality or the entity item page, MPOS always shows all the media template image URLs together with the overwritten image URLs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad pārrakstāt attēla vietrāžus URL elementiem Preces, izmantojot funkciju Rediģēt programmā Excel vai elementa krājumu lapā, MPOS vienmēr rāda visus multivides veidnes attēlu vietrāžus URL kopā ar pārrakstītajiem attēlu vietrāžiem URL.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>After you've finished making your changes, click <bpt id="p1">**</bpt>Publish in Excel<ept id="p1">**</ept> to create a new explicit association entry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad esat beidzis veikt izmaiņas, noklikšķiniet uz <bpt id="p1">**</bpt>Publicēt programmā Excel<ept id="p1">**</ept>, lai izveidotu jaunu tiešas saistības ierakstu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Return to HQ, and click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Atgriezieties uz HQ un noklikšķiniet uz <bpt id="p1">**</bpt>Labi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Run the appropriate synchronization jobs for the entity, and check the preview on the entity page or in MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Palaidiet atbilstošus elementa sinhronizēšanas darbus un pārbaudiet priekšskatījumu elementa lapā vai MPOS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Creating new records</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jaunu ierakstu veidošana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>You can create new records in Excel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jaunus ierakstus var veidot programmā Excel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>However, make sure that you provide the correct information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tomēr, pārliecinieties, vai tiek norādīta pareiza informācija.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>For example, to create a new entry for a catalog, make sure that the catalog ID and catalog name are correct, and also provide a unique file name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Piemēram, lai izveidotu jaunu ierakstu katalogā, pārliecinieties, vai kataloga ID un kataloga nosaukums ir pareizs un norādiet arī unikālu faila nosaukumu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The unique file name is very important, because the uniqueness of records in Excel is validated during publishing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Unikāls faila nosaukums ir ļoti svarīgs, jo ierakstu unikalitāte programmā Excel tiek apstiprināta publicēšanas laikā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>First copy the details from the catalog that you want to create a new record for, and copy the record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vispirms nokopējiet informāciju no kataloga, kuram vēlaties izveidot jaunu ierakstu, un kopējiet ierakstu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>You just have to update the file name and URL, because the rest of the information will be same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jums vienkārši ir jāatjaunina faila nosaukums un vietrādis URL, jo pārējā informācija būs tāda pati.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>To create new records for Product entity items, you use the same basic procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai izveidotu jaunus ierakstus elementa Preces krājumiem, izmantojiet to pašu pamata procedūru.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>From the Excel worksheet, copy an existing record for the product that you to create a new record for, and then replace the image URL and filename.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">No Excel darblapas kopējiet esošu ierakstu precei, kurai izveidojat jaunu ierakstu, un pēc tam aizstājiet attēla vietrādi URL un faila nosaukumu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Make sure that the file name is unique.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārliecinieties, ka faila nosaukums ir unikāls.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Deleting an existing record</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Esoša ieraksta dzēšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Only the overwritten image URL records can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Var dzēst tikai pārrakstītus attēla vietrāžu URL ierakstus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>After an image is deleted and synchronization is completed, the image will no longer appear on the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page or in MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad attēls ir dzēsts un sinhronizācija ir pabeigta, attēls vairs neparādīsies lapā <bpt id="p1">**</bpt>Priekšskatījums<ept id="p1">**</ept> vai MPOS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Image URL records that are derived from the media template can't be deleted, because these records are always derived from the media template every time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Attēla vietrāža URL ierakstus, kas ir iegūti no multivides veidnes, nevar dzēst, jo šie ieraksti vienmēr, katru reizi tiek atvasināti no multivides veidnes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Overwrite from the entity-level Preview page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārrakstīšana no elementa līmeņa lapas Priekšskatījums</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>For all entities except Products, you can overwrite the image URL for a given entity item at the entity item level from the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visiem elementiem, izņemot Preces, var pārrakstīt dotā elementā krājuma attēlu vietrādi URL elementa krājuma līmenī no lapas <bpt id="p1">**</bpt>Priekšskatījums<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>For Products, you can use the "Catalog Products" entity page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Precēm var izmantot elementa lapu "Kataloga preces".</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>This example shows how to overwrite a catalog image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā piemērā parādīts, kā pārrakstīt kataloga attēlu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Click <bpt id="p1">**</bpt>Catalogs<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Media<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Images<ept id="p3">**</ept>, and select the catalog image to update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Katalogi<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Multivide<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Attēli<ept id="p3">**</ept>, un atlasiet kataloga attēlu, kurš jāatjaunina.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>, and enter the image URL to overwrite the media template URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Pievienot<ept id="p1">**</ept> un ievadiet attēla vietrādi URL, lai pārrakstītu multivides veidnes vietrādi URL.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>If you want this image to be shown in MPOS for the catalog, you can set it as the default image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja vēlaties, lai šis attēls būtu redzams katalogam MPOS, to var iestatīt kā noklusējuma attēlu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Labi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>The image URL is updated for this catalog image, and a preview is shown.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Attēla vietrādis URL tiek atjaunināts šim kataloga attēlam, un tiek parādīts priekšskatījums.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>URL updated in the New image dialog box<ept id="p1">](./media/preview3.png)](./media/preview3.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Atjaunināts vietrādis URL dialoglodziņā Jauns attēls<ept id="p1">](./media/preview3.png)](./media/preview3.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>You can also see the image preview for all overwritten image URLs on the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> gallery page.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Jūs varat arī redzēt visu pārrakstīto attēlu vietrāžu URL attēla priekšskatījumu galerijas lapā <bpt id="p1">**</bpt>Kataloga attēli<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Catalog images gallery page<ept id="p1">](./media/preview-4.png)](./media/preview-4.png)</ept></source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Kataloga attēlu galerijas lapa<ept id="p1">](./media/preview-4.png)](./media/preview-4.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Currently, the gallery doesn't show image previews for media template image URLs.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Pašlaik galerija nerāda attēlu priekšskatījumus multivides veidnes attēlu vietrāžiem URL.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>For Catalog, Worker, Customer, and Category entities, if the user explicitly provides a URL through this page, we recommend that you indicate which image is the default image, because Retail Server clients show only one image per Catalog, Customer, Worker, and Category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja elementos Katalogs, Darbinieks, Debitors un Kategorija lietotājs skaidri norāda vietrādi URL, izmantojot šo lapu, mēs iesakām norādīt, kurš attēls ir noklusējuma attēls, jo mazumtirdzniecības servera klientiem tiek rādīts tikai viens attēls uz Katalogu, Debitoru, Darbinieku un Kategoriju.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>If the user doesn't specify a default image, the system determines the default image and send it to the Retail service caller (MPOS or Ecommerce).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja lietotājs nenorāda noklusējuma attēlu, sistēma nosaka noklusējuma attēlu un nosūta to mazumtirdzniecības pakalpojumu izsaucējam (MPOS vai e-Komercija).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Overwrite the image URL for catalog product images from the Preview page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kataloga preces attēlu vietrāža URL pārrakstīšana no lapas Priekšskatījums</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>To overwrite image URLs for catalog product images, you must use the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai pārrakstītu kataloga preču attēlu vietrāža URL, jāizmanto lapa <bpt id="p1">**</bpt>Priekšskatījums<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>You can't use the Edit in Excel functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Funkcionalitāti Rediģēt programmā Excel izmantot nevar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>To overwrite product images at a catalog level, select a catalog, and then select the product to overwrite the image for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai pārrakstītu preču attēlus kataloga līmenī, atlasiet katalogu un pēc tam atlasiet preci, kuras attēlu nepieciešams pārrakstīt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Click <bpt id="p1">**</bpt>Attributes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Atribūti<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>On the next page, select <bpt id="p1">**</bpt>Image<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Edit<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nākamajā lapā atlasiet <bpt id="p1">**</bpt>Attēls<ept id="p1">**</ept> un tad noklikšķiniet uz <bpt id="p2">**</bpt>Rediģēt<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>The <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page opens as a slider dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lapa <bpt id="p1">**</bpt>Priekšskatījums<ept id="p1">**</ept> tiek atvērta kā slīdņa dialoglodziņš.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>, and overwrite the image URL with a new URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Pievienot<ept id="p1">**</ept> un pārrakstiet attēla vietrādi URL ar jaunu vietrādi URL.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Labi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>You now see the preview of the new image and can set it as the default image.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Jūs tagad redzat jauna attēla priekšskatījumu un varat to iestatīt kā noklusējuma attēlu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Image preview in the New image dialog box<ept id="p1">](./media/cat3.png)](./media/cat3.png)</ept></source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Attēla priekšskatījums dialoglodziņā Jauns attēls<ept id="p1">](./media/cat3.png)](./media/cat3.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>After category image association, you must publish the channel and run the Channel job to help guarantee that the changes are published to the channel database.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Pēc kategorijas attēlu saistīšanas varat publicēt kanālu un palaist Kanāla darbu, lai palīdzētu nodrošināt, ka izmaiņas tiek publicētas kanāla datu bāzē.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Setting up images to appear in Offline mode for MPOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Attēlu, kas parādīsies MPOS bezsaistes režīmā, iestatīšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>MPOS can run in Online mode (when MPOS connected to Retail Server) or Offline mode (when there is no Retail Server or network connectivity, and transactions are stored in a local offline database).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS var darboties tiešsaistes režīmā (kad MPOS pieslēgts mazumtirdzniecības serverim) vai bezsaistes režīmā (kad nav mazumtirdzniecības servera vai tīkla savienojamības, un transakcijas tiek saglabātas vietējā bezsaistes datu bāzē).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>When MPOS runs in Offline mode, it can't get images from the external image server to display from Retail Server, because Retail Server connectivity has been lost.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad MPOS darbojas bezsaistes režīmā, tas nevar iegūt attēlus no ārējā attēlu servera, lai tos parādītu no mazumtirdzniecības servera, jo mazumtirdzniecības servera savienojamība ir zudusi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>However, you can still set up images so that they are shown when MPOS runs in Offline mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tomēr joprojām var iestatīt attēlus, lai tie tiktu rādīti, kad MPOS darbojas bezsaistes režīmā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Set up product images to appear in Offline mode for MPOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preču attēlu, kas parādīsies MPOS bezsaistes režīmā, iestatīšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>The product images that must be used in Offline mode can be set up by uploading the required physical image into the base product image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preču attēlus, kas jāizmanto bezsaistes režīmā, var iestatīt, augšupielādējot vajadzīgo fizisko attēlu pamata preces attēlā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Click <bpt id="p1">**</bpt>Product information management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Products<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Products<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Preču informācijas pārvaldība<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Preces<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Preces<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Select the product to set the offline image for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Atlasiet preci, kurai vēlaties iestatīt bezsaistes attēlu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Click <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>, and then click the arrow in the right corner to show the right pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Noklikšķiniet uz <bpt id="p1">**</bpt>Rediģēt<ept id="p1">**</ept> un pēc tam noklikšķiniet uz bultiņas labajā stūrī, lai parādītu labo rūti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>On the <bpt id="p1">**</bpt>Product image<ept id="p1">**</ept> FastTab, click <bpt id="p2">**</bpt>Change image<ept id="p2">**</ept>, and upload the physical image to use for the selected product in Offline mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kopsavilkuma cilnē <bpt id="p1">**</bpt>Preces attēls<ept id="p1">**</ept> noklikšķiniet uz <bpt id="p2">**</bpt>Mainīt attēlu<ept id="p2">**</ept> un augšupielādējiet fizisko attēlu, ko izmantot atlasītajai precei ir bezsaistes režīmā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Save and close the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Saglabājiet un aizveriet lapu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>While MPOS is in Online mode, run the Catalog job in HQ, to make sure that the data is sent at least one time to the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kamēr MPOS darbojas tiešsaistes režīmā, izpildiet HQ Kataloga darbu, lai pārliecinātos, ka dati tiek sūtīti uz bezsaistes datu bāzi vismaz vienu reizi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Put MPOS into Offline mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aktivizējiet MPOS bezsaistes režīmā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>You should see the image that you uploaded for the specific product in HQ.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Vajadzētu būt redzamam attēlam, ko augšupielādējāt noteiktai precei HQ.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Product image in Offline mode<ept id="p1">](./media/offline1.png)](./media/offline1.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Preces attēls bezsaistes režīmā<ept id="p1">](./media/offline1.png)](./media/offline1.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Set up catalog, category, employee, and customer images to appear in Offline mode for MPOS</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kataloga, kategorijas, darbinieka un debitora attēlu, kas parādīties MPOS bezsaistes režīmā, iestatīšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>The catalog, category, employee, and customer images that must be used in Offline mode can be set up by adding the required image's destination link to the gallery and setting the image as the default image for the selected entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kataloga, kategorijas, darbinieka un debitora attēlus, kas jāizmanto bezsaistes režīmā, var iestatīt, pievienojot vajadzīgā attēlā galamērķa saiti galerijai un iestatot attēlu kā noklusējuma attēlu atlasītajam elementam.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Go to the catalog, and then, on the Action Pane, click <bpt id="p1">**</bpt>Media<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Images<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dodieties uz katalogu un pēc tam darbību rūtī noklikšķiniet uz <bpt id="p1">**</bpt>Multivide<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Attēli<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Follow the steps in the <bpt id="p1">[</bpt>Overwrite from the entity-level Preview page<ept id="p1">](#overwrite-from-the-entity-level-preview-page)</ept> section to add the external image URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Izpildiet darbības sadaļā <bpt id="p1">[</bpt>Pārrakstīšana no elementa līmeņa lapas Priekšskatījums<ept id="p1">](#overwrite-from-the-entity-level-preview-page)</ept>, lai pievienotu ārējo attēla vietrādi URL.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Mark this image as the default image for the catalog by selecting the check box against the Image listed in the grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Atzīmējiet šo attēlu kā noklusējuma attēlu katalogam, atzīmējot izvēles rūtiņu pretī Attēlam režģī.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Run the Catalog job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Izpildiet Kataloga darbu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>This image will now be used as the Offline image for that catalog in MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tagad šis attēls tiks izmantots kā šī kataloga bezsaistes attēls MPOS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Follow a similar process for other entities, such as Category, Employee, and Customer.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Veiciet līdzīgu procedūru citiem elementiem, piemēram, Kategorijai, Darbiniekam un Debitoram.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Offline image<ept id="p1">](./media/offline2.png)](./media/offline2.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Bezsaistes attēls<ept id="p1">](./media/offline2.png)](./media/offline2.png)</ept></target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>