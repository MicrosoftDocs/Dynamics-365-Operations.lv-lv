---
title: Valūtas pārvērtēšana konsolidācijas uzņēmumā
description: Šajā tēmā ir aprakstīts, kā konsolidētā uzņēmumā pārvērtēt valūtu.
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b7f0a18910cbaed382971e47eb688c075e7e6a5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178808"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="4cedb-103">Valūtas pārvērtēšana konsolidācijas uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="4cedb-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4cedb-104">Veicot datu konsolidāciju no vienas norēķinu valūtas uz citu, joprojām jāpalaiž valūtas pārvērtēšana, ja ir izmaiņas valūtas maiņas kursos, lai jūsu konta bilances tiktu pareizi pārvērtētas.</span><span class="sxs-lookup"><span data-stu-id="4cedb-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="4cedb-105">Sākotnēji konsolidējot datus, izmantojiet cilni **Valūtas pārrēķināšana**, lai atlasītu sākotnējos maiņas kursus, pārrēķināšanai konsolidācijas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="4cedb-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="4cedb-106">Pēc jaunā valūtas maiņas kursa ievadīšanas (piemēram, nākamajā mēnesī), nepieciešams pārvērtēt kontu bilances.</span><span class="sxs-lookup"><span data-stu-id="4cedb-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="4cedb-107">Nerealizētā peļņa vai zaudējumi pēc tam tiek attiecīgi atjaunināta, pamatojoties uz jauno valūtas maiņas kursu un datumu.</span><span class="sxs-lookup"><span data-stu-id="4cedb-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="4cedb-108">Šajā piemērā tiek parādīti uzskaites ieraksti, kas tiek izveidoti procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="4cedb-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="4cedb-109">Uzņēmuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4cedb-109">Company setup</span></span>
-   <span data-ttu-id="4cedb-110">**Avota/strādājošs uzņēmums (USMF)** – ASV dolāri (USD) tiek izmantoti kā uzskaites un pārskata valūta.</span><span class="sxs-lookup"><span data-stu-id="4cedb-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="4cedb-111">**Konsolidēts uzņēmums (CON)** – eiro (EUR) tiek izmantoti kā uzskaites un pārskata valūta.</span><span class="sxs-lookup"><span data-stu-id="4cedb-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="4cedb-112">**Realizētā peļņa** – Virsgrāmatas konts 801500</span><span class="sxs-lookup"><span data-stu-id="4cedb-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="4cedb-113">**Realizētie zaudējumi** – Virsgrāmatas konts 801600</span><span class="sxs-lookup"><span data-stu-id="4cedb-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="4cedb-114">**Nerealizētā peļņa** – Virsgrāmatas konts 801600</span><span class="sxs-lookup"><span data-stu-id="4cedb-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="4cedb-115">**Nerealizētie zaudējumi** – Virsgrāmatas konts 801400</span><span class="sxs-lookup"><span data-stu-id="4cedb-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="4cedb-116">Sākotnējās darbības</span><span class="sxs-lookup"><span data-stu-id="4cedb-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="4cedb-117">Kases ieņēmumu darbības USMF</span><span class="sxs-lookup"><span data-stu-id="4cedb-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="4cedb-118">Datums</span><span class="sxs-lookup"><span data-stu-id="4cedb-118">Date</span></span>       | <span data-ttu-id="4cedb-119">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="4cedb-119">Ledger account</span></span>               | <span data-ttu-id="4cedb-120">Valūta</span><span class="sxs-lookup"><span data-stu-id="4cedb-120">Currency</span></span> | <span data-ttu-id="4cedb-121">Summa</span><span class="sxs-lookup"><span data-stu-id="4cedb-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="4cedb-122">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="4cedb-122">10/11/2015</span></span> | <span data-ttu-id="4cedb-123">110110 – Skaidra nauda</span><span class="sxs-lookup"><span data-stu-id="4cedb-123">110110 – Cash</span></span>                | <span data-ttu-id="4cedb-124">USD</span><span class="sxs-lookup"><span data-stu-id="4cedb-124">USD</span></span>      | <span data-ttu-id="4cedb-125">500</span><span class="sxs-lookup"><span data-stu-id="4cedb-125">500</span></span>    |
| <span data-ttu-id="4cedb-126">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="4cedb-126">10/11/2015</span></span> | <span data-ttu-id="4cedb-127">130100 – Debitoru parādi</span><span class="sxs-lookup"><span data-stu-id="4cedb-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="4cedb-128">USD</span><span class="sxs-lookup"><span data-stu-id="4cedb-128">USD</span></span>      | <span data-ttu-id="4cedb-129">-500</span><span class="sxs-lookup"><span data-stu-id="4cedb-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="4cedb-130">Valūtu maiņas kursi</span><span class="sxs-lookup"><span data-stu-id="4cedb-130">Exchange rates</span></span>

| <span data-ttu-id="4cedb-131">No valūtas</span><span class="sxs-lookup"><span data-stu-id="4cedb-131">From currency</span></span> | <span data-ttu-id="4cedb-132">Uz valūtu</span><span class="sxs-lookup"><span data-stu-id="4cedb-132">To currency</span></span> | <span data-ttu-id="4cedb-133">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="4cedb-133">Start date</span></span> | <span data-ttu-id="4cedb-134">Valūtas kurss</span><span class="sxs-lookup"><span data-stu-id="4cedb-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="4cedb-135">EUR</span><span class="sxs-lookup"><span data-stu-id="4cedb-135">EUR</span></span>           | <span data-ttu-id="4cedb-136">USD</span><span class="sxs-lookup"><span data-stu-id="4cedb-136">USD</span></span>         | <span data-ttu-id="4cedb-137">01.10.2015</span><span class="sxs-lookup"><span data-stu-id="4cedb-137">10/1/2015</span></span>  | <span data-ttu-id="4cedb-138">200</span><span class="sxs-lookup"><span data-stu-id="4cedb-138">200</span></span>           |
| <span data-ttu-id="4cedb-139">EUR</span><span class="sxs-lookup"><span data-stu-id="4cedb-139">EUR</span></span>           | <span data-ttu-id="4cedb-140">USD</span><span class="sxs-lookup"><span data-stu-id="4cedb-140">USD</span></span>         | <span data-ttu-id="4cedb-141">01.11.2015</span><span class="sxs-lookup"><span data-stu-id="4cedb-141">11/1/2015</span></span>  | <span data-ttu-id="4cedb-142">150</span><span class="sxs-lookup"><span data-stu-id="4cedb-142">150</span></span>           |
| <span data-ttu-id="4cedb-143">EUR</span><span class="sxs-lookup"><span data-stu-id="4cedb-143">EUR</span></span>           | <span data-ttu-id="4cedb-144">USD</span><span class="sxs-lookup"><span data-stu-id="4cedb-144">USD</span></span>         | <span data-ttu-id="4cedb-145">01.12.2012</span><span class="sxs-lookup"><span data-stu-id="4cedb-145">12/1/2012</span></span>  | <span data-ttu-id="4cedb-146">100</span><span class="sxs-lookup"><span data-stu-id="4cedb-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="4cedb-147">Veikt konsolidāciju par 2015. gada oktobri</span><span class="sxs-lookup"><span data-stu-id="4cedb-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="4cedb-148">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="4cedb-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="4cedb-149">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="4cedb-149">Ledger account</span></span> | <span data-ttu-id="4cedb-150">Valūta</span><span class="sxs-lookup"><span data-stu-id="4cedb-150">Currency</span></span> | <span data-ttu-id="4cedb-151">Summa</span><span class="sxs-lookup"><span data-stu-id="4cedb-151">Amount</span></span> | <span data-ttu-id="4cedb-152">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="4cedb-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="4cedb-153">110110</span><span class="sxs-lookup"><span data-stu-id="4cedb-153">110110</span></span>         | <span data-ttu-id="4cedb-154">EUR</span><span class="sxs-lookup"><span data-stu-id="4cedb-154">EUR</span></span>      | <span data-ttu-id="4cedb-155">250</span><span class="sxs-lookup"><span data-stu-id="4cedb-155">250</span></span>    | <span data-ttu-id="4cedb-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="4cedb-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="4cedb-157">130100</span><span class="sxs-lookup"><span data-stu-id="4cedb-157">130100</span></span>         | <span data-ttu-id="4cedb-158">EUR</span><span class="sxs-lookup"><span data-stu-id="4cedb-158">EUR</span></span>      | <span data-ttu-id="4cedb-159">-250</span><span class="sxs-lookup"><span data-stu-id="4cedb-159">-250</span></span>   | <span data-ttu-id="4cedb-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="4cedb-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="4cedb-161">Veikt valūtas pārvērtēšanu kontiem no 2015. gada 1. oktobra līdz 2015. gada 30. novembrim</span><span class="sxs-lookup"><span data-stu-id="4cedb-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="4cedb-162">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="4cedb-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="4cedb-163">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="4cedb-163">Ledger account</span></span> | <span data-ttu-id="4cedb-164">Valūta</span><span class="sxs-lookup"><span data-stu-id="4cedb-164">Currency</span></span> | <span data-ttu-id="4cedb-165">Summa</span><span class="sxs-lookup"><span data-stu-id="4cedb-165">Amount</span></span>  | <span data-ttu-id="4cedb-166">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="4cedb-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="4cedb-167">110110</span><span class="sxs-lookup"><span data-stu-id="4cedb-167">110110</span></span>         | <span data-ttu-id="4cedb-168">EUR</span><span class="sxs-lookup"><span data-stu-id="4cedb-168">EUR</span></span>      | <span data-ttu-id="4cedb-169">333,33</span><span class="sxs-lookup"><span data-stu-id="4cedb-169">333.33</span></span>  | <span data-ttu-id="4cedb-170">Oriģinālā summa 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="4cedb-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="4cedb-171">130100</span><span class="sxs-lookup"><span data-stu-id="4cedb-171">130100</span></span>         | <span data-ttu-id="4cedb-172">EUR</span><span class="sxs-lookup"><span data-stu-id="4cedb-172">EUR</span></span>      | <span data-ttu-id="4cedb-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="4cedb-173">-333.33</span></span> | <span data-ttu-id="4cedb-174">Oriģinālā summa -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="4cedb-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="4cedb-175">801400</span><span class="sxs-lookup"><span data-stu-id="4cedb-175">801400</span></span>         | <span data-ttu-id="4cedb-176">EUR</span><span class="sxs-lookup"><span data-stu-id="4cedb-176">EUR</span></span>      | <span data-ttu-id="4cedb-177">83,33</span><span class="sxs-lookup"><span data-stu-id="4cedb-177">83.33</span></span>   | <span data-ttu-id="4cedb-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="4cedb-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="4cedb-179">801600</span><span class="sxs-lookup"><span data-stu-id="4cedb-179">801600</span></span>         | <span data-ttu-id="4cedb-180">EUR</span><span class="sxs-lookup"><span data-stu-id="4cedb-180">EUR</span></span>      | <span data-ttu-id="4cedb-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="4cedb-181">-83.33</span></span>  | <span data-ttu-id="4cedb-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="4cedb-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="4cedb-183">Jūs redzēsiet papildu darbības pārskata valūtas summām.</span><span class="sxs-lookup"><span data-stu-id="4cedb-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="4cedb-184">Veikt valūtas pārvērtēšanu kontiem no 2015. gada 1. oktobra līdz 2015. gada 31. decembrim</span><span class="sxs-lookup"><span data-stu-id="4cedb-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="4cedb-185">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="4cedb-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="4cedb-186">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="4cedb-186">Ledger account</span></span> | <span data-ttu-id="4cedb-187">Valūta</span><span class="sxs-lookup"><span data-stu-id="4cedb-187">Currency</span></span> | <span data-ttu-id="4cedb-188">Summa</span><span class="sxs-lookup"><span data-stu-id="4cedb-188">Amount</span></span>  | <span data-ttu-id="4cedb-189">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="4cedb-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="4cedb-190">110110</span><span class="sxs-lookup"><span data-stu-id="4cedb-190">110110</span></span>         | <span data-ttu-id="4cedb-191">EUR</span><span class="sxs-lookup"><span data-stu-id="4cedb-191">EUR</span></span>      | <span data-ttu-id="4cedb-192">500,00</span><span class="sxs-lookup"><span data-stu-id="4cedb-192">500.00</span></span>  | <span data-ttu-id="4cedb-193">Oriģinālā summa 500 × 1</span><span class="sxs-lookup"><span data-stu-id="4cedb-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="4cedb-194">130100</span><span class="sxs-lookup"><span data-stu-id="4cedb-194">130100</span></span>         | <span data-ttu-id="4cedb-195">EUR</span><span class="sxs-lookup"><span data-stu-id="4cedb-195">EUR</span></span>      | <span data-ttu-id="4cedb-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="4cedb-196">-500.00</span></span> | <span data-ttu-id="4cedb-197">Oriģinālā summa -500 × 1</span><span class="sxs-lookup"><span data-stu-id="4cedb-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="4cedb-198">801400</span><span class="sxs-lookup"><span data-stu-id="4cedb-198">801400</span></span>         | <span data-ttu-id="4cedb-199">EUR</span><span class="sxs-lookup"><span data-stu-id="4cedb-199">EUR</span></span>      | <span data-ttu-id="4cedb-200">250</span><span class="sxs-lookup"><span data-stu-id="4cedb-200">250</span></span>     | <span data-ttu-id="4cedb-201">500 – 333,33 = 166.67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="4cedb-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="4cedb-202">801600</span><span class="sxs-lookup"><span data-stu-id="4cedb-202">801600</span></span>         | <span data-ttu-id="4cedb-203">EUR</span><span class="sxs-lookup"><span data-stu-id="4cedb-203">EUR</span></span>      | <span data-ttu-id="4cedb-204">-250</span><span class="sxs-lookup"><span data-stu-id="4cedb-204">-250</span></span>    | <span data-ttu-id="4cedb-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="4cedb-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





