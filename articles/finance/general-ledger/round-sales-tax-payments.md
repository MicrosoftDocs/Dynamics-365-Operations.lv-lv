---
title: PVN maksājumi un noapaļošanas kārtulas
description: Šajā rakstā ir izskaidrots, kā iestatīt noapaļošanas kārtulu PVN iestādēm paredzētās atskaitēs, un sniegta informācija par PVN bilances noapaļošanu nosegšanas un PVN iegrāmatošanas darba laikā.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
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
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186329"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="8c0d0-103">PVN maksājumi un noapaļošanas kārtulas</span><span class="sxs-lookup"><span data-stu-id="8c0d0-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c0d0-104">Šajā rakstā ir izskaidrots, kā iestatīt noapaļošanas kārtulu PVN iestādēm paredzētās atskaitēs, un sniegta informācija par PVN bilances noapaļošanu nosegšanas un PVN iegrāmatošanas darba laikā.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="8c0d0-105">Periodiski ir jāziņo par PVN un tas ir jāsamaksā nodokļu iestādēm.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="8c0d0-106">To var izdarīt, lapa PVN palaižot procesu Nosegt un grāmatot PVN.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="8c0d0-107">Noteikta perioda PVN tiek nosegts no PVN kontiem, un PVN apmaksas kontā tiek grāmatota PVN bilance.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="8c0d0-108">PVN apmaksas kontā grāmatoto PVN bilanci var noapaļot atbilstoši nodokļu iestāžu prasībām, iestatot noapaļošanas kārtulu lapā PVN.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="8c0d0-109">Noapaļošanas starpība tiek grāmatota PVN noapaļošanas kontā, kas ir atlasīts virsgrāmatas laukā Automātisko darījumu konti.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="8c0d0-110">Tālāk sniegtajā piemērā ir attēlots, kā darbojas noapaļošanas kārtula nodokļu iestādei.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="8c0d0-111">Piemēri</span><span class="sxs-lookup"><span data-stu-id="8c0d0-111">Examples</span></span>

<span data-ttu-id="8c0d0-112">Kopējā PVN summa par periodu atbilst kredīta bilancei –98 765,43.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="8c0d0-113">Juridiskā persona ir saņēmusi lielāku PVN summu, nekā tā ir samaksājusi.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="8c0d0-114">Tāpēc juridiskā persona ir parādā nodokļu iestādei.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="8c0d0-115">Juridiskā persona vēlas izmantot noapaļošanas metodi, kas noapaļo bilanci līdz tuvākajam veselam skaitlim (1,00).</span><span class="sxs-lookup"><span data-stu-id="8c0d0-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="8c0d0-116">Lietotājs, kurš ir atbildīgs par PVN uzskaiti, veic tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="8c0d0-117">Noklikšķiniet uz Nodokļi &gt; Netiešie nodokļi &gt; PVN &gt; Nodokļu iestādes.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="8c0d0-118">Kopsavilkuma cilnes Vispārīgi laukā Noapaļošanas veids atlasiet opciju Parastais.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="8c0d0-119">Laukā Noapaļošana ievadiet vērtību 1,00.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="8c0d0-120">Kad ir pienācis laiks maksāt PVN nodokļu iestādei, atveriet lapu Nosegt un grāmatot PVN.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="8c0d0-121">(Noklikšķiniet uz Nodokļi &gt; Deklarācijas &gt; PVN &gt; Nosegt un grāmatot PVN.)</span><span class="sxs-lookup"><span data-stu-id="8c0d0-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="8c0d0-122">PVN apmaksas kontā nodokļu parāda suma 98 765,43 tiek noapaļota līdz 98 765.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="8c0d0-123">Tālāk esošajā tabulā ir parādīts, kā summa 98 765,43 tiek noapaļota, izmantojot katru noapaļošanas metodi, kas ir pieejama lapas Nodokļu iestādes laukā Noapaļošanas veids.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="8c0d0-124">Noapaļošanas veida opcija</span><span class="sxs-lookup"><span data-stu-id="8c0d0-124">Rounding form option</span></span>                | <span data-ttu-id="8c0d0-125">Noapaļošanas vērtība = 0,01</span><span class="sxs-lookup"><span data-stu-id="8c0d0-125">Round-off value = 0.01</span></span> | <span data-ttu-id="8c0d0-126">Noapaļošanas vērtība = 0,10</span><span class="sxs-lookup"><span data-stu-id="8c0d0-126">Round-off value = 0.10</span></span> | <span data-ttu-id="8c0d0-127">Noapaļošanas vērtība = 1,00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-127">Round-off value = 1.00</span></span> | <span data-ttu-id="8c0d0-128">Noapaļošanas vērtība = 100,00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="8c0d0-129">Parastais</span><span class="sxs-lookup"><span data-stu-id="8c0d0-129">Normal</span></span>                              | <span data-ttu-id="8c0d0-130">98 765,43</span><span class="sxs-lookup"><span data-stu-id="8c0d0-130">98,765.43</span></span>              | <span data-ttu-id="8c0d0-131">98 765,40</span><span class="sxs-lookup"><span data-stu-id="8c0d0-131">98,765.40</span></span>              | <span data-ttu-id="8c0d0-132">98 765,00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-132">98,765.00</span></span>              | <span data-ttu-id="8c0d0-133">98 800,00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-133">98,800.00</span></span>                |
| <span data-ttu-id="8c0d0-134">Uz zemāku</span><span class="sxs-lookup"><span data-stu-id="8c0d0-134">Downward</span></span>                            | <span data-ttu-id="8c0d0-135">98 765,43</span><span class="sxs-lookup"><span data-stu-id="8c0d0-135">98,765.43</span></span>              | <span data-ttu-id="8c0d0-136">98 765,40</span><span class="sxs-lookup"><span data-stu-id="8c0d0-136">98,765.40</span></span>              | <span data-ttu-id="8c0d0-137">98 765,00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-137">98,765.00</span></span>              | <span data-ttu-id="8c0d0-138">98 700,00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-138">98,700.00</span></span>                |
| <span data-ttu-id="8c0d0-139">Noapaļošana</span><span class="sxs-lookup"><span data-stu-id="8c0d0-139">Rounding-up</span></span>                         | <span data-ttu-id="8c0d0-140">98 765,43</span><span class="sxs-lookup"><span data-stu-id="8c0d0-140">98,765.43</span></span>              | <span data-ttu-id="8c0d0-141">98 765,50</span><span class="sxs-lookup"><span data-stu-id="8c0d0-141">98,765.50</span></span>              | <span data-ttu-id="8c0d0-142">98 766,00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-142">98,766.00</span></span>              | <span data-ttu-id="8c0d0-143">98 800,00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-143">98,800.00</span></span>                |
| <span data-ttu-id="8c0d0-144">Pašu priekšrocība kredīta bilancei</span><span class="sxs-lookup"><span data-stu-id="8c0d0-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="8c0d0-145">98 765,43</span><span class="sxs-lookup"><span data-stu-id="8c0d0-145">98,765.43</span></span>              | <span data-ttu-id="8c0d0-146">98 765,40</span><span class="sxs-lookup"><span data-stu-id="8c0d0-146">98,765.40</span></span>              | <span data-ttu-id="8c0d0-147">98 765,00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-147">98,765.00</span></span>              | <span data-ttu-id="8c0d0-148">98 700,00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-148">98,700.00</span></span>                |
| <span data-ttu-id="8c0d0-149">Pašu priekšrocība debeta bilancei</span><span class="sxs-lookup"><span data-stu-id="8c0d0-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="8c0d0-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="8c0d0-150">98,765.43</span></span>              | <span data-ttu-id="8c0d0-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="8c0d0-151">98,765.50</span></span>              | <span data-ttu-id="8c0d0-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-152">98,766.00</span></span>              | <span data-ttu-id="8c0d0-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="8c0d0-154">Noapaļošana netiek veikta, jo noapaļošanai ir 0,00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="8c0d0-155">noapaļošana (1,0151, 0,00) = 1,0151 noapaļošana (1,0149, 0,0) = 1,0149</span><span class="sxs-lookup"><span data-stu-id="8c0d0-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="8c0d0-156">Normāla noapaļošana, un noapaļošanas precizitāte ir 0,01</span><span class="sxs-lookup"><span data-stu-id="8c0d0-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="8c0d0-157">Noapaļošana</span><span class="sxs-lookup"><span data-stu-id="8c0d0-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="8c0d0-158">Aprēķina process</span><span class="sxs-lookup"><span data-stu-id="8c0d0-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="8c0d0-159">noapaļošana (1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="8c0d0-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="8c0d0-160">noapaļošana (1,015 / 0,01, 0) = noapaļošana (101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="8c0d0-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="8c0d0-161">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="8c0d0-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="8c0d0-162">noapaļošana (1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="8c0d0-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="8c0d0-163">noapaļošana (1,014 / 0,01, 0) = noapaļošana (101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="8c0d0-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="8c0d0-164">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="8c0d0-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="8c0d0-165">noapaļošana (1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="8c0d0-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="8c0d0-166">noapaļošana (1,011 / 0,02, 0) = noapaļošana (50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="8c0d0-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="8c0d0-167">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="8c0d0-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="8c0d0-168">noapaļošana (1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="8c0d0-169">noapaļošana (1,009 / 0,02, 0) = noapaļošana (50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="8c0d0-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="8c0d0-170">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="8c0d0-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="8c0d0-171">Ja atlasāt opciju Pašu priekšrocība, noapaļošana vienmēr tiek veikta atbilstoši juridiskās personas interesēm.</span><span class="sxs-lookup"><span data-stu-id="8c0d0-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="8c0d0-172">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="8c0d0-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="8c0d0-173">PVN apskats</span><span class="sxs-lookup"><span data-stu-id="8c0d0-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="8c0d0-174">PVN maksājuma izveide</span><span class="sxs-lookup"><span data-stu-id="8c0d0-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="8c0d0-175">Izveidot PVN transakcijas dokumentos</span><span class="sxs-lookup"><span data-stu-id="8c0d0-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="8c0d0-176">Grāmatoto PVN transakciju skatīšana</span><span class="sxs-lookup"><span data-stu-id="8c0d0-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="8c0d0-177">noapaļošanas funkcija</span><span class="sxs-lookup"><span data-stu-id="8c0d0-177">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


