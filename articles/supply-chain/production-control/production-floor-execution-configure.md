---
title: Ražošanas izpildes interfeisa konfigurēšana
description: Šajā rakstā ir aprakstīts, kā ražošanas izpildes interfeisam izveidot vienu vai vairākas konfigurācijas. Atverot ražotnes izpildes interfeisu, tas automātiski ielādē atlasīto konfigurāciju un darbu filtru, kas ir raksturīgs pārlūkam un ierīcei. Konfigurācijā ir jāiestata politikas, kas jāpiemēro specifiskam lietojumam.
author: johanhoffmann
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7196306b34a72e4c53113dd644f666346f170ed7
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708730"
---
# <a name="configure-the-production-floor-execution-interface"></a>Ražošanas izpildes interfeisa konfigurēšana

[!include [banner](../includes/banner.md)]

Ražotni izmanto darbinieki, lai izmantotu ražotnes izpildes interfeisu savu ikdienas darbu reģistrēšanai, piemēram, lai sāktu darbu, ziņotu atgriezenisko saiti par darbiem, reģistrētu netiešās aktivitātes un ziņotu par prombūtni. Šīs reģistrācijas ir pamats, lai izsekotu norises un ražošanas pasūtījumu izmaksas, un lai aprēķinātu pamatu darbinieku atalgojumam.

Atverot ražotnes izpildes interfeisu, tas automātiski ielādē atlasīto konfigurāciju un darbu filtru, kas ir raksturīgs pārlūkam un ierīcei. Konfigurācijā ir jāiestata politikas, kas jāpiemēro specifiskam lietojumam. Tālāk ir sniegti daži lietošanas piemēri.

- Ierīcē, kas atrodas uzņēmuma zālē, darbinieki reģistrējas, kad tie ierodas birojā, un viņi reģistrējas, kad tie aiziet, beidzot dienu.
- Ierīcē ražotnē mašīnu operatori reģistrējas, kad tie sāk un pabeidz darbus. Viņi reģistrē arī pārtraukumus un netiešās aktivitātes.

Šajā rakstā aprakstītas dažādas opcijas ražošanas stāva izpildes interfeisa konfigurēšanai katrai ierīcei, kas tiek lietota jūsu vietnē.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Ieslēgt ražošanas stāva izpildes interfeisu un ar to saistītās papildu funkcijas

Ražošanas izpildes interfeiss un vairāki šajā rakstā aprakstītie izvēles iestatījumi ir jāieslēdz sistēmai pirms to lietošanas. Izmantojiet lapu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu jebkuru vai visus tālākajās apakšnodaļās norādītos līdzekļus pēc nepieciešamības.

### <a name="the-production-floor-execution-interface"></a>Ražošanas izpildes interfeiss

Šī ir šajā rakstā aprakstītā primārā funkcija un ir priekšnoteikums visām pārējām šajā sadaļā minētajām funkcijām. Attiecībā uz Piegādes ķēdes pārvaldību 10.0.25 tas ir obligāts un to nevar izslēgt. Ja jūs palaižat versiju, kas vecāka par 10.0.25, tad administratori šo funkcionalitāti var ieslēgt vai izslēgt, *meklējot Ražošanas*[stāva izpildes līdzekli līdzekļu pārvaldības darbvietā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="generate-license-plates"></a>Ģenerēt numura zīmes

Šie līdzekļi padara numura zīmes funkcionalitāti pieejamu ražošanas stāva izpildes interfeisam. Ja vēlaties tos izmantot, aktivizējiet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (šādā secībā):

1. *Darbu kartes ierīcei ir pievienota unikālai noliktavas vienībai, lai ziņotu par pabeigšanu*<br>(No Piegādes ķēdes pārvaldības versijas 10.0.21, šī funkcija ir ieslēgta pēc noklusējuma. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.25 šī funkcija ir obligāta.)
1. *Iespējojiet unikāla noliktavas vienības identifikatora automātisku ģenerēšanu, kad darba kartes ierīcē norādīts pabeigts statuss*<br>(No Piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir obligāta.)

### <a name="print-labels"></a>Drukāt etiķetes

Šie līdzekļi padara etiķešu printēšanas funkcionalitāti pieejamu ražošanas stāva izpildes interfeisam. Ja vēlaties tos izmantot, aktivizējiet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (šādā secībā):

1. *Darbu kartes ierīcei ir pievienota unikālai noliktavas vienībai, lai ziņotu par pabeigšanu*<br>(No Piegādes ķēdes pārvaldības versijas 10.0.21, šī funkcija ir ieslēgta pēc noklusējuma. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.25 šī funkcija ir obligāta.)
1. *Izdrukāt etiķeti no darba karšu ierīces*<br>(No Piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir obligāta.)

### <a name="allow-locking-the-touch-screen"></a>Atļaut skārienekrāna bloķēšanu

Šī funkcija ļauj darbiniekiem bloķēt skārienekrānu, lai tie varētu to sankcionēt.

No Piegādes ķēdes pārvaldības versijas 10.0.21 šī funkcija ir ieslēgta pēc noklusējuma. Tāpat kā Piegādes ķēdes pārvaldībai 10.0.25 šī funkcija ir obligāta un to nevar izslēgt. Ja jūs palaižat versiju, kas vecāka par 10.0.25, administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot līdzekli darba kartes ierīces un darba kartes termināļa bloķēšanai, lai *tos*[varētu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) izmantot līdzekļa pārvaldības darbvietā.

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Aktīvu pārvaldības funkcionalitāte ražošanas izpildes interfeisam

Šī funkcija pievieno pamatlīdzekļu pārvaldības cilni ražošanas izpildes interfeisam. Darbinieki var izmantot šo cilni, lai atlasītu līdzekli, kas ir saistīts ar datora resursu, kas ir darbu saraksta atlasītajā filtrā. Atlasītajam iekārtas pamatlīdzeklim darbinieks var skatīt līdzekļa stāvokli un veselības datus no skaitītāja vērtībām līdz pat četriem atlasītajiem skaitītājiem.

No Piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir ieslēgta pēc noklusējuma. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 šī funkcija ir obligāta un to nevar izslēgt. Ja lietojat versiju, kas vecāka par 10.0.29, administratori šo funkcionalitāti var ieslēgt vai izslēgt, *·*[meklējot līdzekļu pārvaldības funkcionalitāti ražošanas izpildes interfeisa līdzekli līdzekļu pārvaldības darbvietā.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="job-search"></a>Darbu meklēšana

Šī funkcija dod iespēju darbu sarakstam pievienot meklēšanas lauku. Darbinieki var atrast noteiktu darbu, ievadot darba ID vai meklējot visus noteikta pasūtījuma darbus, ievadot pasūtījuma ID. Darbinieki var ievadīt ID, izmantojot maksājumu vai skenējot svītrkodu.

No Piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir ieslēgta pēc noklusējuma. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 šī funkcija ir obligāta un to nevar izslēgt. Ja jūs palaižat versiju, kas vecāka par 10.0.29, *·*[tad administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot darbu meklēšanu ražošanas izpildes interfeisa līdzekli līdzekļu pārvaldības darbvietā.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="report-on-co-products-and-by-products"></a>Pārskats par līdzproduktiem un blakusproduktiem

Šis līdzeklis ļauj darbiniekiem izmantot ražošanas izpildes interfeisu, lai ziņotu par partijas pasūtījumu progresu. Šis pārskats iekļauj pārskatus par līdzproduktiem un blakusproduktiem.

Lai izmantotu šo funkciju, tai jābūt ieslēgtai jūsu sistēmai. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir ieslēgta pēc noklusējuma. Administratori var ieslēgt vai *izslēgt*[šo funkcionalitāti, meklējot pārskatu par līdzproduktiem un blakusproduktiem no ražošanas izpildes interfeisa funkcijas līdzekļu pārvaldības darbvietā.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="display-full-serial-batch-and-license-plate-numbers"></a>Rādīt pilnus sērijas, partijas un numura zīmes numurus

Šis līdzeklis nodrošina uzlabotu pieredzi sarakstu apskatīšanai ar sērijas, partijas un numura zīmes numuriem ražošanas izpildes interfeisā. Rādīšanas izmaiņas no karšu skata, kas parāda ierobežotu rakstzīmju skaitu saraksta skatā, kurā ir pietiekami daudz brīvas vietas pilnu vērtību rādīšanai. Šis saraksts arī nodrošina iespēju meklēt noteiktus numurus.

Lai izmantotu šo funkciju, tai jābūt ieslēgtai jūsu sistēmai. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.25, funkcija ir ieslēgta pēc noklusējuma. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir obligāta, un to nevar izslēgt. Ja lietojat versiju, kas vecāka par 10.0.29 versiju, administratori šo funkcionalitāti var ieslēgt vai izslēgt, meklējot pilnus sērijas, *paketes* un numura zīmes numurus [ražošanas izpildes interfeisa līdzeklī Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietā.


No Piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir ieslēgta pēc noklusējuma. Administratori šo funkcionalitāti *var ieslēgt vai izslēgt, meklējot pilnas sērijas,*[paketes un numura zīmes numurus ražošanas izpildes interfeisa līdzeklī Līdzekļu pārvaldības darbvietā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="register-material-consumption"></a>Reģistrēt materiālu patēriņu

Šī funkcija ļauj darbiniekiem izmantot ražošanas izpildes interfeisu, lai reģistrētu materiālu patēriņu, partijas numurus un sērijas numurus. Dažiem ražotājiem, it īpaši tiem, kas attiecas uz procesa nozarēm, ir skaidri jāreģistrē materiāla daudzums, kas tiek patērēts katrai partijai vai ražošanas pasūtījumam. Piemēram, darbinieki var izmantot svaru, lai novērtētu materiālu daudzumu, kas tiek patērēts viņu darba laikā. Lai nodrošinātu pilnīgu materiālu izsekošanu, šīm organizācijām ir jāreģistrē arī partijas numuri, kas tika patērēti katras preces ražošanai.

Šim līdzeklim ir divas versijas. Viens atbalsta krājumus, *kas nav* iespējoti noliktavas pārvaldības procesu (WMS) izmantošanai. Citi atbalsta krājumus, *kas* ir iespējoti WMS lietošanai. Lai lietotu šo funkcionalitāti, [aktivizējot](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vienu vai abus šos līdzekļus Līdzekļu pārvaldībā (šādā secībā), atkarībā no tā, vai ir krājumi, kas iespējoti WMS:

- *Materiālu patēriņa reģistrācija ražotnes izpildes saskarnē (bez WMS)*
- *Reģistrēt materiālu patēriņu ražošanas izpildes interfeisā (WMS iespējots)*

> [!IMPORTANT]
> Varat izmantot tikai līdzekli, kas nav WMS. Tomēr, ja izmantojat WMS, ir jāaktivizē abas funkcijas.

### <a name="report-on-catch-weight-items"></a>Pārskats par pieļaujamā svara krājumiem

Darbinieki var izmantot ražošanas izpildes interfeisu, lai ziņotu par partijas pasūtījumu progresu saistībā ar pieļaujamā svara krājumiem. Partijas pasūtījumi tiek izveidoti no formulām, kuras var definēt, lai pieļaujamā svara krājumi būtu formulas krājumi, līdzprodukti un blakusprodukti. Formulu var arī noteikt, lai būtu formulas rindas sastāvdaļām, kas definētas pieļaujamam svaram. Pieļaujamā svara krājumiem tiek izmantota divas mērvienības, lai sekotu krājumiem: pieļaujamā svara daudzumam un krājumu daudzumam. Piemēram, pārtikas nozarē kastu gaļu var definēt kā pieļaujamā svara krājumu, kur pieļaujamā svara daudzumu izmanto, lai izsekotu lodziņu skaitu un krājumu daudzumu, ko lieto, lai atsekotu lodziņu svaru.

Lai lietotu šo funkcionalitāti, līdzekļa pārvaldībā grieziet [šādu funkciju](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Sniegt pārskatu par pieļaujamā svara krājumiem no ražošanas izpildes interfeisa*

### <a name="the-my-day-dialog"></a>Dialogs "Mana diena"

Dialogs **Mana diena** sniedz darbiniekiem apskatu par viņu ikdienas reģistrācijām un pašreizējām bilancēm par apmaksāto laiku, apmaksātajām virsstundām, kavējumiem un apmaksātajiem kavējumiem.

Lai izmantotu šo funkciju, tai jābūt ieslēgtai jūsu sistēmai. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir ieslēgta pēc noklusējuma. Administratori šo funkcionalitāti var ieslēgt vai izslēgt *, meklējot skatu "Mana diena" ražošanas izpildes interfeisa līdzekli* līdzekļa [pārvaldības darbvietā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="teams"></a>Grupas

Ja vienā ražošanas darbā ir piešķirti vairāki darbinieki, viņi var veidot grupu. Grupa var nominēt vienu darbinieku kā atbildīgo. Tad atlikušie darbinieki automātiski kļūst par šī vadītāja asistentiem. Iegūtajai komandai tikai atbildīgo ir jāreģistrē darba statuss. Laika ieraksti attiecas uz visiem grupas dalībniekiem.

Lai lietotu šo funkcionalitāti, līdzekļa pārvaldībā grieziet [šādu funkciju](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Ražošanas grupas ražošanas izpildes interfeisā*

### <a name="additional-configuration-in-the-production-floor-execution-interface"></a>Papildu konfigurācija ražošanas izpildes interfeisā

Šī funkcija pievieno iestatījumus tālāk minētās funkcionalitātes lapai **Konfigurēt ražošanas izpildes** izpildi:

- Automātiski atvērt dialoglodziņu **Sākt** darbu, kad meklēšana ir pabeigta.
- Automātiski atvērt pārskata **norises** dialoglodziņu, kad meklēšana ir pabeigta.
- Aizpildiet pārējo daudzumu pārskata **norises** dialoglodziņā.
- Aktivizējiet materiālu patēriņa korekcijas **no pārskata progresa** dialoglodziņa. (Šai funkcionalitātei ir nepieciešams arī *Reģistrēt materiālu patēriņu ražošanas izpildes interfeisa funkcijai (nav WMS*).)
- Iespējojiet meklēšanu pēc projekta ID.

Informācija par to, kā izmantot iestatījumus, ir sniegta tālāk šajā rakstā.

Lai lietotu šo funkcionalitāti, līdzekļa pārvaldībā grieziet [šādu funkciju](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Papildu konfigurācija ražošanas izpildes interfeisā*

## <a name="work-with-production-floor-execution-configurations"></a>Darbs ar ražotnes izpildes interfeisa konfigurācijām

Lai izveidotu un uzturētu ražošanas izpildes konfigurācijas, dodieties uz ražošanas **kontroles iestatīšanas \>\> ražošanas izpildi Konfigurējiet \> ražošanas stāva izpildi**. Lapā **Konfigurēt ražotnes izpildi** tiek parādīts esošo konfigurāciju saraksts. Šajā lapā varat veikt tālāk norādītās darbības.

- Atlasīt jebkuru ražotnes konfigurāciju, kas norādīta kreisajā kolonnā, lai to skatītu un rediģētu.
- Darbību rūtī atlasiet **Jauns**, lai sarakstam pievienotu jaunu konfigurāciju. Pēc tam ievadiet nosaukumu laukā **Konfigurācija**, lai identificētu jauno konfigurāciju. Ievadītam nosaukumam ir jābūt unikālam visās konfigurācijās, un vēlāk nevarēsit to rediģēt. Laukā **Apraksts** varat pēc izvēles ievadīt konfigurācijas aprakstu.

Pēc tam konfigurējiet dažādus iestatījumus atlasītajai konfigurācijai, kā aprakstīts šādās apakšsadaļās.

### <a name="the-general-fasttab"></a>Kopsavilkuma cilne Vispārīgi

Kopsavilkuma cilnē Vispārīgi ir pieejami **šādi** iestatījumi:

- **Ierašanās un aiziešanas laiks** - iestatiet *šo* opciju uz Jā, lai izveidotu vienkāršotu interfeisu, kas nodrošina tikai ierašanās un aiziešanas funkcionalitāti. Šis iestatījums atspējo lielāko daļu citu opciju šajā lapā. Pirms šīs opcijas iespējošanas no **Clnes atlases** kopsavilkuma cilnē ir jānoņem visas rindas.
- **Iespējot meklēšanu** – iestatiet šo opciju kā *Jā*, lai iekļautu meklēšanas lauku darbu sarakstā. Darbinieki var atrast noteiktu darbu, ievadot darba ID vai arī var atrast visus noteikta pasūtījuma darbus, ievadot pasūtījuma ID. Darbinieki var ievadīt ID, izmantojot svītrkodu vai skenējot svītrkodu.
- **Iespējojiet meklēšanu pēc projekta ID** – *iestatiet* šo opciju uz Jā, lai iespējotu darbinieku meklēšanu pēc projekta ID (papildus darba ID un pasūtījuma ID) ražošanas izpildes interfeisa meklēšanas laukā. Šo opciju var iestatīt uz Jā tikai *tad*, ja opcija **Aktivizēt meklēšanu** arī ir iestatīta uz *Jā*.
- **Automātiski atvērt sākuma dialogu** – kad šī opcija *ir* iestatīta uz Jā, automātiski tiek atvērts dialoglodziņš Sākt darbu, **kad** darbinieki izmanto meklēšanas joslu, lai atrastu darbu.
- **Automātiski atvērt pārskata norises dialoglodziņu** — *kad* šī opcija ir iestatīta uz Jā, automātiski tiek atvērts pārskata norises dialoglodziņš, **kad** darbinieki izmanto meklēšanas joslu, lai atrastu darbu.
- **Aktivizēt materiālu koriģēšanu** – iestatiet šo opciju *uz Jā*, lai **iespējotu** pogu **Koriģēt materiālu pārskata** norises dialoglodziņā. Darbinieki var izvēlēties šo pogu, lai koriģētu darba materiālu patēriņu.
- **Reģistrēt daudzumu aiziešanas laikā** — iestatiet šo opciju uz *Jā*, lai mudinātu darbiniekus ziņot par notiekošajiem darbiem, kad viņi aiziet. Ja šī opcija ir iestatīta uz *Nē*, darbinieki netiks mudināti.
- **Bloķēt darbinieku** — ja šī opcija ir iestatīta uz *Nē*, darbinieki tiks izrakstīti uzreiz pēc reģistrācijas (piemēram, jauna darba). Interfeiss tad atgriežas pierakstīšanās lapā. Kad šī opcija ir iestatīta uz *Jā*, darbinieki būs reģistrējies ražošanas izpildes interfeisā. Tomēr darbinieks var manuāli izrakstīties tā, ka cits darbinieks var pieteikties, kamēr ražošanas izpildes interfeiss turpina darboties tajā pašā sistēmas lietotāja kontā. Plašāku informāciju par šiem tabulas kontu veidiem skatiet [Piešķirtie lietotāji](config-job-card-device.md#assigned-users).
- **Izmantot faktisko reģistrācijas laiku** — iestatiet šo opciju uz *Jā*, lai iestatītu laiku katrai jaunajai reģistrācijai tā, lai tas atbilstu precīzajam laikam, kad darbinieks iesniedzis reģistrāciju. Ja šī opcija ir iestatīta uz *Nē*, tā vietā tiek izmantots pierakstīšanās laiks. Parasti šī opcija ir jāiestata uz *Jā*, ja esat iestatījis opciju **Bloķēt darbinieku** un/vai **Viens darbinieks** uz *Jā*, kuru gadījumā darbinieki bieži paliek pierakstījušies ilgāku laiku.
- **Viens darbinieks** – iestatiet šo opciju kā Jā *,* ja tikai viens darbinieks izmanto katru ražošanas izpildes interfeisu, kur šī konfigurācija ir aktīva. Kad šī opcija ir iestatīta uz *Jā*, opcija **Bloķēt darbinieku** automātiski tiek iestatīta uz *Jā*. Turklāt šis iestatījums noņem darbiniekam prasību (un iespēju) pierakstīties, izmantojot žetona ID (vai citu līdzīgu ID). Tā vietā darbinieks pierakstās korporācijai Microsoft Dynamics 365 Supply Chain Management *·*, izmantojot sistēmas lietotāja kontu, kas ir saistīts ar reģistrēto darbinieku (*no* darbinieku tabulas) un vienlaicīgi tiek pieteikts ražošanas izpildes interfeisā ar šo darbinieku.
- **Atļaujiet bloķēt** skārienekrānu – *iestatiet* šo opciju uz Jā, lai ļautu darbiniekiem bloķēt ražošanas stāva izpildes interfeisa skārienekrānu, lai viņi varētu to noslēgt. Kad šī opcija ir iestatīta *uz Jā*, **pierakstīšanās lapai tiek** pievienots bloķēšanas ekrāns pogas numuru iestatīšanai. Kad darbinieks atlasa šo pogu, skārienekrāns uz laiku tiek bloķēts, lai novērstu netīšu ievadi. Tiek parādīts arī atpakaļskaitīšanas taimeris. Darbinieks pēc tam var droši tīrīt ierīci un ekrānu. Kad atpakaļskaitīšanas ir beigusies, skārienekrāns tiek automātiski atbloķēts.
- **Ekrāna bloķēšanas ilgums** — kad opcija **Atļaut skārienekrāna bloķēšanu** ir iestatīta uz *Jā*, izmantojiet šo opciju, lai norādītu sekunžu skaitu, cik ilgi skārienekrānam ir jābūt bloķētam tīrīšanai. Ilgumam jābūt diapazonā no 5 līdz 120 sekundēm.
- **Ģenerēt numura zīmi** — iestatiet šo *opciju* kā Jā, lai ģenerētu jaunu numura zīmi katru reizi, kad darbinieks izmanto ražošanas izpildes interfeisu, lai ziņotu par pabeigšanu. Unikāls noliktavas vienības identifikators tiek ģenerēts no numuru sērijas, kas iestatīta lapā **Noliktavas pārvaldības parametri**. Kad šī opcija ir iestatīta uz *Nē*, darbiniekiem ir jānorāda esoša noliktavas vienība, kad tie reģistrē pabeigšanu.
- **Drukāt etiķeti** – iestatiet šo opciju kā *Jā*, lai drukātu numura zīmes uzlīmi, ja darbinieks izmanto ražošanas izpildes interfeisu, lai ziņotu par pabeigšanu. Etiķetes konfigurācija ir iestatīta dokumentu maršrutēšanā, kā aprakstīts Dokumentu maršrutēšanas [etiķešu izkārtojumos](../warehousing/document-routing-layout-for-license-plates.md).

### <a name="the-tab-selection-fasttab"></a>Ciļņu atlases kopsavilkuma cilne

Izmantojiet iestatījumus kopsavilkuma cilnē **Cilnes atlase,** lai atlasītu cilnes, kuras ražošanas izpildes interfeisam ir jāparāda, kad pašreizējā konfigurācija ir aktīva. Varat veidot tik daudz ciļņu, cik nepieciešams, un pēc tam pievienojiet un sakārtojiet tās pēc vajadzības, izmantojot pogas FastTab rīkjoslā. Papildinformāciju par to, kā šeit veidot cilnes un strādāt ar tiem, skatiet [sadaļā Ražošanas izpildes interfeisa dizains](production-floor-execution-tabs.md).

### <a name="the-report-progress-fasttab"></a>Kopsavilkuma cilne Pārskata norise

Kopsavilkuma cilnē Pārskatu norise ir pieejami **šādi** iestatījumi:

- **Aktivizēt materiālu koriģēšanu** – iestatiet šo opciju *kā Jā* **,** lai iekļautu pogu Pielāgot **materiālu pārskata** norises dialoglodziņā. Darbinieki var izvēlēties šo pogu, lai koriģētu darba materiālu patēriņu.
- **Noklusējuma atlikušais** daudzums – iestatiet šo opciju *kā* Jā, lai iepriekš aizpildītu paredzamo atlikušo daudzumu ražošanas uzdevumam **dialoglodziņā Pārskata** norise.

## <a name="clean-up-job-configurations"></a>Tīrīšanas darba konfigurācijas

Kad ražotnes vadītājs iestata ražotnes izpildes interfeisu, tas atlasa konfigurāciju un darbu filtru. Šīs atlases tiek saglabātas atsauču tabulā Supply Chain Management, un pārlūks izmanto ID, kas tiek glabāts lokālajā sīkfailā, lai atrastu pareizo rindu šajā tabulā. Tabula arī reģistrē datumu un laiku, kad darbinieks pēdējoreiz pierakstījies katrā ierīcē.

Pakešuzdevums periodiski notīra ierakstus atsauču tabulā ierīcēm, kurās pēdējās 60 dienās nav reģistrēta neviena darbība. Varat arī manuāli notīrīt ierakstus jebkurā laikā, veicot tālāk norādītās darbības.

1. Dodieties uz **Ražošanas kontrole \> Iestatījumi \> Ražošanas izpilde \> Konfigurēt ražotnes izpildi**.
1. Darbības rūtī atlasiet **Notīrīt klienta konfigurācijas**.
1. Dialoglodziņā **Notīrīt klienta konfigurāciju** iestatiet lauku **Dienu skaits** uz neaktivitātes dienu skaitu (pirms šodienas), kas jāņem vērā. Tiks noņemtas visas konfigurācijas un pierakstīšanās ieraksti ierīcēm, kas šajā laikā nav bijušas aktīvas.
1. Atlasiet **Labi**, lai notīrītu atbilstīgās konfigurācijas, pamatojoties uz iestatījumu **Dienu skaits**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
