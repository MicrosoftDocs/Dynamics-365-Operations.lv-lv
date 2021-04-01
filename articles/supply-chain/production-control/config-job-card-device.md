---
title: Konfigurēt darbu karti ierīcēm
description: Šajā tēmā ir aprakstītas dažādas opcijas darba kartes ierīces konfigurēšanai.
author: johanhoffmann
manager: tfehr
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch, JmgRegistrationTouchUserConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: c139fb7daa0f40b6b7afb0a707f714502d3146d1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246361"
---
# <a name="configure-job-card-for-devices"></a>Konfigurēt darbu karti ierīcēm

[!include [banner](../includes/banner.md)]

Darba kartes ierīci izmanto ražotnes darbinieki, lai reģistrētu savu ikdienas darbu, piemēram, kad darbi sākti, ziņošana par darbu, netiešo aktivitāšu reģistrēšana un prombūtnes norādīšana. Šīs reģistrācijas ir pamats, lai izsekotu norises un izmaksas ražošanas pasūtījumos un lai aprēķinātu pamatu darbinieku atalgojumam. Šajā tēmā ir aprakstītas dažādas opcijas darba kartes konfigurēšanai.

## <a name="enable-new-features-in-feature-management"></a>Jaunu līdzekļu iespējošana līdzekļu pārvaldībā

Daži šajā tēmā aprakstītie iestatījumi ir jāaktivizē jūsu sistēmā, pirms tie jums būs pieejami. Izmantojiet lapu [līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lai iespējotu jebkuru vai visus tālāk norādītos līdzekļus pēc nepieciešamības.

### <a name="generate-license-plate"></a>Ģenerēt numura zīmi

Lai padarītu šo līdzekli pieejamu, iespējojiet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (secībā):

1. Darbu kartes ierīcei ir pievienota noliktavas vienībai, lai ziņotu par pabeigšanu
1. Iespējojiet unikāla noliktavas vienības identifikatora automātisku ģenerēšanu, kad darba kartes ierīcē norādīts pabeigts statuss

### <a name="print-label"></a>Drukāt etiķeti

Lai padarītu šo līdzekli pieejamu, iespējojiet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (secībā):

1. Darbu kartes ierīcei ir pievienota noliktavas vienībai, lai ziņotu par pabeigšanu
1. Izdrukāt etiķeti no darba karšu ierīces

### <a name="allow-locking-of-touch-screen"></a>Atļaut skārienekrāna bloķēšanu

Lai padarītu šo līdzekli pieejamu, iespējojiet tālāk norādīto līdzekli [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- (Priekšskatījums) Līdzeklis darba kartes ierīces un darba kartes termināļa aizturēšanai, lai var veikt to tīrīšanu

## <a name="manage-your-device-configurations"></a>Jūsu ierīces konfigurāciju pārvaldība

Lai iestatītu ierīces konfigurācijas, pārejiet uz sadaļu **Ražošanas kontrole > Iestatīšana > Ražošanas izpilde > Konfigurēt ierīču darba karti**. Tiek atvērta lapa **Konfigurēt darbu karti ierīcēm**, kurā parādīts esošo konfigurāciju saraksts. No šejienes varat veikt tālāk norādītās darbības: 

- Atlasiet jebkuru ierīces konfigurāciju, kas norādīta kreisajā kolonnā, lai to skatītu un rediģētu.
- Lai sarakstam pievienotu jaunu ierīces konfigurāciju, darbības rūtī atlasiet **Jauns**. Pēc tam ievadiet nosaukumu laukā **Konfigurācija**, lai identificētu jauno konfigurāciju. Šeit ievadītajai vērtībai ir jābūt unikālai starp visām ierīču konfigurācijām, un vēlāk to nevarēsit rediģēt.

Lai iegūtu sīkāku informāciju par katru darbu kartes ierīču konfigurēšanas iestatījumu, skatiet turpmākās sadaļas.

## <a name="general-settings"></a>Vispārīgie iestatījumi

Kopsavilkuma cilne **Vispārīgi** ļauj konfigurēt katru no dažādām opcijām, kas pieejamas atlasītajai ierīces konfigurācijai. Pieejami tālāk norādītie iestatījumi:

- **Reģistrēt daudzumu aiziešanas laikā** — iestatiet to uz **Jā**, lai mudinātu darbiniekus ziņot par notiekošajiem darbiem, kad notiek aiziešana. Ja iestatījums ir **Nē**, darbinieki netiks mudināti.
- **Bloķēt darbinieku** — kad šī opcija ir iestatīta uz **Nē**, katrs darbinieks saņems atteikumu uzreiz pēc reģistrācijas (piemēram, jauna darba), un pēc tam ierīce atgriezīsies pierakstīšanās lapā. Ja šī opcija ir iestatīta uz **Jā**, katrs darbinieks paliks pierakstījies darba kartes ierīcē. Tomēr darbinieks joprojām varēs pieteikties manuāli, lai ļautu pieteikties citam darbiniekam, kamēr darba kartes ierīce joprojām darbojas vienā sistēmas lietotāja kontā. Plašāku informāciju par šiem tabulas kontu veidiem skatiet [Piešķirtie lietotāji](#assigned-users).
- **Svītrkodu skeneris** — iestatiet to uz **Jā**, lai nodrošinātu opciju darba kartes ierīcei, kas ļauj darbiniekiem reģistrēt jauna darba sākumu, skenējot svītrkodu.
- **Izmantot faktisko reģistrācijas laiku** — iestatiet to uz **Jā**, lai iestatītu laiku katrai jaunajai reģistrācijai tā, lai tas atbilstu precīzajam laikam, kad darbinieks iesniedzis reģistrāciju. Iestatiet uz **Nē**, lai tā vietā izmantotu pieteikšanās laiku. Parasti tas ir jāiestata uz **Jā**, ja esat iespējojis opcijas **Bloķēt darbinieku** un/vai **Viens darbinieks**, kuru gadījumā darbinieki bieži paliek pieteikušies ilgāku laiku.
- **Viens darbinieks** — iestatiet šo opciju uz **Jā**, ja tikai viens darbinieks izmanto katru darba kartes ierīci, kurā šī konfigurācija ir aktīva. Kad ir atlasīta šī opcija, opcija **Bloķēt darbinieku** automātiski tiek iestatīta uz **Jā**. Turklāt šī opcija noņem darbiniekam prasību (un iespēju) pieteikties, izmantojot žetona ID (vai līdzīgu). Tā vietā darbinieks pierakstās Supply Chain Management, izmantojot sistēmas lietotāja vienlau kontu, kas ir saistīts ar *laikā reģistrēto darbinieku* (no tabulas *darbinieki* ), un vienlaikus tiek pieteikts darba kartes ierīcē kā šis darbinieks.  Plašāku informāciju par šiem tabulas kontu veidiem skatiet [Piešķirtie lietotāji](#assigned-users).
- **Atļaut darbiniekiem iestatīt personīgos filtrus** — iestatiet šo opciju uz **Jā**, lai ļautu darbiniekiem filtrēt darbus, kas tiem ir redzami ierīcē. Darbinieks var modificēt vērtības jebkuram no trim filtra kritērijiem: **Ražošanas vienība**, **Resursu grupa** un **Resurss**. Ierīcē tiks parādīti tikai tie darbi, kas ir ieplānoti resursiem, kuri atbilst atlasītajiem filtra kritērijiem. Varat arī piešķirt noklusējuma vērtības vienam vai visiem šiem kritērijiem, un tie tiks piemēroti pat tad, ja šī opcija nav atlasīta.
- **Atļaut skārienekrāna bloķēšanu** — iestatiet šo opciju uz **Jā**, lai ļautu darbiniekiem bloķēt darbu kartes ierīces skārienekrānu, lai varētu to tīrīt. Iespējojot šo opciju, ierīces pierakstīšanās lapā tiek pievienota cpoga **Bloķēt ekrānu tīrīšanai**. Kad darbinieks atlasa šo pogu, skārienekrāns uz laiku tiek bloķēts, lai novērstu netīšu ievadi, un ir redzams atpakaļskaitīšanas taimeris. Darbinieks tagad var droši tīrīt ierīci un ekrānu. Kad atpakaļskaitīšanas ir beigusies, skārienekrāns tiek automātiski atbloķēts.
- **Ekrāna bloķēšanas ilgums** — kad opcija **Atļaut skārienekrāna bloķēšanu** ir iespējota, izmantojiet šo opciju, lai norādītu sekunžu skaitu, cik ilgi skārienekrānam ir jābūt bloķētam tīrīšanai. Ilgumam jābūt diapazonā no 5 līdz 120 sekundēm.
- **Ražošanas vienība** — atlasiet ražošanas vienību, kas jālieto kā noklusējuma filtra kritērijs darbu sarakstam, kas redzams katram darbiniekam. Ierīce sākotnēji rādīs tikai darbus, kas ir ieplānoti resursiem, kuri grupēti atlasītajā ražošanas vienībā. Ja ir iespējota opcija **Ļaut darbiniekiem iestatīt personīgos filtrus**, darbinieki varēs rediģēt šo vērtību, citādi šis filtrs vienmēr tiks lietots, kad attiecīgā ierīces konfigurācija būs aktīva.
- **Resursu grupa** — atlasiet resursu grupu, kas jālieto kā noklusējuma filtra kritērijs darbu sarakstam, kas redzams katram darbiniekam. Ierīce sākotnēji rādīs tikai darbus, kas ir ieplānoti resursiem, kuri grupēti atlasītajā resursu grupā. Ja ir iespējota opcija **Ļaut darbiniekiem iestatīt personīgos filtrus**, darbinieki varēs rediģēt šo vērtību, citādi šis filtrs vienmēr tiks lietots, kad attiecīgā ierīces konfigurācija būs aktīva.
- **Resurss** — atlasiet resursu, kas jālieto kā noklusējuma filtra kritērijs darbu sarakstam, kas redzams katram darbiniekam. Ierīce sākotnēji rādīs tikai darbus, kas ir ieplānoti atlasītajam resursam. Ja ir iespējota opcija **Ļaut darbiniekiem iestatīt personīgos filtrus**, darbinieki varēs rediģēt šo vērtību, citādi šis filtrs vienmēr tiks lietots, kad attiecīgā ierīces konfigurācija būs aktīva.
- **Ģenerēt noliktavas vienību** — iestatiet šo opciju uz **Jā**, lai ģenerētu jaunu noliktavas vienību katru reizi, kad darbinieks izmanto darbu karšu ierīci pabeigšanas reģistrēšanai. Unikāls noliktavas vienības identifikators tiek ģenerēts no numuru sērijas, kas iestatīta lapā **Noliktavas pārvaldības parametri**. Kad iestatījums ir **Nē**, darbiniekiem ir jānorāda esoša noliktavas vienība, reģistrējot pabeigšanu.
- **Drukāt etiķeti** — iestatiet šo opciju uz **Jā**, lai izdrukā noliktavas vienības etiķeti, kad darbinieks izmanto darbu karšu ierīci pabeigšanas reģistrācijai. Etiķetes konfigurācija ir iestatīta dokumentu maršrutēšanā, kā tas ir aprakstīts [Dokumentu maršrutēšanas izkārtojumā noliktavas vienību etiķetēm](../warehousing/document-routing-layout-for-license-plates.md).

<a name="assigned-users"></a>

## <a name="assigned-users"></a>Piešķirtie lietotāji

Izmantojiet opsavilkuma cilni **Piešķirtie lietotāji**, lai saistītu vienu vai vairākus sistēmas lietotājus ar pašreizējo ierīces konfigurāciju. Katrs sistēmas lietotājs var tikt piešķirts tikai vienai darba ierīces konfigurācijai.

Iestatot ierīci, IT darbinieks parasti pierakstās Supply Chain Management, izmantojot sistēmas lietotāja kontu. Pēc tam darba ierīces konfigurācija, kas saistīta ar šo sistēmas lietotāju, ir spēkā tik ilgi, kamēr sistēmas lietotājs paliek pierakstījies sistēmā. Šie sistēmas lietotāju konti parasti ir ierobežoti, lai atļautu piekļuvi tikai darba kartes ierīces lapai, bet ne vienai citai Supply Chain Management daļai.

Kad sistēmas lietotājs ir pierakstījies un darba ierīces konfigurācija ir ielādēta, darbinieki var pierakstīties darbu karšu ierīcē, izmantojot savu *laikā reģistrētā darbinieka* kontu (piemēram, skenējot svītrkodu uz sava žetona), tādējādi viņi var sākt jaunus darbus un veikt cita veida reģistrāciju. Dažādi darbinieki var pierakstīties un izrakstīties dienas laikā, kamēr tā pati ierīces konfigurācija paliek spēkā šajā datorā, jo sistēmas lietotājs joprojām ir pierakstījies Supply Chain Management uz visu dienu.

Tomēr, kā iepriekš minēts, kad izmantojat ierīces konfigurāciju ar opciju **Viens darbinieks**, paši darbinieki parasti pierakstās Supply Chain Management, izmantojot sistēmas lietotāju, kas ir saistīts ar viņu pašu *laikā reģistrētā darbinieka* kontu, tāpēc viņi ielādē ierīces konfigurāciju un vienlaikus pierakstās kā darbiniek darbu karšu ierīcē.

## <a name="additional-resources"></a>Papildu resursi

[Reģistrējiet pabeigšanu, izmantojot darba kartes ierīci](report-finished-job-device.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]