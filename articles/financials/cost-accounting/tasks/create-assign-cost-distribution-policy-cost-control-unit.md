--- 
title: "Izmaksu sadales politikas izveide un piešķiršana izmaksu vadības ierīcei"
description: "Izmaksu sadales kārtulas tiek izmantotas, lai sadalītu izmaksas, kas ir finansiāli aprēķinātas uz kolektīvo izmaksu centru."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 32f2bcee1f5905cf395a0e00305eab9b0d8a08a3
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="6d15e-103">Izmaksu sadales politikas izveide un piešķiršana izmaksu vadības ierīcei</span><span class="sxs-lookup"><span data-stu-id="6d15e-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d15e-104">Izmaksu sadales kārtulas tiek izmantotas, lai sadalītu izmaksas, kas ir finansiāli aprēķinātas uz kolektīvo izmaksu centru.</span><span class="sxs-lookup"><span data-stu-id="6d15e-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="6d15e-105">Izmaksu grāmatvedis nodrošina, ka izmaksas tiek sadalītas izmaksu centros, pamatojoties uz atlasīto sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="6d15e-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="6d15e-106">Izmaksu vadības ierīcei tiek piešķirta politika un atbilstošas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="6d15e-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="6d15e-107">Šis uzdevuma ceļvedis izmanto piemēru, lai parādītu, kā izveidot izmaksu sadales politiku un atbilstošas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="6d15e-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="6d15e-108">Politikas izveide</span><span class="sxs-lookup"><span data-stu-id="6d15e-108">Create a policy</span></span>
1. <span data-ttu-id="6d15e-109">Dodieties uz Izmaksu uzskaite > Politikas > Izmaksu sadales politikas.</span><span class="sxs-lookup"><span data-stu-id="6d15e-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="6d15e-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="6d15e-110">Click New.</span></span>
3. <span data-ttu-id="6d15e-111">Laukā Politikas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6d15e-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="6d15e-112">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="6d15e-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6d15e-113">Laukā Izmaksu objekta dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6d15e-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="6d15e-114">Atlasiet Organizācija.</span><span class="sxs-lookup"><span data-stu-id="6d15e-114">Select Organization.</span></span>  
6. <span data-ttu-id="6d15e-115">Laukā Izmaksu elementa dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6d15e-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="6d15e-116">Atlasiet CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="6d15e-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="6d15e-117">Laukā Statistiskā dimensija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6d15e-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="6d15e-118">Atlasiet Statistiskie elementi.</span><span class="sxs-lookup"><span data-stu-id="6d15e-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="6d15e-119">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6d15e-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="6d15e-120">Politikas kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="6d15e-120">Create rules for the policy</span></span>
1. <span data-ttu-id="6d15e-121">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="6d15e-121">Click New.</span></span>
2. <span data-ttu-id="6d15e-122">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="6d15e-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="6d15e-123">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6d15e-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="6d15e-124">Izvērsiet hierarhiju, lai atlasītu 094.</span><span class="sxs-lookup"><span data-stu-id="6d15e-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="6d15e-125">Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6d15e-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="6d15e-126">Atlasiet Citi saimnieciskās darbības izdevumi un pēc tam atlasiet 605110 Tīrīšana.</span><span class="sxs-lookup"><span data-stu-id="6d15e-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="6d15e-127">Laukā Izmaksu izturēšanās atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="6d15e-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="6d15e-128">Atlasiet Fiksētās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="6d15e-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="6d15e-129">Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6d15e-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="6d15e-130">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="6d15e-130">Click New.</span></span>
8. <span data-ttu-id="6d15e-131">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="6d15e-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="6d15e-132">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6d15e-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="6d15e-133">Izvērsiet hierarhiju, lai atlasītu 094.</span><span class="sxs-lookup"><span data-stu-id="6d15e-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="6d15e-134">Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6d15e-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="6d15e-135">Atlasiet Citi saimnieciskās darbības izdevumi un pēc tam atlasiet 605150 Īre.</span><span class="sxs-lookup"><span data-stu-id="6d15e-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="6d15e-136">Laukā Izmaksu izturēšanās atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="6d15e-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="6d15e-137">Atlasiet Fiksētās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="6d15e-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="6d15e-138">Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6d15e-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="6d15e-139">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6d15e-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="6d15e-140">Kārtulu piešķiršana izmaksu vadības ierīcei</span><span class="sxs-lookup"><span data-stu-id="6d15e-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="6d15e-141">Noklikšķiniet uz Izmaksu vadības ierīces politikas piešķires.</span><span class="sxs-lookup"><span data-stu-id="6d15e-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="6d15e-142">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="6d15e-142">Click New.</span></span>
3. <span data-ttu-id="6d15e-143">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="6d15e-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6d15e-144">Laukā Derīgs no uzskaites datuma ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="6d15e-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="6d15e-145">Atlasiet 1. septembris derīgā finanšu gadā.</span><span class="sxs-lookup"><span data-stu-id="6d15e-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="6d15e-146">Laukā Izmaksu vadības ierīce ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6d15e-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="6d15e-147">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6d15e-147">Click Save.</span></span>


