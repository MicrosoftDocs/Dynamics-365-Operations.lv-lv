---
title: "Krājumu vietas"
description: "Krājumu atrašanās vietu dati tiek izmantoti kopā ar pamata noliktavu (WMS I), lai noteiktu, kur tiek glabāti krājumi un kur krājumi tiek izdoti no WMS I noliktavas."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSLocation
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 95d93c9d471cc86877f35340693c171958db71df
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---

# <a name="inventory-locations"></a>Krājumu vietas

[!include[banner](../includes/banner.md)]


Krājumu atrašanās vietu dati tiek izmantoti kopā ar pamata noliktavu (WMS I), lai noteiktu, kur tiek glabāti krājumi un kur krājumi tiek izdoti no WMS I noliktavas.

Šī tēma attiecas uz moduļa Krājumu vadība līdzekļiem. Tā neattiecas uz moduļa Noliktavas pārvaldība līdzekļiem.

Termins novietojums attiecas uz vietu, kur tiek uzglabāti krājumi un no kurienes tie tiek ņemti.

Katrai atrašanās vietai var tikt norādīta arī krājuma ievietošanas vieta. Pēc noklusējuma tās ir vienādas. Krājumi parasti, bet ne vienmēr tiek ievietoti un ņemti no vienas un tās pašas atrašanās vietas. Piemēram, noliktavas statīvos uzglabāti krājumi tiek ņemti no vienas ailes un ievietoti citā. Galvenā ievade tiek noteikta pēc novietojuma nosaukuma, ko parasti nosaka tās koordinātas: noliktava, aile, statīvs, plaukts un nodalījums. Šo nosaukumu vai ID var ievadīt manuāli, vai tas var tikt ģenerēts no novietojuma koordinātām lapā Krājumu vietas, piemēram, 01-02-03-4 novietojumam 1. ailē, 2. statīvā, 3. plauktā, 4. nodalījumā.
Atrašanās vietas rekvizīti

Atrašanās vietai ir šādi rekvizīti:
-   Izmērs (augstums, platums, dziļums un tilpums)
-   Noliktava un ailes, statīva, plaukta un nodalījuma pozīcija
-   Novietojuma tips (uzkrāšanas vieta, izdošanas vietu, saņemšanas doks, izdošanas doks, ražošanas ievades vieta, pārbaudes veikšanas vieta vai Kanban lielveikals)

Tiešsaistes sistēmās var lietot kontroltekstu, lai pārliecinātos, ka operators ir atlasījis pareizo noteikta krājuma novietojumu. Kontroltekstu var izveidot manuāli vai pēc noklusējuma.

## <a name="sort-codes"></a>Kārtošanas kodi
Lietojiet kārtošanas kodus, lai optimizētu izdošanas rindu apstrādi, jo tie sniedz aprakstu par krājumu izdošanu, tostarp, par izdošanas pasūtījumu. Kārtošanas kodi var tikt norādīti pēc ailes un citām koordinātēm vai arī tikt piešķirti novietojumam manuāli.

## <a name="blocked-locations"></a>Bloķētas atrašanās vietas
Dažreiz var būt vajadzīgs norādīt, ka novietojums ir aizturēts uz noteiktu laika periodu, piemēram, lai veiktu remontu. Šādā gadījumā ir ieteicams norādīt tikai ieejas vai izejas plūsmas aizturēšanu.

## <a name="tree-structure"></a>Aplikācijas objektu koka struktūra

Lapā Krājumu vietas varat definēta attēlojuma formātā skatīt noliktavas izkārtojuma koka struktūru, kuras pamatā ir krājumu vietu koordinātes.

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a>Krājumu vietu uzturēšana, izmantojot noliktavas veidlapu

Varat kopēt novietojumus no vienas noliktavas uz citu, kā arī izveidot novietojumus, izmantojot vedni. Pirms vedņa palaišanas pārliecinieties, ka esat definējis noklusējuma novietojumu nosaukumus lapā Noliktava.



<a name="see-also"></a>Skatiet arī
--------

[Jauna noliktavas izkārtojuma izveide (uzdevuma ceļvedis)](/dynamics365/unified-operations/supply-chain/inventory/tasks/create-new-warehouse-layout)

