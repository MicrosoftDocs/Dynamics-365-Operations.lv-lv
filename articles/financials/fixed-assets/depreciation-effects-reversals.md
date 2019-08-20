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
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840605"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="e2226-103">Nolietojuma ietekmes ar apgriešanām</span><span class="sxs-lookup"><span data-stu-id="e2226-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2226-104">Šajā rakstā ir apspriesta pamatlīdzekļu transakcijas atcelšanas potenciālā ietekme.</span><span class="sxs-lookup"><span data-stu-id="e2226-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="e2226-105">Varat apgriezt pamatlīdzekļu transakcijas, kā arī transakcijas, kas ir saistītas ar kādu pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="e2226-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="e2226-106">Apgrieztu transakciju varat arī atcelt.</span><span class="sxs-lookup"><span data-stu-id="e2226-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="e2226-107">Varat apgriezt vai atcelt transakciju, kas nav visjaunākā transakcija, kura tika grāmatota grāmatā par šo līdzekli.</span><span class="sxs-lookup"><span data-stu-id="e2226-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="e2226-108">Jums vispirms ir jānosaka, vai pēc transakcijas, kurai veicat apgriešanu, tika grāmatotas kādas nolietojuma transakcijas.</span><span class="sxs-lookup"><span data-stu-id="e2226-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="e2226-109">Tas nepieciešams tāpēc, ka pēc transakcijas apgriešanas nolietojums netiek pārrēķināts.</span><span class="sxs-lookup"><span data-stu-id="e2226-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="e2226-110">Šī iemesla dēļ pēc apgriešanas nolietojums bieži tiek pārvērtēts vai novērtēts nepietiekami, kā parādīts piemēros.</span><span class="sxs-lookup"><span data-stu-id="e2226-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="e2226-111">Lai nodrošinātu, ka nolietojums ir pareizs, kad veicat transakcijas apgriešanu, neturpiniet apgriešanu, ja saņemat ziņojumu, ka nolietojums netiks pārrēķināts.</span><span class="sxs-lookup"><span data-stu-id="e2226-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="e2226-112">Tā vietā vispirms apgrieziet nolietojuma transakciju, kas tika grāmatota pēc tās transakcijas, kuru mēģinājāt apgriezt, un pēc tam turpiniet apgriešanas procesu.</span><span class="sxs-lookup"><span data-stu-id="e2226-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="e2226-113">Jūs netiksiet brīdināts par nolietojuma pārrēķiniem un varat turpināt apgriešanu.</span><span class="sxs-lookup"><span data-stu-id="e2226-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="e2226-114">Nākamajos piemēros ir parādīti aprēķini, kas rodas, ja pēc ziņojuma saņemšanas procedūru turpināt, neapgriežot nolietojuma transakcijas.</span><span class="sxs-lookup"><span data-stu-id="e2226-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="e2226-115">1. piemērs. Nolietojums tiek pārvērtēts</span><span class="sxs-lookup"><span data-stu-id="e2226-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="e2226-116">Līdzeklis ir iestatīts ar 5 gadu lietošanas laiku un lineāro nolietojumu (60 nolietojuma periodi).</span><span class="sxs-lookup"><span data-stu-id="e2226-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="e2226-117">Šajā piemērā nolietojums tiek pārvērtēts.</span><span class="sxs-lookup"><span data-stu-id="e2226-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="e2226-118">Līdzekļu darbību vēsture</span><span class="sxs-lookup"><span data-stu-id="e2226-118">Asset transaction history</span></span>

| <span data-ttu-id="e2226-119">Datums</span><span class="sxs-lookup"><span data-stu-id="e2226-119">Date</span></span>       | <span data-ttu-id="e2226-120">Darbības tips</span><span class="sxs-lookup"><span data-stu-id="e2226-120">Transaction type</span></span>                                                          | <span data-ttu-id="e2226-121">Summa</span><span class="sxs-lookup"><span data-stu-id="e2226-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="e2226-122">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="e2226-122">January 1</span></span>  | <span data-ttu-id="e2226-123">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="e2226-123">Acquisition</span></span>                                                               | <span data-ttu-id="e2226-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="e2226-124">59,000.00</span></span>                                 |
| <span data-ttu-id="e2226-125">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="e2226-125">January 1</span></span>  | <span data-ttu-id="e2226-126">Kapitālās izmaksas</span><span class="sxs-lookup"><span data-stu-id="e2226-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="e2226-127">1000,00</span><span class="sxs-lookup"><span data-stu-id="e2226-127">1,000.00</span></span>                                  |
| <span data-ttu-id="e2226-128">31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e2226-128">January 31</span></span> | <span data-ttu-id="e2226-129">Nolietojums (izveidots, izmantojot priekšlikumu vienam nolietojuma periodam)</span><span class="sxs-lookup"><span data-stu-id="e2226-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="e2226-130">1000,00 Aprēķins: Atlikusī vērtība (59 000 + 1000) / Atlikušo nolietojuma periodu skaits (60)</span><span class="sxs-lookup"><span data-stu-id="e2226-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="e2226-131">Atgriezta darbība</span><span class="sxs-lookup"><span data-stu-id="e2226-131">Reversal action</span></span>

| <span data-ttu-id="e2226-132">Datums</span><span class="sxs-lookup"><span data-stu-id="e2226-132">Date</span></span>      | <span data-ttu-id="e2226-133">Darījuma veids</span><span class="sxs-lookup"><span data-stu-id="e2226-133">Transaction type</span></span>                | <span data-ttu-id="e2226-134">Summa</span><span class="sxs-lookup"><span data-stu-id="e2226-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="e2226-135">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="e2226-135">January 1</span></span> | <span data-ttu-id="e2226-136">Kapitālo izmaksu atgriešana</span><span class="sxs-lookup"><span data-stu-id="e2226-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="e2226-137">-1000,00</span><span class="sxs-lookup"><span data-stu-id="e2226-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="e2226-138">Nolietojuma ietekme</span><span class="sxs-lookup"><span data-stu-id="e2226-138">Depreciation effect</span></span>

| <span data-ttu-id="e2226-139">Datums</span><span class="sxs-lookup"><span data-stu-id="e2226-139">Date</span></span>        | <span data-ttu-id="e2226-140">Darījuma veids</span><span class="sxs-lookup"><span data-stu-id="e2226-140">Transaction type</span></span>        | <span data-ttu-id="e2226-141">Summa</span><span class="sxs-lookup"><span data-stu-id="e2226-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2226-142">28. februāris</span><span class="sxs-lookup"><span data-stu-id="e2226-142">February 28</span></span> | <span data-ttu-id="e2226-143">Nolietojums (priekšlikums)</span><span class="sxs-lookup"><span data-stu-id="e2226-143">Depreciation (proposal)</span></span> | <span data-ttu-id="e2226-144">983,05 Aprēķins: Atlikusī vērtība (59 000 - 1000 nolietojums) / Atlikušo nolietojuma periodu skaits (59)</span><span class="sxs-lookup"><span data-stu-id="e2226-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="e2226-145">Nolietojums ir pārvērtēts par 16,95 (1000 - 983,05).</span><span class="sxs-lookup"><span data-stu-id="e2226-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="e2226-146">2. piemērs. Nolietojums tiek nepietiekami novērtēts</span><span class="sxs-lookup"><span data-stu-id="e2226-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="e2226-147">Līdzeklis ir iestatīts ar 5 gadu lietošanas laiku un lineāro nolietojumu (60 nolietojuma periodi).</span><span class="sxs-lookup"><span data-stu-id="e2226-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="e2226-148">Šajā piemērā nolietojums tiek nepietiekami novērtēts.</span><span class="sxs-lookup"><span data-stu-id="e2226-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="e2226-149">Līdzekļu darbību vēsture</span><span class="sxs-lookup"><span data-stu-id="e2226-149">Asset transaction history</span></span>

| <span data-ttu-id="e2226-150">Datums</span><span class="sxs-lookup"><span data-stu-id="e2226-150">Date</span></span>       | <span data-ttu-id="e2226-151">Darījuma veids</span><span class="sxs-lookup"><span data-stu-id="e2226-151">Transaction type</span></span>                                                          | <span data-ttu-id="e2226-152">Summa</span><span class="sxs-lookup"><span data-stu-id="e2226-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="e2226-153">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="e2226-153">January 1</span></span>  | <span data-ttu-id="e2226-154">Iegāde</span><span class="sxs-lookup"><span data-stu-id="e2226-154">Acquisition</span></span>                                                               | <span data-ttu-id="e2226-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="e2226-155">59,000.00</span></span>                                   |
| <span data-ttu-id="e2226-156">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="e2226-156">January 1</span></span>  | <span data-ttu-id="e2226-157">Vērtības samazināšana</span><span class="sxs-lookup"><span data-stu-id="e2226-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="e2226-158">1000,00</span><span class="sxs-lookup"><span data-stu-id="e2226-158">1,000.00</span></span>                                    |
| <span data-ttu-id="e2226-159">31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e2226-159">January 31</span></span> | <span data-ttu-id="e2226-160">Nolietojums (izveidots, izmantojot priekšlikumu vienam nolietojuma periodam)</span><span class="sxs-lookup"><span data-stu-id="e2226-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="e2226-161">966,67 Aprēķins: Atlikusī vērtība (59 000 - 1000) / Atlikušo nolietojuma periodu skaits (60)</span><span class="sxs-lookup"><span data-stu-id="e2226-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="e2226-162">Atgriezta darbība</span><span class="sxs-lookup"><span data-stu-id="e2226-162">Reversal action</span></span>

| <span data-ttu-id="e2226-163">Datums</span><span class="sxs-lookup"><span data-stu-id="e2226-163">Date</span></span>      | <span data-ttu-id="e2226-164">Darījuma veids</span><span class="sxs-lookup"><span data-stu-id="e2226-164">Transaction type</span></span>               | <span data-ttu-id="e2226-165">Summa</span><span class="sxs-lookup"><span data-stu-id="e2226-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="e2226-166">1. janvāris</span><span class="sxs-lookup"><span data-stu-id="e2226-166">January 1</span></span> | <span data-ttu-id="e2226-167">Vērtības samazināšanas apgriešana</span><span class="sxs-lookup"><span data-stu-id="e2226-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="e2226-168">-1000,00</span><span class="sxs-lookup"><span data-stu-id="e2226-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="e2226-169">Nolietojuma ietekme</span><span class="sxs-lookup"><span data-stu-id="e2226-169">Depreciation effect</span></span>

| <span data-ttu-id="e2226-170">Datums</span><span class="sxs-lookup"><span data-stu-id="e2226-170">Date</span></span>        | <span data-ttu-id="e2226-171">Darījuma veids</span><span class="sxs-lookup"><span data-stu-id="e2226-171">Transaction type</span></span>        | <span data-ttu-id="e2226-172">Summa</span><span class="sxs-lookup"><span data-stu-id="e2226-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2226-173">28. februāris</span><span class="sxs-lookup"><span data-stu-id="e2226-173">February 28</span></span> | <span data-ttu-id="e2226-174">Nolietojums (priekšlikums)</span><span class="sxs-lookup"><span data-stu-id="e2226-174">Depreciation (proposal)</span></span> | <span data-ttu-id="e2226-175">983,62 Aprēķins: Atlikusī vērtība (59 000 - 966,67 nolietojums) / Atlikušo nolietojuma periodu skaits (59)</span><span class="sxs-lookup"><span data-stu-id="e2226-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="e2226-176">Nolietojums ir nepietiekami novērtēts par 16,95 (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="e2226-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="e2226-177">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e2226-177">Additional resources</span></span>
--------

[<span data-ttu-id="e2226-178">Pamatlīdzekļu nolietojums</span><span class="sxs-lookup"><span data-stu-id="e2226-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)



