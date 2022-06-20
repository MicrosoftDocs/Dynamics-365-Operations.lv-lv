---
title: Iekšējie līdzekļi apkalpošanai
description: Šajā rakstā ir aprakstīts, kā var Microsoft Dynamics 365 Field Service izmantot gan debitoru, gan pamatlīdzekļu pakalpojumiem.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: c946af11737a77c4dadd824893e6cc1e4c77b587
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858627"
---
# <a name="in-house-assets-for-servicing"></a>Iekšējie līdzekļi apkalpošanai

[!include [banner](../../includes/banner.md)]

Programma Microsoft Dynamics 365 Field Service ir izstrādāta, lai apkalpotu klientu līdzekļus. Līdzekļu pārvaldība Dynamics 365 Supply Chain Management ir paredzēta, lai uzturētu iekšējos līdzekļus. Šo divu programmu integrēšana ļauj izmantot Field Service, lai apkalpotu gan klientu līdzekļus, gan iekšējos līdzekļus. Jūs varat arī klasificēt pamatlīdzekļus, pamatojoties uz funkcionālo novietojumu vai hierarhiju, un izsekot apkalpošanu detalizētā līmenī.

Papildinformāciju skatiet šeit [Integrēt Dynamics 365 Field Service un Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Veidnes

Iekšējie pamatlīdzekļi ietver pamata finanšu tabulas karšu vākšanu, kas darbojas kopā datu mijiedarbības laikā, kā redzams nākamajā tabulā.

| Finance and Operations programmas | Customer engagement programmas | Apraksts |
|-----------------------------|-----------------------------------|-------------|
[Līdzekļu pārvaldība līdzeklis dzīves cikla modeļi](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[Līdzekļu pārvaldība līdzeklis dzīves cikla stāvokļi](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[Līdzekļu pārvaldība līdzekļu veidi](mapping-reference.md#124) | msdyn_customerassetcategories | |
[Līdzekļu pārvaldības līdzekļi](mapping-reference.md#125) | msdyn_customerassets | |
[Līdzekļu pārvaldība funkcionālie novietojumi dzīves cikla modeļi](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[Līdzekļu pārvaldība funkcionālais novietojums dzīves cikla stāvokļi](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[Līdzekļu pārvaldība funkcionālie novietojumu veidi](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[Līdzekļu pārvaldība funkcionālie novietojumi](mapping-reference.md#136) | msdyn_functionallocations | |
[Līdzekļu pārvaldība ražotāji](mapping-reference.md#153) | msdyn_manufacturers | |
[Līdzekļu pārvaldības modeļi](mapping-reference.md#154) | msdyn_models | |
[Līdzekļu pārvaldības garantija](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
