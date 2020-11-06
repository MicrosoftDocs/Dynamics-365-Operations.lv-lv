---
title: Ražošanas izpildes interfeisa konfigurēšana
description: Šajā tēmā ir aprakstīts, kā izveidot vienu vai vairākas konfigurācijas ražotnes izpildes interfeisam. Atverot ražotnes izpildes interfeisu, tas automātiski ielādē atlasīto konfigurāciju un darbu filtru, kas ir raksturīgs pārlūkam un ierīcei. Konfigurācijā ir jāiestata politikas, kas jāpiemēro specifiskam lietojumam.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: cf58a7d851577854d08bad70cff69794c3841a2d
ms.sourcegitcommit: 9dd2d38e76d4d93171315ec319e6ce7d51d4e6c7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/15/2020
ms.locfileid: "4012492"
---
# <a name="configure-the-production-floor-execution-interface"></a>Ražošanas izpildes interfeisa konfigurēšana

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Ražotni izmanto darbinieki, lai izmantotu ražotnes izpildes interfeisu savu ikdienas darbu reģistrēšanai, piemēram, lai sāktu darbu, ziņotu atgriezenisko saiti par darbiem, reģistrētu netiešās aktivitātes un ziņotu par prombūtni. Šīs reģistrācijas ir pamats, lai izsekotu norises un ražošanas pasūtījumu izmaksas, un lai aprēķinātu pamatu darbinieku atalgojumam.

Atverot ražotnes izpildes interfeisu, tas automātiski ielādē atlasīto konfigurāciju un darbu filtru, kas ir raksturīgs pārlūkam un ierīcei. Konfigurācijā ir jāiestata politikas, kas jāpiemēro specifiskam lietojumam. Tālāk ir sniegti daži lietošanas piemēri.

- Ierīcē, kas atrodas uzņēmuma zālē, darbinieki reģistrējas, kad tie ierodas birojā, un viņi reģistrējas, kad tie aiziet, beidzot dienu.
- Ierīcē ražotnē mašīnu operatori reģistrējas, kad tie sāk un pabeidz darbus. Viņi reģistrē arī pārtraukumus un netiešās aktivitātes.

Šajā tēmā ir aprakstītas dažādas opcijas darba kartes konfigurēšanai.

## <a name="turn-on-new-features-in-feature-management"></a>Jaunu līdzekļu ieslēgšana līdzekļu pārvaldībā

Daži šajā tēmā aprakstītie iestatījumi ir jāieslēdz jūsu sistēmā, pirms tie jums būs pieejami. Izmantojiet lapu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu jebkuru vai visus tālāk norādītos līdzekļus pēc nepieciešamības.

### <a name="generate-license-plate"></a>Ģenerēt numura zīmi

Lai padarītu šo līdzekli pieejamu, aktivizējiet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (šādā secībā):

1. Darbu kartes ierīcei ir pievienota noliktavas vienībai, lai ziņotu par pabeigšanu
1. Iespējojiet unikāla noliktavas vienības identifikatora automātisku ģenerēšanu, kad darba kartes ierīcē norādīts pabeigts statuss

### <a name="print-label"></a>Drukāt etiķeti

Lai padarītu šo līdzekli pieejamu, aktivizējiet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (šādā secībā):

1. Darbu kartes ierīcei ir pievienota noliktavas vienībai, lai ziņotu par pabeigšanu
1. Izdrukāt etiķeti no darba karšu ierīces

### <a name="allow-locking-the-touch-screen"></a>Atļaut skārienekrāna bloķēšanu

Lai padarītu šo līdzekli pieejamu, ieslēdziet tālāk norādīto līdzekli [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- (Priekšskatījums) Līdzeklis darba kartes ierīces un darba kartes termināļa aizturēšanai, lai var veikt to tīrīšanu

## <a name="work-with-production-floor-execution-configurations"></a>Darbs ar ražotnes izpildes interfeisa konfigurācijām

Lai izveidotu un uzturētu ierīces konfigurācijas, dodieties uz **Ražošanas kontrole \> Iestatīšana \> Ražošanas izpilde \> Konfigurēt ražotnes izpildi**. Lapā **Konfigurēt ražotnes izpildi** tiek parādīts esošo konfigurāciju saraksts. Šajā lapā varat veikt tālāk norādītās darbības.

- Atlasīt jebkuru ražotnes konfigurāciju, kas norādīta kreisajā kolonnā, lai to skatītu un rediģētu.
- Lai sarakstam pievienotu jaunu ierīces konfigurāciju, darbības rūtī atlasiet **Jauns**. Pēc tam ievadiet nosaukumu laukā **Konfigurācija** , lai identificētu jauno konfigurāciju. Ievadītajam nosaukumam ir jābūt unikālam starp visām ierīču konfigurācijām, un vēlāk to nevarēsit rediģēt.

Pēc tam konfigurējiet dažādus atlasītās ierīces konfigurācijas iestatījumus. Pieejami tālāk norādītie lauki.

- **Reģistrēt daudzumu aiziešanas laikā** — iestatiet šo opciju uz *Jā* , lai mudinātu darbiniekus ziņot par notiekošajiem darbiem, kad viņi aiziet. Ja šī opcija ir iestatīta uz *Nē* , darbinieki netiks mudināti.
- **Bloķēt darbinieku** — ja šī opcija ir iestatīta uz *Nē* , darbinieki tiks izrakstīti uzreiz pēc reģistrācijas (piemēram, jauna darba). Pēc tam ierīce atgriezīsies pierakstīšanās lapā. Ja šī opcija ir iestatīta uz *Jā* , visi darbinieki paliks pierakstījušies darba kartes ierīcē. Tomēr darbinieks var manuāli izrakstīties, lai cits darbinieks varētu pierakstīties, kamēr darba kartes ierīce turpina darboties ar to pašu sistēmas lietotāja kontu. Plašāku informāciju par šiem tabulas kontu veidiem skatiet [Piešķirtie lietotāji](config-job-card-device.md#assigned-users).
- **Izmantot faktisko reģistrācijas laiku** — iestatiet šo opciju uz *Jā* , lai iestatītu laiku katrai jaunajai reģistrācijai tā, lai tas atbilstu precīzajam laikam, kad darbinieks iesniedzis reģistrāciju. Ja šī opcija ir iestatīta uz *Nē* , tā vietā tiek izmantots pierakstīšanās laiks. Parasti šī opcija ir jāiestata uz *Jā* , ja esat iestatījis opciju **Bloķēt darbinieku** un/vai **Viens darbinieks** uz *Jā* , kuru gadījumā darbinieki bieži paliek pierakstījušies ilgāku laiku.
- **Viens darbinieks** — iestatiet šo opciju uz *Jā* , ja tikai viens darbinieks izmanto katru darba kartes ierīci, kurā šī konfigurācija ir aktīva. Kad šī opcija ir iestatīta uz *Jā* , opcija **Bloķēt darbinieku** automātiski tiek iestatīta uz *Jā*. Turklāt šis iestatījums noņem darbiniekam prasību (un iespēju) pierakstīties, izmantojot žetona ID (vai citu līdzīgu ID). Tā vietā darbinieks pierakstās Microsoft Dynamics 365 Supply Chain Management, izmantojot sistēmas lietotāja vienlau kontu, kas ir saistīts ar *laikā reģistrēto darbinieku* (no tabulas *darbinieki* ), un vienlaikus tiek pierakstīts darba kartes ierīcē kā šis darbinieks.
- **Atļaut skārienekrāna bloķēšanu** — iestatiet šo opciju uz *Jā* , lai ļautu darbiniekiem bloķēt darbu kartes ierīces skārienekrānu tā, lai varētu to tīrīt. Ja šī opcija ir iestatīta uz *Jā* , ierīces pierakstīšanās lapā tiek pievienota poga **Bloķēt ekrānu tīrīšanai**. Kad darbinieks atlasa šo pogu, skārienekrāns uz laiku tiek bloķēts, lai novērstu netīšu ievadi. Tiek parādīts arī atpakaļskaitīšanas taimeris. Darbinieks pēc tam var droši tīrīt ierīci un ekrānu. Kad atpakaļskaitīšanas ir beigusies, skārienekrāns tiek automātiski atbloķēts.
- **Ekrāna bloķēšanas ilgums** — kad opcija **Atļaut skārienekrāna bloķēšanu** ir iestatīta uz *Jā* , izmantojiet šo opciju, lai norādītu sekunžu skaitu, cik ilgi skārienekrānam ir jābūt bloķētam tīrīšanai. Ilgumam jābūt diapazonā no 5 līdz 120 sekundēm.
- **Ģenerēt noliktavas vienību** — iestatiet šo opciju uz *Jā* , lai ģenerētu jaunu noliktavas vienību katru reizi, kad darbinieks izmanto darbu karšu ierīci pabeigšanas reģistrēšanai. Unikāls noliktavas vienības identifikators tiek ģenerēts no numuru sērijas, kas iestatīta lapā **Noliktavas pārvaldības parametri**. Kad šī opcija ir iestatīta uz *Nē* , darbiniekiem ir jānorāda esoša noliktavas vienība, kad tie reģistrē pabeigšanu.
- **Drukāt etiķeti** — iestatiet šo opciju uz *Jā* , lai izdrukā noliktavas vienības etiķeti, kad darbinieks izmanto darbu karšu ierīci pabeigšanas reģistrācijai. Etiķetes konfigurācija ir iestatīta dokumentu maršrutēšanā, kā tas ir aprakstīts [Dokumentu maršrutēšanas izkārtojumā noliktavas vienību etiķetēm](../warehousing/document-routing-layout-for-license-plates.md).

## <a name="clean-up-job-configurations"></a>Tīrīšanas darba konfigurācijas

Kad ražotnes vadītājs iestata ražotnes izpildes interfeisu, tas atlasa konfigurāciju un darbu filtru. Šīs atlases tiek saglabātas atsauču tabulā Supply Chain Management, un pārlūks izmanto ID, kas tiek glabāts lokālajā sīkfailā, lai atrastu pareizo rindu šajā tabulā. Tabula arī reģistrē datumu un laiku, kad darbinieks pēdējoreiz pierakstījies katrā ierīcē.

Pakešuzdevums periodiski notīra ierakstus atsauču tabulā ierīcēm, kurās pēdējās 60 dienās nav reģistrēta neviena darbība. Varat arī manuāli notīrīt ierakstus jebkurā laikā, veicot tālāk norādītās darbības.

1. Dodieties uz **Ražošanas kontrole \> Iestatījumi \> Ražošanas izpilde \> Konfigurēt ražotnes izpildi**.
1. Darbības rūtī atlasiet **Notīrīt klienta konfigurācijas**.
1. Dialoglodziņā **Notīrīt klienta konfigurāciju** iestatiet lauku **Dienu skaits** uz neaktivitātes dienu skaitu (pirms šodienas), kas jāņem vērā. Tiks noņemtas visas konfigurācijas un pierakstīšanās ieraksti ierīcēm, kas šajā laikā nav bijušas aktīvas.
1. Atlasiet **Labi** , lai notīrītu atbilstīgās konfigurācijas, pamatojoties uz iestatījumu **Dienu skaits**.
