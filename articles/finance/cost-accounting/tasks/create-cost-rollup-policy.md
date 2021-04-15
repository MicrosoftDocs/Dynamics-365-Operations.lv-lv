---
title: Izmaksu apkopošanas politikas izveide
description: Šī procedūra parāda, kā izveidot izmaksu apkopošanas politiku un izveidot kārtulas politikai.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50a50dc359dc4c2741ac4d280a9f97c6a7f2c259
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810022"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="9616a-103">Izmaksu apkopošanas politikas izveide</span><span class="sxs-lookup"><span data-stu-id="9616a-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9616a-104">Šī procedūra parāda, kā izveidot izmaksu apkopošanas politiku un izveidot kārtulas politikai.</span><span class="sxs-lookup"><span data-stu-id="9616a-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="9616a-105">Demonstrācijas dati, kas tiek izmantoti, lai izveidotu šo procedūru, ir USP2.</span><span class="sxs-lookup"><span data-stu-id="9616a-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="9616a-106">Politikas izveide</span><span class="sxs-lookup"><span data-stu-id="9616a-106">Create a policy</span></span>
1. <span data-ttu-id="9616a-107">Dodieties uz Izmaksu uzskaite > Politikas > Izmaksu apkopojuma politikas.</span><span class="sxs-lookup"><span data-stu-id="9616a-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="9616a-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9616a-108">Click New.</span></span>
3. <span data-ttu-id="9616a-109">Laukā Politikas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9616a-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="9616a-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9616a-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9616a-111">Laukā Izmaksu objekta dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9616a-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="9616a-112">Atlasiet Izmaksu apkopojums CC.</span><span class="sxs-lookup"><span data-stu-id="9616a-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="9616a-113">Laukā Izmaksu elementa dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9616a-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="9616a-114">Atlasiet Izmaksu apkopojums CC.</span><span class="sxs-lookup"><span data-stu-id="9616a-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="9616a-115">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9616a-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="9616a-116">Kārtulu izveide izmaksu apkopošanas politikai</span><span class="sxs-lookup"><span data-stu-id="9616a-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="9616a-117">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9616a-117">Click New.</span></span>
2. <span data-ttu-id="9616a-118">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9616a-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="9616a-119">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9616a-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="9616a-120">Atlasiet 007.</span><span class="sxs-lookup"><span data-stu-id="9616a-120">Select 007.</span></span>  
4. <span data-ttu-id="9616a-121">Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9616a-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="9616a-122">Atlasiet Izmaksu apkopojums CE.</span><span class="sxs-lookup"><span data-stu-id="9616a-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="9616a-123">Laukā Sekundārais izmaksu elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9616a-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="9616a-124">Šim piemēram kartējiet sekundāro izmaksu elementu CC-007 uz izmaksu centru.</span><span class="sxs-lookup"><span data-stu-id="9616a-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="9616a-125">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9616a-125">Click New.</span></span>
7. <span data-ttu-id="9616a-126">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9616a-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="9616a-127">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9616a-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="9616a-128">Atlasiet 008.</span><span class="sxs-lookup"><span data-stu-id="9616a-128">Select 008.</span></span>  
9. <span data-ttu-id="9616a-129">Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9616a-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="9616a-130">Atlasiet Izmaksu apkopojums CE.</span><span class="sxs-lookup"><span data-stu-id="9616a-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="9616a-131">Laukā Sekundārais izmaksu elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9616a-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="9616a-132">Šim piemēram kartējiet sekundāro izmaksu elementu CC-008 uz izmaksu centru.</span><span class="sxs-lookup"><span data-stu-id="9616a-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="9616a-133">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9616a-133">Click New.</span></span>
12. <span data-ttu-id="9616a-134">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9616a-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="9616a-135">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9616a-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="9616a-136">Atlasiet 009.</span><span class="sxs-lookup"><span data-stu-id="9616a-136">Select 009.</span></span>  
14. <span data-ttu-id="9616a-137">Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9616a-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="9616a-138">Atlasiet Izmaksu apkopojums CE.</span><span class="sxs-lookup"><span data-stu-id="9616a-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="9616a-139">Laukā Sekundārais izmaksu elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9616a-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="9616a-140">Šim piemēram kartējiet sekundāro izmaksu elementu CC-009 uz izmaksu centru.</span><span class="sxs-lookup"><span data-stu-id="9616a-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="9616a-141">Turpiniet, līdz visi izmaksu centri tiek kartēti uz to attiecīgajiem sekundārajiem izmaksu elementiem.</span><span class="sxs-lookup"><span data-stu-id="9616a-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="9616a-142">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9616a-142">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]