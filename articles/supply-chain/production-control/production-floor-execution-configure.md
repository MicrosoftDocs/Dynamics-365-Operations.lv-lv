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
ms.openlocfilehash: 5a0ead85eaeb6b96b80716614990af8c8e5e70f7
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384751"
---
# <a name="configure-the-production-floor-execution-interface"></a>Ražošanas izpildes interfeisa konfigurēšana

[!include [banner](../includes/banner.md)]

Ražotni izmanto darbinieki, lai izmantotu ražotnes izpildes interfeisu savu ikdienas darbu reģistrēšanai, piemēram, lai sāktu darbu, ziņotu atgriezenisko saiti par darbiem, reģistrētu netiešās aktivitātes un ziņotu par prombūtni. Šīs reģistrācijas ir pamats, lai izsekotu norises un ražošanas pasūtījumu izmaksas, un lai aprēķinātu pamatu darbinieku atalgojumam.

Atverot ražotnes izpildes interfeisu, tas automātiski ielādē atlasīto konfigurāciju un darbu filtru, kas ir raksturīgs pārlūkam un ierīcei. Konfigurācijā ir jāiestata politikas, kas jāpiemēro specifiskam lietojumam. Tālāk ir sniegti daži lietošanas piemēri.

- Ierīcē, kas atrodas uzņēmuma zālē, darbinieki reģistrējas, kad tie ierodas birojā, un viņi reģistrējas, kad tie aiziet, beidzot dienu.
- Ierīcē ražotnē mašīnu operatori reģistrējas, kad tie sāk un pabeidz darbus. Viņi reģistrē arī pārtraukumus un netiešās aktivitātes.

Šajā tēmā ir aprakstītas dažādas ražošanas grīdas izpildes interfeisa konfigurēšanas iespējas katrai ierīcei, kas tiek izmantota jūsu vietnē.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Ieslēgt ražošanas stāva izpildes interfeisu un ar to saistītās papildu funkcijas

Ražošanas stāva izpildes interfeiss, kā arī vairāki papildu iestatījumi, kas aprakstīti šajā tēmā, ir jāieslēdz sistēmā, lai tos varētu izmantot. Izmantojiet lapu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu jebkuru vai visus tālākajās apakšnodaļās norādītos līdzekļus pēc nepieciešamības.

### <a name="the-production-floor-execution-interface"></a>Ražošanas izpildes interfeiss

Šī ir galvenā funkcija, kas aprakstīta šajā tēmā, un tā ir priekšnoteikums visām pārējām šajā sadaļā minētajām funkcijām. No piegādes ķēdes pārvaldības 10.0.25. tas ir obligāts un to nevar izslēgt. Ja izmantojat versiju, kas vecāka par 10.0.25, administratori var ieslēgt vai izslēgt šo funkcionalitāti, līdzekļu pārvaldības *darbvietā* meklējot [ražošanas grīdas izpildes](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) līdzekli.

### <a name="generate-license-plates"></a>Ģenerēt numura zīmes

Šie līdzekļi padara numura zīmes funkcionalitāti pieejamu ražošanas stāva izpildes interfeisam. Ja vēlaties tos izmantot, aktivizējiet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (šādā secībā):

1. *Darbu kartes ierīcei ir pievienota unikālai noliktavas vienībai, lai ziņotu par pabeigšanu*<br>(No piegādes ķēdes pārvaldības versijas 10.0.21 šis līdzeklis pēc noklusējuma ir ieslēgts. No piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir obligāta.)
1. *Iespējojiet unikāla noliktavas vienības identifikatora automātisku ģenerēšanu, kad darba kartes ierīcē norādīts pabeigts statuss*<br>(No piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir obligāta.)

### <a name="print-labels"></a>Drukāt etiķetes

Šie līdzekļi padara etiķešu printēšanas funkcionalitāti pieejamu ražošanas stāva izpildes interfeisam. Ja vēlaties tos izmantot, aktivizējiet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (šādā secībā):

1. *Darbu kartes ierīcei ir pievienota unikālai noliktavas vienībai, lai ziņotu par pabeigšanu*<br>(No piegādes ķēdes pārvaldības versijas 10.0.21 šis līdzeklis pēc noklusējuma ir ieslēgts. No piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir obligāta.)
1. *Izdrukāt etiķeti no darba karšu ierīces*<br>(No piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir obligāta.)

### <a name="allow-locking-the-touch-screen"></a>Atļaut skārienekrāna bloķēšanu

Šī funkcija ļauj darbiniekiem bloķēt skārienekrānu, lai viņi to varētu sanitizēt.

Piegādes ķēdes pārvaldības versijā 10.0.21 šis līdzeklis pēc noklusējuma ir ieslēgts. No piegādes ķēdes pārvaldības 10.0.25 šī funkcija ir obligāta, un to nevar izslēgt. Ja izmantojat versiju, kas vecāka par 10.0.25, administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot *līdzekli darba kartes ierīces un darba kartes termināļa bloķēšanai, lai līdzekļu pārvaldības* darbvietā [tos varētu dezinficēt](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Aktīvu pārvaldības funkcionalitāte ražošanas izpildes interfeisam

Šī funkcija pievieno pamatlīdzekļu pārvaldības cilni ražošanas izpildes interfeisam. Darbinieki var izmantot šo cilni, lai atlasītu līdzekli, kas ir saistīts ar datora resursu, kas ir darbu saraksta atlasītajā filtrā. Atlasītajam iekārtas pamatlīdzeklim darbinieks var skatīt līdzekļa stāvokli un veselības datus no skaitītāja vērtībām līdz pat četriem atlasītajiem skaitītājiem. Ja vēlaties to izmantot, ieslēdziet sekojošo līdzekli [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Aktīvu pārvaldības funkcionalitāte ražošanas izpildes interfeisam*<br>(No piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir ieslēgta pēc noklusējuma.)

### <a name="enable-job-search"></a>Iespējot darbu meklēšanu

Šī funkcija dod iespēju darbu sarakstam pievienot meklēšanas lauku. Darbinieki var atrast noteiktu darbu, ievadot darba ID vai meklējot visus noteikta pasūtījuma darbus, ievadot pasūtījuma ID. Darbinieki var ievadīt ID, izmantojot maksājumu vai skenējot svītrkodu. Ja vēlaties to izmantot, ieslēdziet sekojošo līdzekli [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Darbu meklēšana ražošanas izpildes saskarnē*<br>(No piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir ieslēgta pēc noklusējuma.)

### <a name="enable-reporting-on-co-products-and-by-products"></a>Iespējot pārskatus par līdzproduktiem un blakusproduktiem

Šis līdzeklis ļauj darbiniekiem izmantot ražošanas izpildes interfeisu, lai ziņotu par partijas pasūtījumu progresu. Šis pārskats iekļauj pārskatus par līdzproduktiem un blakusproduktiem. Lai izmantotu šo funkcionalitāti, līdzekļu pārvaldībā [ieslēdziet šādu līdzekli](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Pārskats par līdzproduktiem un blakusproduktiem no ražošanas izpildes saskarnes*

### <a name="enable-the-display-of-full-serial-batch-and-license-plate-numbers"></a>Iespējot pilnu sērijas, partijas un numura zīmes numuru parādīšanu

Šis līdzeklis nodrošina uzlabotu pieredzi sarakstu apskatīšanai ar sērijas, partijas un numura zīmes numuriem ražošanas izpildes interfeisā. Displejs mainās no kartes skata, kurā redzams ierobežots rakstzīmju skaits, uz saraksta skatu, kas nodrošina pietiekami daudz vietas, lai parādītu pilnas vērtības. Šis saraksts arī nodrošina iespēju meklēt noteiktus numurus.

Piegādes ķēdes pārvaldības versijā 10.0.25 šis līdzeklis pēc noklusējuma ir ieslēgts. Administratori var ieslēgt vai izslēgt šo funkcionalitāti, līdzekļu *pārvaldības* darbvietā ražošanas grīdas izpildes interfeisa [līdzekļa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) Rādīt pilnus sērijas, partijas un numura zīmes numurus.

### <a name="enable-registering-of-material-consumption"></a>Iespējot materiālu patēriņa reģistrēšanu

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Šis līdzeklis ļauj darbiniekiem izmantot ražošanas grīdas izpildes interfeisu, lai reģistrētu materiālu patēriņu, partijas numurus un sērijas numurus. Dažiem ražotājiem, jo īpaši tiem, kas darbojas pārstrādes nozarēs, ir skaidri jāreģistrē materiāla daudzums, kas tiek patērēts katrai partijai vai ražošanas pasūtījumam. Piemēram, darbinieki var izmantot skalu, lai nosvērtu materiāla daudzumu, kas tiek patērēts darba laikā. Lai nodrošinātu pilnīgu materiālu izsekojamību, šīm organizācijām jāreģistrē arī partijas numuri, kas tika patērēti, lai ražotu katru produktu.

Šim līdzeklim ir divas versijas. Viens atbalsta krājumus, kuriem *nav* iespējots izmantot papildu noliktavas procesus (WMS). Pārējie atbalsta vienumus, kas *ir iespējoti* WMS izmantošanai. Lai izmantotu šo funkcionalitāti, līdzekļu pārvaldībā [(šādā secībā) ieslēdziet vienu vai abus no šiem līdzekļiem](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) atkarībā no tā, vai jums ir vienumi, kas ir iespējoti WMS:

- *(Priekšskatījums) Materiālu patēriņa reģistrācija ražotnes izpildes saskarnē (bez WMS)*
- *(Priekšskatījums) Reģistrēt materiālu patēriņu ražošanas izpildes interfeisā (WMS iespējots)*

> [!IMPORTANT]
> Jūs varat izmantot tikai funkciju, kas nav WMS. Tomēr, ja izmantojat WMS, ir jāiespējo abi līdzekļi.

### <a name="enable-reporting-on-catch-weight-items"></a>Iespējot pārskatu sniegšanu pieļaujamā svara krājumiem

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Darbinieki var izmantot ražošanas grīdas izpildes interfeisu, lai ziņotu par pieļaujamā svara krājumu partijas pasūtījumu norisi. Partijas pasūtījumi tiek izveidoti no formulām, kuras var definēt, lai pieļaujamā svara krājumi būtu formulas krājumi, līdzprodukti un blakusprodukti. Formulu var arī noteikt, lai būtu formulas rindas sastāvdaļām, kas definētas pieļaujamam svaram. Pieļaujamā svara krājumiem tiek izmantota divas mērvienības, lai sekotu krājumiem: pieļaujamā svara daudzumam un krājumu daudzumam. Piemēram, pārtikas nozarē kastu gaļu var definēt kā pieļaujamā svara krājumu, kur pieļaujamā svara daudzumu izmanto, lai izsekotu lodziņu skaitu un krājumu daudzumu, ko lieto, lai atsekotu lodziņu svaru.

Lai izmantotu šo funkcionalitāti, līdzekļu pārvaldībā [ieslēdziet šādu līdzekli](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *(Priekšskatījums) Pieļaujamā svara krājumu pārskats no ražošanas izpildes interfeisa*

## <a name="work-with-production-floor-execution-configurations"></a>Darbs ar ražotnes izpildes interfeisa konfigurācijām

Lai izveidotu un uzturētu ražošanas grīdas izpildes konfigurācijas, dodieties uz **Ražošanas kontroles \> uzstādījumi \> Ražošanas izpilde Ražošanas grīdas izpildes \>** konfigurēšana. Lapā **Konfigurēt ražotnes izpildi** tiek parādīts esošo konfigurāciju saraksts. Šajā lapā varat veikt tālāk norādītās darbības.

- Atlasīt jebkuru ražotnes konfigurāciju, kas norādīta kreisajā kolonnā, lai to skatītu un rediģētu.
- Darbību rūtī atlasiet **Jauns**, lai sarakstam pievienotu jaunu konfigurāciju. Pēc tam ievadiet nosaukumu laukā **Konfigurācija**, lai identificētu jauno konfigurāciju. Ievadītajam nosaukumam jābūt unikālam starp visām konfigurācijām, un vēlāk to nevarēsit rediģēt.

Pēc tam konfigurējiet dažādus atlasītās konfigurācijas iestatījumus. Pieejami tālāk norādītie lauki:

- **Ierašanās un aiziešanas laiks** - iestatiet šo opciju uz *Jā*, lai izveidotu vienkāršotu interfeisu, kas nodrošina tikai ierašanās un aiziešanas funkcionalitāti. Tas atspējo lielāko daļu citu opciju šajā lapā. Pirms šīs opcijas iespējošanas no **Clnes atlases** kopsavilkuma cilnē ir jānoņem visas rindas.
- **Iespējot meklēšanu** - iestatiet šo opciju uz *Jā*, lai iekļautu meklēšanas lauku darbu sarakstā. Darbinieki var atrast noteiktu darbu, ievadot darba ID vai meklējot visus noteikta pasūtījuma darbus, ievadot pasūtījuma ID. Darbinieki var ievadīt ID, izmantojot maksājumu vai skenējot svītrkodu.
- **Reģistrēt daudzumu aiziešanas laikā** — iestatiet šo opciju uz *Jā*, lai mudinātu darbiniekus ziņot par notiekošajiem darbiem, kad viņi aiziet. Ja šī opcija ir iestatīta uz *Nē*, darbinieki netiks mudināti.
- **Bloķēt darbinieku** — ja šī opcija ir iestatīta uz *Nē*, darbinieki tiks izrakstīti uzreiz pēc reģistrācijas (piemēram, jauna darba). Pēc tam interfeiss atgriezīsies pierakstīšanās lapā. Ja šī opcija ir iestatīta uz *Jā*, darbinieki paliks pieteikušies ražošanas grīdas izpildes interfeisā. Tomēr darbinieks var manuāli izrakstīties, lai cits darbinieks varētu pieteikties, kamēr ražošanas grīdas izpildes interfeiss turpina darboties tajā pašā sistēmas lietotāja kontā. Plašāku informāciju par šiem tabulas kontu veidiem skatiet [Piešķirtie lietotāji](config-job-card-device.md#assigned-users).
- **Izmantot faktisko reģistrācijas laiku** — iestatiet šo opciju uz *Jā*, lai iestatītu laiku katrai jaunajai reģistrācijai tā, lai tas atbilstu precīzajam laikam, kad darbinieks iesniedzis reģistrāciju. Ja šī opcija ir iestatīta uz *Nē*, tā vietā tiek izmantots pierakstīšanās laiks. Parasti šī opcija ir jāiestata uz *Jā*, ja esat iestatījis opciju **Bloķēt darbinieku** un/vai **Viens darbinieks** uz *Jā*, kuru gadījumā darbinieki bieži paliek pierakstījušies ilgāku laiku.
- **Viens darbinieks** — iestatiet šo opciju uz Jā *,* ja tikai viens darbinieks izmanto katru ražošanas grīdas izpildes interfeisu, kurā šī konfigurācija ir aktīva. Kad šī opcija ir iestatīta uz *Jā*, opcija **Bloķēt darbinieku** automātiski tiek iestatīta uz *Jā*. Turklāt šis iestatījums noņem darbiniekam prasību (un iespēju) pierakstīties, izmantojot žetona ID (vai citu līdzīgu ID). Tā vietā darbinieks pierakstās programmā Microsoft Dynamics 365 Supply Chain Management, izmantojot sistēmas lietotāja kontu, kas ir saistīts *ar laikā reģistrētu darbinieku* (no *darbinieku* tabulas), un vienlaikus piesakās ražošanas grīdas izpildes interfeisā kā šis darbinieks.
- **Atļaut skārienekrāna** bloķēšanu — iestatiet šo opciju uz *Jā*, lai darbinieki varētu bloķēt ražošanas grīdas izpildes interfeisa skārienekrānu, lai viņi to varētu dezinficēt. Ja šī opcija ir iestatīta uz *Jā*, **pierakstīšanās lapai tiek pievienots bloķēšanas ekrāns, lai veiktu dezinficēšanu**. Kad darbinieks atlasa šo pogu, skārienekrāns uz laiku tiek bloķēts, lai novērstu netīšu ievadi. Tiek parādīts arī atpakaļskaitīšanas taimeris. Darbinieks pēc tam var droši tīrīt ierīci un ekrānu. Kad atpakaļskaitīšanas ir beigusies, skārienekrāns tiek automātiski atbloķēts.
- **Ekrāna bloķēšanas ilgums** — kad opcija **Atļaut skārienekrāna bloķēšanu** ir iestatīta uz *Jā*, izmantojiet šo opciju, lai norādītu sekunžu skaitu, cik ilgi skārienekrānam ir jābūt bloķētam tīrīšanai. Ilgumam jābūt diapazonā no 5 līdz 120 sekundēm.
- **Ģenerēt numura zīmi** — iestatiet šo opciju uz *Jā*, lai ģenerētu jaunu numura zīmi katru reizi, kad darbinieks izmanto ražošanas grīdas izpildes interfeisu, lai ziņotu par pabeigtu. Unikāls noliktavas vienības identifikators tiek ģenerēts no numuru sērijas, kas iestatīta lapā **Noliktavas pārvaldības parametri**. Kad šī opcija ir iestatīta uz *Nē*, darbiniekiem ir jānorāda esoša noliktavas vienība, kad tie reģistrē pabeigšanu.
- **Drukāt etiķeti** — iestatiet šo opciju uz Jā *,* lai drukātu numura zīmes etiķeti, kad darbinieks izmanto ražošanas grīdas izpildes interfeisu, lai ziņotu par pabeigtu. Etiķetes konfigurācija ir iestatīta dokumentu maršrutēšanā, kā tas ir aprakstīts [Dokumentu maršrutēšanas izkārtojumā noliktavas vienību etiķetēm](../warehousing/document-routing-layout-for-license-plates.md).
- **Cilnes atlase**  - izmantojiet šīs sadaļas iestatījumus, lai izvēlētos, kuras cilnes attēlot pēc ražošanas stāva interfeisa, kad pašreizējā konfigurācija ir aktīva. Varat izveidot tik daudz ciļņu, cik nepieciešams, un pēc tam pievienot un sakārtot tās pēc nepieciešamības. Lai iegūtu sīkāku informāciju par to, kā veidot cilnes un strādāt ar iestatījumiem, skatiet [Izstrādāt ražošanas stāva izpildes interfeisu](production-floor-execution-tabs.md).

## <a name="clean-up-job-configurations"></a>Tīrīšanas darba konfigurācijas

Kad ražotnes vadītājs iestata ražotnes izpildes interfeisu, tas atlasa konfigurāciju un darbu filtru. Šīs atlases tiek saglabātas atsauču tabulā Supply Chain Management, un pārlūks izmanto ID, kas tiek glabāts lokālajā sīkfailā, lai atrastu pareizo rindu šajā tabulā. Tabula arī reģistrē datumu un laiku, kad darbinieks pēdējoreiz pierakstījies katrā ierīcē.

Pakešuzdevums periodiski notīra ierakstus atsauču tabulā ierīcēm, kurās pēdējās 60 dienās nav reģistrēta neviena darbība. Varat arī manuāli notīrīt ierakstus jebkurā laikā, veicot tālāk norādītās darbības.

1. Dodieties uz **Ražošanas kontrole \> Iestatījumi \> Ražošanas izpilde \> Konfigurēt ražotnes izpildi**.
1. Darbības rūtī atlasiet **Notīrīt klienta konfigurācijas**.
1. Dialoglodziņā **Notīrīt klienta konfigurāciju** iestatiet lauku **Dienu skaits** uz neaktivitātes dienu skaitu (pirms šodienas), kas jāņem vērā. Tiks noņemtas visas konfigurācijas un pierakstīšanās ieraksti ierīcēm, kas šajā laikā nav bijušas aktīvas.
1. Atlasiet **Labi**, lai notīrītu atbilstīgās konfigurācijas, pamatojoties uz iestatījumu **Dienu skaits**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
