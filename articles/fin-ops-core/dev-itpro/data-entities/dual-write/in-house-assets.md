---
title: Iekšējie pamatlīdzekļi apkopei
description: Šajā tēmā aprakstīts, kā varat izmantot Microsoft Dtnamics 365 Field Service, lai apkalpotu gan klientu līdzekļus, gan iekšējos līdzekļus.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 0e87a3d645c19fab3bb0560ba5114d193e2d0be7
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997174"
---
# <a name="in-house-assets-for-servicing"></a>Iekšējie pamatlīdzekļi apkopei

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service ir izstrādāta, lai apkalpotu klientu līdzekļus. Līdzekļu pārvaldība Dynamics 365 Supply Chain Management ir paredzēta, lai uzturētu iekšējos līdzekļus. Šo divu programmu integrēšana ļauj izmantot Field Service, lai apkalpotu gan klientu līdzekļus, gan iekšējos līdzekļus. Jūs varat arī klasificēt pamatlīdzekļus, pamatojoties uz funkcionālo novietojumu vai hierarhiju, un izsekot apkalpošanu detalizētā līmenī.

Papildinformāciju skatiet šeit [Integrēt Dynamics 365 Field Service un Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Veidnes

Iekšējie pamatlīdzekļi ietver pamata finanšu elementa karšu vākšanu, kas darbojas kopā datu mijiedarbības laikā, kā redzams nākamajā tabulā.

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
