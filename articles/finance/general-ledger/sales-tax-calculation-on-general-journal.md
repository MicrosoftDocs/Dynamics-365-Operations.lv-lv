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
ms.openlocfilehash: 354076dbc14f34b83d1cd24f591874b9af856af1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186306"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="085df-103">PVN aprēķins vispārējā žurnālā.</span><span class="sxs-lookup"><span data-stu-id="085df-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="085df-104">Šajā tēmā izskaidrots, kā PVN tiek aprēķināts dažādiem kontu tipiem (kreditora, klienta, virsgrāmatas un projekta) vispārējā žurnālā.</span><span class="sxs-lookup"><span data-stu-id="085df-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="085df-105">Procesu var sadalīt trīs daļās:</span><span class="sxs-lookup"><span data-stu-id="085df-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="085df-106">Nosakiet PVN virzienu.</span><span class="sxs-lookup"><span data-stu-id="085df-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="085df-107">Nosakiet PVN summu, kas tiks saglabāta pagaidu PVN tabulā.</span><span class="sxs-lookup"><span data-stu-id="085df-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="085df-108">Nosakiet PVN summu un kontu dokumentā.</span><span class="sxs-lookup"><span data-stu-id="085df-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="085df-109">Nosakiet PVN virzienu.</span><span class="sxs-lookup"><span data-stu-id="085df-109">Determine the sales tax direction</span></span>

<span data-ttu-id="085df-110">PVN virziena noteikšanas veids ir atkarīgs no konta tipa dokumentā.</span><span class="sxs-lookup"><span data-stu-id="085df-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="085df-111">PVN virzienu nosaka konta tipa un PVN koda kombinācija.</span><span class="sxs-lookup"><span data-stu-id="085df-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="085df-112">Tālāk norādītajās sadaļās ir sīkāk aprakstītas iespējas.</span><span class="sxs-lookup"><span data-stu-id="085df-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="085df-113">Konta  tips ir projekts.</span><span class="sxs-lookup"><span data-stu-id="085df-113">Account type is Project</span></span>

<span data-ttu-id="085df-114">Ja dokumentam ir žurnāla rinda, kur konta tips ir **Projekts**, visas žurnāla rindas dokumentā lieto vienu un to pašu nodokļu virzienu.</span><span class="sxs-lookup"><span data-stu-id="085df-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="085df-115">Tālāk esošajā attēlā ir parādīts kārtula.</span><span class="sxs-lookup"><span data-stu-id="085df-115">The following illustration shows the rule.</span></span> <span data-ttu-id="085df-116">Šie punkti parāda iespējamos nodokļu norādījumus projektu kontos.</span><span class="sxs-lookup"><span data-stu-id="085df-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="085df-117">• Ja PVN kods ir importa nodoklis, tad arī PVN virziens ir importa nodoklis.</span><span class="sxs-lookup"><span data-stu-id="085df-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="085df-118">• Ja PVN kods ir ar nodokli neapliekams, tad arī PVN virziens ir nodokli neapliekams pirkums.</span><span class="sxs-lookup"><span data-stu-id="085df-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="085df-119">• Ja PVN kods ir iekšējais nodoklis, tad PVN virziens ir Maksājamais PVN.</span><span class="sxs-lookup"><span data-stu-id="085df-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="085df-120">• Ja PVN kods ir apgrieztais nodoklis, tad PVN virziens ir Maksājamais PVN.</span><span class="sxs-lookup"><span data-stu-id="085df-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="085df-121">Pretējā gadījumā PVN virziens ir Saņemamais PVN.</span><span class="sxs-lookup"><span data-stu-id="085df-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="085df-122">Sekojošā diagramma attēlo šo kārtulu grafiski.</span><span class="sxs-lookup"><span data-stu-id="085df-122">The following diagram illustrates the rule graphically.</span></span>

![Nodokļu virziena iespējas projektu kontiem.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="085df-124">Konta tips ir Kreditors.</span><span class="sxs-lookup"><span data-stu-id="085df-124">Account type is Vendor</span></span>

<span data-ttu-id="085df-125">Ja dokumentam ir žurnāla rinda, kur konta tips ir **Kreditors**, visas žurnāla rindas dokumentā lieto vienu un to pašu nodokļu virzienu.</span><span class="sxs-lookup"><span data-stu-id="085df-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="085df-126">Šie punkti parāda iespējamos nodokļu norādījumus kreditoru kontos.</span><span class="sxs-lookup"><span data-stu-id="085df-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="085df-127">• Ja PVN kods ir ar nodokli neapliekams, tad arī PVN virziens ir nodokli neapliekams pirkums.</span><span class="sxs-lookup"><span data-stu-id="085df-127">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="085df-128">• Ja PVN kods ir iekšējais nodoklis, tad PVN virziens ir Saņemamais PVN.</span><span class="sxs-lookup"><span data-stu-id="085df-128">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="085df-129">• Ja PVN kods ir apgrieztais nodoklis, tad PVN virziens ir Saņemamais PVN.</span><span class="sxs-lookup"><span data-stu-id="085df-129">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>


<span data-ttu-id="085df-130">Pretējā gadījumā PVN virziens ir Maksājamais PVN.</span><span class="sxs-lookup"><span data-stu-id="085df-130">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="085df-131">Sekojošā diagramma attēlo šo kārtulu grafiski.</span><span class="sxs-lookup"><span data-stu-id="085df-131">The following diagram illustrates the rule graphically.</span></span>

![Nodokļu virziena iespējas kreditoru kontiem.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="085df-133">Konta tips ir Klients.</span><span class="sxs-lookup"><span data-stu-id="085df-133">Account type is Customer</span></span>

<span data-ttu-id="085df-134">Ja dokumentam ir žurnāla rinda, kur konta tips ir **Klients**, visas žurnāla rindas dokumentā lieto vienu un to pašu nodokļu virzienu.</span><span class="sxs-lookup"><span data-stu-id="085df-134">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="085df-135">Šie punkti parāda iespējamos nodokļu norādījumus klientu kontiem.</span><span class="sxs-lookup"><span data-stu-id="085df-135">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="085df-136">• Ja PVN kods ir importa nodoklis, tad arī PVN virziens ir importa nodoklis.</span><span class="sxs-lookup"><span data-stu-id="085df-136">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="085df-137">• Ja PVN kods ir ar nodokli neapliekams, tad arī PVN virziens ir nodokli neapliekams pirkums.</span><span class="sxs-lookup"><span data-stu-id="085df-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="085df-138">• Ja PVN kods ir iekšējais nodoklis, tad PVN virziens ir Maksājamais PVN.</span><span class="sxs-lookup"><span data-stu-id="085df-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="085df-139">• Ja PVN kods ir apgrieztais nodoklis, tad PVN virziens ir Maksājamais PVN.</span><span class="sxs-lookup"><span data-stu-id="085df-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="085df-140">Pretējā gadījumā PVN virziens ir Saņemamais PVN.</span><span class="sxs-lookup"><span data-stu-id="085df-140">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="085df-141">Sekojošā diagramma attēlo šo kārtulu grafiski.</span><span class="sxs-lookup"><span data-stu-id="085df-141">The following diagram illustrates the rule graphically.</span></span>

![Nodokļu virziena iespējas klientu kontiem.](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="085df-143">Konta veids ir Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="085df-143">Account type is Ledger</span></span>

<span data-ttu-id="085df-144">Sekojošajā attēlā ir parādīts noteikums, kas tiek lietots, kad dokumentam ir tikai tās žurnāla rindas, kurās konta tips ir **Virsgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="085df-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="085df-145">Šie punkti parāda iespējamos nodokļu norādījumus virsgrāmatu kontiem.</span><span class="sxs-lookup"><span data-stu-id="085df-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="085df-146">• Ja PVN kods ir importa nodoklis, tad arī PVN virziens ir importa nodoklis.</span><span class="sxs-lookup"><span data-stu-id="085df-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="085df-147">• Ja PVN kods ir ar nodokli neapliekams, tad arī PVN virziens ir nodokli neapliekams pirkums.</span><span class="sxs-lookup"><span data-stu-id="085df-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="085df-148">Pretējā gadījumā, ja žurnāla summa ir debets (pozitīvs), PVN virziens ir Saņemamais PVN; ja žurnāla summa ir kredīts (negatīvs), PVN virziens ir Maksājamais PVN.</span><span class="sxs-lookup"><span data-stu-id="085df-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="085df-149">Sekojošā diagramma attēlo šo kārtulu grafiski.</span><span class="sxs-lookup"><span data-stu-id="085df-149">The following diagram illustrates the rule graphically.</span></span>

![Nodokļu virziena iespējas virsgrāmatu kontiem.](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="085df-151">Labojiet PVN virzienu.</span><span class="sxs-lookup"><span data-stu-id="085df-151">Override the sales tax direction</span></span>

<span data-ttu-id="085df-152">PVN virzienu var ignorēt, ja dokumentā ir tikai rindas, kurās konta tips ir **Virsgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="085df-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="085df-153">Dodieties uz **Virsgrāmata\>Kontu plāns\>Konti\>Galvenie konti**un atlasiet **Juridisko personu labojumi** kopsavilkuma cilnē.</span><span class="sxs-lookup"><span data-stu-id="085df-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="085df-154">Nosakiet PVN summu</span><span class="sxs-lookup"><span data-stu-id="085df-154">Determine the sales tax amount</span></span>

<span data-ttu-id="085df-155">Šajā sadaļā ir aprakstīts, kā tiek aprēķināta PVN summa.</span><span class="sxs-lookup"><span data-stu-id="085df-155">This section describes how the sales tax amount sign is calculated.</span></span>

![PVN darījumu lapa](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="085df-157">Sekojošajā tabulā ir parādīts vispārīgais noteikums, lai noteiktu PVN summas apjomu pagaidu PVN tabulā.</span><span class="sxs-lookup"><span data-stu-id="085df-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="085df-158">Žurnāla līniju apjoms</span><span class="sxs-lookup"><span data-stu-id="085df-158">Journal line amount</span></span> | <span data-ttu-id="085df-159">PVN virziens</span><span class="sxs-lookup"><span data-stu-id="085df-159">Sales tax direction</span></span>  | <span data-ttu-id="085df-160">PVN summas apjoms</span><span class="sxs-lookup"><span data-stu-id="085df-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="085df-161">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="085df-161">Positive</span></span>            | <span data-ttu-id="085df-162">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="085df-162">Sales Tax Receivable</span></span> | <span data-ttu-id="085df-163">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="085df-163">Positive</span></span>              |
| <span data-ttu-id="085df-164">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="085df-164">Positive</span></span>            | <span data-ttu-id="085df-165">Maksājamais PVN</span><span class="sxs-lookup"><span data-stu-id="085df-165">Sales Tax Payable</span></span>    | <span data-ttu-id="085df-166">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="085df-166">Negative</span></span>              |
| <span data-ttu-id="085df-167">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="085df-167">Negative</span></span>            | <span data-ttu-id="085df-168">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="085df-168">Sales Tax Receivable</span></span> | <span data-ttu-id="085df-169">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="085df-169">Negative</span></span>              |
| <span data-ttu-id="085df-170">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="085df-170">Negative</span></span>            | <span data-ttu-id="085df-171">Maksājamais PVN</span><span class="sxs-lookup"><span data-stu-id="085df-171">Sales Tax Payable</span></span>    | <span data-ttu-id="085df-172">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="085df-172">Positive</span></span>              |

<span data-ttu-id="085df-173">Pastāv īpašs noteikums dokumentiem, kuriem ir tikai **Projekta** vai **Virsgrāmatas** rindas gadījumos, kad **Virsgrāmatas** rindā ir atlasīta PVN grupa vai preces PVN grupa.</span><span class="sxs-lookup"><span data-stu-id="085df-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="085df-174">Šo noteikumu kontrolē, iespējojot neatkarīgu PVN aprēķināšanas funkciju vispārējiem žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="085df-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="085df-175">Kad šī funkcija ir izslēgta, **Virsgrāmatas** rindas nodokļa summa izmanto **Projekta** rindas debeta/kredīta virzienu.</span><span class="sxs-lookup"><span data-stu-id="085df-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="085df-176">Kad šī funkcija ir ieslēgta, **Virsgrāmatas** rindas nodokļa summa izmanto savu projekta rindas debeta/kredīta virzienu.</span><span class="sxs-lookup"><span data-stu-id="085df-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="085df-177">Sekojošajās Tabulās ir parādīts katra scenārija noteikums.</span><span class="sxs-lookup"><span data-stu-id="085df-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="085df-178">**Noteikums, kad līdzeklis ir ieslēgts.**</span><span class="sxs-lookup"><span data-stu-id="085df-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="085df-179">Projekta žurnāla rindas apjoms</span><span class="sxs-lookup"><span data-stu-id="085df-179">Journal line amount of project</span></span> | <span data-ttu-id="085df-180">PVN virziens</span><span class="sxs-lookup"><span data-stu-id="085df-180">Sales tax direction</span></span>  | <span data-ttu-id="085df-181">PVN summas apjoms</span><span class="sxs-lookup"><span data-stu-id="085df-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="085df-182">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="085df-182">Positive</span></span>                       | <span data-ttu-id="085df-183">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="085df-183">Sales Tax Receivable</span></span> | <span data-ttu-id="085df-184">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="085df-184">Positive</span></span>              |
| <span data-ttu-id="085df-185">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="085df-185">Negative</span></span>                       | <span data-ttu-id="085df-186">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="085df-186">Sales Tax Receivable</span></span> | <span data-ttu-id="085df-187">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="085df-187">Negative</span></span>              |

<span data-ttu-id="085df-188">**Noteikums, kad līdzeklis ir izslēgts.**</span><span class="sxs-lookup"><span data-stu-id="085df-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="085df-189">Virsgrāmatas žurnāla rindas apjoms</span><span class="sxs-lookup"><span data-stu-id="085df-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="085df-190">PVN virziens</span><span class="sxs-lookup"><span data-stu-id="085df-190">Sales tax direction</span></span>  | <span data-ttu-id="085df-191">PVN summas apjoms</span><span class="sxs-lookup"><span data-stu-id="085df-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="085df-192">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="085df-192">Positive</span></span>                       | <span data-ttu-id="085df-193">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="085df-193">Sales Tax Receivable</span></span> | <span data-ttu-id="085df-194">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="085df-194">Positive</span></span>              |
| <span data-ttu-id="085df-195">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="085df-195">Negative</span></span>                       | <span data-ttu-id="085df-196">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="085df-196">Sales Tax Receivable</span></span> | <span data-ttu-id="085df-197">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="085df-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="085df-198">Nosakiet PVN summu un kontu dokumentā.</span><span class="sxs-lookup"><span data-stu-id="085df-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="085df-199">Grāmatojot PVN, galvenais konts tiek iegūts no Virsgrāmatas grāmatošanas grupas profila.</span><span class="sxs-lookup"><span data-stu-id="085df-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="085df-200">Kad tiek saņemti PVN ieņēmumi, sistēma izmanto profilā norādīto PVN saņemamo kontu.</span><span class="sxs-lookup"><span data-stu-id="085df-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="085df-201">Izejamajiem PVN maksājumiem sistēma izmanto profilā norādīto maksājamo PVN kontu.</span><span class="sxs-lookup"><span data-stu-id="085df-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="085df-202">Tālāk esošajā tabulā parādīts galvenais noteikums.</span><span class="sxs-lookup"><span data-stu-id="085df-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="085df-203">PVN virziens</span><span class="sxs-lookup"><span data-stu-id="085df-203">Sales tax direction</span></span>  | <span data-ttu-id="085df-204">PVN summas apjoms</span><span class="sxs-lookup"><span data-stu-id="085df-204">Sales tax amount sign</span></span> | <span data-ttu-id="085df-205">PVN konts</span><span class="sxs-lookup"><span data-stu-id="085df-205">Sales tax account</span></span>      | <span data-ttu-id="085df-206">Dokumenta summa</span><span class="sxs-lookup"><span data-stu-id="085df-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="085df-207">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="085df-207">Sales Tax Receivable</span></span> | <span data-ttu-id="085df-208">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="085df-208">Positive</span></span>              | <span data-ttu-id="085df-209">Saņemamā nodokļa konts</span><span class="sxs-lookup"><span data-stu-id="085df-209">Tax Receivable Account</span></span> | <span data-ttu-id="085df-210">Pozitīvs (debits)</span><span class="sxs-lookup"><span data-stu-id="085df-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="085df-211">Saņemamais PVN</span><span class="sxs-lookup"><span data-stu-id="085df-211">Sales Tax Receivable</span></span> | <span data-ttu-id="085df-212">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="085df-212">Negative</span></span>              | <span data-ttu-id="085df-213">Saņemamā nodokļa konts</span><span class="sxs-lookup"><span data-stu-id="085df-213">Tax Receivable Account</span></span> | <span data-ttu-id="085df-214">Negatīvs (kredīts)</span><span class="sxs-lookup"><span data-stu-id="085df-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="085df-215">Maksājamais PVN</span><span class="sxs-lookup"><span data-stu-id="085df-215">Sales Tax Payable</span></span>    | <span data-ttu-id="085df-216">Pozitīvs</span><span class="sxs-lookup"><span data-stu-id="085df-216">Positive</span></span>              | <span data-ttu-id="085df-217">Kreditoru konts</span><span class="sxs-lookup"><span data-stu-id="085df-217">Tax Payable Account</span></span>    | <span data-ttu-id="085df-218">Negatīvs (kredīts)</span><span class="sxs-lookup"><span data-stu-id="085df-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="085df-219">Maksājamais PVN</span><span class="sxs-lookup"><span data-stu-id="085df-219">Sales Tax Payable</span></span>    | <span data-ttu-id="085df-220">Negatīvs</span><span class="sxs-lookup"><span data-stu-id="085df-220">Negative</span></span>              | <span data-ttu-id="085df-221">Kreditoru konts</span><span class="sxs-lookup"><span data-stu-id="085df-221">Tax Payable Account</span></span>    | <span data-ttu-id="085df-222">Pozitīvs (debits)</span><span class="sxs-lookup"><span data-stu-id="085df-222">Positive (Debit)</span></span>  |
