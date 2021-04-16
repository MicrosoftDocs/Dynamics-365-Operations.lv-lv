---
title: Nomas grāmatošanas tipi
description: Šajā tēmā aprakstīti līdzekļu iznomāšanas transakcijām izmantotie grāmatošanas tipi.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ddc229f3ab8e048390f27503e2c6c26bd1a6f24f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841145"
---
# <a name="lease-posting-types"></a><span data-ttu-id="4c654-103">Nomas grāmatošanas tipi</span><span class="sxs-lookup"><span data-stu-id="4c654-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c654-104">Šajā tēmā aprakstīti līdzekļu iznomāšanas transakcijām izmantotie grāmatošanas tipi.</span><span class="sxs-lookup"><span data-stu-id="4c654-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="4c654-105">Nomas līdzeklis</span><span class="sxs-lookup"><span data-stu-id="4c654-105">Lease asset</span></span>

<span data-ttu-id="4c654-106">Šis konts ir saistīts ar lietošanas tiesību (right-of-use — ROU) līdzekli.</span><span class="sxs-lookup"><span data-stu-id="4c654-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="4c654-107">Šis konts tiek debetēts, ja noma sākotnēji tiek atzīta saskaņā ar jaunajiem nomas uzskaites standartiem, uzskaites standartu kodifikācijas tēmu 842 (ASC 842) un starptautisko finanšu pārskatu standartu 16 (SFPS 16).</span><span class="sxs-lookup"><span data-stu-id="4c654-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="4c654-108">Mainītai nomai šis konts var būt debetēts vai kreditēts atkarībā no tā, vai maiņa palielina vai samazina nomas saistības.</span><span class="sxs-lookup"><span data-stu-id="4c654-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="4c654-109">**Žurnāla ierakstu piemēri**: sākotnējā atzīšana</span><span class="sxs-lookup"><span data-stu-id="4c654-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="4c654-110">**Debets**: nomas līdzeklis XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="4c654-111">**Kredīts**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="4c654-112">Nomas saistības</span><span class="sxs-lookup"><span data-stu-id="4c654-112">Lease liability</span></span>

<span data-ttu-id="4c654-113">Konts ir saistīts ar nomas saistībām, kas rodas, kad maksājumiem tiek piemērota atlaide saskaņā ar jaunajiem IFRS 16 un ASC 842 standartiem.</span><span class="sxs-lookup"><span data-stu-id="4c654-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="4c654-114">Šis konts tiek kreditēts, ja noma sākotnēji tiek atzīta saskaņā ar jaunajiem standartiem.</span><span class="sxs-lookup"><span data-stu-id="4c654-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="4c654-115">Tas tiek debetēts nomas maksājumiem un kreditēts procentu uzkrājumiem.</span><span class="sxs-lookup"><span data-stu-id="4c654-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="4c654-116">**Žurnāla ierakstu piemēri**: sākotnējā atzīšana</span><span class="sxs-lookup"><span data-stu-id="4c654-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="4c654-117">**Debets**: nomas līdzeklis XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="4c654-118">**Kredīts**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="4c654-119">**Žurnāla ierakstu piemērs**: procentu uzkrājumi</span><span class="sxs-lookup"><span data-stu-id="4c654-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="4c654-120">**Debets**: procentu izdevumi XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="4c654-121">**Kredīts**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="4c654-122">**Žurnāla ierakstu piemērs**: nomas maksājums</span><span class="sxs-lookup"><span data-stu-id="4c654-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="4c654-123">**Debets**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="4c654-124">**Kredīts**: kreditora maksājums/nomas maksājums XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="4c654-125">Īstermiņa nomas saistības</span><span class="sxs-lookup"><span data-stu-id="4c654-125">Short-term lease liability</span></span>

<span data-ttu-id="4c654-126">Konts ir saistīts ar īstermiņa nomas saistībām, kur tiek grāmatots īstermiņa nomas saistību pārklasificēšanas žurnāla ieraksts.</span><span class="sxs-lookup"><span data-stu-id="4c654-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="4c654-127">Šis konts tiek kreditēts īstermiņa saistībām no amortizācijas grafika mēneša pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="4c654-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="4c654-128">Tomēr tā pati summa tiek debetēta nākamā mēneša pirmajā dienā.</span><span class="sxs-lookup"><span data-stu-id="4c654-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="4c654-129">**Žurnāla ierakstu piemērs**: īstermiņa nomas saistību pārklasificēšana</span><span class="sxs-lookup"><span data-stu-id="4c654-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="4c654-130">**Debets**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="4c654-131">**Kredīts**: īstermiņa nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="4c654-132">**Debets**: īstermiņa nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="4c654-133">**Kredīts**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="4c654-134">Nolietojuma izmaksas</span><span class="sxs-lookup"><span data-stu-id="4c654-134">Depreciation expense</span></span>

<span data-ttu-id="4c654-135">Konts ir saistīts ar izdevumiem, kas ir saistīti ar LLT līdzekļa amortizāciju saskaņā ar IFRS 16, ASC 842 un finanšu nomu saskaņā ar SGS 17 un ASC 840.</span><span class="sxs-lookup"><span data-stu-id="4c654-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="4c654-136">Šis konts tiek debetēts, ja LLT līdzeklis tiek nolietots katru mēnesi.</span><span class="sxs-lookup"><span data-stu-id="4c654-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="4c654-137">**Žurnāla ierakstu piemērs**: nolietojuma uzkrājumi</span><span class="sxs-lookup"><span data-stu-id="4c654-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="4c654-138">**Debets**: nolietojuma izdevumi XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="4c654-139">**Kredīts**: uzkrātais nolietojums XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="4c654-140">Peļņa/zaudējumi no nomas modifikācijas</span><span class="sxs-lookup"><span data-stu-id="4c654-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="4c654-141">Konts ir saistīts ar jebkuriem guvumiem vai zaudējumiem, kas rodas no nomas modifikācijām.</span><span class="sxs-lookup"><span data-stu-id="4c654-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="4c654-142">Nomas modifikācijas laikā var rasties guvums, ja modifikācija samazina nomas saistības par summu, kas pārsniedz LLT līdzekļa uzskaites vērtību.</span><span class="sxs-lookup"><span data-stu-id="4c654-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="4c654-143">Piemēram, nomai ir pašreizējās $ 150 000 nomas saistības uzskaites vērtība un $ 100 000 LLT aktīva uzskaites vērtība.</span><span class="sxs-lookup"><span data-stu-id="4c654-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="4c654-144">Noma tiek modificēta, un šī modifikācija veido jaunu nākotnes minimālo nomas maksājumu (PVFMLP) $ 40 000 apmērā aktuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="4c654-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="4c654-145">Tāpēc nomas saistības tiks debetētas ar $ 110 000 ($ 150 000 – $ 40 000).</span><span class="sxs-lookup"><span data-stu-id="4c654-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="4c654-146">Tā kā LLT līdzeklis ir tikai $ 100 000, $ 110 000 samazinājums samazina pamatlīdzekli zemāk par 0 (nulli).</span><span class="sxs-lookup"><span data-stu-id="4c654-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="4c654-147">Tāpēc uzskaites vadlīnijas nosaka, ka atlikums ir jārezervē peļņas kontā.</span><span class="sxs-lookup"><span data-stu-id="4c654-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="4c654-148">Šādā gadījumā galīgais žurnāla ieraksts būs debets nomas saistību apmaksai par $ 110 000, kredīts nomas līdzeklim $ 100 000 apmērā un kredīts peļņas kontā $ 10 000.</span><span class="sxs-lookup"><span data-stu-id="4c654-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="4c654-149">**Žurnāla ierakstu piemērs**: nomas modifikācija</span><span class="sxs-lookup"><span data-stu-id="4c654-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="4c654-150">**Debets**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="4c654-151">**Kredīts**: nomas līdzeklis XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="4c654-152">**Kredīts**: peļņa XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="4c654-153">Uzkrātais nolietojums</span><span class="sxs-lookup"><span data-stu-id="4c654-153">Accumulated depreciation</span></span>

<span data-ttu-id="4c654-154">Konts ir saistīts ar LLT līdzekļa kontrāro līdzekļu kontu.</span><span class="sxs-lookup"><span data-stu-id="4c654-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="4c654-155">Šis konts tiek kreditēts, kad tiek grāmatoti nolietojuma izdevumi.</span><span class="sxs-lookup"><span data-stu-id="4c654-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="4c654-156">**Žurnāla ierakstu piemērs**: nolietojuma uzkrājumi</span><span class="sxs-lookup"><span data-stu-id="4c654-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="4c654-157">**Debets**: nolietojuma izdevumi XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="4c654-158">**Kredīts**: uzkrātais nolietojums XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="4c654-159">Mainīgais maksājums</span><span class="sxs-lookup"><span data-stu-id="4c654-159">Variable payment</span></span>

<span data-ttu-id="4c654-160">Konts ir saistīts ar mainīgiem nomas maksājumiem, kas tiek ražoti ar indeksa pārvērtēšanu saskaņā ar ASC 842, ASC 840 un SGS 17 nomu.</span><span class="sxs-lookup"><span data-stu-id="4c654-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="4c654-161">Nomas maksājumu grafikā mainīgie maksājumi ir ietverti kolonnā **Mainīgais maksājums**.</span><span class="sxs-lookup"><span data-stu-id="4c654-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="4c654-162">Šis konts tiek debetēts, ja rēķins tiek veidots, pamatojoties uz maksājumu grafika rindu, kas ietver mainīgo maksājumu.</span><span class="sxs-lookup"><span data-stu-id="4c654-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="4c654-163">**Žurnāla ierakstu piemērs**: nomas maksājums</span><span class="sxs-lookup"><span data-stu-id="4c654-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="4c654-164">**Debets**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="4c654-165">**Debets**: mainīgais maksājums XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="4c654-166">**Kredīts**: kreditora maksājums/nomas maksājums XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="4c654-167">Atliktās nomas maksas līdzeklis (saistības)</span><span class="sxs-lookup"><span data-stu-id="4c654-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="4c654-168">Šis konts ir saistīts ar atlikto nomas masas līdzekli vai saistībām, ko sagatavoja atliktās nomas maksas apstrādes noma.</span><span class="sxs-lookup"><span data-stu-id="4c654-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="4c654-169">Šis konts tiek debetēts, ja rēķins ir grāmatots ar atliktu nomas maksas apstrādes nomu, ja nomas maksājuma summa ir lielāka par perioda taisnvirziena nomas izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="4c654-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="4c654-170">Tas tiek kreditēts, ja nomas maksa ir mazāka par perioda taisnvirziena nomas izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="4c654-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="4c654-171">**Žurnāla ierakstu piemēri**: nomas maksājums (atliktās nomas maksas noma)</span><span class="sxs-lookup"><span data-stu-id="4c654-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="4c654-172">**Debets**: nomas izdevumi XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="4c654-173">**Kredīts**: atliktās nomas maksas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="4c654-174">**Kredīts**: kreditora maksājums/nomas maksājums XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="4c654-175">Nomas izdevumi</span><span class="sxs-lookup"><span data-stu-id="4c654-175">Lease expense</span></span>

<span data-ttu-id="4c654-176">Konts ir saistīts ar nomas izdevumiem, ja noma tiek klasificēta kā atlikta nomas maksas apstrādes noma.</span><span class="sxs-lookup"><span data-stu-id="4c654-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="4c654-177">Šis konts tiek debetēts, ja rēķins ir grāmatots ar atlikto nomasas maksas apstrādes nomu.</span><span class="sxs-lookup"><span data-stu-id="4c654-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="4c654-178">**Žurnāla ierakstu piemēri**: nomas maksājums (atliktās nomas maksas noma)</span><span class="sxs-lookup"><span data-stu-id="4c654-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="4c654-179">**Debets**: nomas izdevumi XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="4c654-180">**Kredīts**: atliktās nomas maksas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="4c654-181">**Kredīts**: kreditora maksājums/nomas maksājums XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="4c654-182">Vērtības samazinājuma izdevumi</span><span class="sxs-lookup"><span data-stu-id="4c654-182">Impairment expense</span></span>

<span data-ttu-id="4c654-183">Konts tiek iegrāmatots, ja noma ir samazinājusies.</span><span class="sxs-lookup"><span data-stu-id="4c654-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="4c654-184">Šis konts tiek debetēts, bet LLT līdzekļu konts tiek tieši kreditēts.</span><span class="sxs-lookup"><span data-stu-id="4c654-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="4c654-185">**Žurnāla ierakstu piemērs**: nomas maksājums</span><span class="sxs-lookup"><span data-stu-id="4c654-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="4c654-186">**Debets**: vērtības samazinājuma izdevumi XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="4c654-187">**Kredīts**: LLT līdzeklis XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="4c654-188">Nomas maksājums</span><span class="sxs-lookup"><span data-stu-id="4c654-188">Lease payment</span></span>

<span data-ttu-id="4c654-189">Konts tiek iegrāmatots, ja parametrs **Maksāt kreditoram** ir izslēgts.</span><span class="sxs-lookup"><span data-stu-id="4c654-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="4c654-190">Tiek kreditēts šis konts, nevis kreditori, ja parametrs ir izslēgts.</span><span class="sxs-lookup"><span data-stu-id="4c654-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="4c654-191">**Žurnāla ierakstu piemērs**: nomas maksājums</span><span class="sxs-lookup"><span data-stu-id="4c654-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="4c654-192">**Debets**: nomas saistības XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="4c654-193">**Kredīts**: nomas maksājums XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="4c654-194">Izdevumu tipa grāmatojumi</span><span class="sxs-lookup"><span data-stu-id="4c654-194">Expense type postings</span></span>

<span data-ttu-id="4c654-195">Katram izdevumu tipam atlasītais konts tiek debetēts, ja tiek ģenerēts maksājums par šo izdevumu tipu.</span><span class="sxs-lookup"><span data-stu-id="4c654-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="4c654-196">Piemēram, konts, kas ir norādīts izmaksu tipam **Apdrošināšana**, tiek debetēts ikreiz, kad tiek izveidots rēķins vai maksājumu žurnāla ieraksts no izpildes izmaksu grafika apdrošināšanas izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="4c654-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="4c654-197">**Žurnāla ierakstu piemērs**: apdrošināšanas maksājums</span><span class="sxs-lookup"><span data-stu-id="4c654-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="4c654-198">**Debets**: apdrošināšanas izdevumu tipa konts XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="4c654-199">**Kredīts**: korespondējošais konts XXX</span><span class="sxs-lookup"><span data-stu-id="4c654-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="4c654-200">Korespondējošais konts tiek atlasīts nomas līmenī rindās, kas attiecas uz izpildes izmaksu maksājumu grafiku.</span><span class="sxs-lookup"><span data-stu-id="4c654-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="4c654-201">Šo korespondējošo kontu var saistīt ar kreditoru vai ar Virsgrāmatas kontu.</span><span class="sxs-lookup"><span data-stu-id="4c654-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
