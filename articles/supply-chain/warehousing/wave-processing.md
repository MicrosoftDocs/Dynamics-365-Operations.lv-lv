---
title: Kopumu izveide un apstrāde
description: Tālāk ir aprakstīts, kā manuāli izveidot, apstrādāt un izlaist kopumu, lai izveidotu izdošanas darbu kravas, sūtījuma, ražošanas pasūtījuma vai Kanban pasūtījuma izveidei.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, WHSParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage, WHSProdWaveTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4b7c01a21dcbe7543332439ee6fd371b426851f4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579932"
---
# <a name="wave-creation-and-processing"></a>Kopumu izveide un apstrāde

[!include [banner](../includes/banner.md)]

Tālāk ir aprakstīts, kā manuāli izveidot, apstrādāt un izlaist kopumu, lai izveidotu izdošanas darbu kravas, sūtījuma, ražošanas pasūtījuma vai Kanban pasūtījuma izveidei. Varat izveidot šādus pasūtījuma veidu kopumus:

- **Pārdošanas pasūtījumi** — izmantojiet sūtījuma kopumus, lai iekļautu rindas no pārdošanas pasūtījumiem. Kad pārdošanas pasūtījums tiek izlaists uz noliktavu, pārdošanas pasūtījuma rindās var iekļaut kopumu.
- **Ražošanas pasūtījumi** — izmantojiet ražošanas kopumus, lai precei iekļautu rindas no materiālu komplektiem (MK).
- **Kanban pasūtījumi** — Kanban kopumos ir iekļauts izdošanas saraksta rindas no Kanban pasūtījumiem.

Pārdošanas pasūtījumiem un Kanban pasūtījumiem pirms pasūtījuma pārvietošanas uz noliktavu attiecīgie krājumi ir jārezervē. Pretējā gadījumā krājumus vai sadalījuma rindas nevar apstrādāt kopumā. Taču ražošanas pasūtījumi ir nedaudz elastīgāki. Ražošanas pasūtījumiem var izvēlēties vienu no šīm opcijām:

- Pieprasīt, ka pirms pasūtījuma pārvietošanas uz noliktavu ir rezervēti visi materiāli.
- Ļaut ražošanas pasūtījumus pārvietot uz noliktavu, lai gan visus materiālus nevar rezervēt. Ja atlasāt šo opciju, pārvietošana uz noliktavu ir manuāli jāatkārto, kad papildu materiāli kļūst pieejami. Tas var noderēt, piemēram, ja jums ir ražošanas sākšanai nepieciešamie materiāli, un varat pagaidīt, līdz kļūst pieejami papildu materiāli.

Izmantojot lauku **Vajadzība pēc materiālu rezervēšanas** lapā **Ražošanas kontroles parametri**, varat norādīt, kuru no šīm ražošanas pasūtījuma opcijām izmantot pēc noklusējuma. Taču jebkurā laikā varat mainīt noteikta ražošanas pasūtījuma iestatījumu, ja nepieciešams. Plašāku informāciju skatiet [Noliktavas parametri kopumu apstrādei](wave-warehouse-parameters.md).

## <a name="create-and-process-a-wave"></a>Kopuma izveide un apstrāde

Šajā diagrammā ir parādīta plūsma, kā tiek veidoti, apstrādāti un izlaisti nosūtīšanas kopumi. Numuri atbilst šajā sadaļā tālāk norādītajām sadaļām.

![Kopuma izveides apstrāde.](media/wave-processing-diagram.png "Kopuma izveides apstrāde")

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat, kopuma veidnei jābūt pieejamai kopuma tipam, kuru vēlaties izveidot (nosūtīšana, ražošana vai Kanban). Kopuma veidne nosaka daudzus iestatījumus, kā kopums tiks ģenerēts un apstrādāts, ieskaitot to, kuras darbības jāveic manuāli un kuras tiek veiktas automātiski. Papildu informāciju skatiet [Kopuma veidnes](wave-templates.md).

### <a name="create-a-wave"></a>Izveidot kopumu

#### <a name="automatically-create-waves-based-on-warehouse-and-order-type"></a>Automātiski izveidot viļņus, pamatojoties uz noliktavu un pasūtījuma tipu

Lai viļņus izveidotu automātiski, iestatiet [Kopuma veidnes](wave-templates.md), kas attiecas uz katru atbilstošo pasūtījuma tipu un noliktavu. Pārliecinieties, vai katrai veidnei ir iestatīta opcija **Automatizēt kopuma izveidi** uz *Jā*.

#### <a name="manually-create-waves"></a>Manuāli izveidojiet kopumus

Lai manuāli izveidotu kopumu, veiciet tālāk aprakstītās darbības:

1. Pārliecinieties, vai atbilstošās [Kopuma veidnes](wave-templates.md) nav iestatītas automātiskai kopuma izveidei noliktavai un pasūtījumu tipiem, kur vēlaties to darīt manuāli.
1. Atkarībā no izveidojamā kopuma veida, noklikšķiniet uz vienas tālāk minētajām opcijām:

    - Dodieties uz **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi kopumi**. Darbību rūtī atlasiet **Kopums**.
    - Dodieties uz **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi ražošanas kopumi**. Darbību rūtī atlasiet **Ražošanas kopums**.
    - Dodieties uz **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi Kanban kopumi**. Darbību rūtī atlasiet **Izveidot kopumu**.

1. Laukā **Apraksts** ievadiet īsu kopuma aprakstu. Tam jāraksturo, kas tiks apstrādāts kopumā.

1. Laukā **Kopuma veidnes nosaukums** atlasiet kopuma veidni kopuma veidam, ko vēlaties izveidot. Kopuma veidnē ir ietvertas kopuma metodes, kas veiks darbības, piemēram, izveidos kopuma darbu. Piemēram, kopuma veidnē sūtījuma kopumiem var būt ietvertas kravu izveides, rindu piešķiršanas kopumiem, papildināšanas un izdošanas darba izveides kopumam metodes.

1. Nav obligāti: ja kopumu atribūtus vēlaties izmantot kā papildu vaicājuma kritēriju kopumam, atribūtus atlasiet laukos **Kopuma atribūti**.

### <a name="specify-what-to-include-in-a-wave"></a>Nosakiet ko iekļaut kopumā

Pēc kopuma izveides jūs esat gatavs sākt pievienot saturu.

> [!NOTE]
> Ja nepieciešams, varat pievienot rindas kopumam pat pēc tā apstrādes, kamēr tas nav izlaists.

#### <a name="automatically-specify-what-to-include-in-a-wave"></a>Automātiski nosakiet, ko iekļaut kopumā

Lai viļņus izveidotu automātiski, iestatiet [Kopuma veidnes](wave-templates.md), kas attiecas uz katru atbilstošo pasūtījuma tipu un noliktavu. Pārliecinieties, vai katrai veidnei ir iestatīta opcija **Automatizēt kopuma izveidi** uz *Jā*. Vai arī veidne var automātiski piešķirt rindas jebkuram atbilstošajam atvērtajam kopumam, ja opcija **Piešķirt atvērtajiem kopumiem** ir iestatīta uz *Jā*.

#### <a name="manually-specify-what-to-include-in-a-wave"></a>Manuāli nosakiet, ko iekļaut kopumā

Kad kopums ir izveidots, bet vēl nav izlaists, varat manuāli norādīt, ko tajā iekļaut. Lai manuāli pievienotu līnijas kopumam:

1. Atkarībā no kopuma veida, lai pievienotu rindas, veiciet vienu no šīm darbībām:

    - Dodieties uz **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi kopumi**. Darbību rūtī atlasiet **Kopums**.
    - Dodieties uz **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi ražošanas kopumi**. Darbību rūtī atlasiet **Ražošanas kopums**.
    - Dodieties uz **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi Kanban kopumi**. Darbību rūtī atlasiet **Izveidot kopumu**.

1. Atlasiet kopumu. Sadaļā Darbību rūts noklikšķiniet uz viena no tālāk aprakstītajiem vienumiem:

      - **Uzturēt kravas**
      - **Uzturēt ražošanu**
      - **Uzturēt Kanban darba izdošanas sarakstus**

1. Loga augšējā daļā atlasiet rindu, lai pievienotu kopumam, un pēc tam noklikšķiniet uz **Pievienot kopumam**. Rinda tiek pārvietota uz kopsavilkuma cilni **Kopuma rindas**.

    Atkārtojiet šo darbību katrai pievienojamajai rindai. Lai pievienotu visas rindas, atlasiet **Pievienot visus**.

    > [!TIP]
    > Sūtījuma kopumiem var ātri atrast noteiktu pasūtījumu, laukā **Kopuma filtra kods** atlasot pielāgoto filtru. Kopuma filtru kodi ietver vaicājuma kritērijus sūtījumiem, kas tika izveidoti formā **Kopuma filtri**. Šis lauks nav pieejams ražošanas vai Kanban kopumiem.
    > Zaļš ķeksītis kolonnā **Kopumā** nozīmē, ka sūtījums tika pievienots kopumam.

### <a name="process-the-wave-to-create-the-picking-work"></a>Apstrādājiet kopumu, lai izveidotu izdošanas darbu

Kad kopums ir izveidots un satur visas nepieciešamās rindas, varat to apstrādāt, lai izveidotu atbilstošu izdošanas darbu.

#### <a name="automatically-process-a-wave"></a>Automātiski apstrādāt kopumu

Lai automātiski apstrādātu kopumu, iestatiet atbilstošās [Kopuma veidnes](wave-templates.md) ar nepieciešamajām automātiskās apstrādes opcijām.

#### <a name="manually-process-a-wave"></a>Manuāli apstrādāt kopumu

Kopumu var apstrādāt tikai tad, ja **Kopuma statuss** is *Izveidots*. Pēc kopuma apstrādes **Kopuma statuss** tiks mainīts uz *Aizturēts*.

Lai manuāli apstrādātu kopumu, kurā ir viss nepieciešamais saturs, rīkojieties šādi:

1. Atkarībā no apstrādājamā kopuma veida veiciet tālāk norādītās darbības:

    - Atlasiet **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi kopumi**. Darbību rūtī atlasiet **Kopums**.
    - Atlasiet **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi ražošanas kopumi**. Darbību rūtī atlasiet **Ražošanas kopums**.
    - Atlasiet **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi Kanban kopumi**. Darbību rūtī atlasiet **Izveidot kopumu**.

1. Atlasiet apstrādājamo kopumu. Darbību rūtī atlasiet **Apstrādāt**.

### <a name="release-the-wave-to-the-warehouse-to-start-picking-and-packing"></a>Izlaidiet kopumu uz noliktavu, lai sāktu izdošanu un iepakošanu

Lai kopumu varētu izlaist, tas ir jāapstrādā. Izlaižot kopumu, izdošanas darbs ir pieejams noliktavā. Varat atcelt kopumu pēc tā izlaišanas un pievienot papildu rindas, bet rindas nevar mainīt.

#### <a name="automatically-release-a-wave"></a>Automātiski apstrādāt kopumu

Lai automātiski apstrādātu kopumu, iestatiet atbilstošās [Kopuma veidnes](wave-templates.md) ar nepieciešamajām automātiskās apstrādes opcijām.

#### <a name="manually-release-a-wave"></a>Manuāli izlaist kopumu

Lai manuāli izlaistu kopumu, veiciet tālāk aprakstītās darbības:

1. Atkarībā no apstrādājamā kopuma veida veiciet tālāk norādītās darbības:

      - Atlasiet **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi kopumi**. Darbību rūtī atlasiet **Kopums**.
      - Atlasiet **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi ražošanas kopumi**. Darbību rūtī atlasiet **Ražošanas kopums**.
      - Atlasiet **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi Kanban kopumi**. Darbību rūtī atlasiet **Izveidot kopumu**.

1. Atlasiet izlaižamo kopumu. Darbību rūtī atlasiet **Izveidot kopumu**.

## <a name="containerize-a-wave"></a>Konteinerizēt kopumu

Automatizētā konteinerizēšana kopuma apstrādāšanas laikā sūtījumiem izveido konteinerus un izdošanas darbu. Detalizētu informāciju par to, kā iestatīt, skatiet [Konteinerizēšana](wave-containerization.md).

## <a name="work-with-the-scheduled-work-creation"></a>Darbs ar plānoto darbu izveidi

Kad *Grafika darba izveides* funkcionalitāte ir aktivizēta, kopuma apstrāde izveidos plānoto darbu, ko visbeidzot izmantos jaunais darba izveides process. Darba izveides laikā darbs tiks bloķēts, izmantojot *Organizācijas līmeņa darba bloķēšanas* iespēju. Lai iegūtu papildu informāciju, skatiet [Darba izveides plānošana kopuma laikā](configure-wave-schedule-work-creation.md).

Šajā plūsmkartē ir parādīts, kā kopuma apstrādes laikā tiek veidots plānotais darbs.

![Ieplānot darba izveidi.](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Plānots darbs

**Plānotā darba detalizētas informācijas** lapa (**Noliktavas pārvaldība \> Darbs \> Plānotā darba informācija**) rāda informāciju par plānoto darbu, kas sākotnēji tika izveidots kopuma apstrādes laikā. Ir pieejami sekojošas **Procesa statusa** vērtības:

- **Ievietots rindā** - plānotais darbs gaida darbu izveides procesu.
- **Pabeigts** – plānotais darbs ir izmantots darba izveidei.
- **Neizdevās** — kopuma apstrāde neizdevās. Ievērojiet, ka plānotais darbs var būt stāvoklī **Neizdevās** ar vai bez saistītā faktiskā darba. Ja faktiskais darba izveides process neizdodas, faktiskais darbs paliek statusā *Atcelts*.

### <a name="batch-job-for-the-work-creation-process"></a>Pakešuzdevums darba izveides procesam

Lai skatītu kopumu apstrādes pakešuzdevumus, atlasiet darbību rūtī **Pakešuzdevumi** lapā **Visi kopumi**.

No šejienes jūs varat skatīt visu pakešuzdevumu detaļas katram pakešuzdevumu laukā.

## <a name="cancel-a-wave"></a>Kopuma atcelšana

Ja nepieciešams, varat atcelt kopumu, kas ir apstrādāts. Lai atceltu kopumu un izveidoto izdošanas darbu, veiciet tālāk norādītās darbības:

1. Atkarībā no atceļamā kopuma veida veiciet tālāk norādītās darbības:

      - Dodieties uz **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi kopumi**.
      - Dodieties uz **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi ražošanas kopumi**.
      - Dodieties uz **Noliktavas pārvaldība** \> **Vispārēji** \> **Kopumi** \> **Sūtījuma kopumi** \> **Visi Kanban kopumi**.

1. Atlasiet atceļamo kopumu. Darbību rūts cilnē **Darbs** atlasiet **Atcelt**.

## <a name="review-wave-batch-job-details"></a>Pārskatīt kopuma pakešuzdevuma detaļas

Izmantojiet **Kopuma pakešuzdevuma informācijas** lapu, lai pārbaudītu pakešuzdevumus un saistītos uzdevumus, kas saistīti ar jebkuru kopumu. Tas ir īpaši noderīgi, lai novērstu problēmas, kas saistītas ar neizdevušos kopumu. Bez šī līdzekļa tikai administratoriem parasti ir piekļuve detalizētai informācijai par pakešuzdevumu. Pakešuzdevuma **Informācijas par kopumu** lapu var padarīt pieejamu lietotājiem, kas nav administratori, un tā nodrošina tikai lasāmu pakešuzdevumu un saistīto uzdevumu skatu.

### <a name="enable-the-wave-batch-job-details-page"></a>Iespējot pakešuzdevuma kopuma informācijas lapu

Ja sistēmā vēl nav iekļauta lapa **Kopuma pakešuzdevuma detalizēta informācija**, dodieties uz [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un ieslēdziet *Kopuma pakešuzdevuma detalizētās informācijas* līdzekli.

### <a name="use-the-wave-batch-job-details-page"></a>Izmantot pakešuzdevuma kopuma informācijas lapu

**Kopuma pakešuzdevuma informācijas** lapa apvieno pakešuzdevumus un pakešuzdevumu uzdevumus, kas ļauj izpētīt visus kopuma soļus bez nepieciešamības naviģēt turp un atpakaļ starp vienu pakešuzdevumu un pakešuzdevumu sarakstu. Lapa nodrošina arī piekļuvi pakešuzdevumu žurnālam un, ja jums ir nepieciešamās atļaujas, nodrošina saiti uz lapu **Pakešuzdevumi**.

Lai atvērtu šo lapu, atlasiet kopumu jebkurā no vairākām atšķirīgām kopuma lappusēm un pēc tam darbību rūtī atlasiet **Kopuma pakešuzdevuma informācija**.

## <a name="review-load-validation-and-error-messages"></a>Kravas pārvaudes un kļūdu ziņojumu pārskats

Kopumu apstrādes laikā sistēma validē un parāda katras slodzes rindas statusu vilnī. Ja brīdinājumi nenotiek, tas turpinās līdz nākamajam kopuma solim. Ja tiek parādīti brīdinājumi, pēc visa kopuma pārbaudes tā vietā tiek parādīta šāda kļūda:

> Atrastas nederīgas ielādes rindas kopumos. Lūdzu, noņemiet nederīgās ielādes rindas.

Pēc tam jūs varat pārskatīt katras slodzes rindas galīgo statusu kopumā un izlabot visus brīdinājumus, pirms mēģināt vēlreiz. Tas ļauj novērst visus brīdinājumus uzreiz pirms kopuma pārstrādes. (Iepriekšējos laidienos sistēma pārtrauca kopuma apstrādi pēc pirmā brīdinājuma, tāpēc brīdinājumus varēja labot tikai pa vienam.)

Veids, kādā sistēma parāda kopuma apstrādes statusa ziņojumus, ir atkarīgs no tā, kā esat iestatījis opciju **Izveidot kopuma apstrādes vēstures žurnālu** lapā **Noliktavas pārvaldības parametri**.

- Ja **Izveidot kopuma apstrādes vēstures žurnālu** ir iestatīta uz *Nē*, ielādes rindas statusa ziņojumi tiek parādīti **Informācijas žurnālā**.
- Ja **Izveidot kopuma apstrādes vēstures žurnālu** ir iestatīta uz *Jā*, ielādes rindas statusa ziņojumi tiek parādīti lapā **Kopuma apstrādes vēstures žurnāls**. Lai skatītu žurnālu, dodieties uz **Noliktavas pārvaldība \> Izejošie kopumi \> Kopumu apstrādes vēstures žurnāls**.

## <a name="additional-resources"></a>Papildu resursi

- [Kopuma apstrādes piemēra konfigurēšana](tasks/configure-wave-processing.md)
- [Laidiena veidnes](wave-templates.md)
- [Konteinerizēšana](wave-containerization.md)