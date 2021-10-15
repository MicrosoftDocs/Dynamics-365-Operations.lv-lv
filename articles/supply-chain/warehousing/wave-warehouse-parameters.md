---
title: Noliktavas parametri kopuma apstrādei
description: Šajā tēmā ir aprakstīts, kā iestatīt noliktavu parametrus kopuma apstrādei programmā . Kopuma apstrādi varat izmantot grupas izdošanas darbam, lai izpildītu vairākus darbu pasūtījumus vienā kopumā.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cd7961ae8f4237bcee7ae4c53365d24ab03c5aa9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572222"
---
# <a name="warehouse-parameters-for-wave-processing"></a>Noliktavas parametri kopuma apstrādei

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt noliktavu parametrus kopuma apstrādei programmā . Kopuma apstrādi varat izmantot grupas izdošanas darbam, lai izpildītu vairākus darbu pasūtījumus vienā kopumā.

Lai izmantotu kopuma apstrādi, lapā **Noliktavas pārvaldības parametri** norādiet šādu informāciju:

- Vai varat apstrādāt kopumus, izmantojot pakešuzdevumu.
- Vai apkopot informāciju žurnālfailā, kad tiek apstrādāti kopumi.

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a>Noliktavas pārvaldības parametru iestatīšana kopuma apstrādei

Lai iestatītu noliktavu parametrus kopuma apstrādei, izpildiet tālāk aprakstītās darbības:

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Noliktavas pārvaldības parametri**.

1. Kopsavilkuma cilnē **Kopuma apstrāde** veiciet šādus iestatījumus:

    - **Kopuma apstrādes pakešgrupa** - Atlasiet pakešuzdevumu grupu, kas jāizmanto, kad apstrādājat kopumus, izmantojot pakešuzdevumus. Pakešuzdevumu grupa norāda serveri, kurā darbosies pakešuzdevumi.
    - **Veikt kopumiem pakešveida apstrādi** — izvēlieties, vai iespējot laišanu automātisku apstrādi, izmantojot pakešuzdevumu. Lai izmantotu paralēlo apstrādi, iestatiet to kā *Jā*. Pakešuzdevumu varat iestatīt lapā **Kopumu apstrāde**. (Skatiet arī piezīmi šī saraksta beigās.)
    - **Izveidot kopuma norises žurnālu** — izvēlieties, vai sistēmai ir jāģenerē žurnāla ieraksts katru reizi, kad krājumam un tā dimensijām sākas un beidzas sadalījums. Šis žurnāls jāiespējo tikai tad, kad tas ir nepieciešams, piemēram, sākotnējās testēšanas vai problēmu novēršanas laikā. Papildu informāciju skatiet [Kopuma sadalījums](wave-allocation-method.md).
    - **Izveidot kopuma apstrādes vēstures žurnālu** — izvēlieties, vai automātiski saglabāt informāciju par kopumu žurnālfailā pēc kopuma apstrādes, tostarp gaidošo sadalījumu paralēlas apstrādes laikā. Parasti to vajadzētu iespējot tikai problēmu novēršanas laikā, jo tā pievieno papildu papildu papildu pieskaitāmās izmaksas. Lai skatītu žurnālu, dodieties uz **Noliktavas pārvaldība \>Izejošie kopumi \> Kopumu apstrādes vēstures žurnāls**. Plašāku informāciju par kopuma apstrādi skatiet sadaļā [Kopuma izveide un apstrāde](wave-processing.md).
    - **Izveidot konteineriizēšanas vēstures žurnālu** — izvēlieties, vai automātiski saglabāt informāciju par kopuma konteinerinēšanu žurnāla failā pēc kopuma apstrādes. Lai aplūkotu žurnālu, dodieties uz **Noliktavas pārvaldība \> Iepakošana un konteinerizēšana \> Konteinerizēšanas vēsture**.
    - **Gaidīt slēgu (ms)** - Ievadiet milisekundēs izteiktu laiku, cik ilgi sadalījuma darbībai ir jāgaida sistēmas resurss, kuru ir bloķējusi cita sadalījuma darbība. Kad šis laiks ir pagājis, kopums netiek apstrādāts un tiek parādīts kļūdas ziņojums.

1. Kopsavilkuma cilnē **Atbrīvot uz noliktavu** veiciet šādus iestatījumus:

    - **Paketes kļūmes kļūda** - izvēlieties, vai ģenerēt kļūdu, ja pārsūtīšana uz noliktavas pakešuzdevumu neizdodas. Ja šis ir aktivizēts, neizdevušos darbus beidzas ar statusu *Kļūda*. Ja šis ir aktivizēts, neizdevušos darbus beidzas ar statusu *Izbeigts*.

> [!NOTE]
> Kopuma apstrādei izmantotajā kopuma veidnē varat norādīt iestatījumus, kuri automatizē kopuma apstrādi. Ja pakešuzdevumam iestatāt grafiku, tā hronometrāža ir jāsaskaņo ar automatizācijas iestatījumiem kopuma veidnē. Papildinformāciju skatiet [Kopuma veidņu izveide](wave-templates.md).
>
> Ja izmantojat *Transporta pārvaldību* un *Uzlabotu noliktavas pārvaldību*, varat norādīt, vai kopuma apstrādes laikā ir jāveic kravu konsolidēšana. Tas var noderēt, piemēram, ja vairākas mazas kravas var nosūtīt vienlaicīgi. Lai konsolidētu noslodzes, kad apstrādājat kopumu, cilnē **Noslodzes** atzīmējiet izvēles rūtiņu **Konsolidēt noslodzes kopuma apstrādes laikā**.</P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a>Pilnas vai daļējas rezervācijas iestatīšana ražošanas kopumiem

Pārdošanas pasūtījumiem un Kanban pasūtījumiem pirms pasūtījuma pārvietošanas uz noliktavu attiecīgie krājumi ir jārezervē. Pretējā gadījumā krājumus vai sadalījuma rindas nevar apstrādāt kopumā. Taču ražošanas pasūtījumi ir nedaudz elastīgāki. Ražošanas pasūtījumiem varat norādīt tālāk aprakstīto informāciju:

- Ļaut ražošanas pasūtījumus pārvietot uz noliktavu, lai gan visus materiālus nevar rezervēt. Ja atlasāt šo opciju, pārvietošana uz noliktavu ir manuāli jāatkārto, kad papildu materiāli kļūst pieejami. Tas var noderēt, piemēram, ja jums ir ražošanas sākšanai nepieciešamie materiāli, un varat pagaidīt, līdz kļūst pieejami papildu materiāli.
- Pieprasīt, ka pirms pasūtījuma pārvietošanas uz noliktavu ir rezervēti visi materiāli.

Lai pieprasītu pilnu rezervēšanu vai atļautu daļēju rezervēšanu, izpildiet tālāk aprakstītās darbības:

1. Dodieties uz **Ražošanas kontrole** \> **Iestatījumi** \> **Ražošanas kontroles parametri**.
1. Cilnes **Vispārīgi** laukā **Izlaist uz noliktavu** atlasiet noklusējuma iestatījumus.
