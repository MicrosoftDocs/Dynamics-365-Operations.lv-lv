---
title: PVN maksājumi un noapaļošanas kārtulas
description: Šajā rakstā ir izskaidrots, kā iestatīt noapaļošanas kārtulu PVN iestādēm paredzētās atskaitēs, un sniegta informācija par PVN bilances noapaļošanu nosegšanas un PVN iegrāmatošanas darba laikā.
author: ShylaThompson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998dbd01352d3fa5040187e81b564d14133464db
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4445759"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="687ca-103">PVN maksājumi un noapaļošanas kārtulas</span><span class="sxs-lookup"><span data-stu-id="687ca-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="687ca-104">Šajā rakstā ir izskaidrots, kā iestatīt noapaļošanas kārtulu PVN iestādēm paredzētās atskaitēs, un sniegta informācija par PVN bilances noapaļošanu nosegšanas un PVN iegrāmatošanas darba laikā.</span><span class="sxs-lookup"><span data-stu-id="687ca-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="687ca-105">Periodiski ir jāziņo par PVN un tas ir jāsamaksā nodokļu iestādēm.</span><span class="sxs-lookup"><span data-stu-id="687ca-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="687ca-106">To var izdarīt, lapa PVN palaižot procesu Nosegt un grāmatot PVN.</span><span class="sxs-lookup"><span data-stu-id="687ca-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="687ca-107">Noteikta perioda PVN tiek nosegts no PVN kontiem, un PVN apmaksas kontā tiek grāmatota PVN bilance.</span><span class="sxs-lookup"><span data-stu-id="687ca-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="687ca-108">PVN apmaksas kontā grāmatoto PVN bilanci var noapaļot atbilstoši nodokļu iestāžu prasībām, iestatot noapaļošanas kārtulu lapā PVN.</span><span class="sxs-lookup"><span data-stu-id="687ca-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="687ca-109">Noapaļošanas starpība tiek grāmatota PVN noapaļošanas kontā, kas ir atlasīts virsgrāmatas laukā Automātisko darījumu konti.</span><span class="sxs-lookup"><span data-stu-id="687ca-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="687ca-110">Tālāk sniegtajā piemērā ir attēlots, kā darbojas noapaļošanas kārtula nodokļu iestādei.</span><span class="sxs-lookup"><span data-stu-id="687ca-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="687ca-111">Piemēri</span><span class="sxs-lookup"><span data-stu-id="687ca-111">Examples</span></span>

<span data-ttu-id="687ca-112">Kopējā PVN summa par periodu atbilst kredīta bilancei –98 765,43.</span><span class="sxs-lookup"><span data-stu-id="687ca-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="687ca-113">Juridiskā persona ir saņēmusi lielāku PVN summu, nekā tā ir samaksājusi.</span><span class="sxs-lookup"><span data-stu-id="687ca-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="687ca-114">Tāpēc juridiskā persona ir parādā nodokļu iestādei.</span><span class="sxs-lookup"><span data-stu-id="687ca-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="687ca-115">Juridiskā persona vēlas izmantot noapaļošanas metodi, kas noapaļo bilanci līdz tuvākajam veselam skaitlim (1,00).</span><span class="sxs-lookup"><span data-stu-id="687ca-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="687ca-116">Lietotājs, kurš ir atbildīgs par PVN uzskaiti, veic tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="687ca-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="687ca-117">Noklikšķiniet uz  **Nodokļi** > **Netiešie nodokļi** > **PVN** > **Nodokļu iestādes**.</span><span class="sxs-lookup"><span data-stu-id="687ca-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="687ca-118">Kopsavilkuma cilnes **Vispārīgi** laukā **Noapaļošanas veids** atlasiet opciju **Parastais**.</span><span class="sxs-lookup"><span data-stu-id="687ca-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="687ca-119">Laukā **Noapaļošana** ievadiet vērtību 1,00.</span><span class="sxs-lookup"><span data-stu-id="687ca-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="687ca-120">Kad ir pienācis laiks maksāt PVN nodokļu iestādei, dodieties uz **Nodokļi** > **Deklarācijas** > **PVN** > **Nosegt un grāmatot PVN**.</span><span class="sxs-lookup"><span data-stu-id="687ca-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="687ca-121">PVN apmaksas kontā jūs redzēsiet nodokļu parāda summa **98 765,43** tiek noapaļota līdz **98 765**.</span><span class="sxs-lookup"><span data-stu-id="687ca-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="687ca-122">Tālāk esošajā tabulā ir parādīts, kā summa 98 765,43 tiek noapaļota, izmantojot katru noapaļošanas metodi, kas ir pieejama lapas **Nodokļu iestādes** laukā **Noapaļošanas veids**.</span><span class="sxs-lookup"><span data-stu-id="687ca-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="687ca-123">Ja noapaļošanas vērtība ir iestatīta kā 0,00, tad:</span><span class="sxs-lookup"><span data-stu-id="687ca-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="687ca-124">Normālai noapaļošanai uzvedība ir tāda pati kā **Noapaļošana = 0,01**.</span><span class="sxs-lookup"><span data-stu-id="687ca-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="687ca-125">Opcijām **Noapaļošanas veida opcijas**, **Uz zemāku**, **Noapaļošana** un **Pašu priekšrocība** uzvedība ir tāda pati kā **Noapaļošana = 1,00**.</span><span class="sxs-lookup"><span data-stu-id="687ca-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="687ca-126">Noapaļošanas veida opcija</span><span class="sxs-lookup"><span data-stu-id="687ca-126">Rounding form option</span></span>                | <span data-ttu-id="687ca-127">Noapaļošanas vērtība = 0,01</span><span class="sxs-lookup"><span data-stu-id="687ca-127">Round-off value = 0.01</span></span> | <span data-ttu-id="687ca-128">Noapaļošanas vērtība = 0,10</span><span class="sxs-lookup"><span data-stu-id="687ca-128">Round-off value = 0.10</span></span> | <span data-ttu-id="687ca-129">Noapaļošanas vērtība = 1,00</span><span class="sxs-lookup"><span data-stu-id="687ca-129">Round-off value = 1.00</span></span> | <span data-ttu-id="687ca-130">Noapaļošanas vērtība = 100,00</span><span class="sxs-lookup"><span data-stu-id="687ca-130">Round-off value = 100.00</span></span> | <span data-ttu-id="687ca-131">Noapaļošanas vērtība = 0,00</span><span class="sxs-lookup"><span data-stu-id="687ca-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="687ca-132">Parasta</span><span class="sxs-lookup"><span data-stu-id="687ca-132">Normal</span></span>                              | <span data-ttu-id="687ca-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="687ca-133">98,765.43</span></span>              | <span data-ttu-id="687ca-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="687ca-134">98,765.40</span></span>              | <span data-ttu-id="687ca-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="687ca-135">98,765.00</span></span>              | <span data-ttu-id="687ca-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="687ca-136">98,800.00</span></span>                | <span data-ttu-id="687ca-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="687ca-137">98,765.43</span></span>                |
| <span data-ttu-id="687ca-138">Uz zemāku</span><span class="sxs-lookup"><span data-stu-id="687ca-138">Downward</span></span>                            | <span data-ttu-id="687ca-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="687ca-139">98,765.43</span></span>              | <span data-ttu-id="687ca-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="687ca-140">98,765.40</span></span>              | <span data-ttu-id="687ca-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="687ca-141">98,765.00</span></span>              | <span data-ttu-id="687ca-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="687ca-142">98,700.00</span></span>                | <span data-ttu-id="687ca-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="687ca-143">98,765.00</span></span>                |
| <span data-ttu-id="687ca-144">Noapaļošana</span><span class="sxs-lookup"><span data-stu-id="687ca-144">Rounding-up</span></span>                         | <span data-ttu-id="687ca-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="687ca-145">98,765.43</span></span>              | <span data-ttu-id="687ca-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="687ca-146">98,765.50</span></span>              | <span data-ttu-id="687ca-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="687ca-147">98,766.00</span></span>              | <span data-ttu-id="687ca-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="687ca-148">98,800.00</span></span>                | <span data-ttu-id="687ca-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="687ca-149">98,766.00</span></span>                |
| <span data-ttu-id="687ca-150">Pašu priekšrocība kredīta bilancei</span><span class="sxs-lookup"><span data-stu-id="687ca-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="687ca-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="687ca-151">98,765.43</span></span>              | <span data-ttu-id="687ca-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="687ca-152">98,765.40</span></span>              | <span data-ttu-id="687ca-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="687ca-153">98,765.00</span></span>              | <span data-ttu-id="687ca-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="687ca-154">98,700.00</span></span>                | <span data-ttu-id="687ca-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="687ca-155">98,765.00</span></span>                |
| <span data-ttu-id="687ca-156">Pašu priekšrocība debeta bilancei</span><span class="sxs-lookup"><span data-stu-id="687ca-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="687ca-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="687ca-157">98,765.43</span></span>              | <span data-ttu-id="687ca-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="687ca-158">98,765.50</span></span>              | <span data-ttu-id="687ca-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="687ca-159">98,766.00</span></span>              | <span data-ttu-id="687ca-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="687ca-160">98,800.00</span></span>                | <span data-ttu-id="687ca-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="687ca-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="687ca-162">Normāla noapaļošana, un noapaļošanas precizitāte ir 0,01</span><span class="sxs-lookup"><span data-stu-id="687ca-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="687ca-163">Noapaļošana</span><span class="sxs-lookup"><span data-stu-id="687ca-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="687ca-164">Aprēķina process</span><span class="sxs-lookup"><span data-stu-id="687ca-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="687ca-165">noapaļošana (1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="687ca-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="687ca-166">noapaļošana (1,015 / 0,01, 0) = noapaļošana (101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="687ca-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="687ca-167">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="687ca-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="687ca-168">noapaļošana (1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="687ca-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="687ca-169">noapaļošana (1,014 / 0,01, 0) = noapaļošana (101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="687ca-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="687ca-170">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="687ca-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="687ca-171">noapaļošana (1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="687ca-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="687ca-172">noapaļošana (1,011 / 0,02, 0) = noapaļošana (50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="687ca-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="687ca-173">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="687ca-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="687ca-174">noapaļošana (1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="687ca-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="687ca-175">noapaļošana (1,009 / 0,02, 0) = noapaļošana (50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="687ca-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="687ca-176">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="687ca-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="687ca-177">Ja atlasāt opciju Pašu priekšrocība, noapaļošana vienmēr tiek veikta atbilstoši juridiskās personas interesēm.</span><span class="sxs-lookup"><span data-stu-id="687ca-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="687ca-178">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="687ca-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="687ca-179">PVN apskats</span><span class="sxs-lookup"><span data-stu-id="687ca-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="687ca-180">PVN maksājuma izveide</span><span class="sxs-lookup"><span data-stu-id="687ca-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="687ca-181">PVN transakciju izveide dokumentos</span><span class="sxs-lookup"><span data-stu-id="687ca-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="687ca-182">Grāmatoto PVN transakciju skatīšana</span><span class="sxs-lookup"><span data-stu-id="687ca-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="687ca-183">noapaļošanas funkcija</span><span class="sxs-lookup"><span data-stu-id="687ca-183">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


