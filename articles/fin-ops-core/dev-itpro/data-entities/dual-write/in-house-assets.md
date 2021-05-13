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
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="9a979-103">Iekšējie līdzekļi apkalpošanai</span><span class="sxs-lookup"><span data-stu-id="9a979-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="9a979-104">Programma Microsoft Dynamics 365 Field Service ir izstrādāta, lai apkalpotu klientu līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="9a979-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="9a979-105">Līdzekļu pārvaldība Dynamics 365 Supply Chain Management ir paredzēta, lai uzturētu iekšējos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="9a979-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="9a979-106">Šo divu programmu integrēšana ļauj izmantot Field Service, lai apkalpotu gan klientu līdzekļus, gan iekšējos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="9a979-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="9a979-107">Jūs varat arī klasificēt pamatlīdzekļus, pamatojoties uz funkcionālo novietojumu vai hierarhiju, un izsekot apkalpošanu detalizētā līmenī.</span><span class="sxs-lookup"><span data-stu-id="9a979-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="9a979-108">Papildinformāciju skatiet šeit [Integrēt Dynamics 365 Field Service un Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="9a979-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="9a979-109">Veidnes</span><span class="sxs-lookup"><span data-stu-id="9a979-109">Templates</span></span>

<span data-ttu-id="9a979-110">Iekšējie pamatlīdzekļi ietver pamata finanšu tabulas karšu vākšanu, kas darbojas kopā datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="9a979-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="9a979-111">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="9a979-111">Finance and Operations apps</span></span> | <span data-ttu-id="9a979-112">Modeļa vadītas programmas programmā Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9a979-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="9a979-113">apraksts</span><span class="sxs-lookup"><span data-stu-id="9a979-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="9a979-114">Līdzekļu pārvaldība līdzeklis dzīves cikla modeļi</span><span class="sxs-lookup"><span data-stu-id="9a979-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="9a979-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="9a979-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="9a979-116">Līdzekļu pārvaldība līdzeklis dzīves cikla stāvokļi</span><span class="sxs-lookup"><span data-stu-id="9a979-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="9a979-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="9a979-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="9a979-118">Līdzekļu pārvaldības līdzekļi</span><span class="sxs-lookup"><span data-stu-id="9a979-118">Asset management assets</span></span> | <span data-ttu-id="9a979-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="9a979-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="9a979-120">Līdzekļu pārvaldība līdzekļu veidi</span><span class="sxs-lookup"><span data-stu-id="9a979-120">Asset management asset types</span></span> | <span data-ttu-id="9a979-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="9a979-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="9a979-122">Līdzekļu pārvaldība funkcionālie novietojumi dzīves cikla modeļi</span><span class="sxs-lookup"><span data-stu-id="9a979-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="9a979-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="9a979-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="9a979-124">Līdzekļu pārvaldība funkcionālais novietojums dzīves cikla stāvokļi</span><span class="sxs-lookup"><span data-stu-id="9a979-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="9a979-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="9a979-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="9a979-126">Līdzekļu pārvaldība funkcionālie novietojumi</span><span class="sxs-lookup"><span data-stu-id="9a979-126">Asset management functional locations</span></span> | <span data-ttu-id="9a979-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="9a979-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="9a979-128">Līdzekļu pārvaldība funkcionālie novietojumu veidi</span><span class="sxs-lookup"><span data-stu-id="9a979-128">Asset management functional location types</span></span> | <span data-ttu-id="9a979-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="9a979-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="9a979-130">Līdzekļu pārvaldība ražotāji</span><span class="sxs-lookup"><span data-stu-id="9a979-130">Asset management manufacturers</span></span> | <span data-ttu-id="9a979-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="9a979-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="9a979-132">Līdzekļu pārvaldības modeļi</span><span class="sxs-lookup"><span data-stu-id="9a979-132">Asset management models</span></span> | <span data-ttu-id="9a979-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="9a979-133">msdyn\_models</span></span> | |
| <span data-ttu-id="9a979-134">Līdzekļu pārvaldības garantija</span><span class="sxs-lookup"><span data-stu-id="9a979-134">Asset management warranty</span></span> | <span data-ttu-id="9a979-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="9a979-135">msdyn\_warranties</span></span> | |

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