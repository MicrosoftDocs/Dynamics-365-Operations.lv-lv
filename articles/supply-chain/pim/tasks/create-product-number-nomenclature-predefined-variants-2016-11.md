---
title: Preces numuru nomenklatūras izveide iepriekš definētiem preces variantiem
description: Šajā tēmā izskaidrots, kā iestatīt produkta numura nomenklatūru iepriekš definētiem produkta variantiem un kā to piešķirt attiecīgajai produkta izmēru grupai.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5cf0efeac2851e6ead6fc5e15a016370dfa620bc
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914911"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="1b1b7-103">Preces numuru nomenklatūras izveide iepriekš definētiem preces variantiem</span><span class="sxs-lookup"><span data-stu-id="1b1b7-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1b1b7-104">Šajā tēmā izskaidrots, kā iestatīt produkta numura nomenklatūru iepriekš definētiem produkta variantiem un kā to piešķirt attiecīgajai produkta izmēru grupai.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="1b1b7-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1b1b7-106">Jauna preces numura nomenklatūra tiek piešķirta Krāsas un Izmēra preces dimensiju grupai.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="1b1b7-107">Šo uzdevumu parasti veic preces noformētājs.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="1b1b7-108">Izveidot preces numura nomenklatūru</span><span class="sxs-lookup"><span data-stu-id="1b1b7-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="1b1b7-109">Atlasiet **Produkta varianta modeļa definīcija**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="1b1b7-110">Atlasiet **Produkta nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="1b1b7-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-111">Select **New**.</span></span>
4. <span data-ttu-id="1b1b7-112">Laukā **Nosaukums** ievadiet nomenklatūras nosaukumu, kas palīdz identificēt mērķa produkta izmēru grupu, piemēram, `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="1b1b7-113">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="1b1b7-114">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-114">Select **Add**.</span></span>
7. <span data-ttu-id="1b1b7-115">Atlasiet **Galvenā produkta** numuru.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="1b1b7-116">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-116">Select **Add**.</span></span>
9. <span data-ttu-id="1b1b7-117">Atlasiet **Pastāvīgais teksts**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="1b1b7-118">Laukā **Teksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="1b1b7-119">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-119">Select **Add**.</span></span>
12. <span data-ttu-id="1b1b7-120">Atlasiet **Krāsa**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-120">Select **Color**.</span></span>
13. <span data-ttu-id="1b1b7-121">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-121">Select **Add**.</span></span>
14. <span data-ttu-id="1b1b7-122">Atlasiet **Pastāvīgais teksts**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="1b1b7-123">Laukā **Teksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="1b1b7-124">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-124">Select **Add**.</span></span>
17. <span data-ttu-id="1b1b7-125">Atlasiet **Izmērs**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-125">Select **Size**.</span></span>
18. <span data-ttu-id="1b1b7-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="1b1b7-127">Piešķirt nomenklatūru preces šablonam</span><span class="sxs-lookup"><span data-stu-id="1b1b7-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="1b1b7-128">Atlasiet **Produkta izmēru grupas**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="1b1b7-129">Atlasiet grupu **Izmēra-krāsas produkta izmērs**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="1b1b7-130">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-130">Select **Edit**.</span></span>
4. <span data-ttu-id="1b1b7-131">Atlasiet **Jā** laukā **Izmantot nomenklatūru**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="1b1b7-132">Ievadiet vai atlasiet vērtību laukā **Produkta varianta numura nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="1b1b7-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-133">Close the page.</span></span>

