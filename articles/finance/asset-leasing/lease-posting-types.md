---
title: Nomas grāmatošanas tipi
description: Šajā tēmā aprakstīti līdzekļu iznomāšanas transakcijām izmantotie grāmatošanas tipi.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b79b02f7e241783d19a315ccff5bb6874a238c38
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995422"
---
# <a name="lease-posting-types"></a><span data-ttu-id="8083f-103">Nomas grāmatošanas tipi</span><span class="sxs-lookup"><span data-stu-id="8083f-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8083f-104">Šajā tēmā aprakstīti līdzekļu iznomāšanas transakcijām izmantotie grāmatošanas tipi.</span><span class="sxs-lookup"><span data-stu-id="8083f-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="8083f-105">Nomas līdzeklis</span><span class="sxs-lookup"><span data-stu-id="8083f-105">Lease asset</span></span>

<span data-ttu-id="8083f-106">Šis konts ir saistīts ar lietošanas tiesību (right-of-use — ROU) līdzekli.</span><span class="sxs-lookup"><span data-stu-id="8083f-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="8083f-107">Šis konts tiek debetēts, ja noma sākotnēji tiek atzīta saskaņā ar jaunajiem nomas uzskaites standartiem, uzskaites standartu kodifikācijas tēmu 842 (ASC 842) un starptautisko finanšu pārskatu standartu 16 (SFPS 16).</span><span class="sxs-lookup"><span data-stu-id="8083f-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="8083f-108">Mainītai nomai šis konts var būt debetēts vai kreditēts atkarībā no tā, vai maiņa palielina vai samazina nomas saistības.</span><span class="sxs-lookup"><span data-stu-id="8083f-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="8083f-109">**Žurnāla ierakstu piemēri**: sākotnējā atzīšana</span><span class="sxs-lookup"><span data-stu-id="8083f-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="8083f-110">**Debets**: nomas līdzeklis XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="8083f-111">**Kredīts**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="8083f-112">Nomas saistības</span><span class="sxs-lookup"><span data-stu-id="8083f-112">Lease liability</span></span>

<span data-ttu-id="8083f-113">Konts ir saistīts ar nomas saistībām, kas rodas, kad maksājumiem tiek piemērota atlaide saskaņā ar jaunajiem IFRS 16 un ASC 842 standartiem.</span><span class="sxs-lookup"><span data-stu-id="8083f-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="8083f-114">Šis konts tiek kreditēts, ja noma sākotnēji tiek atzīta saskaņā ar jaunajiem standartiem.</span><span class="sxs-lookup"><span data-stu-id="8083f-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="8083f-115">Tas tiek debetēts nomas maksājumiem un kreditēts procentu uzkrājumiem.</span><span class="sxs-lookup"><span data-stu-id="8083f-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="8083f-116">**Žurnāla ierakstu piemēri**: sākotnējā atzīšana</span><span class="sxs-lookup"><span data-stu-id="8083f-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="8083f-117">**Debets**: nomas līdzeklis XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="8083f-118">**Kredīts**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="8083f-119">**Žurnāla ierakstu piemērs**: procentu uzkrājumi</span><span class="sxs-lookup"><span data-stu-id="8083f-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="8083f-120">**Debets**: procentu izdevumi XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="8083f-121">**Kredīts**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="8083f-122">**Žurnāla ierakstu piemērs**: nomas maksājums</span><span class="sxs-lookup"><span data-stu-id="8083f-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="8083f-123">**Debets**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="8083f-124">**Kredīts**: kreditora maksājums/nomas maksājums XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="8083f-125">Īstermiņa nomas saistības</span><span class="sxs-lookup"><span data-stu-id="8083f-125">Short-term lease liability</span></span>

<span data-ttu-id="8083f-126">Konts ir saistīts ar īstermiņa nomas saistībām, kur tiek grāmatots īstermiņa nomas saistību pārklasificēšanas žurnāla ieraksts.</span><span class="sxs-lookup"><span data-stu-id="8083f-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="8083f-127">Šis konts tiek kreditēts īstermiņa saistībām no amortizācijas grafika mēneša pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="8083f-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="8083f-128">Tomēr tā pati summa tiek debetēta nākamā mēneša pirmajā dienā.</span><span class="sxs-lookup"><span data-stu-id="8083f-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="8083f-129">**Žurnāla ierakstu piemērs**: īstermiņa nomas saistību pārklasificēšana</span><span class="sxs-lookup"><span data-stu-id="8083f-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="8083f-130">**Debets**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="8083f-131">**Kredīts**: īstermiņa nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="8083f-132">**Debets**: īstermiņa nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="8083f-133">**Kredīts**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="8083f-134">Nolietojuma izmaksas</span><span class="sxs-lookup"><span data-stu-id="8083f-134">Depreciation expense</span></span>

<span data-ttu-id="8083f-135">Konts ir saistīts ar izdevumiem, kas ir saistīti ar LLT līdzekļa amortizāciju saskaņā ar IFRS 16, ASC 842 un finanšu nomu saskaņā ar SGS 17 un ASC 840.</span><span class="sxs-lookup"><span data-stu-id="8083f-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="8083f-136">Šis konts tiek debetēts, ja LLT līdzeklis tiek nolietots katru mēnesi.</span><span class="sxs-lookup"><span data-stu-id="8083f-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="8083f-137">**Žurnāla ierakstu piemērs**: nolietojuma uzkrājumi</span><span class="sxs-lookup"><span data-stu-id="8083f-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="8083f-138">**Debets**: nolietojuma izdevumi XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="8083f-139">**Kredīts**: uzkrātais nolietojums XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="8083f-140">Peļņa/zaudējumi no nomas modifikācijas</span><span class="sxs-lookup"><span data-stu-id="8083f-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="8083f-141">Konts ir saistīts ar jebkuriem guvumiem vai zaudējumiem, kas rodas no nomas modifikācijām.</span><span class="sxs-lookup"><span data-stu-id="8083f-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="8083f-142">Nomas modifikācijas laikā var rasties guvums, ja modifikācija samazina nomas saistības par summu, kas pārsniedz LLT līdzekļa uzskaites vērtību.</span><span class="sxs-lookup"><span data-stu-id="8083f-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="8083f-143">Piemēram, nomai ir pašreizējās $ 150 000 nomas saistības uzskaites vērtība un $ 100 000 LLT aktīva uzskaites vērtība.</span><span class="sxs-lookup"><span data-stu-id="8083f-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="8083f-144">Noma tiek modificēta, un šī modifikācija veido jaunu nākotnes minimālo nomas maksājumu (PVFMLP) $ 40 000 apmērā aktuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="8083f-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="8083f-145">Tāpēc nomas saistības tiks debetētas ar $ 110 000 ($ 150 000 – $ 40 000).</span><span class="sxs-lookup"><span data-stu-id="8083f-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="8083f-146">Tā kā LLT līdzeklis ir tikai $ 100 000, $ 110 000 samazinājums samazina pamatlīdzekli zemāk par 0 (nulli).</span><span class="sxs-lookup"><span data-stu-id="8083f-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="8083f-147">Tāpēc uzskaites vadlīnijas nosaka, ka atlikums ir jārezervē peļņas kontā.</span><span class="sxs-lookup"><span data-stu-id="8083f-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="8083f-148">Šādā gadījumā galīgais žurnāla ieraksts būs debets nomas saistību apmaksai par $ 110 000, kredīts nomas līdzeklim $ 100 000 apmērā un kredīts peļņas kontā $ 10 000.</span><span class="sxs-lookup"><span data-stu-id="8083f-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="8083f-149">**Žurnāla ierakstu piemērs**: nomas modifikācija</span><span class="sxs-lookup"><span data-stu-id="8083f-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="8083f-150">**Debets**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="8083f-151">**Kredīts**: nomas līdzeklis XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="8083f-152">**Kredīts**: peļņa XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="8083f-153">Uzkrātais nolietojums</span><span class="sxs-lookup"><span data-stu-id="8083f-153">Accumulated depreciation</span></span>

<span data-ttu-id="8083f-154">Konts ir saistīts ar LLT līdzekļa kontrāro līdzekļu kontu.</span><span class="sxs-lookup"><span data-stu-id="8083f-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="8083f-155">Šis konts tiek kreditēts, kad tiek grāmatoti nolietojuma izdevumi.</span><span class="sxs-lookup"><span data-stu-id="8083f-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="8083f-156">**Žurnāla ierakstu piemērs**: nolietojuma uzkrājumi</span><span class="sxs-lookup"><span data-stu-id="8083f-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="8083f-157">**Debets**: nolietojuma izdevumi XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="8083f-158">**Kredīts**: uzkrātais nolietojums XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="retained-earnings"></a><span data-ttu-id="8083f-159">Nesadalītā peļņa</span><span class="sxs-lookup"><span data-stu-id="8083f-159">Retained earnings</span></span>

<span data-ttu-id="8083f-160">Konts ir saistīts ar saglabātajiem ienākumiem.</span><span class="sxs-lookup"><span data-stu-id="8083f-160">The account is associated with retained earnings.</span></span> <span data-ttu-id="8083f-161">Šis konts var tikt debetēts vai kreditēts pārejas korekcijas žurnāla ierakstā, izmantojot pilnu retrospektīvo metodi vai kumulatīvās pieaugošās opcijas metodi A.</span><span class="sxs-lookup"><span data-stu-id="8083f-161">This account might be either debited or credited in a transition adjustment journal entry by using the full retrospective method or the cumulative catch-up option A method.</span></span> <span data-ttu-id="8083f-162">Starpība starp sākotnējo LLT līdzekli un nomas saistībām ir rezervēta nesadalītajai peļņai.</span><span class="sxs-lookup"><span data-stu-id="8083f-162">The difference between the initial ROU asset and lease liability is booked to retained earnings.</span></span> <span data-ttu-id="8083f-163">Retos gadījumos saglabātie ienākumi var tikt ietekmēti arī nomas modifikācijas laikā, ja nomas klasifikācija tiek mainīta no finansējuma uz darbību, lai rakstītu LLT līdzekli uz augšu vai uz leju tā, lai tā būtu vienāds ar nomas saistībām.</span><span class="sxs-lookup"><span data-stu-id="8083f-163">In rare cases, the retained earnings might also be affected during lease modification, if the classification of a lease is changed from finance to operating to write the ROU asset up or down so that it equals the lease liability.</span></span>

<span data-ttu-id="8083f-164">**Žurnāla ierakstu piemērs**: pārejas korekcija (pilnīgas atpakaļejošas vai kumulatīvas papildopcijas metode A)</span><span class="sxs-lookup"><span data-stu-id="8083f-164">**Example journal entries:** Transition adjustment (full retrospective or cumulative catch-up option A method)</span></span><br>
<span data-ttu-id="8083f-165">**Debets**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-165">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="8083f-166">**Kredīts**: nomas līdzeklis XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-166">**Credit:** Lease asset XXX</span></span><br>
<span data-ttu-id="8083f-167">**Kredīts**: nesadalītā peļņa XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-167">**Credit:** Retained earnings XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="8083f-168">Mainīgais maksājums</span><span class="sxs-lookup"><span data-stu-id="8083f-168">Variable payment</span></span>

<span data-ttu-id="8083f-169">Konts ir saistīts ar mainīgiem nomas maksājumiem, kas tiek ražoti ar indeksa pārvērtēšanu saskaņā ar ASC 842, ASC 840 un SGS 17 nomu.</span><span class="sxs-lookup"><span data-stu-id="8083f-169">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="8083f-170">Nomas maksājumu grafikā mainīgie maksājumi ir ietverti kolonnā **Mainīgais maksājums**.</span><span class="sxs-lookup"><span data-stu-id="8083f-170">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="8083f-171">Šis konts tiek debetēts, ja rēķins tiek veidots, pamatojoties uz maksājumu grafika rindu, kas ietver mainīgo maksājumu.</span><span class="sxs-lookup"><span data-stu-id="8083f-171">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="8083f-172">**Žurnāla ierakstu piemērs**: nomas maksājums</span><span class="sxs-lookup"><span data-stu-id="8083f-172">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="8083f-173">**Debets**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-173">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="8083f-174">**Debets**: mainīgais maksājums XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-174">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="8083f-175">**Kredīts**: kreditora maksājums/nomas maksājums XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-175">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="8083f-176">Atliktās nomas maksas līdzeklis (saistības)</span><span class="sxs-lookup"><span data-stu-id="8083f-176">Deferred rent asset (liability)</span></span>

<span data-ttu-id="8083f-177">Šis konts ir saistīts ar atlikto nomas masas līdzekli vai saistībām, ko sagatavoja atliktās nomas maksas apstrādes noma.</span><span class="sxs-lookup"><span data-stu-id="8083f-177">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="8083f-178">Šis konts tiek debetēts, ja rēķins ir grāmatots ar atliktu nomas maksas apstrādes nomu, ja nomas maksājuma summa ir lielāka par perioda taisnvirziena nomas izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="8083f-178">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="8083f-179">Tas tiek kreditēts, ja nomas maksa ir mazāka par perioda taisnvirziena nomas izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="8083f-179">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="8083f-180">**Žurnāla ierakstu piemēri**: nomas maksājums (atliktās nomas maksas noma)</span><span class="sxs-lookup"><span data-stu-id="8083f-180">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="8083f-181">**Debets**: nomas izdevumi XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-181">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="8083f-182">**Kredīts**: atliktās nomas maksas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-182">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="8083f-183">**Kredīts**: kreditora maksājums/nomas maksājums XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-183">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="8083f-184">Nomas izdevumi</span><span class="sxs-lookup"><span data-stu-id="8083f-184">Lease expense</span></span>

<span data-ttu-id="8083f-185">Konts ir saistīts ar nomas izdevumiem, ja noma tiek klasificēta kā atlikta nomas maksas apstrādes noma.</span><span class="sxs-lookup"><span data-stu-id="8083f-185">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="8083f-186">Šis konts tiek debetēts, ja rēķins ir grāmatots ar atlikto nomasas maksas apstrādes nomu.</span><span class="sxs-lookup"><span data-stu-id="8083f-186">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="8083f-187">**Žurnāla ierakstu piemēri**: nomas maksājums (atliktās nomas maksas noma)</span><span class="sxs-lookup"><span data-stu-id="8083f-187">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="8083f-188">**Debets**: nomas izdevumi XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-188">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="8083f-189">**Kredīts**: atliktās nomas maksas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-189">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="8083f-190">**Kredīts**: kreditora maksājums/nomas maksājums XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-190">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="8083f-191">Vērtības samazinājuma izdevumi</span><span class="sxs-lookup"><span data-stu-id="8083f-191">Impairment expense</span></span>

<span data-ttu-id="8083f-192">Konts tiek iegrāmatots, ja noma ir samazinājusies.</span><span class="sxs-lookup"><span data-stu-id="8083f-192">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="8083f-193">Šis konts tiek debetēts, bet LLT līdzekļu konts tiek tieši kreditēts.</span><span class="sxs-lookup"><span data-stu-id="8083f-193">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="8083f-194">**Žurnāla ierakstu piemērs**: nomas maksājums</span><span class="sxs-lookup"><span data-stu-id="8083f-194">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="8083f-195">**Debets**: vērtības samazinājuma izdevumi XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-195">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="8083f-196">**Kredīts**: LLT līdzeklis XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-196">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="8083f-197">Nomas maksājums</span><span class="sxs-lookup"><span data-stu-id="8083f-197">Lease payment</span></span>

<span data-ttu-id="8083f-198">Konts tiek iegrāmatots, ja parametrs **Maksāt kreditoram** ir izslēgts.</span><span class="sxs-lookup"><span data-stu-id="8083f-198">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="8083f-199">Tiek kreditēts šis konts, nevis kreditori, ja parametrs ir izslēgts.</span><span class="sxs-lookup"><span data-stu-id="8083f-199">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="8083f-200">**Žurnāla ierakstu piemērs**: nomas maksājums</span><span class="sxs-lookup"><span data-stu-id="8083f-200">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="8083f-201">**Debets**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-201">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="8083f-202">**Kredīts**: nomas maksājums XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-202">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="8083f-203">Izdevumu tipa grāmatojumi</span><span class="sxs-lookup"><span data-stu-id="8083f-203">Expense type postings</span></span>

<span data-ttu-id="8083f-204">Katram izdevumu tipam atlasītais konts tiek debetēts, ja tiek ģenerēts maksājums par šo izdevumu tipu.</span><span class="sxs-lookup"><span data-stu-id="8083f-204">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="8083f-205">Piemēram, konts, kas ir norādīts izmaksu tipam **Apdrošināšana**, tiek debetēts ikreiz, kad tiek izveidots rēķins vai maksājumu žurnāla ieraksts no izpildes izmaksu grafika apdrošināšanas izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="8083f-205">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="8083f-206">**Žurnāla ierakstu piemērs**: apdrošināšanas maksājums</span><span class="sxs-lookup"><span data-stu-id="8083f-206">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="8083f-207">**Debets**: apdrošināšanas izdevumu tipa konts XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-207">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="8083f-208">**Kredīts**: korespondējošais konts XXX</span><span class="sxs-lookup"><span data-stu-id="8083f-208">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="8083f-209">Korespondējošais konts tiek atlasīts nomas līmenī rindās, kas attiecas uz izpildes izmaksu maksājumu grafiku.</span><span class="sxs-lookup"><span data-stu-id="8083f-209">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="8083f-210">Šo korespondējošo kontu var saistīt ar kreditoru vai ar Virsgrāmatas kontu.</span><span class="sxs-lookup"><span data-stu-id="8083f-210">This offset account can associated with the vendor, or with a ledger account.</span></span>
