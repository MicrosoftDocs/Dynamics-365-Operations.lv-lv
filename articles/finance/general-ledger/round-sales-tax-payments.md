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
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7be9be728a6515bb1fc1c9bc90938a3d33ea8da8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204958"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="a359e-103">PVN maksājumi un noapaļošanas kārtulas</span><span class="sxs-lookup"><span data-stu-id="a359e-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a359e-104">Šajā rakstā ir izskaidrots, kā iestatīt noapaļošanas kārtulu PVN iestādēm paredzētās atskaitēs, un sniegta informācija par PVN bilances noapaļošanu nosegšanas un PVN iegrāmatošanas darba laikā.</span><span class="sxs-lookup"><span data-stu-id="a359e-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="a359e-105">Periodiski ir jāziņo par PVN un tas ir jāsamaksā nodokļu iestādēm.</span><span class="sxs-lookup"><span data-stu-id="a359e-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="a359e-106">To var izdarīt, lapa PVN palaižot procesu Nosegt un grāmatot PVN.</span><span class="sxs-lookup"><span data-stu-id="a359e-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="a359e-107">Noteikta perioda PVN tiek nosegts no PVN kontiem, un PVN apmaksas kontā tiek grāmatota PVN bilance.</span><span class="sxs-lookup"><span data-stu-id="a359e-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="a359e-108">PVN apmaksas kontā grāmatoto PVN bilanci var noapaļot atbilstoši nodokļu iestāžu prasībām, iestatot noapaļošanas kārtulu lapā PVN.</span><span class="sxs-lookup"><span data-stu-id="a359e-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="a359e-109">Noapaļošanas starpība tiek grāmatota PVN noapaļošanas kontā, kas ir atlasīts virsgrāmatas laukā Automātisko darījumu konti.</span><span class="sxs-lookup"><span data-stu-id="a359e-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="a359e-110">Tālāk sniegtajā piemērā ir attēlots, kā darbojas noapaļošanas kārtula nodokļu iestādei.</span><span class="sxs-lookup"><span data-stu-id="a359e-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="a359e-111">Piemēri</span><span class="sxs-lookup"><span data-stu-id="a359e-111">Examples</span></span>

<span data-ttu-id="a359e-112">Kopējā PVN summa par periodu atbilst kredīta bilancei –98 765,43.</span><span class="sxs-lookup"><span data-stu-id="a359e-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="a359e-113">Juridiskā persona ir saņēmusi lielāku PVN summu, nekā tā ir samaksājusi.</span><span class="sxs-lookup"><span data-stu-id="a359e-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="a359e-114">Tāpēc juridiskā persona ir parādā nodokļu iestādei.</span><span class="sxs-lookup"><span data-stu-id="a359e-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="a359e-115">Juridiskā persona vēlas izmantot noapaļošanas metodi, kas noapaļo bilanci līdz tuvākajam veselam skaitlim (1,00).</span><span class="sxs-lookup"><span data-stu-id="a359e-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="a359e-116">Lietotājs, kurš ir atbildīgs par PVN uzskaiti, veic tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="a359e-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="a359e-117">Noklikšķiniet uz  **Nodokļi** > **Netiešie nodokļi** > **PVN** > **Nodokļu iestādes**.</span><span class="sxs-lookup"><span data-stu-id="a359e-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="a359e-118">Kopsavilkuma cilnes **Vispārīgi** laukā **Noapaļošanas veids** atlasiet opciju **Parastais**.</span><span class="sxs-lookup"><span data-stu-id="a359e-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="a359e-119">Laukā **Noapaļošana** ievadiet vērtību 1,00.</span><span class="sxs-lookup"><span data-stu-id="a359e-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="a359e-120">Kad ir pienācis laiks maksāt PVN nodokļu iestādei, dodieties uz **Nodokļi** > **Deklarācijas** > **PVN** > **Nosegt un grāmatot PVN**.</span><span class="sxs-lookup"><span data-stu-id="a359e-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="a359e-121">PVN apmaksas kontā jūs redzēsiet nodokļu parāda summa **98 765,43** tiek noapaļota līdz **98 765**.</span><span class="sxs-lookup"><span data-stu-id="a359e-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="a359e-122">Tālāk esošajā tabulā ir parādīts, kā summa 98 765,43 tiek noapaļota, izmantojot katru noapaļošanas metodi, kas ir pieejama lapas **Nodokļu iestādes** laukā **Noapaļošanas veids**.</span><span class="sxs-lookup"><span data-stu-id="a359e-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="a359e-123">Ja noapaļošanas vērtība ir iestatīta kā 0,00, tad:</span><span class="sxs-lookup"><span data-stu-id="a359e-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="a359e-124">Normālai noapaļošanai uzvedība ir tāda pati kā **Noapaļošana = 0,01**.</span><span class="sxs-lookup"><span data-stu-id="a359e-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="a359e-125">Opcijām **Noapaļošanas veida opcijas**, **Uz zemāku**, **Noapaļošana** un **Pašu priekšrocība** uzvedība ir tāda pati kā **Noapaļošana = 1,00**.</span><span class="sxs-lookup"><span data-stu-id="a359e-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="a359e-126">Noapaļošanas veida opcija</span><span class="sxs-lookup"><span data-stu-id="a359e-126">Rounding form option</span></span>                | <span data-ttu-id="a359e-127">Noapaļošanas vērtība = 0,01</span><span class="sxs-lookup"><span data-stu-id="a359e-127">Round-off value = 0.01</span></span> | <span data-ttu-id="a359e-128">Noapaļošanas vērtība = 0,10</span><span class="sxs-lookup"><span data-stu-id="a359e-128">Round-off value = 0.10</span></span> | <span data-ttu-id="a359e-129">Noapaļošanas vērtība = 1,00</span><span class="sxs-lookup"><span data-stu-id="a359e-129">Round-off value = 1.00</span></span> | <span data-ttu-id="a359e-130">Noapaļošanas vērtība = 100,00</span><span class="sxs-lookup"><span data-stu-id="a359e-130">Round-off value = 100.00</span></span> | <span data-ttu-id="a359e-131">Noapaļošanas vērtība = 0,00</span><span class="sxs-lookup"><span data-stu-id="a359e-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="a359e-132">Parasta</span><span class="sxs-lookup"><span data-stu-id="a359e-132">Normal</span></span>                              | <span data-ttu-id="a359e-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="a359e-133">98,765.43</span></span>              | <span data-ttu-id="a359e-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="a359e-134">98,765.40</span></span>              | <span data-ttu-id="a359e-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="a359e-135">98,765.00</span></span>              | <span data-ttu-id="a359e-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="a359e-136">98,800.00</span></span>                | <span data-ttu-id="a359e-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="a359e-137">98,765.43</span></span>                |
| <span data-ttu-id="a359e-138">Uz zemāku</span><span class="sxs-lookup"><span data-stu-id="a359e-138">Downward</span></span>                            | <span data-ttu-id="a359e-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="a359e-139">98,765.43</span></span>              | <span data-ttu-id="a359e-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="a359e-140">98,765.40</span></span>              | <span data-ttu-id="a359e-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="a359e-141">98,765.00</span></span>              | <span data-ttu-id="a359e-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="a359e-142">98,700.00</span></span>                | <span data-ttu-id="a359e-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="a359e-143">98,765.00</span></span>                |
| <span data-ttu-id="a359e-144">Noapaļošana</span><span class="sxs-lookup"><span data-stu-id="a359e-144">Rounding-up</span></span>                         | <span data-ttu-id="a359e-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="a359e-145">98,765.43</span></span>              | <span data-ttu-id="a359e-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="a359e-146">98,765.50</span></span>              | <span data-ttu-id="a359e-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="a359e-147">98,766.00</span></span>              | <span data-ttu-id="a359e-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="a359e-148">98,800.00</span></span>                | <span data-ttu-id="a359e-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="a359e-149">98,766.00</span></span>                |
| <span data-ttu-id="a359e-150">Pašu priekšrocība kredīta bilancei</span><span class="sxs-lookup"><span data-stu-id="a359e-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="a359e-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="a359e-151">98,765.43</span></span>              | <span data-ttu-id="a359e-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="a359e-152">98,765.40</span></span>              | <span data-ttu-id="a359e-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="a359e-153">98,765.00</span></span>              | <span data-ttu-id="a359e-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="a359e-154">98,700.00</span></span>                | <span data-ttu-id="a359e-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="a359e-155">98,765.00</span></span>                |
| <span data-ttu-id="a359e-156">Pašu priekšrocība debeta bilancei</span><span class="sxs-lookup"><span data-stu-id="a359e-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="a359e-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="a359e-157">98,765.43</span></span>              | <span data-ttu-id="a359e-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="a359e-158">98,765.50</span></span>              | <span data-ttu-id="a359e-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="a359e-159">98,766.00</span></span>              | <span data-ttu-id="a359e-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="a359e-160">98,800.00</span></span>                | <span data-ttu-id="a359e-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="a359e-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="a359e-162">Normāla noapaļošana, un noapaļošanas precizitāte ir 0,01</span><span class="sxs-lookup"><span data-stu-id="a359e-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="a359e-163">Noapaļošana</span><span class="sxs-lookup"><span data-stu-id="a359e-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="a359e-164">Aprēķina process</span><span class="sxs-lookup"><span data-stu-id="a359e-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a359e-165">noapaļošana (1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="a359e-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="a359e-166">noapaļošana (1,015 / 0,01, 0) = noapaļošana (101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="a359e-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="a359e-167">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="a359e-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a359e-168">noapaļošana (1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="a359e-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="a359e-169">noapaļošana (1,014 / 0,01, 0) = noapaļošana (101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="a359e-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="a359e-170">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="a359e-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a359e-171">noapaļošana (1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="a359e-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="a359e-172">noapaļošana (1,011 / 0,02, 0) = noapaļošana (50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="a359e-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="a359e-173">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="a359e-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a359e-174">noapaļošana (1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="a359e-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="a359e-175">noapaļošana (1,009 / 0,02, 0) = noapaļošana (50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="a359e-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="a359e-176">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="a359e-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="a359e-177">Ja atlasāt opciju Pašu priekšrocība, noapaļošana vienmēr tiek veikta atbilstoši juridiskās personas interesēm.</span><span class="sxs-lookup"><span data-stu-id="a359e-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="a359e-178">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="a359e-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="a359e-179">PVN apskats</span><span class="sxs-lookup"><span data-stu-id="a359e-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="a359e-180">PVN maksājuma izveide</span><span class="sxs-lookup"><span data-stu-id="a359e-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="a359e-181">PVN transakciju izveide dokumentos</span><span class="sxs-lookup"><span data-stu-id="a359e-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="a359e-182">Grāmatoto PVN transakciju skatīšana</span><span class="sxs-lookup"><span data-stu-id="a359e-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="a359e-183">noapaļošanas funkcija</span><span class="sxs-lookup"><span data-stu-id="a359e-183">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]