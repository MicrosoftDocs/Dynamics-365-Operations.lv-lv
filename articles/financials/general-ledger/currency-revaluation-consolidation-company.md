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
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839429"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="c64e8-103">Valūtas pārvērtēšana konsolidācijas uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="c64e8-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c64e8-104">Veicot datu konsolidāciju no vienas norēķinu valūtas uz citu, joprojām jāpalaiž valūtas pārvērtēšana, ja ir izmaiņas valūtas maiņas kursos, lai jūsu konta bilances tiktu pareizi pārvērtētas.</span><span class="sxs-lookup"><span data-stu-id="c64e8-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="c64e8-105">Sākotnēji konsolidējot datus, izmantojiet cilni **Valūtas pārrēķināšana**, lai atlasītu sākotnējos maiņas kursus, pārrēķināšanai konsolidācijas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="c64e8-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="c64e8-106">Pēc jaunā valūtas maiņas kursa ievadīšanas (piemēram, nākamajā mēnesī), nepieciešams pārvērtēt kontu bilances.</span><span class="sxs-lookup"><span data-stu-id="c64e8-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="c64e8-107">Nerealizētā peļņa vai zaudējumi pēc tam tiek attiecīgi atjaunināta, pamatojoties uz jauno valūtas maiņas kursu un datumu.</span><span class="sxs-lookup"><span data-stu-id="c64e8-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="c64e8-108">Šajā piemērā tiek parādīti uzskaites ieraksti, kas tiek izveidoti procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="c64e8-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="c64e8-109">Uzņēmuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="c64e8-109">Company setup</span></span>
-   <span data-ttu-id="c64e8-110">**Avota/strādājošs uzņēmums (USMF)** – ASV dolāri (USD) tiek izmantoti kā uzskaites un pārskata valūta.</span><span class="sxs-lookup"><span data-stu-id="c64e8-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="c64e8-111">**Konsolidēts uzņēmums (CON)** – eiro (EUR) tiek izmantoti kā uzskaites un pārskata valūta.</span><span class="sxs-lookup"><span data-stu-id="c64e8-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="c64e8-112">**Realizētā peļņa** – Virsgrāmatas konts 801500</span><span class="sxs-lookup"><span data-stu-id="c64e8-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="c64e8-113">**Realizētie zaudējumi** – Virsgrāmatas konts 801600</span><span class="sxs-lookup"><span data-stu-id="c64e8-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="c64e8-114">**Nerealizētā peļņa** – Virsgrāmatas konts 801600</span><span class="sxs-lookup"><span data-stu-id="c64e8-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="c64e8-115">**Nerealizētie zaudējumi** – Virsgrāmatas konts 801400</span><span class="sxs-lookup"><span data-stu-id="c64e8-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="c64e8-116">Sākotnējās darbības</span><span class="sxs-lookup"><span data-stu-id="c64e8-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="c64e8-117">Kases ieņēmumu darbības USMF</span><span class="sxs-lookup"><span data-stu-id="c64e8-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="c64e8-118">Datums</span><span class="sxs-lookup"><span data-stu-id="c64e8-118">Date</span></span>       | <span data-ttu-id="c64e8-119">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="c64e8-119">Ledger account</span></span>               | <span data-ttu-id="c64e8-120">Valūta</span><span class="sxs-lookup"><span data-stu-id="c64e8-120">Currency</span></span> | <span data-ttu-id="c64e8-121">Summa</span><span class="sxs-lookup"><span data-stu-id="c64e8-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="c64e8-122">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="c64e8-122">10/11/2015</span></span> | <span data-ttu-id="c64e8-123">110110 – Skaidra nauda</span><span class="sxs-lookup"><span data-stu-id="c64e8-123">110110 – Cash</span></span>                | <span data-ttu-id="c64e8-124">USD</span><span class="sxs-lookup"><span data-stu-id="c64e8-124">USD</span></span>      | <span data-ttu-id="c64e8-125">500</span><span class="sxs-lookup"><span data-stu-id="c64e8-125">500</span></span>    |
| <span data-ttu-id="c64e8-126">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="c64e8-126">10/11/2015</span></span> | <span data-ttu-id="c64e8-127">130100 – Debitoru parādi</span><span class="sxs-lookup"><span data-stu-id="c64e8-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="c64e8-128">USD</span><span class="sxs-lookup"><span data-stu-id="c64e8-128">USD</span></span>      | <span data-ttu-id="c64e8-129">-500</span><span class="sxs-lookup"><span data-stu-id="c64e8-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="c64e8-130">Valūtu maiņas kursi</span><span class="sxs-lookup"><span data-stu-id="c64e8-130">Exchange rates</span></span>

| <span data-ttu-id="c64e8-131">No valūtas</span><span class="sxs-lookup"><span data-stu-id="c64e8-131">From currency</span></span> | <span data-ttu-id="c64e8-132">Uz valūtu</span><span class="sxs-lookup"><span data-stu-id="c64e8-132">To currency</span></span> | <span data-ttu-id="c64e8-133">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="c64e8-133">Start date</span></span> | <span data-ttu-id="c64e8-134">Valūtas kurss</span><span class="sxs-lookup"><span data-stu-id="c64e8-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="c64e8-135">EUR</span><span class="sxs-lookup"><span data-stu-id="c64e8-135">EUR</span></span>           | <span data-ttu-id="c64e8-136">USD</span><span class="sxs-lookup"><span data-stu-id="c64e8-136">USD</span></span>         | <span data-ttu-id="c64e8-137">01.10.2015</span><span class="sxs-lookup"><span data-stu-id="c64e8-137">10/1/2015</span></span>  | <span data-ttu-id="c64e8-138">200</span><span class="sxs-lookup"><span data-stu-id="c64e8-138">200</span></span>           |
| <span data-ttu-id="c64e8-139">EUR</span><span class="sxs-lookup"><span data-stu-id="c64e8-139">EUR</span></span>           | <span data-ttu-id="c64e8-140">USD</span><span class="sxs-lookup"><span data-stu-id="c64e8-140">USD</span></span>         | <span data-ttu-id="c64e8-141">01.11.2015</span><span class="sxs-lookup"><span data-stu-id="c64e8-141">11/1/2015</span></span>  | <span data-ttu-id="c64e8-142">150</span><span class="sxs-lookup"><span data-stu-id="c64e8-142">150</span></span>           |
| <span data-ttu-id="c64e8-143">EUR</span><span class="sxs-lookup"><span data-stu-id="c64e8-143">EUR</span></span>           | <span data-ttu-id="c64e8-144">USD</span><span class="sxs-lookup"><span data-stu-id="c64e8-144">USD</span></span>         | <span data-ttu-id="c64e8-145">01.12.2012</span><span class="sxs-lookup"><span data-stu-id="c64e8-145">12/1/2012</span></span>  | <span data-ttu-id="c64e8-146">100</span><span class="sxs-lookup"><span data-stu-id="c64e8-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="c64e8-147">Veikt konsolidāciju par 2015. gada oktobri</span><span class="sxs-lookup"><span data-stu-id="c64e8-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="c64e8-148">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="c64e8-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="c64e8-149">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="c64e8-149">Ledger account</span></span> | <span data-ttu-id="c64e8-150">Valūta</span><span class="sxs-lookup"><span data-stu-id="c64e8-150">Currency</span></span> | <span data-ttu-id="c64e8-151">Summa</span><span class="sxs-lookup"><span data-stu-id="c64e8-151">Amount</span></span> | <span data-ttu-id="c64e8-152">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="c64e8-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="c64e8-153">110110</span><span class="sxs-lookup"><span data-stu-id="c64e8-153">110110</span></span>         | <span data-ttu-id="c64e8-154">EUR</span><span class="sxs-lookup"><span data-stu-id="c64e8-154">EUR</span></span>      | <span data-ttu-id="c64e8-155">250</span><span class="sxs-lookup"><span data-stu-id="c64e8-155">250</span></span>    | <span data-ttu-id="c64e8-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="c64e8-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="c64e8-157">130100</span><span class="sxs-lookup"><span data-stu-id="c64e8-157">130100</span></span>         | <span data-ttu-id="c64e8-158">EUR</span><span class="sxs-lookup"><span data-stu-id="c64e8-158">EUR</span></span>      | <span data-ttu-id="c64e8-159">-250</span><span class="sxs-lookup"><span data-stu-id="c64e8-159">-250</span></span>   | <span data-ttu-id="c64e8-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="c64e8-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="c64e8-161">Veikt valūtas pārvērtēšanu kontiem no 2015. gada 1. oktobra līdz 2015. gada 30. novembrim</span><span class="sxs-lookup"><span data-stu-id="c64e8-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="c64e8-162">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="c64e8-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="c64e8-163">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="c64e8-163">Ledger account</span></span> | <span data-ttu-id="c64e8-164">Valūta</span><span class="sxs-lookup"><span data-stu-id="c64e8-164">Currency</span></span> | <span data-ttu-id="c64e8-165">Summa</span><span class="sxs-lookup"><span data-stu-id="c64e8-165">Amount</span></span>  | <span data-ttu-id="c64e8-166">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="c64e8-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="c64e8-167">110110</span><span class="sxs-lookup"><span data-stu-id="c64e8-167">110110</span></span>         | <span data-ttu-id="c64e8-168">EUR</span><span class="sxs-lookup"><span data-stu-id="c64e8-168">EUR</span></span>      | <span data-ttu-id="c64e8-169">333,33</span><span class="sxs-lookup"><span data-stu-id="c64e8-169">333.33</span></span>  | <span data-ttu-id="c64e8-170">Oriģinālā summa 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="c64e8-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="c64e8-171">130100</span><span class="sxs-lookup"><span data-stu-id="c64e8-171">130100</span></span>         | <span data-ttu-id="c64e8-172">EUR</span><span class="sxs-lookup"><span data-stu-id="c64e8-172">EUR</span></span>      | <span data-ttu-id="c64e8-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="c64e8-173">-333.33</span></span> | <span data-ttu-id="c64e8-174">Oriģinālā summa -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="c64e8-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="c64e8-175">801400</span><span class="sxs-lookup"><span data-stu-id="c64e8-175">801400</span></span>         | <span data-ttu-id="c64e8-176">EUR</span><span class="sxs-lookup"><span data-stu-id="c64e8-176">EUR</span></span>      | <span data-ttu-id="c64e8-177">83,33</span><span class="sxs-lookup"><span data-stu-id="c64e8-177">83.33</span></span>   | <span data-ttu-id="c64e8-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="c64e8-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="c64e8-179">801600</span><span class="sxs-lookup"><span data-stu-id="c64e8-179">801600</span></span>         | <span data-ttu-id="c64e8-180">EUR</span><span class="sxs-lookup"><span data-stu-id="c64e8-180">EUR</span></span>      | <span data-ttu-id="c64e8-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="c64e8-181">-83.33</span></span>  | <span data-ttu-id="c64e8-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="c64e8-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="c64e8-183">Jūs redzēsiet papildu darbības pārskata valūtas summām.</span><span class="sxs-lookup"><span data-stu-id="c64e8-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="c64e8-184">Veikt valūtas pārvērtēšanu kontiem no 2015. gada 1. oktobra līdz 2015. gada 31. decembrim</span><span class="sxs-lookup"><span data-stu-id="c64e8-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="c64e8-185">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="c64e8-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="c64e8-186">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="c64e8-186">Ledger account</span></span> | <span data-ttu-id="c64e8-187">Valūta</span><span class="sxs-lookup"><span data-stu-id="c64e8-187">Currency</span></span> | <span data-ttu-id="c64e8-188">Summa</span><span class="sxs-lookup"><span data-stu-id="c64e8-188">Amount</span></span>  | <span data-ttu-id="c64e8-189">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="c64e8-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="c64e8-190">110110</span><span class="sxs-lookup"><span data-stu-id="c64e8-190">110110</span></span>         | <span data-ttu-id="c64e8-191">EUR</span><span class="sxs-lookup"><span data-stu-id="c64e8-191">EUR</span></span>      | <span data-ttu-id="c64e8-192">500,00</span><span class="sxs-lookup"><span data-stu-id="c64e8-192">500.00</span></span>  | <span data-ttu-id="c64e8-193">Oriģinālā summa 500 × 1</span><span class="sxs-lookup"><span data-stu-id="c64e8-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="c64e8-194">130100</span><span class="sxs-lookup"><span data-stu-id="c64e8-194">130100</span></span>         | <span data-ttu-id="c64e8-195">EUR</span><span class="sxs-lookup"><span data-stu-id="c64e8-195">EUR</span></span>      | <span data-ttu-id="c64e8-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="c64e8-196">-500.00</span></span> | <span data-ttu-id="c64e8-197">Oriģinālā summa -500 × 1</span><span class="sxs-lookup"><span data-stu-id="c64e8-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="c64e8-198">801400</span><span class="sxs-lookup"><span data-stu-id="c64e8-198">801400</span></span>         | <span data-ttu-id="c64e8-199">EUR</span><span class="sxs-lookup"><span data-stu-id="c64e8-199">EUR</span></span>      | <span data-ttu-id="c64e8-200">250</span><span class="sxs-lookup"><span data-stu-id="c64e8-200">250</span></span>     | <span data-ttu-id="c64e8-201">500 – 333,33 = 166.67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="c64e8-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="c64e8-202">801600</span><span class="sxs-lookup"><span data-stu-id="c64e8-202">801600</span></span>         | <span data-ttu-id="c64e8-203">EUR</span><span class="sxs-lookup"><span data-stu-id="c64e8-203">EUR</span></span>      | <span data-ttu-id="c64e8-204">-250</span><span class="sxs-lookup"><span data-stu-id="c64e8-204">-250</span></span>    | <span data-ttu-id="c64e8-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="c64e8-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





