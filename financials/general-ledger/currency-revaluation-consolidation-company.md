---
title: "Valūtas pārvērtēšana konsolidācijas uzņēmumā"
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: lv-lv
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="f14f2-102">Valūtas pārvērtēšana konsolidācijas uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="f14f2-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="f14f2-103">Veicot datu konsolidāciju no vienas norēķinu valūtas uz citu, joprojām jāpalaiž valūtas pārvērtēšana, ja ir izmaiņas valūtas maiņas kursos, lai jūsu konta bilances tiktu pareizi pārvērtētas.</span><span class="sxs-lookup"><span data-stu-id="f14f2-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="f14f2-104">Sākotnēji konsolidējot datus, izmantojiet cilni **Valūtas pārrēķināšana**, lai atlasītu sākotnējos maiņas kursus, pārrēķināšanai konsolidācijas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="f14f2-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="f14f2-105">Pēc jaunā valūtas maiņas kursa ievadīšanas (piemēram, nākamajā mēnesī), nepieciešams pārvērtēt kontu bilances.</span><span class="sxs-lookup"><span data-stu-id="f14f2-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="f14f2-106">Nerealizētā peļņa vai zaudējumi pēc tam tiek attiecīgi atjaunināta, pamatojoties uz jauno valūtas maiņas kursu un datumu.</span><span class="sxs-lookup"><span data-stu-id="f14f2-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="f14f2-107">Šajā piemērā tiek parādīti uzskaites ieraksti, kas tiek izveidoti procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="f14f2-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="f14f2-108">Uzņēmuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="f14f2-108">Company setup</span></span>
-   <span data-ttu-id="f14f2-109">**Avota/strādājošs uzņēmums (USMF)** – ASV dolāri (USD) tiek izmantoti kā uzskaites un pārskata valūta.</span><span class="sxs-lookup"><span data-stu-id="f14f2-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="f14f2-110">**Konsolidēts uzņēmums (CON)** – eiro (EUR) tiek izmantoti kā uzskaites un pārskata valūta.</span><span class="sxs-lookup"><span data-stu-id="f14f2-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="f14f2-111">**Realizētā peļņa** – virsgrāmatas konts 801500</span><span class="sxs-lookup"><span data-stu-id="f14f2-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="f14f2-112">**Realizētie zaudējumi** – Virsgrāmatas konts 801600</span><span class="sxs-lookup"><span data-stu-id="f14f2-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f14f2-113">**Nerealizētā peļņa** – Virsgrāmatas konts 801600</span><span class="sxs-lookup"><span data-stu-id="f14f2-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f14f2-114">**Nerealizētie zaudējumi** – Virsgrāmatas konts 801400</span><span class="sxs-lookup"><span data-stu-id="f14f2-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="f14f2-115">Sākotnējās darbības</span><span class="sxs-lookup"><span data-stu-id="f14f2-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="f14f2-116">Kases ieņēmumu darbības USMF</span><span class="sxs-lookup"><span data-stu-id="f14f2-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="f14f2-117">Datums</span><span class="sxs-lookup"><span data-stu-id="f14f2-117">Date</span></span>       | <span data-ttu-id="f14f2-118">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="f14f2-118">Ledger account</span></span>               | <span data-ttu-id="f14f2-119">Valūta</span><span class="sxs-lookup"><span data-stu-id="f14f2-119">Currency</span></span> | <span data-ttu-id="f14f2-120">Summa</span><span class="sxs-lookup"><span data-stu-id="f14f2-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="f14f2-121">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="f14f2-121">10/11/2015</span></span> | <span data-ttu-id="f14f2-122">110110 – Skaidra nauda</span><span class="sxs-lookup"><span data-stu-id="f14f2-122">110110 – Cash</span></span>                | <span data-ttu-id="f14f2-123">USD</span><span class="sxs-lookup"><span data-stu-id="f14f2-123">USD</span></span>      | <span data-ttu-id="f14f2-124">500</span><span class="sxs-lookup"><span data-stu-id="f14f2-124">500</span></span>    |
| <span data-ttu-id="f14f2-125">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="f14f2-125">10/11/2015</span></span> | <span data-ttu-id="f14f2-126">130100 – Debitoru parādi</span><span class="sxs-lookup"><span data-stu-id="f14f2-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="f14f2-127">USD</span><span class="sxs-lookup"><span data-stu-id="f14f2-127">USD</span></span>      | <span data-ttu-id="f14f2-128">-500</span><span class="sxs-lookup"><span data-stu-id="f14f2-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="f14f2-129">Valūtu maiņas kursi</span><span class="sxs-lookup"><span data-stu-id="f14f2-129">Exchange rates</span></span>
| <span data-ttu-id="f14f2-130">No valūtas</span><span class="sxs-lookup"><span data-stu-id="f14f2-130">From currency</span></span> | <span data-ttu-id="f14f2-131">Uz valūtu</span><span class="sxs-lookup"><span data-stu-id="f14f2-131">To currency</span></span> | <span data-ttu-id="f14f2-132">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="f14f2-132">Start date</span></span> | <span data-ttu-id="f14f2-133">Valūtas kurss</span><span class="sxs-lookup"><span data-stu-id="f14f2-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="f14f2-134">EUR</span><span class="sxs-lookup"><span data-stu-id="f14f2-134">EUR</span></span>           | <span data-ttu-id="f14f2-135">USD</span><span class="sxs-lookup"><span data-stu-id="f14f2-135">USD</span></span>         | <span data-ttu-id="f14f2-136">01.10.2015</span><span class="sxs-lookup"><span data-stu-id="f14f2-136">10/1/2015</span></span>  | <span data-ttu-id="f14f2-137">200</span><span class="sxs-lookup"><span data-stu-id="f14f2-137">200</span></span>           |
| <span data-ttu-id="f14f2-138">EUR</span><span class="sxs-lookup"><span data-stu-id="f14f2-138">EUR</span></span>           | <span data-ttu-id="f14f2-139">USD</span><span class="sxs-lookup"><span data-stu-id="f14f2-139">USD</span></span>         | <span data-ttu-id="f14f2-140">01.11.2015</span><span class="sxs-lookup"><span data-stu-id="f14f2-140">11/1/2015</span></span>  | <span data-ttu-id="f14f2-141">150</span><span class="sxs-lookup"><span data-stu-id="f14f2-141">150</span></span>           |
| <span data-ttu-id="f14f2-142">EUR</span><span class="sxs-lookup"><span data-stu-id="f14f2-142">EUR</span></span>           | <span data-ttu-id="f14f2-143">USD</span><span class="sxs-lookup"><span data-stu-id="f14f2-143">USD</span></span>         | <span data-ttu-id="f14f2-144">01.12.2012</span><span class="sxs-lookup"><span data-stu-id="f14f2-144">12/1/2012</span></span>  | <span data-ttu-id="f14f2-145">100</span><span class="sxs-lookup"><span data-stu-id="f14f2-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="f14f2-146">Veikt konsolidāciju par 2015. gada oktobri</span><span class="sxs-lookup"><span data-stu-id="f14f2-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f14f2-147">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="f14f2-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="f14f2-148">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="f14f2-148">Ledger account</span></span> | <span data-ttu-id="f14f2-149">Valūta</span><span class="sxs-lookup"><span data-stu-id="f14f2-149">Currency</span></span> | <span data-ttu-id="f14f2-150">Summa</span><span class="sxs-lookup"><span data-stu-id="f14f2-150">Amount</span></span> | <span data-ttu-id="f14f2-151">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="f14f2-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="f14f2-152">110110</span><span class="sxs-lookup"><span data-stu-id="f14f2-152">110110</span></span>         | <span data-ttu-id="f14f2-153">EUR</span><span class="sxs-lookup"><span data-stu-id="f14f2-153">EUR</span></span>      | <span data-ttu-id="f14f2-154">250</span><span class="sxs-lookup"><span data-stu-id="f14f2-154">250</span></span>    | <span data-ttu-id="f14f2-155">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="f14f2-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="f14f2-156">130100</span><span class="sxs-lookup"><span data-stu-id="f14f2-156">130100</span></span>         | <span data-ttu-id="f14f2-157">EUR</span><span class="sxs-lookup"><span data-stu-id="f14f2-157">EUR</span></span>      | <span data-ttu-id="f14f2-158">-250</span><span class="sxs-lookup"><span data-stu-id="f14f2-158">-250</span></span>   | <span data-ttu-id="f14f2-159">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="f14f2-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="f14f2-160">Veikt valūtas pārvērtēšanu kontiem no 2015. gada 1. oktobra līdz 2015. gada 30. novembrim</span><span class="sxs-lookup"><span data-stu-id="f14f2-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f14f2-161">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="f14f2-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="f14f2-162">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="f14f2-162">Ledger account</span></span> | <span data-ttu-id="f14f2-163">Valūta</span><span class="sxs-lookup"><span data-stu-id="f14f2-163">Currency</span></span> | <span data-ttu-id="f14f2-164">Summa</span><span class="sxs-lookup"><span data-stu-id="f14f2-164">Amount</span></span>  | <span data-ttu-id="f14f2-165">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="f14f2-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="f14f2-166">110110</span><span class="sxs-lookup"><span data-stu-id="f14f2-166">110110</span></span>         | <span data-ttu-id="f14f2-167">EUR</span><span class="sxs-lookup"><span data-stu-id="f14f2-167">EUR</span></span>      | <span data-ttu-id="f14f2-168">333,33</span><span class="sxs-lookup"><span data-stu-id="f14f2-168">333.33</span></span>  | <span data-ttu-id="f14f2-169">Oriģinālā summa 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="f14f2-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="f14f2-170">130100</span><span class="sxs-lookup"><span data-stu-id="f14f2-170">130100</span></span>         | <span data-ttu-id="f14f2-171">EUR</span><span class="sxs-lookup"><span data-stu-id="f14f2-171">EUR</span></span>      | <span data-ttu-id="f14f2-172">-333,33</span><span class="sxs-lookup"><span data-stu-id="f14f2-172">-333.33</span></span> | <span data-ttu-id="f14f2-173">Oriģinālā summa -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="f14f2-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="f14f2-174">801400</span><span class="sxs-lookup"><span data-stu-id="f14f2-174">801400</span></span>         | <span data-ttu-id="f14f2-175">EUR</span><span class="sxs-lookup"><span data-stu-id="f14f2-175">EUR</span></span>      | <span data-ttu-id="f14f2-176">83,33</span><span class="sxs-lookup"><span data-stu-id="f14f2-176">83.33</span></span>   | <span data-ttu-id="f14f2-177">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="f14f2-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="f14f2-178">801600</span><span class="sxs-lookup"><span data-stu-id="f14f2-178">801600</span></span>         | <span data-ttu-id="f14f2-179">EUR</span><span class="sxs-lookup"><span data-stu-id="f14f2-179">EUR</span></span>      | <span data-ttu-id="f14f2-180">-83,33</span><span class="sxs-lookup"><span data-stu-id="f14f2-180">-83.33</span></span>  | <span data-ttu-id="f14f2-181">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="f14f2-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="f14f2-182">Jūs redzēsiet papildu darbības pārskata valūtas summām.</span><span class="sxs-lookup"><span data-stu-id="f14f2-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="f14f2-183">Veikt valūtas pārvērtēšanu kontiem no 2015. gada 1. oktobra līdz 2015. gada 31. decembrim</span><span class="sxs-lookup"><span data-stu-id="f14f2-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f14f2-184">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="f14f2-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="f14f2-185">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="f14f2-185">Ledger account</span></span> | <span data-ttu-id="f14f2-186">Valūta</span><span class="sxs-lookup"><span data-stu-id="f14f2-186">Currency</span></span> | <span data-ttu-id="f14f2-187">Summa</span><span class="sxs-lookup"><span data-stu-id="f14f2-187">Amount</span></span>  | <span data-ttu-id="f14f2-188">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="f14f2-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="f14f2-189">110110</span><span class="sxs-lookup"><span data-stu-id="f14f2-189">110110</span></span>         | <span data-ttu-id="f14f2-190">EUR</span><span class="sxs-lookup"><span data-stu-id="f14f2-190">EUR</span></span>      | <span data-ttu-id="f14f2-191">500,00</span><span class="sxs-lookup"><span data-stu-id="f14f2-191">500.00</span></span>  | <span data-ttu-id="f14f2-192">Oriģinālā summa 500 × 1</span><span class="sxs-lookup"><span data-stu-id="f14f2-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="f14f2-193">130100</span><span class="sxs-lookup"><span data-stu-id="f14f2-193">130100</span></span>         | <span data-ttu-id="f14f2-194">EUR</span><span class="sxs-lookup"><span data-stu-id="f14f2-194">EUR</span></span>      | <span data-ttu-id="f14f2-195">-500,00</span><span class="sxs-lookup"><span data-stu-id="f14f2-195">-500.00</span></span> | <span data-ttu-id="f14f2-196">Oriģinālā summa -500 × 1</span><span class="sxs-lookup"><span data-stu-id="f14f2-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="f14f2-197">801400</span><span class="sxs-lookup"><span data-stu-id="f14f2-197">801400</span></span>         | <span data-ttu-id="f14f2-198">EUR</span><span class="sxs-lookup"><span data-stu-id="f14f2-198">EUR</span></span>      | <span data-ttu-id="f14f2-199">250</span><span class="sxs-lookup"><span data-stu-id="f14f2-199">250</span></span>     | <span data-ttu-id="f14f2-200">500 – 333,33 = 166.67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="f14f2-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="f14f2-201">801600</span><span class="sxs-lookup"><span data-stu-id="f14f2-201">801600</span></span>         | <span data-ttu-id="f14f2-202">EUR</span><span class="sxs-lookup"><span data-stu-id="f14f2-202">EUR</span></span>      | <span data-ttu-id="f14f2-203">-250</span><span class="sxs-lookup"><span data-stu-id="f14f2-203">-250</span></span>    | <span data-ttu-id="f14f2-204">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="f14f2-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






