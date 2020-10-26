---
title: Izmaksu apkopošanas politikas izveide
description: Šī procedūra parāda, kā izveidot izmaksu apkopošanas politiku un izveidot kārtulas politikai.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b6d32cc2c1844c6c334dd00b249c736e153f13d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977651"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="1af68-103">Izmaksu apkopošanas politikas izveide</span><span class="sxs-lookup"><span data-stu-id="1af68-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1af68-104">Šī procedūra parāda, kā izveidot izmaksu apkopošanas politiku un izveidot kārtulas politikai.</span><span class="sxs-lookup"><span data-stu-id="1af68-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="1af68-105">Demonstrācijas dati, kas tiek izmantoti, lai izveidotu šo procedūru, ir USP2.</span><span class="sxs-lookup"><span data-stu-id="1af68-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="1af68-106">Politikas izveide</span><span class="sxs-lookup"><span data-stu-id="1af68-106">Create a policy</span></span>
1. <span data-ttu-id="1af68-107">Dodieties uz Izmaksu uzskaite > Politikas > Izmaksu apkopojuma politikas.</span><span class="sxs-lookup"><span data-stu-id="1af68-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="1af68-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1af68-108">Click New.</span></span>
3. <span data-ttu-id="1af68-109">Laukā Politikas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1af68-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="1af68-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1af68-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1af68-111">Laukā Izmaksu objekta dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1af68-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="1af68-112">Atlasiet Izmaksu apkopojums CC.</span><span class="sxs-lookup"><span data-stu-id="1af68-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="1af68-113">Laukā Izmaksu elementa dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1af68-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="1af68-114">Atlasiet Izmaksu apkopojums CC.</span><span class="sxs-lookup"><span data-stu-id="1af68-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="1af68-115">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="1af68-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="1af68-116">Kārtulu izveide izmaksu apkopošanas politikai</span><span class="sxs-lookup"><span data-stu-id="1af68-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="1af68-117">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1af68-117">Click New.</span></span>
2. <span data-ttu-id="1af68-118">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="1af68-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="1af68-119">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1af68-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="1af68-120">Atlasiet 007.</span><span class="sxs-lookup"><span data-stu-id="1af68-120">Select 007.</span></span>  
4. <span data-ttu-id="1af68-121">Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1af68-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="1af68-122">Atlasiet Izmaksu apkopojums CE.</span><span class="sxs-lookup"><span data-stu-id="1af68-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="1af68-123">Laukā Sekundārais izmaksu elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1af68-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="1af68-124">Šim piemēram kartējiet sekundāro izmaksu elementu CC-007 uz izmaksu centru.</span><span class="sxs-lookup"><span data-stu-id="1af68-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="1af68-125">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1af68-125">Click New.</span></span>
7. <span data-ttu-id="1af68-126">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="1af68-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="1af68-127">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1af68-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="1af68-128">Atlasiet 008.</span><span class="sxs-lookup"><span data-stu-id="1af68-128">Select 008.</span></span>  
9. <span data-ttu-id="1af68-129">Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1af68-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="1af68-130">Atlasiet Izmaksu apkopojums CE.</span><span class="sxs-lookup"><span data-stu-id="1af68-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="1af68-131">Laukā Sekundārais izmaksu elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1af68-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="1af68-132">Šim piemēram kartējiet sekundāro izmaksu elementu CC-008 uz izmaksu centru.</span><span class="sxs-lookup"><span data-stu-id="1af68-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="1af68-133">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1af68-133">Click New.</span></span>
12. <span data-ttu-id="1af68-134">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="1af68-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="1af68-135">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1af68-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="1af68-136">Atlasiet 009.</span><span class="sxs-lookup"><span data-stu-id="1af68-136">Select 009.</span></span>  
14. <span data-ttu-id="1af68-137">Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1af68-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="1af68-138">Atlasiet Izmaksu apkopojums CE.</span><span class="sxs-lookup"><span data-stu-id="1af68-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="1af68-139">Laukā Sekundārais izmaksu elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1af68-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="1af68-140">Šim piemēram kartējiet sekundāro izmaksu elementu CC-009 uz izmaksu centru.</span><span class="sxs-lookup"><span data-stu-id="1af68-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="1af68-141">Turpiniet, līdz visi izmaksu centri tiek kartēti uz to attiecīgajiem sekundārajiem izmaksu elementiem.</span><span class="sxs-lookup"><span data-stu-id="1af68-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="1af68-142">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="1af68-142">Click Save.</span></span>

