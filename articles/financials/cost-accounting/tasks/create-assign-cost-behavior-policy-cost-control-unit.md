---
title: Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei
description: Izmaksu izturēšanās ir izmaksu klasifikācija fiksētajās vai mainīgajās izmaksās.
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
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16d9dceb4c2a22eab9a5ecb8501393444f20498b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841373"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="4e095-103">Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei</span><span class="sxs-lookup"><span data-stu-id="4e095-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4e095-104">Izmaksu izturēšanās ir izmaksu klasifikācija fiksētajās vai mainīgajās izmaksās.</span><span class="sxs-lookup"><span data-stu-id="4e095-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="4e095-105">Lai politika stātos spēkā, politika un attiecīgās kārtulas ir jāpiešķir izmaksu vadības ierīcei.</span><span class="sxs-lookup"><span data-stu-id="4e095-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="4e095-106">Izmantojiet šo procedūru, lai izveidotu un pēc tam piešķirtu politiku izmaksu vadības ierīcei.</span><span class="sxs-lookup"><span data-stu-id="4e095-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="4e095-107">Izmaksu izturēšanās hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="4e095-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="4e095-108">Dodieties uz Izmaksu uzskaite > Dimensijas > Dimensiju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="4e095-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="4e095-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4e095-109">Click New.</span></span>
3. <span data-ttu-id="4e095-110">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="4e095-110">Click Create.</span></span>
4. <span data-ttu-id="4e095-111">Laukā Dimensiju hierarhijas nosaukums ierakstiet "Cost behavior hierarchy".</span><span class="sxs-lookup"><span data-stu-id="4e095-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="4e095-112">Laukā Dimensija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4e095-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="4e095-113">Atlasiet Izmaksu elementi.</span><span class="sxs-lookup"><span data-stu-id="4e095-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="4e095-114">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="4e095-114">Click Save.</span></span>
7. <span data-ttu-id="4e095-115">Noklikšķiniet uz Skatīt hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="4e095-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="4e095-116">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4e095-116">Click New.</span></span>
9. <span data-ttu-id="4e095-117">Laukā Zara nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4e095-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="4e095-118">Ievadiet fiksētās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="4e095-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="4e095-119">Kokā atlasiet "Cost behavior hierarchy".</span><span class="sxs-lookup"><span data-stu-id="4e095-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="4e095-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4e095-120">Click New.</span></span>
12. <span data-ttu-id="4e095-121">Laukā Zara nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4e095-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="4e095-122">Ievadiet mainīgās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="4e095-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="4e095-123">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="4e095-123">Click Save.</span></span>
14. <span data-ttu-id="4e095-124">Kokā atlasiet Cost behavior hierarchy\Fixed cost.</span><span class="sxs-lookup"><span data-stu-id="4e095-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="4e095-125">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4e095-125">Click New.</span></span>
16. <span data-ttu-id="4e095-126">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="4e095-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="4e095-127">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4e095-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4e095-128">Dimensijas elementu diapazons var saturēt atstarpes, bet elementi nedrīkst pārklāties.</span><span class="sxs-lookup"><span data-stu-id="4e095-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="4e095-129">Laukā Mērķa dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4e095-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4e095-130">Dimensijas elementu diapazons var saturēt atstarpes, bet elementi nedrīkst pārklāties.</span><span class="sxs-lookup"><span data-stu-id="4e095-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="4e095-131">Kokā atlasiet Cost behavior hierarchy\Variable cost.</span><span class="sxs-lookup"><span data-stu-id="4e095-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="4e095-132">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4e095-132">Click New.</span></span>
21. <span data-ttu-id="4e095-133">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="4e095-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="4e095-134">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4e095-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4e095-135">Dimensijas elementu diapazons var saturēt atstarpes, bet elementi nedrīkst pārklāties.</span><span class="sxs-lookup"><span data-stu-id="4e095-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="4e095-136">Laukā Mērķa dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4e095-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4e095-137">Dimensijas elementu diapazons var saturēt atstarpes, bet elementi nedrīkst pārklāties.</span><span class="sxs-lookup"><span data-stu-id="4e095-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="4e095-138">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="4e095-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="4e095-139">Politikas un kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="4e095-139">Create the policy and rules</span></span>
1. <span data-ttu-id="4e095-140">Dodieties uz Izmaksu uzskaite > Politikas > Izmaksu izturēšanās politikas.</span><span class="sxs-lookup"><span data-stu-id="4e095-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="4e095-141">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4e095-141">Click New.</span></span>
3. <span data-ttu-id="4e095-142">Laukā Politikas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4e095-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="4e095-143">Laukā Izmaksu elementa dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4e095-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="4e095-144">Atlasiet politikas hierarhiju, ko tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="4e095-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="4e095-145">Laukā Izmaksu objekta dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4e095-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="4e095-146">Atlasiet Organizācija.</span><span class="sxs-lookup"><span data-stu-id="4e095-146">Select Organization.</span></span>  
6. <span data-ttu-id="4e095-147">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="4e095-147">Click Save.</span></span>
7. <span data-ttu-id="4e095-148">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4e095-148">Click New.</span></span>
8. <span data-ttu-id="4e095-149">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="4e095-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4e095-150">Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4e095-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4e095-151">Izvērsiet hierarhiju, lai atlasītu Mainīgās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="4e095-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="4e095-152">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4e095-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4e095-153">Pēc noklusējuma mainīgā procentuālā vērtība ir 100 procenti.</span><span class="sxs-lookup"><span data-stu-id="4e095-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="4e095-154">Noklikšķiniet uz Izmaksu vadības ierīces politikas piešķires.</span><span class="sxs-lookup"><span data-stu-id="4e095-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="4e095-155">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4e095-155">Click New.</span></span>
13. <span data-ttu-id="4e095-156">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="4e095-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="4e095-157">Laukā Derīgs no uzskaites datuma ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="4e095-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="4e095-158">Kārtulas ir efektīvas, un lietotājs vai sistēma var anulēt kārtulu, ja tiek izveidota jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="4e095-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="4e095-159">Laukā Izmaksu vadības ierīce ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4e095-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="4e095-160">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="4e095-160">Click Save.</span></span>

