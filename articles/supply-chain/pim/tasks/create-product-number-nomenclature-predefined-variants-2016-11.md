---
title: Preces numuru nomenklatūras izveide iepriekš definētiem preces variantiem
description: Šajā tēmā izskaidrots, kā iestatīt produkta numura nomenklatūru iepriekš definētiem produkta variantiem un kā to piešķirt attiecīgajai produkta izmēru grupai.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920661"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="a4946-103">Preces numuru nomenklatūras izveide iepriekš definētiem preces variantiem</span><span class="sxs-lookup"><span data-stu-id="a4946-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4946-104">Šajā tēmā izskaidrots, kā iestatīt produkta numura nomenklatūru iepriekš definētiem produkta variantiem un kā to piešķirt attiecīgajai produkta izmēru grupai.</span><span class="sxs-lookup"><span data-stu-id="a4946-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="a4946-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="a4946-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a4946-106">Jauna preces numura nomenklatūra tiek piešķirta Krāsas un Izmēra preces dimensiju grupai.</span><span class="sxs-lookup"><span data-stu-id="a4946-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="a4946-107">Šo uzdevumu parasti veic preces noformētājs.</span><span class="sxs-lookup"><span data-stu-id="a4946-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="a4946-108">Izveidot preces numura nomenklatūru</span><span class="sxs-lookup"><span data-stu-id="a4946-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="a4946-109">Dodieties uz **Preču informācijas pārvaldība \> Iestātījums \> Produktu nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="a4946-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="a4946-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="a4946-110">Select **New**.</span></span>
1. <span data-ttu-id="a4946-111">Laukā **Nosaukums** ievadiet nomenklatūras nosaukumu, kas palīdz identificēt mērķa produkta izmēru grupu, piemēram, `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="a4946-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="a4946-112">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a4946-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="a4946-113">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="a4946-113">Select **Add**.</span></span>
1. <span data-ttu-id="a4946-114">Atlasiet **Galvenā produkta** numuru.</span><span class="sxs-lookup"><span data-stu-id="a4946-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="a4946-115">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="a4946-115">Select **Add**.</span></span>
1. <span data-ttu-id="a4946-116">Atlasiet **Pastāvīgais teksts**.</span><span class="sxs-lookup"><span data-stu-id="a4946-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="a4946-117">Laukā **Teksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a4946-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="a4946-118">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="a4946-118">Select **Add**.</span></span>
1. <span data-ttu-id="a4946-119">Atlasiet **Krāsa**.</span><span class="sxs-lookup"><span data-stu-id="a4946-119">Select **Color**.</span></span>
1. <span data-ttu-id="a4946-120">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="a4946-120">Select **Add**.</span></span>
1. <span data-ttu-id="a4946-121">Atlasiet **Pastāvīgais teksts**.</span><span class="sxs-lookup"><span data-stu-id="a4946-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="a4946-122">Laukā **Teksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a4946-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="a4946-123">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="a4946-123">Select **Add**.</span></span>
1. <span data-ttu-id="a4946-124">Atlasiet **Izmērs**.</span><span class="sxs-lookup"><span data-stu-id="a4946-124">Select **Size**.</span></span>
1. <span data-ttu-id="a4946-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a4946-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="a4946-126">Piešķirt nomenklatūru preces šablonam</span><span class="sxs-lookup"><span data-stu-id="a4946-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="a4946-127">Atlasiet **Produkta izmēru grupas**.</span><span class="sxs-lookup"><span data-stu-id="a4946-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="a4946-128">Atlasiet grupu **Izmēra-krāsas produkta izmērs**.</span><span class="sxs-lookup"><span data-stu-id="a4946-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="a4946-129">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="a4946-129">Select **Edit**.</span></span>
4. <span data-ttu-id="a4946-130">Atlasiet **Jā** laukā **Izmantot nomenklatūru**.</span><span class="sxs-lookup"><span data-stu-id="a4946-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="a4946-131">Ievadiet vai atlasiet vērtību laukā **Produkta varianta numura nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="a4946-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="a4946-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a4946-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]