---
title: Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei
description: Izmantojiet šo procedūru, lai izveidotu un piešķirtu izmaksu sadalījuma politiku un atbilstošas kārtulas izmaksu vadības ierīcei.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f0422a9aaf95184b556293bf6ebcaf4dcfb5b59
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841397"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="f93aa-103">Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei</span><span class="sxs-lookup"><span data-stu-id="f93aa-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f93aa-104">Izmantojiet šo procedūru, lai izveidotu un piešķirtu izmaksu sadalījuma politiku un atbilstošas kārtulas izmaksu vadības ierīcei.</span><span class="sxs-lookup"><span data-stu-id="f93aa-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="f93aa-105">Šajā ierakstā tiek izmantots USP2 demonstrācijas datu uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="f93aa-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="f93aa-106">Politikas izveide</span><span class="sxs-lookup"><span data-stu-id="f93aa-106">Create a policy</span></span>
1. <span data-ttu-id="f93aa-107">Dodieties uz Izmaksu uzskaite > Politikas > Izmaksu sadalījuma politikas.</span><span class="sxs-lookup"><span data-stu-id="f93aa-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="f93aa-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f93aa-108">Click New.</span></span>
3. <span data-ttu-id="f93aa-109">Laukā Politikas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f93aa-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="f93aa-110">Laukā Izmaksu objekta dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f93aa-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="f93aa-111">Atlasiet Organizācija.</span><span class="sxs-lookup"><span data-stu-id="f93aa-111">Select Organization.</span></span>  
5. <span data-ttu-id="f93aa-112">Laukā Statistiskā dimensija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f93aa-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="f93aa-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f93aa-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="f93aa-114">Sadalījuma kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="f93aa-114">Create allocation rules</span></span>
1. <span data-ttu-id="f93aa-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f93aa-115">Click New.</span></span>
2. <span data-ttu-id="f93aa-116">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f93aa-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="f93aa-117">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f93aa-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="f93aa-118">Laukā Izmaksu izturēšanās atlasiet "Total".</span><span class="sxs-lookup"><span data-stu-id="f93aa-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="f93aa-119">Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f93aa-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="f93aa-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f93aa-120">Click New.</span></span>
7. <span data-ttu-id="f93aa-121">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f93aa-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="f93aa-122">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f93aa-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="f93aa-123">Laukā Izmaksu izturēšanās atlasiet "Total".</span><span class="sxs-lookup"><span data-stu-id="f93aa-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="f93aa-124">Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f93aa-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="f93aa-125">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f93aa-125">Click New.</span></span>
12. <span data-ttu-id="f93aa-126">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f93aa-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="f93aa-127">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f93aa-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="f93aa-128">Laukā Izmaksu izturēšanās atlasiet "Total".</span><span class="sxs-lookup"><span data-stu-id="f93aa-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="f93aa-129">Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f93aa-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="f93aa-130">Turpiniet, līdz esat izveidojis visas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="f93aa-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="f93aa-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f93aa-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="f93aa-132">Politikas piešķiršana izmaksu vadības ierīcei</span><span class="sxs-lookup"><span data-stu-id="f93aa-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="f93aa-133">Noklikšķiniet uz Izmaksu vadības ierīces politikas piešķires.</span><span class="sxs-lookup"><span data-stu-id="f93aa-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="f93aa-134">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f93aa-134">Click New.</span></span>
3. <span data-ttu-id="f93aa-135">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f93aa-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f93aa-136">Laukā Derīgs no uzskaites datuma ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="f93aa-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="f93aa-137">Kārtulas ir efektīvas.</span><span class="sxs-lookup"><span data-stu-id="f93aa-137">The rules are date-effective.</span></span> <span data-ttu-id="f93aa-138">Lietotājs vai sistēma var anulēt kārtulas, ja tiek izveidota jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="f93aa-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="f93aa-139">Laukā Izmaksu vadības ierīce ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f93aa-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="f93aa-140">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f93aa-140">Click Save.</span></span>

