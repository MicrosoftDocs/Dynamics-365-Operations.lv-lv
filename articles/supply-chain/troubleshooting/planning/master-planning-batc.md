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
ms.openlocfilehash: 9750a73f0962179512c5e21a614a276c313ff975b7494f31589ca936886ecf6e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781397"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>Vispārējās plānošanas krājumus nevar filtrēt pēc to saistītajām vajadzību grupu vērtībām

KB numurs: 4612572

## <a name="symptoms"></a>Simptomi

Ir jāfiltrē krājumi, kas tiks iekļauti vispārējā plānošanas pakešuzdevumā, pamatojoties uz saistīto ierakstu vērtībām no krājumu vajadzības tabulas. (Piemēram, jūs vēlaties filtrēt krājumus pēc to **Kreditora** un/vai **Vajadzības grupas** vērtības). Pakešuzdevuma filtra iestatījumi ļauj izveidot savienojumu no tabulas **Krājumi** uz tabulu **Krājumu vajadzības**, un pēc tam vaicājumā norādīt lauku vērtības no krājumu vajadzību tabulas. Tomēr pēc šī iestatījuma pabeigšanas sistēma vēl joprojām izveido plānotos pasūtījumus visam krājumu nodrošinājumam ne tikai krājumiem, kas atbilst norādītajām lauku vērtībām krājumu vajadzību tabulā.

## <a name="resolution"></a>Novēršana

Pakešuzdevumu filtrs var filtrēt tikai krājumiem. Lai arī varat pievienot savienojumu **Krājumu vajadzību** tabulai, filtrēšanas iestatījumi, kurus šajā tabulā izveidojat, neietekmē vaicājuma izvadi. Izpildlaikā sistēma palaiž plānošanu visām vajadzības grupām un visām variācijām, kas ir filtrētiem krājumiem. Kad krājums jau ir iekļauts izpildē, visas vajadzības grupas, kas ir iekļautas krājumu filtrā, neietekmē plānošanas izvadi.
