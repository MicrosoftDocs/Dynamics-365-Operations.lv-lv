---
title: Krājumu vietas
description: Krājumu atrašanās vietu dati tiek izmantoti kopā ar pamata noliktavu (WMS I), lai noteiktu, kur tiek glabāti krājumi un kur krājumi tiek izdoti no WMS I noliktavas.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd5ad086cadd2e49585614e7650bb7e30a4e7328
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888591"
---
# <a name="inventory-locations"></a>Krājumu vietas

[!include [banner](../includes/banner.md)]

Krājumu atrašanās vietu dati tiek izmantoti kopā ar pamata noliktavu (WMS I), lai noteiktu, kur tiek glabāti krājumi un kur krājumi tiek izdoti no WMS I noliktavas.

Šis raksts attiecas uz krājumu vadības moduļa funkcijām. Tā neattiecas uz moduļa Noliktavas pārvaldība līdzekļiem.

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



## <a name="additional-resources"></a>Papildu resursi

[Jauna noliktavas izkārtojuma izveide](tasks/create-new-warehouse-layout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]