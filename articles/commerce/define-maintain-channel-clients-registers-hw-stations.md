---
title: Perifērijas ierīču savienošana ar pārdošanas punktu (POS)
description: Šajā tēmā ir izklāstīts, kā perifērijas ierīces savienot ar jūsu Retail POS.
author: rubencdelgado
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 64b228954c040050f605d60cd416c112f3b12e25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802049"
---
# <a name="connect-peripherals-to-the-point-of-sale-pos"></a>Perifērijas ierīču savienošana ar pārdošanas punktu (POS)

[!include [banner](includes/banner.md)]

Šajā tēmā ir izklāstīts, kā perifērijas ierīces savienot ar jūsu Retail POS.

> [!NOTE]
> Lai iegūtu informāciju par noteiktiem instalēšanas norādījumiem, skatiet sadaļu [Retail aparatūras stacijas konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md) un [Modern POS (MPOS) konfigurēšana, instalēšana un aktivizēšana](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Galvenie komponenti

Lai definētu attiecības starp veikalu, pārdošanas punktu (POS) reģistriem vai kanāliem veikalā, un perifērijas ierīcēm, kas šos reģistrus vai kanālus lieto, lai apstrādātu transakcijas, tiek izmantoti vairāki komponenti. Šajā sadaļā ir aprakstīts katrs komponents un paskaidrots, kā tas ir jāizmanto veikalu izvietošanā.

### <a name="pos-registers"></a>POS kases sistēmas

Navigācija: noklikšķiniet uz **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatījumi** &gt; **POS iestatījumi** &gt; **Reģistri**.

POS reģistrs ir elements, kurš tiek izmantots konkrētas POS instances raksturlielumu definēšanai. Šie raksturlielumi ietver aparatūras profilu jeb ar kases sistēmu izmantoto perifērijas ierīču iestatījumus, veikalu, ar kuru ir kartēta šī kases sistēma, un vizuālo noformējumu, ko redz lietotājs, kurš pierakstās šajā kases sistēmā.

### <a name="devices"></a>Ierīces

Navigācija: noklikšķiniet uz **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatījumi** &gt; **POS iestatījumi** &gt; **Ierīces**.

Ierīce ir elements, kas pārstāv fizisku instanci tādai ierīcei, kura ir kartēta uz POS reģistru. Kad ierīce tiek izveidota, tā tiek kartēta uz POS reģistru. Ierīces elements seko līdzi informācijai par laiku, kad POS reģistrs tiek aktivizēts, par izmantotā klienta tipu, kā arī par programmu pakotni, kas ir izvietota konkrētā ierīcē. Ierīces var būt divu veidu: **Retail modern POS** (MPOS) vai **Retail Cloud POS** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS ir POS klienta programma, kas ir instalēta operētājsistēmā Windows 8.1 vai jaunākā personālā datora (PC) operētājsistēmā. Ja programmas tips **Retail Modern POS** ir kartēts uz kādu ierīci, tad lejupielādes pakotni var norādīt konkrētai ierīcei. Šo lejupielādes pakotni var pielāgot, lai iekļautu dažādas instalācijas pakotnes versijas. Spēja izvietot dažādas pakotnes nodrošina elastību gadījumos, kad dažādiem POS reģistriem var būt nepieciešamas dažādas integrācijas. Pārdošanas punkts MPOS tiek izvietots kopā ar iebūvētu aparatūras staciju.

#### <a name="cloud-pos"></a>Cloud POS

Cloud POS ir pārlūkprogrammā pieejams POS. Tā kā tas darbojas pārlūkprogrammā, pārdošanas punktam Cloud POS nav nepieciešama Windows 8.1 vai jaunāka personālā datora (PC) operētājsistēma. Ja programmas veids **Retail Cloud POS** ir kartēts ar noteiktu ierīci modulī Headquarters, šo ierīci var izmantot, lietojot pārlūkprogrammu, un nav nepieciešams lejupielādēt vai instalēt pakotni. Lai lietotu aparatūru, kas pārsniedz svītrkoda skenera iespējas, pārdošanas punktam Cloud POS ir nepieciešama aparatūras stacija.

### <a name="hardware-profile"></a>Aparatūras profils

Navigācija: noklikšķiniet uz **Komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profili** &gt; **Aparatūras profili**.

Aparatūras profils identificē aparatūru, kas ir savienota ar POS reģistru vai aparatūras staciju. Aparatūras profils tiek arī izmantots, lai norādītu maksājumu apstrādātāja parametrus, kas ir jāizmanto, komunicējot ar maksājumu programmatūras izstrādes komplektu (SDK). (Maksājumu SDK tiek izvietots kā daļa no aparatūras stacijas.)

### <a name="hardware-station"></a>Hardware Station

Navigācija: noklikšķiniet uz **Mazumtirdzniecība un komercija** &gt; **Kanāli** &gt; **Veikali** &gt; **Visi mazumtirdzniecības veikali**. Atlasiet veikalu un pēc tam noklikšķiniet uz kopsavilkuma cilnes **Aparatūras stacijas**.

Aparatūras stacija ir biznesa loģikas instance, kas vada POS perifērijas ierīces. Aparatūras stacija tiek automātiski instalēta kopā ar MPOS. Aparatūras staciju var instalēt arī ka savrupu komponentu, un pēc tam tai var piekļūt ar MPOS vai Cloud POS, izmantojot tīmekļa pakalpojumu. Aparatūras stacijai ir jābūt definētai kanāla līmenī.

### <a name="hardware-station-profile"></a>Aparatūras stacijas profils

Navigācija: noklikšķiniet uz **Komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profili** &gt; **Aparatūras stacijas profili**.

Kamēr pati aparatūra stacija tiek norādīta kanāla līmenī un ietver instancei raksturīgu informāciju, piemēram, aparatūras stacijas vietrādi URL, aparatūras stacijas profils ietver informāciju, kas var būt statiska vai kopīga vairākām aparatūras stacijām. Statiskā informācija ietver portu, kas ir jāizmanto, aparatūras staciju pakotni un aparatūras profilu. Statiskā informācijā ietver arī aprakstu par izvietojamās aparatūra stacijas tipu, piemēram, **Norēķināšanās** vai **Atgriešana**, atkarībā no aparatūras, kas ir nepieciešama katrai konkrētajai aparatūras stacijai.

## <a name="scenarios"></a>Scenāriji

### <a name="mpos-with-connected-peripheral-devices"></a>MPOS ar pievienotām perifērijas ierīcēm

[![Tradicionāls, fiksēts pārdošanas punkts](./media/traditional-300x279.png)](./media/traditional.png)

Lai MPOS savienotu ar POS perifērijas ierīcēm tradicionāla, fiksēta POS scenārijā, vispirms pārejiet uz pašu reģistru un piešķiriet tam aparatūras profilu. POS reģistrus varat atrast sadaļā **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **Reģistri**. 

Kad aparatūras profils ir piešķirts, sinhronizējiet izmaiņas ar kanālu datu bāzi, izmantojot sadales grafiku **Reģistri**. Sadales grafikus varat atrast sadaļā **Mazumtirdzniecība un komercija** &gt; **Mazumtirdzniecības un komercijas IT** &gt; **Sadales grafiks**. 

Pēc tam iestatiet kanālā “lokālo” aparatūras staciju. Noklikšķiniet uz **Mazumtirdzniecība un komercija** &gt; **Kanāli** &gt; **Veikali** &gt; **Visi mazumtirdzniecības veikali** un atlasiet kādu veikalu. 

Pēc tam kopsavilkuma cilnē **Aparatūras stacijas** noklikšķiniet uz **Pievienot**, lai pievienotu kādu aparatūras staciju. Ievadiet aprakstu, kā resursdatora nosaukumu ievadiet **localhost** un pēc tam sinhronizējiet izmaiņas ar kanālu, izmantojot sadales grafiku **Kanāla konfigurācija**. Sadales grafikus varat atrast sadaļā **Mazumtirdzniecība un komercija** &gt; **Mazumtirdzniecības un komercijas IT** &gt; **Sadales grafiks**. 

Visbeidzot pārdošanas punktā MPOS izmantojiet operāciju **Atlasīt aparatūras staciju**, lai atlasītu aparatūras staciju **localhost**. Iestatiet aparatūras staciju uz **Aktīvs**. Aparatūras profilam, kas tiek izmantots šajā scenārijā, ir jānāk no paša POS reģistra. Šim scenārijam nav nepieciešams aparatūras stacijas profils.

> [!NOTE]
> Noteiktām aparatūras profila izmaiņām, piemēram, skaidras naudas kastes izmaiņām, ir nepieciešams, lai pēc izmaiņu sinhronizēšanas ar kanālu tiktu atvērta jauna maiņa.
>
> Lai sazinātos ar perifērijas ierīcēm, pārdošanas punktam Cloud POS ir jāizmanto savrupa aparatūras stacija.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS vai Cloud POS ar savrupu aparatūras staciju

[![Kopīgas perifērijas ierīces](./media/shared-300x254.png)](./media/shared.png)

Šādā scenārijā savrupu aparatūras staciju kopīgi lieto MPOS un Cloud POS klienti. Šim scenārijam ir nepieciešams, lai jūs izveidotu aparatūras stacijas profilu, lai norādītu lejupielādes pakotni, portu un aparatūras profilu, kurus šī aparatūras stacija izmanto. Aparatūras stacijas profilu varat atrast sadaļā **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatīša** &gt; **POS iestatīšana** &gt; **POS profili** &gt; **Aparatūras stacijas profili**. 

Kad esat izveidojis aparatūras stacijas profilu, pārejiet uz konkrēto kanālu (**Mazumtirdzniecība un komercija** &gt; **Kanāli** &gt; **Veikali** &gt; **Visi veikali**) un pievienojiet jaunu aparatūras staciju. Šo jauno aparatūras staciju kartējiet uz iepriekš izveidoto aparatūras stacijas profilu. 

Pēc tam sniedziet aprakstu, kas kasierim palīdzēs identificēt šo aparatūras staciju. Laukā **Resursdatora nosaukums** ievadiet resursdatora vietrādi URL šādā formātā: `https://<MachineName:Port>/HardwareStation`. (Ierakstu **&lt;MachineName:Port&gt;** aizstājiet ar aparatūras stacijas faktisko iekārtas nosaukumu un portu, kas ir norādīts aparatūras stacijas profilā.) Savrupai aparatūras stacijai ir jānorāda arī elektronisko līdzekļu pārskaitījumu (electronic funds transfer — EFT) termināļa ID. Šī vērtība identificē EFT termināli, kas ir savienots ar aparatūras staciju, kad maksājumu savienotājs sazinās ar maksājuma nodrošinātāju. 

Pēc tam no faktiskās aparatūras stacijas iekārtas pārejiet uz kanālu un atlasiet aparatūras staciju. Pēc tam noklikšķiniet uz **Lejupielādēt** un instalējiet aparatūras staciju. 

Pēc tam no MPOS vai Cloud POS izmantojiet operāciju **Atlasīt aparatūras staciju**, lai atlasītu iepriekš instalēto aparatūras staciju. Atlasiet vienumu **Savienot pārī**, lai izveidotu drošas attiecības starp POS un aparatūras staciju. Šī darbība ir jāizpilda vienu reizi katrai POS un aparatūras stacijas kombinācijai. 

Kad aparatūras stacija ir savienota pārī, tāda pati operācija tiek izmantota, lai aktivizētu aparatūras staciju, kamēr tā tiek izmantota. Šajā scenārijā aparatūras profils ir jāpiešķir aparatūras stacijas profilam, nevis pašam reģistram. Ja kaut kādu iemeslu dēļ aparatūras stacijai nav tieši piešķirts aparatūras profils, tad tiek izmantots reģistram piešķirtais aparatūras profils.

## <a name="client-maintenance"></a>Klienta uzturēšana

### <a name="registers"></a>Reģistri

POS reģistri galvenokārt tiek pārvaldīti, izmantojot pašus reģistrus, kā arī reģistriem piešķirtos profilus. Atsevišķam reģistram specifiskie atribūti tiek pārvaldīti reģistra līmenī. Šie atribūti ietver veikalu, kur reģistrs tiek lietots, reģistrācijas numuru, aprakstu un EFT termināļa ID, kas ir specifiski pašam reģistram.

### <a name="pos-profiles"></a>POS profili

POS profilus varat atrast sadaļā **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profili**. Daudzus reģistru aspektus var būt noderīgi pārvaldīt, izmantojot profilus, jo profilus var kopīgi lietot daudzi reģistri. Profilus var kartēt uz atsevišķu reģistru vai — ja profils ir spēkā visā veikalā — uz veikalu. Nākamajās sadaļās ir aprakstīti POS profili un to lietošana.

#### <a name="offline-profile"></a>Bezsaistes profils

Bezsaistes profils tiek iestatīts veikala līmenī. Tas tiek izmantots, lai norādītu augšupielādes iestatījumus transakcijām, kas tiek veiktas POS reģistrā, kamēr šim reģistram nav savienojuma ar kanālu datu bāzi.

#### <a name="functionality-profile"></a>Funkcionalitātes profils

Funkcionalitātes profils tiek iestatīts veikala līmenī. Tas tiek izmantots, lai norādītu visa veikala iestatījumus par funkcijām, kuras var izpildīt šajā POS. Ar funkcionalitātes profilu tiek pārvaldītas tālāk uzskaitītās iespējas. Šīs iespējas ir sakārtotas pēc kopsavilkuma cilnes.

- Kopsavilkuma cilne **Vispārīgi**.

    - Starptautiskā Standartizācijas organizācija (ISO).
    - Izveidot debitoru bezsaistes režīmā.
    - E-pasta kvīts profils.
    - Centrālā darbinieku pieteikšanās autentifikācija.

- Kopsavilkuma cilne **Funkcijas**.

    - Pieteikšanās un paplašinātās pieteikšanās pārvaldība.
    - Ar finansēm un valūtu saistīti POS aspekti, piemēram, iespēja ievadīt cenas un definēšana, vai aiz mazām valūtas vienībām ir nepieciešami decimāldaļskaitļi.
    - Laika reģistrācijas iespējošana, izmantojot POS.
    - Kā preces un maksājumi tiek rādīti šajā POS un kvītīs.
    - Darbadienas beigu pārvaldība.
    - Kanāla datu bāzes transakciju paturēšanas parametri.
    - Kā no šī POS tiek uzmeklēti un izveidoti debitori.
    - Kā tiek aprēķinātas atlaides.

- Kopsavilkuma cilne **Summa**.

    - Maksimālās un minimālās atļautās cenas.
    - Atlaižu lietojums un aprēķins.

- Kopsavilkuma cilne **Informācijas kodi**.

    - Visos aspekti par to, kā šajā POS tiek pārvaldīti informācijas kodi. Plašāku informāciju skatiet tēmā [Informācijas kodi un informācijas kodu grupas](info-codes-retail.md).

- Kopsavilkuma cilne **Kvīšu numerācija**.

    - Norādiet kvīšu numerācijas maskas, kas varētu ietvert segmentu veikala numuram, termināļa numuram, konstantēm, kā arī norādiet, vai pārdošana, atgriešana, pārdošanas pasūtījumi un piedāvājumi tiek drukāti atsevišķās sērijās, vai arī tiem visiem tiek izmantota tā pati sērija.

#### <a name="receipt-profiles"></a>Kvīšu profili

Kvīšu profili tiek piešķirti printeriem aparatūras profilā. Tie tiek lietoti, lai norādītu konkrētā printerī drukāto kvīšu tipus. Šie profili ietver iestatījumus kvīšu formātiem un iestatījumus, kas nosaka, vai kvīts tiek drukāta vienmēr, vai arī kasierim tiek lūgts izlemt vai drukāt kvīti. Dažādi printeri var arī lietot dažādus kvīšu profilus. Piemēram, 1. printeris ir standarta termināļa saņemšanas printeris, un tādēļ tam ir mazāki kvīšu formāti. Savukārt 2. printeris ir pilna izmēra kvīšu printeris, kas tiek izmantots, lai drukātu tikai debitoru pasūtījumu kvītis, kurām ir nepieciešams vairāk vietas.

#### <a name="hardware-profiles"></a>Aparatūras profili

Iepriekš šajā rakstā aparatūras profili tiek skaidroti kā komponents klienta iestatīšanai. Aparatūras profili tiek tieši piešķirti POS reģistram vai aparatūras stacijas profilam. Tie tiek izmantoti, lai norādītu ierīču tipus, ko izmanto konkrēts POS reģistrs vai aparatūras stacija. Aparatūras profili tiek arī izmantoti, lai norādītu EFT iestatījumus, kuri tiek izmantoti, lai sazinātos ar maksājumu SDK.

#### <a name="visual-profiles"></a>Vizuālie profili

Vizuālie profili tiek piešķirti reģistra līmenī. Tie tiek izmantoti, lai norādītu konkrēta reģistra dizainu. Profilos ietilpst iestatījumi izmantotās programmas tipam (MPOS vai Cloud POS), izcelšanas krāsai un dizainam, fontu shēmai, pieteikšanās fonam un POS fonam.

### <a name="custom-fields"></a>Pielāgotie lauki

Varat izveidot pielāgotus laukus, lai pievienotu laukus, kas nav iekļauti standarta POS. Plašāku informāciju par to, kā lietot pielāgotus laukus, skatiet emuāra ziņā [Darbs ar pielāgotiem laukiem](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Valodas teksts

Varat pārrakstīt POS noklusējuma virknes, izmantojot valodas teksta ierakstus. Lai pārdošanas punktā pārrakstītu kādu virkni, pievienojiet jaunu valodas teksta rindu. Pēc tam norādiet ID, pārrakstāmo noklusējuma virkni un tekstu, kas pārdošanas punktā POS ir jārāda šīs noklusējuma virknes vietā.

### <a name="hardware-station-profiles"></a>Aparatūras stacijas profili

Aparatūras stacijas profili ir paskaidroti agrāk šajā rakstā. Tie tiek izmantoti, lai aparatūras stacijām piešķirtu no instances neatkarīgu informāciju.

### <a name="channel-reports-configuration"></a>Kanālu pārskatu konfigurācija

Atskaites, kas ir pieejamas mazumtirdzniecības kanālā, jūs iestatāt lapā **Kanālu atskaišu konfigurācija**. Varat izveidot jaunas atskaites, norādot atskaites XML definīciju un piešķirot šo atskaiti konkrētai atļauju grupai šajā POS.

### <a name="devices"></a>Ierīces

Ierīces ir paskaidrotas agrāk šajā rakstā. Tās tiek izmantotas, lai pārvaldītu konkrēta POS reģistra aktivizēšanu. Ierīces tiek arī izmantotas, lai norādītu programmu, kas tiek lietota konkrētam reģistram, un instalācijas pakotni, kas ir jāizmanto, lai instalētu MPOS klientu. Tālāk ir uzskaitīti ierīces aktivizēšanas stāvokļi.

- **Gaidošs** — ierīce ir gatava aktivizēšanai.
- **Aktivizēts** — ierīce ir aktivizēta.
- **Deaktivizēts** — ierīce ir deaktivizēta modulī Headquarters vai POS.
- **Atspējots** — ierīce ir atspējota.

Ar aktivizēšanu saistītā papildinformācija ietver darbinieku, kurš mainīja ierīces aktivizēšanas statusu, aktivizēšanas laikspiedolu un to, vai šīs ierīces konfigurācija tika validēta.

### <a name="client-data-synchronization"></a>Klienta datu sinhronizācija

Visas izmaiņas POS klientā, izņemot izmaiņas ierīces aktivizēšanas statusā, ir nepieciešams sinhronizēt ar kanālu datu bāzi, lai tās stātos spēkā. Lai izmaiņas sinhronizētu ar kanālu datu bāzi, dodieties uz **Mazumtirdzniecība un komercija** &gt; **Mazumtirdzniecības un komercijas IT** &gt; **Sadales grafiks** un palaidiet nepieciešamo sadales grafiku. Lai sinhronizētu klienta datu izmaiņas, jums ir jāpalaiž sadales grafiki **Reģistri** and **Kanāla konfigurācija**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]