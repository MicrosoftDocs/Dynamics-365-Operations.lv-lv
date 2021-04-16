---
title: Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei
description: Izmantojiet šo procedūru, lai izveidotu un piešķirtu izmaksu sadalījuma politiku un atbilstošas kārtulas izmaksu vadības ierīcei.
author: ShylaThompson
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1cff10132e8007be885e9c69d97cf96c30d69f50
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822859"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="ca27f-103">Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei</span><span class="sxs-lookup"><span data-stu-id="ca27f-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca27f-104">Izmantojiet šo procedūru, lai izveidotu un piešķirtu izmaksu sadalījuma politiku un atbilstošas kārtulas izmaksu vadības ierīcei.</span><span class="sxs-lookup"><span data-stu-id="ca27f-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="ca27f-105">Šajā ierakstā tiek izmantots USP2 demonstrācijas datu uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="ca27f-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="ca27f-106">Politikas izveide</span><span class="sxs-lookup"><span data-stu-id="ca27f-106">Create a policy</span></span>
1. <span data-ttu-id="ca27f-107">Dodieties uz Izmaksu uzskaite > Politikas > Izmaksu sadalījuma politikas.</span><span class="sxs-lookup"><span data-stu-id="ca27f-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="ca27f-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ca27f-108">Click New.</span></span>
3. <span data-ttu-id="ca27f-109">Laukā Politikas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca27f-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="ca27f-110">Laukā Izmaksu objekta dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca27f-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="ca27f-111">Atlasiet Organizācija.</span><span class="sxs-lookup"><span data-stu-id="ca27f-111">Select Organization.</span></span>  
5. <span data-ttu-id="ca27f-112">Laukā Statistiskā dimensija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca27f-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="ca27f-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ca27f-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="ca27f-114">Sadalījuma kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="ca27f-114">Create allocation rules</span></span>
1. <span data-ttu-id="ca27f-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ca27f-115">Click New.</span></span>
2. <span data-ttu-id="ca27f-116">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ca27f-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="ca27f-117">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca27f-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="ca27f-118">Laukā Izmaksu izturēšanās atlasiet "Total".</span><span class="sxs-lookup"><span data-stu-id="ca27f-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="ca27f-119">Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca27f-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="ca27f-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ca27f-120">Click New.</span></span>
7. <span data-ttu-id="ca27f-121">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ca27f-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="ca27f-122">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca27f-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="ca27f-123">Laukā Izmaksu izturēšanās atlasiet "Total".</span><span class="sxs-lookup"><span data-stu-id="ca27f-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="ca27f-124">Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca27f-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="ca27f-125">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ca27f-125">Click New.</span></span>
12. <span data-ttu-id="ca27f-126">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ca27f-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="ca27f-127">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca27f-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="ca27f-128">Laukā Izmaksu izturēšanās atlasiet "Total".</span><span class="sxs-lookup"><span data-stu-id="ca27f-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="ca27f-129">Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca27f-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="ca27f-130">Turpiniet, līdz esat izveidojis visas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="ca27f-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="ca27f-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ca27f-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="ca27f-132">Politikas piešķiršana izmaksu vadības ierīcei</span><span class="sxs-lookup"><span data-stu-id="ca27f-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="ca27f-133">Noklikšķiniet uz Izmaksu vadības ierīces politikas piešķires.</span><span class="sxs-lookup"><span data-stu-id="ca27f-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="ca27f-134">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ca27f-134">Click New.</span></span>
3. <span data-ttu-id="ca27f-135">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ca27f-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ca27f-136">Laukā Derīgs no uzskaites datuma ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="ca27f-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="ca27f-137">Kārtulas ir efektīvas.</span><span class="sxs-lookup"><span data-stu-id="ca27f-137">The rules are date-effective.</span></span> <span data-ttu-id="ca27f-138">Lietotājs vai sistēma var anulēt kārtulas, ja tiek izveidota jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="ca27f-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="ca27f-139">Laukā Izmaksu vadības ierīce ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca27f-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="ca27f-140">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ca27f-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]