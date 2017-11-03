---
title: "Reizinātāja nolietojums"
description: "Šajā rakstā ir sniegts pārskats par koeficienta nolietojuma metodi."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 44fa540c31e5302ccf0a65b44b3c45a4c1e1fd1f
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="factor-depreciation"></a><span data-ttu-id="58bca-103">Reizinātāja nolietojums</span><span class="sxs-lookup"><span data-stu-id="58bca-103">Factor depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="58bca-104">Šajā rakstā ir sniegts pārskats par koeficienta nolietojuma metodi.</span><span class="sxs-lookup"><span data-stu-id="58bca-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="58bca-105">Koeficienti ir procenti, kurus lieto, lai pazeminātu pamatlīdzekļu vērtību.</span><span class="sxs-lookup"><span data-stu-id="58bca-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="58bca-106">Ja iestatāt pamatlīdzekļa nolietojuma tabulu un lapā **Nolietojuma tabulas** atlasāt lauka **Metode** vērtību **Koeficients**, varat iestatīt progresīvo, regresīvo vai lineāro nolietojumu.</span><span class="sxs-lookup"><span data-stu-id="58bca-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="58bca-107">Izmantojot progresīvo nolietojumu, katrā nolietojuma periodā palielinās nolietojuma summa.</span><span class="sxs-lookup"><span data-stu-id="58bca-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="58bca-108">Izmantojot regresīvo nolietojumu, katra perioda nolietojuma summa laika gaitā samazinās.</span><span class="sxs-lookup"><span data-stu-id="58bca-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="58bca-109">Izmantojot lineāro nolietojumu, visu periodu nolietojums ir vienāds.</span><span class="sxs-lookup"><span data-stu-id="58bca-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="58bca-110">Tālāk sniegtajos noteikumos un piemēros ir norādīts, kā varat iestatīt katra nolietojuma veida koeficientus.</span><span class="sxs-lookup"><span data-stu-id="58bca-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="58bca-111">Ja atlasāt lauka **Metode** vērtību **Koeficients**, tiek parādīts lauks **Koeficients** un lauks **Intervāls**.</span><span class="sxs-lookup"><span data-stu-id="58bca-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="58bca-112">Progresīvais nolietojums</span><span class="sxs-lookup"><span data-stu-id="58bca-112">Progressive depreciation</span></span>
<span data-ttu-id="58bca-113">Lauka **Koeficients** vērtība ir lielāka nekā **50**.</span><span class="sxs-lookup"><span data-stu-id="58bca-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="58bca-114">Piemērs</span><span class="sxs-lookup"><span data-stu-id="58bca-114">Example</span></span>

<span data-ttu-id="58bca-115">Iegādes cena ir 100 000, koeficents ir 70, lietošanas ilgums ir 10 gadi, un nolietojums sākas 1. janvārī.</span><span class="sxs-lookup"><span data-stu-id="58bca-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="58bca-116">Nolietojuma summas un atlikušās vērtības summas tiek rādītas vienīgi pirmajiem sešiem lietošanas ilguma gadiem.</span><span class="sxs-lookup"><span data-stu-id="58bca-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="58bca-117">Gads</span><span class="sxs-lookup"><span data-stu-id="58bca-117">Year</span></span> | <span data-ttu-id="58bca-118">Periods</span><span class="sxs-lookup"><span data-stu-id="58bca-118">Period</span></span>      | <span data-ttu-id="58bca-119">Nolietojuma summa</span><span class="sxs-lookup"><span data-stu-id="58bca-119">Depreciation amount</span></span> | <span data-ttu-id="58bca-120">Atlikušās vērtības summa</span><span class="sxs-lookup"><span data-stu-id="58bca-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="58bca-121">1</span><span class="sxs-lookup"><span data-stu-id="58bca-121">1</span></span>    | <span data-ttu-id="58bca-122">31. decembris</span><span class="sxs-lookup"><span data-stu-id="58bca-122">December 31</span></span> | <span data-ttu-id="58bca-123">307,69</span><span class="sxs-lookup"><span data-stu-id="58bca-123">307.69</span></span>              | <span data-ttu-id="58bca-124">99 692,31</span><span class="sxs-lookup"><span data-stu-id="58bca-124">99,692.31</span></span>             |
| <span data-ttu-id="58bca-125">2</span><span class="sxs-lookup"><span data-stu-id="58bca-125">2</span></span>    | <span data-ttu-id="58bca-126">31. decembris</span><span class="sxs-lookup"><span data-stu-id="58bca-126">December 31</span></span> | <span data-ttu-id="58bca-127">1 447,21</span><span class="sxs-lookup"><span data-stu-id="58bca-127">1,447.21</span></span>            | <span data-ttu-id="58bca-128">98 245,10</span><span class="sxs-lookup"><span data-stu-id="58bca-128">98,245.10</span></span>             |
| <span data-ttu-id="58bca-129">3</span><span class="sxs-lookup"><span data-stu-id="58bca-129">3</span></span>    | <span data-ttu-id="58bca-130">31. decembris</span><span class="sxs-lookup"><span data-stu-id="58bca-130">December 31</span></span> | <span data-ttu-id="58bca-131">3 104,50</span><span class="sxs-lookup"><span data-stu-id="58bca-131">3,104.50</span></span>            | <span data-ttu-id="58bca-132">95 140,60</span><span class="sxs-lookup"><span data-stu-id="58bca-132">95,140.60</span></span>             |
| <span data-ttu-id="58bca-133">4.</span><span class="sxs-lookup"><span data-stu-id="58bca-133">4</span></span>    | <span data-ttu-id="58bca-134">31. decembris</span><span class="sxs-lookup"><span data-stu-id="58bca-134">December 31</span></span> | <span data-ttu-id="58bca-135">5 150,21</span><span class="sxs-lookup"><span data-stu-id="58bca-135">5,150.21</span></span>            | <span data-ttu-id="58bca-136">89 990,39</span><span class="sxs-lookup"><span data-stu-id="58bca-136">89,990.39</span></span>             |
| <span data-ttu-id="58bca-137">5.</span><span class="sxs-lookup"><span data-stu-id="58bca-137">5</span></span>    | <span data-ttu-id="58bca-138">31. decembris</span><span class="sxs-lookup"><span data-stu-id="58bca-138">December 31</span></span> | <span data-ttu-id="58bca-139">7 522,95</span><span class="sxs-lookup"><span data-stu-id="58bca-139">7,522.95</span></span>            | <span data-ttu-id="58bca-140">82 467,44</span><span class="sxs-lookup"><span data-stu-id="58bca-140">82,467.44</span></span>             |
| <span data-ttu-id="58bca-141">6.</span><span class="sxs-lookup"><span data-stu-id="58bca-141">6</span></span>    | <span data-ttu-id="58bca-142">31. decembris</span><span class="sxs-lookup"><span data-stu-id="58bca-142">December 31</span></span> | <span data-ttu-id="58bca-143">10 184,06</span><span class="sxs-lookup"><span data-stu-id="58bca-143">10,184.06</span></span>           | <span data-ttu-id="58bca-144">72 283,38</span><span class="sxs-lookup"><span data-stu-id="58bca-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="58bca-145">Novirzošais nolietojums</span><span class="sxs-lookup"><span data-stu-id="58bca-145">Digressive depreciation</span></span>
<span data-ttu-id="58bca-146">Lauka **Koeficients** vērtība ir mazāka nekā **50**.</span><span class="sxs-lookup"><span data-stu-id="58bca-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="58bca-147">Piemērs</span><span class="sxs-lookup"><span data-stu-id="58bca-147">Example</span></span>

<span data-ttu-id="58bca-148">Iegādes cena ir 100 000, koeficents ir 20, lietošanas ilgums ir 10 gadi, un nolietojums sākas 1. janvārī.</span><span class="sxs-lookup"><span data-stu-id="58bca-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="58bca-149">Nolietojuma summas un atlikušās vērtības summas tiek rādītas vienīgi pirmajiem sešiem lietošanas ilguma gadiem.</span><span class="sxs-lookup"><span data-stu-id="58bca-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="58bca-150">Gads</span><span class="sxs-lookup"><span data-stu-id="58bca-150">Year</span></span> | <span data-ttu-id="58bca-151">Periods</span><span class="sxs-lookup"><span data-stu-id="58bca-151">Period</span></span>      | <span data-ttu-id="58bca-152">Nolietojuma summa</span><span class="sxs-lookup"><span data-stu-id="58bca-152">Depreciation amount</span></span> | <span data-ttu-id="58bca-153">Atlikušās vērtības summa</span><span class="sxs-lookup"><span data-stu-id="58bca-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="58bca-154">1</span><span class="sxs-lookup"><span data-stu-id="58bca-154">1</span></span>    | <span data-ttu-id="58bca-155">31. decembris</span><span class="sxs-lookup"><span data-stu-id="58bca-155">December 31</span></span> | <span data-ttu-id="58bca-156">56 080,43</span><span class="sxs-lookup"><span data-stu-id="58bca-156">56,080.43</span></span>           | <span data-ttu-id="58bca-157">43 919,57</span><span class="sxs-lookup"><span data-stu-id="58bca-157">43,919.57</span></span>             |
| <span data-ttu-id="58bca-158">2</span><span class="sxs-lookup"><span data-stu-id="58bca-158">2</span></span>    | <span data-ttu-id="58bca-159">31. decembris</span><span class="sxs-lookup"><span data-stu-id="58bca-159">December 31</span></span> | <span data-ttu-id="58bca-160">10 665,70</span><span class="sxs-lookup"><span data-stu-id="58bca-160">10,665.70</span></span>           | <span data-ttu-id="58bca-161">33 253,87</span><span class="sxs-lookup"><span data-stu-id="58bca-161">33,253.87</span></span>             |
| <span data-ttu-id="58bca-162">3</span><span class="sxs-lookup"><span data-stu-id="58bca-162">3</span></span>    | <span data-ttu-id="58bca-163">31. decembris</span><span class="sxs-lookup"><span data-stu-id="58bca-163">December 31</span></span> | <span data-ttu-id="58bca-164">7 156,22</span><span class="sxs-lookup"><span data-stu-id="58bca-164">7,156.22</span></span>            | <span data-ttu-id="58bca-165">26 097,65</span><span class="sxs-lookup"><span data-stu-id="58bca-165">26,097.65</span></span>             |
| <span data-ttu-id="58bca-166">4.</span><span class="sxs-lookup"><span data-stu-id="58bca-166">4</span></span>    | <span data-ttu-id="58bca-167">31. decembris</span><span class="sxs-lookup"><span data-stu-id="58bca-167">December 31</span></span> | <span data-ttu-id="58bca-168">5 538,06</span><span class="sxs-lookup"><span data-stu-id="58bca-168">5,538.06</span></span>            | <span data-ttu-id="58bca-169">20 559,59</span><span class="sxs-lookup"><span data-stu-id="58bca-169">20,559.59</span></span>             |
| <span data-ttu-id="58bca-170">5.</span><span class="sxs-lookup"><span data-stu-id="58bca-170">5</span></span>    | <span data-ttu-id="58bca-171">31. decembris</span><span class="sxs-lookup"><span data-stu-id="58bca-171">December 31</span></span> | <span data-ttu-id="58bca-172">4 579,89</span><span class="sxs-lookup"><span data-stu-id="58bca-172">4,579.89</span></span>            | <span data-ttu-id="58bca-173">15 979,70</span><span class="sxs-lookup"><span data-stu-id="58bca-173">15,979.70</span></span>             |
| <span data-ttu-id="58bca-174">6.</span><span class="sxs-lookup"><span data-stu-id="58bca-174">6</span></span>    | <span data-ttu-id="58bca-175">31. decembris</span><span class="sxs-lookup"><span data-stu-id="58bca-175">December 31</span></span> | <span data-ttu-id="58bca-176">3 937,36</span><span class="sxs-lookup"><span data-stu-id="58bca-176">3,937.36</span></span>            | <span data-ttu-id="58bca-177">12 042,34</span><span class="sxs-lookup"><span data-stu-id="58bca-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="58bca-178">Lineārais nolietojums</span><span class="sxs-lookup"><span data-stu-id="58bca-178">Straight line depreciation</span></span>
<span data-ttu-id="58bca-179">Lauka **Koeficients** vērtība ir **50**.</span><span class="sxs-lookup"><span data-stu-id="58bca-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="58bca-180">Šādā gadījumā nolietojums visos periodos ir vienāds un ir jāņem vērā ietekme, ko izraisa citos laukos norādītas vērtības, kā tas ir aprakstīts rakstā [Lineārā lietošanas ilguma nolietojums](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="58bca-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>




