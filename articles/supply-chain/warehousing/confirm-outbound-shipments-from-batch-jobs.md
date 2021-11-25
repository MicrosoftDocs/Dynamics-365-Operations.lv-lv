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
ms.openlocfilehash: 4af84383fe1d214849d5d05463bd0cbfad7d0536
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778477"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Apstiprināt izejošos sūtījumus no pakešuzdevumiem

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīts, kā iestatīt pakešuzdevumu, kas automātiski apstiprina izejošos pārvedumu sūtījumus kravām, kas ir gatavas sūtīšanai. Šeit aprakstītais pakešuzdevums attiecas tikai uz pārvedumu sūtījumiem, nevis uz pārdošanas pasūtījumiem.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Iespējojiet funkciju Apstiprināt izejošos sūtījumus no pakešuzdevumiem

No Piegādes ķēdes pārvaldības versijas 10.0.21 šī funkcija ir ieslēgta pēc noklusējuma. Administratori var izmantot Līdzekļu [pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lapu, lai pārbaudītu līdzekļu statusu un aktivizētu vai atspējotu to, ja nepieciešams. Šeit līdzeklis tiek norādīts kā:

- **Modulis** - *Noliktavas pārvaldība*
- **Funkcijas nosaukums** - *Apstiprināt izejošos sūtījumus no pakešuzdevumiem*

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