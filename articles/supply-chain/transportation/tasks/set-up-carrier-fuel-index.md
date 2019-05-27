---
title: Pārvadātāja degvielas rādītāja iestatīšana
description: Šajā ceļvedī parādīts, kā izveidot degvielas rādītāja reģionu, degvielas rādītāju un pārvadātāja degvielas rādītāju.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6f72de7ad54a2b2dc1bf40fd8cb86d8b055e2d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552096"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="8cf10-103">Pārvadātāja degvielas rādītāja iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8cf10-103">Set up a carrier fuel index</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8cf10-104">Šajā ceļvedī parādīts, kā izveidot degvielas rādītāja reģionu, degvielas rādītāju un pārvadātāja degvielas rādītāju.</span><span class="sxs-lookup"><span data-stu-id="8cf10-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="8cf10-105">Degvielas rādītāja reģions norāda, uz kuru reģionu degvielas rādītājs attiecas, un degvielas rādītājs norāda degvielas cenu noteiktā laika periodā.</span><span class="sxs-lookup"><span data-stu-id="8cf10-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="8cf10-106">Lai atspoguļotu degvielas cenu izmaiņas laika gaitā, ar pārvadātāju varat saistīt vairākus degvielas rādītājus.</span><span class="sxs-lookup"><span data-stu-id="8cf10-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="8cf10-107">Šos uzdevumus parasti veic transportēšanas koordinators.</span><span class="sxs-lookup"><span data-stu-id="8cf10-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="8cf10-108">Šo procedūru varat lietot demonstrācijas datu uzņēmumā USMF vai savos datos.</span><span class="sxs-lookup"><span data-stu-id="8cf10-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="8cf10-109">Degvielas rādītāja reģiona izveide</span><span class="sxs-lookup"><span data-stu-id="8cf10-109">Create a fuel index region</span></span>
1. <span data-ttu-id="8cf10-110">Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Degvielas rādītāji > Degvielas rādītāju reģioni.</span><span class="sxs-lookup"><span data-stu-id="8cf10-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="8cf10-111">Vispirms ir jāizveido dažādi reģioni, kuros darbojas jūsu uzņēmums un tiek aprēķinātas citas degvielas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="8cf10-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="8cf10-112">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8cf10-112">Click New.</span></span>
3. <span data-ttu-id="8cf10-113">Ierakstiet vērtību laukā Reģions.</span><span class="sxs-lookup"><span data-stu-id="8cf10-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="8cf10-114">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8cf10-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="8cf10-115">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8cf10-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="8cf10-116">Degvielas rādītāja izveide</span><span class="sxs-lookup"><span data-stu-id="8cf10-116">Create a fuel index</span></span>
1. <span data-ttu-id="8cf10-117">Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Degvielas rādītāji > Degvielas rādītāji.</span><span class="sxs-lookup"><span data-stu-id="8cf10-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="8cf10-118">Iestatītajiem reģioniem ir jāievada pašreizējās degvielas cenas.</span><span class="sxs-lookup"><span data-stu-id="8cf10-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="8cf10-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8cf10-119">Click New.</span></span>
3. <span data-ttu-id="8cf10-120">Laukā Reģions noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8cf10-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8cf10-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8cf10-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="8cf10-122">Ievadiet skaitli laukā Cena par galonu.</span><span class="sxs-lookup"><span data-stu-id="8cf10-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="8cf10-123">Laukā Spēkā stāšanās datums un laiks ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="8cf10-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="8cf10-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8cf10-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="8cf10-125">Pārvadātāja degvielas rādītāja izveide</span><span class="sxs-lookup"><span data-stu-id="8cf10-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="8cf10-126">Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Degvielas rādītāji > Pārvadātāju degvielas rādītāji.</span><span class="sxs-lookup"><span data-stu-id="8cf10-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="8cf10-127">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8cf10-127">Click New.</span></span>
3. <span data-ttu-id="8cf10-128">Ierakstiet vērtību laukā Pārvadātāja degvielas rādītājs.</span><span class="sxs-lookup"><span data-stu-id="8cf10-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="8cf10-129">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8cf10-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8cf10-130">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="8cf10-130">Click New.</span></span>
6. <span data-ttu-id="8cf10-131">Laukā Spēkā stāšanās datums un laiks ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="8cf10-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="8cf10-132">Ievadiet skaitli laukā CPG No.</span><span class="sxs-lookup"><span data-stu-id="8cf10-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="8cf10-133">Šajā piemērā varat iestatīt CPG No laukā vērtību 1,95.</span><span class="sxs-lookup"><span data-stu-id="8cf10-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="8cf10-134">Ievadiet skaitli laukā CPG Līdz.</span><span class="sxs-lookup"><span data-stu-id="8cf10-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="8cf10-135">Šajā piemērā varat iestatīt CPG Uz laukā vērtību 2.</span><span class="sxs-lookup"><span data-stu-id="8cf10-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="8cf10-136">Ievadiet skaitli laukā Procenti.</span><span class="sxs-lookup"><span data-stu-id="8cf10-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="8cf10-137">Šajā piemērā varat iestatīt procentu vērtību 3.</span><span class="sxs-lookup"><span data-stu-id="8cf10-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="8cf10-138">Laukā Valūta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8cf10-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="8cf10-139">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8cf10-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="8cf10-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8cf10-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="8cf10-141">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8cf10-141">Click Save.</span></span>

