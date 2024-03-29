---
title: Perifērās ierīces
description: Šajā rakstā ir izskaidroti koncepti, kas ir saistīti ar Commerce perifērijas ierīcēm.
author: BrianShook
ms.date: 09/08/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.custom:
- "268444"
- intro-internal
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b3113626b18ad7f074c808d7631d13b09071bef2
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459999"
---
# <a name="peripherals"></a>Perifērās ierīces

[!include[banner](includes/banner.md)]

Šajā rakstu ir paskaidrotas koncepcijas, kas ir saistītas ar veikala perifērijas ierīcēm. Tajā ir aprakstīti dažādie veidi, kā perifērijas ierīces var pievienot pārdošanas punktam (POS), un komponenti, kas nodrošina savienojuma ar POS pārvaldību.

## <a name="concepts"></a>Koncepcijas

### <a name="pos-registers"></a>POS kases sistēmas

Navigācija: dodieties uz **Retail un Commerce \> kanālu iestatīšanas \> POS iestatīšanas \> reģistriem**. Pārdošanas punkta (POS) kases sistēma ir elements, kas tiek izmantots, lai noteiktu konkrētas POS instances raksturlielumus. Šie raksturlielumi ietver aparatūras profilu jeb ar kases sistēmu izmantoto perifērijas ierīču iestatījumus, veikalu, ar kuru ir kartēta šī kases sistēma, un vizuālo noformējumu, ko redz lietotājs, kurš pierakstās šajā kases sistēmā.

### <a name="devices"></a>Ierīces

Navigācija: dodieties uz **Retail un Commerce \> Channel Setup \> POS iestatīšanas \> ierīcēm**. Ierīce ir elements, kas pārstāv fizisku instanci tādai ierīcei, kura ir kartēta uz POS reģistru. Kad ierīce tiek izveidota, tā tiek kartēta uz POS reģistru. Ierīces elements seko līdzi informācijai par laiku, kad POS reģistrs tiek aktivizēts, par izmantotā klienta tipu, kā arī par programmu pakotni, kas ir izvietota konkrētā ierīcē. 

Ierīces var kartēt ar šādiem programmu veidiem: Retail Modern POS, Retail Cloud POS, Retail Modern POS — Android un Retail Modern POS - iOS.

### <a name="modern-pos"></a>Modern POS

Modern POS ir operētājsistēmai Microsoft Windows paredzētā POS programma. To var izvietot operētājsistēmās Windows 10 un Windows 11.

### <a name="cloud-pos"></a>Cloud POS

Cloud POS ir programmas Modern POS mākoņa versija, kam var piekļūt tīmekļa pārlūkprogrammā.

### <a name="modern-pos-for-ios"></a>Modern POS operētājsistēmai iOS

Modern POS operētājsistēmai iOS ir operētājsistēmai iOS paredzētā programmas Modern POS versija, ko var izvietot iOS ierīcēs.

### <a name="modern-pos-for-android"></a>Modern POS operētājsistēmai Android

Modern POS operētājsistēmai Android ir operētājsistēmai Android paredzētā programmas Modern POS versija, ko var izvietot Android ierīcēs.

### <a name="pos-peripherals"></a>POS perifērās ierīces

POS perifērās ierīces ir ierīces, kas var tieši atbalstīt POS funkcijas. Parasti šīs perifērās ierīces ir sadalītas noteiktās klasēs. Papildinformāciju par šīm klasēm skatiet šī raksta sadaļā "Ierīču klases".

### <a name="hardware-station"></a>Aparatūras stacija

Navigācija: dodieties uz sadaļu **Mazumtirdzniecības un Komercijas \>\> kanāli.\>** Atlasiet veikalu un pēc tam atlasiet kopsavilkuma cilni **Aparatūras stacijas**. Iestatījums **Aparatūras stacija** ir kanāla līmeņa iestatījums, kas tiek izmantots, lai definētu instances, kurās tiks izvietota perifērās ierīces loģika. Šis iestatījums kanāla līmenī tiek izmantots, lai noteiktu aparatūras stacijas raksturlielumus. Tas tiek arī izmantots, lai norādītu aparatūras stacijas, kas ir pieejamas Modern POS instancei konkrētā veikalā. Aparatūras stacija ir iebūvēta programmās Modern POS operētājsistēmai Windows un Android. Aparatūras staciju var arī izvietot atsevišķi kā savrupu Microsoft interneta informācijas pakalpojumu (IIS) programmu. Šajā gadījumā tai var piekļūt, izmantojot tīklu.

### <a name="hardware-profile"></a>Aparatūras profils

Navigācija: dodieties uz **Retail un Commerce Channel \> Setup \> POS iestatīšanas \> POS aparatūras \> profiliem**. Aparatūras profils ir to ierīču saraksts, kas ir konfigurētas POS kases sistēmai vai aparatūras stacijai. Aparatūras profilu var tieši kartēt ar POS kases sistēmu vai aparatūras staciju.

## <a name="devices-classes"></a>Ierīču klases
Parasti POS perifērās ierīces tiek sadalītas klasēs. Šajā sadaļā ir aprakstītas programmā Modern POS atbalstītās ierīces un sniegts pārskats par tām.

### <a name="printer"></a>Printeris

Printeri var būt parastie POS kvīšu printeri un veselas lapas printeri. Printeri tiek atbalstīti, izmantojot objektu saistīšanu un iegulto versiju Retail POS (OPOS) un draivera Microsoft Windows interfeisus. Vienlaikus var lietot līdz diviem printeriem. Šī iespēja ir piemērota scenārijiem, kuros ar kvīšu printeriem tiek drukātas debitoru kvītis par pārdošanu skaidrā naudā bez piegādes, bet debitoru pasūtījumi, kuros ir ietverts vairāk informācijas, tiek drukāti ar veselas lapas printeri. Kvīšu printerus var tieši pievienot datoram, izmantojot USB portu, pievienot tīklam, izmantojot Ethernet, vai pievienot, izmantojot Bluetooth savienojumu.

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

### <a name="scale"></a>Mērogot

Svarus var pievienot datoram, izmantojot USB un OPOS draiverus. Ja transakcijai tiek pievienota prece, kas ir atzīmēta kā sverama prece, POS tiek nolasīta svara informācija no svariem, prece tiek pievienota transakcijai un tiek izmantoti no svariem saņemtie daudzuma dati.

### <a name="pin-pad"></a>PIN bloks

Personas identifikācijas numura (PIN) bloku atbalsts tiek nodrošināts, izmantojot OPOS, taču to pārvaldībai ir jāizmanto maksājumu savienotājs.

### <a name="secondary-display"></a>Sekundārais displejs

Ja ir konfigurēts sekundārais displejs, pamatinformācijas rādīšanai tiek izmantots 2. Windows displejs. Pēc noklusējuma sekundārais displejs nav konfigurējams un rāda ierobežotu saturu. Sekundārā displeja mērķis ir atbalstīt neatkarīgu programmatūras izstrādātāja (ISV) paplašinājumu. 

### <a name="payment-device"></a>Maksājumu ierīce

Maksājumu ierīces atbalts tiek nodrošināts, izmantojot maksājumu savienotāju. Maksājumu ierīces var veikt vienu vai daudzas no funkcijām, ko nodrošina citas ierīču klases. Piemēram, maksājumu ierīce var darboties kā MJL/karšu lasītājs, rindu displejs, paraksta ieguves ierīce vai PIN bloks. Maksājumu ierīču atbalsts tiek nodrošināts neatkarīgi no savrupo ierīču atbalsta, kas tiek nodrošināts citām ierīcēm, kuras ir iekļautas aparatūras profilā.

## <a name="supported-interfaces"></a>Atbalstītie interfeisi
### <a name="opos"></a>OPOS

Lai palīdzētu nodrošināt to, ka kopā ar programmu Commerce var lietot pēc iespējas lielāku ierīču klāstu, galvenā perifēro ierīču platforma, kas tiek atbalstīta, ir nozares standarta platforma OLE punktā POS. Standartu OLE punktā POS ir izstrādājusi organizācija National Retail Federation (NRF), kas ievieš perifēro ierīču nozares standarta sakaru protokolus. OPOS ir plaši izplatīta standarta OLE punktā POS implementācija. Tā ir izstrādāta 1990. gadu vidū un kopš tā laika ir vairākas reizes atjaunināta. OPOS nodrošina ierīču draiveru arhitektūru, kas sniedz iespēju viegli integrēt POS aparatūru Windows sistēmās. OPOS vadības elementi nodrošina saziņu starp saderīgo aparatūru un POS programmatūru. OPOS vadības elements sastāv no divām tālāk norādītajām daļām.

-   **Vadības objekts** — ierīču klases (piemēram, rindu displeju) vadības objekts nodrošina programmatūras interfeisu. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) nodrošina standartizētu OPOS vadības objektu kopu, kas tiek saukta par vispārīgajiem vadības objektiem (CCO). Programmas Commerce POS komponenta pārbaudei tiek izmantoti CCO objekti. Tādējādi pārbaude palīdz nodrošināt to, ka gadījumā, ja programma Commerce nodrošina kādas ierīces klases atbalstu, izmantojot OPOS, var tikt nodrošināts daudzu ierīču veidu atbalsts, ja vien ražotājs nodrošina pakalpojumu objektu, kas ir paredzēts standartam OPOS. Nav nepieciešams atsevišķi pārbaudīt katru ierīču veidu.
-   **Pakalpojumu objekts** — pakalpojumu objekts nodrošina saziņu starp vadības objektu (C) un ierīci. Parasti ierīces pakalpojumu objektu nodrošina ierīces ražotājs. Taču dažos gadījumos pakalpojumu objektu, iespējams, ir nepieciešams lejupielādēt no ražotāja vietnes. Piemēram, var būt pieejama jaunāka pakalpojumu objekta versija. Lai uzzinātu ražotāja vietnes adresi, skatiet aparatūras dokumentāciju.

[![Vadības objekts un pakalpojumu objekts.](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) OLE punktā POS OPOS implementācijas atbalsts palīdz nodrošināt to, ka tad, ja ierīču ražotāji un POS publicētāji ir pareizi ieviesuši standartu, POS sistēmas un atbalstītās ierīces var darboties kopā, pat ja tās iepriekš nav pārbaudītas kopā. 

> [!NOTE]
> OPOS atbalsts nenodrošina visu to ierīču atbalstu, kurām ir OPOS draiveri. Pirmkārt, programmai Commerce ir jānodrošina attiecīgā ierīces veida vai klases atbalsts, izmantojot OPOS. Turklāt pakalpojumu objektos dažreiz var nebūt ietverta jaunākā CCO versija. Ņemiet vērā arī to, ka parasti dažādu pakalpojumu objektu kvalitāte atšķiras.

### <a name="windows"></a>Windows

Kvīšu drukāšana POS ir optimizēta standartam OPOS. OPOS parasti nodrošina daudz ātrāku drukāšanu nekā operētājsistēma Windows. Tāpēc ir ieteicams izmantot OPOS, jo īpaši vidēs, kur tiek drukātas 40 kolonnu kvītis un ir jānodrošina ātra transakciju apstrāde. Lielākajai daļai ierīču ir jāizmanto OPOS vadīklas. Taču daži OPOS kvīšu printeri atbalsta arī Windows draiverus. Izmantojot Windows draiveri, varat piekļūt jaunākajiem fontiem un tīklā lietot vienu printeri vairākām kases sistēmām. Taču Windows draiveru lietošanai ir trūkumi. Tālāk ir sniegti daži šo trūkumu piemēri.

-   Ja tiek izmantoti Windows draiveri, pirms drukāšanas tiek renderēti attēli. Tāpēc drukāšana ir lēnāka, nekā ar printeriem, kam tiek izmantoti OPOS vadības elementi.
-   Ja tiek izmantoti Windows draiveri, ierīces, kas ir pievienotas, izmantojot printeri (ziedlapķēdē), var darboties nepareizi. Piemēram, naudas kasieris var nebūt atvērts vai arī kvīšu printeris var nedarboties, kā paredzēts.
-   Turklāt OPOS atbalsta plašāku kvīšu printeriem raksturīgu mainīgo kopu, piemēram, papīra griešanas vai pavadzīmju drukāšanas mainīgos.
-   Windows printeri netiek atbalstīti IIS aparatūras stacijā. 

Ja izmantotajam Windows printerim ir pieejami OPOS vadības elementi, printerim joprojām ir pareizi jādarbojas kopā ar programmu Commerce.

### <a name="plug-and-play-devices"></a>Spraudņa un vadības ierīces

Kad spraudņa un ēnas ierīce ir pievienota Windows OS versijai, kas atbalsta šo ierīces veidu, tad, lai ierīci varētu izmantot ar paredzēto, nav nepieciešams draiveris. Piemēram, ja sistēma Windows atrod statīva ierīci, operētājsistēma zināt, ka ierīcei ir klases tips "Statīvs" un šī ierīce tiek uztverta kā paraci. Nav nepieciešami nekādi papildu iestatījumi. 

POS perifērijas ierīču gadījumā daudzasPOZITOņu ierīces var spraudņat un atpazīt, izmantojot Windows OS kā cilvēkresursu interfeisa ierīces (HID). Tomēr sistēma Windows, iespējams, nevarēs noteikt ierīces nodrošinātās iespējas, jo ierīcē nav norādīta klase vai ierīces veids. Operētājsistēmā Windows 10 ir pievienotas svītrkoda skeneru un MJL ierīču klases. Tāpēc, ja operētājsistēmā Windows 10 ierīce tiek noteikta kā ietverta vienā no šīm klasēm, atbilstošajā laikā operētājsistēmā Windows tiek gaidīti notikumi no šīs ierīces.

Programma Modern POS atbalsta UWP MJL un skenerus. Tāpēc, kad Modern POS ir gatavs ievadei no vienas no šīm ierīcēm, un ierīce, kas pieder kādai no ierīču klasēm, ir pievienota šai ierīcei. Piemēram, ja Spraudņa un svītrkoda skeneris ir pievienots Windows 10 datoram un svītrkoda pierakstīšanās ir konfigurēta Modern POS, svītrkoda skeneris kļūs aktīvs pierakstīšanās lapā. Nav nepieciešami nekādi papildu iestatījumi.

Papildu POS perifērijas klases tiek pievienotas sistēmai Windows, piemēram, kases naudas kastu un kvīšu printeru klases. Programmā Modern POS vēl nav nodrošināts šo jauno klašu atbalsts.

> [!NOTE] 
> Noteiktas INSTALĒŠANAI ierīces var kļūt nereaģējošas vai neatbildošas, ja tās pārvalda Windows 10 [vadības funkcija, kas tiek saukta PAR SELECTIVE Suspend](/windows-hardware/drivers/usbcon/usb-selective-suspend). Ja PAR aktivizēAKTIVIZĒŠANU, IETEICAMS deaktivizēt atlases bloķēšanas funkciju tai ierīcei. Papildinformāciju skatiet izvēles [aizturēšanas iespējošana](/windows-hardware/drivers/usbcon/usb-selective-suspend#enabling-selective-suspend). 

### <a name="keyboard-wedge"></a>Svītrkoda/magnētiskās joslas nolasīšanas ierīce

Svītrkoda/magnētiskās joslas nolasīšanas ierīces nodrošina datu sūtīšanu uz datoru tā, it kā šie dati būtu ievadīti ar tastatūru. Tāpēc pēc noklusējuma skenētie vai nolasītie dati tiek nosūtīti POS interfeisā aktīvo lauku. Dažos gadījumos šī darbība var izraisīt nepareizā veida datu ieskenēšanu nepareizajā laukā. Piemēram, svītrkods var tikt ieskenēts laikā, kas ir paredzēts kredītkartes datu ievadei. Daudzos gadījumos POS terminālī ir loģika, kas nosaka, vai skenētie vai lasīšanas dati ir svītrkods vai kartes lasīšana. Tādējādi dati tiek pareizi apstrādāti. Taču, ja ierīces ir iestatītas kā OPOS nevis tastatūras žetonu ierīces, kontroli pār to, kā var patērēt datus no šīm ierīcēm, jo vairāk ir zināms par ierīci, kas izveidojusies no datu. Piemēram, no svītrkoda skenera saņemtie dati tiek automātiski atpazīti kā svītrkods, un saistītais ieraksts datu bāzē tiek atrasts ātrāk un vienkāršāk nekā tad, ja tiek izmantota vispārējā virknes meklēšana, kā tas ir svītrkoda/magnētiskās joslas nolasīšanas ierīču gadījumā.

> [!NOTE]
> Kad POS sistēmā tiek izmantoti tastatūras ķīļveida skeneri, tie ir jāprogrammē tā, lai pēc pēdējās skenētās rakstzīmes sūtītu transportēšanas atgriešanu vai **Ievadīt** notikumu. Ja šī konfigurācija nav pabeigta, tastatūras ķīļveida skeneri nedarbosies pareizi. Detalizētu informāciju par to, kā pievienot preču atgriešanas notikumu, skatiet jūsu ierīces ražotāja sniegtajā dokumentācijā.  

### <a name="device-printers"></a>Ierīču printeri

Printerus ar veidu Ierīce var konfigurēt, lai lietotājs varētu atlasīt printeri, kas ir konfigurēts datoram. Ja ir konfigurēts printeris ar tipu Ierīce, ja Modern POS atrod drukāšanas komandu, lietotājam būs jāizvēlas printeris sarakstā. Šī uzvedība atšķiras no Windows draiveriem lietotās funkcionalitātes, jo printera "Windows" tips aparatūras profilā nerāda lietotājam printeru sarakstu. Tā vietā laukā **Ierīces nosaukums** ir jānorāda printera nosaukums.

### <a name="network"></a>Tīkls

Tīklā tiešā veidā, izmantojot starpprocesu saziņas (IPC) aparatūras staciju, kas ir iebūvēta lietojumprogrammā Modern POS operētājsistēmai Windows, vai izmantojot citu Modern POS klientu IIS aparatūras staciju, var lietot tīklā adresējamas naudas kastes, kvīšu printerus un maksājumu termināļus.

## <a name="hardware-station-deployment-options"></a>Aparatūras stacijas izvietošanas iespējas

### <a name="dedicated"></a>Atvēlēts

Mūsdienīgie POS klienti operētājsistēmai Windows un Android ietver **Speciālās** vai iebūvētās aparatūras stacijas. Šie klienti var tieši komunicēt ar perifērijas ierīcēm, izmantojot biznesa loģiku, kas ir iebūvēta lietojumprogrammās. Android programma atbalsta tikai tīkla ierīces. Lai iegūtu vairāk informācijas par perifēro atbalstu Android, apmeklējiet rakstu [Iestatīt POS hibrīda programmu Android un iOS](./dev-itpro/hybridapp.md).

Lai lietotu atvēlēto aparatūras staciju, veiciet šādas darbības.

1. Piešķiriet aparatūras profilu kases sistēmai, kas izmantos Modern POS operētājsistēmai Windows vai programmai Android.
1. Izveidojiet aparatūras staciju ar "Dedicated" veidu veikalam, kur tiks izmantota kases reģistrs. 
1. Atveriet Modern POS veidu, kas nav sastādītājs, un izmantojiet **aparatūras staciju pārvaldības operāciju, lai ieslēgtu aparatūras** stacijas iespējas. Atvēlētā aparatūras stacija pēc noklusējuma būs aktīva. 
1. Izrakstīties no Modern POS. Pēc tam vēlreiz parakstieties un atveriet maiņu. Tagad būs izmantojamas aparatūras profilā konfigurētās perifērijas ierīces. 

### <a name="shared"></a>Koplietots

Dažreiz tas tiek saukts arī par "IIS" aparatūras staciju, "IIS", kas norāda, ka POS programma savieno aparatūras staciju, izmantojot Microsoft interneta informācijas pakalpojumus. POS lietojumprogrammas savienojumam ar IIS aparatūras staciju tiek izmantoti tīmekļa pakalpojumi, kas darbojas datorā, kuram ir pievienotas ierīces. Ja tiek lietota koplietotā aparatūras stacijas, aparatūras stacijai pievienotās perifērās ierīces var izmantot jebkurā POS kases sistēmā, kas ir vienā tīklā ar IIS aparatūras staciju. Tā kā tikai programma Modern POS operētājsistēmai Windows un Android nodrošina iebūvētu perifēro ierīču atbalstu, visās citās lietojumprogrammas Modern POS versijās saziņai ar aparatūras profilā konfigurētajām POS perifērajām ierīcēm ir jāizmanto IIS aparatūras stacija. Tāpēc katrai IIS aparatūras stacijas instancei ir nepieciešams dators, kurā darbojas tīmekļa pakalpojums un lietojumprogramma, kas nodrošina saziņu ar ierīcēm. 

Koplietoto aparatūras staciju var izmantot, lai vairāki pārdošanas punkta klienti varētu kopīgot perifērijas ierīces, vai to var izmantot, lai pārvaldītu fiksēto perifērijas ierīču kopu vienam pārdošanas punktam. 

Kad aparatūras stacija tiek izmantota, lai atbalstītu perifēro ierīču koplietošanu starp vairākiem POS klientiem, jāizmanto tikai naudas kastes, kvīšu printeri un maksājumu termināļi. Nevarat tieši pievienot savrupus svītrkoda skenerus, MJL, rindu displejus, svarus vai citas ierīces. Pretējā gadījumā, ja vairākās POS ierīcēs vienlaikus tiek mēģināts pieprasīt šīs perifērās ierīces, rodas konflikti. Tālāk ir aprakstīts, kā tiek pārvaldīti konflikti atbalstītajām ierīcēm.

-   **Naudas kaste** — naudas kaste tiek atvērta, izmantojot uz ierīci nosūtītu notikumu. Problēmas var rasties, ja naudas kastne tiek izsaukta, kad naudas kasts jau ir atvērta. Aparatūras profila koplietotajā aparatūras stacijas konfigurācijā izmantotais **naudas** kasieris ir jāiestata uz Koplietots. Šis iestatījums nodrošina to, ka brīdī, kad no POS tiek nosūtīta atvēršanas komanda, POS netiek pārbaudīts, vai naudas kaste jau ir atvērta.
-   **Kvīšu printeris** — ja uz aparatūras staciju vienlaikus tiek nosūtītas divas kvīts drukāšanas komandas, viena no komandām var tikt zaudēta atkarībā no ierīces. Dažās ierīcēs ir iekšējā atmiņa vai pieprasījumu ierobežošanas līdzeklis, kas var novērst šo problēmu. Ja drukas komanda netiek veiksmīgi izpildīta, kasieris saņem kļūdas ziņojumu un var vēlreiz mēģināt nosūtīt drukas komandu no POS.
-   **Maksājumu terminālis** — ja kasieris mēģina veikt norēķinus par transakciju, izmantojot maksājumu termināli, kas jau tiek lietots, kasierim tiek parādīts ziņojums ar norādi, ka terminālis tiek lietots, un aicinājumu vēlāk mēģināt vēlreiz. Parasti kasieri var redzēt, ka terminālis jau tiek lietots, un uzgaida, līdz ir pabeigta otra transakcija, pirms vēlreiz mēģina veikt norēķinus.

Kādā no nākamajiem laidieniem ir paredzēts ietvert validācijas līdzekli, lai noteiktu, vai ar aparatūras staciju kartētajam aparatūras profilam ir iestatītas neatbalstītas ierīces. Ja tiek noteikta kāda neatbalstīta ierīce, lietotājs saņem ziņojumu par to, ka ierīces netiek atbalstītas lietošanai ar koplietotām aparatūras stacijām. Ja tiek izmantotas koplietotas aparatūras stacijas, kases sistēmas līmenī ir iestatīta opcijas **Atlasīt norēķinu brīdī** vērtība **Jā**. Šādā gadījumā, kad POS tiek atlasīti transakcijas norēķini, POS lietotājam tiek prasīts atlasīt aparatūras staciju. Ja aparatūras stacija tiek atlasīta tikai norēķinu laikā, aparatūras stacijas atlase tiek tieši pievienota mobilo scenāriju POS darbplūsmai. Papildu ieguvums ir tas, ka koplietošanas scenārijos netiek lietots maksājumu termināļa rindu displejs. Ja maksājumu terminālis tiek izmantots kā rindu displejs, citiem lietotājiem var tikt liegta iespēja izmantot šo termināli, līdz tiek pabeigta transakcija. Mobilajos scenārijos transakcijas rindas var tikt pievienotas ilgākā laika periodā. Tāpēc ir nepieciešama opcija **Atlasīt norēķinu brīdī**, lai nodrošinātu optimālu ierīces pieejamību.

### <a name="network-peripherals"></a>Tīkla perifērās ierīces

Ierīču tīkla apzīmējums aparatūras profilā sniedz iespēju izveidot naudas kastu, kvīšu printeru un maksājumu termināļu tīkla savienojumu.

#### <a name="modern-pos-for-windows"></a>Modern POS operētājsistēmai Windows

Tīkla perifēro ierīču IP adreses varat norādīt divās vietās. Ja Modern POS Windows klientā tiek izmantota viena tīkla perifēro ierīču kopa, šo ierīču IP adreses ir jāiestata, izmantojot kases sistēmas darbību rūts opciju **IP konfigurēšana**. Ja tīkla ierīces tiks koplietotas vairākās POS kases sistēmās, aparatūras profilu, kam ir piešķirta tīkla ierīce, var tieši kartēt ar koplietotu aparatūras staciju. Lai piešķirtu IP adreses, atlasiet aparatūras staciju lapā **Veikali** un pēc tam sadaļas **Aparatūras stacijas** laukā **IP konfigurēšana** norādiet tīkla ierīces, kas ir piešķirtas šai aparatūras stacijai. Ja aparatūras stacijai ir piešķirtas tikai tīkla ierīces, šī aparatūras stacija nav jāizvieto. Šādā gadījumā aparatūras stacija ir nepieciešama tikai tīklā adresējamo ierīču konceptuālai grupēšanai atbilstoši to atrašanās vietai veikalā.

#### <a name="cloud-pos-and-modern-pos-for-ios"></a>Cloud POS un Modern POS operētājsistēmai iOS

Loģika, kas nodrošina fiziski pievienoto un tīklā adresējamo perifēro ierīču darbību, ir ietverta aparatūras stacijā. Tāpēc visiem POS klientiem, izņemot programmu Modern POS operētājsistēmai Windows un Android, ir jāizvieto un jāaktivizē IIS aparatūras stacija, lai nodrošinātu POS saziņu ar perifērajām ierīcēm, neatkarīgi no tā, vai šīs perifērās ierīces ir fiziski savienotas ar aparatūras staciju vai adresētas tīklā.

## <a name="setup-and-configuration"></a>Iestatīšana un konfigurēšana
### <a name="hardware-station-installation"></a>Aparatūras stacijas instalēšana

Norādījumus par IIS aparatūras stacijas instalēšanu skatiet sadaļā [Aparatūras stacijas konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Modern POS operētājsistēmai Windows iestatīšana un konfigurēšana

Informāciju skatiet [Modern POS (MPOS) konfigurēšana, instalēšana un aktivizēšana](retail-modern-pos-device-activation.md).

### <a name="modern-pos-for-android-and-ios-setup-and-configuration"></a>Modern POS operētājsistēmai Android un iOS iestatīšana un konfigurēšana

Informāciju skatiet rakstā [Iestatiet POS hibrīdprogrammu operētājsistēmā Android un iOS](./dev-itpro/hybridapp.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS ierīces iestatīšana un konfigurēšana

Papildinformāciju par OPOS komponentiem skatiet šī dokumenta sadaļā “Atbalstītie interfeisi”. Parasti OPOS draiverus nodrošina ierīces ražotājs. Instalējot OPOS ierīces draiveri, kādā no tālāk norādītajām vietām Windows reģistrā tiek pievienota atslēga.

-   **32 bitu sistēma:** HKEY\_ LOCAL\_ MACHINE\SOFTWARE\OLEforRetail\ServiceOPOS
-   **64 bitu sistēma:** HKEY\_ LOCAL\_ MACHINE\SOFTWARE\RNO6432Node\OLEforRetail\ServiceOPOS

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

Tīkla perifērajām ierīcēm var nodrošināt tiešu atbalstu, izmantojot lietojumprogrammā Modern POS operētājsistēmai Windows un Android programmās iebūvēto aparatūras staciju. Visiem citiem klientiem ir jāizvieto IIS aparatūras stacija.

| Klients      | IPC aparatūras stacija | IIS aparatūras stacija |
|-------------|----------------------|----------------------|
| Windows programma | Jā                  | Jā                  |
| Cloud POS   | Nē                   | Jā                  |
| Android     | Jā                  | Jā                  |
| iOS         | Nē                   | Jā                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Atbalstītie ierīču veidi pēc aparatūras stacijas veida
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS operētājsistēmai Windows ar IPC (iebūvētu) aparatūras staciju

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atbalstītā ierīču klase</th>
<th>Atbalstītie interfeisi</th>
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
<li>UWP (Nav nepieciešama iestatīšana.)</li>
<li>Svītrkoda/magnētiskās joslas nolasīšanas ierīce (Nav nepieciešama iestatīšana.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Naudas kaste</td>
<td><ul>
<li>OPOS</li>
<li>Tīkls </br><strong>Piezīme.</strong> Ja naudas kastei ir konfigurēta opcija <strong>Lietot koplietoto maiņu</strong>, var iestatīt tikai vienu naudas kasti.</li>
</ul></td>
</tr>
<tr class="odd">
<td>2. dokumenta sastādītājs</td>
<td><ul>
<li>OPOS</li>
<li>Tīkls </br><strong>Piezīme.</strong> Ja naudas kastei ir konfigurēta opcija <strong>Lietot koplietoto maiņu</strong>, var iestatīt tikai vienu naudas kasti.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skeneris</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Nav nepieciešama iestatīšana.)</li>
<li>Svītrkoda/magnētiskās joslas nolasīšanas ierīce (Nav nepieciešama iestatīšana.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>2. skeneris</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Nav nepieciešama iestatīšana.)</li>
<li>Svītrkoda/magnētiskās joslas nolasīšanas ierīce (Nav nepieciešama iestatīšana.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Mērogs</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN bloks</td>
<td>OPOS (Atbalsts tiek nodrošināts, pielāgojot maksājumu savienotāju.)</td>
</tr>
<tr class="even">
<td>Paraksta ieguve</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Maksājumu terminālis</td>
<td><ul>
<li>Pielāgotu ierīču atbalsts</li>
<li>Tīkls (Papildinformāciju skatiet maksājumu savienotāja dokumentācijā.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Visi Modern POS klienti, kam ir īpaša "Koplietotā" IIS aparatūras stacija

> [!NOTE]
> Ja IIS aparatūras stacija ir "fiksēts", POS klientam un aparatūras stacijai ir "viens pret vienu" relācija.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atbalstītā ierīču klase</th>
<th>Atbalstītie interfeisi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printeris</td>
<td><ul>
<li>OPOS</li>
<li>Tīkls</li>
</ul></td>
</tr>
<tr class="even">
<td>2. printeris</td>
<td><ul>
<li>OPOS</li>
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
<td>Naudas kaste</td>
<td><ul>
<li>OPOS</li>
<li>Tīkls </br><strong>Piezīme.</strong> Ja naudas kastei ir konfigurēta opcija <strong>Lietot koplietoto maiņu</strong>, katrā aparatūras profilā var iestatīt tikai vienu naudas kasti.</li>
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
<td>OPOS (Atbalsts tiek nodrošināts, pielāgojot maksājumu savienotāju.)</td>
</tr>
<tr class="odd">
<td>Paraksta ieguve</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Maksājumu terminālis</td>
<td><ul>
<li>Pielāgotu ierīču atbalsts</li>
<li>Tīkls (Papildinformāciju skatiet maksājumu savienotāja dokumentācijā.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-share-an-iis-hardware-station"></a>Visi Modern POS klienti, kas koplieto IIS aparatūras staciju

> [!NOTE]
> Ja IIS aparatūras stacija ir koplietota, aparatūras stacija var tikt vienlaikus lietota vairākās ierīcēs. Šādā gadījumā drīkst lietot tikai ierīces, kas ir norādītas tālāk esošajā tabulā. Ja mēģināsit koplietot ierīces, kas nav norādītas šajā tabulā, piemēram, svītrkoda skenerus un MJL, kad vairākās ierīcēs tiks mēģināts pieprasīt vienu perifērijas ierīci, radīsies kļūdas. Turpmāk šāda konfigurācija netiks pieļauta.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atbalstītā ierīču klase</th>
<th>Atbalstītie interfeisi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printeris</td>
<td><ul>
<li>OPOS</li>
<li>Tīkls</li>
</ul></td>
</tr>
<tr class="even">
<td>2. printeris</td>
<td><ul>
<li>OPOS</li>
<li>Tīkls</li>
</ul></td>
</tr>
<tr class="odd">
<td>Naudas kaste</td>
<td><ul>
<li>OPOS</li>
<li>Tīkls </br><strong>Piezīme.</strong> Ja naudas kastei ir konfigurēta opcija <strong>Lietot koplietoto maiņu</strong>, katrā aparatūras profilā var iestatīt tikai vienu naudas kasti.</li>
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
<td>Maksājumu terminālis</td>
<td><ul>
<li>Pielāgotu ierīču atbalsts</li>
<li>Tīkls (Papildinformāciju skatiet maksājumu savienotāja dokumentācijā.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Atbalstīto scenāriju konfigurācija
Lai iegūtu vairāk informācijas par to, kā izveidot aparatūras profilus, skatiet [Perifērijas ierīču pievienošana pārdošanas punktam (POS)](define-maintain-channel-clients-registers-hw-stations.md). 

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS operētājsistēmai Windows ar IPC (iebūvētu) aparatūras staciju

Šī konfigurācija visbiežāk tiek lietota parasto stacionāro POS kases sistēmām. Šajā scenārijā aparatūras profila informācija tiek tieši kartēta ar kases sistēmu. Arī EFT termināļa numurs ir jāiestata kases sistēmā. Lai iestatītu šo konfigurāciju, veiciet tālāk norādītās darbības.

1.  Izveidojiet aparatūras profilu, kurā ir konfigurētas visas nepieciešamās perifērās ierīces.
2.  Kartējiet aparatūras profilu ar POS kases sistēmu.
3.  Izveidojiet veida **Atvēlēts** aparatūras staciju veikalam, kurā tiks lietots POS reģistrs. Pēc izvēles ievadiet aprakstu. 

    > [!NOTE]
    > Nav nepieciešams iestatīt nekādus citus aparatūras stacijas rekvizītus. Visa pārējā nepieciešama informācija, piemēram, aparatūras profils, tiks saņemta no kases sistēmas.

4.  Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.
5.  Atlasiet sadales grafiku **1090**, lai jauno aparatūras profilu sinhronizētu ar veikalu. Atlasiet **Izpildīt tūlīt,** lai sinhronizētu izmaiņas pos.
6.  Atlasiet sadales grafiku **1040**, lai jauno aparatūras staciju sinhronizētu ar veikalu. Atlasiet **Izpildīt tūlīt,** lai sinhronizētu izmaiņas pos.
7.  Instalējiet un aktivizējiet programmu Modern POS operētājsistēmai Windows.
8.  Palaidiet programmu Modern POS operētājsistēmai Windows un sāciet lietot pievienotās perifērās ierīces.

### <a name="modern-pos-for-android-with-an-ipc-built-in-hardware-station"></a>Modern POS operētājsistēmai Android ar IPC (iebūvētu) aparatūras staciju

**Jauns printerim 10.0.8** . Par avansu modernajā POS tiek atbalstīti printeriem, kas ir savienoti ar Printeriem un naudas kasti, izmantojot Android DK portu. Papildu informāciju skatiet rakstā [Iestatiet POS hibrīdprogrammu operētājsistēmās Android un iOS](./dev-itpro/hybridapp.md).

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Visi Modern POS klienti, kam ir saistīta koplietotā IIS aparatūras stacija

Šo konfigurāciju var lietot visiem Modern POS klientiem, kam ir aparatūras stacija, kura tiek lietota tikai vienā POS kases sistēmā. Lai iestatītu šo konfigurāciju, veiciet tālāk norādītās darbības.

1.  Izveidojiet aparatūras profilu, kurā ir konfigurētas visas nepieciešamās perifērās ierīces.
2.  Izveidojiet veida **Atvēlēts** aparatūras staciju veikalam, kurā tiks lietots POS reģistrs.
3.  Atvēlētajā aparatūras stacijā iestatiet tālāk norādītos rekvizītus.
    -   **Resursdatora nosaukums** — tā resursdatora nosaukums, kurā tiks darbināta aparatūras stacija. 
    
        > [!NOTE]
        > Programma Cloud POS var atrisināt **localhost**, lai noteiktu lokālo datoru, kurā tiek darbināta programma Cloud POS. Taču arī sertifikātā, kas ir nepieciešams, lai programmu Cloud POS savienotu pārī ar aparatūras staciju, ir jābūt norādītam datora nosaukumam “Localhost”. Lai nepieļautu problēmas, ir ieteicams veikalam norādīt katras atvēlētās aparatūras stacijas instanci, ja tas ir nepieciešams. Katras aparatūras stacijas resursdatora nosaukumam ir jābūt vienādam ar tā konkrētā datora nosaukumu, kurā tiks izvietota aparatūras stacija.
    
    -   **Ports** — ports, kas ir jāizmanto aparatūras stacijas saziņai ar Modern POS klientu.
    -   **Aparatūras profils** — ja aparatūras stacijā nav nodrošināts aparatūras profils, tiek lietots kases sistēmai piešķirtais aparatūras profils.
    -   **EFT POS numurs** — EFT termināļa ID, kas ir jāizmanto, nosūtot EFT autorizācijas datus. Šo ID nodrošina kredītkaršu procesors.
    -   **Pakotnes nosaukums** — aparatūras stacijas pakotne, kas ir jāizmanto, izvietojot aparatūras staciju.

4.  Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.
5.  Atlasiet sadales grafiku **1090**, lai jauno aparatūras profilu sinhronizētu ar veikalu. Atlasiet **Izpildīt tūlīt,** lai sinhronizētu izmaiņas pos.
6.  Atlasiet sadales grafiku **1040**, lai jauno aparatūras staciju sinhronizētu ar veikalu. Atlasiet **Izpildīt tūlīt,** lai sinhronizētu izmaiņas pos.
7.  Instalējiet aparatūras staciju. Papildinformāciju par to, kā instalēt aparatūras staciju, skatiet [Retail aparatūras stacijas konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md).
8.  Instalējiet un aktivizējiet programmu Modern POS. Papildinformāciju par to, kā instalēt programmu Modern POS, skatiet [Rtail Modern POS (MPOS) konfigurēšana, instalācija un aktivizēšana](retail-modern-pos-device-activation.md).
9.  Pierakstieties programmā Modern POS un atlasiet vienumu **Veikt operācijas bez naudas kastes**.
10. Sāciet operāciju **Pārvaldīt aparatūras stacijas**.
11. Atlasiet **Pārvaldīt**.
12. Aparatūras stacijas pārvaldības lapā iestatiet attiecīgo opciju, lai ieslēgtu aparatūras staciju.
13. Atlasiet aparatūras staciju, kuru vēlaties izmantot, un pēc tam atlasiet Savienot **pārī**.
14. Kad aparatūras stacija ir savienota pārī, atlasiet **Aizvērt**.
15. Aparatūras stacijas atlases lapā atlasiet nesen atlasīto aparatūras staciju, lai to aktivizētu.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Visi Modern POS klienti, kam ir koplietota IIS aparatūras stacija

Šo konfigurāciju var lietot visiem Modern POS klientiem, kuros aparatūras stacijas tiek koplietotas ar citām ierīcēm. Lai iestatītu šo konfigurāciju, veiciet tālāk norādītās darbības.

1.  Izveidojiet aparatūras profilu, kurā ir konfigurētas nepieciešamās perifērās ierīces.
2.  Izveidojiet veida **Koplietots** aparatūras staciju veikalam, kurā tiks lietots POS reģistrs.
3.  Koplietotajā aparatūras stacijā iestatiet tālāk norādītos rekvizītus.
    -   **Resursdatora nosaukums** — tā resursdatora nosaukums, kurā tiks darbināta aparatūras stacija.
    -   **Apraksts** — teksts, kas palīdz identificēt aparatūras staciju, piemēram, **Atgriešanas darbības** vai **Veikala lete**.
    -   **Ports** — ports, kas ir jāizmanto aparatūras stacijas saziņai ar Modern POS klientu.
    -   **Aparatūras profils** — katrai koplietotajai aparatūras stacijai ir nepieciešams aparatūras profils. Aparatūras profilus var koplietot vairākās aparatūras stacijās, taču tiem ir jābūt kartētiem ar katru aparatūras staciju. Turklāt ir ieteicams izmantot koplietotas darba maiņas, ja vairākās ierīcēs tiek lietota viena un tā pati aparatūras stacija. Lai iestatītu koplietotu maiņu, dodieties uz sadaļu **Retail un Commerce Channel \> Setup \> POS iestatīšanas \> POS profili Aparatūras \> profili**. Katram koplietotajam aparatūras profilam atlasiet naudas kasti un iestatiet opcijas **Koplietojama maiņas naudas kaste** vērtību **Jā**.
    -   **EFT POS numurs** — EFT termināļa ID, kas ir jāizmanto, nosūtot EFT autorizācijas datus. Šo ID nodrošina kredītkaršu procesors.
    -   **Pakotnes nosaukums** — aparatūras stacijas pakotne, kas ir jāizmanto, izvietojot aparatūras staciju.

4.  Atkārtojiet 2. un 3. darbību ar katru papildu aparatūras staciju, kas ir nepieciešama veikalā.
5.  Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.
6.  Atlasiet sadales grafiku **1090**, lai jauno aparatūras profilu sinhronizētu ar veikalu. Atlasiet **Izpildīt tūlīt,** lai sinhronizētu izmaiņas pos.
7.  Atlasiet sadales grafiku **1040**, lai jauno aparatūras staciju sinhronizētu ar veikalu. Atlasiet **Izpildīt tūlīt,** lai sinhronizētu izmaiņas pos.
8.  Instalējiet aparatūras staciju katrā resursdatorā, ko iestatījāt, veicot 2. un 3. darbību. Papildinformāciju par to, kā instalēt aparatūras staciju, skatiet [Retail aparatūras stacijas konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md).
9.  Instalējiet un aktivizējiet programmu Modern POS. Papildinformāciju par to, kā instalēt programmu Modern POS, skatiet [Rtail Modern POS (MPOS) konfigurēšana, instalācija un aktivizēšana](retail-modern-pos-device-activation.md).
10. Pierakstieties programmā Modern POS un atlasiet vienumu **Veikt operācijas bez naudas kastes**.
11. Sāciet operāciju **Pārvaldīt aparatūras stacijas**.

12. Atlasiet **Pārvaldīt**.
13. Aparatūras stacijas pārvaldības lapā iestatiet attiecīgo opciju, lai ieslēgtu aparatūras staciju.
14. Atlasiet aparatūras staciju, kuru vēlaties izmantot, un pēc tam atlasiet Savienot **pārī**.
15. Atkārtojiet 14. darbību ar katru aparatūras staciju, kas tiks lietota programmā Modern POS.
16. Kad visas nepieciešamās aparatūras stacijas ir savienotas pārī, atlasiet **Aizvērt**.
17. Aparatūras stacijas atlases lapā atlasiet nesen atlasīto aparatūras staciju, lai to aktivizētu. 

> [!NOTE]
> Ja ierīcēs bieži tiek lietotas dažādas aparatūras stacijas, ir ieteicams konfigurēt programmu Modern POS tā, lai, sākot norēķinu procesu, kasierim tiktu prasīts atlasīt aparatūras staciju. Dodieties uz **Mazumtirdzniecība un Komercija \> Kanāla iestatīšana \> POS iestatīšana \> Reģistri**. Atlasiet kases sistēmu un pēc tam iestatiet opcijas **Atlasīt norēķinu brīdī** vērtību **Jā**. Izmantojiet sadales grafiku **1090**, lai sinhronizētu izmaiņas ar kanālu datu bāzi.

## <a name="extensibility"></a>Paplašināmība
Informāciju par aparatūras stacijas paplašināmības scenārijiem skatiet tēmā [POS integrēšana ar jaunu aparatūras ierīci un paplašinājuma instalētāja ģenerēšana](dev-itpro/hardware-device-extension.md).

## <a name="security"></a>Drošība
Saskaņā ar pašreizējiem drošības standartiem, ražošanas vidē ir jāizmanto tālāk norādītie iestatījumi. 

### <a name="hardware-station-installer"></a>Aparatūras stacijas instalētājs
Aparatūras stacijas instalēšanas programma automātiski veic šos reģistra labojumus instalācijas pašapkalpošanās ietvaros.

-   Ir jāatspējo drošligzdu slāņa (SSL) protokols.
-   Drīkst būt iespējota un tikt lietota tikai transporta slāņa drošības (TLS) protokola versija 1.2 (vai jaunākā pašlaik pieejamā versija). 

### <a name="ssl-and-tls"></a>SSL un TLS
Pēc noklusējuma ir atspējots SSL protokols un visas TLS protokola versijas, izņemot TLS 1.2. Lai rediģētu vai iespējotu šīs vērtības, veiciet tālāk norādītās darbības.
    1.  Nospiediet taustiņu kombināciju Windows logotipa taustiņš+R, lai atvērtu logu **Izpildīt**.
    2.  Laukā **Atvērt** ierakstiet **Regedit un** pēc tam atlasiet **Labi**.
    3.  Ja parādās **lietotāja konta kontroles** ziņojuma lodziņš, atlasiet **Jā**.
    4.  Logā **Reģistra redaktors** pārejiet uz ierakstu **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Ir automātiski ievadītas tālāk norādītās atslēgas, lai atļautu tikai TLS 1.2 lietošanu.
        -   TLS 1.2Server:Enabled=1
        -   TLS 1.2Server:DisabledByDefault=0
        -   TLS 1.2Client:Enabled=1
        -   TLS 1.2Client:DisabledByDefault=0
        -   TLS 1.1Server:Enabled=0
        -   TLS 1.1Client:Enabled=0
        -   TLS 1.0Server:Enabled=0
        -   TLS 1.0Client:Enabled=0
        -   SSL 3.0Server:Enabled=0
        -   SSL 3.0Client:Enabled=0
        -   SSL 2.0Server:Enabled=0
        -   SSL 2.0Client:Enabled=0
-   Nav jāatver neviens papildu tīkla ports, ja vien tie nav nepieciešami noteiktu iemeslu dēļ.
-   Ir jāatspējo krusteniskās izcelsmes resursu koplietošana, un ir jānorāda atļautās izcelsmes, kas tiek pieņemtas.
-   Lai iegūtu sertifikātus, kas tiks izmantoti datoros, kuros tiek darbināta aparatūras stacija, drīkst izmantot tikai uzticamas sertificēšanas iestādes.

> [!NOTE]
> Ir ļoti svarīgi pārskatīt IIS drošības vadlīnijas un maksājumu karšu nozares (PCI) prasības.

## <a name="peripheral-simulator"></a>Perifērijas simulators
Informāciju skatiet [Commerce perifēro ierīču simulators](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>Korporācijas Microsoft pārbaudītas perifērijas ierīces
### <a name="ipc-built-in-hardware-station"></a>IPC (iebūvētā) aparatūras stacija

Tālāk norādītās perifērās ierīces ir pārbaudītas, izmantojot IPC aparatūras staciju, kas ir iebūvēta programmā Modern POS operētājsistēmai Windows.

#### <a name="printer"></a>Printeris

| Ražotājs | Modelis    | Interfeiss | Komentāri                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | USB barošana             |
| Star         | TSP650II | Pielāgots    | Tīkla savienojums   |
| Star         | mPOP     | OPOS      | Bluetooth savienojums |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

> [!NOTE]
> Iebūvētajā aparatūras stacijā netiek atbalstīts Star TSP 100 printeris. Iebūvētā aparatūras stacija izmanto 64 bitu procesu, kas nav saderīgs ar esošajiem Star TP 100 draiveriem. 

#### <a name="bar-code-scanner"></a>Svītrkoda skeneris

| Ražotājs  | Modelis         | Interfeiss | Komentāri |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| HP Integrated | E1L07AA       | OPOS      |          |
| Simbols        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Maksājumu termināļi un PIN bloks

Dynamics 365 Commerce nodrošina kastē esošu risinājumu integrācijai ar Amaksājoten maksājumu pakalpojumiem. Dynamics [365 maksājumu savienotājs Ahaen](dev-itpro/adyen-connector.md) izmanto ierīces diagnostiku Aagnostic [Aagnoen Payment Terminal programmas interfeisu (API)](https://www.adyen.com/blog/introducing-the-terminal-api) un var mijiedarboties ar visiem maksājumu termināļiem, ko šis API atbalsta. Pilnīgu atbalstīto maksājumu termināļu sarakstu skatiet [A termināļos A termināļos](https://www.adyen.com/pos-payments/terminals).

Varat izmantot arī citus maksājumu nodrošinātājus, Dynamics 365 Commerce izveidojot pielāgotu savienotāju. Var izmantot jebkuru maksājumu termināli, ko atbalsta maksājumu nodrošinātājs Dynamics 365 Commerce. Tādā veidā tiek atļauts lietot jebkuru maksājumu ierīces integrācijas modeli, ko atbalsta maksājumu sniedzējs, piemēram, Dynamics 365 Commerce lokālais IP, mākoņa API vai tiešais savienojums (piemēram, NO POS). Papildinformāciju skatiet [sadaļā Maksājumu termināļa beigu maksājumu integrācijas izveide](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Naudas kaste

| Ražotājs | Modelis     | Interfeiss | Komentāri                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Bluetooth savienojums |
| APG          | Atwood    | Pielāgot    | Tīkla savienojums   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |
| Epson        |           | Pielāgot    | Savienots ar tīkla Epson printeri, izmantojot DK portu |

#### <a name="line-display"></a>Rindu displejs

| Ražotājs | Modelis    | Interfeiss | Komentāri |
| ------------ | -------- | --------- | -------- |
| Epson        | DM-D110  | OPOS      |          |
| HP           | T sērija | OPOS      |          |

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

| Ražotājs | Modelis    | Interfeiss | Komentāri                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | USB barošana             |
| Star         | TSP650II | Pielāgots    | Tīkla savienojums   |
| Star         | mPOP     | OPOS      | Bluetooth savienojums |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

#### <a name="bar-code-scanner"></a>Svītrkoda skeneris

| Ražotājs  | Modelis         | Interfeiss | Komentāri |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| HP Integrated | E1L07AA       | OPOS      |          |
| Simbols        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Maksājumu termināļi un PIN bloks

Dynamics 365 Commerce nodrošina kastē esošu risinājumu integrācijai ar Amaksājoten maksājumu pakalpojumiem. Dynamics [365 maksājumu savienotājs Aagnosen](dev-itpro/adyen-connector.md) izmanto ierīces diagnostiku Aagnostic [Aagnoen Payment Terminal API](https://www.adyen.com/blog/introducing-the-terminal-api) un var mijiedarboties ar visiem maksājumu termināļiem, kurus šis API atbalsta. Pilnīgu atbalstīto maksājumu termināļu sarakstu skatiet [A termināļos A termināļos](https://www.adyen.com/pos-payments/terminals).

Varat izmantot arī citus maksājumu nodrošinātājus, Dynamics 365 Commerce izveidojot pielāgotu savienotāju. Var izmantot jebkuru maksājumu termināli, ko atbalsta maksājumu nodrošinātājs Dynamics 365 Commerce. Tādā veidā tiek atļauts lietot jebkuru maksājumu ierīces integrācijas modeli, ko atbalsta maksājumu sniedzējs, piemēram, Dynamics 365 Commerce lokālais IP, mākoņa API vai tiešais savienojums (piemēram, NO POS). Papildinformāciju skatiet [sadaļā Maksājumu termināļa beigu maksājumu integrācijas izveide](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Naudas kaste

| Ražotājs | Modelis     | Interfeiss | Komentāri              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Pielāgot    | Tīkla savienojums |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Pielāgot    | Savienots ar tīkla Epson printeri, izmantojot DK portu |

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

| Ražotājs | Modelis    | Interfeiss | Komentāri                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | USB barošana             |
| Star         | mPOP     | OPOS      | Bluetooth savienojums |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

#### <a name="payment-terminal"></a>Maksājumu terminālis

Dynamics 365 Commerce nodrošina kastē esošu risinājumu integrācijai ar Amaksājoten maksājumu pakalpojumiem. Dynamics [365 maksājumu savienotājs Aagnosen](dev-itpro/adyen-connector.md) izmanto ierīces diagnostiku Aagnostic [Aagnoen Payment Terminal API](https://www.adyen.com/blog/introducing-the-terminal-api) un var mijiedarboties ar visiem maksājumu termināļiem, kurus šis API atbalsta. Pilnīgu atbalstīto maksājumu termināļu sarakstu skatiet [A termināļos A termināļos](https://www.adyen.com/pos-payments/terminals).

Varat izmantot arī citus maksājumu nodrošinātājus, Dynamics 365 Commerce izveidojot pielāgotu savienotāju. Var izmantot jebkuru maksājumu termināli, ko atbalsta maksājumu nodrošinātājs Dynamics 365 Commerce. Tādā veidā tiek atļauts lietot jebkuru maksājumu ierīces integrācijas modeli, ko atbalsta maksājumu sniedzējs, piemēram, Dynamics 365 Commerce lokālais IP, mākoņa API vai tiešais savienojums (piemēram, NO POS). Papildinformāciju skatiet [sadaļā Maksājumu termināļa beigu maksājumu integrācijas izveide](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Naudas kaste

| Ražotājs | Modelis     | Interfeiss | Komentāri              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Pielāgot    | Tīkla savienojums |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Pielāgot    | Savienots ar tīkla Epson printeri, izmantojot DK portu |


## <a name="troubleshooting"></a>Problēmu novēršana
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Programma Modern POS var nodrošināt aparatūras stacijas noteikšanu atlases sarakstā, taču nevar nodrošināt savienošanu pārī

**Risinājums:** pārbaudiet tālāk sniegto iespējamo kļūmju sarakstu.

-   Sertifikāts, kas tiek izmantots datorā, kurā tiek darbināta aparatūras stacija, ir iestatīts kā uzticams datorā, kurā tiek darbināta programma Modern POS.
    -   Lai pārbaudītu šos iestatījumus, tīmekļa pārlūkprogrammā apmeklējiet šo URL: https://&lt;Computer Name&gt;:&lt;Port Number&gt;/HardwareStation/ping.
    -   Šis URL izmanto programmu Ping, lai pārbaudītu, vai datoram var piekļūt, un pārlūkprogramma norāda, vai sertifikāts ir uzticams. (Piemēram, adreses Internet Explorer joslā parādās bloķēšanas simbols. Kad izvēlaties šo simbolu, pārbauda, Internet Explorer vai sertifikāts pašlaik ir uzticams. Varat instalēt sertifikātu lokālajā datorā, skatot detalizētu informāciju par parādīto sertifikātu.)
-   Datorā, kurā tiek darbināta aparatūras stacija, ugunsmūrī ir atvērts ports, kas tiks izmantots aparatūras stacijas darbībai.
-   Aparatūras stacijā ir pareizi instalēta tirgotāja informācija, izmantojot rīku Instalēt tirgotāja informāciju, kas tiek palaists aparatūras stacijas instalēšanas programmas darbības beigās.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Programma Modern POS nevar nodrošināt aparatūras stacijas noteikšanu atlases sarakstā

**Risinājums:** šo problēmu var izraisīt jebkurš no tālāk norādītajiem faktoriem.

-   Programmā Headquarters nav pareizi iestatīta aparatūras stacija. Papildinformāciju skatiet sadaļā Retail [aparatūras stacijas konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md#troubleshooting). 
-   Nav palaisti darbi, lai atjauninātu kanāla konfigurāciju. Šādā gadījumā palaidiet kanāla konfigurācijas darbu Nr. 1070.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Programmā Modern POS nav atainoti jaunie naudas kastes iestatījumi

**Risinājums:** slēdziet pašreizējo partiju. Naudas kastes izmaiņas netiek atjauninātas programmā Modern POS, līdz tiek slēgta pašreizējā partija.

### <a name="modern-pos-is-reporting-an-issue-with-a-peripheral"></a>Programmā Modern POS tiek ziņots problēmu ar perifēro ierīci

**Risinājums:** tālāk ir norādīti daži izplatītākie gadījumi, kad rodas šī problēma.

-   Pārliecinieties, ka ir aizvērtas citas ierīču draiveru konfigurēšanas utilītas. Ja šīs utilītas ir atvērtas, tās var traucēt ierīces pieprasīšanu programmā Modern POS vai aparatūras stacijā.
-   Ja perifērā ierīce tiek koplietota vairākās POS ierīcēs, pārliecinieties, ka tā ir ietverta vienā no tālāk norādītajām kategorijām.
    -   Naudas kaste
    -   Kvīšu printeris
    -   Maksājumu terminālis

    Ja perifērā ierīce nav ietverta nevienā no šīm kategorijām, aparatūras stacija nav paredzēta perifērās ierīces koplietošanai vairākās POS ierīcēs.
-   Dažreiz ierīču draiveri var izraisīt vispārīgo vadības objektu (CCO) darbības traucējumus. Ja nesen ir instalēta kāda ierīce, taču tā nedarbojas pareizi vai ir radušās citas problēmas, šo problēmu bieži vien nav novērt, atkārtoti instalējot CCO. Lai lejupielādētu CCO, apmeklējiet vietni <http://monroecs.com/oposccos_current.htm>.
-   Ja pārbaudes vai problēmu novēršanas laikā bieži veicat perifēro ierīču izmaiņas, iespējams, ir nepieciešams atiestatīt IIS, negaidot līdz automātiskai kešatmiņas atsvaidzināšanai. Lai atiestatītu IIS, veiciet tālāk norādītās darbības.
    1.  Izvēlnē **Sākt** ievadiet **CMD**.
    2.  Meklēšanas rezultātos ar peles labo pogu noklikšķiniet uz **Komandu uzvedne** un pēc tam atlasiet Palaist **kā administrators**.
    3.  Logā **Komandu uzvedne** ievadiet **iisreset /Restart** un pēc tam nospiediet taustiņu Enter.
    4.  Pēc IIS restartēšanas restartējiet programmu Modern POS.
-   Ja bieži veicat perifēro ierīču izmaiņas un arī bieži palaižat un izslēdzat POS klientu, iepriekšējās POS sesijas process dllhost var traucēt pašreizējo sesiju. Šādā gadījumā ierīce var būt nelietojama, līdz aizverat dinamisko saišu bibliotēku (DLL) resursu, kas nodrošina iepriekšējās sesijas pārvaldību. Lai aizvērtu DLL resursu, veiciet tālāk norādītās darbības.
    1.  Izvēlnē **Sākt** ievadiet **Uzdevumu pārvaldnieks**.
    2.  Meklēšanas rezultātos atlasiet **Uzdevumu pārvaldnieks**.
    3.  Uzdevumu pārvaldnieka cilnē Detalizēta informācija **atlasiet** kolonnas **virsrakstu**, kam ir iezīme Nosaukums, lai tabulu kārtotu alfabētiski pēc nosaukuma.
    4.  Ritiniet uz leju līdz failam dllhost.exe.
    5.  Atlasiet katru DLL resursdatoru un pēc tam atlasiet **Beigu uzdevums**.
    6.  Kad DLL resursi ir aizvērti, restartējiet programmu Modern POS.


## <a name="additional-resources"></a>Papildu resursi

[Perifērijas simulators programmai Commerce](dev-itpro/retail-peripheral-simulator.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
