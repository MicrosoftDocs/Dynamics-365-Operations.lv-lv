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
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25a90a137ea3f6dfa43f401354780d99b2fda8fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978490"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="efda3-104">Apgrozījuma bilances finanšu pārskati</span><span class="sxs-lookup"><span data-stu-id="efda3-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="efda3-105">Šajā rakstā ir aprakstīti noklusējuma pārskati apgrozījuma bilancēm.</span><span class="sxs-lookup"><span data-stu-id="efda3-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="efda3-106">Tajā ir aprakstīti arī ar šiem pārskatiem saistītie veidošanas bloki un veids, kā šos pārskatus varat modificēt, lai tie atbilstu jūsu biznesa prasībām.</span><span class="sxs-lookup"><span data-stu-id="efda3-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="efda3-107">Noklusējuma apgrozījuma bilances pārskati</span><span class="sxs-lookup"><span data-stu-id="efda3-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="efda3-108">Finanšu pārskatu veidošanas vidē pieejami trīs apgrozījuma bilances pārskati.</span><span class="sxs-lookup"><span data-stu-id="efda3-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="efda3-109">Noklusējuma pārskats</span><span class="sxs-lookup"><span data-stu-id="efda3-109">Default report</span></span>                                 | <span data-ttu-id="efda3-110">Ko tā dara</span><span class="sxs-lookup"><span data-stu-id="efda3-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efda3-111">Detalizēta apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="efda3-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="efda3-112">Sniedz informāciju par bilanci visiem kontiem un iekļauj debeta un kredīta bilances, kā arī šo bilanču neto summu kopā ar transakcijas datumu, dokumentu un žurnāla aprakstu.</span><span class="sxs-lookup"><span data-stu-id="efda3-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="efda3-113">Kopsavilkuma apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="efda3-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="efda3-114">Sniedz bilances informāciju visiem kontiem un iekļauj sākuma un beigu bilances, kā arī debeta un kredīta bilances kopā ar to neto starpību.</span><span class="sxs-lookup"><span data-stu-id="efda3-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="efda3-115">Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums</span><span class="sxs-lookup"><span data-stu-id="efda3-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="efda3-116">Sniedz bilances informāciju visiem kontiem, un iekļauj sākuma un beigu bilances, kā arī debeta un kredīta bilances kopā ar to neto starpību attiecībā uz pašreizējo gadu un iepriekšējo gadu.</span><span class="sxs-lookup"><span data-stu-id="efda3-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="efda3-117">Veidošanas bloki</span><span class="sxs-lookup"><span data-stu-id="efda3-117">Building blocks</span></span>
<span data-ttu-id="efda3-118">Apgrozījuma bilances finanšu pārskati izmanto tālāk aprakstītos veidošanas blokus.</span><span class="sxs-lookup"><span data-stu-id="efda3-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="efda3-119">Noklusējuma atskaite</span><span class="sxs-lookup"><span data-stu-id="efda3-119">Default report</span></span>                                 | <span data-ttu-id="efda3-120">Rindas definīcija</span><span class="sxs-lookup"><span data-stu-id="efda3-120">Row definition</span></span>          | <span data-ttu-id="efda3-121">Kolonnas definīcija</span><span class="sxs-lookup"><span data-stu-id="efda3-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="efda3-122">Detalizēta apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="efda3-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="efda3-123">Apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="efda3-123">Trial Balance - Default</span></span> | <span data-ttu-id="efda3-124">Detalizēta apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="efda3-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="efda3-125">Kopsavilkuma apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="efda3-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="efda3-126">Apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="efda3-126">Trial Balance - Default</span></span> | <span data-ttu-id="efda3-127">Kopsavilkuma apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="efda3-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="efda3-128">Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums</span><span class="sxs-lookup"><span data-stu-id="efda3-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="efda3-129">Apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="efda3-129">Trial Balance - Default</span></span> | <span data-ttu-id="efda3-130">Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums</span><span class="sxs-lookup"><span data-stu-id="efda3-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="efda3-131">Rindas definīcija</span><span class="sxs-lookup"><span data-stu-id="efda3-131">Row definition</span></span>

<span data-ttu-id="efda3-132">Rindas definīcija, Apgrozījuma bilance – Noklusējums, ietver vienu rindu, kas apkopo datus no visiem galvenajiem kontiem.</span><span class="sxs-lookup"><span data-stu-id="efda3-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="efda3-133">Tāpēc ikviens var ģenerēt pārskatu bez nepieciešamības veikt modifikācijas.</span><span class="sxs-lookup"><span data-stu-id="efda3-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="efda3-134">Kad apskatāt atskaiti, detalizējiet vienu rindu, lai apskatītu detalizētu informāciju par katru kontu.</span><span class="sxs-lookup"><span data-stu-id="efda3-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="efda3-135">Rindas definīciju varat modificēt, lai iekļautu vairāk informācijas.</span><span class="sxs-lookup"><span data-stu-id="efda3-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="efda3-136">Lai modificētu rindas definīciju "apgrozījuma bilance — noklusējuma" un iekļautu rindas visiem kontiem, rīkojieties kā aprakstīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="efda3-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="efda3-137">Noklikšķiniet uz **Rediģēšana** un tad noklikšķiniet uz **Ievietot rindas no dimensijām**.</span><span class="sxs-lookup"><span data-stu-id="efda3-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="efda3-138">Komanda **Ievietot rindas no dimensijām** ļauj izvēlēties, kuras dimensijas vēlaties iekļaut rindas definīcijā.</span><span class="sxs-lookup"><span data-stu-id="efda3-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="efda3-139">Šai rindas definīcijai izmantojiet **Galvenais konts**.</span><span class="sxs-lookup"><span data-stu-id="efda3-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="efda3-140">Pārliecinieties, vai sadaļā **Galvenais konts** ir iekļautas visas rakstzīmes "&", un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="efda3-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="efda3-141">Tagad rindas definīcija satur visus noklusējuma juridiskās personas galvenos kontus.</span><span class="sxs-lookup"><span data-stu-id="efda3-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="efda3-142">Kolonnas definīcija</span><span class="sxs-lookup"><span data-stu-id="efda3-142">Column definition</span></span>

<span data-ttu-id="efda3-143">Katrā apgrozījuma bilances pārskatā izmantota cita kolonnas definīcija.</span><span class="sxs-lookup"><span data-stu-id="efda3-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="efda3-144">Šīs kolonnu definīcijas satur dažādu veidu kolonnas, lai sniegtu dažāda līmeņa detaļas un finanšu datus.</span><span class="sxs-lookup"><span data-stu-id="efda3-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="efda3-145">**Detalizēta apgrozījuma bilance — noklusējuma kolonnu tipi**</span><span class="sxs-lookup"><span data-stu-id="efda3-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="efda3-146">**DESC** — apraksts no rindas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="efda3-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="efda3-147">**ACCT** — kontu kodi.</span><span class="sxs-lookup"><span data-stu-id="efda3-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="efda3-148">**ATTR (3)** — atribūti:</span><span class="sxs-lookup"><span data-stu-id="efda3-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="efda3-149">Transakcijas datums</span><span class="sxs-lookup"><span data-stu-id="efda3-149">Transaction Date</span></span>
        -   <span data-ttu-id="efda3-150">Dokuments</span><span class="sxs-lookup"><span data-stu-id="efda3-150">Voucher</span></span>
        -   <span data-ttu-id="efda3-151">Žurnāla apraksts</span><span class="sxs-lookup"><span data-stu-id="efda3-151">Journal Description</span></span>
    -   <span data-ttu-id="efda3-152">**FD** — finanšu dati, kas satur tikai debetu.</span><span class="sxs-lookup"><span data-stu-id="efda3-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="efda3-153">**FD** — finanšu dati, kas satur tikai kredītu.</span><span class="sxs-lookup"><span data-stu-id="efda3-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="efda3-154">**CALC** — neto starpība.</span><span class="sxs-lookup"><span data-stu-id="efda3-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="efda3-155">**Kopsavilkuma apgrozījuma bilance — noklusējuma kolonnu tipi**</span><span class="sxs-lookup"><span data-stu-id="efda3-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="efda3-156">**ACCT** — kontu kodi.</span><span class="sxs-lookup"><span data-stu-id="efda3-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="efda3-157">**DESC** — apraksts no rindas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="efda3-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="efda3-158">**ATTR** — atribūts:</span><span class="sxs-lookup"><span data-stu-id="efda3-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="efda3-159">Dokuments</span><span class="sxs-lookup"><span data-stu-id="efda3-159">Voucher</span></span>
    -   <span data-ttu-id="efda3-160">**FD** — sākuma bilances finanšu dati.</span><span class="sxs-lookup"><span data-stu-id="efda3-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="efda3-161">**FD** — finanšu dati, kas satur tikai debetu.</span><span class="sxs-lookup"><span data-stu-id="efda3-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="efda3-162">**FD** — finanšu dati, kas satur tikai kredītu.</span><span class="sxs-lookup"><span data-stu-id="efda3-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="efda3-163">**CALC** — neto starpība.</span><span class="sxs-lookup"><span data-stu-id="efda3-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="efda3-164">**CALC** — beigu atlikums.</span><span class="sxs-lookup"><span data-stu-id="efda3-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="efda3-165">**Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums**</span><span class="sxs-lookup"><span data-stu-id="efda3-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="efda3-166">**ACCT** — kontu kodi.</span><span class="sxs-lookup"><span data-stu-id="efda3-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="efda3-167">**DESC** — apraksts no rindas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="efda3-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="efda3-168">**ATTR** — atribūts:</span><span class="sxs-lookup"><span data-stu-id="efda3-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="efda3-169">Dokuments</span><span class="sxs-lookup"><span data-stu-id="efda3-169">Voucher</span></span>
    -   <span data-ttu-id="efda3-170">**FD** — sākuma bilances finanšu dati pašreizējam gadam.</span><span class="sxs-lookup"><span data-stu-id="efda3-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="efda3-171">**FD** — finanšu dati, kas satur tikai debetu pašreizējam gadam.</span><span class="sxs-lookup"><span data-stu-id="efda3-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="efda3-172">**FD** — finanšu dati, kas satur tikai kredītu pašreizējam gadam.</span><span class="sxs-lookup"><span data-stu-id="efda3-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="efda3-173">**CALC** — neto starpība.</span><span class="sxs-lookup"><span data-stu-id="efda3-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="efda3-174">**CALC** — beigu atlikums.</span><span class="sxs-lookup"><span data-stu-id="efda3-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="efda3-175">**FD** — finanšu dati, kas satur tikai debetu pagājušajam gadam.</span><span class="sxs-lookup"><span data-stu-id="efda3-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="efda3-176">**FD** — finanšu dati, kas satur tikai kredītu pagājušajam gadam.</span><span class="sxs-lookup"><span data-stu-id="efda3-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="efda3-177">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="efda3-177">Additional resources</span></span>
--------

[<span data-ttu-id="efda3-178">Finanšu pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="efda3-178">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="efda3-179">Finanšu pārskatu skatīšana</span><span class="sxs-lookup"><span data-stu-id="efda3-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="efda3-180">Dynamics finanšu pārskatu veidošanas emuārs</span><span class="sxs-lookup"><span data-stu-id="efda3-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



