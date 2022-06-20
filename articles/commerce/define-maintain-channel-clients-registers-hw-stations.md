---
title: Perifērijas ierīču savienošana ar pārdošanas punktu (POS)
description: Šajā rakstā ir aprakstīts, kā izveidot savienojumu ar jūsu Retail POS perifērijas ierīcēm.
author: BrianShook
ms.date: 03/01/2022
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
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ffee75e1713c7c9d31b1d023cd055c2f1a3fc43d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897112"
---
# <a name="connect-peripherals-to-the-point-of-sale-pos"></a>Perifērijas ierīču savienošana ar pārdošanas punktu (POS)

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot savienojumu ar jūsu Retail POS perifērijas ierīcēm.

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

Navigācija: dodieties uz **Retail un Commerce Channel \> Setup \> POS iestatīšanas \> POS aparatūras \> profiliem**.

Aparatūras profils norāda aparatūru, kas ir pievienota POS kases sistēmā, izmantojot integrētu vai koplietojamu aparatūras staciju. Aparatūras profils tiek arī izmantots, lai norādītu maksājumu apstrādātāja parametrus, kas ir jāizmanto, komunicējot ar maksājumu programmatūras izstrādes komplektu (SDK). Maksājuma SDK tiek izvietots kā daļa no aparatūras stacijas.

### <a name="hardware-station"></a>Aparatūras stacija

Navigācija: dodieties uz **mazumtirdzniecības un komercijas \>\>\>** kanālu veikalu visos veikalos, atlasiet veikalu un pēc tam atlasiet **kopsavilkuma cilni Aparatūras stacijas.**

Aparatūras stacija ir biznesa loģikas instance, kas vada POS perifērijas ierīces. Aparatūras stacija tiek automātiski instalēta kopā ar MPOS. Aparatūras staciju var instalēt arī ka savrupu komponentu, un pēc tam tai var piekļūt ar MPOS vai Cloud POS, izmantojot tīmekļa pakalpojumu. Aparatūras stacijai ir jābūt definētai kanāla līmenī.

## <a name="scenarios"></a>Scenāriji

### <a name="mpos-with-connected-peripheral-devices"></a>MPOS ar pievienotām perifērijas ierīcēm

[![Tradicionāls, fiksēts pārdošanas punkts.](./media/traditional-300x279.png)](./media/traditional.png)

Lai MPOS savienotu ar POS perifērijas ierīcēm tradicionāla, fiksēta POS scenārijā, vispirms pārejiet uz pašu reģistru un piešķiriet tam aparatūras profilu. POS reģistrus varat atrast sadaļā **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **Reģistri**. 

Kad aparatūras profils ir piešķirts, sinhronizējiet izmaiņas ar kanālu datu bāzi, izmantojot sadales grafiku **Reģistri**. Sadales grafikus varat atrast sadaļā **Mazumtirdzniecība un komercija** &gt; **Mazumtirdzniecības un komercijas IT** &gt; **Sadales grafiks**. 

Tālāk iestatiet atvēlētu aparatūras staciju kanālā. Pārejiet uz **sadaļu Mazumtirdzniecības \>\> un Komercijas \> kanāli—** visi veikali un atlasiet veikalu. 

Pēc tam kopsavilkuma cilnē Aparatūras **stacijas** atlasiet **Pievienot**, lai pievienotu aparatūras staciju. Atlasiet **Dedicated** kā aparatūras stacijas veidu un pēc tam ievadiet aprakstu. Lauks **Aparatūras profils** var tikt atstāts tukšs, jo šajā scenārijā izmantotais aparatūras profils tiek saņemts no pašas POS reģistra. Pēc tam sinhronizējiet kanāla izmaiņas, izmantojot kanāla **konfigurācijas** sadales grafiku. Sadales grafikus var atrast mazumtirdzniecības **un tirdzniecības mazumtirdzniecības \> un commerce IT \> sadales grafikā**. 

Visbeidzot MPOS izmantojiet darbību Atlasīt aparatūras staciju, lai atlasītu aparatūras staciju, kas atbilst aprakstam iepriekš ievadīto vērtību, **·** **un iestatiet aparatūras staciju uz Aktīvu.** 

> [!NOTE]
> - Noteiktām aparatūras profila izmaiņām, piemēram, skaidras naudas kastes izmaiņām, ir nepieciešams, lai pēc izmaiņu sinhronizēšanas ar kanālu tiktu atvērta jauna maiņa.
> - Lai sazinātos ar perifērijas ierīcēm, pārdošanas punktam Cloud POS ir jāizmanto savrupa aparatūras stacija.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS vai Cloud POS ar savrupu aparatūras staciju

[![Kopīgas perifērijas ierīces.](./media/shared-300x254.png)](./media/shared.png)

Šajā scenārijā savrupa aparatūras stacija tiek koplietota starp MPOS un Cloud POS klientiem. Šim scenārijam ir nepieciešams izveidot koplietojamu aparatūras staciju un norādīt lejupielādes pakotni, portu un aparatūras profilu, ko izmanto aparatūras stacija. Nosakiet jaunu aparatūras **staciju, atlasot kopsavilkuma cilni Aparatūras stacijas konkrētajā kanālā (** Mazumtirdzniecības un Komercijas **\>\>\> kanāli veikali visos veikalos)** **un pievienojot jaunu koplietotā veida aparatūras** staciju. 

Pēc tam sniedziet aprakstu, kas kasierim palīdzēs identificēt šo aparatūras staciju. Laukā **Resursdatora nosaukums** ievadiet resursdatora vietrādi URL šādā formātā: `https://<MachineName:Port>/HardwareStation`. (Aizstāt **&lt; MachineName:Port&gt;** ar faktisko aparatūras stacijas datora nosaukumu.) Savrupai aparatūras stacijai jānorāda arī elektronisko līdzekļu pārskaitījuma (EFT) termināļa ID. Šī vērtība identificē EFT termināli, kas ir savienots ar aparatūras staciju, kad maksājumu savienotājs sazinās ar maksājuma nodrošinātāju. 

Pēc tam datorā, kas viesos aparatūras staciju, dodieties uz programmas Headquarters kanālu un atlasiet aparatūras staciju. Pēc tam atlasiet **Lejupielādēt**, lai lejupielādētu aparatūras stacijas instalētāju un instalētu aparatūras staciju. Papildinformāciju par aparatūras stacijas instalēšanu skatiet sadaļā Retail [aparatūras stacijas konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md). 

Pēc tam no MPOS vai Cloud POS izmantojiet operāciju **Atlasīt aparatūras staciju**, lai atlasītu iepriekš instalēto aparatūras staciju. Atlasiet vienumu **Savienot pārī**, lai izveidotu drošas attiecības starp POS un aparatūras staciju. Šī darbība ir jāizpilda vienu reizi katrai POS un aparatūras stacijas kombinācijai. 

Kad aparatūras stacija ir savienota pārī, tāda pati operācija tiek izmantota, lai aktivizētu aparatūras staciju, kamēr tā tiek izmantota. Šajā scenārijā aparatūras profils ir jāpiešķir koplietojamajā aparatūras stacijā, nevis pašā kases sistēmā. Ja kāda iemesla dēļ aparatūras stacijai nav piešķirts neviens aparatūras profils, tiks izmantots kases sistēmā piešķirtais aparatūras profils.

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

    - Norādiet kvīšu numerācijas maskas, kas var ietvert veikala numura, termināļa numura, konstantes un vai pārdošana, atgriešanas, pārdošanas pasūtījumi un piedāvājumi tiek drukāti atsevišķās secībās, vai arī tās visas seko tai pašai sērijai.

#### <a name="receipt-profiles"></a>Kvīšu profili

Kvīšu profili tiek piešķirti printeriem aparatūras profilā. Tie tiek lietoti, lai norādītu konkrētā printerī drukāto kvīšu tipus. Šie profili ietver iestatījumus kvīšu formātiem un iestatījumus, kas nosaka, vai kvīts tiek drukāta vienmēr, vai arī kasierim tiek lūgts izlemt vai drukāt kvīti. Dažādi printeri var arī lietot dažādus kvīšu profilus. Piemēram, 1. printeris ir standarta termināļa saņemšanas printeris, un tādēļ tam ir mazāki kvīšu formāti. Savukārt 2. printeris ir pilna izmēra kvīšu printeris, kas tiek izmantots, lai drukātu tikai debitoru pasūtījumu kvītis, kurām ir nepieciešams vairāk vietas. Papildinformāciju skatiet sadaļā [Kvīts profila konfigurēšana](configure-emailed-receipt-formats.md#configure-a-receipt-profile).

#### <a name="hardware-profiles"></a>Aparatūras profili

Iepriekš šajā rakstā aparatūras profili tiek skaidroti kā komponents klienta iestatīšanai. Aparatūras profili tiek piešķirti tieši POS kases sistēmā vai koplietojamajā aparatūras stacijā, un tiek izmantoti, lai norādītu ierīču veidus, ko izmanto konkrēta POS kases sistēmas vai aparatūras stacija. Aparatūras profili tiek arī izmantoti, lai norādītu EFT iestatījumus, kuri tiek izmantoti, lai sazinātos ar maksājumu SDK.

#### <a name="visual-profiles"></a>Vizuālie profili

Vizuālie profili tiek izmantoti, lai norādītu specifiska reģistra tēmu un tiek piešķirti reģistra līmenī. Profilos ir ietverti izmantotās programmas tipa (MPOS vai Cloud POS) iestatījumi, izcēluma krāsa un tēma, fonta shēma, pierakstīšanās lapas fonā un POS fons. Papildinformāciju skatiet pārdošanas [punkta (POS) vizuālo profilu izveidošana](tasks/create-pos-visual-profile-2016-02.md). 

### <a name="custom-fields"></a>Pielāgotie lauki

Varat izveidot pielāgotus laukus, lai pievienotu laukus, kas nav iekļauti standarta POS. Plašāku informāciju par to, kā lietot pielāgotus laukus, skatiet emuāra ziņā [Darbs ar pielāgotiem laukiem](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Valodas teksts

Varat pārrakstīt POS noklusējuma virknes, izmantojot valodas teksta ierakstus. Lai pārdošanas punktā pārrakstītu kādu virkni, pievienojiet jaunu valodas teksta rindu. Pēc tam norādiet ID, pārrakstāmo noklusējuma virkni un tekstu, kas pārdošanas punktā POS ir jārāda šīs noklusējuma virknes vietā.

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

## <a name="additional-resources"></a>Papildu resursi

[Retail Hardware Station konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
