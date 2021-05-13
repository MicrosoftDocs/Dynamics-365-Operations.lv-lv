---
title: Iekšējie līdzekļi apkalpošanai
description: Šajā tēmā ir aprakstīts, kā var izmantot Microsoft Dynamics 365 Field Service gan debitoru, gan pamatlīdzekļu pakalpojumiem.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941418"
---
# <a name="in-house-assets-for-servicing"></a>Iekšējie līdzekļi apkalpošanai

[!include [banner](../../includes/banner.md)]



Programma Microsoft Dynamics 365 Field Service ir izstrādāta, lai apkalpotu klientu līdzekļus. Līdzekļu pārvaldība Dynamics 365 Supply Chain Management ir paredzēta, lai uzturētu iekšējos līdzekļus. Šo divu programmu integrēšana ļauj izmantot Field Service, lai apkalpotu gan klientu līdzekļus, gan iekšējos līdzekļus. Jūs varat arī klasificēt pamatlīdzekļus, pamatojoties uz funkcionālo novietojumu vai hierarhiju, un izsekot apkalpošanu detalizētā līmenī.

Papildinformāciju skatiet šeit [Integrēt Dynamics 365 Field Service un Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Veidnes

Iekšējie pamatlīdzekļi ietver pamata finanšu tabulas karšu vākšanu, kas darbojas kopā datu mijiedarbības laikā, kā redzams nākamajā tabulā.

| Finance and Operations programmas | Modeļa vadītas programmas programmā Dynamics 365 | apraksts |
|-----------------------------|-----------------------------------|-------------|
| Līdzekļu pārvaldība līdzeklis dzīves cikla modeļi | msdyn\_assetlifecyclemodels | |
| Līdzekļu pārvaldība līdzeklis dzīves cikla stāvokļi | msdyn\_assetlifecyclestates | |
| Līdzekļu pārvaldības līdzekļi | msdyn\_customerassets | |
| Līdzekļu pārvaldība līdzekļu veidi | msdyn\_customerassetcategories | |
| Līdzekļu pārvaldība funkcionālie novietojumi dzīves cikla modeļi | msdyn\_functionallocationlifecyclemodels | |
| Līdzekļu pārvaldība funkcionālais novietojums dzīves cikla stāvokļi | msdyn\_functionallocationlifecyclestates | |
| Līdzekļu pārvaldība funkcionālie novietojumi | msdyn\_functionallocations | |
| Līdzekļu pārvaldība funkcionālie novietojumu veidi | msdyn\_functionallocationtypes | |
| Līdzekļu pārvaldība ražotāji | msdyn\_manufacturers | |
| Līdzekļu pārvaldības modeļi | msdyn\_models | |
| Līdzekļu pārvaldības garantija | msdyn\_warranties | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]