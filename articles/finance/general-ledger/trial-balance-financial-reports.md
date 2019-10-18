---
title: Apgrozījuma bilances finanšu pārskati
description: Šajā rakstā ir aprakstīti noklusējuma pārskati apgrozījuma bilancēm. Tajā ir aprakstīti arī ar šiem pārskatiem saistītie veidošanas bloki un veids, kā šos pārskatus varat modificēt, lai tie atbilstu jūsu biznesa prasībām.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fd4512b02070415b6228c91b66635815dbacaa2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175521"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="2937a-104">Apgrozījuma bilances finanšu pārskati</span><span class="sxs-lookup"><span data-stu-id="2937a-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2937a-105">Šajā rakstā ir aprakstīti noklusējuma pārskati apgrozījuma bilancēm.</span><span class="sxs-lookup"><span data-stu-id="2937a-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="2937a-106">Tajā ir aprakstīti arī ar šiem pārskatiem saistītie veidošanas bloki un veids, kā šos pārskatus varat modificēt, lai tie atbilstu jūsu biznesa prasībām.</span><span class="sxs-lookup"><span data-stu-id="2937a-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="2937a-107">Noklusējuma apgrozījuma bilances pārskati</span><span class="sxs-lookup"><span data-stu-id="2937a-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="2937a-108">Finanšu pārskatu veidošanas vidē pieejami trīs apgrozījuma bilances pārskati.</span><span class="sxs-lookup"><span data-stu-id="2937a-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="2937a-109">Noklusējuma pārskats</span><span class="sxs-lookup"><span data-stu-id="2937a-109">Default report</span></span>                                 | <span data-ttu-id="2937a-110">Ko tā dara</span><span class="sxs-lookup"><span data-stu-id="2937a-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2937a-111">Detalizēta apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="2937a-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="2937a-112">Sniedz informāciju par bilanci visiem kontiem un iekļauj debeta un kredīta bilances, kā arī šo bilanču neto summu kopā ar transakcijas datumu, dokumentu un žurnāla aprakstu.</span><span class="sxs-lookup"><span data-stu-id="2937a-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="2937a-113">Kopsavilkuma apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="2937a-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="2937a-114">Sniedz bilances informāciju visiem kontiem un iekļauj sākuma un beigu bilances, kā arī debeta un kredīta bilances kopā ar to neto starpību.</span><span class="sxs-lookup"><span data-stu-id="2937a-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="2937a-115">Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums</span><span class="sxs-lookup"><span data-stu-id="2937a-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="2937a-116">Sniedz bilances informāciju visiem kontiem, un iekļauj sākuma un beigu bilances, kā arī debeta un kredīta bilances kopā ar to neto starpību attiecībā uz pašreizējo gadu un iepriekšējo gadu.</span><span class="sxs-lookup"><span data-stu-id="2937a-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="2937a-117">Veidošanas bloki</span><span class="sxs-lookup"><span data-stu-id="2937a-117">Building blocks</span></span>
<span data-ttu-id="2937a-118">Apgrozījuma bilances finanšu pārskati izmanto tālāk aprakstītos veidošanas blokus.</span><span class="sxs-lookup"><span data-stu-id="2937a-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="2937a-119">Noklusējuma atskaite</span><span class="sxs-lookup"><span data-stu-id="2937a-119">Default report</span></span>                                 | <span data-ttu-id="2937a-120">Rindas definīcija</span><span class="sxs-lookup"><span data-stu-id="2937a-120">Row definition</span></span>          | <span data-ttu-id="2937a-121">Kolonnas definīcija</span><span class="sxs-lookup"><span data-stu-id="2937a-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="2937a-122">Detalizēta apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="2937a-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="2937a-123">Apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="2937a-123">Trial Balance - Default</span></span> | <span data-ttu-id="2937a-124">Detalizēta apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="2937a-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="2937a-125">Kopsavilkuma apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="2937a-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="2937a-126">Apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="2937a-126">Trial Balance - Default</span></span> | <span data-ttu-id="2937a-127">Kopsavilkuma apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="2937a-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="2937a-128">Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums</span><span class="sxs-lookup"><span data-stu-id="2937a-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="2937a-129">Apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="2937a-129">Trial Balance - Default</span></span> | <span data-ttu-id="2937a-130">Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums</span><span class="sxs-lookup"><span data-stu-id="2937a-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="2937a-131">Rindas definīcija</span><span class="sxs-lookup"><span data-stu-id="2937a-131">Row definition</span></span>

<span data-ttu-id="2937a-132">Rindas definīcija, Apgrozījuma bilance – Noklusējums, ietver vienu rindu, kas apkopo datus no visiem galvenajiem kontiem.</span><span class="sxs-lookup"><span data-stu-id="2937a-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="2937a-133">Tāpēc ikviens var ģenerēt pārskatu bez nepieciešamības veikt modifikācijas.</span><span class="sxs-lookup"><span data-stu-id="2937a-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="2937a-134">Kad apskatāt atskaiti, detalizējiet vienu rindu, lai apskatītu detalizētu informāciju par katru kontu.</span><span class="sxs-lookup"><span data-stu-id="2937a-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="2937a-135">Rindas definīciju varat modificēt, lai iekļautu vairāk informācijas.</span><span class="sxs-lookup"><span data-stu-id="2937a-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="2937a-136">Lai modificētu rindas definīciju "apgrozījuma bilance — noklusējuma" un iekļautu rindas visiem kontiem, rīkojieties kā aprakstīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="2937a-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="2937a-137">Noklikšķiniet uz **Rediģēšana** un tad noklikšķiniet uz **Ievietot rindas no dimensijām**.</span><span class="sxs-lookup"><span data-stu-id="2937a-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="2937a-138">Komanda **Ievietot rindas no dimensijām** ļauj izvēlēties, kuras dimensijas vēlaties iekļaut rindas definīcijā.</span><span class="sxs-lookup"><span data-stu-id="2937a-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="2937a-139">Šai rindas definīcijai izmantojiet **Galvenais konts**.</span><span class="sxs-lookup"><span data-stu-id="2937a-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="2937a-140">Pārliecinieties, vai sadaļā **Galvenais konts** ir iekļautas visas rakstzīmes "&", un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2937a-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="2937a-141">Tagad rindas definīcija satur visus noklusējuma juridiskās personas galvenos kontus.</span><span class="sxs-lookup"><span data-stu-id="2937a-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="2937a-142">Kolonnas definīcija</span><span class="sxs-lookup"><span data-stu-id="2937a-142">Column definition</span></span>

<span data-ttu-id="2937a-143">Katrā apgrozījuma bilances pārskatā izmantota cita kolonnas definīcija.</span><span class="sxs-lookup"><span data-stu-id="2937a-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="2937a-144">Šīs kolonnu definīcijas satur dažādu veidu kolonnas, lai sniegtu dažāda līmeņa detaļas un finanšu datus.</span><span class="sxs-lookup"><span data-stu-id="2937a-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="2937a-145">**Detalizēta apgrozījuma bilance — noklusējuma kolonnu tipi**</span><span class="sxs-lookup"><span data-stu-id="2937a-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="2937a-146">**DESC** — apraksts no rindas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="2937a-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="2937a-147">**ACCT** — kontu kodi.</span><span class="sxs-lookup"><span data-stu-id="2937a-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="2937a-148">**ATTR (3)** — atribūti:</span><span class="sxs-lookup"><span data-stu-id="2937a-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="2937a-149">Transakcijas datums</span><span class="sxs-lookup"><span data-stu-id="2937a-149">Transaction Date</span></span>
        -   <span data-ttu-id="2937a-150">Dokuments</span><span class="sxs-lookup"><span data-stu-id="2937a-150">Voucher</span></span>
        -   <span data-ttu-id="2937a-151">Žurnāla apraksts</span><span class="sxs-lookup"><span data-stu-id="2937a-151">Journal Description</span></span>
    -   <span data-ttu-id="2937a-152">**FD** — finanšu dati, kas satur tikai debetu.</span><span class="sxs-lookup"><span data-stu-id="2937a-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="2937a-153">**FD** — finanšu dati, kas satur tikai kredītu.</span><span class="sxs-lookup"><span data-stu-id="2937a-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="2937a-154">**CALC** — neto starpība.</span><span class="sxs-lookup"><span data-stu-id="2937a-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="2937a-155">**Kopsavilkuma apgrozījuma bilance — noklusējuma kolonnu tipi**</span><span class="sxs-lookup"><span data-stu-id="2937a-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="2937a-156">**ACCT** — kontu kodi.</span><span class="sxs-lookup"><span data-stu-id="2937a-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="2937a-157">**DESC** — apraksts no rindas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="2937a-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="2937a-158">**ATTR** — atribūts:</span><span class="sxs-lookup"><span data-stu-id="2937a-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="2937a-159">Dokuments</span><span class="sxs-lookup"><span data-stu-id="2937a-159">Voucher</span></span>
    -   <span data-ttu-id="2937a-160">**FD** — sākuma bilances finanšu dati.</span><span class="sxs-lookup"><span data-stu-id="2937a-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="2937a-161">**FD** — finanšu dati, kas satur tikai debetu.</span><span class="sxs-lookup"><span data-stu-id="2937a-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="2937a-162">**FD** — finanšu dati, kas satur tikai kredītu.</span><span class="sxs-lookup"><span data-stu-id="2937a-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="2937a-163">**CALC** — neto starpība.</span><span class="sxs-lookup"><span data-stu-id="2937a-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="2937a-164">**CALC** — beigu atlikums.</span><span class="sxs-lookup"><span data-stu-id="2937a-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="2937a-165">**Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums**</span><span class="sxs-lookup"><span data-stu-id="2937a-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="2937a-166">**ACCT** — kontu kodi.</span><span class="sxs-lookup"><span data-stu-id="2937a-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="2937a-167">**DESC** — apraksts no rindas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="2937a-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="2937a-168">**ATTR** — atribūts:</span><span class="sxs-lookup"><span data-stu-id="2937a-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="2937a-169">Dokuments</span><span class="sxs-lookup"><span data-stu-id="2937a-169">Voucher</span></span>
    -   <span data-ttu-id="2937a-170">**FD** — sākuma bilances finanšu dati pašreizējam gadam.</span><span class="sxs-lookup"><span data-stu-id="2937a-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="2937a-171">**FD** — finanšu dati, kas satur tikai debetu pašreizējam gadam.</span><span class="sxs-lookup"><span data-stu-id="2937a-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="2937a-172">**FD** — finanšu dati, kas satur tikai kredītu pašreizējam gadam.</span><span class="sxs-lookup"><span data-stu-id="2937a-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="2937a-173">**CALC** — neto starpība.</span><span class="sxs-lookup"><span data-stu-id="2937a-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="2937a-174">**CALC** — beigu atlikums.</span><span class="sxs-lookup"><span data-stu-id="2937a-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="2937a-175">**FD** — finanšu dati, kas satur tikai debetu pagājušajam gadam.</span><span class="sxs-lookup"><span data-stu-id="2937a-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="2937a-176">**FD** — finanšu dati, kas satur tikai kredītu pagājušajam gadam.</span><span class="sxs-lookup"><span data-stu-id="2937a-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="2937a-177">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2937a-177">Additional resources</span></span>
--------

[<span data-ttu-id="2937a-178">Finanšu pārskati</span><span class="sxs-lookup"><span data-stu-id="2937a-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="2937a-179">Skatīt finanšu pārskatus</span><span class="sxs-lookup"><span data-stu-id="2937a-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="2937a-180">Dynamics finanšu pārskatu veidošanas emuārs</span><span class="sxs-lookup"><span data-stu-id="2937a-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



