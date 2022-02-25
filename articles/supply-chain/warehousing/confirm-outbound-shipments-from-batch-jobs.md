---
title: Apstiprināt izejošos sūtījumus no pakešuzdevumiem
description: Šajā tēmā aprakstīts, kā iestatīt pakešuzdevumu, kas automātiski apstiprina izejošos pārvedumu sūtījumus kravām, kas ir gatavas sūtīšanai.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f68dcfc0c1454ee5b095e186c52faa6c83bf8dc6
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103919"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Apstiprināt izejošos sūtījumus no pakešuzdevumiem

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīts, kā iestatīt pakešuzdevumu, kas automātiski apstiprina izejošos pārvedumu sūtījumus kravām, kas ir gatavas sūtīšanai. Šeit aprakstītais pakešuzdevums attiecas tikai uz pārvedumu sūtījumiem, nevis uz pārdošanas pasūtījumiem.

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>Ieslēgt vai izslēgt līdzekli Apstiprināt nosūtīšanas kravas no pakešuzdevumiem

Lai izmantotu šajā tēmā aprakstīto funkcionalitāti, sistēmai *jābūt ieslēgtai funkcijai Apstiprināt izejošos sūtījumus* no pakešuzdevumiem. No Piegādes ķēdes pārvaldības versijas 10.0.21 šī funkcija ir ieslēgta pēc noklusējuma. Tāpat kā Piegādes ķēdes pārvaldībai 10.0.25 šī funkcija ir obligāta un to nevar izslēgt. Ja lietojat versiju, kas vecāka par 10.0.25, administratori šo funkcionalitāti var ieslēgt vai izslēgt, meklējot līdzekli Apstiprināt izejošos *sūtījumus*[no](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) pakešuzdevumiem līdzekļu pārvaldības darbvietā.

## <a name="process-outbound-shipments"></a>Apstrādāt izejošos sūtījumus

Lai iestatītu ieplānotu pakešuzdevumu, lai palaistu izejošo sūtījuma apstiprinājumu kravām, kas ir gatavas nosūtīšanai:

1. Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Apstrādāt izejošos sūtījumus**.
1. Atveras dialoglodziņš **Apstiprināt sūtījumu**. Kopsavilkuma cilnē **Ieraksti, kas jāiekļauj** atlasiet **Filtrs**.
1. Atveras vaicājumu redaktora dialoglodziņš. Cilnē **Diapazons** pievienojiet rindu ar sekojošajām vērtībām:
    - **Tabula** - *Kravas*
    - **Atvasinātā tabula** - *Kravas*
    - **Lauks** - *Kravas statuss*
    - **Kritēriji** - *Ielādētie*
1. Atlasiet **Labi**, lai atgrieztos dialoglodziņā **Apstiprināt sūtījumu**.
1. Kopsavilkuma cilnē **Palaist fonā** iestatiet **Partijas apstrādi** uz **Jā**.
1. Kopsavilkuma cilnē **Palaist fonā** atlasiet **Periodiskums**.
1. Atveras dialoglodziņš **Definēt periodiskumu**. Iestatiet izpildes grafiku, kas nepieciešams jūsu biznesam.
1. Atlasiet **Labi**, lai atgrieztos dialoglodziņā **Apstiprināt sūtījumu**.
1. Dialoglodziņā **Apstiprināt nosūtīšanu** atlasiet **Labi**, lai pievienotu pakešuzdevumu partijas rindai.

Plašāku informāciju par pakešdatu apstrādi skatiet [Partijas apstrādes pārskats](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]