--- 
title: "Preces numura izveide iepriekš definētiem preces variantiem"
description: "Šajā ceļvedī parādīts, kā iestatīt preces numura nomenklatūru iepriekš definētiem preču variantiem, un kā to var piesaistīt attiecīgai preces dimensijas grupai."
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6294e4608b31c37aa713e3a7a2028b409b5a8366
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a><span data-ttu-id="25767-103">Preces numura izveide iepriekš definētiem preces variantiem</span><span class="sxs-lookup"><span data-stu-id="25767-103">Create a product number for predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25767-104">Šajā ceļvedī parādīts, kā iestatīt preces numura nomenklatūru iepriekš definētiem preču variantiem, un kā to var piesaistīt attiecīgai preces dimensijas grupai.</span><span class="sxs-lookup"><span data-stu-id="25767-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="25767-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="25767-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="25767-106">Jauna preces numura nomenklatūra tiek piešķirta Krāsas un Izmēra preces dimensiju grupai.</span><span class="sxs-lookup"><span data-stu-id="25767-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="25767-107">Šo uzdevumu parasti veic preces noformētājs.</span><span class="sxs-lookup"><span data-stu-id="25767-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="25767-108">Izveidot preces numura nomenklatūru</span><span class="sxs-lookup"><span data-stu-id="25767-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="25767-109">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="25767-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="25767-110">Noklikšķiniet uz Preču nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="25767-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="25767-111">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="25767-111">Click New.</span></span>
4. <span data-ttu-id="25767-112">Laukā Nosaukums ievadiet nomenklatūras nosaukumu, kuru apzīmējumi palīdz identificēt mērķa preces dimensiju grupu, piemēram, ColorSize.</span><span class="sxs-lookup"><span data-stu-id="25767-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="25767-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="25767-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="25767-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="25767-114">Click Add.</span></span>
7. <span data-ttu-id="25767-115">Noklikšķiniet uz Preces šablona numurs.</span><span class="sxs-lookup"><span data-stu-id="25767-115">Click Product master number.</span></span>
8. <span data-ttu-id="25767-116">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="25767-116">Click Add.</span></span>
9. <span data-ttu-id="25767-117">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="25767-117">Click Text constant.</span></span>
10. <span data-ttu-id="25767-118">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="25767-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="25767-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="25767-119">Click Add.</span></span>
12. <span data-ttu-id="25767-120">Noklikšķiniet uz Krāsa.</span><span class="sxs-lookup"><span data-stu-id="25767-120">Click Color.</span></span>
13. <span data-ttu-id="25767-121">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="25767-121">Click Add.</span></span>
14. <span data-ttu-id="25767-122">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="25767-122">Click Text constant.</span></span>
15. <span data-ttu-id="25767-123">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="25767-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="25767-124">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="25767-124">Click Add.</span></span>
17. <span data-ttu-id="25767-125">Noklikšķiniet uz Izmērs.</span><span class="sxs-lookup"><span data-stu-id="25767-125">Click Size.</span></span>
18. <span data-ttu-id="25767-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="25767-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="25767-127">Piešķirt nomenklatūru preces šablonam</span><span class="sxs-lookup"><span data-stu-id="25767-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="25767-128">Noklikšķiniet uz Preces dimensiju grupas.</span><span class="sxs-lookup"><span data-stu-id="25767-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="25767-129">Atlasiet SizeCol preces dimensiju grupu.</span><span class="sxs-lookup"><span data-stu-id="25767-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="25767-130">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="25767-130">Click Edit.</span></span>
4. <span data-ttu-id="25767-131">Atlasiet Jā laukā Izmantot nomenklatūru.</span><span class="sxs-lookup"><span data-stu-id="25767-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="25767-132">Laukā Preces varianta numura nomenklatūra ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="25767-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="25767-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="25767-133">Close the page.</span></span>


