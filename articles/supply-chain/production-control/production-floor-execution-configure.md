---
title: Ražošanas izpildes interfeisa konfigurēšana
description: Šajā tēmā ir aprakstīts, kā izveidot vienu vai vairākas konfigurācijas ražotnes izpildes interfeisam. Atverot ražotnes izpildes interfeisu, tas automātiski ielādē atlasīto konfigurāciju un darbu filtru, kas ir raksturīgs pārlūkam un ierīcei. Konfigurācijā ir jāiestata politikas, kas jāpiemēro specifiskam lietojumam.
author: johanhoffmann
ms.date: 10/05/2020
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
ms.openlocfilehash: 15fcfd72027e081e633fe68209cf85f528ff02d7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576932"
---
# <a name="configure-the-production-floor-execution-interface"></a>Ražošanas izpildes interfeisa konfigurēšana

[!include [banner](../includes/banner.md)]

Ražotni izmanto darbinieki, lai izmantotu ražotnes izpildes interfeisu savu ikdienas darbu reģistrēšanai, piemēram, lai sāktu darbu, ziņotu atgriezenisko saiti par darbiem, reģistrētu netiešās aktivitātes un ziņotu par prombūtni. Šīs reģistrācijas ir pamats, lai izsekotu norises un ražošanas pasūtījumu izmaksas, un lai aprēķinātu pamatu darbinieku atalgojumam.

Atverot ražotnes izpildes interfeisu, tas automātiski ielādē atlasīto konfigurāciju un darbu filtru, kas ir raksturīgs pārlūkam un ierīcei. Konfigurācijā ir jāiestata politikas, kas jāpiemēro specifiskam lietojumam. Tālāk ir sniegti daži lietošanas piemēri.

- Ierīcē, kas atrodas uzņēmuma zālē, darbinieki reģistrējas, kad tie ierodas birojā, un viņi reģistrējas, kad tie aiziet, beidzot dienu.
- Ierīcē ražotnē mašīnu operatori reģistrējas, kad tie sāk un pabeidz darbus. Viņi reģistrē arī pārtraukumus un netiešās aktivitātes.

Šajā tēmā ir aprakstītas dažādas opcijas darba kartes konfigurēšanai.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Ieslēgt ražošanas stāva izpildes interfeisu un ar to saistītās papildu funkcijas

Ražošanas stāva izpildes interfeiss, kā arī vairāki papildu iestatījumi, kas aprakstīti šajā tēmā, ir jāieslēdz sistēmā, lai tos varētu izmantot. Izmantojiet lapu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu jebkuru vai visus tālākajās apakšnodaļās norādītos līdzekļus pēc nepieciešamības.

### <a name="the-production-floor-execution-interface"></a>Ražošanas izpildes interfeiss

Šis ir galvenais šajā tēmā aprakstītais līdzeklis. Tas jūsu sistēmai pievieno ražošanas stāva izpildes interfeisu. Lai to iespējotu, ieslēdziet sekojošo līdzekli [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Ražošanas stāva izpilde

### <a name="generate-license-plates"></a>Ģenerēt numura zīmes

Šie līdzekļi padara numura zīmes funkcionalitāti pieejamu ražošanas stāva izpildes interfeisam. Ja vēlaties tos izmantot, aktivizējiet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (šādā secībā):

1. Darbu kartes ierīcei ir pievienota noliktavas vienībai, lai ziņotu par pabeigšanu
1. Iespējojiet unikāla noliktavas vienības identifikatora automātisku ģenerēšanu, kad darba kartes ierīcē norādīts pabeigts statuss

### <a name="print-labels"></a>Drukāt etiķetes

Šie līdzekļi padara etiķešu printēšanas funkcionalitāti pieejamu ražošanas stāva izpildes interfeisam. Ja vēlaties tos izmantot, aktivizējiet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (šādā secībā):

1. Darbu kartes ierīcei ir pievienota noliktavas vienībai, lai ziņotu par pabeigšanu
1. Izdrukāt etiķeti no darba karšu ierīces

### <a name="allow-locking-the-touch-screen"></a>Atļaut skārienekrāna bloķēšanu

Šis līdzeklis pievieno pogu ražošanas stāva izpildes interfeisam, kas ļauj darbiniekiem notīrīt skārienjūtīgo ekrānu. Ja vēlaties to izmantot, ieslēdziet sekojošo līdzekli [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Līdzeklis darba kartes ierīces un darba kartes termināļa aizturēšanai, lai var veikt to tīrīšanu

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Aktīvu pārvaldības funkcionalitāte ražošanas izpildes interfeisam

Šī funkcija pievieno pamatlīdzekļu pārvaldības cilni ražošanas izpildes interfeisam. Darbinieki var izmantot šo cilni, lai atlasītu līdzekli, kas ir saistīts ar datora resursu, kas ir darbu saraksta atlasītajā filtrā. Atlasītajam iekārtas pamatlīdzeklim darbinieks var skatīt līdzekļa stāvokli un veselības datus no skaitītāja vērtībām līdz pat četriem atlasītajiem skaitītājiem. Ja vēlaties to izmantot, ieslēdziet sekojošo līdzekli [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Aktīvu pārvaldības funkcionalitāte ražošanas izpildes interfeisam

### <a name="enable-job-search"></a>Iespējot darbu meklēšanu

Šī funkcija dod iespēju darbu sarakstam pievienot meklēšanas lauku. Darbinieki var atrast noteiktu darbu, ievadot darba ID vai meklējot visus noteikta pasūtījuma darbus, ievadot pasūtījuma ID. Darbinieki var ievadīt ID, izmantojot maksājumu vai skenējot svītrkodu. Ja vēlaties to izmantot, ieslēdziet sekojošo līdzekli [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Darbu meklēšana ražošanas izpildes saskarnē

## <a name="work-with-production-floor-execution-configurations"></a>Darbs ar ražotnes izpildes interfeisa konfigurācijām

Lai izveidotu un uzturētu ierīces konfigurācijas, dodieties uz **Ražošanas kontrole \> Iestatīšana \> Ražošanas izpilde \> Konfigurēt ražotnes izpildi**. Lapā **Konfigurēt ražotnes izpildi** tiek parādīts esošo konfigurāciju saraksts. Šajā lapā varat veikt tālāk norādītās darbības.

- Atlasīt jebkuru ražotnes konfigurāciju, kas norādīta kreisajā kolonnā, lai to skatītu un rediģētu.
- Lai sarakstam pievienotu jaunu ierīces konfigurāciju, darbības rūtī atlasiet **Jauns**. Pēc tam ievadiet nosaukumu laukā **Konfigurācija**, lai identificētu jauno konfigurāciju. Ievadītajam nosaukumam ir jābūt unikālam starp visām ierīču konfigurācijām, un vēlāk to nevarēsit rediģēt.

Pēc tam konfigurējiet dažādus atlasītās ierīces konfigurācijas iestatījumus. Pieejami tālāk norādītie lauki:

- **Ierašanās un aiziešanas laiks** - iestatiet šo opciju uz *Jā*, lai izveidotu vienkāršotu interfeisu, kas nodrošina tikai ierašanās un aiziešanas funkcionalitāti. Tas atspējo lielāko daļu citu opciju šajā lapā. Pirms šīs opcijas iespējošanas no **Clnes atlases** kopsavilkuma cilnē ir jānoņem visas rindas.
- **Iespējot meklēšanu** - iestatiet šo opciju uz *Jā*, lai iekļautu meklēšanas lauku darbu sarakstā. Darbinieki var atrast noteiktu darbu, ievadot darba ID vai meklējot visus noteikta pasūtījuma darbus, ievadot pasūtījuma ID. Darbinieki var ievadīt ID, izmantojot maksājumu vai skenējot svītrkodu.
- **Reģistrēt daudzumu aiziešanas laikā** — iestatiet šo opciju uz *Jā*, lai mudinātu darbiniekus ziņot par notiekošajiem darbiem, kad viņi aiziet. Ja šī opcija ir iestatīta uz *Nē*, darbinieki netiks mudināti.
- **Bloķēt darbinieku** — ja šī opcija ir iestatīta uz *Nē*, darbinieki tiks izrakstīti uzreiz pēc reģistrācijas (piemēram, jauna darba). Pēc tam ierīce atgriezīsies pierakstīšanās lapā. Ja šī opcija ir iestatīta uz *Jā*, visi darbinieki paliks pierakstījušies darba kartes ierīcē. Tomēr darbinieks var manuāli izrakstīties, lai cits darbinieks varētu pierakstīties, kamēr darba kartes ierīce turpina darboties ar to pašu sistēmas lietotāja kontu. Plašāku informāciju par šiem tabulas kontu veidiem skatiet [Piešķirtie lietotāji](config-job-card-device.md#assigned-users).
- **Izmantot faktisko reģistrācijas laiku** — iestatiet šo opciju uz *Jā*, lai iestatītu laiku katrai jaunajai reģistrācijai tā, lai tas atbilstu precīzajam laikam, kad darbinieks iesniedzis reģistrāciju. Ja šī opcija ir iestatīta uz *Nē*, tā vietā tiek izmantots pierakstīšanās laiks. Parasti šī opcija ir jāiestata uz *Jā*, ja esat iestatījis opciju **Bloķēt darbinieku** un/vai **Viens darbinieks** uz *Jā*, kuru gadījumā darbinieki bieži paliek pierakstījušies ilgāku laiku.
- **Viens darbinieks** — iestatiet šo opciju uz *Jā*, ja tikai viens darbinieks izmanto katru darba kartes ierīci, kurā šī konfigurācija ir aktīva. Kad šī opcija ir iestatīta uz *Jā*, opcija **Bloķēt darbinieku** automātiski tiek iestatīta uz *Jā*. Turklāt šis iestatījums noņem darbiniekam prasību (un iespēju) pierakstīties, izmantojot žetona ID (vai citu līdzīgu ID). Tā vietā darbinieks pierakstās Microsoft Dynamics 365 Supply Chain Management, izmantojot sistēmas lietotāja vienlau kontu, kas ir saistīts ar *laikā reģistrēto darbinieku* (no tabulas *darbinieki*), un vienlaikus tiek pierakstīts darba kartes ierīcē kā šis darbinieks.
- **Atļaut skārienekrāna bloķēšanu** — iestatiet šo opciju uz *Jā*, lai ļautu darbiniekiem bloķēt darbu kartes ierīces skārienekrānu tā, lai varētu to tīrīt. Ja šī opcija ir iestatīta uz *Jā*, ierīces pierakstīšanās lapā tiek pievienota poga **Bloķēt ekrānu tīrīšanai**. Kad darbinieks atlasa šo pogu, skārienekrāns uz laiku tiek bloķēts, lai novērstu netīšu ievadi. Tiek parādīts arī atpakaļskaitīšanas taimeris. Darbinieks pēc tam var droši tīrīt ierīci un ekrānu. Kad atpakaļskaitīšanas ir beigusies, skārienekrāns tiek automātiski atbloķēts.
- **Ekrāna bloķēšanas ilgums** — kad opcija **Atļaut skārienekrāna bloķēšanu** ir iestatīta uz *Jā*, izmantojiet šo opciju, lai norādītu sekunžu skaitu, cik ilgi skārienekrānam ir jābūt bloķētam tīrīšanai. Ilgumam jābūt diapazonā no 5 līdz 120 sekundēm.
- **Ģenerēt noliktavas vienību** — iestatiet šo opciju uz *Jā*, lai ģenerētu jaunu noliktavas vienību katru reizi, kad darbinieks izmanto darbu karšu ierīci pabeigšanas reģistrēšanai. Unikāls noliktavas vienības identifikators tiek ģenerēts no numuru sērijas, kas iestatīta lapā **Noliktavas pārvaldības parametri**. Kad šī opcija ir iestatīta uz *Nē*, darbiniekiem ir jānorāda esoša noliktavas vienība, kad tie reģistrē pabeigšanu.
- **Drukāt etiķeti** — iestatiet šo opciju uz *Jā*, lai izdrukā noliktavas vienības etiķeti, kad darbinieks izmanto darbu karšu ierīci pabeigšanas reģistrācijai. Etiķetes konfigurācija ir iestatīta dokumentu maršrutēšanā, kā tas ir aprakstīts [Dokumentu maršrutēšanas izkārtojumā noliktavas vienību etiķetēm](../warehousing/document-routing-layout-for-license-plates.md).
- **Cilnes atlase** - izmantojiet šīs sadaļas iestatījumus, lai izvēlētos, kuras cilnes attēlot pēc ražošanas stāva interfeisa, kad pašreizējā konfigurācija ir aktīva. Varat izveidot tik daudz ciļņu, cik nepieciešams, un pēc tam pievienot un sakārtot tās pēc nepieciešamības. Lai iegūtu sīkāku informāciju par to, kā veidot cilnes un strādāt ar iestatījumiem, skatiet [Izstrādāt ražošanas stāva izpildes interfeisu](production-floor-execution-tabs.md).

## <a name="clean-up-job-configurations"></a>Tīrīšanas darba konfigurācijas

Kad ražotnes vadītājs iestata ražotnes izpildes interfeisu, tas atlasa konfigurāciju un darbu filtru. Šīs atlases tiek saglabātas atsauču tabulā Supply Chain Management, un pārlūks izmanto ID, kas tiek glabāts lokālajā sīkfailā, lai atrastu pareizo rindu šajā tabulā. Tabula arī reģistrē datumu un laiku, kad darbinieks pēdējoreiz pierakstījies katrā ierīcē.

Pakešuzdevums periodiski notīra ierakstus atsauču tabulā ierīcēm, kurās pēdējās 60 dienās nav reģistrēta neviena darbība. Varat arī manuāli notīrīt ierakstus jebkurā laikā, veicot tālāk norādītās darbības.

1. Dodieties uz **Ražošanas kontrole \> Iestatījumi \> Ražošanas izpilde \> Konfigurēt ražotnes izpildi**.
1. Darbības rūtī atlasiet **Notīrīt klienta konfigurācijas**.
1. Dialoglodziņā **Notīrīt klienta konfigurāciju** iestatiet lauku **Dienu skaits** uz neaktivitātes dienu skaitu (pirms šodienas), kas jāņem vērā. Tiks noņemtas visas konfigurācijas un pierakstīšanās ieraksti ierīcēm, kas šajā laikā nav bijušas aktīvas.
1. Atlasiet **Labi**, lai notīrītu atbilstīgās konfigurācijas, pamatojoties uz iestatījumu **Dienu skaits**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
