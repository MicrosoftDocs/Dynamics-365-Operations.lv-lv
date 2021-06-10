---
title: Apgrozījuma bilances finanšu pārskati
description: Šajā rakstā ir aprakstīti noklusējuma pārskati apgrozījuma bilancēm. Tajā ir aprakstīti arī ar šiem pārskatiem saistītie veidošanas bloki un veids, kā šos pārskatus varat modificēt, lai tie atbilstu jūsu biznesa prasībām.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 26ec03422315a280f7e779f992cf694eb5f845ea
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103662"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="1a8a0-104">Apgrozījuma bilances finanšu pārskati</span><span class="sxs-lookup"><span data-stu-id="1a8a0-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a8a0-105">Šajā rakstā ir aprakstīti noklusējuma pārskati apgrozījuma bilancēm.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="1a8a0-106">Tajā ir aprakstīti arī ar šiem pārskatiem saistītie veidošanas bloki un veids, kā šos pārskatus varat modificēt, lai tie atbilstu jūsu biznesa prasībām.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

## <a name="default-trial-balance-reports"></a><span data-ttu-id="1a8a0-107">Noklusējuma apgrozījuma bilances pārskati</span><span class="sxs-lookup"><span data-stu-id="1a8a0-107">Default trial balance reports</span></span>

<span data-ttu-id="1a8a0-108">Finanšu pārskatu veidošanas vidē pieejami trīs apgrozījuma bilances pārskati.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="1a8a0-109">Noklusējuma pārskats</span><span class="sxs-lookup"><span data-stu-id="1a8a0-109">Default report</span></span>                                 | <span data-ttu-id="1a8a0-110">Ko tā dara</span><span class="sxs-lookup"><span data-stu-id="1a8a0-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a8a0-111">Detalizēta apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="1a8a0-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="1a8a0-112">Sniedz informāciju par bilanci visiem kontiem un iekļauj debeta un kredīta bilances, kā arī šo bilanču neto summu kopā ar transakcijas datumu, dokumentu un žurnāla aprakstu.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="1a8a0-113">Kopsavilkuma apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="1a8a0-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="1a8a0-114">Sniedz bilances informāciju visiem kontiem un iekļauj sākuma un beigu bilances, kā arī debeta un kredīta bilances kopā ar to neto starpību.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="1a8a0-115">Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums</span><span class="sxs-lookup"><span data-stu-id="1a8a0-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="1a8a0-116">Sniedz bilances informāciju visiem kontiem, un iekļauj sākuma un beigu bilances, kā arī debeta un kredīta bilances kopā ar to neto starpību attiecībā uz pašreizējo gadu un iepriekšējo gadu.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="1a8a0-117">Veidošanas bloki</span><span class="sxs-lookup"><span data-stu-id="1a8a0-117">Building blocks</span></span>
<span data-ttu-id="1a8a0-118">Apgrozījuma bilances finanšu pārskati izmanto tālāk aprakstītos veidošanas blokus.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="1a8a0-119">Noklusējuma atskaite</span><span class="sxs-lookup"><span data-stu-id="1a8a0-119">Default report</span></span>                                 | <span data-ttu-id="1a8a0-120">Rindas definīcija</span><span class="sxs-lookup"><span data-stu-id="1a8a0-120">Row definition</span></span>          | <span data-ttu-id="1a8a0-121">Kolonnas definīcija</span><span class="sxs-lookup"><span data-stu-id="1a8a0-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="1a8a0-122">Detalizēta apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="1a8a0-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="1a8a0-123">Apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="1a8a0-123">Trial Balance - Default</span></span> | <span data-ttu-id="1a8a0-124">Detalizēta apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="1a8a0-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="1a8a0-125">Kopsavilkuma apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="1a8a0-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="1a8a0-126">Apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="1a8a0-126">Trial Balance - Default</span></span> | <span data-ttu-id="1a8a0-127">Kopsavilkuma apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="1a8a0-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="1a8a0-128">Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums</span><span class="sxs-lookup"><span data-stu-id="1a8a0-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="1a8a0-129">Apgrozījuma bilance — noklusējums</span><span class="sxs-lookup"><span data-stu-id="1a8a0-129">Trial Balance - Default</span></span> | <span data-ttu-id="1a8a0-130">Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums</span><span class="sxs-lookup"><span data-stu-id="1a8a0-130">Summary Trial Balance Year Over Year - Default</span></span> |

> [!NOTE] 
> <span data-ttu-id="1a8a0-131">Palaižot **Apgrozījuma bilances** atskaiti Financial reporting, noteikti atzīmējiet izvēles rūtiņas **Rādīt rindas bez summām** un **Rādīt atskaites bez rindām** cilnē **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-131">When running the **Trial Balance** report in Financial reporting, be sure to select the check boxes for **Display rows with no amounts** and **Display reports with no active rows** on the **Settings** tab.</span></span>

### <a name="row-definition"></a><span data-ttu-id="1a8a0-132">Rindas definīcija</span><span class="sxs-lookup"><span data-stu-id="1a8a0-132">Row definition</span></span>

<span data-ttu-id="1a8a0-133">Rindas definīcija, Apgrozījuma bilance – Noklusējums, ietver vienu rindu, kas apkopo datus no visiem galvenajiem kontiem.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-133">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="1a8a0-134">Tāpēc ikviens var ģenerēt pārskatu bez nepieciešamības veikt modifikācijas.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-134">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="1a8a0-135">Kad apskatāt atskaiti, detalizējiet vienu rindu, lai apskatītu detalizētu informāciju par katru kontu.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-135">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="1a8a0-136">Rindas definīciju varat modificēt, lai iekļautu vairāk informācijas.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-136">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="1a8a0-137">Lai modificētu rindas definīciju "apgrozījuma bilance — noklusējuma" un iekļautu rindas visiem kontiem, rīkojieties kā aprakstīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-137">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="1a8a0-138">Noklikšķiniet uz **Rediģēšana** un tad noklikšķiniet uz **Ievietot rindas no dimensijām**.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-138">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="1a8a0-139">Komanda **Ievietot rindas no dimensijām** ļauj izvēlēties, kuras dimensijas vēlaties iekļaut rindas definīcijā.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-139">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="1a8a0-140">Šai rindas definīcijai izmantojiet **Galvenais konts**.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-140">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="1a8a0-141">Pārliecinieties, vai sadaļā **Galvenais konts** ir iekļautas visas rakstzīmes "&", un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-141">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="1a8a0-142">Tagad rindas definīcija satur visus noklusējuma juridiskās personas galvenos kontus.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-142">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="1a8a0-143">Kolonnas definīcija</span><span class="sxs-lookup"><span data-stu-id="1a8a0-143">Column definition</span></span>

<span data-ttu-id="1a8a0-144">Katrā apgrozījuma bilances pārskatā izmantota cita kolonnas definīcija.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-144">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="1a8a0-145">Šīs kolonnu definīcijas satur dažādu veidu kolonnas, lai sniegtu dažāda līmeņa detaļas un finanšu datus.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-145">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="1a8a0-146">**Detalizēta apgrozījuma bilance — noklusējuma kolonnu tipi**</span><span class="sxs-lookup"><span data-stu-id="1a8a0-146">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="1a8a0-147">**DESC** — apraksts no rindas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-147">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="1a8a0-148">**ACCT** — kontu kodi.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-148">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="1a8a0-149">**ATTR (3)** — atribūti:</span><span class="sxs-lookup"><span data-stu-id="1a8a0-149">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="1a8a0-150">Transakcijas datums</span><span class="sxs-lookup"><span data-stu-id="1a8a0-150">Transaction Date</span></span>
        -   <span data-ttu-id="1a8a0-151">Dokuments</span><span class="sxs-lookup"><span data-stu-id="1a8a0-151">Voucher</span></span>
        -   <span data-ttu-id="1a8a0-152">Žurnāla apraksts</span><span class="sxs-lookup"><span data-stu-id="1a8a0-152">Journal Description</span></span>
    -   <span data-ttu-id="1a8a0-153">**FD** — finanšu dati, kas satur tikai debetu.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-153">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="1a8a0-154">**FD** — finanšu dati, kas satur tikai kredītu.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-154">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="1a8a0-155">**CALC** — neto starpība.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-155">**CALC** – The net difference</span></span>
-   <span data-ttu-id="1a8a0-156">**Kopsavilkuma apgrozījuma bilance — noklusējuma kolonnu tipi**</span><span class="sxs-lookup"><span data-stu-id="1a8a0-156">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="1a8a0-157">**ACCT** — kontu kodi.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-157">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="1a8a0-158">**DESC** — apraksts no rindas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-158">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="1a8a0-159">**ATTR** — atribūts:</span><span class="sxs-lookup"><span data-stu-id="1a8a0-159">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="1a8a0-160">Dokuments</span><span class="sxs-lookup"><span data-stu-id="1a8a0-160">Voucher</span></span>
    -   <span data-ttu-id="1a8a0-161">**FD** — sākuma bilances finanšu dati.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-161">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="1a8a0-162">**FD** — finanšu dati, kas satur tikai debetu.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-162">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="1a8a0-163">**FD** — finanšu dati, kas satur tikai kredītu.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-163">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="1a8a0-164">**CALC** — neto starpība.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-164">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="1a8a0-165">**CALC** — beigu atlikums.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-165">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="1a8a0-166">**Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums**</span><span class="sxs-lookup"><span data-stu-id="1a8a0-166">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="1a8a0-167">**ACCT** — kontu kodi.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-167">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="1a8a0-168">**DESC** — apraksts no rindas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-168">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="1a8a0-169">**ATTR** — atribūts:</span><span class="sxs-lookup"><span data-stu-id="1a8a0-169">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="1a8a0-170">Dokuments</span><span class="sxs-lookup"><span data-stu-id="1a8a0-170">Voucher</span></span>
    -   <span data-ttu-id="1a8a0-171">**FD** — sākuma bilances finanšu dati pašreizējam gadam.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-171">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="1a8a0-172">**FD** — finanšu dati, kas satur tikai debetu pašreizējam gadam.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-172">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="1a8a0-173">**FD** — finanšu dati, kas satur tikai kredītu pašreizējam gadam.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-173">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="1a8a0-174">**CALC** — neto starpība.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-174">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="1a8a0-175">**CALC** — beigu atlikums.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-175">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="1a8a0-176">**FD** — finanšu dati, kas satur tikai debetu pagājušajam gadam.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-176">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="1a8a0-177">**FD** — finanšu dati, kas satur tikai kredītu pagājušajam gadam.</span><span class="sxs-lookup"><span data-stu-id="1a8a0-177">**FD** – Financial data that contains only credits for the last year</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a8a0-178">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1a8a0-178">Additional resources</span></span>

[<span data-ttu-id="1a8a0-179">Finanšu pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="1a8a0-179">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="1a8a0-180">Finanšu pārskatu skatīšana</span><span class="sxs-lookup"><span data-stu-id="1a8a0-180">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="1a8a0-181">Dynamics finanšu pārskatu veidošanas emuārs</span><span class="sxs-lookup"><span data-stu-id="1a8a0-181">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
