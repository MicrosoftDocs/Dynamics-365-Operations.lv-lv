---
title: "Nosaka un uztur kanālu klientiem, reģistrus un aparatūras stacijas"
description: "Šajā vikirakstā ir izklāstīts, kā perifērijas ierīces savienot ar jūsu Retail POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dee5745670ad86000795f2913f99f49c0f123a00
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Nosaka un uztur kanālu klientiem, reģistrus un aparatūras stacijas

Šajā vikirakstā ir izklāstīts, kā perifērijas ierīces savienot ar jūsu Retail POS.

**Piezīme:** Konkrētas instalēšanas instrukcijas skatiet rakstā [Retail aparatūras stacijas konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md) un [Retail Modern POS pašapkalpošanās lejupielādēšana/instalēšana, un Modern POS un Cloud POS ierīces aktivizēšana](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Galvenie komponenti
Lai definētu attiecības starp veikalu, pārdošanas punktu (POS) reģistriem vai kanāliem veikalā, un mazumtirdzniecības perifērijas ierīcēm, kas šos reģistrus vai kanālus lieto, lai apstrādātu transakcijas, tiek izmantoti vairāki komponenti. Šajā sadaļā ir aprakstīts katrs komponents un paskaidrots, kā tas ir jāizmanto mazumtirdzniecības veikalu izvietošanā.

### <a name="pos-registers"></a>POS kases sistēmas

Navigācija: Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**reģistrē**. POS reģistrs ir vienība, ko izmanto, lai noteiktu konkrētu gadījumu POS raksturlielumus. Šie raksturlielumi ietver aparatūras profilu vai uzstādīšanas mazumtirdzniecības perifērijas ierīcēm, ko izmantos reģistru, veikalā, ka reģistrā tiek kartēts uz un vizuālo pieredzi lietotājam, kas piesakās, ka reģistrā.

### <a name="devices"></a>Ierīces

Navigācija: Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**ierīces**. Ierīce ir elements, kas pārstāv fizisku instanci tādai ierīcei, kura ir kartēta uz POS reģistru. Kad ierīce tiek izveidota, tā tiek kartēta uz POS reģistru. Ierīces elements seko līdzi informācijai par laiku, kad POS reģistrs tiek aktivizēts, par izmantotā klienta tipu, kā arī par programmu pakotni, kas ir izvietota konkrētā ierīcē. Ierīces var būt divu veidu: **Retail Modern POS** (MPOS) vai **Retail Cloud POS** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS ir POS klienta programma, kas ir instalēta operētājsistēmā Windows 8.1 vai jaunākā personālā datora (PC) operētājsistēmā. Ja programmas tips **Retail Modern POS** ir kartēts uz kādu ierīci, tad lejupielādes pakotni var norādīt konkrētai ierīcei. Šo lejupielādes pakotni var pielāgot, lai iekļautu dažādas instalācijas pakotnes versijas. Spēja izvietot dažādas pakotnes nodrošina elastību gadījumos, kad dažādiem POS reģistriem var būt nepieciešamas dažādas integrācijas. Pārdošanas punkts MPOS tiek izvietots kopā ar iebūvētu aparatūras staciju.

#### <a name="cloud-pos"></a>Cloud POS

Mākonis POS ir pārlūka balstīts POS. Jo tā darbojas pārlūkprogrammā, mākonis POS neprasa Windows 8.1 vai jaunāka PC balstīta operētājsistēma. Ja programmas tips **Retail Cloud POS** ir kartēts uz noteiktu ierīci apstrādes birojā, šo ierīci var lietot, izmantojot pārlūkprogrammu, un nav nepieciešams lejupielādēt vai instalēt pakotni. Lai lietotu aparatūru, kas pārsniedz svītrkoda skenera iespējas, pārdošanas punktam Cloud POS ir nepieciešama aparatūras stacija.

### <a name="hardware-profile"></a>Aparatūras profils

Navigācija: Noklikšķiniet uz **Commerce**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**POS profili**&gt;**Hardware Profili**. Aparatūras profils identificē aparatūru, kas ir savienota ar POS reģistru vai aparatūras staciju. Aparatūras profils tiek arī izmantots, lai norādītu maksājumu apstrādātāja parametrus, kas ir jāizmanto, komunicējot ar maksājumu programmatūras izstrādes komplektu (SDK). (Maksājumu SDK tiek izvietots kā daļa no aparatūras stacijas.)

### <a name="hardware-station"></a>Aparatūras stacija

Navigācija: Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**kanālus**&gt;**mazumtirdzniecības veikali**&gt;**visiem mazumtirdzniecības veikali**. Atlasiet veikalu un pēc tam noklikšķiniet uz kopsavilkuma cilnes **Aparatūras stacijas**. Aparatūras stacija ir biznesa loģikas instance, kas vada POS perifērijas ierīces. Aparatūras stacija tiek automātiski instalēta kopā ar MPOS. Aparatūras staciju var instalēt arī ka savrupu komponentu, un pēc tam tai var piekļūt ar MPOS vai Cloud POS, izmantojot tīmekļa pakalpojumu. Aparatūras stacijai ir jābūt definētai kanāla līmenī.

### <a name="hardware-station-profile"></a>Aparatūras stacijas profils

Navigācija: Noklikšķiniet uz **Commerce**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**POS profili**&gt;**stacijas aparatūras profili**. Kamēr pati aparatūra stacija tiek norādīta kanāla līmenī un ietver instancei raksturīgu informāciju, piemēram, aparatūras stacijas vietrādi URL, aparatūras stacijas profils ietver informāciju, kas var būt statiska vai kopīga vairākām aparatūras stacijām. Statiskā informācija ietver portu, kas ir jāizmanto, aparatūras staciju pakotni un aparatūras profilu. Statiskā informācijā ietver arī aprakstu par izvietojamās aparatūra stacijas tipu, piemēram, **Norēķināšanās **vai **Atgriešana**, atkarībā no aparatūras, kas ir nepieciešama katrai konkrētajai aparatūras stacijai.

## <a name="scenarios"></a>Scenāriji
### <a name="mpos-with-connected-peripheral-devices"></a>MPOS ar pievienotām perifērijas ierīcēm

[![Tradicionālā, fiksēta tirdzniecības vietai](./media/traditional-300x279.png)](./media/traditional.png) pieslēgties MPOS POS perifērijas tradicionālo fiksēto POS scenāriju, vispirms naviģējiet uz reģistru, pats par sevi, un piešķirt aparatūras profilu. Jūs varat atrast pie POS reģistros **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**reģistrē**. Kad aparatūras profils ir piešķirts, sinhronizējiet izmaiņas ar kanālu datu bāzi, izmantojot sadales grafiku “Reģistri”. Jūs varat atrast pie izplatīšanas grafikus **mazumtirdzniecības un komercijas**&gt;**mazumtirdzniecības tā**&gt;**sadalījuma grafiks**. Pēc tam iestatiet kanālā “lokālo” aparatūras staciju. Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**kanālus**&gt;**mazumtirdzniecības veikali**&gt;**visiem mazumtirdzniecības veikali**, un jāizvēlas veikals. Pēc tam kopsavilkuma cilnē **Aparatūras stacijas** noklikšķiniet uz **Pievienot**, lai pievienotu kādu aparatūras staciju. Ievadiet aprakstu, kā resursdatora nosaukumu ievadiet **localhost** un pēc tam sinhronizējiet izmaiņas uz kanālu, izmantojot sadales grafiku “Kanāla konfigurācija”. Jūs varat atrast pie izplatīšanas grafikus **mazumtirdzniecības un komercijas**&gt;**mazumtirdzniecības tā**&gt;**sadalījuma grafiks**. Visbeidzot pārdošanas punktā MPOS izmantojiet operāciju **Atlasīt aparatūras staciju**, lai atlasītu aparatūras staciju **localhost**. Iestatiet aparatūras staciju uz **Aktīvs**. Aparatūras profilam, kas tiek izmantots šajā scenārijā, ir jānāk no paša POS reģistra. Šim scenārijam nav nepieciešams aparatūras stacijas profils. **Piezīme.** Noteiktām aparatūras profila izmaiņām, piemēram, skaidras naudas kastes izmaiņām, ir nepieciešams, lai pēc izmaiņu sinhronizēšanas ar kanālu tiktu atvērta jauna maiņa. **Piezīme.** Lai sazinātos ar mazumtirdzniecības perifērijas ierīcēm, pārdošanas punktam Cloud POS ir jāizmanto savrupa aparatūras stacija.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS vai Cloud POS ar savrupu aparatūras staciju

\[Caption id = "pielikumu\_340041" izlīdzināt = "alignleft" width = "300"\][![kopīgi perifērijas](./media/shared-300x254.png)](./media/shared.png) kopīgi perifērijas\[/parakstu\] šādā gadījumā atsevišķa aparatūras stacija tiek koplietota MPOS un mākonis POS pacientu vidū. Šim scenārijam ir nepieciešams, lai jūs izveidotu aparatūras stacijas profilu, lai norādītu lejupielādes pakotni, portu un aparatūras profilu, kurus šī aparatūras stacija izmanto. Staciju aparatūras profilu, var atrast **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**POS profili**&gt;**stacijas aparatūras profili**. Pēc tam, kad esat izveidojis staciju aparatūras profilu, naviģējiet uz specifiskiem mazumtirdzniecības kanāls (**mazumtirdzniecības un komercijas**&gt;**kanālus**&gt;**mazumtirdzniecības veikali**&gt;**visiem mazumtirdzniecības veikali**), un pievienot jaunu aparatūru staciju. Šo jauno aparatūras staciju kartējiet uz iepriekš izveidoto aparatūras stacijas profilu. Pēc tam sniedziet aprakstu, kas kasierim palīdzēs identificēt šo aparatūras staciju. Šajā **resursdatora nosaukumu** laukā, ievadiet uzņēmēja mašīna vietrādi URL šādā formātā: **https://&lt;MachineName:Port&gt;/HardwareStation**. (Aizstāt **&lt;MachineName:Port&gt;** ar nosaukumu faktiskā mašīnu stacijas aparatūru un ostā, kas norādīta stacijas aparatūras profilu.) Atsevišķa aparatūras stacijas, vajadzētu norādīt arī elektronisko līdzekļu transfer (EFT) termināļa ID. Šī vērtība identificē EFT termināli, kas ir savienots ar aparatūras staciju, kad maksājumu savienotājs sazinās ar maksājuma nodrošinātāju. Pēc tam no faktiskās aparatūras stacijas iekārtas pārejiet uz kanālu un atlasiet aparatūras staciju. Pēc tam noklikšķiniet uz **Lejupielādēt** un instalējiet aparatūras staciju. Pēc tam no MPOS vai Cloud POS izmantojiet operāciju **Atlasīt aparatūras staciju**, lai atlasītu iepriekš instalēto aparatūras staciju. Atlasiet vienumu **Savienot pārī**, lai izveidotu drošas attiecības starp POS un aparatūras staciju. Šī darbība ir jāizpilda vienu reizi katrai POS un aparatūras stacijas kombinācijai. Kad aparatūras stacija ir savienota pārī, tāda pati operācija tiek izmantota, lai aktivizētu aparatūras staciju, kamēr tā tiek izmantota. Šī scenārija aparatūras profilu jāpiešķir staciju aparatūras profilu, nevis pats reģistrs. Ja kādu iemeslu dēļ aparatūras stacijas nav tieši piešķirtas aparatūras profilu, tad piešķirts reģistra aparatūras profils tiek lietots

## <a name="client-maintenance"></a>Klienta uzturēšana
### <a name="registers"></a>Reģistri

POS reģistri galvenokārt tiek pārvaldīti, izmantojot pašus reģistrus, kā arī reģistriem piešķirtos profilus. Atsevišķam reģistram specifiskie atribūti tiek pārvaldīti reģistra līmenī. Šie atribūti ietver veikalu, kur reģistrs tiek lietots, reģistrācijas numuru, aprakstu un EFT termināļa ID, kas ir specifiski pašam reģistram.

### <a name="pos-profiles"></a>POS profili

Jūs varat atrast pie POS profili **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**POS profili**. Daudzus reģistru aspektus var būt noderīgi pārvaldīt, izmantojot profilus, jo profilus var kopīgi lietot daudzi reģistri. Profilus var kartēt uz atsevišķu reģistru vai — ja profils ir spēkā visā veikalā — uz mazumtirdzniecības veikalu. Nākamajās sadaļās ir aprakstīti POS profili un to lietošana.

#### <a name="offline-profile"></a>Bezsaistes profils

Bezsaistes profils tiek iestatīts veikala līmenī. Tas tiek izmantots, lai norādītu augšupielādes iestatījumus transakcijām, kas tiek veiktas POS reģistrā, kamēr šim reģistram nav savienojuma ar kanālu datu bāzi.

#### <a name="functionality-profile"></a>Funkcionalitātes profils

Funkcionalitātes profils tiek iestatīts veikala līmenī. Tas tiek izmantots, lai norādītu veikalu iestatījumus par funkcijām, kuras var veikt, POS. Šādas iespējas tiek pārvaldītas caur funkcionalitāti profilu. Šīs iespējas ir sakārtotas pēc kopsavilkuma cilnes.

-   Kopsavilkuma cilne **Vispārīgi**.
    -   Starptautiskā Standartizācijas organizācija (ISO).
    -   Izveidot debitoru bezsaistes režīmā.
    -   E-pasta kvīts profils.
    -   Centrālā darbinieku pieteikšanās autentifikācija.
-   Kopsavilkuma cilne **Funkcijas**.
    -   Pieteikšanās un paplašinātās pieteikšanās pārvaldība.
    -   Ar finansēm un valūtu saistīti POS aspekti, piemēram, iespēja ievadīt cenas un definēšana, vai aiz mazām valūtas vienībām ir nepieciešami decimāldaļskaitļi.
    -   Laika reģistrācijas iespējošana, izmantojot POS.
    -   Kā preces un maksājumi tiek rādīti šajā POS un kvītīs.
    -   Darbadienas beigu pārvaldība.
    -   Kanāla datu bāzes transakciju paturēšanas parametri.
    -   Kā no šī POS tiek uzmeklēti un izveidoti debitori.
    -   Kā tiek aprēķinātas atlaides.
-   Kopsavilkuma cilne **Summa**.
    -   Maksimālās un minimālās atļautās cenas.
    -   Atlaižu lietojums un aprēķins.
-   Kopsavilkuma cilne **Informācijas kodi**.
    -   Visos aspektos kā info kodi tiek pārvaldīti POS. Plašāku informāciju sk. [Info kodu](info-codes-retail.md).
-   Kopsavilkuma cilne **Kvīšu numerācija**.
    -   Norādiet kvīšu numerācijas maskas, kas varētu ietvert segmentu veikala numuram, termināļa numuram, konstantēm, kā arī norādiet, vai pārdošana, atgriešana, pārdošanas pasūtījumi un piedāvājumi tiek drukāti atsevišķās sērijās, vai arī tiem visiem tiek izmantota tā pati sērija.

#### <a name="receipt-profiles"></a>Kvīšu profili

Kvīšu profili tiek piešķirti printeriem aparatūras profilā. Tie tiek lietoti, lai norādītu konkrētā printerī drukāto kvīšu tipus. Šie profili ietver iestatījumus kvīšu formātiem un iestatījumus, kas nosaka, vai kvīts tiek drukāta vienmēr, vai arī kasierim tiek lūgts izlemt vai drukāt kvīti. Dažādi printeri var arī lietot dažādus kvīšu profilus. Piemēram, 1. printeris ir standarta termināļa saņemšanas printeris, un tādēļ tam ir mazāki kvīšu formāti. Savukārt 2. printeris ir pilna izmēra kvīšu printeris, kas tiek izmantots, lai drukātu tikai debitoru pasūtījumu kvītis, kurām ir nepieciešams vairāk vietas.

#### <a name="hardware-profiles"></a>Aparatūras profili

Iepriekš šajā rakstā aparatūras profili tiek skaidroti kā komponents klienta iestatīšanai. Aparatūras profili tiek tieši piešķirti POS reģistram vai aparatūras stacijas profilam. Tie tiek izmantoti, lai norādītu ierīču tipus, ko izmanto konkrēts POS reģistrs vai aparatūras stacija. Aparatūras profili tiek arī izmantoti, lai norādītu EFT iestatījumus, kuri tiek izmantoti, lai sazinātos ar maksājumu SDK.

#### <a name="visual-profiles"></a>Vizuālie profili

Vizuālie profili tiek piešķirti reģistra līmenī. Tie tiek izmantoti, lai norādītu konkrēta reģistra dizainu. Profilos ietilpst iestatījumi izmantotās programmas tipam (MPOS vai Cloud POS), izcelšanas krāsai un dizainam, fontu shēmai, pieteikšanās fonam un POS fonam.

### <a name="custom-fields"></a>Pielāgoti lauki

Varat izveidot pielāgotus laukus, lai pievienotu laukus, kas nav sniegts no box POS. Plašāku informāciju par to, kā lietot pielāgotus laukus, apskatīt [darbs ar pielāgotiem laukiem blog post](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Valodas teksts

Varat pārrakstīt POS noklusējuma virknes, izmantojot valodas teksta ierakstus. Lai pārdošanas punktā pārrakstītu kādu virkni, pievienojiet jaunu valodas teksta rindu. Pēc tam norādiet ID, pārrakstāmo noklusējuma virkni un tekstu, kas pārdošanas punktā POS ir jārāda šīs noklusējuma virknes vietā.

### <a name="hardware-station-profiles"></a>Aparatūras stacijas profili

Aparatūras stacijas profili ir paskaidroti agrāk šajā rakstā. Tie tiek izmantoti, lai aparatūras stacijām piešķirtu no instances neatkarīgu informāciju.

### <a name="channel-reports-configuration"></a>Kanālu pārskatu konfigurācija

Atskaites, kas ir pieejamas mazumtirdzniecības kanālā, jūs iestatāt lapā **Mazumtirdzniecības kanālu atskaišu konfigurācija**. Varat izveidot jaunas atskaites, norādot atskaites XML definīciju un piešķirot šo atskaiti konkrētai atļauju grupai šajā POS.

### <a name="devices"></a>Ierīces

Ierīces ir paskaidrotas agrāk šajā rakstā. Tās tiek izmantotas, lai pārvaldītu konkrēta POS reģistra aktivizēšanu. Ierīces tiek arī izmantotas, lai norādītu programmu, kas tiek lietota konkrētam reģistram, un instalācijas pakotni, kas ir jāizmanto, lai instalētu MPOS klientu. Tālāk ir uzskaitīti ierīces aktivizēšanas stāvokļi.

-   **Gaidošs** — ierīce ir gatava aktivizēšanai.
-   **Aktivizēts** — ierīce ir aktivizēta.
-   **Deaktivizēts** — ierīce ir deaktivizēta apstrādes birojā vai ar POS.
-   **Atspējots** — ierīce ir atspējota.

Ar aktivizēšanu saistītā papildinformācija ietver darbinieku, kurš mainīja ierīces aktivizēšanas statusu, aktivizēšanas laikspiedolu un to, vai šīs ierīces konfigurācija tika validēta.

### <a name="client-data-synchronization"></a>Klienta datu sinhronizācija

Visas izmaiņas POS klientā, izņemot izmaiņas ierīces aktivizēšanas statusā, ir nepieciešams sinhronizēt ar kanālu datu bāzi, lai tās stātos spēkā. Sinhronizēt izmaiņas kanālu datu bāzi, dodieties uz **mazumtirdzniecības un komercijas**&gt;**mazumtirdzniecības tā**&gt;**sadalījuma grafiks**, un palaidiet nepieciešamo sadalījuma grafiks. Klienta izmaiņām jums ir jāpalaiž sadales grafiki “Reģistri” un “Kanāla konfigurācija”.


