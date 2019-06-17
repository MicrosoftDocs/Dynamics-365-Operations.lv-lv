<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="Notifications-POS.md" target-language="lv-LV">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>Notifications-POS.74d2b9.6c813cfea9b570e8dfd5dbe7f3ca1f4ba8594420.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>6c813cfea9b570e8dfd5dbe7f3ca1f4ba8594420</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\Notifications-POS.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Show order notifications in the point of sale (POS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pasūtījumu paziņojumu parādīšana pārdošanas punktā (POS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to enable order notifications in the point of sale and the notification framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā tēmā ir aprakstīts, kā pārdošanas punktā iespējot pasūtījumu paziņojumu rādīšanu, un aprakstīta paziņojumu struktūra</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Show order notifications in the point of sale (POS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pasūtījumu paziņojumu parādīšana pārdošanas punktā (POS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In the modern retail environment, store associates are assigned various tasks, such as helping customers, entering transactions, doing stock counts, and receiving orders in the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modernajā mazumtirdzniecības vidē veikala darbiniekiem tiek piešķirti dažādi uzdevumi, piemēram, palīdzēšana klientiem, transakciju ievadīšana, krājumu uzskaites veikšana un pasūtījumu pieņemšana veikalā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The point of sale (POS) client provides a single application where associates can perform all these tasks and many others.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārdošanas punkta (POS) klients nodrošina vienu programmu, kur veikala darbinieki vat izpildīt visus šos un vēl daudzus citus uzdevumus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Because various tasks must be performed during the day, associates might have to be notified when something requires their attention.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tā kā dienas laikā ir jāizpilda dažādi uzdevumi, veikala darbinieki, iespējams, ir jāinformē par lietām, kurām šiem darbiniekiem būtu jāpievērš uzmanība.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The notification framework in the POS helps by letting retailers configure role-based notifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Paziņojumu struktūra programmā POS atrisina šo problēmu, ļaujot mazumtirgotājiem konfigurēt paziņojumus atkarībā no lomām.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>In Microsoft Dynamics 365 for Retail with application update 5, these notifications can be configured only for POS operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Programmā Microsoft Dynamics 365 for Retailar 5. lietojumprogrammas atjauninājumu šos paziņojumus var konfigurēt tikai POS operācijām.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Currently, the system can show notifications only for order fulfillment operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pašlaik sistēma var parādīt paziņojumus tikai par pasūtījuma izpildes operācijām.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>However, because the framework is designed to be extensible, developers will eventually be able to write a notification handler for any operation and show the notifications for that operation in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tomēr struktūra ir veidota paplašināma, tādēļ izstrādātāji galu galā varēs rakstīt paziņojumu apdarinātāju jebkādai operācijai un parādīt paziņojumus par šīm operācijām POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Enable notifications for order fulfillment operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Paziņojumu iespējošana pasūtījumu izpildes operācijām</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To enable notifications for order fulfillment operations, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai iespējotu paziņojumus par pasūtījumu izpildes operācijām, izpildiet tālāk aprakstītās darbības.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS setup<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>Operations<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pārejiet uz sadaļu <bpt id="p1">**</bpt>Mazumtirdzniecība<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Kanāla iestatīšana<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS iestatīšana<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>Operācijas<ept id="p5">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Search for the <bpt id="p1">**</bpt>Order fulfillment<ept id="p1">**</ept> operation, and select the <bpt id="p2">**</bpt>Enable notifications<ept id="p2">**</ept> check box for it to specify that the notification framework should listen to the handler for this operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Meklējiet operāciju <bpt id="p1">**</bpt>Pasūtījuma izpilde<ept id="p1">**</ept> un atzīmējiet tās izvēles rūtiņu <bpt id="p2">**</bpt>Iespējot paziņojumus<ept id="p2">**</ept>, lai norādītu, ka paziņojumu struktūrai jāņem vērā šīs operācijas apdarinātājs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If the handler is implemented, notifications for this operation will then be shown in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja apdarinātājs ir ieviests, šīs operācijas paziņojumi tiks rādīti POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Employees<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Workers<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph>, under Retail tab, open the POS permissions associated with the worker.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dodieties uz <bpt id="p1">**</bpt>Mazumtirdzniecība<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Darbinieki<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Nodarbinātie<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> cilnē Mazumtirdzniecība atveriet POS atļaujas, kas saistītas ar nodarbināto.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Expand the <bpt id="p1">**</bpt>Notifications<ept id="p1">**</ept> FastTab, add the <bpt id="p2">**</bpt>Order fulfillment<ept id="p2">**</ept> operation, and set the <bpt id="p3">**</bpt>Display order<ept id="p3">**</ept> field to <bpt id="p4">**</bpt>1<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Izvērsiet kopsavilkuma cilni <bpt id="p1">**</bpt>Paziņojumi<ept id="p1">**</ept>, pievienojiet operāciju <bpt id="p2">**</bpt>Pasūtījuma izpilde<ept id="p2">**</ept> un iestatiet laukam <bpt id="p3">**</bpt>Rādīt pasūtījumu<ept id="p3">**</ept> vērtību <bpt id="p4">**</bpt>1<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>If more than one notification is configured, this field is used to arrange the notifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja ir konfigurēti vairāki paziņojumi, šis lauks tiek izmantots, lai kārtotu paziņojumus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Notifications that have a lower <bpt id="p1">**</bpt>Display order<ept id="p1">**</ept> value appear above notifications that have a higher value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Paziņojumi, kuriem ir zemākā vērtība <bpt id="p1">**</bpt>Rādīt pasūtījumu<ept id="p1">**</ept> tiek rādīti pirms paziņojumiem, kam ir lielāka vērtība.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Notifications that have a <bpt id="p1">**</bpt>Display order<ept id="p1">**</ept> value of <bpt id="p2">**</bpt>1<ept id="p2">**</ept> are at the top.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Paziņojumi, kam <bpt id="p1">**</bpt>Rādīt pasūtījumu<ept id="p1">**</ept> vērtība ir <bpt id="p2">**</bpt>1<ept id="p2">**</ept>, tiek rādīti augšā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Notifications are shown only for operations that are added on the <bpt id="p1">**</bpt>Notifications<ept id="p1">**</ept> FastTab, and you can add operations there only if the <bpt id="p2">**</bpt>Enable notifications<ept id="p2">**</ept> check box for those operations has been selected on the <bpt id="p3">**</bpt>POS operations<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Paziņojumi tiek rādīti tikai operācijām, kas tiek pievienotas kopsavilkuma cilnē <bpt id="p1">**</bpt>Paziņojumi<ept id="p1">**</ept>, un operācijas var pievienot tikai tad, ja šīm operācijām ir atzīmēta izvēles rūtiņa <bpt id="p2">**</bpt>Iespējot paziņojumus<ept id="p2">**</ept> lapā <bpt id="p3">**</bpt>POS operācijas<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Additionally, notifications for an operation are shown to workers only if the operation is added to the POS permissions for those workers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Turklāt paziņojumi par šo operāciju tiek rādīti darbiniekiem tikai tad, ja operācija tiek pievienota šo darbinieku POS atļaujām.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Notifications can be overridden at the user level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Paziņojumus var ignorēt lietotāja līmenī.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Open the worker's record, select <bpt id="p1">**</bpt>POS permissions<ept id="p1">**</ept>, and then edit the user's notification subscription.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Atveriet darbinieka ierakstu, atlasiet <bpt id="p1">**</bpt>POS atļaujas<ept id="p1">**</ept> un pēc tam rediģējiet lietotāja paziņojumu abonementu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS setup<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS profiles<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>Functionality profiles<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Doties uz <bpt id="p1">**</bpt>Mazumtirdzniecība<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Kanāla iestatīšana<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS iestatīšana<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS profili<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>Funkcionalitātes profili<ept id="p5">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In the <bpt id="p1">**</bpt>Notification interval<ept id="p1">**</ept> field, specify how often notifications should be pulled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Laukā <bpt id="p1">**</bpt>Paziņošanas intervāls<ept id="p1">**</ept> norādiet, cik bieži paziņojumi jārāda.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>For some notifications, the POS must make real-time calls to the back-office application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dažiem paziņojumiem sistēmai POS ir jāveic reāllaika izsaukums grāmatvedības programmai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>These calls consume the compute capacity of your back-office application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šie zvani patērē grāmatvedības programmai nepieciešamo datora noslodzi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Therefore, when you set the notification interval, you should consider both your business requirements and the impact of real-time calls to the back-office application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tādēļ, iestatot paziņošanas intervālu, jāņem vērā gan uzņēmuma prasības, gan reāllaika izsaukumu grāmatvedības programmai ietekme.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>A value of <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero) turns off notifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vērtība <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (nulle) izslēdz paziņojumus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dodieties uz <bpt id="p1">**</bpt>Mazumtirdzniecība<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Mazumtirdzniecības IT<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Sadales grafiks<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Select the <bpt id="p1">**</bpt>1060<ept id="p1">**</ept> (<bpt id="p2">**</bpt>Staff<ept id="p2">**</ept>) schedule to synchronize notification subscription settings, and then select <bpt id="p3">**</bpt>Run now<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Atlasiet grafiku <bpt id="p1">**</bpt>1060<ept id="p1">**</ept> (<bpt id="p2">**</bpt>Personāls<ept id="p2">**</ept>), lai sinhronizētu paziņojumu abonementa iestatījumus, un pēc tam atlasiet <bpt id="p3">**</bpt>Izpildīt tūlīt<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Next, select the <bpt id="p1">**</bpt>1070<ept id="p1">**</ept> (<bpt id="p2">**</bpt>Channel configuration<ept id="p2">**</ept>) schedule to synchronize the permission interval, and then select <bpt id="p3">**</bpt>Run now<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tālāk sinhronizējiet atļaujas intervālu, atlasot <bpt id="p1">**</bpt>1070<ept id="p1">**</ept> (<bpt id="p2">**</bpt>Kanāla konfigurācija<ept id="p2">**</ept>), un pēc tam atlasiet <bpt id="p3">**</bpt>Izpildīt tūlīt<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>View notifications in the POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Paziņojumu skatīšana programmā POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>After you complete the preceding steps, the workers will be able to view the notifications in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pēc visu darbību pabeigšanas darbinieki varēs skatīt paziņojumus programmā POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>To view notifications, press the notification icon in the top right corner of the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai skatītu paziņojumus, POS augšējā labajā stūrī nospiediet uz paziņojuma ikonas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>A notification center appears and shows notifications for the order fulfillment operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tiek parādīts paziņojumu centrs un paziņojumi par pasūtījuma izpildes operāciju.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The notification center should show the following groups in the order fulfillment operation:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Paziņojumu centrā rāda tālāk norādītās grupas, kas ietilpst pasūtījuma izpildes operācijā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>Store pickup<ept id="p1">**</ept> – This group shows the count of orders that have a delivery mode of <bpt id="p2">**</bpt>Pickup<ept id="p2">**</ept>, and that are scheduled for pickup from the current store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Izdot veikalā<ept id="p1">**</ept> — ar šo grupu tiek rādīts tādu pasūtījumu skaits, kuru piegādes metode ir <bpt id="p2">**</bpt>Izdošana<ept id="p2">**</ept> un kuriem izdošana ir plānota no pašreizējā veikala.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>You can press the number on the group to open the <bpt id="p1">**</bpt>Order fulfillment<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varat nospiest uz grupas numura, lai atvērtu lapu <bpt id="p1">**</bpt>Pasūtījuma izpilde<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>In this case, the page will be filtered so that it shows only the active orders that are set up for pickup from the current store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā gadījumā lapa tiek filtrēta tā, lai rādītu tikai aktīvos pasūtījumus, kas tika iestatīti izdošanai no pašreizējā veikala.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">**</bpt>Ship from store<ept id="p1">**</ept> – This group shows the count of orders that have the delivery mode of <bpt id="p2">**</bpt>Shipping<ept id="p2">**</ept>, and that are scheduled for shipment from the current store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Nosūtīt no veikala<ept id="p1">**</ept> — ar šo grupu tiek rādīts tādu pasūtījumu skaits, kuru piegādes metode ir <bpt id="p2">**</bpt>Nosūtīšana<ept id="p2">**</ept> un kuriem nosūtīšana ir plānota no pašreizējā veikala.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>You can press the number on the group to open the <bpt id="p1">**</bpt>Order fulfillment<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varat nospiest uz grupas numura, lai atvērtu lapu <bpt id="p1">**</bpt>Pasūtījuma izpilde<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>In this case, the page will be filtered so that it shows only the active orders that are set up for shipment from the current store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā gadījumā lapa tiek filtrēta tā, lai rādītu tikai aktīvos pasūtījumus, kas tika iestatīti nosūtīšanai no pašreizējā veikala.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>When new orders are assigned to the store for fulfillment, the notification icon changes to indicate that there are new notifications, and the count for the appropriate groups is updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kad veikalam izpildei tiek piešķirti jauni pasūtījumi, paziņojumu ikona mainās, lai rādītu jaunos paziņojumus, un tiek atjaunināts atbilstošo grupu skaits.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Even though the groups are refreshed at regular intervals however, POS users can manually refresh the groups at any time by selecting the <bpt id="p1">**</bpt>Refresh<ept id="p1">**</ept> button next to the group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kaut gan grupas tiek atsvaidzinātas regulāri, POS lietotāji var manuāli atsvaidzināt grupas jebkurā laikā, atlasot pogu <bpt id="p1">**</bpt>Atsvaidzināt<ept id="p1">**</ept> blakus grupas nosaukumam.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Lastly, if a group has a new item, that the current worker hasn't viewed, then the group shows a burst symbol to indicate new content.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visbeidzot, ja grupai ir jauns krājums, ko pašreizējais darbinieks nav skatījis, grupai parāda sprādziena simbols, kas norāda par jaunu saturu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Enable live content on POS buttons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reāllaika satura iespējošana uz POS pogas</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>POS buttons can now show a count to help workers easily determine which tasks require their immediate attention.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tagad uz POS pogas var parādīt skaitu, lai darbinieki varētu viegli noteikt, kādiem uzdevumiem nekavējoties jāpievērš uzmanība.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>To show this number on a POS button, you must complete the notification setup that is described earlier in this topic (that is, you must enable notifications for an operation, set up a notification interval, and update the POS permission group for the worker).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai šo skaitu parādītu uz POS pogas, jāveic paziņojumu iestatīšana, kā aprakstīts iepriekš šajā tēmā (t.i., jāiespējo paziņojumi operācijai, jāiestata paziņošanas intervāls un jāatjaunina POS darbinieka atļauju grupa).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Additionally, you must open the button grid designer, view the button's properties, and select the <bpt id="p1">**</bpt>Enable live content<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Turklāt ir jāatver pogas režģa veidotājs, jāapskata pogas rekvizīti un jāatzīmē izvēles rūtiņa <bpt id="p1">**</bpt>Iespējot reāllaika saturu<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>In the <bpt id="p1">**</bpt>Content alignment<ept id="p1">**</ept> field, you can select whether the count appears in the upper-right corner of the button (<bpt id="p2">**</bpt>Top right<ept id="p2">**</ept>) or in the center (<bpt id="p3">**</bpt>Center<ept id="p3">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Laukā <bpt id="p1">**</bpt>Satura pielāgošana<ept id="p1">**</ept> varat atlasīt, vai skaits tiek rādīts pogas augšējā labajā stūrī (<bpt id="p2">**</bpt>Augšējā labajā stūrī<ept id="p2">**</ept>) vai vidū (<bpt id="p3">**</bpt>Vidū<ept id="p3">**</ept>).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The live content can be enabled for operations only if the <bpt id="p1">**</bpt>Enable notifications<ept id="p1">**</ept> check box has been selected for them on the <bpt id="p2">**</bpt>POS operations<ept id="p2">**</ept> page, as described earlier in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reāllaika saturu operācijām var iespējot tikai tad, ja tām ir atzīmēta izvēles rūtiņa <bpt id="p1">**</bpt>Iespējot paziņojumus<ept id="p1">**</ept> lapā <bpt id="p2">**</bpt>POS operācijas<ept id="p2">**</ept>, kā aprakstīts iepriekš šajā tēmā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The following illustration shows the live content settings in the button grid designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tālāk attēlā ir parādīts reāllaika satura iestatījumi pogas režģa veidotājā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source><bpt id="p1">![</bpt>Live content settings in the button grid designer<ept id="p1">]</ept><bpt id="p2">(./media/ButtonGridDesigner.png "</bpt>Live content settings in the button grid designer<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>Reāllaika satura iestatījumi pogas režģa veidotājā<ept id="p1">]</ept><bpt id="p2">(./media/ButtonGridDesigner.png "</bpt>Reāllaika satura iestatījumi pogas režģa veidotājā<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To show the notification count on a button, you need to ensure that the correct screen layout is being updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai parādītu paziņojumu skaitu uz pogas, ir jāpārliecinās, ka tiek atjaunināts atbilstošais ekrāna izkārtojums.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>To determine the screen layout that is being used by the POS, select the <bpt id="p1">**</bpt>Settings<ept id="p1">**</ept> icon in upper-right corner and note the <bpt id="p2">**</bpt>Screen layout ID<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Layout resolution<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai noteiktu ekrāna izkārtojumu, ko izmanto POS, augšējā labajā stūrī atlasiet ikonu <bpt id="p1">**</bpt>Iestatījumi<ept id="p1">**</ept> un piefiksējiet rādītājus <bpt id="p2">**</bpt>Ekrāna izkārtojuma ID<ept id="p2">**</ept> un <bpt id="p3">**</bpt>Izkārtojuma izšķirtspēja<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Now using Edge browser, go to the <bpt id="p1">**</bpt>Screen layout<ept id="p1">**</ept> page in Dynamics 365 for Finance and Operations, find the <bpt id="p2">**</bpt>Screen layout ID<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Layout resolution<ept id="p3">**</ept> identified above and select the <bpt id="p4">**</bpt>Enable live content<ept id="p4">**</ept> check box.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Izmantojot pārlūkprogrammu Edge, dodieties uz lapu <bpt id="p1">**</bpt>Ekrāna izkārtojums<ept id="p1">**</ept> pakalpojumā Dynamics 365 for Finance and Operations, atrodiet iepriekš noteiktos rādītājus <bpt id="p2">**</bpt>Ekrāna izkārtojuma ID<ept id="p2">**</ept> un <bpt id="p3">**</bpt>Izkārtojuma izšķirtspēja<ept id="p3">**</ept> un atzīmējiet izvēles rūtiņu <bpt id="p4">**</bpt>Iespējot tiešsaistes saturu<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> Distribution schedule<ept id="p1">**</ept> and run the 1090 (Registers) job to synchronize layout changes.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Dodieties uz <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Mazumtirdzniecības IT <ph id="ph2">\&gt;</ph> Sadales grafiks<ept id="p1">**</ept> un palaidiet darbu 1090 (Reģistri), lai sinhronizētu izkārtojuma izmaiņas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">![</bpt>Find the screen layout used by POS<ept id="p1">]</ept><bpt id="p2">(./media/Choose_screen_layout.png "</bpt>Find the screen layout <ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>Atrast ekrāna izkārtojumu, ko izmanto POS<ept id="p1">]</ept><bpt id="p2">(./media/Choose_screen_layout.png "</bpt>Atrast ekrāna izkārtojumu <ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The following illustration shows the effect of selecting <bpt id="p1">**</bpt>Top right<ept id="p1">**</ept> versus <bpt id="p2">**</bpt>Center<ept id="p2">**</ept> in the <bpt id="p3">**</bpt>Content alignment<ept id="p3">**</ept> field for buttons of various sizes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tālāk attēlā ir parādīts rezultāts, atlasot dažāda izmēra pogu <bpt id="p1">**</bpt>Augšējā labajā stūrī<ept id="p1">**</ept> vai <bpt id="p2">**</bpt>Vidū<ept id="p2">**</ept> laukā <bpt id="p3">**</bpt>Satura pielāgošana<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">![</bpt>Live content on POS buttons<ept id="p1">]</ept><bpt id="p2">(./media/ButtonsWithLiveContent.png "</bpt>Live content on POS buttons<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>Reāllaika saturs uz POS pogas<ept id="p1">]</ept><bpt id="p2">(./media/ButtonsWithLiveContent.png "</bpt>Reāllaika saturs uz POS pogas<ept id="p2">")</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>