---
title: Preces numuru nomenklatūras izveide iepriekš definētiem preces variantiem
description: Šajā tēmā izskaidrots, kā iestatīt produkta numura nomenklatūru iepriekš definētiem produkta variantiem un kā to piešķirt attiecīgajai produkta izmēru grupai.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6871765a450295a3f308ec7e706f1b126071585f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986051"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="dcc75-103">Preces numuru nomenklatūras izveide iepriekš definētiem preces variantiem</span><span class="sxs-lookup"><span data-stu-id="dcc75-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dcc75-104">Šajā tēmā izskaidrots, kā iestatīt produkta numura nomenklatūru iepriekš definētiem produkta variantiem un kā to piešķirt attiecīgajai produkta izmēru grupai.</span><span class="sxs-lookup"><span data-stu-id="dcc75-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="dcc75-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="dcc75-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="dcc75-106">Jauna preces numura nomenklatūra tiek piešķirta Krāsas un Izmēra preces dimensiju grupai.</span><span class="sxs-lookup"><span data-stu-id="dcc75-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="dcc75-107">Šo uzdevumu parasti veic preces noformētājs.</span><span class="sxs-lookup"><span data-stu-id="dcc75-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="dcc75-108">Izveidot preces numura nomenklatūru</span><span class="sxs-lookup"><span data-stu-id="dcc75-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="dcc75-109">Atlasiet **Produkta varianta modeļa definīcija**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="dcc75-110">Atlasiet **Produkta nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="dcc75-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-111">Select **New**.</span></span>
4. <span data-ttu-id="dcc75-112">Laukā **Nosaukums** ievadiet nomenklatūras nosaukumu, kas palīdz identificēt mērķa produkta izmēru grupu, piemēram, `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="dcc75-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="dcc75-113">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="dcc75-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="dcc75-114">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-114">Select **Add**.</span></span>
7. <span data-ttu-id="dcc75-115">Atlasiet **Galvenā produkta** numuru.</span><span class="sxs-lookup"><span data-stu-id="dcc75-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="dcc75-116">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-116">Select **Add**.</span></span>
9. <span data-ttu-id="dcc75-117">Atlasiet **Pastāvīgais teksts**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="dcc75-118">Laukā **Teksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="dcc75-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="dcc75-119">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-119">Select **Add**.</span></span>
12. <span data-ttu-id="dcc75-120">Atlasiet **Krāsa**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-120">Select **Color**.</span></span>
13. <span data-ttu-id="dcc75-121">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-121">Select **Add**.</span></span>
14. <span data-ttu-id="dcc75-122">Atlasiet **Pastāvīgais teksts**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="dcc75-123">Laukā **Teksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="dcc75-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="dcc75-124">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-124">Select **Add**.</span></span>
17. <span data-ttu-id="dcc75-125">Atlasiet **Izmērs**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-125">Select **Size**.</span></span>
18. <span data-ttu-id="dcc75-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dcc75-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="dcc75-127">Piešķirt nomenklatūru preces šablonam</span><span class="sxs-lookup"><span data-stu-id="dcc75-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="dcc75-128">Atlasiet **Produkta izmēru grupas**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="dcc75-129">Atlasiet grupu **Izmēra-krāsas produkta izmērs**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="dcc75-130">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-130">Select **Edit**.</span></span>
4. <span data-ttu-id="dcc75-131">Atlasiet **Jā** laukā **Izmantot nomenklatūru**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="dcc75-132">Ievadiet vai atlasiet vērtību laukā **Produkta varianta numura nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="dcc75-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="dcc75-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dcc75-133">Close the page.</span></span>

