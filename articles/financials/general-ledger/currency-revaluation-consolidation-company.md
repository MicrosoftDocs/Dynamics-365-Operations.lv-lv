---
title: "Valūtas pārvērtēšana konsolidācijas uzņēmumā"
description: "Šajā tēmā ir aprakstīts, kā konsolidētā uzņēmumā pārvērtēt valūtu."
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ad0083018d2734cb1e36cbf5f94105376c57cdf9
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.contentlocale: lv-lv
ms.lasthandoff: 10/02/2018

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="be002-103">Valūtas pārvērtēšana konsolidācijas uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="be002-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be002-104">Veicot datu konsolidāciju no vienas norēķinu valūtas uz citu, joprojām jāpalaiž valūtas pārvērtēšana, ja ir izmaiņas valūtas maiņas kursos, lai jūsu konta bilances tiktu pareizi pārvērtētas.</span><span class="sxs-lookup"><span data-stu-id="be002-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="be002-105">Sākotnēji konsolidējot datus, izmantojiet cilni **Valūtas pārrēķināšana**, lai atlasītu sākotnējos maiņas kursus, pārrēķināšanai konsolidācijas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="be002-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="be002-106">Pēc jaunā valūtas maiņas kursa ievadīšanas (piemēram, nākamajā mēnesī), nepieciešams pārvērtēt kontu bilances.</span><span class="sxs-lookup"><span data-stu-id="be002-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="be002-107">Nerealizētā peļņa vai zaudējumi pēc tam tiek attiecīgi atjaunināta, pamatojoties uz jauno valūtas maiņas kursu un datumu.</span><span class="sxs-lookup"><span data-stu-id="be002-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="be002-108">Šajā piemērā tiek parādīti uzskaites ieraksti, kas tiek izveidoti procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="be002-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="be002-109">Uzņēmuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="be002-109">Company setup</span></span>
-   <span data-ttu-id="be002-110">**Avota/strādājošs uzņēmums (USMF)** – ASV dolāri (USD) tiek izmantoti kā uzskaites un pārskata valūta.</span><span class="sxs-lookup"><span data-stu-id="be002-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="be002-111">**Konsolidēts uzņēmums (CON)** – eiro (EUR) tiek izmantoti kā uzskaites un pārskata valūta.</span><span class="sxs-lookup"><span data-stu-id="be002-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="be002-112">**Realizētā peļņa** – Virsgrāmatas konts 801500</span><span class="sxs-lookup"><span data-stu-id="be002-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="be002-113">**Realizētie zaudējumi** – Virsgrāmatas konts 801600</span><span class="sxs-lookup"><span data-stu-id="be002-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="be002-114">**Nerealizētā peļņa** – Virsgrāmatas konts 801600</span><span class="sxs-lookup"><span data-stu-id="be002-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="be002-115">**Nerealizētie zaudējumi** – Virsgrāmatas konts 801400</span><span class="sxs-lookup"><span data-stu-id="be002-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="be002-116">Sākotnējās darbības</span><span class="sxs-lookup"><span data-stu-id="be002-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="be002-117">Kases ieņēmumu darbības USMF</span><span class="sxs-lookup"><span data-stu-id="be002-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="be002-118">Datums</span><span class="sxs-lookup"><span data-stu-id="be002-118">Date</span></span>       | <span data-ttu-id="be002-119">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="be002-119">Ledger account</span></span>               | <span data-ttu-id="be002-120">Valūta</span><span class="sxs-lookup"><span data-stu-id="be002-120">Currency</span></span> | <span data-ttu-id="be002-121">Summa</span><span class="sxs-lookup"><span data-stu-id="be002-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="be002-122">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="be002-122">10/11/2015</span></span> | <span data-ttu-id="be002-123">110110 – Skaidra nauda</span><span class="sxs-lookup"><span data-stu-id="be002-123">110110 – Cash</span></span>                | <span data-ttu-id="be002-124">USD</span><span class="sxs-lookup"><span data-stu-id="be002-124">USD</span></span>      | <span data-ttu-id="be002-125">500</span><span class="sxs-lookup"><span data-stu-id="be002-125">500</span></span>    |
| <span data-ttu-id="be002-126">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="be002-126">10/11/2015</span></span> | <span data-ttu-id="be002-127">130100 – Debitoru parādi</span><span class="sxs-lookup"><span data-stu-id="be002-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="be002-128">USD</span><span class="sxs-lookup"><span data-stu-id="be002-128">USD</span></span>      | <span data-ttu-id="be002-129">-500</span><span class="sxs-lookup"><span data-stu-id="be002-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="be002-130">Valūtu maiņas kursi</span><span class="sxs-lookup"><span data-stu-id="be002-130">Exchange rates</span></span>

| <span data-ttu-id="be002-131">No valūtas</span><span class="sxs-lookup"><span data-stu-id="be002-131">From currency</span></span> | <span data-ttu-id="be002-132">Uz valūtu</span><span class="sxs-lookup"><span data-stu-id="be002-132">To currency</span></span> | <span data-ttu-id="be002-133">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="be002-133">Start date</span></span> | <span data-ttu-id="be002-134">Valūtas kurss</span><span class="sxs-lookup"><span data-stu-id="be002-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="be002-135">EUR</span><span class="sxs-lookup"><span data-stu-id="be002-135">EUR</span></span>           | <span data-ttu-id="be002-136">USD</span><span class="sxs-lookup"><span data-stu-id="be002-136">USD</span></span>         | <span data-ttu-id="be002-137">01.10.2015</span><span class="sxs-lookup"><span data-stu-id="be002-137">10/1/2015</span></span>  | <span data-ttu-id="be002-138">200</span><span class="sxs-lookup"><span data-stu-id="be002-138">200</span></span>           |
| <span data-ttu-id="be002-139">EUR</span><span class="sxs-lookup"><span data-stu-id="be002-139">EUR</span></span>           | <span data-ttu-id="be002-140">USD</span><span class="sxs-lookup"><span data-stu-id="be002-140">USD</span></span>         | <span data-ttu-id="be002-141">01.11.2015</span><span class="sxs-lookup"><span data-stu-id="be002-141">11/1/2015</span></span>  | <span data-ttu-id="be002-142">150</span><span class="sxs-lookup"><span data-stu-id="be002-142">150</span></span>           |
| <span data-ttu-id="be002-143">EUR</span><span class="sxs-lookup"><span data-stu-id="be002-143">EUR</span></span>           | <span data-ttu-id="be002-144">USD</span><span class="sxs-lookup"><span data-stu-id="be002-144">USD</span></span>         | <span data-ttu-id="be002-145">01.12.2012</span><span class="sxs-lookup"><span data-stu-id="be002-145">12/1/2012</span></span>  | <span data-ttu-id="be002-146">100</span><span class="sxs-lookup"><span data-stu-id="be002-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="be002-147">Veikt konsolidāciju par 2015. gada oktobri</span><span class="sxs-lookup"><span data-stu-id="be002-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="be002-148">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="be002-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="be002-149">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="be002-149">Ledger account</span></span> | <span data-ttu-id="be002-150">Valūta</span><span class="sxs-lookup"><span data-stu-id="be002-150">Currency</span></span> | <span data-ttu-id="be002-151">Summa</span><span class="sxs-lookup"><span data-stu-id="be002-151">Amount</span></span> | <span data-ttu-id="be002-152">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="be002-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="be002-153">110110</span><span class="sxs-lookup"><span data-stu-id="be002-153">110110</span></span>         | <span data-ttu-id="be002-154">EUR</span><span class="sxs-lookup"><span data-stu-id="be002-154">EUR</span></span>      | <span data-ttu-id="be002-155">250</span><span class="sxs-lookup"><span data-stu-id="be002-155">250</span></span>    | <span data-ttu-id="be002-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="be002-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="be002-157">130100</span><span class="sxs-lookup"><span data-stu-id="be002-157">130100</span></span>         | <span data-ttu-id="be002-158">EUR</span><span class="sxs-lookup"><span data-stu-id="be002-158">EUR</span></span>      | <span data-ttu-id="be002-159">-250</span><span class="sxs-lookup"><span data-stu-id="be002-159">-250</span></span>   | <span data-ttu-id="be002-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="be002-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="be002-161">Veikt valūtas pārvērtēšanu kontiem no 2015. gada 1. oktobra līdz 2015. gada 30. novembrim</span><span class="sxs-lookup"><span data-stu-id="be002-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="be002-162">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="be002-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="be002-163">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="be002-163">Ledger account</span></span> | <span data-ttu-id="be002-164">Valūta</span><span class="sxs-lookup"><span data-stu-id="be002-164">Currency</span></span> | <span data-ttu-id="be002-165">Summa</span><span class="sxs-lookup"><span data-stu-id="be002-165">Amount</span></span>  | <span data-ttu-id="be002-166">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="be002-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="be002-167">110110</span><span class="sxs-lookup"><span data-stu-id="be002-167">110110</span></span>         | <span data-ttu-id="be002-168">EUR</span><span class="sxs-lookup"><span data-stu-id="be002-168">EUR</span></span>      | <span data-ttu-id="be002-169">333,33</span><span class="sxs-lookup"><span data-stu-id="be002-169">333.33</span></span>  | <span data-ttu-id="be002-170">Oriģinālā summa 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="be002-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="be002-171">130100</span><span class="sxs-lookup"><span data-stu-id="be002-171">130100</span></span>         | <span data-ttu-id="be002-172">EUR</span><span class="sxs-lookup"><span data-stu-id="be002-172">EUR</span></span>      | <span data-ttu-id="be002-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="be002-173">-333.33</span></span> | <span data-ttu-id="be002-174">Oriģinālā summa -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="be002-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="be002-175">801400</span><span class="sxs-lookup"><span data-stu-id="be002-175">801400</span></span>         | <span data-ttu-id="be002-176">EUR</span><span class="sxs-lookup"><span data-stu-id="be002-176">EUR</span></span>      | <span data-ttu-id="be002-177">83,33</span><span class="sxs-lookup"><span data-stu-id="be002-177">83.33</span></span>   | <span data-ttu-id="be002-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="be002-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="be002-179">801600</span><span class="sxs-lookup"><span data-stu-id="be002-179">801600</span></span>         | <span data-ttu-id="be002-180">EUR</span><span class="sxs-lookup"><span data-stu-id="be002-180">EUR</span></span>      | <span data-ttu-id="be002-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="be002-181">-83.33</span></span>  | <span data-ttu-id="be002-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="be002-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="be002-183">Jūs redzēsiet papildu darbības pārskata valūtas summām.</span><span class="sxs-lookup"><span data-stu-id="be002-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="be002-184">Veikt valūtas pārvērtēšanu kontiem no 2015. gada 1. oktobra līdz 2015. gada 31. decembrim</span><span class="sxs-lookup"><span data-stu-id="be002-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="be002-185">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="be002-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="be002-186">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="be002-186">Ledger account</span></span> | <span data-ttu-id="be002-187">Valūta</span><span class="sxs-lookup"><span data-stu-id="be002-187">Currency</span></span> | <span data-ttu-id="be002-188">Summa</span><span class="sxs-lookup"><span data-stu-id="be002-188">Amount</span></span>  | <span data-ttu-id="be002-189">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="be002-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="be002-190">110110</span><span class="sxs-lookup"><span data-stu-id="be002-190">110110</span></span>         | <span data-ttu-id="be002-191">EUR</span><span class="sxs-lookup"><span data-stu-id="be002-191">EUR</span></span>      | <span data-ttu-id="be002-192">500,00</span><span class="sxs-lookup"><span data-stu-id="be002-192">500.00</span></span>  | <span data-ttu-id="be002-193">Oriģinālā summa 500 × 1</span><span class="sxs-lookup"><span data-stu-id="be002-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="be002-194">130100</span><span class="sxs-lookup"><span data-stu-id="be002-194">130100</span></span>         | <span data-ttu-id="be002-195">EUR</span><span class="sxs-lookup"><span data-stu-id="be002-195">EUR</span></span>      | <span data-ttu-id="be002-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="be002-196">-500.00</span></span> | <span data-ttu-id="be002-197">Oriģinālā summa -500 × 1</span><span class="sxs-lookup"><span data-stu-id="be002-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="be002-198">801400</span><span class="sxs-lookup"><span data-stu-id="be002-198">801400</span></span>         | <span data-ttu-id="be002-199">EUR</span><span class="sxs-lookup"><span data-stu-id="be002-199">EUR</span></span>      | <span data-ttu-id="be002-200">250</span><span class="sxs-lookup"><span data-stu-id="be002-200">250</span></span>     | <span data-ttu-id="be002-201">500 – 333,33 = 166.67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="be002-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="be002-202">801600</span><span class="sxs-lookup"><span data-stu-id="be002-202">801600</span></span>         | <span data-ttu-id="be002-203">EUR</span><span class="sxs-lookup"><span data-stu-id="be002-203">EUR</span></span>      | <span data-ttu-id="be002-204">-250</span><span class="sxs-lookup"><span data-stu-id="be002-204">-250</span></span>    | <span data-ttu-id="be002-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="be002-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






