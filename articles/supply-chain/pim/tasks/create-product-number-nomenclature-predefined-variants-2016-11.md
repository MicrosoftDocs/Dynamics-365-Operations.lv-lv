---
title: Preces numuru nomenklatūras izveide iepriekš definētiem preces variantiem
description: Šajā ceļvedī parādīts, kā iestatīt preces numura nomenklatūru iepriekš definētiem preču variantiem, un kā to var piesaistīt attiecīgai preces dimensijas grupai.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 6a2e61fd99cb80a1a9cc3d8e985fb0f14e3c2fc2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844685"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="ccb15-103">Preces numuru nomenklatūras izveide iepriekš definētiem preces variantiem</span><span class="sxs-lookup"><span data-stu-id="ccb15-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ccb15-104">Šajā ceļvedī parādīts, kā iestatīt preces numura nomenklatūru iepriekš definētiem preču variantiem, un kā to var piesaistīt attiecīgai preces dimensijas grupai.</span><span class="sxs-lookup"><span data-stu-id="ccb15-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="ccb15-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="ccb15-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ccb15-106">Jauna preces numura nomenklatūra tiek piešķirta Krāsas un Izmēra preces dimensiju grupai.</span><span class="sxs-lookup"><span data-stu-id="ccb15-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="ccb15-107">Šo uzdevumu parasti veic preces noformētājs.</span><span class="sxs-lookup"><span data-stu-id="ccb15-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="ccb15-108">Izveidot preces numura nomenklatūru</span><span class="sxs-lookup"><span data-stu-id="ccb15-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="ccb15-109">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="ccb15-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ccb15-110">Noklikšķiniet uz Preču nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="ccb15-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="ccb15-111">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="ccb15-111">Click New.</span></span>
4. <span data-ttu-id="ccb15-112">Laukā Nosaukums ievadiet nomenklatūras nosaukumu, kuru apzīmējumi palīdz identificēt mērķa preces dimensiju grupu, piemēram, ColorSize.</span><span class="sxs-lookup"><span data-stu-id="ccb15-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="ccb15-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ccb15-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="ccb15-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ccb15-114">Click Add.</span></span>
7. <span data-ttu-id="ccb15-115">Noklikšķiniet uz Preces šablona numurs.</span><span class="sxs-lookup"><span data-stu-id="ccb15-115">Click Product master number.</span></span>
8. <span data-ttu-id="ccb15-116">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ccb15-116">Click Add.</span></span>
9. <span data-ttu-id="ccb15-117">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="ccb15-117">Click Text constant.</span></span>
10. <span data-ttu-id="ccb15-118">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="ccb15-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="ccb15-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ccb15-119">Click Add.</span></span>
12. <span data-ttu-id="ccb15-120">Noklikšķiniet uz Krāsa.</span><span class="sxs-lookup"><span data-stu-id="ccb15-120">Click Color.</span></span>
13. <span data-ttu-id="ccb15-121">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ccb15-121">Click Add.</span></span>
14. <span data-ttu-id="ccb15-122">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="ccb15-122">Click Text constant.</span></span>
15. <span data-ttu-id="ccb15-123">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="ccb15-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="ccb15-124">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ccb15-124">Click Add.</span></span>
17. <span data-ttu-id="ccb15-125">Noklikšķiniet uz Izmērs.</span><span class="sxs-lookup"><span data-stu-id="ccb15-125">Click Size.</span></span>
18. <span data-ttu-id="ccb15-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ccb15-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="ccb15-127">Piešķirt nomenklatūru preces šablonam</span><span class="sxs-lookup"><span data-stu-id="ccb15-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="ccb15-128">Noklikšķiniet uz Preces dimensiju grupas.</span><span class="sxs-lookup"><span data-stu-id="ccb15-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="ccb15-129">Atlasiet SizeCol preces dimensiju grupu.</span><span class="sxs-lookup"><span data-stu-id="ccb15-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="ccb15-130">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="ccb15-130">Click Edit.</span></span>
4. <span data-ttu-id="ccb15-131">Atlasiet Jā laukā Izmantot nomenklatūru.</span><span class="sxs-lookup"><span data-stu-id="ccb15-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="ccb15-132">Laukā Preces varianta numura nomenklatūra ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ccb15-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="ccb15-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ccb15-133">Close the page.</span></span>

