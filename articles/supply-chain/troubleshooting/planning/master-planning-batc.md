---
title: Vispārējās plānošanas krājumus nevar filtrēt pēc to saistītajām vajadzību grupu vērtībām
description: Vispārējās plānošanas krājumus nevar filtrēt pēc to saistītajām vajadzību grupu vērtībām.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049479"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>Vispārējās plānošanas krājumus nevar filtrēt pēc to saistītajām vajadzību grupu vērtībām

KB numurs: 4612572

## <a name="symptoms"></a>Simptomi

Ir jāfiltrē krājumi, kas tiks iekļauti vispārējā plānošanas pakešuzdevumā, pamatojoties uz saistīto ierakstu vērtībām no krājumu vajadzības tabulas. (Piemēram, jūs vēlaties filtrēt krājumus pēc to **Kreditora** un/vai **Vajadzības grupas** vērtības). Pakešuzdevuma filtra iestatījumi ļauj izveidot savienojumu no tabulas **Krājumi** uz tabulu **Krājumu vajadzības**, un pēc tam vaicājumā norādīt lauku vērtības no krājumu vajadzību tabulas. Tomēr pēc šī iestatījuma pabeigšanas sistēma vēl joprojām izveido plānotos pasūtījumus visam krājumu nodrošinājumam ne tikai krājumiem, kas atbilst norādītajām lauku vērtībām krājumu vajadzību tabulā.

## <a name="resolution"></a>Novēršana

Pakešuzdevumu filtrs var filtrēt tikai krājumiem. Lai arī varat pievienot savienojumu **Krājumu vajadzību** tabulai, filtrēšanas iestatījumi, kurus šajā tabulā izveidojat, neietekmē vaicājuma izvadi. Izpildlaikā sistēma palaiž plānošanu visām vajadzības grupām un visām variācijām, kas ir filtrētiem krājumiem. Kad krājums jau ir iekļauts izpildē, visas vajadzības grupas, kas ir iekļautas krājumu filtrā, neietekmē plānošanas izvadi.
