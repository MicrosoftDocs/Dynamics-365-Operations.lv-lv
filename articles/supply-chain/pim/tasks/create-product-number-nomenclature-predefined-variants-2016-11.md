--- 
title: "Preces numura izveide iepriekš definētiem preces variantiem"
description: "Šajā ceļvedī parādīts, kā iestatīt preces numura nomenklatūru iepriekš definētiem preču variantiem, un kā to var piesaistīt attiecīgai preces dimensijas grupai."
author: ShylaThompson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 7881701385c802578e5e5c412951a1507efa5acf
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-product-number-for-predefined-product-variants"></a><span data-ttu-id="35be2-103">Preces numura izveide iepriekš definētiem preces variantiem</span><span class="sxs-lookup"><span data-stu-id="35be2-103">Create a product number for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35be2-104">Šajā ceļvedī parādīts, kā iestatīt preces numura nomenklatūru iepriekš definētiem preču variantiem, un kā to var piesaistīt attiecīgai preces dimensijas grupai.</span><span class="sxs-lookup"><span data-stu-id="35be2-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="35be2-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="35be2-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="35be2-106">Jauna preces numura nomenklatūra tiek piešķirta Krāsas un Izmēra preces dimensiju grupai.</span><span class="sxs-lookup"><span data-stu-id="35be2-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="35be2-107">Šo uzdevumu parasti veic preces noformētājs.</span><span class="sxs-lookup"><span data-stu-id="35be2-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="35be2-108">Izveidot preces numura nomenklatūru</span><span class="sxs-lookup"><span data-stu-id="35be2-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="35be2-109">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="35be2-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="35be2-110">Noklikšķiniet uz Preču nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="35be2-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="35be2-111">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="35be2-111">Click New.</span></span>
4. <span data-ttu-id="35be2-112">Laukā Nosaukums ievadiet nomenklatūras nosaukumu, kuru apzīmējumi palīdz identificēt mērķa preces dimensiju grupu, piemēram, ColorSize.</span><span class="sxs-lookup"><span data-stu-id="35be2-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize.</span></span>
5. <span data-ttu-id="35be2-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="35be2-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="35be2-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="35be2-114">Click Add.</span></span>
7. <span data-ttu-id="35be2-115">Noklikšķiniet uz Preces šablona numurs.</span><span class="sxs-lookup"><span data-stu-id="35be2-115">Click Product master number.</span></span>
8. <span data-ttu-id="35be2-116">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="35be2-116">Click Add.</span></span>
9. <span data-ttu-id="35be2-117">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="35be2-117">Click Text constant.</span></span>
10. <span data-ttu-id="35be2-118">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="35be2-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="35be2-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="35be2-119">Click Add.</span></span>
12. <span data-ttu-id="35be2-120">Noklikšķiniet uz Krāsa.</span><span class="sxs-lookup"><span data-stu-id="35be2-120">Click Color.</span></span>
13. <span data-ttu-id="35be2-121">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="35be2-121">Click Add.</span></span>
14. <span data-ttu-id="35be2-122">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="35be2-122">Click Text constant.</span></span>
15. <span data-ttu-id="35be2-123">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="35be2-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="35be2-124">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="35be2-124">Click Add.</span></span>
17. <span data-ttu-id="35be2-125">Noklikšķiniet uz Izmērs.</span><span class="sxs-lookup"><span data-stu-id="35be2-125">Click Size.</span></span>
18. <span data-ttu-id="35be2-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="35be2-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="35be2-127">Piešķirt nomenklatūru preces šablonam</span><span class="sxs-lookup"><span data-stu-id="35be2-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="35be2-128">Noklikšķiniet uz Preces dimensiju grupas.</span><span class="sxs-lookup"><span data-stu-id="35be2-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="35be2-129">Atlasiet SizeCol preces dimensiju grupu.</span><span class="sxs-lookup"><span data-stu-id="35be2-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="35be2-130">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="35be2-130">Click Edit.</span></span>
4. <span data-ttu-id="35be2-131">Atlasiet Jā laukā Izmantot nomenklatūru.</span><span class="sxs-lookup"><span data-stu-id="35be2-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="35be2-132">Laukā Preces varianta numura nomenklatūra ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="35be2-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="35be2-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="35be2-133">Close the page.</span></span>


