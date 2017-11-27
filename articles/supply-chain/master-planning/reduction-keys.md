---
title: "Samazināšanas principi"
description: "Šajā rakstā ir sniegti piemēri, kas izskaidro, kā iestatīt samazināšanas principu. Šeit iekļauta informācija par dažādiem samazināšanas principa iestatījumiem un to visu rezultātiem. Samazināšanas principu var izmantot, lai noteiktu, kā samazināt budžeta vajadzības."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 506ca3aac7ad271ca7472f3b74627e94d97a74ee
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="reduction-keys"></a><span data-ttu-id="dc3ec-105">Samazināšanas principi</span><span class="sxs-lookup"><span data-stu-id="dc3ec-105">Reduction keys</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="dc3ec-106">Šajā rakstā ir sniegti piemēri, kas izskaidro, kā iestatīt samazināšanas principu.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="dc3ec-107">Šeit iekļauta informācija par dažādiem samazināšanas principa iestatījumiem un to visu rezultātiem.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="dc3ec-108">Samazināšanas principu var izmantot, lai noteiktu, kā samazināt budžeta vajadzības.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="dc3ec-109">1. piemērs: Procenti — samazināšanas princips prognozes samazināšanai</span><span class="sxs-lookup"><span data-stu-id="dc3ec-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="dc3ec-110">Šis piemērs parāda, kā samazināšanas princips samazina pieprasījuma apjoma prognozes prasības atbilstoši samazināšanas principa noteiktajiem procentiem un laika periodiem.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1.  <span data-ttu-id="dc3ec-111">Lapā **Samazināšanas principi** iestatiet šādas rindas.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-111">On the **Reduction keys** page, set up the following lines.</span></span>
    | <span data-ttu-id="dc3ec-112">Izdodamais atlikums</span><span class="sxs-lookup"><span data-stu-id="dc3ec-112">Change</span></span> | <span data-ttu-id="dc3ec-113">Vienība</span><span class="sxs-lookup"><span data-stu-id="dc3ec-113">Unit</span></span>  | <span data-ttu-id="dc3ec-114">Procenti</span><span class="sxs-lookup"><span data-stu-id="dc3ec-114">Percent</span></span> |
    |--------|-------|---------|
    | <span data-ttu-id="dc3ec-115">1</span><span class="sxs-lookup"><span data-stu-id="dc3ec-115">1</span></span>      | <span data-ttu-id="dc3ec-116">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="dc3ec-116">Month</span></span> | <span data-ttu-id="dc3ec-117">100</span><span class="sxs-lookup"><span data-stu-id="dc3ec-117">100</span></span>     |
    | <span data-ttu-id="dc3ec-118">2</span><span class="sxs-lookup"><span data-stu-id="dc3ec-118">2</span></span>      | <span data-ttu-id="dc3ec-119">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="dc3ec-119">Month</span></span> | <span data-ttu-id="dc3ec-120">75</span><span class="sxs-lookup"><span data-stu-id="dc3ec-120">75</span></span>      |
    | <span data-ttu-id="dc3ec-121">3</span><span class="sxs-lookup"><span data-stu-id="dc3ec-121">3</span></span>      | <span data-ttu-id="dc3ec-122">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="dc3ec-122">Month</span></span> | <span data-ttu-id="dc3ec-123">50</span><span class="sxs-lookup"><span data-stu-id="dc3ec-123">50</span></span>      |
    | <span data-ttu-id="dc3ec-124">4.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-124">4</span></span>      | <span data-ttu-id="dc3ec-125">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="dc3ec-125">Month</span></span> | <span data-ttu-id="dc3ec-126">25</span><span class="sxs-lookup"><span data-stu-id="dc3ec-126">25</span></span>      |

2.  <span data-ttu-id="dc3ec-127">Piesaistiet samazināšanas principu krājuma vajadzību grupai.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-127">Link the reduction key to the item's coverage group.</span></span>
3.  <span data-ttu-id="dc3ec-128">Lapas **Vispārējie plāni** laukā **Samazināšanas princips** atlasiet **Procenti — samazināšanas princips**.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4.  <span data-ttu-id="dc3ec-129">Izveidojiet pieprasījuma apjoma prognozi 1000 gabaliem mēnesī.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="dc3ec-130">Sākot budžeta plānošanu 1. janvārī, pieprasījuma apjoma prognozes vajadzības tiek patērētas atbilstoši procentiem, ko iestatāt lapā **Samazināšanas principi**.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="dc3ec-131">Uz vispārējo plānu tiek pārsūtīti šādi vajadzību daudzumi.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="dc3ec-132">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="dc3ec-132">Month</span></span>                | <span data-ttu-id="dc3ec-133">Vajadzīgo gabalu skaits</span><span class="sxs-lookup"><span data-stu-id="dc3ec-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="dc3ec-134">janvāris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-134">January</span></span>              | <span data-ttu-id="dc3ec-135">0</span><span class="sxs-lookup"><span data-stu-id="dc3ec-135">0</span></span>                         |
| <span data-ttu-id="dc3ec-136">Februārī</span><span class="sxs-lookup"><span data-stu-id="dc3ec-136">February</span></span>             | <span data-ttu-id="dc3ec-137">250</span><span class="sxs-lookup"><span data-stu-id="dc3ec-137">250</span></span>                       |
| <span data-ttu-id="dc3ec-138">Martā</span><span class="sxs-lookup"><span data-stu-id="dc3ec-138">March</span></span>                | <span data-ttu-id="dc3ec-139">500</span><span class="sxs-lookup"><span data-stu-id="dc3ec-139">500</span></span>                       |
| <span data-ttu-id="dc3ec-140">Aprīlī</span><span class="sxs-lookup"><span data-stu-id="dc3ec-140">April</span></span>                | <span data-ttu-id="dc3ec-141">750</span><span class="sxs-lookup"><span data-stu-id="dc3ec-141">750</span></span>                       |
| <span data-ttu-id="dc3ec-142">Maijs – decembris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-142">May through December</span></span> | <span data-ttu-id="dc3ec-143">1000</span><span class="sxs-lookup"><span data-stu-id="dc3ec-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="dc3ec-144">2. piemērs. Transakciju samazināšanas principa prognozes samazināšanas princips</span><span class="sxs-lookup"><span data-stu-id="dc3ec-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="dc3ec-145">Šis piemērs parāda, kā faktiskie pasūtījumi, ko samazināšanas princips noteicis noteiktos periodos, samazina pieprasījuma apjoma prognozes vajadzības.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="dc3ec-146">Lapas **Vispārējie plāni** laukā **Samazināšanas princips** atlasiet **Transakcijas — samazināšanas princips**.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="dc3ec-147">Šādi pārdošanas pasūtījumi ir 1. janvārī.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="dc3ec-148">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="dc3ec-148">Month</span></span>    | <span data-ttu-id="dc3ec-149">Pasūtīto gabalu skaits</span><span class="sxs-lookup"><span data-stu-id="dc3ec-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="dc3ec-150">janvāris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-150">January</span></span>  | <span data-ttu-id="dc3ec-151">956</span><span class="sxs-lookup"><span data-stu-id="dc3ec-151">956</span></span>                      |
| <span data-ttu-id="dc3ec-152">Februārī</span><span class="sxs-lookup"><span data-stu-id="dc3ec-152">February</span></span> | <span data-ttu-id="dc3ec-153">1176</span><span class="sxs-lookup"><span data-stu-id="dc3ec-153">1,176</span></span>                    |
| <span data-ttu-id="dc3ec-154">Martā</span><span class="sxs-lookup"><span data-stu-id="dc3ec-154">March</span></span>    | <span data-ttu-id="dc3ec-155">451</span><span class="sxs-lookup"><span data-stu-id="dc3ec-155">451</span></span>                      |
| <span data-ttu-id="dc3ec-156">Aprīlī</span><span class="sxs-lookup"><span data-stu-id="dc3ec-156">April</span></span>    | <span data-ttu-id="dc3ec-157">119</span><span class="sxs-lookup"><span data-stu-id="dc3ec-157">119</span></span>                      |

<span data-ttu-id="dc3ec-158">Ja izmantojat to pašu pieprasījuma apjoma prognozi 1000 gabaliem mēnesī, uz vispārējo plānu tiek pārsūtīti šādi vajadzību daudzumi.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="dc3ec-159">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="dc3ec-159">Month</span></span>                | <span data-ttu-id="dc3ec-160">Vajadzīgo gabalu skaits</span><span class="sxs-lookup"><span data-stu-id="dc3ec-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="dc3ec-161">janvāris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-161">January</span></span>              | <span data-ttu-id="dc3ec-162">44</span><span class="sxs-lookup"><span data-stu-id="dc3ec-162">44</span></span>                        |
| <span data-ttu-id="dc3ec-163">Februārī</span><span class="sxs-lookup"><span data-stu-id="dc3ec-163">February</span></span>             | <span data-ttu-id="dc3ec-164">0</span><span class="sxs-lookup"><span data-stu-id="dc3ec-164">0</span></span>                         |
| <span data-ttu-id="dc3ec-165">Martā</span><span class="sxs-lookup"><span data-stu-id="dc3ec-165">March</span></span>                | <span data-ttu-id="dc3ec-166">549</span><span class="sxs-lookup"><span data-stu-id="dc3ec-166">549</span></span>                       |
| <span data-ttu-id="dc3ec-167">Aprīlī</span><span class="sxs-lookup"><span data-stu-id="dc3ec-167">April</span></span>                | <span data-ttu-id="dc3ec-168">881</span><span class="sxs-lookup"><span data-stu-id="dc3ec-168">881</span></span>                       |
| <span data-ttu-id="dc3ec-169">Maijs – decembris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-169">May through December</span></span> | <span data-ttu-id="dc3ec-170">1000</span><span class="sxs-lookup"><span data-stu-id="dc3ec-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="dc3ec-171">3. piemērs:. Transakciju dinamiskā perioda prognozes samazināšanas princips</span><span class="sxs-lookup"><span data-stu-id="dc3ec-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="dc3ec-172">Vairāmā gadījumu sistēmas ir iestatītas tā, lai darbības samazina pieprasījuma apjoma prognozi noteiktos prognozes periodos: nedēļās, mēnešus utt.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="dc3ec-173">Šie periodi ir definēti samazināšanas principā.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="dc3ec-174">Tomēr laiks starp divām pieprasījuma apjoma prognozes rindām var arī *nozīmēt* periodu.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1.  <span data-ttu-id="dc3ec-175">Izveidojiet pieprasījuma apjoma prognozi šādiem datumiem un daudzumiem.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-175">Create a demand forecast for the following dates and quantities.</span></span>
    | <span data-ttu-id="dc3ec-176">Datums</span><span class="sxs-lookup"><span data-stu-id="dc3ec-176">Date</span></span>       | <span data-ttu-id="dc3ec-177">Pieprasījuma apjoma prognoze</span><span class="sxs-lookup"><span data-stu-id="dc3ec-177">Demand forecast</span></span> |
    |------------|-----------------|
    | <span data-ttu-id="dc3ec-178">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-178">January 1</span></span>  | <span data-ttu-id="dc3ec-179">1000</span><span class="sxs-lookup"><span data-stu-id="dc3ec-179">1,000</span></span>           |
    | <span data-ttu-id="dc3ec-180">5. janvāris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-180">January 5</span></span>  | <span data-ttu-id="dc3ec-181">500</span><span class="sxs-lookup"><span data-stu-id="dc3ec-181">500</span></span>             |
    | <span data-ttu-id="dc3ec-182">12. janvāris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-182">January 12</span></span> | <span data-ttu-id="dc3ec-183">1000</span><span class="sxs-lookup"><span data-stu-id="dc3ec-183">1,000</span></span>           |

    <span data-ttu-id="dc3ec-184">Šajā prognozē nav skaidri izteikta perioda starp prognozes datumiem: starp pirmo un otro datumu ir četru dienu ilgs posms, un starp otro un trešo datumu ir septiņu ilgs dienu posms.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="dc3ec-185">Šie dažādie posmi ir dinamiskais periods.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-185">These various spans are the dynamic periods.</span></span>
2.  <span data-ttu-id="dc3ec-186">Izveidojiet pārdošanas pasūtījuma rindas, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-186">Create sales order lines as follows.</span></span>
    | <span data-ttu-id="dc3ec-187">Datums</span><span class="sxs-lookup"><span data-stu-id="dc3ec-187">Date</span></span>                             | <span data-ttu-id="dc3ec-188">Pārdošanas pasūtījumu daudzums</span><span class="sxs-lookup"><span data-stu-id="dc3ec-188">Sales order quantity</span></span> |
    |----------------------------------|----------------------|
    | <span data-ttu-id="dc3ec-189">Iepriekšējā gada 15. decembris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-189">December 15 in the previous year</span></span> | <span data-ttu-id="dc3ec-190">500</span><span class="sxs-lookup"><span data-stu-id="dc3ec-190">500</span></span>                  |
    | <span data-ttu-id="dc3ec-191">3. janvāris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-191">January 3</span></span>                        | <span data-ttu-id="dc3ec-192">100</span><span class="sxs-lookup"><span data-stu-id="dc3ec-192">100</span></span>                  |
    | <span data-ttu-id="dc3ec-193">10. janvāris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-193">January 10</span></span>                       | <span data-ttu-id="dc3ec-194">200</span><span class="sxs-lookup"><span data-stu-id="dc3ec-194">200</span></span>                  |

<span data-ttu-id="dc3ec-195">Prognoze tiks samazināta šādi.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="dc3ec-196">Pirmais pārdošanas pasūtījums nav nevienā periodā, tādēļ tas nesamazinās nevienu prognozi.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="dc3ec-197">Otrais pārdošanas pasūtījums ir no 1. līdz 5. janvārim, tāpēc prognoze tiks samazināta 1. janvārī par 100.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="dc3ec-198">Trešais pārdošanas pasūtījums ir no 5. līdz 12. janvārim, tāpēc prognoze tiks samazināta 5. janvārī par 200.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="dc3ec-199">Lai izpildītu prognozi, tiks izveidots šāds plānotais pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="dc3ec-200">Pieprasījuma apjoma prognozes datums</span><span class="sxs-lookup"><span data-stu-id="dc3ec-200">Demand forecast date</span></span> | <span data-ttu-id="dc3ec-201">Samazināts daudzums</span><span class="sxs-lookup"><span data-stu-id="dc3ec-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="dc3ec-202">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-202">January 1</span></span>            | <span data-ttu-id="dc3ec-203">900</span><span class="sxs-lookup"><span data-stu-id="dc3ec-203">900</span></span>              |
| <span data-ttu-id="dc3ec-204">5. janvāris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-204">January 5</span></span>            | <span data-ttu-id="dc3ec-205">300</span><span class="sxs-lookup"><span data-stu-id="dc3ec-205">300</span></span>              |
| <span data-ttu-id="dc3ec-206">12. janvāris</span><span class="sxs-lookup"><span data-stu-id="dc3ec-206">January 12</span></span>           | <span data-ttu-id="dc3ec-207">1000</span><span class="sxs-lookup"><span data-stu-id="dc3ec-207">1,000</span></span>            |

<span data-ttu-id="dc3ec-208">Kopsavilkums par **Transakcijas — dinamiskais periods** samazinājumu:</span><span class="sxs-lookup"><span data-stu-id="dc3ec-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="dc3ec-209">Prognozes vajadzības samazina faktisko pasūtījumu darbības, kas tiek veiktas dinamiskajā periodā.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="dc3ec-210">Dinamiskais periods attiecas uz pašreizējiem prognozes datumiem un beidzas nākamās prognozes sākumā.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="dc3ec-211">Šī metode neizmanto un nepieprasa samazināšanas principu.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="dc3ec-212">Izmantojot šo opciju, notiek šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="dc3ec-213">Ja prognoze ir pilnībā samazināta, prognozes vajadzības pašreizējai prognozei ir 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="dc3ec-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="dc3ec-214">Ja nav nevienas turpmākas prognozes, tiek samazinātas prognozes vajadzības no pēdējās ievadītās prognozes.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="dc3ec-215">Prognozes samazināšanas aprēķinā tiek iekļauti laika periodi.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="dc3ec-216">Prognozes samazināšanas aprēķinā tiek iekļautas dienas(+).</span><span class="sxs-lookup"><span data-stu-id="dc3ec-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="dc3ec-217">Ja faktiskā pasūtījuma transakcijas pārsniedz prognozes vajadzības, atlikušās transakcijas netiek pārsūtītas uz nākamo prognozes periodu.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="see-also"></a><span data-ttu-id="dc3ec-218">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="dc3ec-218">See also</span></span>
--------

[<span data-ttu-id="dc3ec-219">Vispārējie plāni</span><span class="sxs-lookup"><span data-stu-id="dc3ec-219">Master plans</span></span>](master-plans.md)




