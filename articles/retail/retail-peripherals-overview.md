---
title: Retail perifērijas ierīces
description: Šajā tēmā ir paskaidrotas koncepcijas, kas ir saistītas ar mazumtirdzniecības perifērajām ierīcēm.
author: rubencdelgado
manager: AnnBe
ms.date: 01/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice, RetailHardwareProfile
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9aba1dabe3b2304c1f0dfd449982af1d4bc15d6b
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742637"
---
# <a name="retail-peripherals"></a>Retail perifērijas ierīces

[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrotas koncepcijas, kas ir saistītas ar mazumtirdzniecības perifērajām ierīcēm. Tajā ir aprakstīti dažādie veidi, kā perifērijas ierīces var pievienot pārdošanas punktam (POS), un komponenti, kas nodrošina savienojuma ar POS pārvaldību.

## <a name="concepts"></a>Koncepcijas

### <a name="pos-registers"></a>POS kases sistēmas

Navigācija: noklikšķiniet uz **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **Reģistri**. Pārdošanas punkta (POS) kases sistēma ir elements, kas tiek izmantots, lai noteiktu konkrētas POS instances raksturlielumus. Šie raksturlielumi ietver aparatūras profilu jeb ar kases sistēmu izmantoto mazumtirdzniecības perifērijas ierīču iestatījumus, veikalu, ar kuru ir kartēta šī kases sistēma, un vizuālo noformējumu, ko redz lietotājs, kurš pierakstās šajā kases sistēmā.

### <a name="devices"></a>Ierīces

Navigācija: noklikšķiniet uz **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **Ierīces**. Ierīce ir elements, kas pārstāv fizisku instanci tādai ierīcei, kura ir kartēta uz POS reģistru. Kad ierīce tiek izveidota, tā tiek kartēta uz POS reģistru. Ierīces elements seko līdzi informācijai par laiku, kad POS reģistrs tiek aktivizēts, par izmantotā klienta tipu, kā arī par programmu pakotni, kas ir izvietota konkrētā ierīcē. Ierīces var kartēt ar šiem lietojumprogrammu veidiem: Retail Modern POS, Retail Cloud POS, Retail Modern POS — Windows Phone, Retail Modern POS — Android un Retail Modern POS — ISP.

### <a name="retail-modern-pos"></a>Retail Modern POS

Modern POS ir operētājsistēmai Microsoft Windows paredzētā POS programma. To var izvietot operētājsistēmās (OS) Windows 10.

### <a name="cloud-pos"></a>Cloud POS

Cloud POS ir programmas Modern POS mākoņa versija, kam var piekļūt tīmekļa pārlūkprogrammā.

### <a name="modern-pos-for-ios"></a>Modern POS operētājsistēmai iOS

Modern POS operētājsistēmai iOS ir operētājsistēmai iOS paredzētā programmas Modern POS versija, ko var izvietot iOS ierīcēs.

### <a name="modern-pos-for-android"></a>Modern POS operētājsistēmai Android

Modern POS operētājsistēmai Android ir operētājsistēmai Android paredzētā programmas Modern POS versija, ko var izvietot Android ierīcēs.

### <a name="pos-peripherals"></a>POS perifērās ierīces

POS perifērās ierīces ir ierīces, kas var tieši atbalstīt POS funkcijas. Parasti šīs perifērās ierīces ir sadalītas noteiktās klasēs. Papildinformāciju par šīm klasēm skatiet šīs tēmas sadaļā “Ierīču klases”.

### <a name="hardware-station"></a>Hardware Station

Navigācija: noklikšķiniet uz **Mazumtirdzniecība** &gt; **Kanāli** &gt; **Mazumtirdzniecības veikali** &gt; **Visi mazumtirdzniecības veikali**. Atlasiet veikalu un pēc tam noklikšķiniet uz kopsavilkuma cilnes **Aparatūras stacijas**. Iestatījums **Aparatūras stacija** ir kanāla līmeņa iestatījums, kas tiek izmantots, lai definētu instances, kurās tiks izvietota mazumtirdzniecības perifērās ierīces loģika. Šis iestatījums kanāla līmenī tiek izmantots, lai noteiktu aparatūras stacijas raksturlielumus. Tas tiek arī izmantots, lai norādītu aparatūras stacijas, kas ir pieejamas Modern POS instancei konkrētā veikalā. Aparatūras stacija ir iebūvēta programmā Modern POS operētājsistēmai Windows. Aparatūras staciju var arī izvietot atsevišķi kā savrupu Microsoft interneta informācijas pakalpojumu (IIS) programmu. Šādā gadījumā tai var piekļūt tīklā.

### <a name="hardware-profile"></a>Aparatūras profils

Navigācija: noklikšķiniet uz **Retail** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profili** &gt; **Aparatūras profili**. Aparatūras profils ir to ierīču saraksts, kas ir konfigurētas POS kases sistēmai vai aparatūras stacijai. Aparatūras profilu var tieši kartēt ar POS kases sistēmu vai aparatūras staciju.

## <a name="devices-classes"></a>Ierīču klases
Parasti POS perifērās ierīces tiek sadalītas klasēs. Šajā sadaļā ir aprakstītas programmā Modern POS atbalstītās ierīces un sniegts pārskats par tām.

### <a name="printer"></a>Printeris

Printeri var būt parastie POS kvīšu printeri un veselas lapas printeri. Printeru atbalsts tiek nodrošināts, izmantojot objektu saistīšanu un iegulšanu punktā Retail POS (OPOS) un Microsoft Windows draiveru interfeisus. Vienlaikus var lietot līdz diviem printeriem. Šī iespēja ir piemērota scenārijiem, kuros ar kvīšu printeriem tiek drukātas debitoru kvītis par pārdošanu skaidrā naudā bez piegādes, bet debitoru pasūtījumi, kuros ir ietverts vairāk informācijas, tiek drukāti ar veselas lapas printeri. Kvīšu printerus var tieši pievienot datoram, izmantojot USB portu, pievienot tīklam, izmantojot Ethernet, vai pievienot, izmantojot Bluetooth savienojumu.

### <a name="scanner"></a>Skeneris

Vienlaikus var lietot līdz diviem svītrkoda skeneriem. Šī iespēja ir piemērota scenārijiem, kuros ir nepieciešams vieglāk pārvietojams skeneris, lai skenētu lielas vai smagas preces, bet vairumam standarta izmēra preču tiek izmantots nekustīgs iebūvētais skeneris, lai paātrinātu norēķināšanos. Skeneru atbalstu var nodrošināt, izmantojot OPOS, universālās Windows platformas (UWP) vai svītrkoda/magnētiskās joslas nolasīšanas ierīces interfeisu. Skenera pievienošanai datoram var izmantot USB vai Bluetooth savienojumu.

### <a name="msr"></a>MJL (magnētiskās joslas lasītājs)

Izmantojot OPOS draiverus var iestatīt vienu USB magnētiskās joslas lasītāju (MJL) Ja vēlaties izmantot savrupu MJL elektronisko līdzekļu pārskaitījuma (EFT) maksājumu transakcijām, MJL pārvaldībai ir jāizmanto maksājumu savienotājs. Savrupu MJL var izmantot debitoru lojalitātes programmas datu ievadei, darbinieku pierakstīšanās nodrošināšanai un dāvanu kartes datu ievadei neatkarīgi no maksājumu savienotāja.

### <a name="cash-drawer"></a>Naudas kaste

Katrā aparatūras profilā var tikt atbalstītas līdz divām naudas kastēm. Šī iespēja nodrošina to, ka vienlaikus katrā kases sistēmā var būt pieejamas divas aktīvās darba maiņas. Koplietotas maiņas gadījumā vai tad, ja vairākas mobilās POS ierīces vienlaikus lieto naudas kasti, katrā aparatūras profilā ir atļauts izmantot tikai vienu naudas kasi. Naudas kastes var tieši pievienot datoram, izmantojot USB portu, pievienot tīklam vai pievienot kvīšu printerim, izmantojot RJ12 interfeisu. Dažos gadījumos naudas kastes var arī pievienot, izmantojot Bluetooth savienojumu.

### <a name="line-display"></a>Rindu displejs

Rindu displeji tiek izmantoti, lai debitoram transakcijas laikā parādītu preces, transakciju bilances un citu noderīgu informāciju. Vienu rindu displeju var pievienot datoram, izmantojot USB portu un OPOS draiverus.

### <a name="signature-capture"></a>Paraksta ieguve

Paraksta ieguves ierīces var tieši pievienot datoram, izmantojot USB portu un OPOS draiverus. Ja ir konfigurēta paraksta ieguve, debitoram tiek prasīts parakstīties uz ierīces. Kad paraksts ir nodrošināts, tas tiek parādīts kasierim, lai viņš to apstiprinātu.

### <a name="scale"></a>Mērogs

Svarus var pievienot datoram, izmantojot USP un OPOS draiverus. Ja transakcijai tiek pievienota prece, kas ir atzīmēta kā sverama prece, POS tiek nolasīta svara informācija no svariem, prece tiek pievienota transakcijai un tiek izmantoti no svariem saņemtie daudzuma dati.

### <a name="pin-pad"></a>PIN bloks

Personas identifikācijas numura (PIN) bloku atbalsts tiek nodrošināts, izmantojot OPOS, taču to pārvaldībai ir jāizmanto maksājumu savienotājs.

### <a name="secondary-display"></a>Sekundārais displejs

Ja ir konfigurēts sekundārais displejs, pamatinformācijas rādīšanai tiek izmantots 2. Windows displejs. Sekundārā displeja mērķis ir nodrošināt neatkarīga programmatūras izstrādātāja (NPI) paplašinājuma atbalstu, jo standarta konfigurācijā sekundāro displeju nevar konfigurēt un tajā tiek rādīts ierobežots saturs.

### <a name="payment-device"></a>Maksājumu ierīce

Maksājumu ierīces atbalts tiek nodrošināts, izmantojot maksājumu savienotāju. Maksājumu ierīces var veikt vienu vai daudzas no funkcijām, ko nodrošina citas ierīču klases. Piemēram, maksājumu ierīce var darboties kā MJL/karšu lasītājs, rindu displejs, paraksta ieguves ierīce vai PIN bloks. Maksājumu ierīču atbalsts tiek nodrošināts neatkarīgi no savrupo ierīču atbalsta, kas tiek nodrošināts citām ierīcēm, kuras ir iekļautas aparatūras profilā.

## <a name="supported-interfaces"></a>Atbalstītie interfeisi

### <a name="opos"></a>OPOS

Lai palīdzētu nodrošināt to, ka kopā ar programmu Microsoft Dynamics 365 for Retail var lietot pēc iespējas lielāku ierīču klāstu, galvenā mazumtirdzniecības perifēro ierīču platforma, kas tiek atbalstīta programmā Microsoft Dynamics 365 for Retail, ir nozares standarta platforma OLE punktā POS. Standartu OLE punktā POS ir izstrādājusi organizācija National Retail Federation (NRF), kas ievieš mazumtirdzniecības perifēro ierīču nozares standarta sakaru protokolus. OPOS ir plaši izplatīta standarta OLE punktā POS implementācija. Tā ir izstrādāta 1990. gadu vidū un kopš tā laika ir vairākas reizes atjaunināta. OPOS nodrošina ierīču draiveru arhitektūru, kas sniedz iespēju viegli integrēt POS aparatūru Windows sistēmās. OPOS vadības elementi nodrošina saziņu starp saderīgo aparatūru un POS programmatūru. OPOS vadības elements sastāv no divām tālāk norādītajām daļām.

- **Vadības objekts** — ierīču klases (piemēram, rindu displeju) vadības objekts nodrošina programmatūras interfeisu. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) nodrošina standartizētu OPOS vadības objektu kopu, kas tiek saukta par vispārīgajiem vadības objektiem (CCO). Programmas Microsoft Dynamics 365 for Retail POS komponenta pārbaudei tiek izmantoti CCO objekti. Tādējādi pārbaude palīdz nodrošināt to, ka gadījumā, ja programma Microsoft Dynamics 365 for Retail nodrošina kādas ierīces klases atbalstu, izmantojot OPOS, var tikt nodrošināts daudzu ierīču veidu atbalsts, ja vien ražotājs nodrošina pakalpojumu objektu, kas ir paredzēts standartam OPOS. Nav nepieciešams atsevišķi pārbaudīt katru ierīču veidu.
- **Pakalpojumu objekts** — pakalpojumu objekts nodrošina saziņu starp vadības objektu (C) un ierīci. Parasti ierīces pakalpojumu objektu nodrošina ierīces ražotājs. Taču dažos gadījumos pakalpojumu objektu, iespējams, ir nepieciešams lejupielādēt no ražotāja vietnes. Piemēram, var būt pieejama jaunāka pakalpojumu objekta versija. Lai uzzinātu ražotāja vietnes adresi, skatiet aparatūras dokumentāciju.

[![Vadības objekts un pakalpojumu objekts](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png)

OLE punktā POS OPOS implementācijas atbalsts palīdz nodrošināt to, ka tad, ja ierīču ražotāji un POS publicētāji ir pareizi ieviesuši standartu, POS sistēmas un atbalstītās ierīces var darboties kopā, pat ja tās iepriekš nav pārbaudītas kopā.

> [!NOTE]
> OPOS atbalsts nenodrošina visu to ierīču atbalstu, kurām ir OPOS draiveri. Pirmkārt, programmai Microsoft Dynamics 365 for Retail ir jānodrošina attiecīgā ierīces veida vai klases atbalsts, izmantojot OPOS. Turklāt pakalpojumu objektos dažreiz var nebūt ietverta jaunākā CCO versija. Ņemiet vērā arī to, ka parasti dažādu pakalpojumu objektu kvalitāte atšķiras.

### <a name="windows"></a>Windows

Kvīšu drukāšana POS ir optimizēta standartam OPOS. OPOS parasti nodrošina daudz ātrāku drukāšanu nekā operētājsistēma Windows. Tāpēc ir ieteicams izmantot OPOS, jo īpaši mazumtirdzniecības vidēs, kur tiek drukātas 40 kolonnu kvītis un ir jānodrošina ātra transakciju apstrāde. Vairumam ierīču tiek lietoti OPOS vadības elementi. Taču daži OPOS kvīšu printeri atbalsta arī Windows draiverus. Izmantojot Windows draiveri, varat piekļūt jaunākajiem fontiem un tīklā lietot vienu printeri vairākām kases sistēmām. Taču Windows draiveru lietošanai ir trūkumi. Tālāk ir sniegti daži šo trūkumu piemēri.

- Ja tiek izmantoti Windows draiveri, pirms drukāšanas tiek renderēti attēli. Tāpēc drukāšana ir lēnāka, nekā ar printeriem, kam tiek izmantoti OPOS vadības elementi.
- Ja tiek izmantoti Windows draiveri, ierīces, kas ir pievienotas, izmantojot printeri (ziedlapķēdē), var darboties nepareizi. Piemēram, iespējams, netiks atvērta naudas kaste vai kvīšu printeris nedarbosies, kā ir paredzēts.
- Turklāt OPOS atbalsta plašāku mazumtirdzniecības kvīšu printeriem raksturīgu mainīgo kopu, piemēram, papīra griešanas vai pavadzīmju drukāšanas mainīgos.

Ja izmantotajam Windows printerim ir pieejami OPOS vadības elementi, printerim joprojām ir pareizi jādarbojas kopā ar programmu Microsoft Dynamics 365 for Retail.

### <a name="universal-windows-platform"></a>Universālā Windows platforma

Attiecībā uz mazumtirdzniecības perifērajām ierīcēm: UWP ir saistīta ar Windows Plug and Play ierīču atbalstu. Ja Plug and Play ierīce tiek pievienota operētājsistēmas Windows versijai, ka atbalsta šo ierīču veidu, ierīces pareizai lietošanai nav nepieciešami nekādi draiveri. Piemēram, ja operētājsistēmā Windows tiek noteikts Bluetooth skaļrunis, tiek noteikts, ka ierīces klases veids ir **Skaļrunis**. Tāpēc ierīce tiek apstrādāta kā skaļrunis. Nav nepieciešami nekādi papildu iestatījumi. Var pievienot daudzas USB POS ierīces, un tās operētājsistēmā Windows tiek atpazītas kā cilvēka interfeisa ierīces (HID). Taču operētājsistēmā, iespējams, nevar noteikt ierīces nodrošinātās iespējas, jo nav norādīta ierīces klase vai veids. Operētājsistēmā Windows 10 ir pievienotas svītrkoda skeneru un MJL ierīču klases. Tāpēc, ja operētājsistēmā Windows 10 ierīce tiek noteikta kā ietverta vienā no šīm klasēm, atbilstošajā laikā operētājsistēmā Windows tiek gaidīti notikumi no šīs ierīces. Programma Modern POS atbalsta UWP MJL un skenerus. Tāpēc, kad tā ir gatava ievadei no kādas no šīm ierīcēm un ir pievienota kādā no šīm klasēm ietverta ierīce, šo ierīci var lietot. Piemēram, ja Windows 10 datoram ir pievienots UWP svītrkoda skeneris un programmā Modern POS ir konfigurēta pierakstīšanās ar svītrkodu, pierakstīšanās ekrānā tiek aktivizēts svītrkoda skeneris. Nav nepieciešami nekādi papildu iestatījumi. Operētājsistēmai Windows tiek pievienotas papildu apkalpošanas punkta UWP ierīču klases. Šīs klases ietver naudas kastu un kvīšu printeru klases. Programmā Modern POS vēl nav nodrošināts šo jauno klašu atbalsts.

### <a name="keyboard-wedge"></a>Svītrkoda/magnētiskās joslas nolasīšanas ierīce

Svītrkoda/magnētiskās joslas nolasīšanas ierīces nodrošina datu sūtīšanu uz datoru tā, it kā šie dati būtu ievadīti ar tastatūru. Tāpēc pēc noklusējuma skenētie vai nolasītie dati tiek nosūtīti POS interfeisā aktīvo lauku. Dažos gadījumos šī darbība var izraisīt nepareizā veida datu ieskenēšanu nepareizajā laukā. Piemēram, svītrkods var tikt ieskenēts laikā, kas ir paredzēts kredītkartes datu ievadei. Daudzos gadījumos POS pastāv loģika, kas nosaka, vai skenētie vai nolasītie dati ir svītrkods vai kartes nolasīšanas dati. Tādējādi dati tiek pareizi apstrādāti. Taču, ja ierīces ir iestatītas kā OPOS, nevis kā svītrkoda/magnētiskās joslas nolasīšanas ierīces, ir pieejama plašāka kontrole pār to, kā var izmantot no šīm ierīcēm saņemtos datus, jo ir pieejams vairāk informācijas par ierīci, no kuras ir iegūti dati. Piemēram, no svītrkoda skenera saņemtie dati tiek automātiski atpazīti kā svītrkods, un saistītais ieraksts datu bāzē tiek atrasts ātrāk un vienkāršāk nekā tad, ja tiek izmantota vispārējā virknes meklēšana, kā tas ir svītrkoda/magnētiskās joslas nolasīšanas ierīču gadījumā.

### <a name="native-printer"></a>Vietējais printeris

Vietējos (veida nosaukums aparatūras profilā ir Ierīce) printerus var konfigurēt, lai prasītu lietotājam atlasīt konkrētajam datoram konfigurētu printeri. Ja ir konfigurēts veida **Ierīce** printeris un programmā Modern POS tiek saņemta drukas komanda, lietotajam tiek prasīts sarakstā atlasīt printeri. Šī darbība atšķiras no Windows draiveru darbības, jo, ja tiek izmantots aparatūras profila printera veids **Windows**, netiek rādīts printeru saraksts. Tā vietā laukā **Ierīces nosaukums** ir jānorāda printera nosaukums.

### <a name="windows"></a>Windows

Ierīces veids **Windows** tiek lietots tikai printeriem. Ja aparatūras profilā ir konfigurēts Windows printeris, ir jānorāda konkrētā printera nosaukums. Ja ir konfigurēts Windows printeris un programmā Modern POS tiek saņemts drukas notikums, šis notikums tiek pārsūtīts uz norādīto Windows printeri. Lietotājam netiek prasīts atlasīt printeri.

### <a name="network"></a>Tīkls

Tīklā adresējamas naudas kastes, kvīšu printerus un maksājumu termināļus var izmantot tīklā — vai nu tiešā veidā, izmantojot starpprocesu saziņas (IPC) aparatūras staciju, kas ir iebūvēta programmā Modern POS operētājsistēmai Windows un programmatūrā Modern POS operētājsistēmai Android, vai ar citu Modern POS klientu IIS aparatūras stacijas starpniecību.

## <a name="hardware-station-deployment-options"></a>Aparatūras stacijas izvietošanas iespējas

### <a name="ipc-built-in"></a>IPC (iebūvēta)

Starpprocesu saziņas (IPC) aparatūras stacija ir iebūvēta programmā Modern POS operētājsistēmai Windows un Modern POS operētājsistēmai Android. Lai lietotu IPC aparatūras staciju, piešķiriet aparatūras profilu kases sistēmai, kurā tiks lietota lietojumprogramma Modern POS operētājsistēmai Windows. Pēc tam izveidojiet veida **Atvēlēts** aparatūras staciju veikalam, kurā tiks lietota šī kases sistēma. Kad palaižat programmu Modern POS, ir aktivizēta IPC aparatūras stacija un konfigurētās POS perifērās ierīces ir gatavas lietošanai. Ja kāda iemesla dēļ īslaicīgi nav nepieciešama lokālā aparatūra, izmantojiet operāciju **Pārvaldīt aparatūras stacijas**, lai izslēgtu aparatūras stacijas iespējas. Programmā Modern POS IPC aparatūras staciju var izmantot arī tiešai saziņai ar tīkla perifērajām ierīcēm.

### <a name="iis"></a>IIS

IIS jeb savrupo aparatūras stacijas versiju var izmantot divos veidos. Apzīmējums “IIS” norāda, ka POS programmas savienojumam ar aparatūras staciju tiek izmantoti Microsoft interneta informācijas pakalpojumi. POS lietojumprogrammas savienojumam ar IIS aparatūras staciju tiek izmantoti tīmekļa pakalpojumi, kas darbojas datorā, kuram ir pievienotas ierīces. Ja tiek lietoti IIS, aparatūras stacijai pievienotās mazumtirdzniecības perifērās ierīces var izmantot jebkurā POS kases sistēmā, kas ir vienā tīklā ar IIS aparatūras staciju. Tā kā tikai programma Modern POS operētājsistēmai Windows nodrošina iebūvētu mazumtirdzniecības perifēro ierīču atbalstu, visās citās lietojumprogrammas Modern POS versijās saziņai ar aparatūras profilā konfigurētajām POS perifērajām ierīcēm ir jāizmanto IIS aparatūras stacija. Tāpēc katrai IIS aparatūras stacijas instancei ir nepieciešams dators, kurā darbojas tīmekļa pakalpojums un lietojumprogramma, kas nodrošina saziņu ar ierīcēm. IIS aparatūras stacija ir nepieciešama visām lietojumprogrammas Modern POS versijām, kas nav paredzētas operētājsistēmai Windows.

#### <a name="dedicated"></a>Atvēlēts

Programmā Modern POS veida **Atvēlēts** aparatūras stacijas tiek izmantotas, lai noteiktu perifērās ierīces, kas ir tieši pievienotas datoram, kurā tiek darbināta lietojumprogramma. Taču veidu **Atvēlēts** var izmantot arī IIS aparatūras stacijām. Parasta stacionārā POS scenārijā, kurā tiek izmantota POS lietojumprogramma Cloud POS, aparatūras stacijas veids **Atvēlēts** tiek izmantots IIS aparatūras stacijām, kas ir izvietotas tajā pašā datorā, kurā tiek darbināta programma Cloud POS. Attiecībā uz mazumtirdzniecības perifērajām ierīcēm: atvēlētā IIS aparatūras stacija nodrošina labāku mazumtirdzniecības perifēro ierīču atbalstu parastajā stacionārā POS scenārijos. Atvēlētās aparatūras stacijas nodrošina visu to perifēro ierīču atbalstu, kas tiek atbalstītas aparatūras profilā.

#### <a name="shared"></a>Koplietots

Koplietotās aparatūras stacijas ir paredzētas lietošanai vairākās POS ierīcēs dienas laikā. Koplietotās aparatūras stacijas ir optimizētas, lai nodrošinātu tikai naudas kastu, kvīšu printeri un maksājumu terminālu atbalstu. Nevarat tieši pievienot savrupus svītrkoda skenerus, MJL, rindu displejus, svarus vai citas ierīces. Pretējā gadījumā, ja vairākās POS ierīcēs vienlaikus tiek mēģināts pieprasīt šīs perifērās ierīces, rodas konflikti. Tālāk ir aprakstīts, kā tiek pārvaldīti atbalstīto ierīču konflikti.

- **Naudas kaste** — naudas kaste tiek atvērta, izmantojot uz ierīci nosūtītu notikumu. Vienīgā problēma, kas var rasties naudas kastes izsaukuma laikā, rodas, ja naudas kaste jau ir atvērta. Ja tiek izmantotas koplietotas aparatūras stacijas, naudas kastēm aparatūras profilā ir jāiestata parametrs **Koplietots**. Šis iestatījums nodrošina to, ka brīdī, kad no POS tiek nosūtīta atvēršanas komanda, POS netiek pārbaudīts, vai naudas kaste jau ir atvērta.
- **Kvīšu printeris** — ja uz aparatūras staciju vienlaikus tiek nosūtītas divas kvīts drukāšanas komandas, viena no komandām var tikt zaudēta atkarībā no ierīces. Dažās ierīcēs ir iekšējā atmiņa vai pieprasījumu ierobežošanas līdzeklis, kas var novērst šo problēmu. Ja drukas komanda netiek veiksmīgi izpildīta, kasieris saņem kļūdas ziņojumu un var vēlreiz mēģināt nosūtīt drukas komandu no POS.
- **Maksājumu terminālis** — ja kasieris mēģina veikt norēķinus par transakciju, izmantojot maksājumu termināli, kas jau tiek lietots, kasierim tiek parādīts ziņojums ar norādi, ka terminālis tiek lietots, un aicinājumu vēlāk mēģināt vēlreiz. Parasti kasieri var redzēt, ka terminālis jau tiek lietots, un uzgaida, līdz ir pabeigta otra transakcija, pirms vēlreiz mēģina veikt norēķinus.

Kādā no nākamajiem laidieniem ir paredzēts ietvert validācijas līdzekli, lai noteiktu, vai ar aparatūras staciju kartētajam aparatūras profilam ir iestatītas neatbalstītas ierīces. Ja tiek noteikta kāda neatbalstīta ierīce, lietotājs saņem ziņojumu par to, ka ierīces netiek atbalstītas lietošanai ar koplietotām aparatūras stacijām. Ja tiek izmantotas koplietotas aparatūras stacijas, kases sistēmas līmenī ir iestatīta opcijas **Atlasīt norēķinu brīdī** vērtība **Jā**. Šādā gadījumā, kad POS tiek atlasīti transakcijas norēķini, POS lietotājam tiek prasīts atlasīt aparatūras staciju. Ja aparatūras stacija tiek atlasīta tikai norēķinu laikā, aparatūras stacijas atlase tiek tieši pievienota mobilo scenāriju POS darbplūsmai. Papildu ieguvums ir tas, ka koplietošanas scenārijos netiek lietots maksājumu termināļa rindu displejs. Ja maksājumu terminālis tiek izmantots kā rindu displejs, citiem lietotājiem var tikt liegta iespēja izmantot šo termināli, līdz tiek pabeigta transakcija. Mobilajos scenārijos transakcijas rindas var tikt pievienotas ilgākā laika periodā. Tāpēc ir nepieciešama opcija **Atlasīt norēķinu brīdī**, lai nodrošinātu optimālu ierīces pieejamību.

### <a name="network-peripherals"></a>Tīkla perifērās ierīces

Ierīču tīkla apzīmējums aparatūras profilā sniedz iespēju izveidot naudas kastu, kvīšu printeru un maksājumu termināļu tīkla savienojumu.

#### <a name="modern-pos-for-windows"></a>Modern POS operētājsistēmai Windows

Tīkla perifēro ierīču IP adreses varat norādīt divās vietās. Ja Modern POS Windows klientā tiek izmantota viena tīkla perifēro ierīču kopa, šo ierīču IP adreses ir jāiestata, izmantojot kases sistēmas darbību rūts opciju **IP konfigurēšana**. Ja tīkla ierīces tiks koplietotas vairākās POS kases sistēmās, aparatūras profilu, kam ir piešķirta tīkla ierīce, var tieši kartēt ar koplietotu aparatūras staciju. Lai piešķirtu IP adreses, atlasiet aparatūras staciju lapā **Mazumtirdzniecības veikali** un pēc tam sadaļas **Aparatūras stacijas** laukā **IP konfigurēšana** norādiet tīkla ierīces, kas ir piešķirtas šai aparatūras stacijai. Ja aparatūras stacijai ir piešķirtas tikai tīkla ierīces, šī aparatūras stacija nav jāizvieto. Šādā gadījumā aparatūras stacija ir nepieciešama tikai tīklā adresējamo ierīču konceptuālai grupēšanai atbilstoši to atrašanās vietai mazumtirdzniecības veikalā.

#### <a name="modern-pos-for-android"></a>Modern POS operētājsistēmai Android

Sākot ar Dynamics 365 for Retail versiju 8.1.3, programma Modern POS operētājsistēmai Android ietver iebūvētu IPC aparatūras staciju. Šī aparatūras stacija atbalsta saziņu ar tīkla printeriem un maksājumu savienotājiem. Lai iegūtu plašāku informāciju, apmeklējiet rakstu [Hybrid programma operētājsistēmai Android](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/hybridapp#dedicated-hardware-station-support-for-the-hybrid-android-app). 

#### <a name="cloud-pos-and-modern-pos-for-ios"></a>Cloud POS un Modern POS operētājsistēmai iOS

Loģika, kas nodrošina fiziski pievienoto un tīklā adresējamo perifēro ierīču darbību, ir ietverta aparatūras stacijā. Tāpēc visiem POS klientiem, izņemot programmu Modern POS operētājsistēmai Windows, ir jāizvieto un jāaktivizē IIS aparatūras stacija, lai nodrošinātu POS saziņu ar perifērajām ierīcēm, neatkarīgi no tā, vai šīs perifērās ierīces ir fiziski savienotas ar aparatūras staciju vai adresētas tīklā.

## <a name="setup-and-configuration"></a>Iestatīšana un konfigurēšana

### <a name="hardware-station-installation"></a>Aparatūras stacijas instalēšana

Informāciju skatiet tēmā [Retail hardware station konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Modern POS operētājsistēmai Windows iestatīšana un konfigurēšana

Informāciju skatiet rakstā [Retail Modern POS konfigurēšana un instalēšana](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS ierīces iestatīšana un konfigurēšana

Papildinformāciju par OPOS komponentiem skatiet šī dokumenta sadaļā “Atbalstītie interfeisi”. Parasti OPOS draiverus nodrošina ierīces ražotājs. Instalējot OPOS ierīces draiveri, kādā no tālāk norādītajām vietām Windows reģistrā tiek pievienota atslēga.

- **32 bitu sistēma:** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS
- **64 bitu sistēma:** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

Reģistra atrašanās vietā ServiceOPOS konfigurētās ierīces ir sakārtotas atbilstoši OPOS ierīču klasei. Tiek saglabāti vairāki ierīču draiveri.

## <a name="supported-scenarios-by-hardware-station-type"></a>Atbalstītie scenāriji pēc aparatūras stacijas veida

### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Klienta atbalsts — IPC aparatūras stacijas un IIS aparatūras stacijas salīdzinājums

Tālāk esošajā tabulā ir norādītas atbalstītās topoloģijas un izvietošanas scenāriji.

| Klients      | IPC aparatūras stacija | IIS aparatūras stacija |
|-------------|----------------------|----------------------|
| Windows programma | Jā                  | Jā                  |
| Cloud POS   | Nē                   | Jā                  |
| Android     | Jā                  | Jā                  |
| iOS         | Nē                   | Jā                  |

### <a name="network-peripherals"></a>Tīkla perifērās ierīces

Tīkla perifērajām ierīcēm var nodrošināt tiešu atbalstu, izmantojot lietojumprogrammā Modern POS operētājsistēmai Windows iebūvēto aparatūras staciju. Visiem citiem klientiem ir jāizvieto IIS aparatūras stacija.

| Klients      | IPC aparatūras stacija | IIS aparatūras stacija |
|-------------|----------------------|----------------------|
| Windows programma | Jā                  | Jā                  |
| Cloud POS   | Nē                   | Jā                  |
| Android     | Jā                  | Jā                  |
| iOS         | Nē                   | Jā                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Atbalstītie ierīču veidi pēc aparatūras stacijas veida

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS operētājsistēmai Windows ar IPC (iebūvētu) aparatūras staciju

<table>
<thead>
<tr>
<th>Atbalstītā ierīču klase</th>
<th>Atbalstītie interfeisi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Printeris</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows draiveris</li>
<li>Ierīce</li>
<li>Tīkls</li>
</ul>
</td>
</tr>
<tr>
<td>2. printeris</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows draiveris</li>
<li>Ierīce</li>
<li>Tīkls</li>
</ul>
</td>
</tr>
<tr>
<td>Rindu displejs</td>
<td>OPOS</td>
</tr>
<tr>
<td>Duālais displejs</td>
<td>Windows draiveris</td>
</tr>
<tr>
<td>MJL (magnētiskās joslas lasītājs)</td>
<td>
<ul>
<li>OPOS</li>
<li>UWP (Nav nepieciešama iestatīšana.)</li>
<li>Svītrkoda/magnētiskās joslas nolasīšanas ierīce (Nav nepieciešama iestatīšana.)</li>
</ul>
</td>
</tr>
<tr>
<td>Naudas kaste</td>
<td>
<ul>
<li>OPOS</li>
<li>Tīkls
<p><strong>Piezīme.</strong> Ja naudas kastei ir konfigurēta opcija <strong>Lietot koplietoto maiņu</strong>, var iestatīt tikai vienu naudas kasti.</p>
</li>
</ul>
</td>
</tr>
<tr>
<td>2. dokumenta sastādītājs</td>
<td>
<ul>
<li>OPOS</li>
<li>Tīkls
<p><strong>Piezīme.</strong> Ja naudas kastei ir konfigurēta opcija <strong>Lietot koplietoto maiņu</strong>, var iestatīt tikai vienu naudas kasti.</p>
</li>
</ul>
</td>
</tr>
<tr>
<td>Skeneris</td>
<td>
<ul>
<li>OPOS</li>
<li>UWP (Nav nepieciešama iestatīšana.)</li>
<li>Svītrkoda/magnētiskās joslas nolasīšanas ierīce (Nav nepieciešama iestatīšana.)</li>
</ul>
</td>
</tr>
<tr>
<td>2. skeneris</td>
<td>
<ul>
<li>OPOS</li>
<li>UWP (Nav nepieciešama iestatīšana.)</li>
<li>Svītrkoda/magnētiskās joslas nolasīšanas ierīce (Nav nepieciešama iestatīšana.)</li>
</ul>
</td>
</tr>
<tr>
<td>Mērogs</td>
<td>OPOS</td>
</tr>
<tr>
<td>PIN bloks</td>
<td>OPOS (Atbalsts tiek nodrošināts, pielāgojot maksājumu savienotāju.)</td>
</tr>
<tr>
<td>Paraksta ieguve</td>
<td>OPOS</td>
</tr>
<tr>
<td>Maksājumu terminālis</td>
<td>
<ul>
<li>Pielāgotu ierīču atbalsts</li>
<li>Tīkls (Papildinformāciju skatiet maksājumu savienotāja dokumentācijā.)</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Visi Modern POS klienti, kam ir atvēlēta IIS aparatūras stacija

> [!NOTE]
> Ja IIS aparatūras stacija ir atvēlēta, pastāv relācija viens pret vienu starp POS klientu un aparatūras staciju.

<table>
<thead>
<tr>
<th>Atbalstītā ierīču klase</th>
<th>Atbalstītie interfeisi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Printeris</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows draiveris
<p><strong>Piezīme.</strong> Attiecībā uz Windows printeriem tīklā: aparatūras stacijas lietotājam ir jābūt piešķirtai atļaujai piekļūt printerim.</p>
</li>
<li>Tīkls</li>
</ul>
</td>
</tr>
<tr>
<td>2. printeris</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows draiveris</li>
<li>Tīkls</li>
</ul>
</td>
</tr>
<tr>
<td>Rindu displejs</td>
<td>OPOS</td>
</tr>
<tr>
<td>MJL (magnētiskās joslas lasītājs)</td>
<td>OPOS</td>
</tr>
<tr>
<td>Naudas kaste</td>
<td>
<ul>
<li>OPOS</li>
<li>Tīkls
<p><strong>Piezīme.</strong> Ja naudas kastei ir konfigurēta opcija <strong>Lietot koplietoto maiņu</strong>, katrā aparatūras profilā var iestatīt tikai vienu naudas kasti.</p>
</li>
</ul>
</td>
</tr>
<tr>
<td>2. dokumenta sastādītājs</td>
<td>
<ul>
<li>OPOS</li>
<li>Tīkls</li>
</ul>
</td>
</tr>
<tr>
<td>Skeneris</td>
<td>OPOS</td>
</tr>
<tr>
<td>2. skeneris</td>
<td>OPOS</td>
</tr>
<tr>
<td>Mērogs</td>
<td>OPOS</td>
</tr>
<tr>
<td>PIN bloks</td>
<td>OPOS (Atbalsts tiek nodrošināts, pielāgojot maksājumu savienotāju.)</td>
</tr>
<tr>
<td>Paraksta ieguve</td>
<td>OPOS</td>
</tr>
<tr>
<td>Maksājumu terminālis</td>
<td>
<ul>
<li>Pielāgotu ierīču atbalsts</li>
<li>Tīkls (Papildinformāciju skatiet maksājumu savienotāja dokumentācijā.)</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Visi Modern POS klienti, kam ir koplietota IIS aparatūras stacija

> [!NOTE]
> Ja IIS aparatūras stacija ir koplietota, aparatūras stacija var tikt vienlaikus lietota vairākās ierīcēs. Šādā gadījumā drīkst lietot tikai ierīces, kas ir norādītas tālāk esošajā tabulā. Ja mēģināsit koplietot ierīces, kas nav norādītas šajā tabulā, piemēram, svītrkoda skenerus un MJL, kad vairākās ierīcēs tiks mēģināts pieprasīt vienu perifērijas ierīci, radīsies kļūdas. Turpmāk šāda konfigurācija netiks pieļauta.

<table>
<thead>
<tr>
<th>Atbalstītā ierīču klase</th>
<th>Atbalstītie interfeisi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Printeris</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows draiveris
<p><strong>Piezīme.</strong> Attiecībā uz Windows printeriem tīklā: aparatūras stacijas lietotājam ir jābūt piešķirtai atļaujai piekļūt printerim.</p>
</li>
<li>Tīkls</li>
</ul>
</td>
</tr>
<tr>
<td>2. printeris</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows draiveris</li>
<li>Tīkls</li>
</ul>
</td>
</tr>
<tr>
<td>Naudas kaste</td>
<td>
<ul>
<li>OPOS</li>
<li>Tīkls
<p><strong>Piezīme.</strong> Ja naudas kastei ir konfigurēta opcija <strong>Lietot koplietoto maiņu</strong>, katrā aparatūras profilā var iestatīt tikai vienu naudas kasti.</p>
</li>
</ul>
</td>
</tr>
<tr>
<td>2. dokumenta sastādītājs</td>
<td>
<ul>
<li>OPOS</li>
<li>Tīkls</li>
</ul>
</td>
</tr>
<tr>
<td>Maksājumu terminālis</td>
<td>
<ul>
<li>Pielāgotu ierīču atbalsts</li>
<li>Tīkls (Papildinformāciju skatiet maksājumu savienotāja dokumentācijā.)</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Atbalstīto scenāriju konfigurācija

Papildinformāciju par to, kā izveidot aparatūras profilus, skatiet tēmā [Kanāla klientu, tostarp kases sistēmu un aparatūras staciju, definēšana un uzturēšana](define-maintain-channel-clients-registers-hw-stations.md).

> [!NOTE]
> Attiecībā uz Microsoft Dynamics 365 for Retail versiju 1611: vairs netiek lietots aparatūras staciju profils. Atribūti, kas iepriekš bija jāiestata aparatūras stacijas profilā, tagad ir ietverti pašā aparatūras stacijā.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS operētājsistēmai Windows ar IPC (iebūvētu) aparatūras staciju

Šī konfigurācija visbiežāk tiek lietota parasto stacionāro POS kases sistēmām. Šajā scenārijā aparatūras profila informācija tiek tieši kartēta ar kases sistēmu. Arī EFT termināļa numurs ir jāiestata kases sistēmā. Lai iestatītu šo konfigurāciju, veiciet tālāk norādītās darbības.

1. Izveidojiet aparatūras profilu, kurā ir konfigurētas visas nepieciešamās perifērās ierīces.
2. Kartējiet aparatūras profilu ar POS kases sistēmu.
3. Izveidojiet veida **Atvēlēts** aparatūras staciju mazumtirdzniecības veikalam, kurā tiks lietota šī POS kases sistēma. Pēc izvēles ievadiet aprakstu.

    > [!NOTE]
    > Nav nepieciešams iestatīt nekādus citus aparatūras stacijas rekvizītus. Visa pārējā nepieciešama informācija, piemēram, aparatūras profils, tiks saņemta no kases sistēmas.

4. Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiks**.
5. Atlasiet sadales grafiku **1090**, lai jauno aparatūras profilu sinhronizētu ar veikalu. Noklikšķiniet uz **Izpildīt tūlīt**, lai sinhronizētu izmaiņas ar POS.
6. Atlasiet sadales grafiku **1070**, lai jauno aparatūras staciju sinhronizētu ar veikalu. Noklikšķiniet uz **Izpildīt tūlīt**, lai sinhronizētu izmaiņas ar POS.
7. Instalējiet un aktivizējiet programmu Modern POS operētājsistēmai Windows.
8. Palaidiet programmu Modern POS operētājsistēmai Windows un sāciet lietot pievienotās perifērās ierīces.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Visi Modern POS klienti, kam ir atvēlēta IIS aparatūras stacija

Šo konfigurāciju var lietot visiem Modern POS klientiem, kam ir aparatūras stacija, kura tiek lietota tikai vienā POS kases sistēmā. Lai iestatītu šo konfigurāciju, veiciet tālāk norādītās darbības.

1. Izveidojiet aparatūras profilu, kurā ir konfigurētas visas nepieciešamās perifērās ierīces.
2. Izveidojiet veida **Atvēlēts** aparatūras staciju mazumtirdzniecības veikalam, kurā tiks lietota šī POS kases sistēma.
3. Atvēlētajā aparatūras stacijā iestatiet tālāk norādītos rekvizītus.

    - **Resursdatora nosaukums** — tā resursdatora nosaukums, kurā tiks darbināta aparatūras stacija.

        > [!NOTE]
        > Programma Cloud POS var atrisināt **localhost**, lai noteiktu lokālo datoru, kurā tiek darbināta programma Cloud POS. Taču arī sertifikātā, kas ir nepieciešams, lai programmu Cloud POS savienotu pārī ar aparatūras staciju, ir jābūt norādītam datora nosaukumam “Localhost”. Lai nepieļautu problēmas, ir ieteicams veikalam norādīt katras atvēlētās aparatūras stacijas instanci, ja tas ir nepieciešams. Katras aparatūras stacijas resursdatora nosaukumam ir jābūt vienādam ar tā konkrētā datora nosaukumu, kurā tiks izvietota aparatūras stacija.

    - **Ports** — ports, kas ir jāizmanto aparatūras stacijas saziņai ar Modern POS klientu.
    - **Aparatūras profils** — ja aparatūras stacijā nav nodrošināts aparatūras profils, tiek lietots kases sistēmai piešķirtais aparatūras profils.
    - **EFT POS numurs** — EFT termināļa ID, kas ir jāizmanto, nosūtot EFT autorizācijas datus. Šo ID nodrošina kredītkaršu procesors.
    - **Pakotnes nosaukums** — aparatūras stacijas pakotne, kas ir jāizmanto, izvietojot aparatūras staciju.

4. Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiks**.
5. Atlasiet sadales grafiku **1090**, lai jauno aparatūras profilu sinhronizētu ar veikalu. Noklikšķiniet uz **Izpildīt tūlīt**, lai sinhronizētu izmaiņas ar POS.
6. Atlasiet sadales grafiku **1040**, lai jauno aparatūras staciju sinhronizētu ar veikalu. Noklikšķiniet uz **Izpildīt tūlīt**, lai sinhronizētu izmaiņas ar POS.
7. Instalējiet aparatūras staciju. Papildinformāciju par to, kā instalēt aparatūras staciju, skatiet tēmā [Retail hardware station konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md).
8. Instalējiet un aktivizējiet programmu Modern POS. Papildinformāciju par to, kā instalēt programmu Modern POS, skatiet rakstā [Retail Modern POS konfigurēšana un instalēšana](retail-modern-pos-device-activation.md).
9. Pierakstieties programmā Modern POS un atlasiet vienumu **Veikt operācijas bez naudas kastes**.
10. Sāciet operāciju **Pārvaldīt aparatūras stacijas**.
11. Noklikšķiniet uz **Pārvaldīt**.
12. Aparatūras stacijas pārvaldības lapā iestatiet attiecīgo opciju, lai ieslēgtu aparatūras staciju.
13. Atlasiet izmantojamo aparatūras staciju un pēc tam noklikšķiniet uz **Savienot pārī**.
14. Kad aparatūras stacija ir savienota pārī, noklikšķiniet uz **Aizvērt**.
15. Aparatūras stacijas atlases lapā noklikšķiniet uz nesen atlasītās aparatūras stacijas, lai to aktivizētu.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Visi Modern POS klienti, kam ir koplietota IIS aparatūras stacija

Šo konfigurāciju var lietot visiem Modern POS klientiem, kuros aparatūras stacijas tiek koplietotas ar citām ierīcēm. Lai iestatītu šo konfigurāciju, veiciet tālāk norādītās darbības.

1. Izveidojiet aparatūras profilu, kurā ir konfigurētas nepieciešamās perifērās ierīces.
2. Izveidojiet veida **Koplietots** aparatūras staciju mazumtirdzniecības veikalam, kurā tiks lietota šī POS kases sistēma.
3. Koplietotajā aparatūras stacijā iestatiet tālāk norādītos rekvizītus.

    - **Resursdatora nosaukums** — tā resursdatora nosaukums, kurā tiks darbināta aparatūras stacija.
    - **Apraksts** — teksts, kas palīdz identificēt aparatūras staciju, piemēram, **Atgriešanas darbības** vai **Veikala lete**.
    - **Ports** — ports, kas ir jāizmanto aparatūras stacijas saziņai ar Modern POS klientu.
    - **Aparatūras profils** — katrai koplietotajai aparatūras stacijai ir nepieciešams aparatūras profils. Aparatūras profilus var koplietot vairākās aparatūras stacijās, taču tiem ir jābūt kartētiem ar katru aparatūras staciju. Turklāt ir ieteicams izmantot koplietotas darba maiņas, ja vairākās ierīcēs tiek lietota viena un tā pati aparatūras stacija. Lai iestatītu koplietotu darba maiņu, noklikšķiniet uz **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profili** &gt; **Aparatūras profili**. Katram koplietotajam aparatūras profilam atlasiet naudas kasti un iestatiet opcijas **Koplietojama maiņas naudas kaste** vērtību **Jā**.
    - **EFT POS numurs** — EFT termināļa ID, kas ir jāizmanto, nosūtot EFT autorizācijas datus. Šo ID nodrošina kredītkaršu procesors.
    - **Pakotnes nosaukums** — aparatūras stacijas pakotne, kas ir jāizmanto, izvietojot aparatūras staciju.

4. Atkārtojiet 2. un 3. darbību ar katru papildu aparatūras staciju, kas ir nepieciešama veikalā.
5. Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiks**.
6. Atlasiet sadales grafiku **1090**, lai jauno aparatūras profilu sinhronizētu ar veikalu. Noklikšķiniet uz **Izpildīt tūlīt**, lai sinhronizētu izmaiņas ar POS.
7. Atlasiet sadales grafiku **1040**, lai jauno aparatūras staciju sinhronizētu ar veikalu. Noklikšķiniet uz **Izpildīt tūlīt**, lai sinhronizētu izmaiņas ar POS.
8. Instalējiet aparatūras staciju katrā resursdatorā, ko iestatījāt, veicot 2. un 3. darbību. Papildinformāciju par to, kā instalēt aparatūras staciju, skatiet tēmā [Retail hardware station konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md).
9. Instalējiet un aktivizējiet programmu Modern POS. Papildinformāciju par to, kā instalēt programmu Modern POS, skatiet rakstā [Retail Modern POS konfigurēšana un instalēšana](retail-modern-pos-device-activation.md).
10. Pierakstieties programmā Modern POS un atlasiet vienumu **Veikt operācijas bez naudas kastes**.
11. Sāciet operāciju **Pārvaldīt aparatūras stacijas**.
12. Noklikšķiniet uz **Pārvaldīt**.
13. Aparatūras stacijas pārvaldības lapā iestatiet attiecīgo opciju, lai ieslēgtu aparatūras staciju.
14. Atlasiet izmantojamo aparatūras staciju un pēc tam noklikšķiniet uz **Savienot pārī**.
15. Atkārtojiet 14. darbību ar katru aparatūras staciju, kas tiks lietota programmā Modern POS.
16. Kad visas nepieciešamās aparatūras stacijas ir savienotas pārī, noklikšķiniet uz **Aizvērt**.
17. Aparatūras stacijas atlases lapā noklikšķiniet uz nesen atlasītās aparatūras stacijas, lai to aktivizētu.

    > [!NOTE]
    > Ja ierīcēs bieži tiek lietotas dažādas aparatūras stacijas, ir ieteicams konfigurēt programmu Modern POS tā, lai, sākot norēķinu procesu, kasierim tiktu prasīts atlasīt aparatūras staciju. Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **Reģistri**. Atlasiet kases sistēmu un pēc tam iestatiet opcijas **Atlasīt norēķinu brīdī** vērtību **Jā**. Izmantojiet sadales grafiku **1090**, lai sinhronizētu izmaiņas ar kanālu datu bāzi.

## <a name="extensibility"></a>Paplašināmība

Informāciju par aparatūras stacijas paplašināmības scenārijiem skatiet tēmā [Aparatūras stacijas paplašināmība](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Drošība

Saskaņā ar pašreizējiem drošības standartiem, ražošanas vidē ir jāizmanto tālāk norādītie iestatījumi.

> [!NOTE]
> Aparatūras stacijas instalēšanas programma automātiski veic šos reģistra labojumus instalācijas pašapkalpošanās ietvaros.

- Ir jāatspējo drošligzdu slāņa (SSL) protokols.
- Drīkst būt iespējota un tikt lietota tikai transporta slāņa drošības (TLS) protokola versija 1.2 (vai jaunākā pašlaik pieejamā versija).

    > [!NOTE]
    > Pēc noklusējuma ir atspējots SSL protokols un visas TLS protokola versijas, izņemot TLS 1.2.

    Lai rediģētu vai iespējotu šīs vērtības, veiciet tālāk norādītās darbības.

    1. Nospiediet taustiņu kombināciju Windows logotipa taustiņš+R, lai atvērtu logu **Izpildīt**.
    2. Laukā **Atvērt** ievadiet **Regedit** un pēc tam noklikšķiniet uz **Labi**.
    3. Ja tiek parādīts ziņojuma lodziņš **Lietotāja konta kontrole** noklikšķiniet uz **Jā**.
    4. Logā **Reģistra redaktors** pārejiet uz ierakstu **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Ir automātiski ievadītas tālāk norādītās atslēgas, lai atļautu tikai TLS 1.2 lietošanu.

        - TLS 1.2Server:Enabled=1
        - TLS 1.2Server:DisabledByDefault=0
        - TLS 1.2Client:Enabled=1
        - TLS 1.2Client:DisabledByDefault=0
        - TLS 1.1Server:Enabled=0
        - TLS 1.1Client:Enabled=0
        - TLS 1.0Server:Enabled=0
        - TLS 1.0Client:Enabled=0
        - SSL 3.0Server:Enabled=0
        - SSL 3.0Client:Enabled=0
        - SSL 2.0Server:Enabled=0
        - SSL 2.0Client:Enabled=0

- Nedrīkst būt atvērti nekādi papildu tīkla porti, ja vien tie nav nepieciešami zināmiem, norādītiem iemesliem.
- Ir jāatspējo krusteniskās izcelsmes resursu koplietošana, un ir jānorāda atļautās izcelsmes, kas tiek pieņemtas.
- Lai iegūtu sertifikātus, kas tiks izmantoti datoros, kuros tiek darbināta aparatūras stacija, drīkst izmantot tikai uzticamas sertificēšanas iestādes.

> [!NOTE]
> Ir ļoti svarīgi pārskatīt IIS drošības vadlīnijas un maksājumu karšu nozares (PCI) prasības.

## <a name="peripheral-simulator"></a>Perifērijas simulators

Informāciju skatiet tēmā [Mazumtirdzniecības perifēro ierīču simulators](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>Korporācijas Microsoft pārbaudītas perifērijas ierīces

### <a name="ipc-built-in-hardware-station"></a>IPC (iebūvētā) aparatūras stacija

Tālāk norādītās perifērās ierīces ir pārbaudītas, izmantojot IPC aparatūras staciju, kas ir iebūvēta programmā Modern POS operētājsistēmai Windows.

#### <a name="printer"></a>Printeris

| Ražotājs | Modelis      | Interfeiss | Komentāri                |
|--------------|------------|-----------|-------------------------|
| Epson        | Tm-T88IV   | OPOS      |                         |
| Epson        | TM-T88V    | OPOS      |                         |
| Epson        | ePOS-Print | Pielāgots    | Tīkla savienojums   |
| Star         | TSP650II   | OPOS      |                         |
| Star         | TSP650II   | Pielāgots    | Tīkla savienojums   |
| Star         | mPOP       | OPOS      | Bluetooth savienojums |
| HP           | F7M67AA    | OPOS      | USB barošana             |

#### <a name="bar-code-scanner"></a>Svītrkoda skeneris

| Ražotājs  | Modelis         | Interfeiss | Komentāri |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Simbols        | LS2208        | OPOS      |          |
| HP Integrated | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>PIN bloks

| Ražotājs | Modelis  | Interfeiss | Komentāri                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Nepieciešama maksājumu savienojuma pielāgošana |

#### <a name="payment-terminal"></a>Maksājumu terminālis

| Ražotājs | Modelis        | Interfeiss | Komentāri                                                                       |
|--------------|--------------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300        | Pielāgots    | Nepieciešama maksājumu savienojuma pielāgošana                                |
| VeriFone     | MX925        | Pielāgots    | Nepieciešama maksājumu savienojuma pielāgošana; tīkla un USB savienojums |
| VeriFone     | MX915        | Pielāgots    | Nepieciešama maksājumu savienojuma pielāgošana; tīkla un USB savienojums |
| Verifone     | Skatiet komentārus | Adyen     | Adyen savienotājs atbalsta visas ierīces, kas ir norādītas [šeit](https://www.adyen.com/pos-payments/terminals) |

#### <a name="cash-drawer"></a>Naudas kaste

| Izgatavotājs | Modelis     | Interfeiss | Komentāri                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Bluetooth savienojums |
| APG          | Atwood    | Pielāgots    | Tīkla savienojums   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>Rindu displejs

| Ražotājs  | Modelis   | Interfeiss | Komentāri |
|---------------|---------|-----------|----------|
| HP integrated | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Paraksta ieguve

| Ražotājs | Modelis  | Interfeiss | Komentāri |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Mērogs

| Ražotājs | Modelis         | Interfeiss | Komentāri |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MJL (magnētiskās joslas lasītājs)

| Ražotājs | Modelis       | Interfeiss | Komentāri |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Atvēlēta IIS aparatūras stacija

Tālāk norādītās perifērās ierīces ir pārbaudītas, izmantojot atvēlētu (nekoplietotu) IIS aparatūras staciju kopā ar programmām Modern POS operētājsistēmai Windows un Cloud POS.

#### <a name="printer"></a>Printeris

| Ražotājs | Modelis    | Interfeiss | Komentāri                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Pielāgots    | Tīkla savienojums     |
| HP           | F7M67AA  | OPOS      | USB barošana               |

#### <a name="bar-code-scanner"></a>Svītrkoda skeneris

| Ražotājs  | Modelis   | Interfeiss | Komentāri |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| Simbols        | LS2208  | OPOS      |          |
| HP Integrated | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>PIN bloks

| Ražotājs | Modelis  | Interfeiss | Komentāri                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Nepieciešama maksājumu savienojuma pielāgošana |

#### <a name="payment-terminal"></a>Maksājumu terminālis

| Ražotājs | Modelis | Interfeiss | Komentāri                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Pielāgots    | Nepieciešama maksājumu savienojuma pielāgošana                                |
| VeriFone     | MX925 | Pielāgots    | Nepieciešama maksājumu savienojuma pielāgošana; tīkla un USB savienojums |
| VeriFone     | MX915 | Pielāgots    | Nepieciešama maksājumu savienojuma pielāgošana; tīkla un USB savienojums |

#### <a name="cash-drawer"></a>Naudas kaste

| Ražotājs | Modelis     | Interfeiss | Komentāri              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Pielāgots    | Tīkla savienojums |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>Rindu displejs

| Ražotājs  | Modelis   | Interfeiss | Komentāri |
|---------------|---------|-----------|----------|
| HP integrated | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Paraksta ieguve

| Ražotājs | Modelis  | Interfeiss | Komentāri |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Mērogs

| Ražotājs | Modelis         | Interfeiss | Komentāri |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MJL (magnētiskās joslas lasītājs)

| Ražotājs | Modelis       | Interfeiss | Komentāri |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Koplietota IIS aparatūras stacija

Tālāk norādītās perifērās ierīces ir pārbaudītas, izmantojot koplietotu IIS aparatūras staciju kopā ar programmām Modern POS operētājsistēmai Windows un Cloud POS.

> [!NOTE]
> Tiek atbalstīts tikai printeris, maksājumu terminālis un naudas kaste.

#### <a name="printer"></a>Printeris

| Ražotājs | Modelis    | Interfeiss | Komentāri                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Pielāgots    | Tīkla savienojums     |
| HP           | F7M67AA  | OPOS      | USB barošana               |

#### <a name="payment-terminal"></a>Maksājumu terminālis

| Ražotājs | Modelis | Interfeiss | Komentāri                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Pielāgots    | Nepieciešama maksājumu savienojuma pielāgošana; tīkla un USB savienojums |
| VeriFone     | MX915 | Pielāgots    | Nepieciešama maksājumu savienojuma pielāgošana; tīkla un USB savienojums |

#### <a name="cash-drawer"></a>Naudas kaste

| Ražotājs | Modelis     | Interfeiss | Komentāri              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Pielāgots    | Tīkla savienojums |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>Problēmu novēršana

### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Programma Modern POS var nodrošināt aparatūras stacijas noteikšanu atlases sarakstā, taču nevar nodrošināt savienošanu pārī

**Risinājums:** pārbaudiet tālāk sniegto iespējamo kļūmju sarakstu.

- Sertifikāts, kas tiek izmantots datorā, kurā tiek darbināta aparatūras stacija, ir iestatīts kā uzticams datorā, kurā tiek darbināta programma Modern POS.

    - Lai pārbaudītu šo iestatījumu, tīmekļa pārlūkprogrammā dodieties uz šādu vietrādi URL: `https://<Computer Name>:<Port Number>/HardwareStation/ping`.
    - Šis URL izmanto programmu Ping, lai pārbaudītu, vai datoram var piekļūt, un pārlūkprogramma norāda, vai sertifikāts ir uzticams. (Piemēram, pārlūkprogrammā Internet Explorer adreses joslā tiek parādīta slēdzenes ikona. Kad noklikšķināt uz šīs ikona, pārlūkprogramma Internet Explorer pārbauda, vai sertifikāts pašlaik ir uzticams. Varat instalēt sertifikātu lokālajā datorā, skatot detalizētu informāciju par parādīto sertifikātu.)

- Datorā, kurā tiek darbināta aparatūras stacija, ugunsmūrī ir atvērts ports, kas tiks izmantots aparatūras stacijas darbībai.
- Aparatūras stacijā ir pareizi instalēta tirgotāja informācija, izmantojot rīku Instalēt tirgotāja informāciju, kas tiek palaists aparatūras stacijas instalēšanas programmas darbības beigās.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Programma Modern POS nevar nodrošināt aparatūras stacijas noteikšanu atlases sarakstā

**Risinājums:** šo problēmu var izraisīt jebkurš no tālāk norādītajiem faktoriem.

- Aparatūras stacija nav pareizi iestatīta galvenajā birojā. Izmantojiet iepriekš šajā tēmā norādītās darbības, lai pārbaudītu, vai aparatūras stacijas profils un aparatūras stacija ir pareizi ievadīti.
- Nav palaisti darbi, lai atjauninātu kanāla konfigurāciju. Šādā gadījumā palaidiet kanāla konfigurācijas darbu Nr. 1070.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Programmā Modern POS nav atainoti jaunie naudas kastes iestatījumi

**Risinājums:** slēdziet pašreizējo partiju. Naudas kastes izmaiņas netiek atjauninātas programmā Modern POS, līdz tiek slēgta pašreizējā partija.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Programmā Modern POS tiek ziņots problēmu ar mazumtirdzniecības perifēro ierīci

**Risinājums:** tālāk ir norādīti daži izplatītākie gadījumi, kad rodas šī problēma.

- Pārliecinieties, ka ir aizvērtas citas ierīču draiveru konfigurēšanas utilītas. Ja šīs utilītas ir atvērtas, tās var traucēt ierīces pieprasīšanu programmā Modern POS vai aparatūras stacijā.
- Ja mazumtirdzniecības perifērā ierīce tiek koplietota vairākās POS ierīcēs, pārliecinieties, ka tā ir ietverta vienā no tālāk norādītajām kategorijām.

    - Naudas kaste
    - Kvīšu printeris
    - Maksājumu terminālis

    Ja perifērā ierīce nav ietverta nevienā no šīm kategorijām, aparatūras stacija nav paredzēta perifērās ierīces koplietošanai vairākās POS ierīcēs.

- Dažreiz ierīču draiveri var izraisīt vispārīgo vadības objektu (CCO) darbības traucējumus. Ja nesen ir instalēta kāda ierīce, taču tā nedarbojas pareizi vai ir radušās citas problēmas, šo problēmu bieži vien nav novērt, atkārtoti instalējot CCO. Lai lejupielādētu CCO, apmeklējiet vietni <http://monroecs.com/oposccos_current.htm>.
- Ja pārbaudes vai problēmu novēršanas laikā bieži veicat perifēro ierīču izmaiņas, iespējams, ir nepieciešams atiestatīt IIS, negaidot līdz automātiskai kešatmiņas atsvaidzināšanai. Lai atiestatītu IIS, veiciet tālāk norādītās darbības.

    1. Izvēlnē **Sākt** ievadiet **CMD**.
    2. Meklēšanas rezultātos noklikšķiniet uz **Komandu uzvedne** un pēc tam noklikšķiniet uz **Palaist kā administratoram**.
    3. Logā **Komandu uzvedne** ievadiet **iisreset /Restart** un pēc tam nospiediet taustiņu Enter.
    4. Pēc IIS restartēšanas restartējiet programmu Modern POS.

- Ja bieži veicat perifēro ierīču izmaiņas un arī bieži palaižat un izslēdzat POS klientu, iepriekšējās POS sesijas process dllhost var traucēt pašreizējo sesiju. Šādā gadījumā ierīce var būt nelietojama, līdz aizverat dinamisko saišu bibliotēku (DLL) resursu, kas nodrošina iepriekšējās sesijas pārvaldību. Lai aizvērtu DLL resursu, veiciet tālāk norādītās darbības.

    1. Izvēlnē **Sākt** ievadiet **Uzdevumu pārvaldnieks**.
    2. Meklēšanas rezultātu sarakstā noklikšķiniet uz **Uzdevumu pārvaldnieks**.
    3. Uzdevumu pārvaldnieka cilnē **Detalizēta informācija** noklikšķiniet uz kolonnas virsraksta **Nosaukums**, lai sakārtotu tabulu alfabēta secībā pēc nosaukuma.
    4. Ritiniet uz leju līdz failam dllhost.exe.
    5. Atlasiet katru DLL resursu un pēc tam noklikšķiniet uz **Beigt uzdevumu**.
    6. Kad DLL resursi ir aizvērti, restartējiet programmu Modern POS.

## <a name="additional-resources"></a>Papildu resursi

[Retail perifērijas ierīču simulators](dev-itpro/retail-peripheral-simulator.md)
