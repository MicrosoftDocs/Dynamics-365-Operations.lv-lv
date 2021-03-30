---
title: Valūtas pārvērtēšana konsolidācijas uzņēmumā
description: Šajā tēmā ir aprakstīts, kā konsolidētā uzņēmumā pārvērtēt valūtu.
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81de31ee75b4be38256505bc7b875dc15473c75a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212233"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="f036b-103">Valūtas pārvērtēšana konsolidācijas uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="f036b-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f036b-104">Veicot datu konsolidāciju no vienas norēķinu valūtas uz citu, joprojām jāpalaiž valūtas pārvērtēšana, ja ir izmaiņas valūtas maiņas kursos, lai jūsu konta bilances tiktu pareizi pārvērtētas.</span><span class="sxs-lookup"><span data-stu-id="f036b-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="f036b-105">Sākotnēji konsolidējot datus, izmantojiet cilni **Valūtas pārrēķināšana**, lai atlasītu sākotnējos maiņas kursus, pārrēķināšanai konsolidācijas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="f036b-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="f036b-106">Pēc jaunā valūtas maiņas kursa ievadīšanas (piemēram, nākamajā mēnesī), nepieciešams pārvērtēt kontu bilances.</span><span class="sxs-lookup"><span data-stu-id="f036b-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="f036b-107">Nerealizētā peļņa vai zaudējumi pēc tam tiek attiecīgi atjaunināta, pamatojoties uz jauno valūtas maiņas kursu un datumu.</span><span class="sxs-lookup"><span data-stu-id="f036b-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="f036b-108">Šajā piemērā tiek parādīti uzskaites ieraksti, kas tiek izveidoti procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="f036b-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="f036b-109">Uzņēmuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="f036b-109">Company setup</span></span>
-   <span data-ttu-id="f036b-110">**Avota/strādājošs uzņēmums (USMF)** – ASV dolāri (USD) tiek izmantoti kā uzskaites un pārskata valūta.</span><span class="sxs-lookup"><span data-stu-id="f036b-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="f036b-111">**Konsolidēts uzņēmums (CON)** – eiro (EUR) tiek izmantoti kā uzskaites un pārskata valūta.</span><span class="sxs-lookup"><span data-stu-id="f036b-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="f036b-112">**Realizētā peļņa** – Virsgrāmatas konts 801500</span><span class="sxs-lookup"><span data-stu-id="f036b-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="f036b-113">**Realizētie zaudējumi** – Virsgrāmatas konts 801600</span><span class="sxs-lookup"><span data-stu-id="f036b-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f036b-114">**Nerealizētā peļņa** – Virsgrāmatas konts 801600</span><span class="sxs-lookup"><span data-stu-id="f036b-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f036b-115">**Nerealizētie zaudējumi** – Virsgrāmatas konts 801400</span><span class="sxs-lookup"><span data-stu-id="f036b-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="f036b-116">Sākotnējās darbības</span><span class="sxs-lookup"><span data-stu-id="f036b-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="f036b-117">Kases ieņēmumu darbības USMF</span><span class="sxs-lookup"><span data-stu-id="f036b-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="f036b-118">Datums</span><span class="sxs-lookup"><span data-stu-id="f036b-118">Date</span></span>       | <span data-ttu-id="f036b-119">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="f036b-119">Ledger account</span></span>               | <span data-ttu-id="f036b-120">Valūta</span><span class="sxs-lookup"><span data-stu-id="f036b-120">Currency</span></span> | <span data-ttu-id="f036b-121">Summa</span><span class="sxs-lookup"><span data-stu-id="f036b-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="f036b-122">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="f036b-122">10/11/2015</span></span> | <span data-ttu-id="f036b-123">110110 – Skaidra nauda</span><span class="sxs-lookup"><span data-stu-id="f036b-123">110110 – Cash</span></span>                | <span data-ttu-id="f036b-124">USD</span><span class="sxs-lookup"><span data-stu-id="f036b-124">USD</span></span>      | <span data-ttu-id="f036b-125">500</span><span class="sxs-lookup"><span data-stu-id="f036b-125">500</span></span>    |
| <span data-ttu-id="f036b-126">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="f036b-126">10/11/2015</span></span> | <span data-ttu-id="f036b-127">130100 – Debitoru parādi</span><span class="sxs-lookup"><span data-stu-id="f036b-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="f036b-128">USD</span><span class="sxs-lookup"><span data-stu-id="f036b-128">USD</span></span>      | <span data-ttu-id="f036b-129">-500</span><span class="sxs-lookup"><span data-stu-id="f036b-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="f036b-130">Valūtu maiņas kursi</span><span class="sxs-lookup"><span data-stu-id="f036b-130">Exchange rates</span></span>

| <span data-ttu-id="f036b-131">No valūtas</span><span class="sxs-lookup"><span data-stu-id="f036b-131">From currency</span></span> | <span data-ttu-id="f036b-132">Uz valūtu</span><span class="sxs-lookup"><span data-stu-id="f036b-132">To currency</span></span> | <span data-ttu-id="f036b-133">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="f036b-133">Start date</span></span> | <span data-ttu-id="f036b-134">Valūtas kurss</span><span class="sxs-lookup"><span data-stu-id="f036b-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="f036b-135">EUR</span><span class="sxs-lookup"><span data-stu-id="f036b-135">EUR</span></span>           | <span data-ttu-id="f036b-136">USD</span><span class="sxs-lookup"><span data-stu-id="f036b-136">USD</span></span>         | <span data-ttu-id="f036b-137">01.10.2015</span><span class="sxs-lookup"><span data-stu-id="f036b-137">10/1/2015</span></span>  | <span data-ttu-id="f036b-138">200</span><span class="sxs-lookup"><span data-stu-id="f036b-138">200</span></span>           |
| <span data-ttu-id="f036b-139">EUR</span><span class="sxs-lookup"><span data-stu-id="f036b-139">EUR</span></span>           | <span data-ttu-id="f036b-140">USD</span><span class="sxs-lookup"><span data-stu-id="f036b-140">USD</span></span>         | <span data-ttu-id="f036b-141">01.11.2015</span><span class="sxs-lookup"><span data-stu-id="f036b-141">11/1/2015</span></span>  | <span data-ttu-id="f036b-142">150</span><span class="sxs-lookup"><span data-stu-id="f036b-142">150</span></span>           |
| <span data-ttu-id="f036b-143">EUR</span><span class="sxs-lookup"><span data-stu-id="f036b-143">EUR</span></span>           | <span data-ttu-id="f036b-144">USD</span><span class="sxs-lookup"><span data-stu-id="f036b-144">USD</span></span>         | <span data-ttu-id="f036b-145">01.12.2012</span><span class="sxs-lookup"><span data-stu-id="f036b-145">12/1/2012</span></span>  | <span data-ttu-id="f036b-146">100</span><span class="sxs-lookup"><span data-stu-id="f036b-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="f036b-147">Veikt konsolidāciju par 2015. gada oktobri</span><span class="sxs-lookup"><span data-stu-id="f036b-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f036b-148">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="f036b-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="f036b-149">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="f036b-149">Ledger account</span></span> | <span data-ttu-id="f036b-150">Valūta</span><span class="sxs-lookup"><span data-stu-id="f036b-150">Currency</span></span> | <span data-ttu-id="f036b-151">Summa</span><span class="sxs-lookup"><span data-stu-id="f036b-151">Amount</span></span> | <span data-ttu-id="f036b-152">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="f036b-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="f036b-153">110110</span><span class="sxs-lookup"><span data-stu-id="f036b-153">110110</span></span>         | <span data-ttu-id="f036b-154">EUR</span><span class="sxs-lookup"><span data-stu-id="f036b-154">EUR</span></span>      | <span data-ttu-id="f036b-155">250</span><span class="sxs-lookup"><span data-stu-id="f036b-155">250</span></span>    | <span data-ttu-id="f036b-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="f036b-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="f036b-157">130100</span><span class="sxs-lookup"><span data-stu-id="f036b-157">130100</span></span>         | <span data-ttu-id="f036b-158">EUR</span><span class="sxs-lookup"><span data-stu-id="f036b-158">EUR</span></span>      | <span data-ttu-id="f036b-159">-250</span><span class="sxs-lookup"><span data-stu-id="f036b-159">-250</span></span>   | <span data-ttu-id="f036b-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="f036b-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="f036b-161">Veikt valūtas pārvērtēšanu kontiem no 2015. gada 1. oktobra līdz 2015. gada 30. novembrim</span><span class="sxs-lookup"><span data-stu-id="f036b-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f036b-162">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="f036b-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="f036b-163">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="f036b-163">Ledger account</span></span> | <span data-ttu-id="f036b-164">Valūta</span><span class="sxs-lookup"><span data-stu-id="f036b-164">Currency</span></span> | <span data-ttu-id="f036b-165">Summa</span><span class="sxs-lookup"><span data-stu-id="f036b-165">Amount</span></span>  | <span data-ttu-id="f036b-166">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="f036b-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="f036b-167">110110</span><span class="sxs-lookup"><span data-stu-id="f036b-167">110110</span></span>         | <span data-ttu-id="f036b-168">EUR</span><span class="sxs-lookup"><span data-stu-id="f036b-168">EUR</span></span>      | <span data-ttu-id="f036b-169">333,33</span><span class="sxs-lookup"><span data-stu-id="f036b-169">333.33</span></span>  | <span data-ttu-id="f036b-170">Oriģinālā summa 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="f036b-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="f036b-171">130100</span><span class="sxs-lookup"><span data-stu-id="f036b-171">130100</span></span>         | <span data-ttu-id="f036b-172">EUR</span><span class="sxs-lookup"><span data-stu-id="f036b-172">EUR</span></span>      | <span data-ttu-id="f036b-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="f036b-173">-333.33</span></span> | <span data-ttu-id="f036b-174">Oriģinālā summa -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="f036b-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="f036b-175">801400</span><span class="sxs-lookup"><span data-stu-id="f036b-175">801400</span></span>         | <span data-ttu-id="f036b-176">EUR</span><span class="sxs-lookup"><span data-stu-id="f036b-176">EUR</span></span>      | <span data-ttu-id="f036b-177">83,33</span><span class="sxs-lookup"><span data-stu-id="f036b-177">83.33</span></span>   | <span data-ttu-id="f036b-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="f036b-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="f036b-179">801600</span><span class="sxs-lookup"><span data-stu-id="f036b-179">801600</span></span>         | <span data-ttu-id="f036b-180">EUR</span><span class="sxs-lookup"><span data-stu-id="f036b-180">EUR</span></span>      | <span data-ttu-id="f036b-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="f036b-181">-83.33</span></span>  | <span data-ttu-id="f036b-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="f036b-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="f036b-183">Jūs redzēsiet papildu darbības pārskata valūtas summām.</span><span class="sxs-lookup"><span data-stu-id="f036b-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="f036b-184">Veikt valūtas pārvērtēšanu kontiem no 2015. gada 1. oktobra līdz 2015. gada 31. decembrim</span><span class="sxs-lookup"><span data-stu-id="f036b-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f036b-185">Bilances konsolidētajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="f036b-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="f036b-186">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="f036b-186">Ledger account</span></span> | <span data-ttu-id="f036b-187">Valūta</span><span class="sxs-lookup"><span data-stu-id="f036b-187">Currency</span></span> | <span data-ttu-id="f036b-188">Summa</span><span class="sxs-lookup"><span data-stu-id="f036b-188">Amount</span></span>  | <span data-ttu-id="f036b-189">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="f036b-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="f036b-190">110110</span><span class="sxs-lookup"><span data-stu-id="f036b-190">110110</span></span>         | <span data-ttu-id="f036b-191">EUR</span><span class="sxs-lookup"><span data-stu-id="f036b-191">EUR</span></span>      | <span data-ttu-id="f036b-192">500,00</span><span class="sxs-lookup"><span data-stu-id="f036b-192">500.00</span></span>  | <span data-ttu-id="f036b-193">Oriģinālā summa 500 × 1</span><span class="sxs-lookup"><span data-stu-id="f036b-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="f036b-194">130100</span><span class="sxs-lookup"><span data-stu-id="f036b-194">130100</span></span>         | <span data-ttu-id="f036b-195">EUR</span><span class="sxs-lookup"><span data-stu-id="f036b-195">EUR</span></span>      | <span data-ttu-id="f036b-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="f036b-196">-500.00</span></span> | <span data-ttu-id="f036b-197">Oriģinālā summa -500 × 1</span><span class="sxs-lookup"><span data-stu-id="f036b-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="f036b-198">801400</span><span class="sxs-lookup"><span data-stu-id="f036b-198">801400</span></span>         | <span data-ttu-id="f036b-199">EUR</span><span class="sxs-lookup"><span data-stu-id="f036b-199">EUR</span></span>      | <span data-ttu-id="f036b-200">250</span><span class="sxs-lookup"><span data-stu-id="f036b-200">250</span></span>     | <span data-ttu-id="f036b-201">500 – 333,33 = 166.67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="f036b-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="f036b-202">801600</span><span class="sxs-lookup"><span data-stu-id="f036b-202">801600</span></span>         | <span data-ttu-id="f036b-203">EUR</span><span class="sxs-lookup"><span data-stu-id="f036b-203">EUR</span></span>      | <span data-ttu-id="f036b-204">-250</span><span class="sxs-lookup"><span data-stu-id="f036b-204">-250</span></span>    | <span data-ttu-id="f036b-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="f036b-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]