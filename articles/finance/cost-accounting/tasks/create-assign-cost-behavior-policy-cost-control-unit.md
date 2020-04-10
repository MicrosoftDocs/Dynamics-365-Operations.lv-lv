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
ms.openlocfilehash: 7e923bd4e8f89aa9398b6327fe28998f845218d4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144408"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="e9846-103">Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei</span><span class="sxs-lookup"><span data-stu-id="e9846-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e9846-104">Izmaksu izturēšanās ir izmaksu klasifikācija fiksētajās vai mainīgajās izmaksās.</span><span class="sxs-lookup"><span data-stu-id="e9846-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="e9846-105">Lai politika stātos spēkā, politika un attiecīgās kārtulas ir jāpiešķir izmaksu vadības ierīcei.</span><span class="sxs-lookup"><span data-stu-id="e9846-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="e9846-106">Izmantojiet šo procedūru, lai izveidotu un pēc tam piešķirtu politiku izmaksu vadības ierīcei.</span><span class="sxs-lookup"><span data-stu-id="e9846-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="e9846-107">Izmaksu izturēšanās hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="e9846-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="e9846-108">Dodieties uz Izmaksu uzskaite > Dimensijas > Dimensiju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="e9846-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="e9846-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e9846-109">Click New.</span></span>
3. <span data-ttu-id="e9846-110">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="e9846-110">Click Create.</span></span>
4. <span data-ttu-id="e9846-111">Laukā Dimensiju hierarhijas nosaukums ierakstiet "Cost behavior hierarchy".</span><span class="sxs-lookup"><span data-stu-id="e9846-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="e9846-112">Laukā Dimensija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9846-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="e9846-113">Atlasiet Izmaksu elementi.</span><span class="sxs-lookup"><span data-stu-id="e9846-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="e9846-114">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e9846-114">Click Save.</span></span>
7. <span data-ttu-id="e9846-115">Noklikšķiniet uz Skatīt hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="e9846-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="e9846-116">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e9846-116">Click New.</span></span>
9. <span data-ttu-id="e9846-117">Laukā Zara nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9846-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="e9846-118">Ievadiet fiksētās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e9846-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="e9846-119">Kokā atlasiet "Cost behavior hierarchy".</span><span class="sxs-lookup"><span data-stu-id="e9846-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="e9846-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e9846-120">Click New.</span></span>
12. <span data-ttu-id="e9846-121">Laukā Zara nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9846-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="e9846-122">Ievadiet mainīgās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e9846-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="e9846-123">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e9846-123">Click Save.</span></span>
14. <span data-ttu-id="e9846-124">Kokā atlasiet Cost behavior hierarchy\Fixed cost.</span><span class="sxs-lookup"><span data-stu-id="e9846-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="e9846-125">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e9846-125">Click New.</span></span>
16. <span data-ttu-id="e9846-126">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e9846-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="e9846-127">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9846-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="e9846-128">Dimensijas elementu diapazons var saturēt atstarpes, bet elementi nedrīkst pārklāties.</span><span class="sxs-lookup"><span data-stu-id="e9846-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="e9846-129">Laukā Mērķa dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9846-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="e9846-130">Dimensijas elementu diapazons var saturēt atstarpes, bet elementi nedrīkst pārklāties.</span><span class="sxs-lookup"><span data-stu-id="e9846-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="e9846-131">Kokā atlasiet Cost behavior hierarchy\Variable cost.</span><span class="sxs-lookup"><span data-stu-id="e9846-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="e9846-132">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e9846-132">Click New.</span></span>
21. <span data-ttu-id="e9846-133">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e9846-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="e9846-134">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9846-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="e9846-135">Dimensijas elementu diapazons var saturēt atstarpes, bet elementi nedrīkst pārklāties.</span><span class="sxs-lookup"><span data-stu-id="e9846-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="e9846-136">Laukā Mērķa dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9846-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="e9846-137">Dimensijas elementu diapazons var saturēt atstarpes, bet elementi nedrīkst pārklāties.</span><span class="sxs-lookup"><span data-stu-id="e9846-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="e9846-138">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e9846-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="e9846-139">Politikas un kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="e9846-139">Create the policy and rules</span></span>
1. <span data-ttu-id="e9846-140">Dodieties uz Izmaksu uzskaite > Politikas > Izmaksu izturēšanās politikas.</span><span class="sxs-lookup"><span data-stu-id="e9846-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="e9846-141">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e9846-141">Click New.</span></span>
3. <span data-ttu-id="e9846-142">Laukā Politikas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9846-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="e9846-143">Laukā Izmaksu elementa dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9846-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="e9846-144">Atlasiet politikas hierarhiju, ko tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="e9846-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="e9846-145">Laukā Izmaksu objekta dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9846-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="e9846-146">Atlasiet Organizācija.</span><span class="sxs-lookup"><span data-stu-id="e9846-146">Select Organization.</span></span>  
6. <span data-ttu-id="e9846-147">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e9846-147">Click Save.</span></span>
7. <span data-ttu-id="e9846-148">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e9846-148">Click New.</span></span>
8. <span data-ttu-id="e9846-149">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e9846-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="e9846-150">Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9846-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="e9846-151">Izvērsiet hierarhiju, lai atlasītu Mainīgās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e9846-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="e9846-152">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9846-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="e9846-153">Pēc noklusējuma mainīgā procentuālā vērtība ir 100 procenti.</span><span class="sxs-lookup"><span data-stu-id="e9846-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="e9846-154">Noklikšķiniet uz Izmaksu vadības ierīces politikas piešķires.</span><span class="sxs-lookup"><span data-stu-id="e9846-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="e9846-155">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e9846-155">Click New.</span></span>
13. <span data-ttu-id="e9846-156">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e9846-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="e9846-157">Laukā Derīgs no uzskaites datuma ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="e9846-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="e9846-158">Kārtulas ir efektīvas, un lietotājs vai sistēma var anulēt kārtulu, ja tiek izveidota jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="e9846-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="e9846-159">Laukā Izmaksu vadības ierīce ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9846-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="e9846-160">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e9846-160">Click Save.</span></span>

