---
title: Nolietojuma ietekmes ar apgriešanām
description: Šajā rakstā ir apspriesta pamatlīdzekļu transakcijas atcelšanas potenciālā ietekme.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd4c4a9e7e89b34b1311b38310877b45e4d95b22
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445475"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="5bc1e-103">Nolietojuma ietekmes ar apgriešanām</span><span class="sxs-lookup"><span data-stu-id="5bc1e-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5bc1e-104">Šajā rakstā ir apspriesta pamatlīdzekļu transakcijas atcelšanas potenciālā ietekme.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="5bc1e-105">Varat apgriezt pamatlīdzekļu transakcijas, kā arī transakcijas, kas ir saistītas ar kādu pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="5bc1e-106">Apgrieztu transakciju varat arī atcelt.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="5bc1e-107">Varat apgriezt vai atcelt transakciju, kas nav visjaunākā transakcija, kura tika grāmatota grāmatā par šo līdzekli.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="5bc1e-108">Jums vispirms ir jānosaka, vai pēc transakcijas, kurai veicat apgriešanu, tika grāmatotas kādas nolietojuma transakcijas.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="5bc1e-109">Tas nepieciešams tāpēc, ka pēc transakcijas apgriešanas nolietojums netiek pārrēķināts.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="5bc1e-110">Šī iemesla dēļ pēc apgriešanas nolietojums bieži tiek pārvērtēts vai novērtēts nepietiekami, kā parādīts piemēros.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="5bc1e-111">Lai nodrošinātu, ka nolietojums ir pareizs, kad veicat transakcijas apgriešanu, neturpiniet apgriešanu, ja saņemat ziņojumu, ka nolietojums netiks pārrēķināts.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="5bc1e-112">Tā vietā vispirms apgrieziet nolietojuma transakciju, kas tika grāmatota pēc tās transakcijas, kuru mēģinājāt apgriezt, un pēc tam turpiniet apgriešanas procesu.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="5bc1e-113">Jūs netiksiet brīdināts par nolietojuma pārrēķiniem un varat turpināt apgriešanu.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="5bc1e-114">Nākamajos piemēros ir parādīti aprēķini, kas rodas, ja pēc ziņojuma saņemšanas procedūru turpināt, neapgriežot nolietojuma transakcijas.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="5bc1e-115">1. piemērs. Nolietojums tiek pārvērtēts</span><span class="sxs-lookup"><span data-stu-id="5bc1e-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="5bc1e-116">Līdzeklis ir iestatīts ar 5 gadu lietošanas laiku un lineāro nolietojumu (60 nolietojuma periodi).</span><span class="sxs-lookup"><span data-stu-id="5bc1e-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="5bc1e-117">Šajā piemērā nolietojums tiek pārvērtēts.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="5bc1e-118">Līdzekļu darbību vēsture</span><span class="sxs-lookup"><span data-stu-id="5bc1e-118">Asset transaction history</span></span>

| <span data-ttu-id="5bc1e-119">Datums</span><span class="sxs-lookup"><span data-stu-id="5bc1e-119">Date</span></span>       | <span data-ttu-id="5bc1e-120">Darbības tips</span><span class="sxs-lookup"><span data-stu-id="5bc1e-120">Transaction type</span></span>                                                          | <span data-ttu-id="5bc1e-121">Summa</span><span class="sxs-lookup"><span data-stu-id="5bc1e-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="5bc1e-122">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="5bc1e-122">January 1</span></span>  | <span data-ttu-id="5bc1e-123">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="5bc1e-123">Acquisition</span></span>                                                               | <span data-ttu-id="5bc1e-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="5bc1e-124">59,000.00</span></span>                                 |
| <span data-ttu-id="5bc1e-125">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="5bc1e-125">January 1</span></span>  | <span data-ttu-id="5bc1e-126">Kapitālās izmaksas</span><span class="sxs-lookup"><span data-stu-id="5bc1e-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="5bc1e-127">1000,00</span><span class="sxs-lookup"><span data-stu-id="5bc1e-127">1,000.00</span></span>                                  |
| <span data-ttu-id="5bc1e-128">31. janvāris</span><span class="sxs-lookup"><span data-stu-id="5bc1e-128">January 31</span></span> | <span data-ttu-id="5bc1e-129">Nolietojums (izveidots, izmantojot priekšlikumu vienam nolietojuma periodam)</span><span class="sxs-lookup"><span data-stu-id="5bc1e-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="5bc1e-130">1000,00 Aprēķins: Atlikusī vērtība (59 000 + 1000) / Atlikušo nolietojuma periodu skaits (60)</span><span class="sxs-lookup"><span data-stu-id="5bc1e-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="5bc1e-131">Atgriezta darbība</span><span class="sxs-lookup"><span data-stu-id="5bc1e-131">Reversal action</span></span>

| <span data-ttu-id="5bc1e-132">Datums</span><span class="sxs-lookup"><span data-stu-id="5bc1e-132">Date</span></span>      | <span data-ttu-id="5bc1e-133">Darījuma veids</span><span class="sxs-lookup"><span data-stu-id="5bc1e-133">Transaction type</span></span>                | <span data-ttu-id="5bc1e-134">Summa</span><span class="sxs-lookup"><span data-stu-id="5bc1e-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="5bc1e-135">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="5bc1e-135">January 1</span></span> | <span data-ttu-id="5bc1e-136">Kapitālo izmaksu atgriešana</span><span class="sxs-lookup"><span data-stu-id="5bc1e-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="5bc1e-137">-1000,00</span><span class="sxs-lookup"><span data-stu-id="5bc1e-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="5bc1e-138">Nolietojuma ietekme</span><span class="sxs-lookup"><span data-stu-id="5bc1e-138">Depreciation effect</span></span>

| <span data-ttu-id="5bc1e-139">Datums</span><span class="sxs-lookup"><span data-stu-id="5bc1e-139">Date</span></span>        | <span data-ttu-id="5bc1e-140">Darījuma veids</span><span class="sxs-lookup"><span data-stu-id="5bc1e-140">Transaction type</span></span>        | <span data-ttu-id="5bc1e-141">Summa</span><span class="sxs-lookup"><span data-stu-id="5bc1e-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc1e-142">28. februāris</span><span class="sxs-lookup"><span data-stu-id="5bc1e-142">February 28</span></span> | <span data-ttu-id="5bc1e-143">Nolietojums (priekšlikums)</span><span class="sxs-lookup"><span data-stu-id="5bc1e-143">Depreciation (proposal)</span></span> | <span data-ttu-id="5bc1e-144">983,05 Aprēķins: Atlikusī vērtība (59 000 - 1000 nolietojums) / Atlikušo nolietojuma periodu skaits (59)</span><span class="sxs-lookup"><span data-stu-id="5bc1e-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="5bc1e-145">Nolietojums ir pārvērtēts par 16,95 (1000 - 983,05).</span><span class="sxs-lookup"><span data-stu-id="5bc1e-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="5bc1e-146">2. piemērs. Nolietojums tiek nepietiekami novērtēts</span><span class="sxs-lookup"><span data-stu-id="5bc1e-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="5bc1e-147">Līdzeklis ir iestatīts ar 5 gadu lietošanas laiku un lineāro nolietojumu (60 nolietojuma periodi).</span><span class="sxs-lookup"><span data-stu-id="5bc1e-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="5bc1e-148">Šajā piemērā nolietojums tiek nepietiekami novērtēts.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="5bc1e-149">Līdzekļu darbību vēsture</span><span class="sxs-lookup"><span data-stu-id="5bc1e-149">Asset transaction history</span></span>

| <span data-ttu-id="5bc1e-150">Datums</span><span class="sxs-lookup"><span data-stu-id="5bc1e-150">Date</span></span>       | <span data-ttu-id="5bc1e-151">Darījuma veids</span><span class="sxs-lookup"><span data-stu-id="5bc1e-151">Transaction type</span></span>                                                          | <span data-ttu-id="5bc1e-152">Summa</span><span class="sxs-lookup"><span data-stu-id="5bc1e-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="5bc1e-153">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="5bc1e-153">January 1</span></span>  | <span data-ttu-id="5bc1e-154">Iegāde</span><span class="sxs-lookup"><span data-stu-id="5bc1e-154">Acquisition</span></span>                                                               | <span data-ttu-id="5bc1e-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="5bc1e-155">59,000.00</span></span>                                   |
| <span data-ttu-id="5bc1e-156">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="5bc1e-156">January 1</span></span>  | <span data-ttu-id="5bc1e-157">Vērtības samazināšana</span><span class="sxs-lookup"><span data-stu-id="5bc1e-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="5bc1e-158">1000,00</span><span class="sxs-lookup"><span data-stu-id="5bc1e-158">1,000.00</span></span>                                    |
| <span data-ttu-id="5bc1e-159">31. janvāris</span><span class="sxs-lookup"><span data-stu-id="5bc1e-159">January 31</span></span> | <span data-ttu-id="5bc1e-160">Nolietojums (izveidots, izmantojot priekšlikumu vienam nolietojuma periodam)</span><span class="sxs-lookup"><span data-stu-id="5bc1e-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="5bc1e-161">966,67 Aprēķins: Atlikusī vērtība (59 000 - 1000) / Atlikušo nolietojuma periodu skaits (60)</span><span class="sxs-lookup"><span data-stu-id="5bc1e-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="5bc1e-162">Atgriezta darbība</span><span class="sxs-lookup"><span data-stu-id="5bc1e-162">Reversal action</span></span>

| <span data-ttu-id="5bc1e-163">Datums</span><span class="sxs-lookup"><span data-stu-id="5bc1e-163">Date</span></span>      | <span data-ttu-id="5bc1e-164">Darījuma veids</span><span class="sxs-lookup"><span data-stu-id="5bc1e-164">Transaction type</span></span>               | <span data-ttu-id="5bc1e-165">Summa</span><span class="sxs-lookup"><span data-stu-id="5bc1e-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="5bc1e-166">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="5bc1e-166">January 1</span></span> | <span data-ttu-id="5bc1e-167">Vērtības samazināšanas apgriešana</span><span class="sxs-lookup"><span data-stu-id="5bc1e-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="5bc1e-168">-1000,00</span><span class="sxs-lookup"><span data-stu-id="5bc1e-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="5bc1e-169">Nolietojuma ietekme</span><span class="sxs-lookup"><span data-stu-id="5bc1e-169">Depreciation effect</span></span>

| <span data-ttu-id="5bc1e-170">Datums</span><span class="sxs-lookup"><span data-stu-id="5bc1e-170">Date</span></span>        | <span data-ttu-id="5bc1e-171">Darījuma veids</span><span class="sxs-lookup"><span data-stu-id="5bc1e-171">Transaction type</span></span>        | <span data-ttu-id="5bc1e-172">Summa</span><span class="sxs-lookup"><span data-stu-id="5bc1e-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc1e-173">28. februāris</span><span class="sxs-lookup"><span data-stu-id="5bc1e-173">February 28</span></span> | <span data-ttu-id="5bc1e-174">Nolietojums (priekšlikums)</span><span class="sxs-lookup"><span data-stu-id="5bc1e-174">Depreciation (proposal)</span></span> | <span data-ttu-id="5bc1e-175">983,62 Aprēķins: Atlikusī vērtība (59 000 - 966,67 nolietojums) / Atlikušo nolietojuma periodu skaits (59)</span><span class="sxs-lookup"><span data-stu-id="5bc1e-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="5bc1e-176">Nolietojums ir nepietiekami novērtēts par 16,95 (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="5bc1e-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="5bc1e-177">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5bc1e-177">Additional resources</span></span>
--------

[<span data-ttu-id="5bc1e-178">Pamatlīdzekļu nolietojums</span><span class="sxs-lookup"><span data-stu-id="5bc1e-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)



