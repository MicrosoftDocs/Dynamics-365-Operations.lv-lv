---
title: Duālie pārskati
description: Šajā tēmā ir sniegts piemērs, kā varat izpildīt gan starptautiskā finanšu pārskatu standarta (International Financial Reporting Standard — IFRS), gan likumā noteiktās prasības pārskatiem līdzekļu nomā.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96e1d4d460aef2f74422d5e4bd4fc68255466455
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445776"
---
# <a name="dual-reporting"></a><span data-ttu-id="743c0-103">Duālie pārskati</span><span class="sxs-lookup"><span data-stu-id="743c0-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="743c0-104">Šajā tēmā ir sniegts piemērs, kā varat izpildīt gan starptautiskā finanšu pārskatu standarta (International Financial Reporting Standard — IFRS), gan likumā noteiktās prasības pārskatiem līdzekļu nomā.</span><span class="sxs-lookup"><span data-stu-id="743c0-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="743c0-105">Ir nepieciešams labi pazīt grāmatošanas līmeņus Microsoft Dynamics 365 Finance, tas padarīs šo piemēru vieglāk saprotamu.</span><span class="sxs-lookup"><span data-stu-id="743c0-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="743c0-106">Paraugs</span><span class="sxs-lookup"><span data-stu-id="743c0-106">Example</span></span>

<span data-ttu-id="743c0-107">Tālāk minētais piemērs uzskaita nomu saskaņā ar Itālijā obligāto pārskatu sniegšanu, izmantojot gan skaudras naudas bāzes metodi, gan IFRS pārskata metodes.</span><span class="sxs-lookup"><span data-stu-id="743c0-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="743c0-108">Uzņēmumam ir jāizveido trīs grāmatas, lai uzskaitītu gan Itālijā obligātās prasības, gan IFRS 16 prasības.</span><span class="sxs-lookup"><span data-stu-id="743c0-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="743c0-109">Viena grāmata ir nepieciešama IFRS 16, viena ir nepieciešama obligātajām prasībām, un viena grāmata ir nepieciešama, lai automātiski anulētu obligātos grāmatojumus.</span><span class="sxs-lookup"><span data-stu-id="743c0-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="743c0-110">Grāmatas ir iestatītas, kā parādīts tālāk redzamajās tabulās.</span><span class="sxs-lookup"><span data-stu-id="743c0-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="743c0-111">**IFRS 16 grāmata**</span><span class="sxs-lookup"><span data-stu-id="743c0-111">**IFRS 16 book**</span></span>

<span data-ttu-id="743c0-112">IFRS 16 grāmata ir iestatīta tā, lai tā atbilstu IFRS 16 uzskaites standartam.</span><span class="sxs-lookup"><span data-stu-id="743c0-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="743c0-113">Visi ieraksti, kas tiek grāmatoti šajā grāmatā, tiks grāmatoti pielāgotajā slānī.</span><span class="sxs-lookup"><span data-stu-id="743c0-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="743c0-114">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="743c0-114">Name</span></span>                                    | <span data-ttu-id="743c0-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="743c0-116">Grāmatas tips</span><span class="sxs-lookup"><span data-stu-id="743c0-116">Book type</span></span>                               | <span data-ttu-id="743c0-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="743c0-117">IFRS 16</span></span>        |
| <span data-ttu-id="743c0-118">Grāmatas apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-118">Book description</span></span>                        | <span data-ttu-id="743c0-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="743c0-119">IFRS 16</span></span>        |
| <span data-ttu-id="743c0-120">Grāmatošanas līmenis</span><span class="sxs-lookup"><span data-stu-id="743c0-120">Posting Layer</span></span>                           | <span data-ttu-id="743c0-121">1. pielāgotais līmenis</span><span class="sxs-lookup"><span data-stu-id="743c0-121">Custom layer 1</span></span> |
| <span data-ttu-id="743c0-122">Nomas veids</span><span class="sxs-lookup"><span data-stu-id="743c0-122">Lease Type</span></span>                              | <span data-ttu-id="743c0-123">Finance</span><span class="sxs-lookup"><span data-stu-id="743c0-123">Finance</span></span>        |
| <span data-ttu-id="743c0-124">Uzskaites struktūra</span><span class="sxs-lookup"><span data-stu-id="743c0-124">Accounting Framework</span></span>                    | <span data-ttu-id="743c0-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="743c0-125">IFRS 16</span></span>        |
| <span data-ttu-id="743c0-126">Nomas termiņa / lietderīgās lietošanas laika iestatīšana</span><span class="sxs-lookup"><span data-stu-id="743c0-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="743c0-127">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-127">0.00</span></span>           |
| <span data-ttu-id="743c0-128">Pašreizējās vērtības / līdzekļa patiesās vērtības iestatīšana</span><span class="sxs-lookup"><span data-stu-id="743c0-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="743c0-129">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-129">0.00</span></span>           |
| <span data-ttu-id="743c0-130">Īstermiņa slieksnis</span><span class="sxs-lookup"><span data-stu-id="743c0-130">Short-term threshold</span></span>                    | <span data-ttu-id="743c0-131">12.</span><span class="sxs-lookup"><span data-stu-id="743c0-131">12</span></span>             |
| <span data-ttu-id="743c0-132">Nelielas vērtības slieksnis</span><span class="sxs-lookup"><span data-stu-id="743c0-132">Low Value Threshold</span></span>                     | <span data-ttu-id="743c0-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-133">5,000.00</span></span>       |
| <span data-ttu-id="743c0-134">Maksāt kreditoram</span><span class="sxs-lookup"><span data-stu-id="743c0-134">Pay to Vendor</span></span>                           | <span data-ttu-id="743c0-135">Nr.</span><span class="sxs-lookup"><span data-stu-id="743c0-135">No</span></span>             |

<span data-ttu-id="743c0-136">**Obligātā grāmata**</span><span class="sxs-lookup"><span data-stu-id="743c0-136">**Statutory book**</span></span>

<span data-ttu-id="743c0-137">Obligātā grāmata ir skaidras naudas bāzes grāmata, kurā uzņēmums uzskaitīs nomas izdevumus kā skaidras naudas summu, kas katru mēnesi tiek maksāta par īri.</span><span class="sxs-lookup"><span data-stu-id="743c0-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="743c0-138">Šī grāmata nerada līdzekļa lietošanas tiesības (LLT) vai nomas saistības.</span><span class="sxs-lookup"><span data-stu-id="743c0-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="743c0-139">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="743c0-139">Name</span></span>                                    | <span data-ttu-id="743c0-140">Apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="743c0-141">Grāmatas tips</span><span class="sxs-lookup"><span data-stu-id="743c0-141">Book type</span></span>                               | <span data-ttu-id="743c0-142">Obligāta</span><span class="sxs-lookup"><span data-stu-id="743c0-142">Statutory</span></span>   |
| <span data-ttu-id="743c0-143">Grāmatas apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-143">Book description</span></span>                        | <span data-ttu-id="743c0-144">Vietējie vispārpieņemtie grāmatvedības principi</span><span class="sxs-lookup"><span data-stu-id="743c0-144">Local GAAP</span></span>  |
| <span data-ttu-id="743c0-145">Grāmatošanas līmenis</span><span class="sxs-lookup"><span data-stu-id="743c0-145">Posting Layer</span></span>                           | <span data-ttu-id="743c0-146">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="743c0-146">Current</span></span>     |
| <span data-ttu-id="743c0-147">Nomas veids</span><span class="sxs-lookup"><span data-stu-id="743c0-147">Lease Type</span></span>                              | <span data-ttu-id="743c0-148">Automātiski</span><span class="sxs-lookup"><span data-stu-id="743c0-148">Automatic</span></span>   |
| <span data-ttu-id="743c0-149">Uzskaites struktūra</span><span class="sxs-lookup"><span data-stu-id="743c0-149">Accounting Framework</span></span>                    | <span data-ttu-id="743c0-150">Skaidras naudas bāze</span><span class="sxs-lookup"><span data-stu-id="743c0-150">Cash basis</span></span>  |
| <span data-ttu-id="743c0-151">Nomas termiņa / lietderīgās lietošanas laika iestatīšana</span><span class="sxs-lookup"><span data-stu-id="743c0-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="743c0-152">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-152">0.00</span></span>        |
| <span data-ttu-id="743c0-153">Pašreizējās vērtības / līdzekļa patiesās vērtības iestatīšana</span><span class="sxs-lookup"><span data-stu-id="743c0-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="743c0-154">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-154">0.00</span></span>        |
| <span data-ttu-id="743c0-155">Īstermiņa slieksnis</span><span class="sxs-lookup"><span data-stu-id="743c0-155">Short-term threshold</span></span>                    | <span data-ttu-id="743c0-156">0</span><span class="sxs-lookup"><span data-stu-id="743c0-156">0</span></span>           |
| <span data-ttu-id="743c0-157">Nelielas vērtības slieksnis</span><span class="sxs-lookup"><span data-stu-id="743c0-157">Low Value Threshold</span></span>                     | <span data-ttu-id="743c0-158">0</span><span class="sxs-lookup"><span data-stu-id="743c0-158">0</span></span>           |
| <span data-ttu-id="743c0-159">Maksāt kreditoram</span><span class="sxs-lookup"><span data-stu-id="743c0-159">Pay to Vendor</span></span>                           | <span data-ttu-id="743c0-160">Nr.</span><span class="sxs-lookup"><span data-stu-id="743c0-160">No</span></span>          |

<span data-ttu-id="743c0-161">**Obligātā anulēšanas grāmata**</span><span class="sxs-lookup"><span data-stu-id="743c0-161">**Statutory reversal book**</span></span>

<span data-ttu-id="743c0-162">Obligātā anulēšanas grāmata ir iestatīta tādā pašā veidā kā obligātā grāmata.</span><span class="sxs-lookup"><span data-stu-id="743c0-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="743c0-163">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="743c0-163">Name</span></span>                                    | <span data-ttu-id="743c0-164">Apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="743c0-165">Grāmatas tips</span><span class="sxs-lookup"><span data-stu-id="743c0-165">Book type</span></span>                               | <span data-ttu-id="743c0-166">Obligātā — anulēšanas</span><span class="sxs-lookup"><span data-stu-id="743c0-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="743c0-167">Grāmatas apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-167">Book description</span></span>                        | <span data-ttu-id="743c0-168">Rezervēt, lai anulētu obligāto grāmatu</span><span class="sxs-lookup"><span data-stu-id="743c0-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="743c0-169">Grāmatošanas līmenis</span><span class="sxs-lookup"><span data-stu-id="743c0-169">Posting Layer</span></span>                           | <span data-ttu-id="743c0-170">1. pielāgotais līmenis</span><span class="sxs-lookup"><span data-stu-id="743c0-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="743c0-171">Nomas veids</span><span class="sxs-lookup"><span data-stu-id="743c0-171">Lease Type</span></span>                              | <span data-ttu-id="743c0-172">Automātiski</span><span class="sxs-lookup"><span data-stu-id="743c0-172">Automatic</span></span>                      |
| <span data-ttu-id="743c0-173">Uzskaites struktūra</span><span class="sxs-lookup"><span data-stu-id="743c0-173">Accounting Framework</span></span>                    | <span data-ttu-id="743c0-174">Skaidras naudas bāze</span><span class="sxs-lookup"><span data-stu-id="743c0-174">Cash basis</span></span>                     |
| <span data-ttu-id="743c0-175">Nomas termiņa / lietderīgās lietošanas laika iestatīšana</span><span class="sxs-lookup"><span data-stu-id="743c0-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="743c0-176">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-176">0.00</span></span>                           |
| <span data-ttu-id="743c0-177">Pašreizējās vērtības / līdzekļa patiesās vērtības iestatīšana</span><span class="sxs-lookup"><span data-stu-id="743c0-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="743c0-178">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-178">0.00</span></span>                           |
| <span data-ttu-id="743c0-179">Īstermiņa slieksnis</span><span class="sxs-lookup"><span data-stu-id="743c0-179">Short-term threshold</span></span>                    | <span data-ttu-id="743c0-180">0</span><span class="sxs-lookup"><span data-stu-id="743c0-180">0</span></span>                              |
| <span data-ttu-id="743c0-181">Nelielas vērtības slieksnis</span><span class="sxs-lookup"><span data-stu-id="743c0-181">Low Value Threshold</span></span>                     | <span data-ttu-id="743c0-182">0</span><span class="sxs-lookup"><span data-stu-id="743c0-182">0</span></span>                              |
| <span data-ttu-id="743c0-183">Maksāt kreditoram</span><span class="sxs-lookup"><span data-stu-id="743c0-183">Pay to Vendor</span></span>                           | <span data-ttu-id="743c0-184">Nr.</span><span class="sxs-lookup"><span data-stu-id="743c0-184">No</span></span>                             |

<span data-ttu-id="743c0-185">Šim piemēram ir izveidota noma, kam ir tālāk norādītie iestatījumi cilnēs **Vispārīgi** un **Maksājuma grafika rindas**.</span><span class="sxs-lookup"><span data-stu-id="743c0-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="743c0-186">**Cilne Vispārīgi**</span><span class="sxs-lookup"><span data-stu-id="743c0-186">**General tab**</span></span>

| <span data-ttu-id="743c0-187">Lauks</span><span class="sxs-lookup"><span data-stu-id="743c0-187">Field</span></span>                      | <span data-ttu-id="743c0-188">Vērtība</span><span class="sxs-lookup"><span data-stu-id="743c0-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="743c0-189">Salīdzināmā aizņēmuma procentu likme</span><span class="sxs-lookup"><span data-stu-id="743c0-189">Incremental borrowing rate</span></span> | <span data-ttu-id="743c0-190">5%</span><span class="sxs-lookup"><span data-stu-id="743c0-190">5%</span></span>               |
| <span data-ttu-id="743c0-191">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="743c0-191">Commencement date</span></span>          | <span data-ttu-id="743c0-192">01.01.2020.</span><span class="sxs-lookup"><span data-stu-id="743c0-192">1/1/2020</span></span>         |
| <span data-ttu-id="743c0-193">Nomas grupa</span><span class="sxs-lookup"><span data-stu-id="743c0-193">Lease group</span></span>                | <span data-ttu-id="743c0-194">Ēkas</span><span class="sxs-lookup"><span data-stu-id="743c0-194">Buildings</span></span>        |
| <span data-ttu-id="743c0-195">Kreditors</span><span class="sxs-lookup"><span data-stu-id="743c0-195">Vendor</span></span>                     | <span data-ttu-id="743c0-196">1001</span><span class="sxs-lookup"><span data-stu-id="743c0-196">1001</span></span>             |
| <span data-ttu-id="743c0-197">Līdzekļa patiesā vērtība</span><span class="sxs-lookup"><span data-stu-id="743c0-197">Fair value of the asset</span></span>    | <span data-ttu-id="743c0-198">245,000</span><span class="sxs-lookup"><span data-stu-id="743c0-198">245,000</span></span>          |
| <span data-ttu-id="743c0-199">Līdzekļa lietderīgās lietošanas laiks</span><span class="sxs-lookup"><span data-stu-id="743c0-199">Asset useful life</span></span>          | <span data-ttu-id="743c0-200">120</span><span class="sxs-lookup"><span data-stu-id="743c0-200">120</span></span>              |
| <span data-ttu-id="743c0-201">Gada maksājuma veids</span><span class="sxs-lookup"><span data-stu-id="743c0-201">Annuity type</span></span>               | <span data-ttu-id="743c0-202">Parastais gada maksājums</span><span class="sxs-lookup"><span data-stu-id="743c0-202">Ordinary annuity</span></span> |
| <span data-ttu-id="743c0-203">Pievienošanas intervāls</span><span class="sxs-lookup"><span data-stu-id="743c0-203">Compounding interval</span></span>       | <span data-ttu-id="743c0-204">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="743c0-204">Monthly</span></span>          |

<span data-ttu-id="743c0-205">**Cilne Maksājumu grafika rindas**</span><span class="sxs-lookup"><span data-stu-id="743c0-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="743c0-206">Lauks</span><span class="sxs-lookup"><span data-stu-id="743c0-206">Field</span></span>             | <span data-ttu-id="743c0-207">Vērtība</span><span class="sxs-lookup"><span data-stu-id="743c0-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="743c0-208">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="743c0-208">Start date</span></span>        | <span data-ttu-id="743c0-209">01.01.2020.</span><span class="sxs-lookup"><span data-stu-id="743c0-209">1/1/2020</span></span>   |
| <span data-ttu-id="743c0-210">Perioda intervāls</span><span class="sxs-lookup"><span data-stu-id="743c0-210">Period interval</span></span>   | <span data-ttu-id="743c0-211">Mēneši</span><span class="sxs-lookup"><span data-stu-id="743c0-211">Months</span></span>     |
| <span data-ttu-id="743c0-212">Periodi</span><span class="sxs-lookup"><span data-stu-id="743c0-212">Periods</span></span>           | <span data-ttu-id="743c0-213">24</span><span class="sxs-lookup"><span data-stu-id="743c0-213">24</span></span>         |
| <span data-ttu-id="743c0-214">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="743c0-214">End date</span></span>          | <span data-ttu-id="743c0-215">31.12.2020.</span><span class="sxs-lookup"><span data-stu-id="743c0-215">12/31/2020</span></span> |
| <span data-ttu-id="743c0-216">Maksājumu biežums</span><span class="sxs-lookup"><span data-stu-id="743c0-216">Payment frequency</span></span> | <span data-ttu-id="743c0-217">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="743c0-217">Monthly</span></span>    |
| <span data-ttu-id="743c0-218">Maksājuma summa</span><span class="sxs-lookup"><span data-stu-id="743c0-218">Payment amount</span></span>    | <span data-ttu-id="743c0-219">1000</span><span class="sxs-lookup"><span data-stu-id="743c0-219">1,000</span></span>      |

<span data-ttu-id="743c0-220">Lai šo nomu uzskaitītu divās struktūrās, jāizmanto pašreizējais grāmatošanas līmenis un pielāgotais grāmatošanas līmenis.</span><span class="sxs-lookup"><span data-stu-id="743c0-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="743c0-221">Tālāk redzamajā tabulā ir parādīts katra žurnāla ieraksta piemērs, kas nepieciešams pilnīgi atspoguļotu finanšu datus saskaņā ar katru pārskata standartu.</span><span class="sxs-lookup"><span data-stu-id="743c0-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="743c0-222">Pēc tam tiek sniegts detalizēts katra žurnāla ieraksta apraksts par nomas pirmo mēnesi.</span><span class="sxs-lookup"><span data-stu-id="743c0-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="743c0-223">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="743c0-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="743c0-224">Apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="743c0-225">Obligātā grāmata (pašreizējais slānis)</span><span class="sxs-lookup"><span data-stu-id="743c0-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="743c0-226">Pašreizējais slānis kopā</span><span class="sxs-lookup"><span data-stu-id="743c0-226">Current layer total</span></span></th>
<th><span data-ttu-id="743c0-227">Anulēšanas grāmata (pielāgotais slānis)</span><span class="sxs-lookup"><span data-stu-id="743c0-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="743c0-228">IFRS 16 grāmata (pielāgotais slānis)</span><span class="sxs-lookup"><span data-stu-id="743c0-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="743c0-229">Pašreizējā slāņa + pielāgotā slāņa kopsumma</span><span class="sxs-lookup"><span data-stu-id="743c0-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="743c0-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="743c0-230">JE-100</span></span></th>
<th><span data-ttu-id="743c0-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="743c0-231">JE-110</span></span></th>
<th><span data-ttu-id="743c0-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="743c0-232">JE-120</span></span></th>
<th><span data-ttu-id="743c0-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="743c0-233">JE-130</span></span></th>
<th><span data-ttu-id="743c0-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="743c0-234">JE-140</span></span></th>
<th><span data-ttu-id="743c0-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="743c0-235">JE-150</span></span></th>
<th><span data-ttu-id="743c0-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="743c0-236">JE-160</span></span></th>
<th><span data-ttu-id="743c0-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="743c0-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="743c0-238">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="743c0-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="743c0-239">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="743c0-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="743c0-240">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="743c0-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="743c0-241">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="743c0-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="743c0-242">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="743c0-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="743c0-243">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="743c0-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="743c0-244">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="743c0-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="743c0-245">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="743c0-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="743c0-246">1</span><span class="sxs-lookup"><span data-stu-id="743c0-246">1</span></span></td>
<td><span data-ttu-id="743c0-247">Nomas izdevumi</span><span class="sxs-lookup"><span data-stu-id="743c0-247">Lease expense</span></span></td>
<td><span data-ttu-id="743c0-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-249">1,000.00</span></span></td>
<td><span data-ttu-id="743c0-250">-1000,00</span><span class="sxs-lookup"><span data-stu-id="743c0-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-251">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-252">2</span><span class="sxs-lookup"><span data-stu-id="743c0-252">2</span></span></td>
<td><span data-ttu-id="743c0-253">Bankas komisija</span><span class="sxs-lookup"><span data-stu-id="743c0-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-254">3.00</span><span class="sxs-lookup"><span data-stu-id="743c0-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-255">3.00</span><span class="sxs-lookup"><span data-stu-id="743c0-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-256">3.00</span><span class="sxs-lookup"><span data-stu-id="743c0-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-257">3</span><span class="sxs-lookup"><span data-stu-id="743c0-257">3</span></span></td>
<td><span data-ttu-id="743c0-258">PVN izdevumi</span><span class="sxs-lookup"><span data-stu-id="743c0-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-259">5.00</span><span class="sxs-lookup"><span data-stu-id="743c0-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-260">5.00</span><span class="sxs-lookup"><span data-stu-id="743c0-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-261">5.00</span><span class="sxs-lookup"><span data-stu-id="743c0-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-262">4</span><span class="sxs-lookup"><span data-stu-id="743c0-262">4</span></span></td>
<td><span data-ttu-id="743c0-263">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="743c0-263">Clearing account</span></span></td>
<td><span data-ttu-id="743c0-264">-1000,00</span><span class="sxs-lookup"><span data-stu-id="743c0-264">-1,000.00</span></span></td>
<td><span data-ttu-id="743c0-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-266">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-266">0.00</span></span></td>
<td><span data-ttu-id="743c0-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-268">-1000,00</span><span class="sxs-lookup"><span data-stu-id="743c0-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-269">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-270">5</span><span class="sxs-lookup"><span data-stu-id="743c0-270">5</span></span></td>
<td><span data-ttu-id="743c0-271">Kreditoru parādi</span><span class="sxs-lookup"><span data-stu-id="743c0-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-272">-1008,00</span><span class="sxs-lookup"><span data-stu-id="743c0-272">-1,008.00</span></span></td>
<td><span data-ttu-id="743c0-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="743c0-273">1,008.00</span></span></td>
<td><span data-ttu-id="743c0-274">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-275">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-276">6</span><span class="sxs-lookup"><span data-stu-id="743c0-276">6</span></span></td>
<td><span data-ttu-id="743c0-277">LLT līdzeklis</span><span class="sxs-lookup"><span data-stu-id="743c0-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-278">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="743c0-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="743c0-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-281">7</span><span class="sxs-lookup"><span data-stu-id="743c0-281">7</span></span></td>
<td><span data-ttu-id="743c0-282">Finanšu nomas saistības</span><span class="sxs-lookup"><span data-stu-id="743c0-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-283">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="743c0-284">-22,794.00</span></span></td>
<td><span data-ttu-id="743c0-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-285">1,000.00</span></span></td>
<td><span data-ttu-id="743c0-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="743c0-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="743c0-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-288">8</span><span class="sxs-lookup"><span data-stu-id="743c0-288">8</span></span></td>
<td><span data-ttu-id="743c0-289">Maksājamie procenti</span><span class="sxs-lookup"><span data-stu-id="743c0-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-290">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-291">94.97</span><span class="sxs-lookup"><span data-stu-id="743c0-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-292">94.97</span><span class="sxs-lookup"><span data-stu-id="743c0-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-293">9</span><span class="sxs-lookup"><span data-stu-id="743c0-293">9</span></span></td>
<td><span data-ttu-id="743c0-294">Kase</span><span class="sxs-lookup"><span data-stu-id="743c0-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-295">-1008,00</span><span class="sxs-lookup"><span data-stu-id="743c0-295">-1,008.00</span></span></td>
<td><span data-ttu-id="743c0-296">-1008,00</span><span class="sxs-lookup"><span data-stu-id="743c0-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-297">-1008,00</span><span class="sxs-lookup"><span data-stu-id="743c0-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-298">10.</span><span class="sxs-lookup"><span data-stu-id="743c0-298">10</span></span></td>
<td><span data-ttu-id="743c0-299">Nolietojuma izmaksas</span><span class="sxs-lookup"><span data-stu-id="743c0-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-300">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-301">949.75</span><span class="sxs-lookup"><span data-stu-id="743c0-301">949.75</span></span></td>
<td><span data-ttu-id="743c0-302">949.75</span><span class="sxs-lookup"><span data-stu-id="743c0-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-303">11.</span><span class="sxs-lookup"><span data-stu-id="743c0-303">11</span></span></td>
<td><span data-ttu-id="743c0-304">Uzkrātais nolietojums</span><span class="sxs-lookup"><span data-stu-id="743c0-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-305">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="743c0-306">-949.75</span></span></td>
<td><span data-ttu-id="743c0-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="743c0-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="743c0-308">Kā redzams iepriekšējā tabulā, ir nepieciešamas trīs grāmatas, lai sniegtu pārskatu saskaņā obligāto un IFRS pārskatu sniegšanu.</span><span class="sxs-lookup"><span data-stu-id="743c0-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="743c0-309">Obligātajā grāmatā ierakstīti nomas maksājumi saskaņā ar noteikumiem par skaidras naudas bāzes uzskaiti, pamatojoties uz pašreizējo slāni.</span><span class="sxs-lookup"><span data-stu-id="743c0-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="743c0-310">Obligātā anulēšanas grāmata anulē obligātos žurnāla ierakstus.</span><span class="sxs-lookup"><span data-stu-id="743c0-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="743c0-311">IFRS 16 grāmata izveido žurnāla ierakstus, kas ir nepieciešami saskaņā ar IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="743c0-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="743c0-312">Noma ir jāievada tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="743c0-312">You must enter a lease only one time.</span></span> <span data-ttu-id="743c0-313">Pēc tam varat atvērt lapu **Grāmatas**, lai skatītu visas ar nomu saistītās grāmatas.</span><span class="sxs-lookup"><span data-stu-id="743c0-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="743c0-314">Kad izveidojat grāmatas, visām trim no tām jābūt saistītām ar to pašu nomas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="743c0-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="743c0-315">Pirmajā žurnāla ierakstā reģistrēti nomas izdevumi saskaņā ar obligāto grāmatu.</span><span class="sxs-lookup"><span data-stu-id="743c0-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="743c0-316">Varat izveidot maksājumus vai nu partijā, vai atlasot maksājumu grafiku obligātajā grāmatā.</span><span class="sxs-lookup"><span data-stu-id="743c0-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="743c0-317">Šajā piemērā tālāk norādītais žurnāla ieraksts ir izveidots obligātajai grāmatai no maksājumu grafika.</span><span class="sxs-lookup"><span data-stu-id="743c0-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="743c0-318">Nomas maksājums — 01.31.2020. — JE 100</span><span class="sxs-lookup"><span data-stu-id="743c0-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="743c0-319">Konta veids</span><span class="sxs-lookup"><span data-stu-id="743c0-319">Account type</span></span> | <span data-ttu-id="743c0-320">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="743c0-320">Account number</span></span> | <span data-ttu-id="743c0-321">Līmenis</span><span class="sxs-lookup"><span data-stu-id="743c0-321">Layer</span></span>   | <span data-ttu-id="743c0-322">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-322">Account description</span></span> | <span data-ttu-id="743c0-323">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-323">Debit</span></span>    | <span data-ttu-id="743c0-324">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="743c0-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-325">Ledger</span></span>       | <span data-ttu-id="743c0-326">1</span><span class="sxs-lookup"><span data-stu-id="743c0-326">1</span></span>              | <span data-ttu-id="743c0-327">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="743c0-327">Current</span></span> | <span data-ttu-id="743c0-328">Nomas izdevumi</span><span class="sxs-lookup"><span data-stu-id="743c0-328">Lease expense</span></span>       | <span data-ttu-id="743c0-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-329">1,000.00</span></span> |          |
| <span data-ttu-id="743c0-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-330">Ledger</span></span>       | <span data-ttu-id="743c0-331">4</span><span class="sxs-lookup"><span data-stu-id="743c0-331">4</span></span>              | <span data-ttu-id="743c0-332">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="743c0-332">Current</span></span> | <span data-ttu-id="743c0-333">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="743c0-333">Clearing account</span></span>    |          | <span data-ttu-id="743c0-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-334">1,000.00</span></span> |

<span data-ttu-id="743c0-335">Par Kreditoru rēķiniem atbildīgais darbinieks izmanto standarta Dynamics 365 funkcionalitāti, lai izveidotu rēķinu, kas jāmaksā par nomu ārpus Līdzekļu nomas.</span><span class="sxs-lookup"><span data-stu-id="743c0-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="743c0-336">Tomēr tā vietā, lai atlasītu **Nomas izdevumi** kā debeta kontu, par Kreditoru rēķiniem atbildīgais darbinieks atlasa dzēšanas kontu, lai ģenerētu tālāk norādīto ierakstu.</span><span class="sxs-lookup"><span data-stu-id="743c0-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="743c0-337">KR process — 31.012020. — JE 110</span><span class="sxs-lookup"><span data-stu-id="743c0-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="743c0-338">Konta veids</span><span class="sxs-lookup"><span data-stu-id="743c0-338">Account type</span></span> | <span data-ttu-id="743c0-339">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="743c0-339">Account number</span></span> | <span data-ttu-id="743c0-340">Līmenis</span><span class="sxs-lookup"><span data-stu-id="743c0-340">Layer</span></span>   | <span data-ttu-id="743c0-341">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-341">Account description</span></span> | <span data-ttu-id="743c0-342">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-342">Debit</span></span>    | <span data-ttu-id="743c0-343">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="743c0-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-344">Ledger</span></span>       | <span data-ttu-id="743c0-345">4</span><span class="sxs-lookup"><span data-stu-id="743c0-345">4</span></span>              | <span data-ttu-id="743c0-346">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="743c0-346">Current</span></span> | <span data-ttu-id="743c0-347">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="743c0-347">Clearing account</span></span>    | <span data-ttu-id="743c0-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-348">1,000.00</span></span> |          |
| <span data-ttu-id="743c0-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-349">Ledger</span></span>       | <span data-ttu-id="743c0-350">2</span><span class="sxs-lookup"><span data-stu-id="743c0-350">2</span></span>              | <span data-ttu-id="743c0-351">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="743c0-351">Current</span></span> | <span data-ttu-id="743c0-352">Bankas komisija</span><span class="sxs-lookup"><span data-stu-id="743c0-352">Bank fee</span></span>            | <span data-ttu-id="743c0-353">3.00</span><span class="sxs-lookup"><span data-stu-id="743c0-353">3.00</span></span>     |          |
| <span data-ttu-id="743c0-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-354">Ledger</span></span>       | <span data-ttu-id="743c0-355">3</span><span class="sxs-lookup"><span data-stu-id="743c0-355">3</span></span>              | <span data-ttu-id="743c0-356">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="743c0-356">Current</span></span> | <span data-ttu-id="743c0-357">PVN izdevumi</span><span class="sxs-lookup"><span data-stu-id="743c0-357">VAT expense</span></span>         | <span data-ttu-id="743c0-358">5.00</span><span class="sxs-lookup"><span data-stu-id="743c0-358">5.00</span></span>     |          |
| <span data-ttu-id="743c0-359">Kreditors</span><span class="sxs-lookup"><span data-stu-id="743c0-359">Vendor</span></span>       | <span data-ttu-id="743c0-360">5</span><span class="sxs-lookup"><span data-stu-id="743c0-360">5</span></span>              | <span data-ttu-id="743c0-361">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="743c0-361">Current</span></span> | <span data-ttu-id="743c0-362">Kreditoru parādi</span><span class="sxs-lookup"><span data-stu-id="743c0-362">Accounts payable</span></span>    |          | <span data-ttu-id="743c0-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="743c0-363">1,008.00</span></span> |

<span data-ttu-id="743c0-364">Kad izraksts tiek izsniegts kreditoram, veiciet parastu maksāšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="743c0-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="743c0-365">Šī procesa laikā tiek ģenerēts tālāk norādītais žurnāla ieraksts.</span><span class="sxs-lookup"><span data-stu-id="743c0-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="743c0-366">Skaidras naudas maksājums – 31.01.2020. – JE 120</span><span class="sxs-lookup"><span data-stu-id="743c0-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="743c0-367">Konta veids</span><span class="sxs-lookup"><span data-stu-id="743c0-367">Account type</span></span> | <span data-ttu-id="743c0-368">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="743c0-368">Account number</span></span> | <span data-ttu-id="743c0-369">Līmenis</span><span class="sxs-lookup"><span data-stu-id="743c0-369">Layer</span></span>   | <span data-ttu-id="743c0-370">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-370">Account description</span></span> | <span data-ttu-id="743c0-371">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-371">Debit</span></span>    | <span data-ttu-id="743c0-372">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="743c0-373">Kreditors</span><span class="sxs-lookup"><span data-stu-id="743c0-373">Vendor</span></span>       | <span data-ttu-id="743c0-374">5</span><span class="sxs-lookup"><span data-stu-id="743c0-374">5</span></span>              | <span data-ttu-id="743c0-375">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="743c0-375">Current</span></span> | <span data-ttu-id="743c0-376">Parādi kreditoriem</span><span class="sxs-lookup"><span data-stu-id="743c0-376">Accounts Payable</span></span>    | <span data-ttu-id="743c0-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="743c0-377">1,008.00</span></span> |          |
| <span data-ttu-id="743c0-378">Banka</span><span class="sxs-lookup"><span data-stu-id="743c0-378">Bank</span></span>         | <span data-ttu-id="743c0-379">9</span><span class="sxs-lookup"><span data-stu-id="743c0-379">9</span></span>              | <span data-ttu-id="743c0-380">Pašreizējos</span><span class="sxs-lookup"><span data-stu-id="743c0-380">Current</span></span> | <span data-ttu-id="743c0-381">Kase</span><span class="sxs-lookup"><span data-stu-id="743c0-381">Cash</span></span>                |          | <span data-ttu-id="743c0-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="743c0-382">1,008.00</span></span> |

<span data-ttu-id="743c0-383">Šajā brīdī esat pilnībā uzskaitījis šo nomu saskaņā ar obligātajām prasībām un varat ģenerēt apgrozījuma bilanci, izmantojot pašreizējo slāni.</span><span class="sxs-lookup"><span data-stu-id="743c0-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="743c0-384">Sistēma izveido apgrozījuma bilanci ar tālāk norādītajiem skaitļiem.</span><span class="sxs-lookup"><span data-stu-id="743c0-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="743c0-385">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="743c0-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="743c0-386">Apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="743c0-387">Obligātā grāmata (pašreizējais slānis)</span><span class="sxs-lookup"><span data-stu-id="743c0-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="743c0-388">Pašreizējais slānis kopā</span><span class="sxs-lookup"><span data-stu-id="743c0-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="743c0-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="743c0-389">JE-100</span></span></th>
<th><span data-ttu-id="743c0-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="743c0-390">JE-110</span></span></th>
<th><span data-ttu-id="743c0-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="743c0-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="743c0-392">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="743c0-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="743c0-393">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="743c0-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="743c0-394">Deb. (kred.)</span><span class="sxs-lookup"><span data-stu-id="743c0-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="743c0-395">1</span><span class="sxs-lookup"><span data-stu-id="743c0-395">1</span></span></td>
<td><span data-ttu-id="743c0-396">Nomas izdevumi</span><span class="sxs-lookup"><span data-stu-id="743c0-396">Lease expense</span></span></td>
<td><span data-ttu-id="743c0-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-399">2</span><span class="sxs-lookup"><span data-stu-id="743c0-399">2</span></span></td>
<td><span data-ttu-id="743c0-400">Bankas komisija</span><span class="sxs-lookup"><span data-stu-id="743c0-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-401">3.00</span><span class="sxs-lookup"><span data-stu-id="743c0-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-402">3.00</span><span class="sxs-lookup"><span data-stu-id="743c0-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-403">3</span><span class="sxs-lookup"><span data-stu-id="743c0-403">3</span></span></td>
<td><span data-ttu-id="743c0-404">PVN izdevumi</span><span class="sxs-lookup"><span data-stu-id="743c0-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-405">5.00</span><span class="sxs-lookup"><span data-stu-id="743c0-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-406">5.00</span><span class="sxs-lookup"><span data-stu-id="743c0-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-407">4</span><span class="sxs-lookup"><span data-stu-id="743c0-407">4</span></span></td>
<td><span data-ttu-id="743c0-408">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="743c0-408">Clearing account</span></span></td>
<td><span data-ttu-id="743c0-409">-1000,00</span><span class="sxs-lookup"><span data-stu-id="743c0-409">-1,000.00</span></span></td>
<td><span data-ttu-id="743c0-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-411">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-412">5</span><span class="sxs-lookup"><span data-stu-id="743c0-412">5</span></span></td>
<td><span data-ttu-id="743c0-413">Kreditoru parādi</span><span class="sxs-lookup"><span data-stu-id="743c0-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="743c0-414">-1008,00</span><span class="sxs-lookup"><span data-stu-id="743c0-414">-1,008.00</span></span></td>
<td><span data-ttu-id="743c0-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="743c0-415">1,008.00</span></span></td>
<td><span data-ttu-id="743c0-416">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-417">6</span><span class="sxs-lookup"><span data-stu-id="743c0-417">6</span></span></td>
<td><span data-ttu-id="743c0-418">LLT līdzeklis</span><span class="sxs-lookup"><span data-stu-id="743c0-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-419">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-420">7</span><span class="sxs-lookup"><span data-stu-id="743c0-420">7</span></span></td>
<td><span data-ttu-id="743c0-421">Finanšu nomas saistības</span><span class="sxs-lookup"><span data-stu-id="743c0-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-422">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-423">8</span><span class="sxs-lookup"><span data-stu-id="743c0-423">8</span></span></td>
<td><span data-ttu-id="743c0-424">Maksājamie procenti</span><span class="sxs-lookup"><span data-stu-id="743c0-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-425">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-426">9</span><span class="sxs-lookup"><span data-stu-id="743c0-426">9</span></span></td>
<td><span data-ttu-id="743c0-427">Kase</span><span class="sxs-lookup"><span data-stu-id="743c0-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-428">-1008,00</span><span class="sxs-lookup"><span data-stu-id="743c0-428">-1,008.00</span></span></td>
<td><span data-ttu-id="743c0-429">-1008,00</span><span class="sxs-lookup"><span data-stu-id="743c0-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-430">10.</span><span class="sxs-lookup"><span data-stu-id="743c0-430">10</span></span></td>
<td><span data-ttu-id="743c0-431">Nolietojuma izmaksas</span><span class="sxs-lookup"><span data-stu-id="743c0-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-432">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="743c0-433">11.</span><span class="sxs-lookup"><span data-stu-id="743c0-433">11</span></span></td>
<td><span data-ttu-id="743c0-434">Uzkrātais nolietojums</span><span class="sxs-lookup"><span data-stu-id="743c0-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="743c0-435">0.00</span><span class="sxs-lookup"><span data-stu-id="743c0-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="743c0-436">Ja vēlaties izmantot IFRS 16 skaitļus, lai palaistu to pašu apgrozījuma bilanci, ir jāanulē obligātie uzskaites žurnāla ieraksti un jāgrāmato IFRS 16 žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="743c0-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="743c0-437">Lai anulētu obligātos žurnāla ierakstus, šajā piemērā ir iekļauta obligātā anulēšanas grāmata ar tādiem pašiem iestatījumiem kā obligātajai grāmatai, bet ar pretēju grāmatošanas profilu.</span><span class="sxs-lookup"><span data-stu-id="743c0-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="743c0-438">Piemēram, obligātā grāmata *debetēja* nomas izdevumu kontu, bet anulēšanas grāmata *kreditēs* šo kontu.</span><span class="sxs-lookup"><span data-stu-id="743c0-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="743c0-439">Šīs attiecības ir viegli definētas Līdzekļu nomas grāmatošanas kontos lapā **Līdzekļu nomas parametri** lapā (**Līdzekļu noma \> Iestatījumi \> Līdzekļu nomas parametri**).</span><span class="sxs-lookup"><span data-stu-id="743c0-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="743c0-440">Kad tas pats process, kas tika izmantots obligātajai grāmatai, tiek izmantots anulēšanas grāmatai, tiek izveidots tālāk norādītais žurnāla ieraksts.</span><span class="sxs-lookup"><span data-stu-id="743c0-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="743c0-441">Atšķirība ir tāda, ka anulēšanas grāmata anulē obligātās grāmatas ierakstus.</span><span class="sxs-lookup"><span data-stu-id="743c0-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="743c0-442">Anulēšanas ieraksti arī tiek veikti pielāgotā slānī.</span><span class="sxs-lookup"><span data-stu-id="743c0-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="743c0-443">Ja apgrozījuma bilance tiek palaista pašreizējā slānī, anulējošie žurnāla ieraksti nav ietverti.</span><span class="sxs-lookup"><span data-stu-id="743c0-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="743c0-444">Nomas maksājums — 01.31.2020. — JE 130</span><span class="sxs-lookup"><span data-stu-id="743c0-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="743c0-445">Konta veids</span><span class="sxs-lookup"><span data-stu-id="743c0-445">Account type</span></span> | <span data-ttu-id="743c0-446">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="743c0-446">Account number</span></span> | <span data-ttu-id="743c0-447">Līmenis</span><span class="sxs-lookup"><span data-stu-id="743c0-447">Layer</span></span>  | <span data-ttu-id="743c0-448">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-448">Account description</span></span> | <span data-ttu-id="743c0-449">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-449">Debit</span></span>    | <span data-ttu-id="743c0-450">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="743c0-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-451">Ledger</span></span>       | <span data-ttu-id="743c0-452">4</span><span class="sxs-lookup"><span data-stu-id="743c0-452">4</span></span>              | <span data-ttu-id="743c0-453">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="743c0-453">Custom</span></span> | <span data-ttu-id="743c0-454">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="743c0-454">Clearing account</span></span>    | <span data-ttu-id="743c0-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-455">1,000.00</span></span> |          |
| <span data-ttu-id="743c0-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-456">Ledger</span></span>       | <span data-ttu-id="743c0-457">1</span><span class="sxs-lookup"><span data-stu-id="743c0-457">1</span></span>              | <span data-ttu-id="743c0-458">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="743c0-458">Custom</span></span> | <span data-ttu-id="743c0-459">Nomas izdevumi</span><span class="sxs-lookup"><span data-stu-id="743c0-459">Lease expense</span></span>       |          | <span data-ttu-id="743c0-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-460">1,000.00</span></span> |

<span data-ttu-id="743c0-461">Tagad, kad ir likvidēti obligātā žurnāla ieraksti, tiks grāmatoti visi žurnāla ieraksti, kas ir nepieciešami IFRS 16 grāmatai.</span><span class="sxs-lookup"><span data-stu-id="743c0-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="743c0-462">Šie ieraksti ietver sākotnējo LLT un saistību atzīšanu, kā arī procentu un nolietojuma ierakstu.</span><span class="sxs-lookup"><span data-stu-id="743c0-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="743c0-463">Sākotnējā atzīšana — 01.01.2020. — JE 140</span><span class="sxs-lookup"><span data-stu-id="743c0-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="743c0-464">Konta veids</span><span class="sxs-lookup"><span data-stu-id="743c0-464">Account type</span></span> | <span data-ttu-id="743c0-465">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="743c0-465">Account number</span></span> | <span data-ttu-id="743c0-466">Līmenis</span><span class="sxs-lookup"><span data-stu-id="743c0-466">Layer</span></span>  | <span data-ttu-id="743c0-467">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-467">Account description</span></span>      | <span data-ttu-id="743c0-468">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-468">Debit</span></span>     | <span data-ttu-id="743c0-469">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="743c0-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-470">Ledger</span></span>       | <span data-ttu-id="743c0-471">6</span><span class="sxs-lookup"><span data-stu-id="743c0-471">6</span></span>              | <span data-ttu-id="743c0-472">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="743c0-472">Custom</span></span> | <span data-ttu-id="743c0-473">LLT līdzeklis</span><span class="sxs-lookup"><span data-stu-id="743c0-473">ROU Asset</span></span>                | <span data-ttu-id="743c0-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="743c0-474">22,793.90</span></span> |           |
| <span data-ttu-id="743c0-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-475">Ledger</span></span>       | <span data-ttu-id="743c0-476">7</span><span class="sxs-lookup"><span data-stu-id="743c0-476">7</span></span>              | <span data-ttu-id="743c0-477">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="743c0-477">Custom</span></span> | <span data-ttu-id="743c0-478">Finanšu nomas saistības</span><span class="sxs-lookup"><span data-stu-id="743c0-478">Finance lease obligation</span></span> |           | <span data-ttu-id="743c0-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="743c0-479">22,793.90</span></span> |

<span data-ttu-id="743c0-480">Nomas maksājums tiek grāmatots līdzīgi citi nomas maksājumi.</span><span class="sxs-lookup"><span data-stu-id="743c0-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="743c0-481">Dzēšanas konta izmantošanas iemesls ir nodrošināt, ka skaidra nauda tiek kreditēta tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="743c0-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="743c0-482">Nomas maksājums — 01.31.2020. — JE 150</span><span class="sxs-lookup"><span data-stu-id="743c0-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="743c0-483">Konta veids</span><span class="sxs-lookup"><span data-stu-id="743c0-483">Account type</span></span> | <span data-ttu-id="743c0-484">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="743c0-484">Account number</span></span> | <span data-ttu-id="743c0-485">Līmenis</span><span class="sxs-lookup"><span data-stu-id="743c0-485">Layer</span></span>  | <span data-ttu-id="743c0-486">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-486">Account description</span></span>      | <span data-ttu-id="743c0-487">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-487">Debit</span></span>    | <span data-ttu-id="743c0-488">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="743c0-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-489">Ledger</span></span>       | <span data-ttu-id="743c0-490">7</span><span class="sxs-lookup"><span data-stu-id="743c0-490">7</span></span>              | <span data-ttu-id="743c0-491">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="743c0-491">Custom</span></span> | <span data-ttu-id="743c0-492">Finanšu nomas saistības</span><span class="sxs-lookup"><span data-stu-id="743c0-492">Finance lease obligation</span></span> | <span data-ttu-id="743c0-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-493">1,000.00</span></span> |          |
| <span data-ttu-id="743c0-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-494">Ledger</span></span>       | <span data-ttu-id="743c0-495">4</span><span class="sxs-lookup"><span data-stu-id="743c0-495">4</span></span>              | <span data-ttu-id="743c0-496">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="743c0-496">Custom</span></span> | <span data-ttu-id="743c0-497">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="743c0-497">Clearing account</span></span>         |          | <span data-ttu-id="743c0-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="743c0-498">1,000.00</span></span> |

<span data-ttu-id="743c0-499">Procentu izdevumu žurnāla ieraksts tiek ģenerēts no saistību amortizācijas grafika.</span><span class="sxs-lookup"><span data-stu-id="743c0-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="743c0-500">Procentu izdevumi — 31.01.2020. — JE 160</span><span class="sxs-lookup"><span data-stu-id="743c0-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="743c0-501">Konta veids</span><span class="sxs-lookup"><span data-stu-id="743c0-501">Account type</span></span> | <span data-ttu-id="743c0-502">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="743c0-502">Account number</span></span> | <span data-ttu-id="743c0-503">Līmenis</span><span class="sxs-lookup"><span data-stu-id="743c0-503">Layer</span></span>  | <span data-ttu-id="743c0-504">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-504">Account description</span></span>      | <span data-ttu-id="743c0-505">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-505">Debit</span></span> | <span data-ttu-id="743c0-506">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="743c0-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-507">Ledger</span></span>       | <span data-ttu-id="743c0-508">8</span><span class="sxs-lookup"><span data-stu-id="743c0-508">8</span></span>              | <span data-ttu-id="743c0-509">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="743c0-509">Custom</span></span> | <span data-ttu-id="743c0-510">Maksājamie procenti</span><span class="sxs-lookup"><span data-stu-id="743c0-510">Interest expense</span></span>         | <span data-ttu-id="743c0-511">94.97</span><span class="sxs-lookup"><span data-stu-id="743c0-511">94.97</span></span> |        |
| <span data-ttu-id="743c0-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-512">Ledger</span></span>       | <span data-ttu-id="743c0-513">7</span><span class="sxs-lookup"><span data-stu-id="743c0-513">7</span></span>              | <span data-ttu-id="743c0-514">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="743c0-514">Custom</span></span> | <span data-ttu-id="743c0-515">Finanšu nomas saistības</span><span class="sxs-lookup"><span data-stu-id="743c0-515">Finance lease obligation</span></span> |       | <span data-ttu-id="743c0-516">94.97</span><span class="sxs-lookup"><span data-stu-id="743c0-516">94.97</span></span>  |

<span data-ttu-id="743c0-517">Nolietojuma izdevumu žurnāla ieraksts tiek ģenerēts no līdzekļa nolietojuma grafika.</span><span class="sxs-lookup"><span data-stu-id="743c0-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="743c0-518">Nolietojuma izdevumi — 31.01.2020. — JE 170</span><span class="sxs-lookup"><span data-stu-id="743c0-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="743c0-519">Konta veids</span><span class="sxs-lookup"><span data-stu-id="743c0-519">Account type</span></span> | <span data-ttu-id="743c0-520">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="743c0-520">Account number</span></span> | <span data-ttu-id="743c0-521">Līmenis</span><span class="sxs-lookup"><span data-stu-id="743c0-521">Layer</span></span>  | <span data-ttu-id="743c0-522">Konta apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-522">Account description</span></span>      | <span data-ttu-id="743c0-523">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-523">Debit</span></span>  | <span data-ttu-id="743c0-524">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="743c0-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="743c0-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-525">Ledger</span></span>       | <span data-ttu-id="743c0-526">10.</span><span class="sxs-lookup"><span data-stu-id="743c0-526">10</span></span>             | <span data-ttu-id="743c0-527">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="743c0-527">Custom</span></span> | <span data-ttu-id="743c0-528">Nolietojuma izmaksas</span><span class="sxs-lookup"><span data-stu-id="743c0-528">Depreciation expense</span></span>     | <span data-ttu-id="743c0-529">949.75</span><span class="sxs-lookup"><span data-stu-id="743c0-529">949.75</span></span> |        |
| <span data-ttu-id="743c0-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="743c0-530">Ledger</span></span>       | <span data-ttu-id="743c0-531">11.</span><span class="sxs-lookup"><span data-stu-id="743c0-531">11</span></span>             | <span data-ttu-id="743c0-532">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="743c0-532">Custom</span></span> | <span data-ttu-id="743c0-533">Uzkrātais nolietojums</span><span class="sxs-lookup"><span data-stu-id="743c0-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="743c0-534">949.75</span><span class="sxs-lookup"><span data-stu-id="743c0-534">949.75</span></span> |

<span data-ttu-id="743c0-535">Pēc tam, kad visi šie žurnāla ieraksti ir izveidoti un grāmatoti, redzēsiet tālāk norādītās "1. pielāgotā slāņa" vērtības.</span><span class="sxs-lookup"><span data-stu-id="743c0-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="743c0-536">Ņemiet vērā, ka pēdējā kolonnā ir ietverta bankas komisija, pievienotās vērtības nodokļa (PVN) izdevumi un skaidras naudas samazinājums no iepriekšējā slāņa, bet tajā nav ietverti obligātie žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="743c0-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="743c0-537">Tādējādi tiek sasniegtas patiesas duālo pārskatu iespējas.</span><span class="sxs-lookup"><span data-stu-id="743c0-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="743c0-538">Šajā brīdī uzņēmumam vienkārši ir jāpalaiž apgrozījuma bilance un jākombinē pašreizējais slānis un pielāgotais slānis, lai izveidotu IFRS apgrozījuma bilanci.</span><span class="sxs-lookup"><span data-stu-id="743c0-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="743c0-539">Konta Nr.</span><span class="sxs-lookup"><span data-stu-id="743c0-539">Account No</span></span> | <span data-ttu-id="743c0-540">Apraksts</span><span class="sxs-lookup"><span data-stu-id="743c0-540">Description</span></span>              | <span data-ttu-id="743c0-541">Obligātā grāmata\-Pašreizējais slānis\-JE\-100\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="743c0-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="743c0-542">Obligātā grāmata\-Pašreizējais slānis\-JE\-110\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="743c0-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="743c0-543">Obligātā grāmata\-Pašreizējais slānis\-JE\-120\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="743c0-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="743c0-544">Pašreizējais slānis \- Kopā</span><span class="sxs-lookup"><span data-stu-id="743c0-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="743c0-545">Anulēšanas grāmata\-pielāgotais slānis\-JE\-130\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="743c0-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="743c0-546">IFRS 16 grāmata\-pielāgotais slānis\-JE\-140\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="743c0-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="743c0-547">IFRS 16 grāmata\-pielāgotais slānis\-JE\-150\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="743c0-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="743c0-548">IFRS 16 grāmata\-pielāgotais slānis\-JE\-160\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="743c0-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="743c0-549">IFRS 16 grāmata\-pielāgotais slānis\-JE\-170\-Deb. \(kred.\)</span><span class="sxs-lookup"><span data-stu-id="743c0-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="743c0-550">pielāgotais slānis \+ Pašreizējais slānis \- Kopā</span><span class="sxs-lookup"><span data-stu-id="743c0-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="743c0-551">1</span><span class="sxs-lookup"><span data-stu-id="743c0-551">1</span></span>          | <span data-ttu-id="743c0-552">Nomas izdevumi</span><span class="sxs-lookup"><span data-stu-id="743c0-552">Lease expense</span></span>            | <span data-ttu-id="743c0-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="743c0-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-554">1,000\.00</span></span>               |   | <span data-ttu-id="743c0-555">\-1000</span><span class="sxs-lookup"><span data-stu-id="743c0-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="743c0-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-556">0\.00</span></span>                                   |
| <span data-ttu-id="743c0-557">2</span><span class="sxs-lookup"><span data-stu-id="743c0-557">2</span></span>          | <span data-ttu-id="743c0-558">Bankas komisija</span><span class="sxs-lookup"><span data-stu-id="743c0-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="743c0-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="743c0-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="743c0-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-561">3\.00</span></span>                                   |
| <span data-ttu-id="743c0-562">3</span><span class="sxs-lookup"><span data-stu-id="743c0-562">3</span></span>          | <span data-ttu-id="743c0-563">PVN izdevumi</span><span class="sxs-lookup"><span data-stu-id="743c0-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="743c0-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="743c0-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="743c0-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-566">5\.00</span></span>                                   |
| <span data-ttu-id="743c0-567">4</span><span class="sxs-lookup"><span data-stu-id="743c0-567">4</span></span>          | <span data-ttu-id="743c0-568">Dzēšanas konts</span><span class="sxs-lookup"><span data-stu-id="743c0-568">Clearing account</span></span>         | <span data-ttu-id="743c0-569">\-1000\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="743c0-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="743c0-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-571">0\.00</span></span>                   |   | <span data-ttu-id="743c0-572">1000</span><span class="sxs-lookup"><span data-stu-id="743c0-572">1,000</span></span>                                           |                                                | <span data-ttu-id="743c0-573">\-1000</span><span class="sxs-lookup"><span data-stu-id="743c0-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="743c0-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-574">0\.00</span></span>                                   |
| <span data-ttu-id="743c0-575">5</span><span class="sxs-lookup"><span data-stu-id="743c0-575">5</span></span>          | <span data-ttu-id="743c0-576">Kreditoru parādi</span><span class="sxs-lookup"><span data-stu-id="743c0-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="743c0-577">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="743c0-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-578">1,008\.00</span></span>                                         | <span data-ttu-id="743c0-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="743c0-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-580">0\.00</span></span>                                   |
| <span data-ttu-id="743c0-581">6</span><span class="sxs-lookup"><span data-stu-id="743c0-581">6</span></span>          | <span data-ttu-id="743c0-582">LLT līdzeklis</span><span class="sxs-lookup"><span data-stu-id="743c0-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="743c0-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="743c0-584">22,794</span><span class="sxs-lookup"><span data-stu-id="743c0-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="743c0-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="743c0-585">22,793\.90</span></span>                              |
| <span data-ttu-id="743c0-586">7</span><span class="sxs-lookup"><span data-stu-id="743c0-586">7</span></span>          | <span data-ttu-id="743c0-587">Finanšu nomas saistības</span><span class="sxs-lookup"><span data-stu-id="743c0-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="743c0-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="743c0-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="743c0-589">\-22,794</span></span>                                       | <span data-ttu-id="743c0-590">1000</span><span class="sxs-lookup"><span data-stu-id="743c0-590">1,000</span></span>                                          | <span data-ttu-id="743c0-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="743c0-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="743c0-592">\-21 888\.87</span><span class="sxs-lookup"><span data-stu-id="743c0-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="743c0-593">8</span><span class="sxs-lookup"><span data-stu-id="743c0-593">8</span></span>          | <span data-ttu-id="743c0-594">Maksājamie procenti</span><span class="sxs-lookup"><span data-stu-id="743c0-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="743c0-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="743c0-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="743c0-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="743c0-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="743c0-597">94\.97</span></span>                                  |
| <span data-ttu-id="743c0-598">9</span><span class="sxs-lookup"><span data-stu-id="743c0-598">9</span></span>          | <span data-ttu-id="743c0-599">Kase</span><span class="sxs-lookup"><span data-stu-id="743c0-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="743c0-600">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="743c0-601">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="743c0-602">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="743c0-603">10.</span><span class="sxs-lookup"><span data-stu-id="743c0-603">10</span></span>         | <span data-ttu-id="743c0-604">Nolietojuma izmaksas</span><span class="sxs-lookup"><span data-stu-id="743c0-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="743c0-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="743c0-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="743c0-606">949\.75</span></span>                                        | <span data-ttu-id="743c0-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="743c0-607">949\.75</span></span>                                 |
| <span data-ttu-id="743c0-608">11.</span><span class="sxs-lookup"><span data-stu-id="743c0-608">11</span></span>         | <span data-ttu-id="743c0-609">Uzkrātais nolietojums</span><span class="sxs-lookup"><span data-stu-id="743c0-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="743c0-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="743c0-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="743c0-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="743c0-611">\-949\.75</span></span>                                      | <span data-ttu-id="743c0-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="743c0-612">\-949\.75</span></span>                               |


