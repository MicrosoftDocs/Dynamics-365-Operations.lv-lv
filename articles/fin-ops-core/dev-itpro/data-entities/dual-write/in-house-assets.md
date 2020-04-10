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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 1e423199d0639db5e403e280880036b590149095
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172950"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="64ab5-103">Iekšējie pamatlīdzekļi apkopei</span><span class="sxs-lookup"><span data-stu-id="64ab5-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="64ab5-104">Microsoft Dynamics 365 Field Service ir izstrādāta, lai apkalpotu klientu līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="64ab5-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="64ab5-105">Līdzekļu pārvaldība Dynamics 365 Supply Chain Management ir paredzēta, lai uzturētu iekšējos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="64ab5-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="64ab5-106">Šo divu programmu integrēšana ļauj izmantot Field Service, lai apkalpotu gan klientu līdzekļus, gan iekšējos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="64ab5-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="64ab5-107">Jūs varat arī klasificēt pamatlīdzekļus, pamatojoties uz funkcionālo novietojumu vai hierarhiju, un izsekot apkalpošanu detalizētā līmenī.</span><span class="sxs-lookup"><span data-stu-id="64ab5-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="64ab5-108">Papildinformāciju skatiet šeit [Integrēt Dynamics 365 Field Service un Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="64ab5-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="64ab5-109">Veidnes</span><span class="sxs-lookup"><span data-stu-id="64ab5-109">Templates</span></span>

<span data-ttu-id="64ab5-110">Iekšējie pamatlīdzekļi ietver pamata finanšu elementa karšu vākšanu, kas darbojas kopā datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="64ab5-110">In-house-assets include a collection of core entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="64ab5-111">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="64ab5-111">Finance and Operations apps</span></span> | <span data-ttu-id="64ab5-112">Modeļa vadītas programmas programmā Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="64ab5-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="64ab5-113">apraksts</span><span class="sxs-lookup"><span data-stu-id="64ab5-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="64ab5-114">Līdzekļu pārvaldība līdzeklis dzīves cikla modeļi</span><span class="sxs-lookup"><span data-stu-id="64ab5-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="64ab5-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="64ab5-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="64ab5-116">Līdzekļu pārvaldība līdzeklis dzīves cikla stāvokļi</span><span class="sxs-lookup"><span data-stu-id="64ab5-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="64ab5-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="64ab5-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="64ab5-118">Līdzekļu pārvaldības līdzekļi</span><span class="sxs-lookup"><span data-stu-id="64ab5-118">Asset management assets</span></span> | <span data-ttu-id="64ab5-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="64ab5-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="64ab5-120">Līdzekļu pārvaldība līdzekļu veidi</span><span class="sxs-lookup"><span data-stu-id="64ab5-120">Asset management asset types</span></span> | <span data-ttu-id="64ab5-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="64ab5-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="64ab5-122">Līdzekļu pārvaldība funkcionālie novietojumi dzīves cikla modeļi</span><span class="sxs-lookup"><span data-stu-id="64ab5-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="64ab5-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="64ab5-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="64ab5-124">Līdzekļu pārvaldība funkcionālais novietojums dzīves cikla stāvokļi</span><span class="sxs-lookup"><span data-stu-id="64ab5-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="64ab5-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="64ab5-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="64ab5-126">Līdzekļu pārvaldība funkcionālie novietojumi</span><span class="sxs-lookup"><span data-stu-id="64ab5-126">Asset management functional locations</span></span> | <span data-ttu-id="64ab5-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="64ab5-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="64ab5-128">Līdzekļu pārvaldība funkcionālie novietojumu veidi</span><span class="sxs-lookup"><span data-stu-id="64ab5-128">Asset management functional location types</span></span> | <span data-ttu-id="64ab5-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="64ab5-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="64ab5-130">Līdzekļu pārvaldība ražotāji</span><span class="sxs-lookup"><span data-stu-id="64ab5-130">Asset management manufacturers</span></span> | <span data-ttu-id="64ab5-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="64ab5-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="64ab5-132">Līdzekļu pārvaldības modeļi</span><span class="sxs-lookup"><span data-stu-id="64ab5-132">Asset management models</span></span> | <span data-ttu-id="64ab5-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="64ab5-133">msdyn\_models</span></span> | |
| <span data-ttu-id="64ab5-134">Līdzekļu pārvaldības garantija</span><span class="sxs-lookup"><span data-stu-id="64ab5-134">Asset management warranty</span></span> | <span data-ttu-id="64ab5-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="64ab5-135">msdyn\_warranties</span></span> | |

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
