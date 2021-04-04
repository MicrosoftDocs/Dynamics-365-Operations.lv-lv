---
title: Plānot darba izveidi kopuma laikā
description: Šajā tēmā ir aprakstīts, kā iestatīt un izmantot grafika darba izveides kopuma apstrādes metodi.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501226"
---
# <a name="schedule-work-creation-during-wave"></a>Plānot darba izveidi kopuma laikā

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Izmantojiet *Darba plānošanas darba izveides* līdzekli kā daļu no jūsu izveidošanas procesa, lai palīdzētu palielināt kopuma apstrādes caurlaidi, liekot sistēmai izveidot darbu, izmantojot paralēlu apstrādi.

Kad funkcionalitāte ir aktivizēta, plānotais darbs tiks izveidots automātiski, un sistēma tiks visbeidzot apstrādājusi faktisko darbu. Ja kopuma noslodzes rindu skaits sasniedz iepriekš noteiktu slieksni, sistēma izveidos faktisko darbu ātrāk, lietojot paralēlo, asinhrono apstrādi.

## <a name="enable-the-schedule-work-creation-feature"></a>Iespējot darba plānošanas darba izveides līdzekli

### <a name="enable-the-feature-in-feature-management"></a>Jaunu līdzekļu iespējošana līdzekļu pārvaldībā

Lai varētu izmantot līdzekli *Darba izveides grafiks*, tas vispirms ir jāieslēdz jūsu sistēmā. Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Darba izveides grafiks*

> [!NOTE]
> Pirms *Darba plānošanas izveides* jāiespējo *Organizācijas līmeņa darba bloķēšanas* funkcija.

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

1. Atlasiet bultiņu, kas norāda uz kolonnu **Atlasītās metodes**, lai pārvietotu atlasīto rindu uz šo kolonnu. (Vienlaicīgi var būt tikai viena atlasītā metode, kas izmanto vai nu *WHSScheduleWorkCreationWaveStepMethod*, vai *createWork*, tāpēc esošā rinda ar **Metodes nosaukumu** *createWork*  tiek automātiski pārvietota uz režģi **Atlikušās metodes**.)

## <a name="set-wave-task-processing-threshold-data"></a>Iestatīt kopuma uzdevuma apstrādes sliekšņa datus

Sistēma izveidos noklusējuma kopuma uzdevuma apstrādes sliekšņa datus, pirmo reizi palaižot kopuma procesu, izmantojot jebkuru uz uzdevumu balstītu apstrādi. Dati tiek izmantoti, lai kontrolētu, kad kopuma apstrāde darbosies asinhroni un būs uz uzdevumiem balstīta, kas ļauj to apstrādāt un izveidot darbu paralēli.

Noklusējuma dati sākotnēji izmantos 15 sliekšņa vērtību minimālajam kravas rindu skaitam (MINIMUMWAVELOADLINES). Tas nozīmē, ka, kad sistēma apstrādā laidienu ar vairāk nekā 15 noslodzes rindām, tas izmantos asinhronu uzdevumu apstrādi. Varat manuāli ievietot/atjaunināt šos datus tabulā **WHSWaveTaskProcessingThresholdParameters** savās pārbaudes vidēs, bet, ja jums ir jāmaina šis iestatījums ražošanas vidē, ir jāsazinās ar Microsoft atbalsta dienestu, lai pieprasītu atjaunināšanu.

## <a name="work-with-the-feature"></a>Darbs ar šo līdzekli

Kad *Grafika darba izveides* funkcionalitāte ir aktivizēta, kopuma apstrāde izveidos plānoto darbu, ko visbeidzot izmantos jaunais darba izveides process. Darba izveides laikā darbs tiks bloķēts, izmantojot *Organizācijas līmeņa darba bloķēšanas* iespēju.

Šajā plūsmkartē ir parādīts, kā kopuma apstrādes laikā tiek veidots plānotais darbs.

![Ieplānot darba izveidi](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Plānots darbs

**Plānotā darba detalizētas informācijas** lapa (**Noliktavas pārvaldība \> Darbs \> Plānotā darba informācija**) rāda informāciju par plānoto darbu, kas sākotnēji tika izveidots kopuma apstrādes laikā. Ir pieejami sekojošas **Procesa statusa** vērtības:

- **Ievietots rindā** - plānotais darbs gaida darbu izveides procesu.
- **Pabeigts** – plānotais darbs ir izmantots darba izveidei.
- **Neizdevās** — kopuma apstrāde neizdevās. Ievērojiet, ka plānotais darbs var būt stāvoklī **Neizdevās** ar vai bez saistītā faktiskā darba. Ja faktiskais darba izveides process neizdodas, faktiskais darbs paliek statusā *Atcelts*.

### <a name="batch-job-for-the-work-creation-process"></a>Pakešuzdevums darba izveides procesam

Lai skatītu kopumu apstrādes pakešuzdevumus, atlasiet darbību rūtī **Pakešuzdevumi** lapā **Visi kopumi**.

No šejienes jūs varat skatīt visu pakešuzdevumu detaļas katram pakešuzdevumu laukā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]