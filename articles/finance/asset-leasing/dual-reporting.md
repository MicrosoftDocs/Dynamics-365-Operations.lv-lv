---
title: Duālie pārskati
description: Šajā tēmā ir sniegts piemērs, kā varat izpildīt gan starptautiskā finanšu pārskatu standarta (International Financial Reporting Standard — IFRS), gan likumā noteiktās prasības pārskatiem līdzekļu nomā.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 86f42f8db707f3b8c62b9ec4c39ad6464f080748
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881160"
---
# <a name="dual-reporting"></a><span data-ttu-id="a622f-103">Duālie pārskati</span><span class="sxs-lookup"><span data-stu-id="a622f-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a622f-104">Šajā tēmā ir sniegts piemērs, kā varat izpildīt gan starptautiskā finanšu pārskatu standarta (International Financial Reporting Standard — IFRS), gan likumā noteiktās prasības pārskatiem līdzekļu nomā.</span><span class="sxs-lookup"><span data-stu-id="a622f-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="a622f-105">Ir nepieciešams labi pazīt grāmatošanas līmeņus Microsoft Dynamics 365 Finance, tas padarīs šo piemēru vieglāk saprotamu.</span><span class="sxs-lookup"><span data-stu-id="a622f-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="a622f-106">Paraugs</span><span class="sxs-lookup"><span data-stu-id="a622f-106">Example</span></span>

<span data-ttu-id="a622f-107">Tālāk minētais piemērs uzskaita nomu saskaņā ar Itālijā obligāto pārskatu sniegšanu, izmantojot gan skaudras naudas bāzes metodi, gan IFRS pārskata metodes.</span><span class="sxs-lookup"><span data-stu-id="a622f-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="a622f-108">Uzņēmumam ir jāizveido trīs grāmatas, lai uzskaitītu gan Itālijā obligātās prasības, gan IFRS 16 prasības.</span><span class="sxs-lookup"><span data-stu-id="a622f-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="a622f-109">Viena grāmata ir nepieciešama IFRS 16, viena ir nepieciešama obligātajām prasībām, un viena grāmata ir nepieciešama, lai automātiski anulētu obligātos grāmatojumus.</span><span class="sxs-lookup"><span data-stu-id="a622f-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="a622f-110">Grāmatas ir iestatītas, kā parādīts tālāk redzamajās tabulās.</span><span class="sxs-lookup"><span data-stu-id="a622f-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="a622f-111">**IFRS 16 grāmata**</span><span class="sxs-lookup"><span data-stu-id="a622f-111">**IFRS 16 book**</span></span>

<span data-ttu-id="a622f-112">IFRS 16 grāmata ir iestatīta tā, lai tā atbilstu IFRS 16 uzskaites standartam.</span><span class="sxs-lookup"><span data-stu-id="a622f-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="a622f-113">Visi ieraksti, kas tiek grāmatoti šajā grāmatā, tiks grāmatoti pielāgotajā slānī.</span><span class="sxs-lookup"><span data-stu-id="a622f-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="a622f-114">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="a622f-114">Name</span></span>                                    | <span data-ttu-id="a622f-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="a622f-116">Grāmatas tips</span><span class="sxs-lookup"><span data-stu-id="a622f-116">Book type</span></span>                               | <span data-ttu-id="a622f-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="a622f-117">IFRS 16</span></span>        |
| <span data-ttu-id="a622f-118">Grāmatas apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-118">Book description</span></span>                        | <span data-ttu-id="a622f-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="a622f-119">IFRS 16</span></span>        |
| <span data-ttu-id="a622f-120">Grāmatošanas līmenis</span><span class="sxs-lookup"><span data-stu-id="a622f-120">Posting Layer</span></span>                           | <span data-ttu-id="a622f-121">1. pielāgotais līmenis</span><span class="sxs-lookup"><span data-stu-id="a622f-121">Custom layer 1</span></span> |
| <span data-ttu-id="a622f-122">Nomas veids</span><span class="sxs-lookup"><span data-stu-id="a622f-122">Lease Type</span></span>                              | <span data-ttu-id="a622f-123">Finance</span><span class="sxs-lookup"><span data-stu-id="a622f-123">Finance</span></span>        |
| <span data-ttu-id="a622f-124">Uzskaites struktūra</span><span class="sxs-lookup"><span data-stu-id="a622f-124">Accounting Framework</span></span>                    | <span data-ttu-id="a622f-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="a622f-125">IFRS 16</span></span>        |
| <span data-ttu-id="a622f-126">Nomas termiņa / lietderīgās lietošanas laika iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a622f-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="a622f-127">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-127">0.00</span></span>           |
| <span data-ttu-id="a622f-128">Pašreizējās vērtības / līdzekļa patiesās vērtības iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a622f-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="a622f-129">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-129">0.00</span></span>           |
| <span data-ttu-id="a622f-130">Īstermiņa slieksnis</span><span class="sxs-lookup"><span data-stu-id="a622f-130">Short-term threshold</span></span>                    | <span data-ttu-id="a622f-131">12.</span><span class="sxs-lookup"><span data-stu-id="a622f-131">12</span></span>             |
| <span data-ttu-id="a622f-132">Nelielas vērtības slieksnis</span><span class="sxs-lookup"><span data-stu-id="a622f-132">Low Value Threshold</span></span>                     | <span data-ttu-id="a622f-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-133">5,000.00</span></span>       |
| <span data-ttu-id="a622f-134">Maksāt kreditoram</span><span class="sxs-lookup"><span data-stu-id="a622f-134">Pay to Vendor</span></span>                           | <span data-ttu-id="a622f-135">Nr.</span><span class="sxs-lookup"><span data-stu-id="a622f-135">No</span></span>             |

<span data-ttu-id="a622f-136">**Obligātā grāmata**</span><span class="sxs-lookup"><span data-stu-id="a622f-136">**Statutory book**</span></span>

<span data-ttu-id="a622f-137">Obligātā grāmata ir skaidras naudas bāzes grāmata, kurā uzņēmums uzskaitīs nomas izdevumus kā skaidras naudas summu, kas katru mēnesi tiek maksāta par īri.</span><span class="sxs-lookup"><span data-stu-id="a622f-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="a622f-138">Šī grāmata nerada līdzekļa lietošanas tiesības (LLT) vai nomas saistības.</span><span class="sxs-lookup"><span data-stu-id="a622f-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="a622f-139">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="a622f-139">Name</span></span>                                    | <span data-ttu-id="a622f-140">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="a622f-141">Grāmatas tips</span><span class="sxs-lookup"><span data-stu-id="a622f-141">Book type</span></span>                               | <span data-ttu-id="a622f-142">Obligāta</span><span class="sxs-lookup"><span data-stu-id="a622f-142">Statutory</span></span>   |
| <span data-ttu-id="a622f-143">Grāmatas apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-143">Book description</span></span>                        | <span data-ttu-id="a622f-144">Vietējie vispārpieņemtie grāmatvedības principi</span><span class="sxs-lookup"><span data-stu-id="a622f-144">Local GAAP</span></span>  |
| <span data-ttu-id="a622f-145">Grāmatošanas līmenis</span><span class="sxs-lookup"><span data-stu-id="a622f-145">Posting Layer</span></span>                           | <span data-ttu-id="a622f-146">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="a622f-146">Current</span></span>     |
| <span data-ttu-id="a622f-147">Nomas veids</span><span class="sxs-lookup"><span data-stu-id="a622f-147">Lease Type</span></span>                              | <span data-ttu-id="a622f-148">Automātiski</span><span class="sxs-lookup"><span data-stu-id="a622f-148">Automatic</span></span>   |
| <span data-ttu-id="a622f-149">Uzskaites struktūra</span><span class="sxs-lookup"><span data-stu-id="a622f-149">Accounting Framework</span></span>                    | <span data-ttu-id="a622f-150">Skaidras naudas bāze</span><span class="sxs-lookup"><span data-stu-id="a622f-150">Cash basis</span></span>  |
| <span data-ttu-id="a622f-151">Nomas termiņa / lietderīgās lietošanas laika iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a622f-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="a622f-152">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-152">0.00</span></span>        |
| <span data-ttu-id="a622f-153">Pašreizējās vērtības / līdzekļa patiesās vērtības iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a622f-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="a622f-154">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-154">0.00</span></span>        |
| <span data-ttu-id="a622f-155">Īstermiņa slieksnis</span><span class="sxs-lookup"><span data-stu-id="a622f-155">Short-term threshold</span></span>                    | <span data-ttu-id="a622f-156">0</span><span class="sxs-lookup"><span data-stu-id="a622f-156">0</span></span>           |
| <span data-ttu-id="a622f-157">Nelielas vērtības slieksnis</span><span class="sxs-lookup"><span data-stu-id="a622f-157">Low Value Threshold</span></span>                     | <span data-ttu-id="a622f-158">0</span><span class="sxs-lookup"><span data-stu-id="a622f-158">0</span></span>           |
| <span data-ttu-id="a622f-159">Maksāt kreditoram</span><span class="sxs-lookup"><span data-stu-id="a622f-159">Pay to Vendor</span></span>                           | <span data-ttu-id="a622f-160">Nr.</span><span class="sxs-lookup"><span data-stu-id="a622f-160">No</span></span>          |

<span data-ttu-id="a622f-161">**Obligātā anulēšanas grāmata**</span><span class="sxs-lookup"><span data-stu-id="a622f-161">**Statutory reversal book**</span></span>

<span data-ttu-id="a622f-162">Obligātā anulēšanas grāmata ir iestatīta tādā pašā veidā kā obligātā grāmata.</span><span class="sxs-lookup"><span data-stu-id="a622f-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="a622f-163">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="a622f-163">Name</span></span>                                    | <span data-ttu-id="a622f-164">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="a622f-165">Grāmatas tips</span><span class="sxs-lookup"><span data-stu-id="a622f-165">Book type</span></span>                               | <span data-ttu-id="a622f-166">Obligātā — anulēšanas</span><span class="sxs-lookup"><span data-stu-id="a622f-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="a622f-167">Grāmatas apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-167">Book description</span></span>                        | <span data-ttu-id="a622f-168">Rezervēt, lai anulētu obligāto grāmatu</span><span class="sxs-lookup"><span data-stu-id="a622f-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="a622f-169">Grāmatošanas līmenis</span><span class="sxs-lookup"><span data-stu-id="a622f-169">Posting Layer</span></span>                           | <span data-ttu-id="a622f-170">1. pielāgotais līmenis</span><span class="sxs-lookup"><span data-stu-id="a622f-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="a622f-171">Nomas veids</span><span class="sxs-lookup"><span data-stu-id="a622f-171">Lease Type</span></span>                              | <span data-ttu-id="a622f-172">Automātiski</span><span class="sxs-lookup"><span data-stu-id="a622f-172">Automatic</span></span>                      |
| <span data-ttu-id="a622f-173">Uzskaites struktūra</span><span class="sxs-lookup"><span data-stu-id="a622f-173">Accounting Framework</span></span>                    | <span data-ttu-id="a622f-174">Skaidras naudas bāze</span><span class="sxs-lookup"><span data-stu-id="a622f-174">Cash basis</span></span>                     |
| <span data-ttu-id="a622f-175">Nomas termiņa / lietderīgās lietošanas laika iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a622f-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="a622f-176">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-176">0.00</span></span>                           |
| <span data-ttu-id="a622f-177">Pašreizējās vērtības / līdzekļa patiesās vērtības iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a622f-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="a622f-178">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-178">0.00</span></span>                           |
| <span data-ttu-id="a622f-179">Īstermiņa slieksnis</span><span class="sxs-lookup"><span data-stu-id="a622f-179">Short-term threshold</span></span>                    | <span data-ttu-id="a622f-180">0</span><span class="sxs-lookup"><span data-stu-id="a622f-180">0</span></span>                              |
| <span data-ttu-id="a622f-181">Nelielas vērtības slieksnis</span><span class="sxs-lookup"><span data-stu-id="a622f-181">Low Value Threshold</span></span>                     | <span data-ttu-id="a622f-182">0</span><span class="sxs-lookup"><span data-stu-id="a622f-182">0</span></span>                              |
| <span data-ttu-id="a622f-183">Maksāt kreditoram</span><span class="sxs-lookup"><span data-stu-id="a622f-183">Pay to Vendor</span></span>                           | <span data-ttu-id="a622f-184">Nr.</span><span class="sxs-lookup"><span data-stu-id="a622f-184">No</span></span>                             |

<span data-ttu-id="a622f-185">Šim piemēram ir izveidota noma, kam ir tālāk norādītie iestatījumi cilnēs **Vispārīgi** un **Maksājuma grafika rindas**.</span><span class="sxs-lookup"><span data-stu-id="a622f-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="a622f-186">**Cilne Vispārīgi**</span><span class="sxs-lookup"><span data-stu-id="a622f-186">**General tab**</span></span>

| <span data-ttu-id="a622f-187">Lauks</span><span class="sxs-lookup"><span data-stu-id="a622f-187">Field</span></span>                      | <span data-ttu-id="a622f-188">Vērtība</span><span class="sxs-lookup"><span data-stu-id="a622f-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="a622f-189">Salīdzināmā aizņēmuma procentu likme</span><span class="sxs-lookup"><span data-stu-id="a622f-189">Incremental borrowing rate</span></span> | <span data-ttu-id="a622f-190">5%</span><span class="sxs-lookup"><span data-stu-id="a622f-190">5%</span></span>               |
| <span data-ttu-id="a622f-191">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="a622f-191">Commencement date</span></span>          | <span data-ttu-id="a622f-192">01.01.2020.</span><span class="sxs-lookup"><span data-stu-id="a622f-192">1/1/2020</span></span>         |
| <span data-ttu-id="a622f-193">Nomas grupa</span><span class="sxs-lookup"><span data-stu-id="a622f-193">Lease group</span></span>                | <span data-ttu-id="a622f-194">Ēkas</span><span class="sxs-lookup"><span data-stu-id="a622f-194">Buildings</span></span>        |
| <span data-ttu-id="a622f-195">Kreditors</span><span class="sxs-lookup"><span data-stu-id="a622f-195">Vendor</span></span>                     | <span data-ttu-id="a622f-196">1001</span><span class="sxs-lookup"><span data-stu-id="a622f-196">1001</span></span>             |
| <span data-ttu-id="a622f-197">Līdzekļa patiesā vērtība</span><span class="sxs-lookup"><span data-stu-id="a622f-197">Fair value of the asset</span></span>    | <span data-ttu-id="a622f-198">245,000</span><span class="sxs-lookup"><span data-stu-id="a622f-198">245,000</span></span>          |
| <span data-ttu-id="a622f-199">Līdzekļa lietderīgās lietošanas laiks</span><span class="sxs-lookup"><span data-stu-id="a622f-199">Asset useful life</span></span>          | <span data-ttu-id="a622f-200">120</span><span class="sxs-lookup"><span data-stu-id="a622f-200">120</span></span>              |
| <span data-ttu-id="a622f-201">Gada maksājuma veids</span><span class="sxs-lookup"><span data-stu-id="a622f-201">Annuity type</span></span>               | <span data-ttu-id="a622f-202">Parastais gada maksājums</span><span class="sxs-lookup"><span data-stu-id="a622f-202">Ordinary annuity</span></span> |
| <span data-ttu-id="a622f-203">Pievienošanas intervāls</span><span class="sxs-lookup"><span data-stu-id="a622f-203">Compounding interval</span></span>       | <span data-ttu-id="a622f-204">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="a622f-204">Monthly</span></span>          |

<span data-ttu-id="a622f-205">**Cilne Maksājumu grafika rindas**</span><span class="sxs-lookup"><span data-stu-id="a622f-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="a622f-206">Lauks</span><span class="sxs-lookup"><span data-stu-id="a622f-206">Field</span></span>             | <span data-ttu-id="a622f-207">Vērtība</span><span class="sxs-lookup"><span data-stu-id="a622f-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="a622f-208">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="a622f-208">Start date</span></span>        | <span data-ttu-id="a622f-209">01.01.2020.</span><span class="sxs-lookup"><span data-stu-id="a622f-209">1/1/2020</span></span>   |
| <span data-ttu-id="a622f-210">Perioda intervāls</span><span class="sxs-lookup"><span data-stu-id="a622f-210">Period interval</span></span>   | <span data-ttu-id="a622f-211">Mēneši</span><span class="sxs-lookup"><span data-stu-id="a622f-211">Months</span></span>     |
| <span data-ttu-id="a622f-212">Periodi</span><span class="sxs-lookup"><span data-stu-id="a622f-212">Periods</span></span>           | <span data-ttu-id="a622f-213">24</span><span class="sxs-lookup"><span data-stu-id="a622f-213">24</span></span>         |
| <span data-ttu-id="a622f-214">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="a622f-214">End date</span></span>          | <span data-ttu-id="a622f-215">31.12.2020.</span><span class="sxs-lookup"><span data-stu-id="a622f-215">12/31/2020</span></span> |
| <span data-ttu-id="a622f-216">Maksājumu biežums</span><span class="sxs-lookup"><span data-stu-id="a622f-216">Payment frequency</span></span> | <span data-ttu-id="a622f-217">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="a622f-217">Monthly</span></span>    |
| <span data-ttu-id="a622f-218">Maksājuma summa</span><span class="sxs-lookup"><span data-stu-id="a622f-218">Payment amount</span></span>    | <span data-ttu-id="a622f-219">1000</span><span class="sxs-lookup"><span data-stu-id="a622f-219">1,000</span></span>      |

<span data-ttu-id="a622f-220">Lai šo nomu uzskaitītu divās struktūrās, jāizmanto pašreizējais grāmatošanas līmenis un pielāgotais grāmatošanas līmenis.</span><span class="sxs-lookup"><span data-stu-id="a622f-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="a622f-221">Tālāk redzamajā tabulā ir parādīts katra žurnāla ieraksta piemērs, kas nepieciešams pilnīgi atspoguļotu finanšu datus saskaņā ar katru pārskata standartu.</span><span class="sxs-lookup"><span data-stu-id="a622f-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="a622f-222">Pēc tam tiek sniegts detalizēts katra žurnāla ieraksta apraksts par nomas pirmo mēnesi.</span><span class="sxs-lookup"><span data-stu-id="a622f-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="a622f-223">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="a622f-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="a622f-224">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="a622f-225">Obligātā grāmata (pašreizējais slānis)</span><span class="sxs-lookup"><span data-stu-id="a622f-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="a622f-226">Pašreizējais slānis kopā</span><span class="sxs-lookup"><span data-stu-id="a622f-226">Current layer total</span></span></th>
<th><span data-ttu-id="a622f-227">Anulēšanas grāmata (pielāgotais slānis)</span><span class="sxs-lookup"><span data-stu-id="a622f-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="a622f-228">IFRS 16 grāmata (pielāgotais slānis)</span><span class="sxs-lookup"><span data-stu-id="a622f-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="a622f-229">Pašreizējā slāņa + pielāgotā slāņa kopsumma</span><span class="sxs-lookup"><span data-stu-id="a622f-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a622f-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="a622f-230">JE-100</span></span></th>
<th><span data-ttu-id="a622f-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="a622f-231">JE-110</span></span></th>
<th><span data-ttu-id="a622f-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="a622f-232">JE-120</span></span></th>
<th><span data-ttu-id="a622f-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="a622f-233">JE-130</span></span></th>
<th><span data-ttu-id="a622f-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="a622f-234">JE-140</span></span></th>
<th><span data-ttu-id="a622f-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="a622f-235">JE-150</span></span></th>
<th><span data-ttu-id="a622f-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="a622f-236">JE-160</span></span></th>
<th><span data-ttu-id="a622f-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="a622f-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a622f-238">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="a622f-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a622f-239">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="a622f-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a622f-240">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="a622f-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a622f-241">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="a622f-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a622f-242">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="a622f-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a622f-243">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="a622f-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a622f-244">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="a622f-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a622f-245">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="a622f-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a622f-246">1</span><span class="sxs-lookup"><span data-stu-id="a622f-246">1</span></span></td>
<td><span data-ttu-id="a622f-247">Nomas izdevumi</span><span class="sxs-lookup"><span data-stu-id="a622f-247">Lease expense</span></span></td>
<td><span data-ttu-id="a622f-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-249">1,000.00</span></span></td>
<td><span data-ttu-id="a622f-250">-1000,00</span><span class="sxs-lookup"><span data-stu-id="a622f-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-251">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-252">2</span><span class="sxs-lookup"><span data-stu-id="a622f-252">2</span></span></td>
<td><span data-ttu-id="a622f-253">Bankas komisija</span><span class="sxs-lookup"><span data-stu-id="a622f-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-254">3.00</span><span class="sxs-lookup"><span data-stu-id="a622f-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-255">3.00</span><span class="sxs-lookup"><span data-stu-id="a622f-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-256">3.00</span><span class="sxs-lookup"><span data-stu-id="a622f-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-257">3</span><span class="sxs-lookup"><span data-stu-id="a622f-257">3</span></span></td>
<td><span data-ttu-id="a622f-258">PVN izdevumi</span><span class="sxs-lookup"><span data-stu-id="a622f-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-259">5.00</span><span class="sxs-lookup"><span data-stu-id="a622f-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-260">5.00</span><span class="sxs-lookup"><span data-stu-id="a622f-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-261">5.00</span><span class="sxs-lookup"><span data-stu-id="a622f-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-262">4</span><span class="sxs-lookup"><span data-stu-id="a622f-262">4</span></span></td>
<td><span data-ttu-id="a622f-263">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="a622f-263">Clearing account</span></span></td>
<td><span data-ttu-id="a622f-264">-1000,00</span><span class="sxs-lookup"><span data-stu-id="a622f-264">-1,000.00</span></span></td>
<td><span data-ttu-id="a622f-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-266">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-266">0.00</span></span></td>
<td><span data-ttu-id="a622f-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-268">-1000,00</span><span class="sxs-lookup"><span data-stu-id="a622f-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-269">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-270">5</span><span class="sxs-lookup"><span data-stu-id="a622f-270">5</span></span></td>
<td><span data-ttu-id="a622f-271">Kreditoru parādi</span><span class="sxs-lookup"><span data-stu-id="a622f-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-272">-1008,00</span><span class="sxs-lookup"><span data-stu-id="a622f-272">-1,008.00</span></span></td>
<td><span data-ttu-id="a622f-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a622f-273">1,008.00</span></span></td>
<td><span data-ttu-id="a622f-274">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-275">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-276">6</span><span class="sxs-lookup"><span data-stu-id="a622f-276">6</span></span></td>
<td><span data-ttu-id="a622f-277">LLT līdzeklis</span><span class="sxs-lookup"><span data-stu-id="a622f-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-278">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="a622f-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="a622f-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-281">7</span><span class="sxs-lookup"><span data-stu-id="a622f-281">7</span></span></td>
<td><span data-ttu-id="a622f-282">Finanšu nomas saistības</span><span class="sxs-lookup"><span data-stu-id="a622f-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-283">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="a622f-284">-22,794.00</span></span></td>
<td><span data-ttu-id="a622f-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-285">1,000.00</span></span></td>
<td><span data-ttu-id="a622f-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="a622f-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="a622f-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-288">8</span><span class="sxs-lookup"><span data-stu-id="a622f-288">8</span></span></td>
<td><span data-ttu-id="a622f-289">Maksājamie procenti</span><span class="sxs-lookup"><span data-stu-id="a622f-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-290">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-291">94.97</span><span class="sxs-lookup"><span data-stu-id="a622f-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-292">94.97</span><span class="sxs-lookup"><span data-stu-id="a622f-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-293">9</span><span class="sxs-lookup"><span data-stu-id="a622f-293">9</span></span></td>
<td><span data-ttu-id="a622f-294">Kase</span><span class="sxs-lookup"><span data-stu-id="a622f-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-295">-1008,00</span><span class="sxs-lookup"><span data-stu-id="a622f-295">-1,008.00</span></span></td>
<td><span data-ttu-id="a622f-296">-1008,00</span><span class="sxs-lookup"><span data-stu-id="a622f-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-297">-1008,00</span><span class="sxs-lookup"><span data-stu-id="a622f-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-298">10.</span><span class="sxs-lookup"><span data-stu-id="a622f-298">10</span></span></td>
<td><span data-ttu-id="a622f-299">Nolietojuma izmaksas</span><span class="sxs-lookup"><span data-stu-id="a622f-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-300">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-301">949.75</span><span class="sxs-lookup"><span data-stu-id="a622f-301">949.75</span></span></td>
<td><span data-ttu-id="a622f-302">949.75</span><span class="sxs-lookup"><span data-stu-id="a622f-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-303">11.</span><span class="sxs-lookup"><span data-stu-id="a622f-303">11</span></span></td>
<td><span data-ttu-id="a622f-304">Uzkrātais nolietojums</span><span class="sxs-lookup"><span data-stu-id="a622f-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-305">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="a622f-306">-949.75</span></span></td>
<td><span data-ttu-id="a622f-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="a622f-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a622f-308">Kā redzams iepriekšējā tabulā, ir nepieciešamas trīs grāmatas, lai sniegtu pārskatu saskaņā obligāto un IFRS pārskatu sniegšanu.</span><span class="sxs-lookup"><span data-stu-id="a622f-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="a622f-309">Obligātajā grāmatā ierakstīti nomas maksājumi saskaņā ar noteikumiem par skaidras naudas bāzes uzskaiti, pamatojoties uz pašreizējo slāni.</span><span class="sxs-lookup"><span data-stu-id="a622f-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="a622f-310">Obligātā anulēšanas grāmata anulē obligātos žurnāla ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a622f-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="a622f-311">IFRS 16 grāmata izveido žurnāla ierakstus, kas ir nepieciešami saskaņā ar IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="a622f-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="a622f-312">Noma ir jāievada tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="a622f-312">You must enter a lease only one time.</span></span> <span data-ttu-id="a622f-313">Pēc tam varat atvērt lapu **Grāmatas**, lai skatītu visas ar nomu saistītās grāmatas.</span><span class="sxs-lookup"><span data-stu-id="a622f-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="a622f-314">Kad izveidojat grāmatas, visām trim no tām jābūt saistītām ar to pašu nomas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a622f-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="a622f-315">Pirmajā žurnāla ierakstā reģistrēti nomas izdevumi saskaņā ar obligāto grāmatu.</span><span class="sxs-lookup"><span data-stu-id="a622f-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="a622f-316">Varat izveidot maksājumus vai nu partijā, vai atlasot maksājumu grafiku obligātajā grāmatā.</span><span class="sxs-lookup"><span data-stu-id="a622f-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="a622f-317">Šajā piemērā tālāk norādītais žurnāla ieraksts ir izveidots obligātajai grāmatai no maksājumu grafika.</span><span class="sxs-lookup"><span data-stu-id="a622f-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="a622f-318">Nomas maksājums — 01.31.2020. — JE 100</span><span class="sxs-lookup"><span data-stu-id="a622f-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="a622f-319">Konta veids</span><span class="sxs-lookup"><span data-stu-id="a622f-319">Account type</span></span> | <span data-ttu-id="a622f-320">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="a622f-320">Account number</span></span> | <span data-ttu-id="a622f-321">Līmenis</span><span class="sxs-lookup"><span data-stu-id="a622f-321">Layer</span></span>   | <span data-ttu-id="a622f-322">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-322">Account description</span></span> | <span data-ttu-id="a622f-323">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-323">Debit</span></span>    | <span data-ttu-id="a622f-324">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="a622f-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-325">Ledger</span></span>       | <span data-ttu-id="a622f-326">1</span><span class="sxs-lookup"><span data-stu-id="a622f-326">1</span></span>              | <span data-ttu-id="a622f-327">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="a622f-327">Current</span></span> | <span data-ttu-id="a622f-328">Nomas izdevumi</span><span class="sxs-lookup"><span data-stu-id="a622f-328">Lease expense</span></span>       | <span data-ttu-id="a622f-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-329">1,000.00</span></span> |          |
| <span data-ttu-id="a622f-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-330">Ledger</span></span>       | <span data-ttu-id="a622f-331">4</span><span class="sxs-lookup"><span data-stu-id="a622f-331">4</span></span>              | <span data-ttu-id="a622f-332">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="a622f-332">Current</span></span> | <span data-ttu-id="a622f-333">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="a622f-333">Clearing account</span></span>    |          | <span data-ttu-id="a622f-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-334">1,000.00</span></span> |

<span data-ttu-id="a622f-335">Par Kreditoru rēķiniem atbildīgais darbinieks izmanto standarta Dynamics 365 funkcionalitāti, lai izveidotu rēķinu, kas jāmaksā par nomu ārpus Līdzekļu nomas.</span><span class="sxs-lookup"><span data-stu-id="a622f-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="a622f-336">Tomēr tā vietā, lai atlasītu **Nomas izdevumi** kā debeta kontu, par Kreditoru rēķiniem atbildīgais darbinieks atlasa dzēšanas kontu, lai ģenerētu tālāk norādīto ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a622f-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="a622f-337">KR process — 31.012020. — JE 110</span><span class="sxs-lookup"><span data-stu-id="a622f-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="a622f-338">Konta veids</span><span class="sxs-lookup"><span data-stu-id="a622f-338">Account type</span></span> | <span data-ttu-id="a622f-339">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="a622f-339">Account number</span></span> | <span data-ttu-id="a622f-340">Līmenis</span><span class="sxs-lookup"><span data-stu-id="a622f-340">Layer</span></span>   | <span data-ttu-id="a622f-341">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-341">Account description</span></span> | <span data-ttu-id="a622f-342">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-342">Debit</span></span>    | <span data-ttu-id="a622f-343">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="a622f-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-344">Ledger</span></span>       | <span data-ttu-id="a622f-345">4</span><span class="sxs-lookup"><span data-stu-id="a622f-345">4</span></span>              | <span data-ttu-id="a622f-346">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="a622f-346">Current</span></span> | <span data-ttu-id="a622f-347">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="a622f-347">Clearing account</span></span>    | <span data-ttu-id="a622f-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-348">1,000.00</span></span> |          |
| <span data-ttu-id="a622f-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-349">Ledger</span></span>       | <span data-ttu-id="a622f-350">2</span><span class="sxs-lookup"><span data-stu-id="a622f-350">2</span></span>              | <span data-ttu-id="a622f-351">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="a622f-351">Current</span></span> | <span data-ttu-id="a622f-352">Bankas komisija</span><span class="sxs-lookup"><span data-stu-id="a622f-352">Bank fee</span></span>            | <span data-ttu-id="a622f-353">3.00</span><span class="sxs-lookup"><span data-stu-id="a622f-353">3.00</span></span>     |          |
| <span data-ttu-id="a622f-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-354">Ledger</span></span>       | <span data-ttu-id="a622f-355">3</span><span class="sxs-lookup"><span data-stu-id="a622f-355">3</span></span>              | <span data-ttu-id="a622f-356">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="a622f-356">Current</span></span> | <span data-ttu-id="a622f-357">PVN izdevumi</span><span class="sxs-lookup"><span data-stu-id="a622f-357">VAT expense</span></span>         | <span data-ttu-id="a622f-358">5.00</span><span class="sxs-lookup"><span data-stu-id="a622f-358">5.00</span></span>     |          |
| <span data-ttu-id="a622f-359">Kreditors</span><span class="sxs-lookup"><span data-stu-id="a622f-359">Vendor</span></span>       | <span data-ttu-id="a622f-360">5</span><span class="sxs-lookup"><span data-stu-id="a622f-360">5</span></span>              | <span data-ttu-id="a622f-361">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="a622f-361">Current</span></span> | <span data-ttu-id="a622f-362">Kreditoru parādi</span><span class="sxs-lookup"><span data-stu-id="a622f-362">Accounts payable</span></span>    |          | <span data-ttu-id="a622f-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a622f-363">1,008.00</span></span> |

<span data-ttu-id="a622f-364">Kad izraksts tiek izsniegts kreditoram, veiciet parastu maksāšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="a622f-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="a622f-365">Šī procesa laikā tiek ģenerēts tālāk norādītais žurnāla ieraksts.</span><span class="sxs-lookup"><span data-stu-id="a622f-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="a622f-366">Skaidras naudas maksājums – 31.01.2020. – JE 120</span><span class="sxs-lookup"><span data-stu-id="a622f-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="a622f-367">Konta veids</span><span class="sxs-lookup"><span data-stu-id="a622f-367">Account type</span></span> | <span data-ttu-id="a622f-368">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="a622f-368">Account number</span></span> | <span data-ttu-id="a622f-369">Līmenis</span><span class="sxs-lookup"><span data-stu-id="a622f-369">Layer</span></span>   | <span data-ttu-id="a622f-370">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-370">Account description</span></span> | <span data-ttu-id="a622f-371">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-371">Debit</span></span>    | <span data-ttu-id="a622f-372">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="a622f-373">Kreditors</span><span class="sxs-lookup"><span data-stu-id="a622f-373">Vendor</span></span>       | <span data-ttu-id="a622f-374">5</span><span class="sxs-lookup"><span data-stu-id="a622f-374">5</span></span>              | <span data-ttu-id="a622f-375">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="a622f-375">Current</span></span> | <span data-ttu-id="a622f-376">Parādi kreditoriem</span><span class="sxs-lookup"><span data-stu-id="a622f-376">Accounts Payable</span></span>    | <span data-ttu-id="a622f-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a622f-377">1,008.00</span></span> |          |
| <span data-ttu-id="a622f-378">Banka</span><span class="sxs-lookup"><span data-stu-id="a622f-378">Bank</span></span>         | <span data-ttu-id="a622f-379">9</span><span class="sxs-lookup"><span data-stu-id="a622f-379">9</span></span>              | <span data-ttu-id="a622f-380">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="a622f-380">Current</span></span> | <span data-ttu-id="a622f-381">Kase</span><span class="sxs-lookup"><span data-stu-id="a622f-381">Cash</span></span>                |          | <span data-ttu-id="a622f-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a622f-382">1,008.00</span></span> |

<span data-ttu-id="a622f-383">Šajā brīdī esat pilnībā uzskaitījis šo nomu saskaņā ar obligātajām prasībām un varat ģenerēt apgrozījuma bilanci, izmantojot pašreizējo slāni.</span><span class="sxs-lookup"><span data-stu-id="a622f-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="a622f-384">Sistēma izveido apgrozījuma bilanci ar tālāk norādītajiem skaitļiem.</span><span class="sxs-lookup"><span data-stu-id="a622f-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="a622f-385">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="a622f-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="a622f-386">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="a622f-387">Obligātā grāmata (pašreizējais slānis)</span><span class="sxs-lookup"><span data-stu-id="a622f-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="a622f-388">Pašreizējais slānis kopā</span><span class="sxs-lookup"><span data-stu-id="a622f-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a622f-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="a622f-389">JE-100</span></span></th>
<th><span data-ttu-id="a622f-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="a622f-390">JE-110</span></span></th>
<th><span data-ttu-id="a622f-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="a622f-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a622f-392">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="a622f-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a622f-393">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="a622f-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a622f-394">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="a622f-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a622f-395">1</span><span class="sxs-lookup"><span data-stu-id="a622f-395">1</span></span></td>
<td><span data-ttu-id="a622f-396">Nomas izdevumi</span><span class="sxs-lookup"><span data-stu-id="a622f-396">Lease expense</span></span></td>
<td><span data-ttu-id="a622f-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-399">2</span><span class="sxs-lookup"><span data-stu-id="a622f-399">2</span></span></td>
<td><span data-ttu-id="a622f-400">Bankas komisija</span><span class="sxs-lookup"><span data-stu-id="a622f-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-401">3.00</span><span class="sxs-lookup"><span data-stu-id="a622f-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-402">3.00</span><span class="sxs-lookup"><span data-stu-id="a622f-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-403">3</span><span class="sxs-lookup"><span data-stu-id="a622f-403">3</span></span></td>
<td><span data-ttu-id="a622f-404">PVN izdevumi</span><span class="sxs-lookup"><span data-stu-id="a622f-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-405">5.00</span><span class="sxs-lookup"><span data-stu-id="a622f-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-406">5.00</span><span class="sxs-lookup"><span data-stu-id="a622f-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-407">4</span><span class="sxs-lookup"><span data-stu-id="a622f-407">4</span></span></td>
<td><span data-ttu-id="a622f-408">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="a622f-408">Clearing account</span></span></td>
<td><span data-ttu-id="a622f-409">-1000,00</span><span class="sxs-lookup"><span data-stu-id="a622f-409">-1,000.00</span></span></td>
<td><span data-ttu-id="a622f-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-411">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-412">5</span><span class="sxs-lookup"><span data-stu-id="a622f-412">5</span></span></td>
<td><span data-ttu-id="a622f-413">Kreditoru parādi</span><span class="sxs-lookup"><span data-stu-id="a622f-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="a622f-414">-1008,00</span><span class="sxs-lookup"><span data-stu-id="a622f-414">-1,008.00</span></span></td>
<td><span data-ttu-id="a622f-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a622f-415">1,008.00</span></span></td>
<td><span data-ttu-id="a622f-416">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-417">6</span><span class="sxs-lookup"><span data-stu-id="a622f-417">6</span></span></td>
<td><span data-ttu-id="a622f-418">LLT līdzeklis</span><span class="sxs-lookup"><span data-stu-id="a622f-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-419">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-420">7</span><span class="sxs-lookup"><span data-stu-id="a622f-420">7</span></span></td>
<td><span data-ttu-id="a622f-421">Finanšu nomas saistības</span><span class="sxs-lookup"><span data-stu-id="a622f-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-422">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-423">8</span><span class="sxs-lookup"><span data-stu-id="a622f-423">8</span></span></td>
<td><span data-ttu-id="a622f-424">Maksājamie procenti</span><span class="sxs-lookup"><span data-stu-id="a622f-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-425">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-426">9</span><span class="sxs-lookup"><span data-stu-id="a622f-426">9</span></span></td>
<td><span data-ttu-id="a622f-427">Kase</span><span class="sxs-lookup"><span data-stu-id="a622f-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-428">-1008,00</span><span class="sxs-lookup"><span data-stu-id="a622f-428">-1,008.00</span></span></td>
<td><span data-ttu-id="a622f-429">-1008,00</span><span class="sxs-lookup"><span data-stu-id="a622f-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-430">10.</span><span class="sxs-lookup"><span data-stu-id="a622f-430">10</span></span></td>
<td><span data-ttu-id="a622f-431">Nolietojuma izmaksas</span><span class="sxs-lookup"><span data-stu-id="a622f-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-432">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a622f-433">11.</span><span class="sxs-lookup"><span data-stu-id="a622f-433">11</span></span></td>
<td><span data-ttu-id="a622f-434">Uzkrātais nolietojums</span><span class="sxs-lookup"><span data-stu-id="a622f-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a622f-435">0.00</span><span class="sxs-lookup"><span data-stu-id="a622f-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a622f-436">Ja vēlaties izmantot IFRS 16 skaitļus, lai palaistu to pašu apgrozījuma bilanci, ir jāanulē obligātie uzskaites žurnāla ieraksti un jāgrāmato IFRS 16 žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="a622f-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="a622f-437">Lai anulētu obligātos žurnāla ierakstus, šajā piemērā ir iekļauta obligātā anulēšanas grāmata ar tādiem pašiem iestatījumiem kā obligātajai grāmatai, bet ar pretēju grāmatošanas profilu.</span><span class="sxs-lookup"><span data-stu-id="a622f-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="a622f-438">Piemēram, obligātā grāmata *debetēja* nomas izdevumu kontu, bet anulēšanas grāmata *kreditēs* šo kontu.</span><span class="sxs-lookup"><span data-stu-id="a622f-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="a622f-439">Šīs attiecības ir viegli definētas Līdzekļu nomas grāmatošanas kontos lapā **Līdzekļu nomas parametri** lapā (**Līdzekļu noma \> Iestatījumi \> Līdzekļu nomas parametri**).</span><span class="sxs-lookup"><span data-stu-id="a622f-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="a622f-440">Kad tas pats process, kas tika izmantots obligātajai grāmatai, tiek izmantots anulēšanas grāmatai, tiek izveidots tālāk norādītais žurnāla ieraksts.</span><span class="sxs-lookup"><span data-stu-id="a622f-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="a622f-441">Atšķirība ir tāda, ka anulēšanas grāmata anulē obligātās grāmatas ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a622f-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="a622f-442">Anulēšanas ieraksti arī tiek veikti pielāgotā slānī.</span><span class="sxs-lookup"><span data-stu-id="a622f-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="a622f-443">Ja apgrozījuma bilance tiek palaista pašreizējā slānī, anulējošie žurnāla ieraksti nav ietverti.</span><span class="sxs-lookup"><span data-stu-id="a622f-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="a622f-444">Nomas maksājums — 01.31.2020. — JE 130</span><span class="sxs-lookup"><span data-stu-id="a622f-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="a622f-445">Konta veids</span><span class="sxs-lookup"><span data-stu-id="a622f-445">Account type</span></span> | <span data-ttu-id="a622f-446">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="a622f-446">Account number</span></span> | <span data-ttu-id="a622f-447">Līmenis</span><span class="sxs-lookup"><span data-stu-id="a622f-447">Layer</span></span>  | <span data-ttu-id="a622f-448">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-448">Account description</span></span> | <span data-ttu-id="a622f-449">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-449">Debit</span></span>    | <span data-ttu-id="a622f-450">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="a622f-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-451">Ledger</span></span>       | <span data-ttu-id="a622f-452">4</span><span class="sxs-lookup"><span data-stu-id="a622f-452">4</span></span>              | <span data-ttu-id="a622f-453">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="a622f-453">Custom</span></span> | <span data-ttu-id="a622f-454">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="a622f-454">Clearing account</span></span>    | <span data-ttu-id="a622f-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-455">1,000.00</span></span> |          |
| <span data-ttu-id="a622f-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-456">Ledger</span></span>       | <span data-ttu-id="a622f-457">1</span><span class="sxs-lookup"><span data-stu-id="a622f-457">1</span></span>              | <span data-ttu-id="a622f-458">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="a622f-458">Custom</span></span> | <span data-ttu-id="a622f-459">Nomas izdevumi</span><span class="sxs-lookup"><span data-stu-id="a622f-459">Lease expense</span></span>       |          | <span data-ttu-id="a622f-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-460">1,000.00</span></span> |

<span data-ttu-id="a622f-461">Tagad, kad ir likvidēti obligātā žurnāla ieraksti, tiks grāmatoti visi žurnāla ieraksti, kas ir nepieciešami IFRS 16 grāmatai.</span><span class="sxs-lookup"><span data-stu-id="a622f-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="a622f-462">Šie ieraksti ietver sākotnējo LLT un saistību atzīšanu, kā arī procentu un nolietojuma ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a622f-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="a622f-463">Sākotnējā atzīšana — 01.01.2020. — JE 140</span><span class="sxs-lookup"><span data-stu-id="a622f-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="a622f-464">Konta veids</span><span class="sxs-lookup"><span data-stu-id="a622f-464">Account type</span></span> | <span data-ttu-id="a622f-465">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="a622f-465">Account number</span></span> | <span data-ttu-id="a622f-466">Līmenis</span><span class="sxs-lookup"><span data-stu-id="a622f-466">Layer</span></span>  | <span data-ttu-id="a622f-467">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-467">Account description</span></span>      | <span data-ttu-id="a622f-468">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-468">Debit</span></span>     | <span data-ttu-id="a622f-469">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="a622f-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-470">Ledger</span></span>       | <span data-ttu-id="a622f-471">6</span><span class="sxs-lookup"><span data-stu-id="a622f-471">6</span></span>              | <span data-ttu-id="a622f-472">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="a622f-472">Custom</span></span> | <span data-ttu-id="a622f-473">LLT līdzeklis</span><span class="sxs-lookup"><span data-stu-id="a622f-473">ROU Asset</span></span>                | <span data-ttu-id="a622f-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="a622f-474">22,793.90</span></span> |           |
| <span data-ttu-id="a622f-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-475">Ledger</span></span>       | <span data-ttu-id="a622f-476">7</span><span class="sxs-lookup"><span data-stu-id="a622f-476">7</span></span>              | <span data-ttu-id="a622f-477">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="a622f-477">Custom</span></span> | <span data-ttu-id="a622f-478">Finanšu nomas saistības</span><span class="sxs-lookup"><span data-stu-id="a622f-478">Finance lease obligation</span></span> |           | <span data-ttu-id="a622f-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="a622f-479">22,793.90</span></span> |

<span data-ttu-id="a622f-480">Nomas maksājums tiek grāmatots līdzīgi citi nomas maksājumi.</span><span class="sxs-lookup"><span data-stu-id="a622f-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="a622f-481">Dzēšanas konta izmantošanas iemesls ir nodrošināt, ka skaidra nauda tiek kreditēta tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="a622f-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="a622f-482">Nomas maksājums — 01.31.2020. — JE 150</span><span class="sxs-lookup"><span data-stu-id="a622f-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="a622f-483">Konta veids</span><span class="sxs-lookup"><span data-stu-id="a622f-483">Account type</span></span> | <span data-ttu-id="a622f-484">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="a622f-484">Account number</span></span> | <span data-ttu-id="a622f-485">Līmenis</span><span class="sxs-lookup"><span data-stu-id="a622f-485">Layer</span></span>  | <span data-ttu-id="a622f-486">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-486">Account description</span></span>      | <span data-ttu-id="a622f-487">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-487">Debit</span></span>    | <span data-ttu-id="a622f-488">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="a622f-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-489">Ledger</span></span>       | <span data-ttu-id="a622f-490">7</span><span class="sxs-lookup"><span data-stu-id="a622f-490">7</span></span>              | <span data-ttu-id="a622f-491">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="a622f-491">Custom</span></span> | <span data-ttu-id="a622f-492">Finanšu nomas saistības</span><span class="sxs-lookup"><span data-stu-id="a622f-492">Finance lease obligation</span></span> | <span data-ttu-id="a622f-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-493">1,000.00</span></span> |          |
| <span data-ttu-id="a622f-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-494">Ledger</span></span>       | <span data-ttu-id="a622f-495">4</span><span class="sxs-lookup"><span data-stu-id="a622f-495">4</span></span>              | <span data-ttu-id="a622f-496">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="a622f-496">Custom</span></span> | <span data-ttu-id="a622f-497">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="a622f-497">Clearing account</span></span>         |          | <span data-ttu-id="a622f-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a622f-498">1,000.00</span></span> |

<span data-ttu-id="a622f-499">Procentu izdevumu žurnāla ieraksts tiek ģenerēts no saistību amortizācijas grafika.</span><span class="sxs-lookup"><span data-stu-id="a622f-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="a622f-500">Procentu izdevumi — 31.01.2020. — JE 160</span><span class="sxs-lookup"><span data-stu-id="a622f-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="a622f-501">Konta veids</span><span class="sxs-lookup"><span data-stu-id="a622f-501">Account type</span></span> | <span data-ttu-id="a622f-502">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="a622f-502">Account number</span></span> | <span data-ttu-id="a622f-503">Līmenis</span><span class="sxs-lookup"><span data-stu-id="a622f-503">Layer</span></span>  | <span data-ttu-id="a622f-504">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-504">Account description</span></span>      | <span data-ttu-id="a622f-505">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-505">Debit</span></span> | <span data-ttu-id="a622f-506">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="a622f-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-507">Ledger</span></span>       | <span data-ttu-id="a622f-508">8</span><span class="sxs-lookup"><span data-stu-id="a622f-508">8</span></span>              | <span data-ttu-id="a622f-509">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="a622f-509">Custom</span></span> | <span data-ttu-id="a622f-510">Maksājamie procenti</span><span class="sxs-lookup"><span data-stu-id="a622f-510">Interest expense</span></span>         | <span data-ttu-id="a622f-511">94.97</span><span class="sxs-lookup"><span data-stu-id="a622f-511">94.97</span></span> |        |
| <span data-ttu-id="a622f-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-512">Ledger</span></span>       | <span data-ttu-id="a622f-513">7</span><span class="sxs-lookup"><span data-stu-id="a622f-513">7</span></span>              | <span data-ttu-id="a622f-514">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="a622f-514">Custom</span></span> | <span data-ttu-id="a622f-515">Finanšu nomas saistības</span><span class="sxs-lookup"><span data-stu-id="a622f-515">Finance lease obligation</span></span> |       | <span data-ttu-id="a622f-516">94.97</span><span class="sxs-lookup"><span data-stu-id="a622f-516">94.97</span></span>  |

<span data-ttu-id="a622f-517">Nolietojuma izdevumu žurnāla ieraksts tiek ģenerēts no līdzekļa nolietojuma grafika.</span><span class="sxs-lookup"><span data-stu-id="a622f-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="a622f-518">Nolietojuma izdevumi — 31.01.2020. — JE 170</span><span class="sxs-lookup"><span data-stu-id="a622f-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="a622f-519">Konta veids</span><span class="sxs-lookup"><span data-stu-id="a622f-519">Account type</span></span> | <span data-ttu-id="a622f-520">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="a622f-520">Account number</span></span> | <span data-ttu-id="a622f-521">Līmenis</span><span class="sxs-lookup"><span data-stu-id="a622f-521">Layer</span></span>  | <span data-ttu-id="a622f-522">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-522">Account description</span></span>      | <span data-ttu-id="a622f-523">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-523">Debit</span></span>  | <span data-ttu-id="a622f-524">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="a622f-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="a622f-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-525">Ledger</span></span>       | <span data-ttu-id="a622f-526">10.</span><span class="sxs-lookup"><span data-stu-id="a622f-526">10</span></span>             | <span data-ttu-id="a622f-527">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="a622f-527">Custom</span></span> | <span data-ttu-id="a622f-528">Nolietojuma izmaksas</span><span class="sxs-lookup"><span data-stu-id="a622f-528">Depreciation expense</span></span>     | <span data-ttu-id="a622f-529">949.75</span><span class="sxs-lookup"><span data-stu-id="a622f-529">949.75</span></span> |        |
| <span data-ttu-id="a622f-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="a622f-530">Ledger</span></span>       | <span data-ttu-id="a622f-531">11.</span><span class="sxs-lookup"><span data-stu-id="a622f-531">11</span></span>             | <span data-ttu-id="a622f-532">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="a622f-532">Custom</span></span> | <span data-ttu-id="a622f-533">Uzkrātais nolietojums</span><span class="sxs-lookup"><span data-stu-id="a622f-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="a622f-534">949.75</span><span class="sxs-lookup"><span data-stu-id="a622f-534">949.75</span></span> |

<span data-ttu-id="a622f-535">Pēc tam, kad visi šie žurnāla ieraksti ir izveidoti un grāmatoti, redzēsiet tālāk norādītās "1. pielāgotā slāņa" vērtības.</span><span class="sxs-lookup"><span data-stu-id="a622f-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="a622f-536">Ņemiet vērā, ka pēdējā kolonnā ir ietverta bankas komisija, pievienotās vērtības nodokļa (PVN) izdevumi un skaidras naudas samazinājums no iepriekšējā slāņa, bet tajā nav ietverti obligātie žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="a622f-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="a622f-537">Tādējādi tiek sasniegtas patiesas duālo pārskatu iespējas.</span><span class="sxs-lookup"><span data-stu-id="a622f-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="a622f-538">Šajā brīdī uzņēmumam vienkārši ir jāpalaiž apgrozījuma bilance un jākombinē pašreizējais slānis un pielāgotais slānis, lai izveidotu IFRS apgrozījuma bilanci.</span><span class="sxs-lookup"><span data-stu-id="a622f-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="a622f-539">Konta Nr.</span><span class="sxs-lookup"><span data-stu-id="a622f-539">Account No</span></span> | <span data-ttu-id="a622f-540">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a622f-540">Description</span></span>              | <span data-ttu-id="a622f-541">Obligātā grāmata\-Pašreizējais slānis\-JE\-100\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="a622f-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="a622f-542">Obligātā grāmata\-Pašreizējais slānis\-JE\-110\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="a622f-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="a622f-543">Obligātā grāmata\-Pašreizējais slānis\-JE\-120\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="a622f-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="a622f-544">Pašreizējais slānis \- Kopā</span><span class="sxs-lookup"><span data-stu-id="a622f-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="a622f-545">Anulēšanas grāmata\-pielāgotais slānis\-JE\-130\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="a622f-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="a622f-546">IFRS 16 grāmata\-pielāgotais slānis\-JE\-140\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="a622f-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="a622f-547">IFRS 16 grāmata\-pielāgotais slānis\-JE\-150\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="a622f-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="a622f-548">IFRS 16 grāmata\-pielāgotais slānis\-JE\-160\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="a622f-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="a622f-549">IFRS 16 grāmata\-pielāgotais slānis\-JE\-170\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="a622f-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="a622f-550">pielāgotais slānis \+ Pašreizējais slānis \- Kopā</span><span class="sxs-lookup"><span data-stu-id="a622f-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="a622f-551">1</span><span class="sxs-lookup"><span data-stu-id="a622f-551">1</span></span>          | <span data-ttu-id="a622f-552">Nomas izdevumi</span><span class="sxs-lookup"><span data-stu-id="a622f-552">Lease expense</span></span>            | <span data-ttu-id="a622f-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="a622f-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-554">1,000\.00</span></span>               |   | <span data-ttu-id="a622f-555">\-1000</span><span class="sxs-lookup"><span data-stu-id="a622f-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="a622f-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-556">0\.00</span></span>                                   |
| <span data-ttu-id="a622f-557">2</span><span class="sxs-lookup"><span data-stu-id="a622f-557">2</span></span>          | <span data-ttu-id="a622f-558">Bankas komisija</span><span class="sxs-lookup"><span data-stu-id="a622f-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="a622f-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="a622f-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="a622f-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-561">3\.00</span></span>                                   |
| <span data-ttu-id="a622f-562">3</span><span class="sxs-lookup"><span data-stu-id="a622f-562">3</span></span>          | <span data-ttu-id="a622f-563">PVN izdevumi</span><span class="sxs-lookup"><span data-stu-id="a622f-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="a622f-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="a622f-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="a622f-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-566">5\.00</span></span>                                   |
| <span data-ttu-id="a622f-567">4</span><span class="sxs-lookup"><span data-stu-id="a622f-567">4</span></span>          | <span data-ttu-id="a622f-568">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="a622f-568">Clearing account</span></span>         | <span data-ttu-id="a622f-569">\-1000\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="a622f-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="a622f-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-571">0\.00</span></span>                   |   | <span data-ttu-id="a622f-572">1000</span><span class="sxs-lookup"><span data-stu-id="a622f-572">1,000</span></span>                                           |                                                | <span data-ttu-id="a622f-573">\-1000</span><span class="sxs-lookup"><span data-stu-id="a622f-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="a622f-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-574">0\.00</span></span>                                   |
| <span data-ttu-id="a622f-575">5</span><span class="sxs-lookup"><span data-stu-id="a622f-575">5</span></span>          | <span data-ttu-id="a622f-576">Kreditoru parādi</span><span class="sxs-lookup"><span data-stu-id="a622f-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="a622f-577">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="a622f-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-578">1,008\.00</span></span>                                         | <span data-ttu-id="a622f-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="a622f-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-580">0\.00</span></span>                                   |
| <span data-ttu-id="a622f-581">6</span><span class="sxs-lookup"><span data-stu-id="a622f-581">6</span></span>          | <span data-ttu-id="a622f-582">LLT līdzeklis</span><span class="sxs-lookup"><span data-stu-id="a622f-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="a622f-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="a622f-584">22,794</span><span class="sxs-lookup"><span data-stu-id="a622f-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="a622f-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="a622f-585">22,793\.90</span></span>                              |
| <span data-ttu-id="a622f-586">7</span><span class="sxs-lookup"><span data-stu-id="a622f-586">7</span></span>          | <span data-ttu-id="a622f-587">Finanšu nomas saistības</span><span class="sxs-lookup"><span data-stu-id="a622f-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="a622f-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="a622f-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="a622f-589">\-22,794</span></span>                                       | <span data-ttu-id="a622f-590">1000</span><span class="sxs-lookup"><span data-stu-id="a622f-590">1,000</span></span>                                          | <span data-ttu-id="a622f-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="a622f-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="a622f-592">\-21 888\.87</span><span class="sxs-lookup"><span data-stu-id="a622f-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="a622f-593">8</span><span class="sxs-lookup"><span data-stu-id="a622f-593">8</span></span>          | <span data-ttu-id="a622f-594">Maksājamie procenti</span><span class="sxs-lookup"><span data-stu-id="a622f-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="a622f-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="a622f-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="a622f-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="a622f-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="a622f-597">94\.97</span></span>                                  |
| <span data-ttu-id="a622f-598">9</span><span class="sxs-lookup"><span data-stu-id="a622f-598">9</span></span>          | <span data-ttu-id="a622f-599">Kase</span><span class="sxs-lookup"><span data-stu-id="a622f-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="a622f-600">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="a622f-601">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="a622f-602">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="a622f-603">10.</span><span class="sxs-lookup"><span data-stu-id="a622f-603">10</span></span>         | <span data-ttu-id="a622f-604">Nolietojuma izmaksas</span><span class="sxs-lookup"><span data-stu-id="a622f-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="a622f-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="a622f-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="a622f-606">949\.75</span></span>                                        | <span data-ttu-id="a622f-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="a622f-607">949\.75</span></span>                                 |
| <span data-ttu-id="a622f-608">11.</span><span class="sxs-lookup"><span data-stu-id="a622f-608">11</span></span>         | <span data-ttu-id="a622f-609">Uzkrātais nolietojums</span><span class="sxs-lookup"><span data-stu-id="a622f-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="a622f-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="a622f-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="a622f-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="a622f-611">\-949\.75</span></span>                                      | <span data-ttu-id="a622f-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="a622f-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
