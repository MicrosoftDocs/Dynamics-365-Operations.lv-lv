---
title: "Mazumtirdzniecības perifērijas pārskats"
description: "Šajā tēmā ir paskaidrots, koncepcijas, kas saistītas ar mazumtirdzniecības perifērijas ierīces. Tas ir aprakstīti dažādi veidi, kā ka perifērijas ierīces var savienot ar pārdošanu (POS) un komponenti, kas ir atbildīga par savienojuma izveidi ar POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 268444
ms.assetid: 2ea93e43-8019-49a0-a7f8-325565ebc52d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 79a43c35691f16d773b88faad63c4ab79cb93f1f
ms.openlocfilehash: c6fb3922ba2c4b15f1043d0bcbac40ff2da9a469
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripherals-overview"></a>Mazumtirdzniecības perifērijas pārskats

Šajā tēmā ir paskaidrots, koncepcijas, kas saistītas ar mazumtirdzniecības perifērijas ierīces. Tas ir aprakstīti dažādi veidi, kā ka perifērijas ierīces var savienot ar pārdošanu (POS) un komponenti, kas ir atbildīga par savienojuma izveidi ar POS.

<a name="concepts"></a>Koncepcijas
--------

### <a name="pos-registers"></a>POS kases sistēmas

Navigācija: Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**reģistrē**. Sale (POS) reģistrs ir vienība, ko izmanto, lai noteiktu konkrētu gadījumu POS raksturlielumus. Šie raksturlielumi ietver aparatūras profilu vai uzstādīšanas mazumtirdzniecības perifērijas ierīcēm, kas tiks izmantota lietotājam, kurš parakstās reģistrā reģistra, veikalā, ka reģistrā tiek kartēts uz un vizuālo pieredzi.

### <a name="devices"></a>Ierīces

Navigācija: Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**ierīces**. Ierīce ir elements, kas pārstāv fizisku instanci tādai ierīcei, kura ir kartēta uz POS reģistru. Kad ierīce ir izveidota, tā ir kartēta uz POS reģistrā. Ierīces elements seko līdzi informācijai par laiku, kad POS reģistrs tiek aktivizēts, par izmantotā klienta tipu, kā arī par programmu pakotni, kas ir izvietota konkrētā ierīcē. Ierīces, var kartēt uz šādas lietojumprogrammas: mazumtirdzniecības mūsdienu POS, mazumtirdzniecības mākonis POS, mazumtirdzniecības mūsdienu POS-Windows Phone, mazumtirdzniecības mūsdienu POS-Android un mazumtirdzniecības mūsdienu POS-iOS.

### <a name="retail-modern-pos"></a>Retail Modern POS

Mūsdienu POS ir POS programma Microsoft Windows. To var izvietot Windows 10 operētājsistēmās (OSs).

### <a name="cloud-pos"></a>Cloud POS

Mākonis POS ir mūsdienu POS programma, kas var piekļūt web pārlūkprogrammā bāzētu versija.

### <a name="modern-pos-for-ios"></a>Mūsdienu POS iOS

IOS versija, kuras pamatā ir mūsdienu POS programma, kuru var izvietot iOS ierīcēs ir mūsdienu POS iOS.

### <a name="modern-pos-for-android"></a>Mūsdienu POS Android

Mūsdienu POS Android ir Android versija, kuras pamatā ir mūsdienu POS programma, kuru var izvietot uz Android ierīcēm.

### <a name="pos-peripherals"></a>POS perifērijas ierīces

POS perifērijas ierīces ir ierīces, kas viennozīmīgi atbalstīja POS funkcijām. Parasti šīm perifērijas ierīcēm tiek iedalīti konkrētās klasēs. Plašāku informāciju par šīm nodarbībām, skatiet šīs tēmas sadaļā "Ierīces klases".

### <a name="hardware-station"></a>Aparatūras stacija

Navigācija: Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**kanālus**&gt;**mazumtirdzniecības veikali**&gt;**visiem mazumtirdzniecības veikali**. Atlasiet veikalu un pēc tam noklikšķiniet uz kopsavilkuma cilnes **Aparatūras stacijas**. **Aparatūras stacijas** iestatījums ir kanāls līmeņa iestatījums, kas tiek izmantota, lai noteiktu gadījumus, kur tiks izvietoti mazumtirdzniecības perifērijas loģika. Kanāla līmenī, šis iestatījums tiek izmantots, lai noteiktu aparatūras stacijas raksturojums. To izmanto arī, lai sarakstā aparatūras stacijas, kas pieejamas mūsdienu POS instances attiecīgajā veikalā. Aparatūras stacija ir iebūvēts mūsdienu POS programma Windows. Aparatūras stacijas var arī izvietot patstāvīgi kā savrupu programmu Microsoft Internet Information Services (IIS). Šajā gadījumā tas var piekļūt, izmantojot tīklu.

### <a name="hardware-profile"></a>Aparatūras profils

Navigācija: Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**POS profili**&gt;**Hardware Profili**. Aparatūras profils ir ierīču sarakstu, kuras ir konfigurētas POS reģistrā vai aparatūras stacija. Tieši uz POS reģistrā vai aparatūras stacijas var kartēt aparatūras profilu.

## <a name="devices-classes"></a>Ierīču klasēm
POS perifērijas ierīces parasti tiek iedalīti kategorijās. Šajā sadaļā aprakstītas un sniedz pārskatu par ierīcēm, kas nodrošina mūsdienu POS.

### <a name="printer"></a>Printeris

Printeru ietver tradicionālo POS saņemšanas gan pilnas lappuses printeri. Printeris tiek atbalstīti, izmantojot objektu saistīšanu un iegulšanu mazumtirdzniecības POS (OPOS) un Microsoft Windows draivera saskarnes. Līdz pat divi printeri var tikt lietoti vienlaikus. Šī iespēja nodrošina scenārijus, kur cash-and-carry klienta apliecinājumi tiek drukāti saņemšana printeri, tā kā klientu pasūtījumiem, kas pārvadā vairāk informācijas, tiek drukāts pilnlappuses printeri. Saņemšana printeri var tieši savienots ar datoru, izmantojot USB, savienots ar tīklu, izmantojot Ethernet vai savienoti, izmantojot Bluetooth.

### <a name="scanner"></a>Skeneris

Līdz pat divu svītru kodu skeneri var tikt lietoti vienlaikus. Šī iespēja nodrošina scenārijus, ja skenerim, kas ir mobilāki ir vajadzīga, lai skenēt lielu vai smago elementu, tā kā fiksēto iegults skenera tiek izmantots lielākajā daļā standarta izmēra objektus, lai paātrinātu paņemšanas laiki. Caur OPOS, Universal Windows platformas (UWP) vai tastatūras ķīlis saskarnes var atbalstīt skeneriem. Izveidot savienojumu ar datoru, skeneri var izmantot USB vai Bluetooth.

### <a name="msr"></a>MJL (magnētiskās joslas lasītājs)

Vienu USB magnētisko svītru lasītāju (MSR) var iestatīt, izmantojot OPOS draiveru. Ja vēlaties lietot stand-alone MSR elektronisko naudas pārskaitījumu (EFT) maksājumu darījumiem, maksājumu Connector jāpārvalda MSR. Stand-alone MSRs var izmantot klientu lojalitātes ieraksta, darbinieku pierakstīšanās un dāvanu kartes ierakstā, neatkarīgi no maksājumu savienotāju.

### <a name="cash-drawer"></a>Naudas atvilktnes

Divas naudas atvilktnes var atbalstīt vienu aparatūras profilu. Šī iespēja ļauj divas aktīvās maiņām, katrā reģistrā ir pieejama tajā pašā laikā. Koplietojamo maiņu vai naudas atvilktnes, ko izmanto vairākas mobilo POS ierīces, tajā pašā laikā, tikai viens naudas atvilktne ir atļauta par aparatūras profilu. Naudas atvilktnes var tieši savienots ar datoru, izmantojot USB, savienots ar tīklu vai pieslēgts printeris saņemšanas caur RJ12 interfeisu. Dažos gadījumos naudas atvilktnes var tikt arī savienoti, izmantojot Bluetooth.

### <a name="line-display"></a>Rindu displejs

Līnija parāda tiek izmantoti, lai rādītu produktus, darījumu atlikumu un citu noderīgu informāciju klientam darījuma laikā. Vienu rindu displejs var savienot ar datoru, izmantojot USB, izmantojot OPOS draiverus.

### <a name="signature-capture"></a>Paraksta ieguve

Paraksts tveršanas ierīces var savienot tieši ar datoru, izmantojot USB, izmantojot OPOS draiveru. Paraksts sagūstīt konfigurējot klientam tiek piedāvāts parakstīt ierīcē. Kad paraksts ir iesniedzis, tas ir redzams kasieris pieņemšanas.

### <a name="scale"></a>Mērogs

Svarus var savienot ar datoru, izmantojot USP, izmantojot OPOS draiveru. Kad produkts, kas ir atzīmēts kā "Weighed" produkts tiek pievienota darbība, POS no skalas nolasa svaru, pievieno produkta darbība un izmanto mēroga nosacījumu daudzumu.

### <a name="pin-pad"></a>PIN bloks

Personiskā identifikācijas numura (PIN) spilventiņi tiek atbalstītas caur OPOS, bet tās ir jāvada, izmantojot maksājumu savienotāju.

### <a name="secondary-display"></a>Sekundārs displejs

Konfigurējot sekundāro displeju skaits 2 Windows displeja izmanto, lai parādītu pamatinformāciju. Sekundārs displejs mērķis ir atbalstīt neatkarīga programmatūras pārdevēja (ISV) paplašinājumu, jo standarta komplektācijā, sekundārs displejs nav konfigurējams, un rāda ierobežoto saturu.

### <a name="payment-device"></a>Maksājumu ierīce

Ierīce atbalsta maksājumu īsteno maksājumu savienotāju. Maksājumu ierīcēm var veikt vienu vai daudzām funkcijām, kuras sniedz citām ierīču klasēm. Piemēram, maksājumu ierīce var funkcionēt kā MSR/karšu lasītājs, rindu displejs, paraksta tveršanas ierīce vai PIN spilventiņu. Atbalsta maksājumu ierīcēm tiek īstenoti neatkarīgi no atsevišķu ierīci atbalstu, kas paredzēts citām ierīcēm, kas ir iekļauti aparatūras profilu.

## <a name="supported-interfaces"></a>Atbalstīto interfeisu
### <a name="opos"></a>OPOS

Lai palīdzētu nodrošināt, ka lielākais ierīču klāstu, ko var izmantot ar Microsoft Dynamics 365 operācijām - mazumtirdzniecības, POS nozares standartam OLE ir primārā mazumtirdzniecības perifērijas ierīces platforma, kas tiek atbalstīta programmā Microsoft Dynamics 365 operācijām - mazumtirdzniecības. POS standarta OLE tika ražots ar valsts mazumtirdzniecības federācija (NRF), kas nosaka nozares standarta sakaru protokolus mazumtirdzniecības perifērijas ierīcēm. OPOS ir plaši pieņemts OLE POS standarta ieviešanu. Tā tika izstrādāta 1990. gadu vidū un ir atjaunināts vairākas reizes kopš. OPOS nodrošina ierīces draivera arhitektūrā, kas iespējo viegli integrāciju POS aparatūras ar Windows balstītās POS sistēmām. OPOS vadīklas turi saziņu starp saderīgu aparatūru un POS programmatūra. OPOS kontrole sastāv no divām daļām:

-   **Kontrolēt objekta** -ierīces klase (piemēram, līnija parāda) kontroles objekts nodrošina saskarni datorprogramma. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) nodrošina standartizētu OPOS kontroles objekti, kas tiek sauktas arī par kopīgas kontroles objekti (CCOs) kopumu. CCOs tiek izmantota, lai pārbaudītu POS komponentu Microsoft Dynamics 365 operācijām - mazumtirdzniecības. Tādēļ, testēšana, palīdz garantēt, ka, Microsoft Dynamics 365 operācijām - mazumtirdzniecības atbalsta ierīces klase caur OPOS, daudzi ierīču tipiem var atbalstīt, ja ražotājs nodrošina pakalpojumu objekts, kas tiek būvētas OPOS. Jums nav precīzi pārbaudīt katras ierīces tipu.
-   **Pakalpojumu objektu** – pakalpojuma objekts nodrošina saziņu starp kontroles objekts (CCO) un ierīci. Parasti, servisa objektu ierīcei nodrošina ierīces ražotājs. Tomēr dažos gadījumos, iespējams, jums lejupielādēt no ražotāja vietnes pakalpojumu objekts. Piemēram, jaunākās servisa objektu var būt pieejami. Atrast ražotāja vietnē adresi, skatiet aparatūras dokumentāciju.

[![Kontrolēt objektu un pakalpojumu objektu](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) OLE OPOS īstenošanas atbalsts POS palīdz garantēt, ka, ja pareizi ieviestu standarta ierīču ražotāji un ražotāju organizācijas izdevējiem, POS sistēmām un atbalstītās ierīces var strādāt kopā, pat tad, ja tie iepriekš nebija uzrādījuši kopā. **Piezīme:** OPOS atbalsts negarantē atbalstu visām ierīcēm, kas ir OPOS draiveri. Microsoft Dynamics 365 operācijām - mazumtirdzniecības vispirms ir jāatbalsta šo ierīces tipu vai klasi, izmantojot OPOS. Turklāt pakalpojumu objektus iespējams, ne vienmēr ir atjaunināta ar jaunāko versiju CCOs. Jums jāapzinās, ka kopumā kvalitātes pakalpojumu objekti mainās.

### <a name="windows"></a>Windows

POS izdrukas saņemšanas ir optimizēta OPOS. OPOS mēdz būt daudz ātrāk nekā drukāšana, caur logiem. Tādēļ ir ieteicams izmantot OPOS, it īpaši mazumtirdzniecības vidē, kur 40 kolonnā ieņēmumi tiek drukāti un transakciju ilgums nedrīkst būt ātri. Lielākajai daļa ierīču izmantos OPOS kontrolē. Tomēr dažas OPOS saņemšana printeri atbalsta Windows draiveri. Lietojot Windows draiveri, varat piekļūt jaunāko fonti un tīkla viens printeris vairākos reģistros. Tomēr pastāv trūkumi, izmantojot Windows draiveri. Lūk, daži piemēri, šie trūkumi:

-   Lietojot Windows draiveri, attēli tiek apstrādāti pirms drukāšanas. Tādēļ, drukāšanas mēdz būt lēnāka, nekā tas ir ar printeriem, kas izmantoto, OPOS.
-   Ierīcēm, kas ir savienotas ar printeri ("margrietiņa-pieķēdēts"), iespējams, nedarbosies pareizi, lietojot Windows draiveri. Piemēram, naudas atvilktnes, iespējams, nevarēs atvērt, vai kvīts printerī varētu ne vārdu, kā jūs to sagaidāt.
-   OPOS atbalsta arī plašākas kopums mainīgie, kas attiecas uz mazumtirdzniecības saņemšana printeri, piemēram, papīra griešanas vai pavadzīmes drukāšanai.

Ja OPOS vadīklas ir pieejamas ar Windows printera, kuru lietojat, printeris vēl ir jāstrādā pareizi ar Microsoft Dynamics 365 operācijām - mazumtirdzniecības.

### <a name="universal-windows-platform"></a>Universal Windows platformas

UWP, attiecībā uz mazumtirdzniecības perifēro iekārtu, ir saistīta ar Windows atbalsta Plug and Play ierīces. Plug and Play ierīci, kas pievienots Windows OS versija, kas atbalsta šo ierīces tipu, ir nepieciešams, lai ierīci varētu izmantot kā paredzēti bez vadītāja. Piemēram, ja sistēma Windows atrod Bluetooth skaļruņu ierīces, OS zina ierīcei ir **Speaker** klases tipa. Tāpēc, un tā izturas pret šo ierīci kā skaļruni. Nekādu papildu iestatījums ir nepieciešams. Ja POS ierīces, daudzas USB ierīces var pievienot un sistēma Windows atpazīs tos kā cilvēka interfeisa ierīcēm (HIDs). Tomēr, iespējams, tas nevarēs noteikt tās iespējas, kuras nodrošina ierīce, jo ierīce nav norādīts klases vai veida ierīces. 10. Windows ierīču klasēm, svītru kodu skeneri un MSRs piebilda. Tāpēc, ja ierīces deklarē pati Windows 10 kā ierīce ir viena no šīm klasēm gūsiet, Windows uzklausīs notikumiem no ierīces piemērotos laikos. Mūsdienu POS atbalsta UWP MSRs un skenerus. Tādēļ, kad tā ir gatava datu ievadīšanai no vienas no šīm ierīcēm, un ir savienota ierīce, kurai pieder viena no šīm klasēm gūsiet, ierīci var lietot. Piemēram, ja UWP bārs kodu skeneris ir pievienots Windows 10 datoru un svītru kodu pierakstīšanās ir konfigurēts izmantošanai ar mūsdienu POS, svītru kodu skeneri kļūs aktīva pieteikšanās ekrānā. Nekādu papildu iestatījums ir nepieciešams. Papildu punktu pakalpojumu UWP ierīču klasēm tiek pievienoti Windows. Šīm klasēm klasēm ietver naudas atvilktnes un saņemšana printeri. Šīs jaunās ierīces klases mūsdienu POS atbalsts tiek gaidīta.

### <a name="keyboard-wedge"></a>Keyboard wedge

Tastatūras ķīlis ierīces nosūtīt datus datorā kā tad, ja dati tika ievadīts tastatūrā. Tādēļ, pēc noklusējuma lauks, kas darbojas pie ražotāju organizācijas saņems datus, kas ir skenētas vai ar rokas vēzienu aizgaiņāja. Dažos gadījumos šāda uzvedība var izraisīt nepareiza tipa datus jāskenē nepareizi laukā. Piemēram, lauks, kas paredzēts kredīta kartes datu ievades varētu ieskenēts svītrkodu. Daudzos gadījumos ir loģika POS, kas nosaka, vai dati, kas ir skenētas vai ar rokas vēzienu aizgaiņāja ir svītru kodu vai kartes zvēliens. Tāpēc dati ir apstrādāti pareizi. Tomēr, kad ierīcēm ir iestatīti kā OPOS, nevis ķīlis ierīces tastatūru, ir lielāka kontrole pār to, kā datus no šīs ierīces var patērēt, jo vairāk "zināms" par ierīci, kuras datu avots. Piemēram, datus no svītru kodu skeneri automātiski tiek atpazīta kā svītru kodu un saistīto ierakstu datu bāzē atrastas daudz vienkāršāk un ātrāk, nekā ja vispārīgais virkni meklēšanas tika izmantoti kā tastatūras ķīlis ierīču gadījumā.

### <a name="native-printer"></a>Iezemiešu printeri

Dzimtā (vai "Ierīce", kā tipu ir nosaukta aparatūras profilu) printeri, var konfigurēt, lai vaicāt lietotājam izvēlēties printeri, kas ir konfigurēts izmantošanai ar datoru. Kad printeris ir **ierīce** tips ir konfigurēta, ja drukāšanas darbību, sastopas mūsdienu POS lietotājiem tiek piedāvāts atlasīt printeri sarakstā. Šis princips atšķiras no uzvedības Windows draiveri, jo **Windows** printera tipa aparatūras profilu neuzrāda printeru saraksts. Tā vietā tas prasa, nosaukta printera jāsniedz **ierīces nosaukums** lauks.

### <a name="windows"></a>Windows

**Windows** ierīces tips tiek izmantots tikai printeriem. Konfigurējot Windows printera aparatūras profilu, jāierīko īpaša printera nosaukumu. Ja mūsdienu POS sastopas drukas notikumiem, ja ir konfigurēta Windows printeri, notikums tiks nodota norādīto Windows printeri. Lietotājs netiks piedāvāts atlasīt printeri.

### <a name="network"></a>Tīkls

Tīklā, tieši caur Interprocess Communications (IPC) aparatūras staciju, kas ir iebūvēts mūsdienu POS sistēmai Windows lietojumprogrammu vai caur citiem klientiem modernu POS IIS aparatūras iecirkni var izmantot tīkla adres naudas atvilktnes, saņemšana printeri un maksājumu termināļi.

## <a name="hardware-station-deployment-options"></a>Aparatūras stacijas izvietošanas opcijas
### <a name="ipc-built-in"></a>IPC (iebūvēta)

Interprocess Communications (IPC) aparatūras stacija ir iebūvēts mūsdienu POS sistēmai Windows pieteikumu. Izmantot aparatūras IPC stacija, piešķirt reģistru izmanto mūsdienu POS sistēmai Windows lietojumprogrammu aparatūras profilu. Pēc tam izveidot aparatūras stacijas **Dedicated** tipa krātuvi, kurā reģistrs izmantos. Startējot mūsdienu POS, IPC aparatūras stacija būs aktīva un POS perifērijas ierīcēm, ko esat konfigurējis būs gatavs lietošanai. Ja jūs īslaicīgi nav nepieciešama vietējo aparatūras kādu iemeslu dēļ, izmantojiet **pārvaldītu aparatūru stacijas** operāciju, lai izslēgtu aparatūras stacijas iespējas. Mūsdienu POS sazināties tieši ar tīkla perifērijas ierīces var izmantot arī IPC aparatūras stacija.

### <a name="iis"></a>IIS

Jūs varat izmantot IIS vai savrupiem versija aparatūras stacijas divos veidos. Deskriptors "IIS" nozīmē, ka POS lietojumprogramma pieslēdzas aparatūras staciju, izmantojot Microsoft Internet Information Services. POS lietojumprogramma pieslēdzas IIS aparatūras stacijas, izmantojot web pakalpojumus, kas darbojas datorā, kurā ierīces ir pievienotas. Ja lieto IIS, mazumtirdzniecības perifērijas ierīces, kas pievienotas aparatūras staciju var izmantot ar jebkuru POS reģistru, kas ir tajā pašā tīklā kā IIS aparatūras stacija. Jo tikai mūsdienu POS sistēmai Windows ir iebūvēts atbalsts mazumtirdzniecības perifērijas, visas citas modernās POS lietojumprogrammas jāizmanto IIS aparatūras stacijas sazināties ar POS perifērijas ierīcēm, kas ir konfigurēts aparatūras profilu. Tādēļ katrs gadījums IIS aparatūras stacijas pieprasa, dators, kurā darbojas web pakalpojumu un lietojumprogrammu, kas komunicē ar ierīcēm. IIS aparatūras stacija ir nepieciešama visas ne - Windows mūsdienu POS lietojumprogrammas.

#### <a name="dedicated"></a>Atvēlēts

Mūsdienu POS aparatūras stacijās izmanto **Dedicated** tipa atklāt perifērijas ierīces ir tieši pievienoti datoram, kur tiek izmantota app. Tomēr, **Dedicated** tipu var arī izmantot IIS aparatūras stacijām. Tradicionālās, fixed POS scenāriju, kas izmanto mākonis POS POS pieteikumu **Dedicated** aparatūras stacijas tipu lieto IIS aparatūras staciju, kas izvietota vienā datorā, kurā darbojas mākonis POS. Veltīta IIS aparatūras stacijas no mazumtirdzniecības perifērijas viedokļa, labāk mazumtirdzniecības perifērijas atbalsts tradicionālo, fixed POS scenāriji. Īpaši izstrādāts aparatūras stacijas atbalsta visas palīgierīces, kas atbalsta aparatūras profilu.

#### <a name="shared"></a>Koplietots

Kopīgi aparatūras stacijas paredzēts izmantot vairākas POS ierīces caur gaitā dienā. Kopīgi aparatūras stacijām ir optimizēts, lai atbalsta tikai naudas atvilktnes, saņemšana printeri un maksājumu termināļi. Nevar tieši izveidot savienojumu stand-alone svītru kodu skeneri, MSRs, līnija parāda, skalas vai citām ierīcēm. Pretējā gadījumā konflikti rodas, ja vairākās POS ierīces mēģina apgalvot šīm perifērijas ierīcēm, tajā pašā laikā. Lūk, kā konflikti tiek pārvaldīti atbalstītajām ierīcēm:

-   **Naudas atvilktne** – naudas atvilktne ir atvērta caur notikumu, kas tiek nosūtīts uz ierīci. Vienīgais jautājums, kas var rasties, ja naudas atvilktne sauc rodas, ja naudas atvilktne ir jau atvērta. Attiecībā uz kopīgu aparatūras stacijas naudas atvilktne ir jābūt uzstādītam kā **Shared** aparatūras profilu. Šis iestatījums neļauj POS pārbaude vai naudas atvilktnes jau ir atvērta, ja to sūta komandu atvērt.
-   **Saņemšana printeri** – ja divi saņemšanas drukāšanas komandas tiek nosūtītas aparatūras stacijas tajā pašā laikā, viens no komandas, kas var tikt zaudēts, atkarībā no ierīces. Dažām ierīcēm ir iekšējā atmiņā vai apvienošana, kuras var novērst šo problēmu. Ja drukāšanas darbība nav sekmīga, kasieris saņem kļūdas ziņojumu un varat vēlreiz mēģināt veikt drukāšanas darbība no POS.
-   **Gala maksājums** – ja kasieris mēģinājumiem konkurss par gala maksājumu darbību, kas jau tiek izmantots, ziņojums brīdina kasieris terminālā tiek izmantota, un lūdz kasieris, vēlāk mēģiniet vēlreiz. Parasti, kasieri, var redzēt, ka termināla jau tiek izmantots un gaidīs līdz cita transakcija ir pabeigta, pirms tie mēģina vēlreiz konkursu.

Validācija ir plānots nākotnē atbrīvot, atklāt vai neatbalstītu ierīces ir iestatītas aparatūras profilu, kas ir kartēts koplietošanas aparatūras stacija. Ja tiek konstatētas visas ierīces, kas netiek atbalstīts, lietotājs saņems ziņojumu, kurā teikts, ka ierīces netiek atbalstītas koplietojamo aparatūras stacijām. Attiecībā uz kopīgu aparatūras stacijas **atlasīt pēc konkursa** opcija ir iestatīta uz **Jā** reģistrā līmenī. Pēc tam POS lietotājiem tiek piedāvāts izvēlieties aparatūras staciju, atlasot piedāvājumu pie ražotāju organizācijas darbībai. Aparatūras staciju, ja ir atlasīta tikai brīdī, kad konkursa staciju aparatūras atlasi tiek pievienota tieši POS darbplūsmas mobilo scenārijiem. Kā papildu labumu, gala maksājuma rindu displejs netiek izmantots koplietotā scenārijiem. Ja gala maksājums tiek izmantots kā rindu displejs, citi lietotāji var tikt bloķēts no līdz brīdim, kad attiecīgais darījums ir noslēgts, izmantojot šo terminālu. Mobilo scenārijus, rindas var būt pievienots darbību ilgākā laika posmā. Tādēļ **atlasīt pēc konkursa** iespēja ir nepieciešama, lai nodrošinātu optimālu ierīces pieejamība.

### <a name="network-peripherals"></a>Tīkla perifērijas ierīcēm

Tīkla apzīmēšanas ierīces aparatūras profilu aktivizē naudas atvilktnes, saņemšana printeri un maksājumu termināļi ir savienoti, izmantojot tīkla savienojumu.

#### <a name="modern-pos-for-windows"></a>Mūsdienu POS sistēmai Windows

IP adreses tīkla perifērijas ierīcēm var norādīt divas vietas. Ja mūsdienu POS Windows klients izmanto vienotu tīkla perifērijas ierīcēm, jums vajadzētu noteikt šīs ierīces IP adreses, izmantojot **IP konfigurācija** opcija darbību rūtī reģistru, pats par sevi. Šajā gadījumā tīkla ierīces, kas tiks dalīta starp POS reģistri, var kartēt aparatūras profilu, kas ir tīkla ierīces, kas tai piešķirti tieši uz staciju koplietošanas aparatūras. Piešķirt IP adreses, izvēlieties staciju ka aparatūras **mazumtirdzniecības veikali** lapa, un pēc tam izmantojiet **IP konfigurācija** opcija **aparatūras stacijas** sadaļu, lai norādītu tīkla ierīces, kas tiek piešķirti šo staciju aparatūra. Aparatūras stacijām, kas ir tikai tīkla ierīcēm, nav nepieciešams izvietot aparatūru stacija, pats par sevi. Šajā gadījumā aparatūras stacija ir nepieciešama tikai, lai konceptuāli grupēt atkarībā no to atrašanās vietas, mazumtirdzniecības veikalu tīklu adres ierīcēm.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Mākonis POS, mūsdienu POS iOS un mūsdienu POS Android

Loģika, kas vada fiziski saistīti un adres tīkla perifērijas ierīces atrodas stacijas aparatūru. Tādēļ visas POS klientiem, izņemot mūsdienu POS sistēmai Windows, IIS aparatūras stacijai jābūt izvietotiem un aktīvi darbojas, lai ļautu sazināties ar perifēro iekārtu, neatkarīgi no tā, vai šīm perifērijas fiziski savienots ar aparatūras staciju vai adresēts tīklā POS.

## <a name="setup-and-configuration"></a>Iestatīšanu un konfigurēšanu
### <a name="hardware-station-installation"></a>Aparatūras stacijas uzstādīšana

Informāciju, skatiet [mazumtirdzniecības stacijas aparatūras un iekārtas](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Mūsdienu POS sistēmai Windows iestatīšanu un konfigurēšanu

Informāciju, skatiet [mazumtirdzniecības mūsdienu POS konfigurāciju un uzstādīšana](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS ierīces uzstādīšana un konfigurācija

Plašāku informāciju par komponentu OPOS skatiet šī dokumenta sadaļu "Atbalstītās saskarnes". Parasti OPOS draiveri nodrošina ierīces ražotājs. Kad OPOS ierīces draiveris ir instalēts, tas pievieno atslēgu Windows reģistra vienā no šīm vietām:

-   **32 bitu sistēmu:** HKEY\_vietējo\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64 bitu sistēmas:** HKEY\_vietējo\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

Reģistra atrašanās vietā ServiceOPOS, konfigurēta ierīces tiek organizēta atbilstoši OPOS ierīces klase. Tiek saglabātas vairākas ierīces draiverus.

## <a name="supported-scenarios-by-hardware-station-type"></a>Atbalstīta scenārijus ar aparatūras stacijas tips
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Klientu atbalsts-IPC aparatūras stacijas vs IIS aparatūras stacija

Šajā tabulā apskatāms, topoloģijas un izvietošanas scenārijos, kas ir atbalstīts.

| Klients      | IPC aparatūras stacija | IIS aparatūras stacija |
|-------------|----------------------|----------------------|
| Windows app | Jā                  | Jā                  |
| Cloud POS   | Nav                   | Jā                  |
| Android     | Nav                   | Jā                  |
| iOS         | Nav                   | Jā                  |

### <a name="network-peripherals"></a>Tīkla perifērijas ierīcēm

Tīkla perifērijas ierīces var atbalstīt tieši caur aparatūras staciju, kas ir iebūvēts mūsdienu POS sistēmai Windows pieteikumu. Attiecībā uz citiem klientiem, jums tās jāizvieto IIS aparatūras stacija.

| Klients      | IPC aparatūras stacija | IIS aparatūras stacija |
|-------------|----------------------|----------------------|
| Windows app | Jā                  | Jā                  |
| Cloud POS   | Nav                   | Jā                  |
| Android     | Nav                   | Jā                  |
| iOS         | Nav                   | Jā                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Atbalsta aparatūras stacijas veida ierīču tipi
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Mūsdienu POS sistēmai Windows ar IPC (iebūvēti) aparatūras stacija

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atbalstītās ierīces klase</th>
<th>Atbalstīto interfeisu</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printeris</td>
<td><ul>
<li>OPOS</li>
<li>Windows draiveris</li>
<li>Ierīce</li>
<li>Tīkls</li>
</ul></td>
</tr>
<tr class="even">
<td>2. printeris</td>
<td><ul>
<li>OPOS</li>
<li>Windows draiveris</li>
<li>Ierīce</li>
<li>Tīkls</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rindu displejs</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Duālais displejs</td>
<td>Windows draiveris</td>
</tr>
<tr class="odd">
<td>MJL (magnētiskās joslas lasītājs)</td>
<td><ul>
<li>OPOS</li>
<li>UWP (nav setup ir nepieciešama).</li>
<li>Tastatūras ķīlis (nav setup ir nepieciešama).</li>
</ul></td>
</tr>
<tr class="even">
<td>Dokumenta sastādītājs</td>
<td><ul>
<li>OPOS</li>
<li>Tīkla <strong>Piezīme:</strong> tikai vienu atvilktni var iestatīt, ja <strong>izmantot koplietojamo pāreju</strong> ir konfigurēta uz paplātes.</li>
</ul></td>
</tr>
<tr class="odd">
<td>2. dokumenta sastādītājs</td>
<td><ul>
<li>OPOS</li>
<li>Tīkla <strong>Piezīme:</strong> tikai vienu atvilktni var iestatīt, ja <strong>izmantot koplietojamo pāreju</strong> ir konfigurēta uz paplātes.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skeneris</td>
<td><ul>
<li>OPOS</li>
<li>UWP (nav setup ir nepieciešama).</li>
<li>Tastatūras ķīlis (nav setup ir nepieciešama).</li>
</ul></td>
</tr>
<tr class="odd">
<td>2. skeneris</td>
<td><ul>
<li>OPOS</li>
<li>UWP (nav setup ir nepieciešama).</li>
<li>Tastatūras ķīlis (nav setup ir nepieciešama).</li>
</ul></td>
</tr>
<tr class="even">
<td>Mērogs</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN bloks</td>
<td>OPOS (atbalsts tiek sniegts, izmantojot maksājumu savienotājs pielāgošanas.)</td>
</tr>
<tr class="even">
<td>Paraksta ieguve</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Maksājumu terminālis </td>
<td><ul>
<li>Pielāgoto ierīču atbalsts</li>
<li>Tīkla (Papildinformāciju skatiet maksājuma savienotājs dokumentācijā).</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Visas mūsdienu POS klientiem, kas ir veltīta IIS aparatūras stacija

**Piezīme:** ja IIS aparatūras stacija ir "speciālā", ir relācija starp POS klientu un aparatūras stacija.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atbalstītās ierīces klase</th>
<th>Atbalstīto interfeisu</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printeris</td>
<td><ul>
<li>OPOS</li>
<li>Windows draiveru <strong>Piezīme:</strong> For Windows printeri tīklā, aparatūras stacijas lietotājam jābūt atļaujai piekļūt printerim.</li>
<li>Tīkls</li>
</ul></td>
</tr>
<tr class="even">
<td>2. printeris</td>
<td><ul>
<li>OPOS</li>
<li>Windows draiveris</li>
<li>Tīkls</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rindu displejs</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>MJL (magnētiskās joslas lasītājs)</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Dokumenta sastādītājs</td>
<td><ul>
<li>OPOS</li>
<li>Tīkla <strong>Piezīme:</strong> tikai vienu atvilktni par aparatūras profilu var iestatīt, ja <strong>izmantot koplietojamo pāreju</strong> ir konfigurēta uz paplātes.</li>
</ul></td>
</tr>
<tr class="even">
<td>2. dokumenta sastādītājs</td>
<td><ul>
<li>OPOS</li>
<li>Tīkls</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skeneris</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>2. skeneris</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Mērogs</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>PIN bloks</td>
<td>OPOS (atbalsts tiek sniegts, izmantojot maksājumu savienotājs pielāgošanas.)</td>
</tr>
<tr class="odd">
<td>SIG. ieguve</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Maksājumu terminālis </td>
<td><ul>
<li>Pielāgoto ierīču atbalsts</li>
<li>Tīkla (Papildinformāciju skatiet maksājuma savienotājs dokumentācijā).</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Visas mūsdienu POS klientiem, kas ir koplietošanas IIS aparatūras stacija

**Piezīme:** ja IIS aparatūras stacija ir "kopīgi", vairākas ierīces aparatūras staciju var izmantot vienlaicīgi. Šajā scenārijā, jums vajadzētu izmantot tikai ierīcēs, kas ir uzskaitīti tabulā turpmāk. Ja mēģināt koplietot ierīces, kas nav uzskaitīti šeit, piemēram, svītru kodu skeneri un MSRs, kļūdas rodas, ja vairākas ierīces mēģina apgalvot pašu perifērijas. Nākotnē šāda konfigurācija būs skaidri novērsts.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atbalstītās ierīces klase</th>
<th>Atbalstīto interfeisu</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printeris</td>
<td><ul>
<li>OPOS</li>
<li>Windows draiveru <strong>Piezīme:</strong> For Windows printeri tīklā, aparatūras stacijas lietotājam jābūt atļaujai piekļūt printerim.</li>
<li>Tīkls</li>
</ul></td>
</tr>
<tr class="even">
<td>2. printeris</td>
<td><ul>
<li>OPOS</li>
<li>Windows draiveris</li>
<li>Tīkls</li>
</ul></td>
</tr>
<tr class="odd">
<td>Dokumenta sastādītājs</td>
<td><ul>
<li>OPOS</li>
<li>Tīkla <strong>Piezīme:</strong> tikai vienu atvilktni par aparatūras profilu var iestatīt, ja <strong>izmantot koplietojamo pāreju</strong> ir konfigurēta uz paplātes.</li>
</ul></td>
</tr>
<tr class="even">
<td>2. dokumenta sastādītājs</td>
<td><ul>
<li>OPOS</li>
<li>Tīkls</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maksājumu terminālis </td>
<td><ul>
<li>Pielāgoto ierīču atbalsts</li>
<li>Tīkla (Papildinformāciju skatiet maksājuma savienotājs dokumentācijā).</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Konfigurācija, kas domāta atbalstīto scenāriji
Papildinformāciju par aparatūras profili, sk [definēt un saglabāt kanālu klientu uzdevumā, tostarp reģistriem un aparatūras stacijas](define-maintain-channel-clients-registers-hw-stations.md). **Piezīme:** par Microsoft Dynamics 365 darbību versija 1611, stacijas aparatūras profils vairs neizmanto. Atribūtus, kurus iepriekš iestatāt staciju aparatūras profilu tagad ir daļa no aparatūras stacija, pats par sevi.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Mūsdienu POS sistēmai Windows ar IPC (iebūvēti) aparatūras stacija

Šī konfigurācija ir tipiskākās konfigurācija tradicionālo, fixed POS reģistriem. Šī scenārija aparatūras profilu informāciju tiek plānots tieši pati reģistra. EFT terminālu skaits jānosaka arī par reģistru, pats par sevi. Lai iestatītu šo konfigurāciju, rīkojieties šādi.

1.  Radīt aparatūras profilu, kur nepieciešama perifērijas ierīces ir konfigurēti.
2.  Kartēt aparatūras profilu POS reģistrā.
3.  Radīt aparatūras stacijas **Dedicated** tipa mazumtirdzniecības veikalā, kurā izmantos POS reģistrā. Apraksts nav obligāts. **Piezīme:** jums nav aparatūras stacijā noteikt citus rekvizītus. Visu citu pieprasīto informāciju, piemēram, aparatūras profilu, nāks no reģistra, pats par sevi.
4.  Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**mazumtirdzniecības tā**&gt;**sadalījuma grafiks**.
5.  Atlasiet **1090** sadales grafiks, lai sinhronizētu jaunās aparatūras profilu krātuvē. Noklikšķiniet uz **bēgtu** ro sinhronizācijas izmaiņas.
6.  Atlasiet **1040** sadales grafiks, lai sinhronizētu jaunās aparatūras stacijas uz veikalu. Noklikšķiniet uz **bēgtu** ro sinhronizācijas izmaiņas.
7.  Instalēt un aktivizēt mūsdienu POS sistēmai Windows.
8.  Mūsdienu POS sistēmas Windows startēšana un sāk izmantot pievienotās perifērijas ierīces.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Visas mūsdienu POS klientiem, kas ir veltīta IIS aparatūras stacija

Šī konfigurācija var izmantot visas modernās POS klientiem, kas ir aparatūras stacijas, ko izmanto tikai viena POS reģistrēties. Lai iestatītu šo konfigurāciju, rīkojieties šādi.

1.  Radīt aparatūras profilu, kur nepieciešama perifērijas ierīces ir konfigurēti.
2.  Radīt aparatūras stacijas **Dedicated** tipa mazumtirdzniecības veikalā, kurā izmantos POS reģistrā.
3.  Speciāla aparatūra stacijā, iestatiet šādus rekvizītus:
    -   **Resursdatora nosaukums** -resursdatorā, kur darbosies aparatūras stacijas nosaukumu. **Piezīme:** POS mākonis var atrisināt **localhost** noteikt lokālajā datorā, kur darbojas mākonis POS. Tomēr, sertifikāts, kas ir nepieciešama, lai pāri mākonis POS aparatūras stacijā jābūt arī "Localhost" ar datora nosaukumu. Lai izvairītos no problēmas, mēs iesakām sarakstu, piemēram, katrā veikalā, kā to prasa īpašu aparatūru stacijas. Katras stacijas aparatūra, resursdatora nosaukumu vajadzētu būt noteiktu datora nosaukumu kur staciju aparatūra tiks izvietota.
    -   **Port** – ostas stacijas aparatūras izmantot saziņai ar mūsdienu POS klientu.
    -   **Aparatūras profils** – ja aparatūras profilu nav nosacījumu pati aparatūra stacija, aparatūras profilu, kurš tiek piešķirts reģistra tiks izmantoti.
    -   **EFT POS numuru** -EFT termināļa ID, ko izmantot, nosūtot EFT atļaujām. Šo identifikāciju nodrošina kredītkaršu procesors.
    -   **Pakotnes nosaukums** – aparatūras stacijas iepakojuma izmantot aparatūras stacija izvietojot.

4.  Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**mazumtirdzniecības tā**&gt;**sadalījuma grafiks**.
5.  Atlasiet **1090** sadales grafiks, lai sinhronizētu jaunās aparatūras profilu krātuvē. Noklikšķiniet uz **bēgtu** ro sinhronizācijas izmaiņas.
6.  Atlasiet **1040** sadales grafiks, lai sinhronizētu jaunās aparatūras stacijas uz veikalu. Noklikšķiniet uz **bēgtu** ro sinhronizācijas izmaiņas.
7.  Instalētu aparatūru stacija. Plašāku informāciju par to, kā instalēt aparatūru staciju, skatiet [mazumtirdzniecības stacijas aparatūras un iekārtas](retail-hardware-station-configuration-installation.md).
8.  Instalēt un aktivizēt mūsdienu POS. Plašāku informāciju par to, kā uzstādīt modernas POS, sk [mazumtirdzniecības mūsdienu POS konfigurāciju un uzstādīšana](retail-modern-pos-device-activation.md).
9.  Ieejiet mūsdienu POS un atlasiet **veikt operācijas, ne atvilktnes**.
10. Sākt **pārvaldītu aparatūru stacijas** darbību.
11. Noklikšķiniet uz **pārvaldīt**.
12. Aparatūras staciju pārvaldības lapā iestatiet opciju ieslēgt aparatūras stacija.
13. Izvēlieties aparatūras staciju un pēc tam noklikšķiniet uz **pāri**.
14. Pēc aparatūras stacijas ir savienotas pārī, noklikšķiniet uz **tuvu**.
15. Aparatūras stacijas atlases lapā noklikšķiniet uz pēdējo atlasīto aparatūras stacijas, lai to aktivizētu.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Visas mūsdienu POS klientiem, kas ir koplietošanas IIS aparatūras stacija

Šī konfigurācija var izmantot visas modernās POS klientus, ka aparatūras stacijas dalīties ar citām ierīcēm. Lai iestatītu šo konfigurāciju, rīkojieties šādi.

1.  Kur ir konfigurēti nepieciešamo perifērijas aparatūras profila izveide.
2.  Radīt aparatūras stacijas **Shared** tipa mazumtirdzniecības veikalā, kurā izmantos POS reģistrā.
3.  Koplietojamo aparatūras stacijā, iestatiet šādus rekvizītus:
    -   **Resursdatora nosaukums** -resursdatorā, kur darbosies aparatūras stacijas nosaukumu.
    -   **Aprakstu** -tekstu, kurš palīdzēs identificēt stacijas aparatūru, piemēram, **atgriež** vai **pie veikala**.
    -   **Port** – ostas stacijas aparatūras izmantot saziņai ar mūsdienu POS klientu.
    -   **Aparatūras profils** – koplietošanas aparatūras stacijas katru aparatūras staciju būtu aparatūras profilu. Aparatūras profilus var koplietot aparatūras stacijas, bet tie ir samērot katru aparatūras staciju. Turklāt mēs iesakām izmantot koplietojamu maiņās, kad vairākas ierīces, kas izmanto vienu un to pašu koplietojamo aparatūras stacija. Lai iestatītu koplietojamās pāreju, noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**POS profili**&gt;**Hardware Profili**. Katru kopīgu aparatūras profils atlasiet naudas atvilktnes un iestatīt **Shared maiņu atvilktne** iespēju **Jā**.
    -   **EFT POS numuru** -EFT termināļa ID, ko izmantot, nosūtot EFT atļaujām. Šo identifikāciju nodrošina kredītkaršu procesors.
    -   **Pakotnes nosaukums** – aparatūras stacijas iepakojuma izmantot aparatūras stacija izvietojot.

4.  Atkārtojiet 2. un 3. soli katrai papildu aparatūra stacijas, kas tiek prasīts uzglabāt.
5.  Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**mazumtirdzniecības tā**&gt;**sadalījuma grafiks**.
6.  Atlasiet **1090** sadales grafiks, lai sinhronizētu jaunās aparatūras profilu krātuvē. Noklikšķiniet uz **bēgtu** ro sinhronizācijas izmaiņas.
7.  Atlasiet **1040** sadales grafiks, lai sinhronizētu jaunās aparatūras stacijas uz veikalu. Noklikšķiniet uz **bēgtu** ro sinhronizācijas izmaiņas.
8.  Instalētu aparatūru stacijas katrā resursdatorā, ko iestatāt formā 2. un 3. soli. Plašāku informāciju par to, kā instalēt aparatūru staciju, skatiet [mazumtirdzniecības stacijas aparatūras un iekārtas](retail-hardware-station-configuration-installation.md).
9.  Instalēt un aktivizēt mūsdienu POS. Plašāku informāciju par to, kā uzstādīt modernas POS, sk [mazumtirdzniecības mūsdienu POS konfigurāciju un uzstādīšana](retail-modern-pos-device-activation.md).
10. Ieejiet mūsdienu POS un atlasiet **veikt operācijas, ne atvilktnes**.
11. Sākt **pārvaldītu aparatūru stacijas** darbību.

12. Noklikšķiniet uz **pārvaldīt**.
13. Aparatūras staciju pārvaldības lapā iestatiet opciju ieslēgt aparatūras stacija.
14. Izvēlieties aparatūras staciju un pēc tam noklikšķiniet uz **pāri**.
15. Katrs aparatūras staciju, kas izmanto mūsdienu POS atkārtojiet darbību 14.
16. Pēc tam, kad visas nepieciešamās aparatūras stacijas ir savienotas pārī, noklikšķiniet **tuvu**.
17. Aparatūras stacijas atlases lapā noklikšķiniet uz pēdējo atlasīto aparatūras stacijas, lai to aktivizētu. **Piezīme:** ja ierīces bieži izmanto dažādas aparatūras stacijas, ieteicams konfigurēt mūsdienu POS pamudinājusi kasieri izvēlieties aparatūras staciju, kad viņi sāks konkursa procesa. Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**reģistrē**. Izvēlieties reģistrēties un pēc tam iestatiet **pēc piedāvājumu izvēlētos** iespēju **Jā**. Izmantojiet **1090** sadalījuma grafiks sinhronizēt izmaiņas kanālu datu bāzē.

## <a name="extensibility"></a>Paplašināmība
Informāciju par paplašināšanas scenārijus stacijas aparatūru, skatiet [aparatūras stacijas paplašināšanu](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Drošība
Saskaņā ar pašreizējo drošības standartiem, ir jāizmanto šādi iestatījumi ražošanas vidē: **Piezīme:** aparatūras stacijas uzstādītājam automātiski veikt labojumus šīs reģistra kā daļu no iekārtas, izmantojot pašapkalpošanās līdzekļus.

-   Drošligzdu slāņa (SSL) ir atspējota.
-   Tikai Transport Layer Security (TLS) 1.2 (vai pašreizējo augstāko versija) aktivizē un izmantot. **Piezīme:** pēc noklusējuma ir atspējota SSL un TLS izņemot TLS 1.2 visas versijas. Lai rediģētu vai iespējotu šīs vērtības, rīkojieties šādi:
    1.  Nospiediet Windows logotipa taustiņu + R, lai atvērtu **palaist** logu.
    2.  Šajā **Open** laukā, ievadiet **Regedit**, un pēc tam noklikšķiniet uz **labi**.
    3.  Ja **User Account Control** parādās ziņojuma lodziņš, klikšķiniet uz **Jā**.
    4.  Šajā **Registry Editor** logā naviģējiet uz **HKEY\_vietējo\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Šādus taustiņus automātiski ievadīta tikai pagaidiet TLS 1.2:
        -   TLS 1.2Server: iespējots = 1
        -   TLS 1.2Server:DisabledByDefault = 0
        -   TLS 1.2Client: iespējots = 1
        -   TLS 1.2Client:DisabledByDefault = 0
        -   TLS 1.1Server: iespējots = 0
        -   TLS 1.1Client: iespējots = 0
        -   TLS 1.0Server: iespējots = 0
        -   TLS 1.0Client: iespējots = 0
        -   SSL 3.0Server: iespējots = 0
        -   SSL 3.0Client: iespējots = 0
        -   SSL 2.0Server: iespējots = 0
        -   SSL 2.0Client: iespējots = 0
-   Nekādu papildu tīkla portus vajadzētu būt pieejamai, ja vien tie ir nepieciešami zināmi, norādīto iemeslu dēļ.
-   Cross-izcelsmes resursu koplietošanas jāizslēdz un jānorāda atļauto izcelsme, kas ir pieņemts.
-   Tikai uzticamas sertificēšanas institūcijas būtu jāizmanto, lai iegūtu sertifikātu, kas datoros, kas darbojas stacijas aparatūra tiks izmantota.

**Piezīme:** ir ļoti svarīgi, pārskatīt drošības vadlīnijas attiecībā uz IIS un maksājumu karšu nozare (PCI) prasībām.

## <a name="peripheral-simulator"></a>Perifērijas simulators
Informāciju, skatiet [mazumtirdzniecības perifērijas simulator](retail-peripheral-simulator.md).

## <a name="microsofttested-peripheral-devices"></a>Microsofttested perifērijas ierīcēm
### <a name="ipc-built-in-hardware-station"></a>IPC (iebūvēti) aparatūras stacija

Šīm perifērijas ierīcēm tika pārbaudīta, izmantojot IPC aparatūras staciju, kas mūsdienu POS sistēmā Windows ir iebūvēts.

#### <a name="printer"></a>Printeris

| Ražotājs | Modelis    | Interfeiss | Komentāri                |
|--------------|----------|-----------|-------------------------|
| Epson        | TM T88IV | OPOS      |                         |
| Epson        | TM T88V  | OPOS      |                         |
| Zvaigzne         | TSP650II | OPOS      |                         |
| Zvaigzne         | TSP650II | Pielāgot    | Savienots ar tīklu   |
| Zvaigzne         | mPOP     | OPOS      | Savienoti, izmantojot Bluetooth |
| ZS           | F7M67AA  | OPOS      | Powered USB             |

#### <a name="bar-code-scanner"></a>Svītrkodu skeneri

| Ražotājs  | Modelis         | Interfeiss | Komentāri |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Simbols        | LS2208        | OPOS      |          |
| Integrēts ZS | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>PIN bloks

| Ražotājs | Modelis  | Interfeiss | Komentāri                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Prasa pielāgojumus maksājumu savienotājs |

#### <a name="payment-terminal"></a>Maksājumu terminālis 

| Ražotājs | Modelis | Interfeiss | Komentāri                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Ekvinokcija      | L5300 | Pielāgot    | Prasa pielāgojumus maksājumu savienotājs                                |
| VeriFone     | MX925 | Pielāgot    | Prasa pielāgojumus maksājumu savienotājs; savienots ar tīklu un USB |
| VeriFone     | MX915 | Pielāgot    | Prasa pielāgojumus maksājumu savienotājs; savienots ar tīklu un USB |

#### <a name="cash-drawer"></a>Naudas atvilktnes

| Ražotājs | Modelis     | Interfeiss | Komentāri                |
|--------------|-----------|-----------|-------------------------|
| Zvaigzne         | mPOP      | OPOS      | Savienoti, izmantojot Bluetooth |
| APG          | Atwood    | Pielāgot    | Savienots ar tīklu   |
| Zvaigzne         | SMD2-1317 | OPOS      |                         |
| ZS           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>Rindu displejs

| Ražotājs  | Modelis   | Interfeiss | Komentāri |
|---------------|---------|-----------|----------|
| Integrēts ZS | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Paraksta ieguve

| Ražotājs | Modelis  | Interfeiss | Komentāri |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Mērogs

| Ražotājs | Modelis         | Interfeiss | Komentāri |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MJL (magnētiskās joslas lasītājs)

| Ražotājs | Modelis       | Interfeiss | Komentāri |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| ZS           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Veltīta IIS aparatūras stacija

Izmantojot speciālu (netiek koplietota) IIS aparatūras stacija kopā ar mūsdienu POS sistēmai Windows un mākonis POS tika pārbaudītas šīm perifērijas ierīcēm.

#### <a name="printer"></a>Printeris

| Ražotājs | Modelis    | Interfeiss | Komentāri                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM T88IV | OPOS      |                           |
| Epson        | TM T88V  | OPOS      |                           |
| Zvaigzne         | TSP650II | OPOS      |                           |
| Zvaigzne         | TSP650II | Pielāgot    | Savienots ar tīklu     |
| Zvaigzne         | TSP100   | OPOS      | Prasa TSP650II draiveri |
| ZS           | F7M67AA  | OPOS      | Powered USB               |

#### <a name="bar-code-scanner"></a>Svītrkodu skeneri

| Ražotājs  | Modelis   | Interfeiss | Komentāri |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| Simbols        | LS2208  | OPOS      |          |
| Integrēts ZS | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>PIN bloks

| Ražotājs | Modelis  | Interfeiss | Komentāri                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Prasa pielāgojumus maksājumu savienotājs |

#### <a name="payment-terminal"></a>Maksājumu terminālis 

| Ražotājs | Modelis | Interfeiss | Komentāri                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Ekvinokcija      | L5300 | Pielāgot    | Prasa pielāgojumus maksājumu savienotājs                                |
| VeriFone     | MX925 | Pielāgot    | Prasa pielāgojumus maksājumu savienotājs; savienots ar tīklu un USB |
| VeriFone     | MX915 | Pielāgot    | Prasa pielāgojumus maksājumu savienotājs; savienots ar tīklu un USB |

#### <a name="cash-drawer"></a>Naudas atvilktnes

| Ražotājs | Modelis     | Interfeiss | Komentāri              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Pielāgot    | Savienots ar tīklu |
| Zvaigzne         | SMD2-1317 | OPOS      |                       |
| ZS           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>Rindu displejs

| Ražotājs  | Modelis   | Interfeiss | Komentāri |
|---------------|---------|-----------|----------|
| Integrēts ZS | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Paraksta ieguve

| Ražotājs | Modelis  | Interfeiss | Komentāri |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Mērogs

| Ražotājs | Modelis         | Interfeiss | Komentāri |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MJL (magnētiskās joslas lasītājs)

| Ražotājs | Modelis       | Interfeiss | Komentāri |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| ZS           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Koplietojamo IIS aparatūras stacija

Izmantojot koplietoto IIS aparatūras stacija kopā ar mūsdienu POS sistēmai Windows un mākonis POS tika pārbaudītas šīm perifērijas ierīcēm. **Piezīme:** tiek atbalstīti tikai printeris, maksājumu termināli un naudas atvilktnes.

#### <a name="printer"></a>Printeris

| Ražotājs | Modelis    | Interfeiss | Komentāri                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM T88IV | OPOS      |                           |
| Epson        | TM T88V  | OPOS      |                           |
| Zvaigzne         | TSP650II | OPOS      |                           |
| Zvaigzne         | TSP650II | Pielāgot    | Savienots ar tīklu     |
| Zvaigzne         | TSP100   | OPOS      | Prasa TSP650II draiveri |
| ZS           | F7M67AA  | OPOS      | Powered USB               |

#### <a name="payment-terminal"></a>Maksājumu terminālis 

| Ražotājs | Modelis | Interfeiss | Komentāri                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Pielāgot    | Prasa pielāgojumus maksājumu savienotājs; savienots ar tīklu un USB |
| VeriFone     | MX915 | Pielāgot    | Prasa pielāgojumus maksājumu savienotājs; savienots ar tīklu un USB |

#### <a name="cash-drawer"></a>Naudas atvilktnes

| Ražotājs | Modelis     | Interfeiss | Komentāri              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Pielāgot    | Savienots ar tīklu |
| Zvaigzne         | SMD2-1317 | OPOS      |                       |
| ZS           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>Problēmu novēršana
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Mūsdienu POS aparatūras stacijas var noteikt tās atlases sarakstā, bet tā nevar pabeigt savienošana pārī

**Risinājums:** pārbaudīt iespējamās kļūmes punktus šajā sarakstā:

-   Datorā, kurā darbojas mūsdienu POS uzticas sertifikāts, kas tiek izmantots datorā, kurā darbojas stacijas aparatūru.
    -   Lai pārbaudītu šo iestatījumu web pārlūkprogrammā dodieties uz šādu URL: https://&lt;datora nosaukums&gt;:&lt;porta numuru&gt;/HardwareStation/ping.
    -   Šis URL izmanto ping, pārbaudiet, vai datorā var piekļūt, un pārlūkprogrammas norāda, vai sertifikāts ir uzticams. (Piemēram, Internet Explorer, tiek parādīta slēdzenes ikona adrešu joslā. Noklikšķinot uz šīs ikonas, Internet Explorer pārbauda, vai sertifikāts ir pašlaik uzticama. Varat instalēt sertifikātu lokālajā datorā, skatot detalizētu informāciju par sertifikātu, kas tiek parādīts.)
-   Datorā, kurā darbojas stacijas aparatūra, ostas, kuru izmantos aparatūras stacija tiek atvērts ugunsmūri.
-   Staciju aparatūra pareizi instalēta tirgotāja konta informāciju, izmantojot instalēšanas komersanta informācijas rīks, kas darbojas aparatūra stacijas uzstādītājam beigās.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Mūsdienu POS aparatūras stacija nevar noteikt tās atlases sarakstā

**Risinājums:** nu šādi faktori var izraisīt šo problēmu:

-   Aparatūras stacija nav iestatīts pareizi galvenajā mītnē. Lai pārbaudītu staciju aparatūras profilu un staciju aparatūra ir pareizi ievadīta, veiciet darbības iepriekš šajā tēmā.
-   Darbi nav palaist atjauninātu kanālu konfigurēšanai. Šajā gadījumā izpildiet 1070 darbu kanālu konfigurēšanai.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Mūsdienu POS neatspoguļo jauno naudas atvilktnes iestatījumus

**Risinājums:** aizvērt pašreizējo partiju. Izmaiņas naudas atvilktnes nav atjaunināts uz mūsdienu POS līdz pašreizējai partijai tiek aizvērts.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Mūsdienu POS ziņo jautājums ar perifērijas mazumtirdzniecības

**Risinājums:** šeit ir daži tipiski iemesli šo jautājumu:

-   Pārliecinieties, vai ir aizvērtas citas ierīces draivera konfigurācijas utilītās. Ja šie komunālie pakalpojumi ir atvērti, viņi var liegt mūsdienu POS vai aparatūras staciju, apgalvojot, ka ierīce.
-   Ja mazumtirdzniecības perifēro koplieto vairākas POS ierīces, pārliecinieties, ka tā pieder pie kādas no šādām kategorijām:
    -   Naudas atvilktnes
    -   Saņemšana printeri
    -   Maksājumu terminālis 

    Ja perifēro nepieder kādai no šīm kategorijām, aparatūras stacija nav paredzēta, lai ļautu perifēro jāsadala starp vairākiem POS ierīces.
-   Dažreiz, ierīces draiveri var radīt ar kopīgas kontroles objekti (CCOs) vairs nedarbojas pareizi. Ja ierīce nesen uzstādīta, bet tā nedarbojas pareizi vai ja konstatējat citas problēmas, bieži jautājumu var atrisināt, atkārtoti instalējot CCOs. Lai lejupielādētu CCOs, apmeklējiet <http://monroecs.com/oposccos_current.htm>.
-   Ja veicat perifērijas biežas izmaiņas testēšanu vai problēmu novēršanas laikā, esat atiestatīt IIS, nevis gaida, lai cache atsvaidzināt sevi. Lai restartētu IIS, rīkojieties šādi:
    1.  No **sākt** izvēlne, tipa **CMD**.
    2.  Meklēšanas rezultātus, noklikšķiniet ar peles labo pogu **komandu uzvednes**, un pēc tam noklikšķiniet uz **palaist kā administratoram**.
    3.  Šajā **komandu uzvednes** logā ierakstiet **iisreset setup** un pēc tam nospiediet taustiņu Enter.
    4.  Pēc IIS restartēšanas restartējiet mūsdienu POS.
-   Kamēr jūs gūstat biežajām izmaiņām uz perifērijas ierīcēm, ja arī bieži sākt un izietu no POS klientu, dllhost process no POS iepriekšējās sesijas var traucēt pašreizējo sesiju. Šajā gadījumā ierīce varētu nebūt lietojami līdz aizverat dinamisko saišu bibliotēkas (DLL) uzņēmēja, kas ir vadošā iepriekšējās sesijas. Lai aizvērtu DLL uzņēmējas, rīkojieties šādi:
    1.  No **sākt** izvēlne, tipa **uzdevumu pārvaldnieka**.
    2.  Meklēšanas rezultātos noklikšķiniet **uzdevumu pārvaldnieka**.
    3.  Uzdevumu pārvaldniekā, par **detaļas** cilni, noklikšķiniet uz kolonnas virsraksta, kas tiek apzīmēts ar **Name** uz galda sakārtotu alfabētiskā secībā pēc nosaukuma.
    4.  Ritiniet uz leju, līdz atrodat dllhost.exe.
    5.  Atlasiet katru DLL uzņēmējas un pēc tam noklikšķiniet uz **Beigt uzdevumu**.
    6.  Pēc DLL saimniekiem ir slēgti, restartējiet mūsdienu POS.


<a name="see-also"></a>Skatiet arī
--------

[Mazumtirdzniecības perifērijas simulators](retail-peripheral-simulator.md)


