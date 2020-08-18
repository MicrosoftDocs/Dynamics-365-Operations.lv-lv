---
title: Apstiprināt izejošos sūtījumus no pakešuzdevumiem
description: Šajā tēmā aprakstīts, kā iestatīt pakešuzdevumu, kas automātiski apstiprina izejošos pārvedumu sūtījumus kravām, kas ir gatavas sūtīšanai.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 41dbfb90b7b19c964e725ee0a4c769402414fb17
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652250"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Apstiprināt izejošos sūtījumus no pakešuzdevumiem

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīts, kā iestatīt pakešuzdevumu, kas automātiski apstiprina izejošos pārvedumu sūtījumus kravām, kas ir gatavas sūtīšanai. Šeit aprakstītais pakešuzdevums attiecas tikai uz pārvedumu sūtījumiem, nevis uz pārdošanas pasūtījumiem.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Iespējojiet funkciju Apstiprināt izejošos sūtījumus no pakešuzdevumiem

Lai varētu izmantot šo līdzekli, tam vispirms jābūt iespējotam sistēmā. Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lapu, lai pārbaudītu līdzekļa statusu un iespējotu to pēc nepieciešamības. Funkcija tiek norādīta kā:

- **Modulis** - *Noliktavas pārvaldība*
- **Funkcijas nosaukums** - *Apstiprināt izejošos sūtījumus no pakešuzdevumiem*

## <a name="process-outbound-shipments"></a>Apstrādāt izejošos sūtījumus

Lai iestatītu ieplānotu pakešuzdevumu, lai palaistu izejošo sūtījuma apstiprinājumu kravām, kas ir gatavas nosūtīšanai:

1. Dodieties uz **Noliktavas pārvaldība \>Periodiskie uzdevumi \> Apstrādāt izejošos sūtījumus**.
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
