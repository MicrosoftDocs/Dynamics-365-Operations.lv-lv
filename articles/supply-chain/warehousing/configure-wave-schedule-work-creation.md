---
title: Plānot darba izveidi kopuma laikā
description: Šajā tēmā ir aprakstīts, kā iestatīt un izmantot grafika darba izveides kopuma apstrādes metodi.
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 358f5a87cdb42f0ff646948da8d38475cf49e3f2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577916"
---
# <a name="schedule-work-creation-during-wave"></a>Plānot darba izveidi kopuma laikā

[!include [banner](../../includes/banner.md)]

Izmantojiet *Darba plānošanas darba izveides* līdzekli kā daļu no jūsu izveidošanas procesa, lai palīdzētu palielināt kopuma apstrādes caurlaidi, liekot sistēmai izveidot darbu, izmantojot paralēlu apstrādi.

Kad funkcionalitāte ir aktivizēta, plānotais darbs tiks izveidots automātiski, un sistēma tiks visbeidzot apstrādājusi faktisko darbu. Ja kopuma noslodzes rindu skaits sasniedz iepriekš noteiktu slieksni, sistēma izveidos faktisko darbu ātrāk, lietojot paralēlo, asinhrono apstrādi.

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a>Ieslēgt ieplānotos darba izveides līdzekļus līdzekļu pārvaldībā

Lai izmantotu šajā tēmā aprakstītos līdzekļus, tie sistēmai ir jāieslēdz. Izmantojiet [Līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lai iespējotu tālāk norādītos līdzekļus šādā secībā:

1. **Organizācijas darba bloķēšana** - nepieciešama gan manuālai, gan automātiskai ieplānotā darba izveidošanai.
1. **Plānošanas darba izveide** - nepieciešama gan manuālai, gan automātiskai ieplānotā darba izveidošanai.
1. **Organizācijas darba "Plānošanas darba izveides" kopuma metode** - nepieciešama gan manuālai, gan automātiskai ieplānotā darba izveidošanai. Jums šī funkcija nav nepieciešama, ja izmantosit tikai manuālo konfigurāciju.

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a>Automātiski konfigurēt ieplānota darba izveidi

Ja uzņēmumā iespējojat *Organizācijas "Plānošanas darba izveides" kopuma metodes* līdzekli, sistēmā automātiski tiek parādīts šāds elements:

- *Plānošanas darba izveides* kopuma metode (`WHSScheduleWorkCreationWaveStepMethod`) ir pievienota un konfigurēta tā, lai tā darbotos paralēli visām juridiskajām personām.
- Visu juridisko personu kopumu veidnes, kuru **Kopuma veidnes tips** ir iestatīts uz *Nosūtīšana* un **Veidnes statuss** iestatīts uz *Derīgs*, *Izveides darba* metode tiks aizstāta ar *Plānošanas darba izveides* metodi. Tomēr kopuma veidnes no juridiskām personām, kur *Izveides darba* metode var būt atkārtojama, netiks modificētas.
- Uzdevumu konfigurācijas *Darba plānošanas izveides* metodei tiks izveidotas visām noliktavām no visām juridiskajām personām, kurām ir iespējots **Izmantot noliktavas vadības procesus**. Tas nozīmē, ka *Darba plānošanas izveides* metode tagad tiek palaista paralēli pēc noklusējuma. Esošās noliktavas, kuru **Noliktavas vadības procesu izmantošana** tiek mainīta no *Nē* uz *Jā*, pēc noklusējuma izpildīs arī šo metodi.
- Visas juridiskās personas apstrādās kopumus paketēs un opcijai **Gaidīt slēgu (ms)** tiks iestatīta noklusējuma vērtība *60000* ms, ja tā iepriekš tika iestatīta uz *0* ms.
- Visām jaunajām izveidotām kopuma veidnēm būs *Grafika darba izveides* kopuma metode, nevis metode *Izveidot darbu*.

Esošās uzdevumu un kopuma apstrādes konfigurācijas tiks paturētas arī visām juridiskajām personām, kas jau ir konfigurētas, lai apstrādātu kopumus partijās, un visām noliktavām, kas jau ir konfigurētas, lai paralēli izmantotu metodi *Plānošanas darba izveide*.

Ja nepieciešams, varat manuāli atgriezt jebkurus vai visus iestatījumus, kas tika veikti automātiski, kad iespējojāt *Organizācijas grafika darba izveides kopuma metodes* līdzekli, tālāk rīkojoties šādi:

- Kopumu veidnes atradīsiet, dodoties uz **Noliktavas pārvaldība \> Iestatījumi \> Kopumi \> Kopuma veidnes**. Aizstāt *Darba plānošanas izveides* metodi ar *Izveidot darbu*.
- Noliktavu parametrus atradīsiet, dodoties uz **Navigācijas rūts \> Iestatījumi \> Noliktavas vadības parametri**. Cilnē **Kopuma apstrāde** lietojiet vēlamās vērtības **Kopuma apstrādei partijā** un **Gaidīt bloķēšanu (ms)**.
- Kopumu metodes atradīsiet, dodoties uz **Noliktavas pārvaldība \> Iestatījumi \> Kopumi \> Kopuma procesa metodes**. Atlasiet `WHSScheduleWorkCreationWaveStepMethod` un darbību rūtī atlasiet **Uzdevuma konfigurācija**. Ja nepieciešams, modificējiet vai dzēsiet pakešuzdevumu skaitu un katrai uzskaitītai noliktavai piešķirto kopuma grupu.

## <a name="manually-configure-scheduled-work-creation"></a>Manuāli konfigurēt ieplānota darba izveidi

Ja neiespējosit [*Organizācijas "Plānot darba izveidi" kopuma metodes* līdzekli](#Auto-enable-schedule-work-creation), , varat izmantot šajā sadaļā sniegtās procedūras, lai manuāli konfigurētu plānotā darba izveidi, kā nepieciešams.

### <a name="manually-enable-batch-processing-of-waves"></a>Manuāli iespējot kopumu pakešveida apstrādi

Lai izmantotu paralēlās asinhronās metodes priekšrocības noliktavas darba izveidošanai, kopuma procesam ir jādarbojas paketē. Lai to iestatītu:

1. Dodieties uz  **Noliktavas vadība \> Iestatīšana \> Noliktavas pārvaldības parametri**.
1. Cilnē **Vispārīgi** iestatiet opciju **Veikt kopumiem pakešveida apstrādi** uz *Jā*. Varat arī atlasīt atvēlēto **Kopuma apstrādes pakešuzdevumu grupu**, lai novērstu pakešuzdevumu rindas apstrādes darbību vienlaicīgi ar citiem procesiem.
1. Iestatiet **Gaidīt bloķēšanas (ms) laiku**, kas tiek lietots, ja sistēma apstrādā vairākus kopumus vienlaicīgi. Lielākajai daļai ražošanas procesu ieteicams izmantot vērtību *60000*.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Manuāli iespējot jauno kopuma darbības metodi esošajām kopuma veidnēm

Sākt, izveidojot jaunu kopuma darbības metodi un iespējojot to paralēlā asinhronā uzdevuma apstrādē.

1. Dodieties uz  **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma procesa metodes**.
1. Atlasiet  **Reģenerēšanas metodi** un ievērojiet, ka *WHSScheduleWorkCreationWaveStepMethod* ir pievienots kopuma apstrādes metožu sarakstam, ko varat izmantot nosūtīšanas kopuma veidnēs.
1. Atlasiet ierakstu ar **Metodes nosaukumu** *WHSScheduleWorkCreationWaveStepMethod* un atlasiet **Uzdevuma konfigurāciju**.
1. Darbību rūtī atlasiet **Jauns**, lai pievienotu rindu režģim, un pēc tam atlasiet šos iestatījumus:

    - **Noliktava** - izvēlieties noliktavu, ko izmantosiet darba izveides apstrādes plānošanai.
    - **Maksimālais pakešuzdevumu skaits** - norādiet maksimālo pakešuzdevumu skaitu. Vairākumā gadījumu šai vērtībai jābūt diapazonā no 8 līdz 16, tomēr mēs iesakām veikt optimālu iestatījumu, kas veidots, pamatojoties uz jūsu scenārijiem.
    - **Kopuma apstrādes partijas** grupa — atlasiet atvēlēto kopuma apstrādes partijas grupu, lai optimizētu jūsu partijas rindas apstrādi.

Tagad varat atjaunināt esošu kopuma veidni (vai izveidot jaunu), lai izmantotu *Darba izveides grafika* kopuma apstrādes metodi.

1. Dodieties uz  **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Saraksta rūtī atlasiet kopuma veidni, kuru vēlaties atjaunināt (ja pārbaudes izmantojat demonstrācijas datus, tad varat izmantot *24 nosūtīšanas noklusējumu*).
1. Izvērsiet kopsavilkuma cilni **Metodes** un atlasiet rindu ar **Nosaukumu** *Darba izveides grafiku* režģī **Atlikušās metodes**.
1. Atlasiet bultiņu, kas norāda uz kolonnu **Atlasītās metodes**, lai pārvietotu atlasīto rindu uz šo kolonnu. (Vienlaicīgi var būt tikai viena atlasītā metode, kas izmanto vai nu `WHSScheduleWorkCreationWaveStepMethod`, vai `createWork`, tāpēc esošā rinda ar **Metodes nosaukumu** `createWork` tiek automātiski pārvietota uz režģi **Atlikušās metodes**.)

## <a name="set-wave-task-processing-threshold-data"></a>Iestatīt kopuma uzdevuma apstrādes sliekšņa datus

Sistēma izveidos noklusējuma kopuma uzdevuma apstrādes sliekšņa datus, pirmo reizi palaižot kopuma procesu, izmantojot jebkuru uz uzdevumu balstītu apstrādi. Dati tiek izmantoti, lai kontrolētu, kad kopuma apstrāde darbosies asinhroni un būs uz uzdevumiem balstīta, kas ļauj to apstrādāt un izveidot darbu paralēli.

Noklusējuma dati sākotnēji izmantos 15 sliekšņa vērtību minimālajam kravas rindu skaitam (`MINIMUMWAVELOADLINES`). Tas nozīmē, ka, kad sistēma apstrādā laidienu ar vairāk nekā 15 noslodzes rindām, tas izmantos asinhronu uzdevumu apstrādi. Šos datus var manuāli ievietot/atjaunināt `WHSWaveTaskProcessingThresholdParameters` tabulā testēšanas vidēs. Ja jums ir jāmaina šis iestatījums ražošanas vidē, jums ir jāsazinās ar Microsoft Support, lai pieprasītu atjauninājumu.

## <a name="work-with-the-scheduled-work-creation"></a>Darbs ar plānoto darbu izveidi

Detalizētu informāciju par to, kā strādāt ar plānoto darba izveidi, skatiet sadaļā [Kopuma izveide un apstrāde](wave-processing.md). 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
