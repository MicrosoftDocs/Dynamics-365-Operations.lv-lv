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
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b22dba0106721c095e6ce2e9b76cb9f5267e1c28
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208731"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="3730a-103">Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei</span><span class="sxs-lookup"><span data-stu-id="3730a-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3730a-104">Izmantojiet šo procedūru, lai izveidotu un piešķirtu izmaksu sadalījuma politiku un atbilstošas kārtulas izmaksu vadības ierīcei.</span><span class="sxs-lookup"><span data-stu-id="3730a-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="3730a-105">Šajā ierakstā tiek izmantots USP2 demonstrācijas datu uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="3730a-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="3730a-106">Politikas izveide</span><span class="sxs-lookup"><span data-stu-id="3730a-106">Create a policy</span></span>
1. <span data-ttu-id="3730a-107">Dodieties uz Izmaksu uzskaite > Politikas > Izmaksu sadalījuma politikas.</span><span class="sxs-lookup"><span data-stu-id="3730a-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="3730a-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3730a-108">Click New.</span></span>
3. <span data-ttu-id="3730a-109">Laukā Politikas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3730a-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="3730a-110">Laukā Izmaksu objekta dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3730a-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="3730a-111">Atlasiet Organizācija.</span><span class="sxs-lookup"><span data-stu-id="3730a-111">Select Organization.</span></span>  
5. <span data-ttu-id="3730a-112">Laukā Statistiskā dimensija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3730a-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="3730a-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3730a-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="3730a-114">Sadalījuma kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="3730a-114">Create allocation rules</span></span>
1. <span data-ttu-id="3730a-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3730a-115">Click New.</span></span>
2. <span data-ttu-id="3730a-116">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3730a-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="3730a-117">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3730a-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="3730a-118">Laukā Izmaksu izturēšanās atlasiet "Total".</span><span class="sxs-lookup"><span data-stu-id="3730a-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="3730a-119">Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3730a-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="3730a-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3730a-120">Click New.</span></span>
7. <span data-ttu-id="3730a-121">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3730a-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="3730a-122">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3730a-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="3730a-123">Laukā Izmaksu izturēšanās atlasiet "Total".</span><span class="sxs-lookup"><span data-stu-id="3730a-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="3730a-124">Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3730a-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="3730a-125">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3730a-125">Click New.</span></span>
12. <span data-ttu-id="3730a-126">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3730a-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="3730a-127">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3730a-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="3730a-128">Laukā Izmaksu izturēšanās atlasiet "Total".</span><span class="sxs-lookup"><span data-stu-id="3730a-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="3730a-129">Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3730a-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="3730a-130">Turpiniet, līdz esat izveidojis visas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="3730a-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="3730a-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3730a-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="3730a-132">Politikas piešķiršana izmaksu vadības ierīcei</span><span class="sxs-lookup"><span data-stu-id="3730a-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="3730a-133">Noklikšķiniet uz Izmaksu vadības ierīces politikas piešķires.</span><span class="sxs-lookup"><span data-stu-id="3730a-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="3730a-134">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3730a-134">Click New.</span></span>
3. <span data-ttu-id="3730a-135">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3730a-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3730a-136">Laukā Derīgs no uzskaites datuma ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="3730a-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="3730a-137">Kārtulas ir efektīvas.</span><span class="sxs-lookup"><span data-stu-id="3730a-137">The rules are date-effective.</span></span> <span data-ttu-id="3730a-138">Lietotājs vai sistēma var anulēt kārtulas, ja tiek izveidota jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="3730a-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="3730a-139">Laukā Izmaksu vadības ierīce ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3730a-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="3730a-140">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3730a-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]