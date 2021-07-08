---
title: Noliktavas krājumu korekcija
description: Šajā tēmā sniegta informācija par noliktavas krājumu korekciju žurnālu un apstrādi, ja izmantojat mēroga vienības.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1bf147ce430d84980516d8d4824081ee2a9321a2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271236"
---
# <a name="warehouse-inventory-adjustment"></a>Noliktavas krājumu korekcija

[!include [banner](../includes/banner.md)]

Noliktavas krājumu korekcijas līdzeklis tiek izmantots, palaižot mākoņa un malas skalas vienības [ražošanas darba noslodzei](cloud-edge-workload-manufacturing.md) un [noliktavas pārvaldības darba noslodzei](cloud-edge-workload-warehousing.md).

Ja darbinieks veic krājumu korekciju, izmantojot noliktavas programmu pret mēroga vienības noliktavas pārvaldības darba slodzi, fiziskais rīcībā esošo krājumu atjauninājums ir jāapstrādā ar pakešuzdevumu **Noliktavas krājumu korekcijas žurnāls**, ko palaižat un plānojat, atverot **Noliktavas pārvaldība > Periodiskie uzdevumi > Noliktavas krājumu korekciju žurnāls**.

Tālāk minētajiem noliktavas programmas darba procesiem pašlaik tiek izmantots **Noliktavas krājumu korekcijas žurnāls** mēroga vienības darba noslodzei:

- Korekcija ienākošā/izejošā
- Cikla inventarizācija
- Numura zīmes ielāde

Vairākas krājumu darbības ir izveidotas kā daļa no katra krājumu korekcijas procesa, jo centrmezgla un mēroga vienību izvietojumi koplieto šos krājumu ierakstus.

## <a name="inventory-adjustment-example"></a>Krājumu korekciju piemērs

Šajā piemērā noliktavas darbinieks ir izmantojis noliktavas programmu, lai reģistrētu rīcībā esošo krājumu pievienošanu.

Vispirms mēroga vienības darba noslodze izveido noliktavas krājumu korekcijas darbību pozitīvam fiziskajam pielāgojumam, kas pēc tam tiek sinhronizēts ar centrmezglu, un rezultātā palielinās rīcībā esošie krājumi centrmezgla ietvaros.

| tips                                    | Mēroga vienība | Virziens | Centrmezgls |
|-----------------------------------------|------------|-----------|-----|
| Noliktavas krājumu korekcija          | +1         | ->        | +1  |

Pēc tam centrmezgls apstrādā uzskaites žurnāla grāmatošanu, kas tiek saņemta, izmantojot [ziņojumu procesora ziņojumus](cloud-edge-message-processor-messages.md). Tas atjaunina rīcībā esošos papildu krājumus. Lai novērstu dubultos rīcībā esošos krājumus, centrmezgls kā daļu no šī procesa izveido korespondējošo darbību un noņem iepriekš reģistrētos rīcībā esošos krājumus, kas ir saistīti ar noliktavas krājumu korekciju.

| tips                                    | Mēroga vienība | Virziens | Centrmezgls |
|-----------------------------------------|------------|-----------|-----|
| Inventarizācija                                | +1         | <-        | +1  |
| Noliktavas krājuma korekcija (korespondējošā) | -1         | <-        | -1  |

Kad mēroga vienība centrmezglā ir izveidojusi **Noliktavas krājumu korekciju žurnālu**, varat pārskatīt gan **Inventarizācijas žurnālu**, gan **Korespondējošo žurnālu**, kas ir izveidots centrmezglā kā daļa korekcijas procesa.

Jūs variet pārskatīt katru no šiem žurnāla ierakstiem un transakcijam Supply Chain Management, rīkojoties šādi:

1. Pieteikties mēroga vienībā.
1. Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Noliktavas krājumu korekciju žurnāls**.
1. Lapā **Noliktavas krājumu korekciju žurnāls** atrodiet un atveriet žurnālu, kurā ierakstītas rīcībā esošo krājumu izmaiņas. Sadaļā **Žurnāla rindas** ir parādīti visi šajā žurnālā ierakstītie pielāgojumi.
1. Pieteikties centrmezglā.
1. Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Noliktavas krājumu korekciju žurnāls**.
1. Ja pārkraušanas mezgls un mēroga vienība ir sinhronizēta, lapā **Noliktavas krājumu korekciju žurnāls** jums vajadzētu redzēt to pašu žurnālu.
1. Atvērt žurnālu. Ja [ziņojumu procesora ziņojumi](cloud-edge-message-processor-messages.md) ir apstrādāti, virsrakstā redzēsit saites uz **Inventarizācijas žurnālu** un **Korespondējošo žurnālu**.
    - Žurnālam **Inventarizācijas žurnāls** jārāda tādas pašas dimensiju vērtības kā žurnāla rindām.
    - Žurnālam **Korespondējošais žurnāls** ir jārāda nobīdi, kas noņem dubulto krājuma korekciju.
    > [!NOTE]
    > Kad sinhronizācija un apstrāde ir pabeigta, **Inventarizācijas žurnāls** un **Korespondējošais žurnāls** tiek sinhronizēti atpakaļ uz mēroga vienību. Tos var arī skatīt no atbilstošās lapas **Noliktavas krājumu korekciju žurnāls**.
