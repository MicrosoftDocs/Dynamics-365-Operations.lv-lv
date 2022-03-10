---
title: Novērtējiet visas vairāku SKU atrašanās vietas direktīvu darbības
description: Ir pievienots jauns līdzeklis, lai novērtētu visas darbības vairāku SKU atrašanās vietu direktīvām. Šajā lapā sniegti norādījumi par to, kā to iespējot.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2d5f7cf548eb6c18d9700c73ef084f197b78542e
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102967"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Vairāku SKU opcija neizvērtē vairāku atrašanās vietu direktīvu darbības

## <a name="symptoms"></a>Simptomi

*Pārdošanas pasūtījuma* darba pasūtījuma veida un *Izvietošanas* darba veida novietojuma direktīvas nenovērtē vairākas novietojuma direktīvas, kad ir atlasīta opcija. **Vairāki SKU**. Tiek novērtēta tikai pirmā novietojuma direktīvas darbība.

## <a name="resolution"></a>Novēršana

Versijā 10.0.15 ir pievienots jauns līdzeklis *Novērtēt visas darbības vairāku SKU novietojuma direktīvām* (skatiet [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Šis līdzeklis novērtē visas darbības vairāku SKU novietojuma direktīvām. No Piegādes ķēdes pārvaldības versijas 10.0.21 šī funkcija ir ieslēgta pēc noklusējuma.  Tāpat kā Piegādes ķēdes pārvaldībai 10.0.25 šī funkcija ir obligāta un to nevar izslēgt. Administratori var izmantot Līdzekļu [pārvaldības lapu](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai pārbaudītu līdzekļu statusu un aktivizētu vai atspējotu to, ja nepieciešams.
