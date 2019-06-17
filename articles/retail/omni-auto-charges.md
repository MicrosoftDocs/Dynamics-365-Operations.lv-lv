<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="omni-auto-charges.md" target-language="lv-LV">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>omni-auto-charges.2f6e37.47829a6fcae37e03510929dc46b942455016df0b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>47829a6fcae37e03510929dc46b942455016df0b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\omni-auto-charges.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Multikanālu papildu automātiskās maksas</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes capabilities for managing additional order charges for Retail channel orders using advanced auto charges features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā tēmā ir aprakstītas iespējas pārvaldīt pasūtījuma papildu maksas mazumtirdzniecības kanāla pasūtījumiem, izmantojot papildu automātisko maksu līdzekļus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Multikanālu papildu automātiskās maksas</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information on configuration and deployment of the advanced auto-charges feature which are available in Dynamics 365 for Retail version 10.0.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā tēmā ir sniegta informācija par to, kā konfigurēt un izvietot papildu automātisko maksu līdzekli, kas ir pieejams Dynamics 365 for Retail versijā 10.0.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When the advanced auto-charges features are enabled, orders created in any supported Retail channel (point of sale (POS), call center, and online), can take advantage of the <bpt id="p1">[</bpt>auto-charges<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations defined in the ERP application for both header and line-level related charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja ir iespējoti papildu automātisko maksu līdzekļi, jebkurā atbalstītajā mazumtirdzniecības kanālā (pārdošanas punktā (POS), zvanu centrā un tiešsaistē) izveidotajiem pasūtījumiem var izmantot ERP lietojumprogrammā definētās <bpt id="p1">[</bpt>automātisko maksu<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> konfigurācijas gan galvas, gan rindas līmeņa saistītajām maksām.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In releases prior to Dynamics 365 for Retail version 10.0, <bpt id="p1">[</bpt>auto-charge<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations are only accessible by orders created in e-Commerce and call center channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Laidienos pirms Dynamics 365 for Retail versijas 10.0 <bpt id="p1">[</bpt>automātisko maksu<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> konfigurācijas ir pieejamas tikai pasūtījumiem, kas ir izveidoti e-komercijas un zvanu centra kanālos.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In versions 10.0 and later, POS-created orders can leverage the auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Versijā 10.0 un jaunākās versijās automātisko maksu konfigurācijas var izmantot POS sistēmā izveidotiem pasūtījumiem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>That way, additional miscellaneous charges can systematically be added to sales transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tādējādi var pārdošanas transakcijām sistemātiski pievienot papildu papildmaksas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>When using releases prior to version 10.0, a POS user is prompted to manually enter a shipping fee during the creation of a "ship all" or "ship selected" POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Laidienos pirms versijas 10.0, veicot POS transakciju Piegādāt visu vai Piegādāt atlasīto, POS lietotājam tiek prasīts manuāli ievadīt piegādes maksu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>While the miscellaneous charges capabilities of the application are utilized in respect to how the charges are written to the order, no systematic calculation is provided – the calculation relies on the user's input to determine the value of the charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Lai gan programmas papildmaksu iespējas tiek izmantotas attiecībā uz to, kā maksas tiek ierakstītas pasūtījumā, netiek nodrošināts sistemātisks aprēķins — maksu vērtības aprēķinam tiek izmantota lietotāja ievadītā vērtība.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The charges can only be added as a single "shipping" related charges code and cannot easily be edited or changed in the POS after they are created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maksas var pievienot tikai kā vienu ar piegādi saistītu maksu kodu, un pēc maksu izveides, tā nevar viegli rediģēt vai mainīt POS sistēmā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The use of manual prompts to add shipping charges is still available in versions 10.0 and later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Versijā 10.0 un jaunākās versijās joprojām ir pieejama iespēja izmantot manuālas piegādes maksu pievienošanas uzvednes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If an organization does not enable the <bpt id="p1">**</bpt>Advanced Auto-charges<ept id="p1">**</ept> parameter, the POS prompts for manual entry of charges will remain the same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja organizācija neiespējo parametru <bpt id="p1">**</bpt>Papildu automātiskās maksas<ept id="p1">**</ept>, tiek izmantotas tādas pašas POS sistēmas uzvednes ar aicinājumu manuāli ievadīt maksas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>With the advanced auto-charges feature, POS users can have systematic calculations for any defined miscellaneous charges based on auto-charges setup tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Papildu automātisko maksu līdzeklis sniedz POS lietotājiem iespēju izmantot jebkuru definēto papildmaksu sistemātisku aprēķinu, pamatojoties uz automātisko maksu iestatījumu tabulām.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In addition, users will have the ability to add or edit an unlimited amount of additional charges and fees to any POS sales transaction at the header or line-level (for a cash and carry or customer order).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Turklāt lietotāji var pievienot vai rediģēt neierobežotu skaitu papildu maksu un nodevu jebkurai POS pārdošanas transakcijai galvas vai rindas līmenī (skaidrā naudā apmaksātam pasūtījumam bez piegādes vai debitora pasūtījumam).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Enabling advanced auto-charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Papildu automātisko maksu iespējošana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>On the <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail parameters<ept id="p1">**</ept> page, go to the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab. On the <bpt id="p3">**</bpt>Charges<ept id="p3">**</ept> FastTab, set <bpt id="p4">**</bpt>Use advanced auto-charges<ept id="p4">**</ept> to <bpt id="p5">**</bpt>Yes<ept id="p5">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Lapā <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Mazumtirdzniecības iestatīšana <ph id="ph2">\&gt;</ph> Parametri <ph id="ph3">\&gt;</ph> Mazumtirdzniecības parametri<ept id="p1">**</ept> dodieties uz cilni <bpt id="p2">**</bpt>Klientu pasūtījumi<ept id="p2">**</ept>. Kopsavilkuma cilnē <bpt id="p3">**</bpt>Maksas<ept id="p3">**</ept> opcijai <bpt id="p4">**</bpt>Izmantot papildu automātiskās maksas<ept id="p4">**</ept> iestatiet vērtību <bpt id="p5">**</bpt>Jā<ept id="p5">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Advanced Auto-Charges Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Parametrs Papildu automātiskās maksas</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>When advanced auto-charges are enabled, users are no longer prompted to manually enter a shipping charge at the POS terminal when creating a ship-all or ship-selected customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad ir iespējotas papildu automātiskās maksas, izveidojot debitora pasūtījumu Piegādāt visu vai Piegādāt atlasīto, lietotājiem vairs netiek parādīta uzvedne ar norādi manuāli ievadīt piegādes maksu POS terminālī.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>POS order charges are systematically calculated and added to the POS transaction (if a corresponding auto-charges table that matches the criterion of the order being created are found).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS pasūtījuma maksas tiek sistemātiski aprēķinātas un pievienotas POS transakcijai (ja tiek atrasta izveidotā pasūtījuma kritērijiem atbilstoša automātisko maksājumu tabula).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Users can also add or maintain header or line-level charges manually through newly added POS operations that can be added to the POS screen layouts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lietotāji var arī manuāli pievienot vai uzturēt galvas vai rindas līmeņa maksas, izmantojot jaunās POS operācijas, ko var pievienot POS ekrāna izkārtojumiem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>When advanced auto-charges are enabled, the existing <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> for <bpt id="p2">**</bpt>Shipping charges code<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> are no longer utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad ir iespējotas papildu automātiskās maksas, vairs netiek izmantoti esošie vienumu <bpt id="p2">**</bpt>Piegādes maksu kods<ept id="p2">**</ept> un <bpt id="p3">**</bpt>Atmaksāt piegādes maksas<ept id="p3">**</ept> parametri sadaļā <bpt id="p1">**</bpt>Mazumtirdzniecības parametri<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>These parameters are only applicable if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šie parametri tiek lietoti tikai tad, ja ir iestatīta parametra <bpt id="p1">**</bpt>Izmantot papildu automātiskās maksas<ept id="p1">**</ept> vērtība <bpt id="p2">**</bpt>Nē<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Before you enable this feature, ensure that you have tested and trained your employees, as this will change the business process flow of how shipping or other charges are calculated and added to POS sales orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pirms šī līdzekļa iespējošanas noteikti veiciet savu darbinieku pārbaudi un apmācību, jo tādējādi tiks mainīta biznesa procesu plūsma piegādes vai citu maksu aprēķināšanai un pievienošanai POS pārdošanas pasūtījumiem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Make sure that you understand the impact of the process flow to the creation of transactions from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārliecinieties, vai saprotat procesa plūsmas ietekmi uz transakciju izveidi POS sistēmā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For call center and e-Commerce orders, the impact of enabling advanced auto-charges is minimal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Papildu automātisko maksu iespējošana minimāli ietekmē zvanu centra un e-komercijas pasūtījumus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Call center and e-Commerce applications will continue to have the same behavior they have had historically related to the auto-charges tables to calculate additional order fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zvanu centra un e-komercijas lietojumprogrammas darbojas tāpat kā iepriekš attiecībā uz automātisko maksājumu tabulu izmantošanu, lai aprēķinātu pasūtījuma papildu maksas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Call center channel users will continue to have the ability to manually edit any system calculated auto-charges at the header or line level, or manually add additional miscellaneous charges at the header or line level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zvanu centra kanāla lietotāji joprojām var manuāli rediģēt jebkuru sistēmas aprēķināto automātisko maksu galvas vai rindas līmenī vai manuāli pievienot papildu papildmaksas galvas vai rindas līmenī.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Additional POS operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS papildu operācijas</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For advanced auto-charges to work properly in your POS application environment, new POS operations have been added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai nodrošinātu papildu automātisko maksu pareizu darbību POS lietojumprogrammu vidē, ir pievienotas jaunas POS operācijas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>These operations must be added to your <bpt id="p1">[</bpt>POS screen layouts<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> and deployed to the POS devices as you deploy advanced auto-charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šīs operācijas ir jāpievieno jūsu <bpt id="p1">[</bpt>POS ekrāna izkārtojumiem<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> un jāizvieto POS ierīcēs, kad izvietojat papildu automātiskās maksas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If these operations are not added, users will not be able to manage or maintain miscellaneous charges on the POS transactions and will have no way of adjusting or changing the charges values that are systematically calculated based on auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja šīs operācijas netiek pievienotas, lietotāji nevar pārvaldīt vai uzturēt POS transakciju papildmaksas un nevar nekādā veidā pielāgot vai mainīt maksu vērtības, kas ir sistemātiski aprēķinātas, pamatojoties uz automātisko maksu konfigurācijām.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>At minimum, it is suggested that you deploy the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation to your POS layout.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Ir ieteicams izvietot POS izkārtojumā vismaz operāciju <bpt id="p1">**</bpt>Pārvaldīt maksas<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The new operations are as follows.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Tālāk ir norādītas jaunās operācijas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>142 - Manage charges<ept id="p1">**</ept> – Use this operation to allow POS users to view and edit miscellaneous charges for the POS transaction that were either added manually or systematically through auto-charges calculations.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>142. Pārvaldīt maksas<ept id="p1">**</ept> — izmantojiet šo operāciju, lai sniegtu POS lietotājiem iespēju skatīt un rediģēt papildmaksas POS transakcijām, kas tika pievienotas manuāli vai sistemātiski, izmantojot automātisko maksu aprēķinus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>141 - Add header charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a header-level miscellaneous charge to any POS sales transaction (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>141. Pievienot galvenes maksas<ept id="p1">**</ept> — izmantojiet šo operāciju, lai sniegtu lietotājam iespēju manuāli pievienot galvenes līmeņa papildmaksu jebkurai POS pārdošanas transakcijai (un atlasīt izmantojamo maksu kodu).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>140 - Add line charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a line level miscellaneous charge to any POS sales transaction line (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>140. Pievienot rindas maksas<ept id="p1">**</ept> — izmantojiet šo operāciju, lai sniegtu lietotājam iespēju manuāli pievienot rindas līmeņa papildmaksu jebkurai POS pārdošanas transakcijas rindai (un atlasīt izmantojamo maksu kodu).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>143 - Recalculate charges<ept id="p1">**</ept> – Use this operation to perform a full re-calculation of the charges for the sales transaction.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>143. Pārrēķināt maksas<ept id="p1">**</ept> — izmantojiet šo operāciju, lai pārdošanas transakcijas maksas pārrēķinātu pilnībā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Any previously user-overwritten auto-charges will be recalculated based on the current cart configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visas lietotāja iepriekš pārrakstītās automātiskās maksas tiek pārrēķinātas, pamatojoties uz pašreizējo groza konfigurāciju.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>As with all POS operations, security configurations can be made to require manager approval in order to execute the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tāpat kā visām POS operācijām, arī šai operācijai var izveidot drošības konfigurācijas, lai pieprasītu, ka vadītājam ir jāapstiprina operācijas izpilde.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>It is important to note that the above listed POS operations can also be added to the POS layout even if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ir svarīgi atzīmēt, ka iepriekš uzskaitītās POS operācijas var pievienot POS izkārtojumam arī tad, ja parametrs <bpt id="p1">**</bpt>Izmantot papildu automātiskās maksas<ept id="p1">**</ept> ir atspējots.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In this scenario, organizations will still get added benefits of being able to view manually added charges and edit them using the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šādā gadījumā organizācijas vēl joprojām iegūst papildu priekšrocības, kas ļauj skatīt manuāli pievienotās maksas un rediģēt tās, izmantojot operāciju <bpt id="p1">**</bpt>Pārvaldīt maksas<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Users may also use the <bpt id="p1">**</bpt>Add header charges<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Add line charges<ept id="p2">**</ept> operations for POS transactions even when <bpt id="p3">**</bpt>Use advanced auto-charges<ept id="p3">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lietotāji var izmantot arī POS transakciju operāciju <bpt id="p1">**</bpt>Pievienot virsraksta maksas<ept id="p1">**</ept> un <bpt id="p2">**</bpt>Pievienot rindas maksas<ept id="p2">**</ept> arī tad, ja parametrs <bpt id="p3">**</bpt>Izmanto papildu automātiskās maksas<ept id="p3">**</ept> ir atspējots.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation has less functionality if used when <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja parametrs <bpt id="p2">**</bpt>Izmantot papildu automātiskās maksas<ept id="p2">**</ept> ir atspējots, izmantošanas gadījumā operācijai <bpt id="p1">**</bpt>Pārrēķināt maksas<ept id="p1">**</ept> ir zemāka funkcionalitāte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In this sceanrio, nothing would be recalculated and any charges manually added to the transaction would just reset to $0.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā gadījumā neviena vērtība netiks pārrēķināta, un visas transakcijai manuāli pievienotās maksas tiks atiestatītas uz $0,00.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Use case examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lietošanas gadījumu piemēri</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In this section, sample use cases are presented to help you understand the configuration and usage of auto-charges and miscellaneous charges within the context of Retail channel orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā sadaļā ir aprakstīti lietošanas gadījumu piemēri, lai palīdzētu jums saprast, kā konfigurēt un izmantot automātiskās maksas un papildmaksas mazumtirdzniecības kanāla pasūtījumu kontekstā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>These examples illustrate the behavior of the application when the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter has been enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajos piemēros ir aprakstīta lietojumprogrammas darbība gadījumā, ja ir iespējots parametrs <bpt id="p1">**</bpt>Izmantot papildu automātiskās maksas<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Auto-charges header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Galvas līmeņa automātisko maksu piemērs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lietošanas gadījuma scenārijs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>A retailer wants to automatically add charges for freight when transactions are created in any Retail channel that require a shipment of products to the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mazumtirgotājs vēlas automātiski pievienot transportēšanas maksas, kad jebkurā mazumtirdzniecības kanālā tiek izveidotas transakcijas, kurām ir nepieciešama preču piegāde debitoram.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The retailer offers 2 methods of delivery: Ground and Air.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mazumtirgotājs piedāvā 2 piegādes metodes: pa zemi un pa gaisu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>If a customer chooses Ground delivery and the order value is less than $100, the retailer wants to charge the customer a freight charge of $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja debitors izvēlas piegādi pa zemi un pasūtījuma vērtība ir mazāka nekā 100 USD, mazumtirgotājs vēlas iekasēt no debitora transportēšanas maksu 10,00 USD apmērā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>If the order is over $100 in value and the customer chooses ground shipping, the customer will not be charged any additional freight fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja pasūtījuma vērtība ir lielāka nekā 100 USD un debitors izvēlas piegādi pa zemi, debitoram nav jāmaksā nekādas papildu transportēšanas maksas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If the customer chooses the Air method of delivery for all orders, regardless of their total value, will be charged a freight fee of $20.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja debitors izvēlas piegādi pa gaisu visiem pasūtījumiem neatkarīgi no to kopējās vērtības, tiek iekasēta transportēšanas maksa 20,00 USD apmērā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Iestatīšana un konfigurēšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This scenario requires the configuration of two auto-charges tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šī scenārija ietvaros ir jākonfigurē divas automātisko maksu tabulas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Go to <bpt id="p1">**</bpt>Accounts receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārejiet uz sadaļu <bpt id="p1">**</bpt>Kreditori <ph id="ph1">\&gt;</ph> Maksu iestatīšana <ph id="ph2">\&gt;</ph> Automātiskās maksas<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Configure two different header-level auto charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurējiet divas dažādas galvas līmeņa automātiskās maksas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Configure one for the "Ground mode" of delivery and one for the "Air mode" of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurēt vienu maksu piegādes pa zemi režīmam un vienu maksu piegādes pa gaisu režīmam.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>For this scenario, configure them to be used for "All customers".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šī scenārija ietvaros konfigurējiet tās lietošanai visiem debitoriem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>For the ground delivery charges, in the lines section of the <bpt id="p1">**</bpt>Auto-charges<ept id="p1">**</ept> page, define a charge that will be applied for orders between $.01 and $100 as $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai konfigurētu piegādes pa zemi maksas, lapas <bpt id="p1">**</bpt>Automātiskās maksas<ept id="p1">**</ept> rindu sadaļā definējiet maksu 10.00 USD apmērā, kas ir jālieto pasūtījumiem, kuru vērtība ir no 0,01 USD līdz 100 USD.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Create another charges line to indicate orders over $100.01 will have no charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Izveidojiet citu maksu rindu, lai norādītu, ka pasūtījumiem, kuru vērtība ir lielāka nekā 100,01 USD, netiek lietotas nekādas maksas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Automātisko maksu piemērs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>For the air delivery charges, in the lines section of the auto-charges form, define a charge of $20.00 that will be applied to all orders (between a value of $.01 to $9,999,999).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai konfigurētu piegādes pa gaisu maksas, formas Automātiskās maksas rindu sadaļā definējiet maksu 20,00 USD apmērā, kas ir jālieto visiem pasūtījumiem (kuru vērtība ir no 0,01 USD līdz 9 999 999 USD).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Send the changes to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nosūtiet izmaiņas uz Retail Server/kanāla DB, lai tās varētu lietot POS sistēmā, izpildot darbu <bpt id="p1">**</bpt>1040 sadales grafiks<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārdošanas transakciju apstrāde šim scenārijam</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>After the configuration steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have the ground or air delivery methods set at the header level will utilize these charges and automatically apply them to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad ir izpildītas iepriekš aprakstītās konfigurēšanas darbības un izmaiņas ir ieviestas kanāla datu bāzē, jebkuram POS sistēmas, zvanu centra vai e-komercijas kanālā izveidotajam debitora pasūtījumam vai pārdošanas transakcijai, kam galvas līmenī ir iestatīta piegāde pa zemi vai pa gaisu, tiek izmantotas šīs maksas, un šādā gadījumā tās tiek automātiski lietotas pārdošanas darbībai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>At this time the charges will apply to all sales transactions created within the legal entity that utilize these delivery modes, as there is no functionality to designate that an auto-charge configuration will only apply to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pašlaik maksas tiek lietotas visām pārdošanas transakcijām, kas ir izveidotas juridiskajai personai, kura izmanto šos piegādes režīmus, jo nav pieejama funkcionalitāte, kas sniedz iespēju norādīt, ka automātiskās maksas konfigurācija ir jālieto tikai noteiktam pārdošanas kanālam.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For POS and e-Commerce scenarios, because there is no clearly defined "header" on these orders, header-level charges will only apply if all sales lines on the transaction are set to ship with the exact same mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS un e-komercijas scenārijos pasūtījumos nav skaidri definētas galvas, tāpēc galvas līmeņa maksas tiek lietotas tikai tad, ja visām transakcijas pārdošanas rindām ir iestatīts viens un tas pats piegādes režīms.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>If there are "mixed-modes" of fulfillment on the transactions created by POS or e-Commerce, only line-level auto-charges will be considered and applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja POS vai e-komercijas sistēmā izveidotajām transakcijām ir iestatīti jaukti izpildes režīmi, tiek izvērtētas un lietotas tikai rindas līmeņa automātiskās maksas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>In call center scenarios, the user has control over the setting of the delivery mode at the order header, therefore header-level charges will apply for these orders even if some of the sales lines have been configured to use a different mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zvanu centra scenārijos lietotājs var kontrolēt piegādes režīma iestatījumu pasūtījuma galvā, tāpēc šiem pasūtījumiem tiek lietotas galvas līmeņa maksas pat tad, ja dažas no pārdošanas rindām ir konfigurētas cita piegādes režīma izmantošanai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Header-level charges for call center orders will always be based on the mode of delivery that is defined at the order header level of the sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zvanu centra pasūtījumu galvas līmeņa maksas vienmēr tiek noteiktas, pamatojoties uz piegādes režīmu, kas ir definēts pārdošanas pasūtījuma galvas līmenī.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Auto-charges line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rindas līmeņa automātisko maksu piemērs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lietošanas gadījuma scenārijs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>A retailer wants to add an additional charge to the customer for setup fees when the customer purchases a particular model of computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mazumtirgotājs vēlas no debitora iekasēt papildu maksu par iestatīšanu gadījumā, ja debitors iegādājas noteiktu datora modeli.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This computer requires additional non-optional setup actions that the retailer will perform for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šim datoram ir nepieciešamas obligātas papildu iestatīšanas darbības, kuras mazumtirgotājs veic debitora vietā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The retailer has informed customers that there will be an additional fee for this setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mazumtirgotājs ir informējis debitorus par to, ka par šo iestatīšanu tiek ņemta papildu maksa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The retailer prefers to manage the charges related to this fee separately from the product sales price for financial reporting purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mazumtirgotājs vēlas finanšu pārskatu izveides nolūkos pārvaldīt ar šīs iestatīšanas maksas atsevišķi no preču pārdošanas cenas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>A setup fee of $19.99 will be charged to the customer when this specific computer is purchased in any retail channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Iegādājoties šo konkrēto datoru jebkurā mazumtirdzniecības kanālā, no debitora tiek iekasēta iestatīšanas maksa 19,99 USD apmērā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Iestatīšana un konfigurēšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This scenario requires the configuration of one line-level auto charges table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šī scenārija ietvaros ir jākonfigurē viena rindas līmeņa automātisko maksu tabula.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Go to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārejiet uz sadaļu <bpt id="p1">**</bpt>Kreditori <ph id="ph1">\&gt;</ph> Maksu iestatīšana <ph id="ph2">\&gt;</ph> Automātiskās maksas<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Set the <bpt id="p1">**</bpt>Level<ept id="p1">**</ept> drop-down menu to <bpt id="p2">**</bpt>Line<ept id="p2">**</ept>, and create a new auto-charges record for all customers and for the specific product or product group where the setup fees will be charged.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nolaižamajā izvēlnē <bpt id="p1">**</bpt>Līmenis<ept id="p1">**</ept> iestatiet vērtību <bpt id="p2">**</bpt>Rinda<ept id="p2">**</ept> un izveidojiet jaunu automātisko maksājumu ierakstu visiem debitoriem un konkrētajai precei vai preču grupai, par kuru tiks iekasēta iestatīšanas maksa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Automātisko maksu piemērs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nosūtiet maksas uz Retail Server/kanāla DB, lai tās varētu lietot POS sistēmā, izpildot darbu <bpt id="p1">**</bpt>1040 sadales grafiks<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārdošanas transakciju apstrāde šim scenārijam</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>After the configurations steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have this item on the order will trigger a line-level charge to be systematically added to the order total.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad ir izpildītas iepriekš aprakstītās konfigurēšanas darbības un izmaiņas ir ieviestas kanāla datu bāzē, jebkurš POS sistēmas, zvanu centra vai e-komercijas kanālā izveidotais debitora pasūtījums vai pārdošanas transakcija, kurā tiek pasūtīta šī prece, izraisa rindas līmeņa maksas sistemātisku pievienošanu pasūtījuma kopsummai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>At this time the charges will apply to any sales line that matches the configuration of the line-level auto charges within the legal entity, as there is no functionality to configure a line-level auto-charge to apply only to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pašlaik maksas tiek lietotas jebkurai pārdošanas rindai, kas atbilst rindas līmeņa automātisko maksu konfigurācijai konkrētajai juridiskajai personai, jo nav pieejama funkcionalitāte, kas sniedz iespēju konfigurēt rindas līmeņa automātiskās maksas lietošanu tikai noteiktam pārdošanas kanālam.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Manual header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Manuālu galvas līmeņa maksu piemērs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Use case scenario description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lietošanas gadījuma scenārija apraksts</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>A retailer is making an exception to typical processes by offering to provide a special home delivery of products to a customers who order products in the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mazumtirgotājs ievieš parastā procesa izņēmumu, piedāvājot nodrošināt īpašu preču piegādi uz mājām debitoriem, kas pasūta preces veikalā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The retailer and the customer have agreed that the customer will pay an additional $25 handling fee for this service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mazumtirgotājs un debitors ir vienojušies pa to, ka debitors par šo pakalpojumu maksās papildu apstrādes maksu 25 USD.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The order-taker needs to add this additional fee to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pasūtījuma pieņēmējam ir jāpievieno šī papildu maksa transakcijai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Because the fee is a blanket fee and not related to any single product on the order, a header charge will be utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tā kā šī ir vienota maksa un tā nav saistīta ne ar vienu atsevišķu pasūtījumā ietverto preci, tiek lietota galvas līmeņa maksa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Iestatīšana un konfigurēšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nodrošiniet, ka šī scenārija ietvaros izmantotais maksu kods ir pareizi konfigurēts, pārejot uz sadaļu <bpt id="p1">**</bpt>Debitori <ph id="ph1">\&gt;</ph> Maksu iestatīšana <ph id="ph2">\&gt;</ph> Maksas<ept id="p1">**</ept>, lai definētu scenārijam piemērotu maksu kodu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maksu piemērs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Ja maksa ir jāapstrādā kā ar piegādi saistīta maksa, lai varētu lietot ar piegādi saistītas atlaides vai akcijas, maksu koda opcijas <bpt id="p1">**</bpt>Piegādes maksa<ept id="p1">**</ept> vērtību iestatiet uz <bpt id="p2">**</bpt>Jā<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>If this charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja šo maksu ir arī atļauts sistemātiski atlīdzināt, veicot atgriešanas transakciju POS lietojumprogrammā, iestatiet opcijas <bpt id="p1">**</bpt>Atmaksājams<ept id="p1">**</ept> vērtību <bpt id="p2">**</bpt>Jā<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Karodziņš <bpt id="p1">**</bpt>Atmaksājams<ept id="p1">**</ept> tiek lietots tikai tad, ja ir iestatīta parametra <bpt id="p2">**</bpt>Izmantot papildu automātiskās maksas<ept id="p2">**</ept> vērtība <bpt id="p3">**</bpt>Jā<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nosūtiet maksas uz Retail Server/kanāla DB, lai tās varētu lietot POS sistēmā, izpildot darbu <bpt id="p1">**</bpt>1040 sadales grafiks<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>The <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 141).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">[</bpt>POS ekrāna izkārtojumā<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> ir jākonfigurē operācija <bpt id="p1">**</bpt>Pievienot galvas līmeņa maksu<ept id="p1">**</ept>, lai šo operāciju (141. operāciju) varētu izsaukt, izmantojot lietotajam POS sistēmā pieejamu pogu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ekrāna izkārtojuma izmaiņas ir jāizplata mazumtirdzniecības kanālā, kā arī izmantojot sadales grafika funkciju.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Sales processing of manual header charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Manuālo galvas līmeņa maksu apstrāde pārdošanas laikā</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai izpildītu scenāriju POS lietojumprogramma, POS lietotājs izveido pārdošanas transakciju kā parasti, pievienojot tai preces un jebkādas citas konfigurācijas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Prior to collecting payment, the user should execute the <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation, which will prompt the user to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pirms maksājuma iekasēšanas lietotājam ir izpilda operācija <bpt id="p1">**</bpt>Pievienot galvas līmeņa maksu<ept id="p1">**</ept>, kas prasa lietotājam atlasīt maksu kodu un ievadīt maksu vērtību.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Once the user completes the process, the charge will be added to the sales order as a header-level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad lietotājs ir pabeidzis šo procesu, maksa tiek pievienota pārdošanas pasūtījumam kā galvas līmenī maksa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>This process can be applied in the call center by using the existing <bpt id="p1">**</bpt>Charges<ept id="p1">**</ept> feature found on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab on the toolbar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šo procesu var lietot zvanu centrā, izmantojot esošo līdzekli <bpt id="p1">**</bpt>Maksas<ept id="p1">**</ept>, kas ir pieejams rīkjoslas cilnē <bpt id="p2">**</bpt>Pārdot<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page, the user can add a new charges line to the order header.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lapā <bpt id="p1">**</bpt>Uzturiet maksas<ept id="p1">**</ept> lietotājs var pievienot jaunu maksu rindu pasūtījuma galvai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Manual line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Manuālu rindas līmeņa maksu piemērs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lietošanas gadījuma scenārijs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>A customer has requested that 2 of the 5 items on their sales order be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Debitors ir pieprasījis, lai 2 no 5 pārdošanas pasūtījumā ietvertajiem krājumiem tiktu iesaiņoti kā dāvanas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>The retailer offers this optional service for a fee of $2.00 per item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mazumtirgotājs piedāvā šo papildu pakalpojumu, iekasējot maksu 2,00 USD apmērā par katru krājumu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The order-taker will need to add these fees to the specific items that need to be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pasūtījuma pieņēmējam ir jāpievieno šīs maksas konkrētajiem krājumiem, kas ir jāiesaiņo kā dāvanas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Iestatīšana un konfigurēšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nodrošiniet, ka šī scenārija ietvaros izmantotais maksu kods ir pareizi konfigurēts, pārejot uz sadaļu <bpt id="p1">**</bpt>Debitori <ph id="ph1">\&gt;</ph> Maksu iestatīšana <ph id="ph2">\&gt;</ph> Maksas<ept id="p1">**</ept>, lai definētu scenārijam piemērotu maksu kodu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set the <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja maksa ir jāapstrādā kā ar piegādi saistīta maksa, lai varētu lietot ar piegādi saistītas atlaides vai akcijas, iestatiet maksu koda opcijas <bpt id="p1">**</bpt>Piegādes maksa<ept id="p1">**</ept> vērtību <bpt id="p2">**</bpt>Jā<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>If the charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja maksu ir arī atļauts sistemātiski atlīdzināt, veicot atgriešanas transakciju POS lietojumprogrammā, iestatiet opcijas <bpt id="p1">**</bpt>Atmaksājams<ept id="p1">**</ept> vērtību <bpt id="p2">**</bpt>Jā<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Karodziņš <bpt id="p1">**</bpt>Atmaksājams<ept id="p1">**</ept> tiek lietots tikai tad, ja ir iestatīta parametra <bpt id="p2">**</bpt>Izmantot papildu automātiskās maksas<ept id="p2">**</ept> vērtība <bpt id="p3">**</bpt>Jā<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nosūtiet maksas uz Retail Server/kanāla DB, lai tās varētu lietot POS sistēmā, izpildot darbu <bpt id="p1">**</bpt>1040 sadales grafiks<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>The <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 140).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Operācija <bpt id="p1">**</bpt>Pievienot rindas līmeņa maksu<ept id="p1">**</ept> ir jākonfigurē <bpt id="p2">[</bpt>POS ekrāna izkārtojumā<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> tā, lai šo operāciju (140. operāciju) varētu izsaukt, izmantojot lietotajam POS sistēmā pieejamu pogu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ekrāna izkārtojuma izmaiņas ir jāizplata mazumtirdzniecības kanālā, kā arī izmantojot sadales grafika funkciju.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Sales processing of the manual line charge</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Manuālas rindas līmeņa maksas apstrāde pārdošanas laikā</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai izpildītu scenāriju POS lietojumprogramma, POS lietotājs izveido pārdošanas transakciju kā parasti, pievienojot tai preces un jebkādas citas konfigurācijas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Prior to collecting payment, the user should select the specific line where the charge will apply from the POS item list display and execute the <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pirms maksājuma iekasēšanas lietotājam POS krājumu saraksta ekrānā ir jāatlasa konkrētā rinda, kurai tiks lietota maksa, un jāizpilda operācija <bpt id="p1">**</bpt>Pievienotu rindas līmeņa maksu<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The user will be prompted to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lietotājam tiek prasīts atlasīt maksu kodu un ievadīt maksu vērtību.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Once the user completes the process, the charge will be linked to the line and added to the order total as a line level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad lietotājs ir pabeidzis šo procesu, maksa tiek saistīta ar attiecīgo rindu un pievienota pasūtījuma kopsummai kā rindas līmenī maksa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The user can repeat the process to add additional line charges to other items lines on the transaction if needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lietotājs var atkārtot šos procesu, lai pievienotu papildu maksas citām transakcijas krājumu rindām, ja tas ir nepieciešams.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The same process can be applied in the call center by using the "maintain charges" feature found under the <bpt id="p1">**</bpt>Financials<ept id="p1">**</ept> drop-down menu in the <bpt id="p2">**</bpt>Sales order lines<ept id="p2">**</ept> section on the <bpt id="p3">**</bpt>Sales order<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tādu pašu procesu var lietot zvanu centrā, izmantojot funkciju Uzturēt maksas, kas ir pieejama nolaižamajā izvēlnē <bpt id="p1">**</bpt>Finanšu dati<ept id="p1">**</ept> lapas <bpt id="p3">**</bpt>Pārdošanas pasūtījums<ept id="p3">**</ept> sadaļā <bpt id="p2">**</bpt>Pārdošanas pasūtījuma rindas<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>This will open the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page where the user can add a new line specific charge to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tādējādi tiek atvērta lapa <bpt id="p1">**</bpt>Uzturēt maksas<ept id="p1">**</ept>, kurā lietotājs var pievienot transakcijai jaunu rindai raksturīgu maksu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Additional features</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Papildu līdzekļi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Editing charges on a POS sales transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maksu rediģēšana POS pārdošanas transakcijas ietvaros</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>The <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation (142) should be added to the <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a user can view and edit or override any system-calculated or manually-created header or line-level charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">[</bpt>POS ekrāna izkārtojumam<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> ir jāpievieno operācija <bpt id="p1">**</bpt>Pārvaldīt maksas<ept id="p1">**</ept> (142), lai lietotājs varētu skatīt un rediģēt vai pārlabot jebkuras sistēmas aprēķinātās vai manuāli izveidotās galvas vai rindas līmeņa maksas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>If the operation is not added, users will not be able to adjust the value of the charges on the POS transaction, nor will they be able to view the details of the charges such as the type of charges code tied to the charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja operācija netiek pievienota, lietotāji nevar pielāgot POS transakcijas maksu vērtību, kā arī nevar skatīt detalizētu informāciju par maksām, piemēram, ar maksām saistīto maksu koda veidu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>On the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> page in POS, the user can view both header and line-level charges details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS sistēmas lapā <bpt id="p1">**</bpt>Pārvaldīt maksas<ept id="p1">**</ept> lietotājs var skatīt detalizētu informāciju gan par galvas līmeņa, gan par rindas līmeņa maksām.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The user can use the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> function available on this page to make changes to the amount charged to a specific charges line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lietotājs var izmantot šajā lapā pieejamo funkciju <bpt id="p1">**</bpt>Rediģēt<ept id="p1">**</ept>, lai mainītu iekasēto summu noteiktā maksu rindā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Once a charges line is overwritten manually, it will not be systematically recalculated unless the user initiates the <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad ir manuāli pārrakstīta maksu rinda, tā netiek sistemātiski pārrēķināta, ja vien lietotājs neuzsāk operāciju <bpt id="p1">**</bpt>Pārrēķināt maksas<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>If the <bpt id="p1">**</bpt>Charge override reason code<ept id="p1">**</ept> has been configured on the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> setup page, the user will be prompted to provide a reason code when charges have been modified in the POS application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja iestatīšanas lapā <bpt id="p2">**</bpt>Mazumtirdzniecības parametri<ept id="p2">**</ept> ir konfigurēta opcija <bpt id="p1">**</bpt>Maksu pārlabošanas iemesla kods<ept id="p1">**</ept>, pēc maksu izmainīšanas POS lietojumprogrammā lietotājam tiek prasīts norādīt iemesla kodu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>If reason codes have been captured for overwritten charges, a new report is also available to review and audit these overrides.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja tiek noteikti pārrakstītu maksu iemeslu kodi, tiek nodrošināts arī jauns pārskats, kurā var pārskatīt un auditēt šīs pārlabošanas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The report can be found in <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge override history<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārskats ir pieejams sadaļā <bpt id="p1">**</bpt>Mazumtirdzniecība <ph id="ph1">\&gt;</ph> Pieprasījumi un pārskati <ph id="ph2">\&gt;</ph> Maksu pārlabošanas vēsture<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Refunding charges on a POS return transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maksu atmaksāšana POS atgriešanas transakcijas ietvaros</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>If the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>, the existing retail parameter for <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> is no longer applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja ir iestatīta parametra <bpt id="p1">**</bpt>Izmantot papildu automātiskās maksas<ept id="p1">**</ept> vērtība <bpt id="p2">**</bpt>Jā<ept id="p2">**</ept>, vairs netiek lietota esošā mazumtirdzniecības parametra <bpt id="p3">**</bpt>Atmaksāt piegādes maksas<ept id="p3">**</ept> vērtība.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>To indicate which charges should be systematically refunded to a customer when using advanced auto-charges, ensure the related charges code has been configured as <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai norādītu, kuras maksas ir sistemātiski jāatmaksā debitoram, izmantojot papildu automātiskās maksas, pārliecinieties, vai saistītais maksu kods ir konfigurēts kā <bpt id="p1">**</bpt>Atmaksājams<ept id="p1">**</ept> iestatīšanas lapā <bpt id="p2">**</bpt>Maksu kods<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Make sure that the settings have been synchronized to your Retail channel databases through distribution schedule processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārliecinieties, vai iestatījumi ir sinhronizēti ar jūsu mazumtirdzniecības kanāla datu bāzēs, izmantojot sadales grafika apstrādi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Refunding charges on a return order transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maksu atmaksāšana atgriešanas pasūtījuma transakcijas ietvaros</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Charges are not systematically refunded to <bpt id="p1">**</bpt>Return orders<ept id="p1">**</ept> created in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maksas netiek sistemātiski atmaksātas programmā Retail izveidoto <bpt id="p1">**</bpt>atgriešanas pasūtījumu<ept id="p1">**</ept> ietvaros.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Users are required to select the <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> option when creating the <bpt id="p2">**</bpt>Return order<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad tiek izveidots <bpt id="p2">**</bpt>atgriešanas pasūtījums<ept id="p2">**</ept>, lietotājiem ir jāatlasa opcija <bpt id="p1">**</bpt>Kopēt maksas<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is not selected, charges from the original sales transaction will not be automatically refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja nav atlasīta opcija <bpt id="p1">**</bpt>Kopēt maksas<ept id="p1">**</ept>, netiek automātiski atgrieztas sākotnējā pārdošanas transakcijā ietvertās maksas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is selected, all charges will be copied to the return order and the user can manually edit or remove any charges they do not want to have refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja ir atlasīta opcija <bpt id="p1">**</bpt>Kopēt maksas<ept id="p1">**</ept>, visas maksas tiek kopētas uz atgriešanas pasūtījumu un lietotājs var manuāli rediģēt vai noņemt jebkuras maksas, kuras viņš nevēlas atmaksāt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The call center return order process currently does not acknowledge the <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zvanu centra atgriešanas pasūtījumu apstrādes procesā pašlaik netiek ņemts vērā karodziņš <bpt id="p1">**</bpt>Atmaksājams<ept id="p1">**</ept> iestatījumu sadaļā <bpt id="p2">**</bpt>Maksu kods<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Configuring POS receipts to show charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS kvīšu konfigurēšana maksu parādīšanai</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>The following receipt elements have been added to the receipt line and footer to support the advanced auto-charges functionality.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Lai nodrošinātu papildu automātisko maksu funkcionalitātes atbalstu, kvīts rindai un kājenei ir pievienoti tālāk norādītie kvīts elementi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source><bpt id="p1">**</bpt>Line Shipping Charges<ept id="p1">**</ept> – This line-level element can be used to recap specific charges codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Rindas piegādes maksas<ept id="p1">**</ept> — šo rindas līmeņa elementu var izmantot, lai iegūtu kopsavilkumu par noteiktiem maksu kodiem, kas ir lietoti pārdošanas rindai.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Only charges codes that have been flagged as <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> charges on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page will be displayed here.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Šeit tiek rādīti tikai tie maksu kodi, kas ir atzīmēti ar maksu veida karodziņu <bpt id="p1">**</bpt>Piegāde<ept id="p1">**</ept> lapā <bpt id="p2">**</bpt>Maksu kods<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source><bpt id="p1">**</bpt>Line Other Charges<ept id="p1">**</ept> – This line-level element can be used to recap any non-shipping specific charge codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Citas rindas maksas<ept id="p1">**</ept> — šo rindas līmeņa elementu var izmantot, lai iegūtu kopsavilkumu par visu ar piegādi nesaistītu maksu kodiem, kas ir lietoti šai pārdošanas rindai.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>These are charges codes where the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page has not been enabled.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Tie ir maksu kodi, kas nav atzīmēti ar karodziņu <bpt id="p1">**</bpt>Piegāde<ept id="p1">**</ept> lapā<bpt id="p2">**</bpt>Maksu kods<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><bpt id="p1">**</bpt>Order Shipping Charges Details<ept id="p1">**</ept> – This footer-level element displays the descriptions of the charge codes applied to the order that have been flagged as <bpt id="p2">**</bpt>Shipping<ept id="p2">**</ept> charges on the <bpt id="p3">**</bpt>Charges code<ept id="p3">**</ept> setup page.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Detalizēta informācija par pasūtījuma piegādes maksām<ept id="p1">**</ept> — šis kājenes līmeņa elements rāda to pasūtījumam lietoto maksu kodu aprakstus, kas iestatīšanas lapā <bpt id="p3">**</bpt>Maksu kods<ept id="p3">**</ept> ir atzīmēti ar maksu veida karodziņu <bpt id="p2">**</bpt>Piegāde<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source><bpt id="p1">**</bpt>Order Shipping Charges<ept id="p1">**</ept> – This footer-level element shows the dollar value of the shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Pasūtījuma piegādes maksas<ept id="p1">**</ept> — šis kājenes līmeņa elements rāda ar piegādi saistīto maksu vērtību dolāros.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">**</bpt>Order Other Charges Details<ept id="p1">**</ept> – This footer-level element displays the description of the charges codes applied to the order that have not been flagged as shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Detalizēta informācija par citām pasūtījuma maksām<ept id="p1">**</ept> — šis kājenes līmeņa elements rāda to pasūtījumam lietoto maksu kodu aprakstus, kas nav atzīmēti kā ar piegādi saistītas maksas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source><bpt id="p1">**</bpt>Order Other Charges<ept id="p1">**</ept> – This footer-level element displays the dollar value of the other charges that are not shipping-related.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Citas pasūtījuma maksas<ept id="p1">**</ept> — šis kājenes līmeņa elements rāda ar citu, ar piegādi nesaistīto maksu vērtību dolāros.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>It is recommended that the organization also add free text fields to the receipt footer, in order to define the areas where charges will be recapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Organizācijai ir ieteicams pievienot kvīts kājenei arī brīvā teksta laukus, lai definētu apgabalus, kur tiks veidoti kopsavilkumi par maksām.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Preventing charges from being calculated until the POS order is completed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maksu aprēķināšanas liegšana līdz POS pasūtījuma pabeigšanai</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Some organizations may prefer to wait until the user has finished adding all of the sales lines to the POS transaction before calculating charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dažas organizācijas var izvēlēties pirms maksu parēķināšanas uzgaidīt, līdz lietotājs ir pabeidzis visu pārdošanas rindu pievienošanu POS transakcijai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>To prevent calculation of charges as items are added to the POS transaction, turn on the <bpt id="p1">**</bpt>Manual charge calculation<ept id="p1">**</ept> parameter in the <bpt id="p2">**</bpt>Functionality profile<ept id="p2">**</ept> used by the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai nepieļautu maksu aprēķināšanu, kamēr POS transakcijai tiek pievienoti krājumi, iespējojiet parametru <bpt id="p1">**</bpt>Manuāls maksas aprēķins<ept id="p1">**</ept> veikalam izmantotajā <bpt id="p2">**</bpt>funkcionalitātes profilā<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Enabling this parameter will require the POS user to use the <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation when they have completed adding the products to the POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja ir iespējots šis parametrs, kad POS lietotājs ir pabeidzis preču pievienošanu POS transakcijai, viņam ir jāizmanto operācija <bpt id="p1">**</bpt>Aprēķināt kopsummas<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>The <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation will then trigger the calculation of any auto charges for the order header or lines as applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pēc tam operācija <bpt id="p1">**</bpt>Aprēķināt kopsummas<ept id="p1">**</ept> aktivizē jebkuru pasūtījuma galvas vai rindas līmeņa automātisko maksu aprēķinu, ja tas ir attiecināms.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Charges override reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maksu ignorēšanas pārskati</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>If users manually override the calculated charges or add a manual charge to the transaction, this data will available for auditing in the <bpt id="p1">**</bpt>Charge Override History<ept id="p1">**</ept> report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja lietotāji manuāli ignorē aprēķinātās maksas vai pievieno transakcijai manuālas maksas, šie dati būs pieejami auditēšanai pārskatā <bpt id="p1">**</bpt>Maksu ignorēšanas vēsture<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The report can be accessed from <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge Override History<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārskats ir pieejams sadaļā <bpt id="p1">**</bpt>Mazumtirdzniecība <ph id="ph1">\&gt;</ph> Pieprasījumi un pārskati <ph id="ph2">\&gt;</ph> Maksu ignorēšanas vēsture<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>It is important to note that the data needed for this report is imported from the channel database into HQ through the "P" distribution schedule jobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ir svarīgi atzīmēt, ka šim pārskatam nepieciešamie dati tiek importēti no kanāla datu bāzes uz HQ, izmantojot "P" sadales grafika darbus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Therefore, information about overrides just performed in the POS may not be immediately available on this report until this job has uploaded the store transaction data into HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tāpēc informācija par POS veiktajām ignorēšanas darbībām tūlītēji var nebūt pieejama šajā pārskatā, bet tikai tad, kad ar šo darbu HQ ir augšupielādēti saglabātie darbību dati.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>