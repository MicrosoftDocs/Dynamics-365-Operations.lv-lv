---
title: PVN aprēķins vispārējā žurnālā.
description: Šajā tēmā izskaidrots, kā PVN tiek aprēķināts dažādiem kontu tipiem (kreditora, klienta, virsgrāmatas un projekta) vispārējā žurnālā.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: dd1df355d39065d6959915cc916987d3c58b15a6
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570198"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="ca8b9-103">PVN aprēķins vispārējā žurnālā.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca8b9-104">Šajā tēmā izskaidrots, kā PVN tiek aprēķināts dažādiem kontu tipiem (kreditora, klienta, virsgrāmatas un projekta) vispārējā žurnālā.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="ca8b9-105">Procesu var sadalīt trīs daļās:</span><span class="sxs-lookup"><span data-stu-id="ca8b9-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="ca8b9-106">Nosakiet PVN virzienu.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="ca8b9-107">Nosakiet PVN summu, kas tiks saglabāta pagaidu PVN tabulā.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="ca8b9-108">Nosakiet PVN summu un kontu dokumentā.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="ca8b9-109">Nosakiet PVN virzienu.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-109">Determine the sales tax direction</span></span>

<span data-ttu-id="ca8b9-110">PVN virziena noteikšanas veids ir atkarīgs no konta tipa dokumentā.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="ca8b9-111">PVN virzienu nosaka konta tipa un PVN koda kombinācija.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="ca8b9-112">Tālāk norādītajās sadaļās ir sīkāk aprakstītas iespējas.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="ca8b9-113">Konta  tips ir projekts.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-113">Account type is Project</span></span>

<span data-ttu-id="ca8b9-114">Ja dokumentam ir žurnāla rinda, kur konta tips ir **Projekts**, visas žurnāla rindas dokumentā lieto vienu un to pašu nodokļu virzienu.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="ca8b9-115">Tālāk esošajā attēlā ir parādīts kārtula.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-115">The following illustration shows the rule.</span></span> <span data-ttu-id="ca8b9-116">Šie punkti parāda iespējamos nodokļu norādījumus projektu kontos.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="ca8b9-117">• Ja PVN kods ir importa nodoklis, tad arī PVN virziens ir importa nodoklis.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="ca8b9-118">• Ja PVN kods ir ar nodokli neapliekams, tad arī PVN virziens ir nodokli neapliekams pirkums.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="ca8b9-119">• Ja PVN kods ir iekšējais nodoklis, tad PVN virziens ir Maksājamais PVN.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="ca8b9-120">• Ja PVN kods ir apgrieztais nodoklis, tad PVN virziens ir Maksājamais PVN.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="ca8b9-121">Pretējā gadījumā PVN virziens ir Saņemamais PVN.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="ca8b9-122">Sekojošā diagramma attēlo šo kārtulu grafiski.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-122">The following diagram illustrates the rule graphically.</span></span>

![Nodokļu virziena iespējas projektu kontiem.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="ca8b9-124">Konta tips ir Kreditors.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-124">Account type is Vendor</span></span>

<span data-ttu-id="ca8b9-125">Ja dokumentam ir žurnāla rinda, kur konta tips ir **Kreditors**, visas žurnāla rindas dokumentā lieto vienu un to pašu nodokļu virzienu.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="ca8b9-126">Šie punkti parāda iespējamos nodokļu norādījumus kreditoru kontos.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="ca8b9-127">• Ja PVN kods ir ar nodokli neapliekams, tad arī PVN virziens ir nodokli neapliekams pirkums.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-127">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="ca8b9-128">• Ja PVN kods ir iekšējais nodoklis, tad PVN virziens ir Saņemamais PVN.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-128">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="ca8b9-129">• Ja PVN kods ir apgrieztais nodoklis, tad PVN virziens ir Saņemamais PVN.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-129">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>


<span data-ttu-id="ca8b9-130">Pretējā gadījumā PVN virziens ir Maksājamais PVN.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-130">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="ca8b9-131">Sekojošā diagramma attēlo šo kārtulu grafiski.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-131">The following diagram illustrates the rule graphically.</span></span>

![Nodokļu virziena iespējas kreditoru kontiem.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="ca8b9-133">Konta tips ir Klients.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-133">Account type is Customer</span></span>

<span data-ttu-id="ca8b9-134">Ja dokumentam ir žurnāla rinda, kur konta tips ir **Klients**, visas žurnāla rindas dokumentā lieto vienu un to pašu nodokļu virzienu.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-134">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="ca8b9-135">Šie punkti parāda iespējamos nodokļu norādījumus klientu kontiem.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-135">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="ca8b9-136">• Ja PVN kods ir importa nodoklis, tad arī PVN virziens ir importa nodoklis.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-136">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="ca8b9-137">• Ja PVN kods ir ar nodokli neapliekams, tad arī PVN virziens ir nodokli neapliekams pirkums.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="ca8b9-138">• Ja PVN kods ir iekšējais nodoklis, tad PVN virziens ir Maksājamais PVN.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="ca8b9-139">• Ja PVN kods ir apgrieztais nodoklis, tad PVN virziens ir Maksājamais PVN.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="ca8b9-140">Pretējā gadījumā PVN virziens ir Saņemamais PVN.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-140">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="ca8b9-141">Sekojošā diagramma attēlo šo kārtulu grafiski.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-141">The following diagram illustrates the rule graphically.</span></span>

![Nodokļu virziena iespējas klientu kontiem.](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="ca8b9-143">Konta veids ir Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-143">Account type is Ledger</span></span>

<span data-ttu-id="ca8b9-144">Sekojošajā attēlā ir parādīts noteikums, kas tiek lietots, kad dokumentam ir tikai tās žurnāla rindas, kurās konta tips ir **Virsgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="ca8b9-145">Šie punkti parāda iespējamos nodokļu norādījumus virsgrāmatu kontiem.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="ca8b9-146">• Ja PVN kods ir importa nodoklis, tad arī PVN virziens ir importa nodoklis.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="ca8b9-147">• Ja PVN kods ir ar nodokli neapliekams, tad arī PVN virziens ir nodokli neapliekams pirkums.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="ca8b9-148">Pretējā gadījumā, ja žurnāla summa ir debets (pozitīvs), PVN virziens ir Saņemamais PVN; ja žurnāla summa ir kredīts (negatīvs), PVN virziens ir Maksājamais PVN.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="ca8b9-149">Sekojošā diagramma attēlo šo kārtulu grafiski.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-149">The following diagram illustrates the rule graphically.</span></span>

![Nodokļu virziena iespējas virsgrāmatu kontiem.](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="ca8b9-151">Labojiet PVN virzienu.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-151">Override the sales tax direction</span></span>

<span data-ttu-id="ca8b9-152">PVN virzienu var ignorēt, ja dokumentā ir tikai rindas, kurās konta tips ir **Virsgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="ca8b9-153">Dodieties uz **Virsgrāmata\>Kontu plāns\>Konti\>Galvenie konti**un atlasiet **Juridisko personu labojumi** kopsavilkuma cilnē.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="ca8b9-154">Nosakiet PVN summu</span><span class="sxs-lookup"><span data-stu-id="ca8b9-154">Determine the sales tax amount</span></span>

<span data-ttu-id="ca8b9-155">Šajā sadaļā ir aprakstīts, kā tiek aprēķināta PVN summa.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-155">This section describes how the sales tax amount sign is calculated.</span></span>

![PVN darījumu lapa](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="ca8b9-157">Sekojošajā tabulā ir parādīts vispārīgais noteikums, lai noteiktu PVN summas apjomu pagaidu PVN tabulā.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="ca8b9-158">Žurnāla līniju apjoms</span><span class="sxs-lookup"><span data-stu-id="ca8b9-158">Journal line amount</span></span> | <span data-ttu-id="ca8b9-159">PVN virziens</span><span class="sxs-lookup"><span data-stu-id="ca8b9-159">Sales tax direction</span></span>  | <span data-ttu-id="ca8b9-160">PVN summas apjoms</span><span class="sxs-lookup"><span data-stu-id="ca8b9-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="ca8b9-161">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-161">Positive</span></span>            | <span data-ttu-id="ca8b9-162">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="ca8b9-162">Sales Tax Receivable</span></span> | <span data-ttu-id="ca8b9-163">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-163">Positive</span></span>              |
| <span data-ttu-id="ca8b9-164">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-164">Positive</span></span>            | <span data-ttu-id="ca8b9-165">Maksājamais PVN</span><span class="sxs-lookup"><span data-stu-id="ca8b9-165">Sales Tax Payable</span></span>    | <span data-ttu-id="ca8b9-166">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-166">Negative</span></span>              |
| <span data-ttu-id="ca8b9-167">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-167">Negative</span></span>            | <span data-ttu-id="ca8b9-168">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="ca8b9-168">Sales Tax Receivable</span></span> | <span data-ttu-id="ca8b9-169">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-169">Negative</span></span>              |
| <span data-ttu-id="ca8b9-170">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-170">Negative</span></span>            | <span data-ttu-id="ca8b9-171">Maksājamais PVN</span><span class="sxs-lookup"><span data-stu-id="ca8b9-171">Sales Tax Payable</span></span>    | <span data-ttu-id="ca8b9-172">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-172">Positive</span></span>              |

<span data-ttu-id="ca8b9-173">Pastāv īpašs noteikums dokumentiem, kuriem ir tikai **Projekta** vai **Virsgrāmatas** rindas gadījumos, kad **Virsgrāmatas** rindā ir atlasīta PVN grupa vai preces PVN grupa.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="ca8b9-174">Šo noteikumu kontrolē, iespējojot neatkarīgu PVN aprēķināšanas funkciju vispārējiem žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="ca8b9-175">Kad šī funkcija ir izslēgta, **Virsgrāmatas** rindas nodokļa summa izmanto **Projekta** rindas debeta/kredīta virzienu.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="ca8b9-176">Kad šī funkcija ir ieslēgta, **Virsgrāmatas** rindas nodokļa summa izmanto savu projekta rindas debeta/kredīta virzienu.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="ca8b9-177">Sekojošajās Tabulās ir parādīts katra scenārija noteikums.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="ca8b9-178">**Noteikums, kad līdzeklis ir ieslēgts.**</span><span class="sxs-lookup"><span data-stu-id="ca8b9-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="ca8b9-179">Projekta žurnāla rindas apjoms</span><span class="sxs-lookup"><span data-stu-id="ca8b9-179">Journal line amount of project</span></span> | <span data-ttu-id="ca8b9-180">PVN virziens</span><span class="sxs-lookup"><span data-stu-id="ca8b9-180">Sales tax direction</span></span>  | <span data-ttu-id="ca8b9-181">PVN summas apjoms</span><span class="sxs-lookup"><span data-stu-id="ca8b9-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="ca8b9-182">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-182">Positive</span></span>                       | <span data-ttu-id="ca8b9-183">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="ca8b9-183">Sales Tax Receivable</span></span> | <span data-ttu-id="ca8b9-184">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-184">Positive</span></span>              |
| <span data-ttu-id="ca8b9-185">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-185">Negative</span></span>                       | <span data-ttu-id="ca8b9-186">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="ca8b9-186">Sales Tax Receivable</span></span> | <span data-ttu-id="ca8b9-187">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-187">Negative</span></span>              |

<span data-ttu-id="ca8b9-188">**Noteikums, kad līdzeklis ir izslēgts.**</span><span class="sxs-lookup"><span data-stu-id="ca8b9-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="ca8b9-189">Virsgrāmatas žurnāla rindas apjoms</span><span class="sxs-lookup"><span data-stu-id="ca8b9-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="ca8b9-190">PVN virziens</span><span class="sxs-lookup"><span data-stu-id="ca8b9-190">Sales tax direction</span></span>  | <span data-ttu-id="ca8b9-191">PVN summas apjoms</span><span class="sxs-lookup"><span data-stu-id="ca8b9-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="ca8b9-192">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-192">Positive</span></span>                       | <span data-ttu-id="ca8b9-193">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="ca8b9-193">Sales Tax Receivable</span></span> | <span data-ttu-id="ca8b9-194">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-194">Positive</span></span>              |
| <span data-ttu-id="ca8b9-195">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-195">Negative</span></span>                       | <span data-ttu-id="ca8b9-196">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="ca8b9-196">Sales Tax Receivable</span></span> | <span data-ttu-id="ca8b9-197">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="ca8b9-198">Nosakiet PVN summu un kontu dokumentā.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="ca8b9-199">Grāmatojot PVN, galvenais konts tiek iegūts no Virsgrāmatas grāmatošanas grupas profila.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="ca8b9-200">Kad tiek saņemti PVN ieņēmumi, sistēma izmanto profilā norādīto PVN saņemamo kontu.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="ca8b9-201">Izejamajiem PVN maksājumiem sistēma izmanto profilā norādīto maksājamo PVN kontu.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="ca8b9-202">Tālāk esošajā tabulā parādīts galvenais noteikums.</span><span class="sxs-lookup"><span data-stu-id="ca8b9-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="ca8b9-203">PVN virziens</span><span class="sxs-lookup"><span data-stu-id="ca8b9-203">Sales tax direction</span></span>  | <span data-ttu-id="ca8b9-204">PVN summas apjoms</span><span class="sxs-lookup"><span data-stu-id="ca8b9-204">Sales tax amount sign</span></span> | <span data-ttu-id="ca8b9-205">PVN konts</span><span class="sxs-lookup"><span data-stu-id="ca8b9-205">Sales tax account</span></span>      | <span data-ttu-id="ca8b9-206">Dokumenta summa</span><span class="sxs-lookup"><span data-stu-id="ca8b9-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="ca8b9-207">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="ca8b9-207">Sales Tax Receivable</span></span> | <span data-ttu-id="ca8b9-208">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-208">Positive</span></span>              | <span data-ttu-id="ca8b9-209">Saņemamā nodokļa konts</span><span class="sxs-lookup"><span data-stu-id="ca8b9-209">Tax Receivable Account</span></span> | <span data-ttu-id="ca8b9-210">Pozitīvs (debits)</span><span class="sxs-lookup"><span data-stu-id="ca8b9-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="ca8b9-211">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="ca8b9-211">Sales Tax Receivable</span></span> | <span data-ttu-id="ca8b9-212">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-212">Negative</span></span>              | <span data-ttu-id="ca8b9-213">Saņemamā nodokļa konts</span><span class="sxs-lookup"><span data-stu-id="ca8b9-213">Tax Receivable Account</span></span> | <span data-ttu-id="ca8b9-214">Negatīvs (kredīts)</span><span class="sxs-lookup"><span data-stu-id="ca8b9-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="ca8b9-215">Maksājamais PVN</span><span class="sxs-lookup"><span data-stu-id="ca8b9-215">Sales Tax Payable</span></span>    | <span data-ttu-id="ca8b9-216">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-216">Positive</span></span>              | <span data-ttu-id="ca8b9-217">Kreditoru konts</span><span class="sxs-lookup"><span data-stu-id="ca8b9-217">Tax Payable Account</span></span>    | <span data-ttu-id="ca8b9-218">Negatīvs (kredīts)</span><span class="sxs-lookup"><span data-stu-id="ca8b9-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="ca8b9-219">Maksājamais PVN</span><span class="sxs-lookup"><span data-stu-id="ca8b9-219">Sales Tax Payable</span></span>    | <span data-ttu-id="ca8b9-220">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="ca8b9-220">Negative</span></span>              | <span data-ttu-id="ca8b9-221">Kreditoru konts</span><span class="sxs-lookup"><span data-stu-id="ca8b9-221">Tax Payable Account</span></span>    | <span data-ttu-id="ca8b9-222">Pozitīvs (debits)</span><span class="sxs-lookup"><span data-stu-id="ca8b9-222">Positive (Debit)</span></span>  |
