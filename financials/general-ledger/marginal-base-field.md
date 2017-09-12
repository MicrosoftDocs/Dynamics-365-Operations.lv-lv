---
title: "PVN likmju aprēķins, pamatojoties uz laukiem Aprēķina pamatā un Aprēķina metode"
description: "Šajā rakstā ir paskaidrots, kā laukos Aprēķina pamatā un Aprēķina metode norādītās vērtības nosaka nodokļu likmes pārdošanas un pirkšanas transakcijās."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: e16e91208cdd6c1a5c904fb763454371b02c71fd
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="517b6-103">PVN likmju aprēķins, pamatojoties uz laukiem Aprēķina pamatā un Aprēķina metode</span><span class="sxs-lookup"><span data-stu-id="517b6-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="517b6-104">Šajā rakstā ir paskaidrots, kā laukos Aprēķina pamatā un Aprēķina metode norādītās vērtības nosaka nodokļu likmes pārdošanas un pirkšanas transakcijās.</span><span class="sxs-lookup"><span data-stu-id="517b6-104">This article explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="517b6-105">Lauks Aprēķina pamatā, kurš atrodas lapas Pārdošanas nodokļa kodi kopsavilkuma cilnē Aprēķins, nosaka, kura summa tiek izmantota atbilstošo nodokļu likmju atlasīšanai no likmēm lapā Pārdošanas nodokļa kodu vērtības.</span><span class="sxs-lookup"><span data-stu-id="517b6-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="517b6-106">Summas tips laukā Aprēķina pamatā kopā ar metodi laukā Aprēķina metode nosaka loģiku transakcijas pareizo nodokļu likmju atrašanai.</span><span class="sxs-lookup"><span data-stu-id="517b6-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="517b6-107">Dažādas vērtību kombinācijas šajos laukos rada ļoti dažādus PVN aprēķinus, kā parādīts turpmākajos piemēros.</span><span class="sxs-lookup"><span data-stu-id="517b6-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="517b6-108">Piemēros tiek izmantoti tādas pašas nodokļu intervālu vērtības, kādas ir iestatītas katram nodokļu kodam lapā Pārdošanas nodokļa kodu vērtības.</span><span class="sxs-lookup"><span data-stu-id="517b6-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="517b6-109">Lai atvērtu šo lapu, lapā PVN kodi noklikšķiniet uz PVN kods &gt; Vērtības.</span><span class="sxs-lookup"><span data-stu-id="517b6-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="517b6-110">Ja vērtība Aprēķina pamatā vienā vai vairākos pārdošanas nodokļa kodos ir balstīta uz rindu summām vai vienībām, tad lauka Aprēķina metode vērtība lapā Virsgrāmatas parametri ir jāiestata uz Rinda.</span><span class="sxs-lookup"><span data-stu-id="517b6-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="517b6-111"> Neto summa rindai</span><span class="sxs-lookup"><span data-stu-id="517b6-111">Net amount per line</span></span>
<span data-ttu-id="517b6-112">Atlasiet šo opciju, lai pārdošanas nodokļa likmes noteiktu, pamatojoties uz neto summu rēķina rindām, izslēdzot pārējos nodokļus.</span><span class="sxs-lookup"><span data-stu-id="517b6-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="517b6-113">Paraugs</span><span class="sxs-lookup"><span data-stu-id="517b6-113">Example</span></span>

<span data-ttu-id="517b6-114">Pārdošanas nodokļa likmes tiek iestatītas tālāk norādītajiem intervāliem.</span><span class="sxs-lookup"><span data-stu-id="517b6-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="517b6-115">Summas intervāls</span><span class="sxs-lookup"><span data-stu-id="517b6-115">Amount interval</span></span>    | <span data-ttu-id="517b6-116">Nodokļa likme</span><span class="sxs-lookup"><span data-stu-id="517b6-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="517b6-117">0 - 50</span><span class="sxs-lookup"><span data-stu-id="517b6-117">0 - 50</span></span>             | <span data-ttu-id="517b6-118">30%</span><span class="sxs-lookup"><span data-stu-id="517b6-118">30%</span></span>      |
| <span data-ttu-id="517b6-119">50 - 100</span><span class="sxs-lookup"><span data-stu-id="517b6-119">50 - 100</span></span>           | <span data-ttu-id="517b6-120">20%</span><span class="sxs-lookup"><span data-stu-id="517b6-120">20%</span></span>      |
| <span data-ttu-id="517b6-121">100–0 (&gt;100)</span><span class="sxs-lookup"><span data-stu-id="517b6-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="517b6-122">10%</span><span class="sxs-lookup"><span data-stu-id="517b6-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="517b6-123">Augšējā robeža nulle (0) pēdējā intervālā nozīmē, ka visas summas, kas pārsniedz 100, tiek iekļautas intervālā.</span><span class="sxs-lookup"><span data-stu-id="517b6-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="517b6-124">Aprēķina pamatā: **Neto summa rindai**</span><span class="sxs-lookup"><span data-stu-id="517b6-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="517b6-125">Aprēķina metode: **Intervāls**</span><span class="sxs-lookup"><span data-stu-id="517b6-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="517b6-126">Jūs iegādājaties 8 lampas, kas maksā 25,00/gabalā.</span><span class="sxs-lookup"><span data-stu-id="517b6-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="517b6-127">Rēķina rindas neto summa ir 200,00.</span><span class="sxs-lookup"><span data-stu-id="517b6-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="517b6-128">Nodokli aprēķina šādi:</span><span class="sxs-lookup"><span data-stu-id="517b6-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="517b6-129">PVN kopsumma = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35,00</span><span class="sxs-lookup"><span data-stu-id="517b6-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="517b6-130">Rēķina kopsumma = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="517b6-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="517b6-131">**Novirze**</span><span class="sxs-lookup"><span data-stu-id="517b6-131">**Variation**</span></span> 

<span data-ttu-id="517b6-132">Ja rēķinā ir divas rindas ar četrām precēm katrā rindā, katras rindas neto summa ir 100,00 un PVN tiek aprēķināts tālāk norādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="517b6-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="517b6-133">1. rindas PVN = 50 x 30% + 50 x 20% = 15 + 10 = 25,00</span><span class="sxs-lookup"><span data-stu-id="517b6-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="517b6-134">2. rindas PVN = 50 x 30% + 50 x 20% = 15 + 10 = 25,00</span><span class="sxs-lookup"><span data-stu-id="517b6-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="517b6-135">PVN kopsumma = 25,00 + 25,00 = 50,00</span><span class="sxs-lookup"><span data-stu-id="517b6-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="517b6-136">Rēķina kopsumma = 200,00 + 50,00 = 250,00</span><span class="sxs-lookup"><span data-stu-id="517b6-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="517b6-137"> Neto summa uz vienību</span><span class="sxs-lookup"><span data-stu-id="517b6-137">Net amount per unit</span></span>
<span data-ttu-id="517b6-138">Atlasiet šo opciju, lai noteiktu pārdošanas nodokļa likmes, pamatojoties uz katras vienības vērtību, izslēdzot pārējos nodokļus.</span><span class="sxs-lookup"><span data-stu-id="517b6-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="517b6-139">Ja ir atlasīta no vienības atkarīga vērtība Aprēķina pamatā, tad Pārdošanas nodokļa kodam ir jānorāda arī Vienība.</span><span class="sxs-lookup"><span data-stu-id="517b6-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="517b6-140">Paraugs</span><span class="sxs-lookup"><span data-stu-id="517b6-140">Example</span></span>

<span data-ttu-id="517b6-141">Pārdošanas nodokļa likmes tiek iestatītas tālāk norādītajiem intervāliem.</span><span class="sxs-lookup"><span data-stu-id="517b6-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="517b6-142">Summa</span><span class="sxs-lookup"><span data-stu-id="517b6-142">Amount</span></span>             | <span data-ttu-id="517b6-143">Nodokļa likme</span><span class="sxs-lookup"><span data-stu-id="517b6-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="517b6-144">0 - 50</span><span class="sxs-lookup"><span data-stu-id="517b6-144">0 - 50</span></span>             | <span data-ttu-id="517b6-145">30%</span><span class="sxs-lookup"><span data-stu-id="517b6-145">30%</span></span>      |
| <span data-ttu-id="517b6-146">50 - 100</span><span class="sxs-lookup"><span data-stu-id="517b6-146">50 - 100</span></span>           | <span data-ttu-id="517b6-147">20%</span><span class="sxs-lookup"><span data-stu-id="517b6-147">20%</span></span>      |
| <span data-ttu-id="517b6-148">100–0 (&gt;100)</span><span class="sxs-lookup"><span data-stu-id="517b6-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="517b6-149">10%</span><span class="sxs-lookup"><span data-stu-id="517b6-149">10%</span></span>      |

<span data-ttu-id="517b6-150">Aprēķina pamatā: **Neto summa uz vienību**</span><span class="sxs-lookup"><span data-stu-id="517b6-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="517b6-151">Aprēķina metode: **Pilna summa**</span><span class="sxs-lookup"><span data-stu-id="517b6-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="517b6-152">Jūs iegādājaties 8 lampas, kas maksā 25,00/gabalā.</span><span class="sxs-lookup"><span data-stu-id="517b6-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="517b6-153">Rēķina rindas neto summa ir 200,00.</span><span class="sxs-lookup"><span data-stu-id="517b6-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="517b6-154">Nodoklis tiek aprēķināts šādi: Pārdošanas nodoklis uz vienību = 25,00 x 30% = 7,50 Kopējais pārdošanas nodoklis = 7,50 x 8 vienības = 60,00 Rēķina kopsumma = 200,00 + 60,00 = 260,00</span><span class="sxs-lookup"><span data-stu-id="517b6-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="517b6-155"> Rēķina bilances neto summa</span><span class="sxs-lookup"><span data-stu-id="517b6-155">Net amount of invoice balance</span></span>

<span data-ttu-id="517b6-156">Atlasiet šo opciju, lai pārdošanas nodokļa likmes noteiktu, pamatojoties uz rēķina kopējo vērtību, izslēdzot pārējos nodokļus.</span><span class="sxs-lookup"><span data-stu-id="517b6-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="517b6-157">Paraugs</span><span class="sxs-lookup"><span data-stu-id="517b6-157">Example</span></span>

<span data-ttu-id="517b6-158">Pārdošanas nodokļa likmes tiek iestatītas tālāk norādītajiem intervāliem.</span><span class="sxs-lookup"><span data-stu-id="517b6-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="517b6-159">Summa</span><span class="sxs-lookup"><span data-stu-id="517b6-159">Amount</span></span>            | <span data-ttu-id="517b6-160">Nodokļa likme</span><span class="sxs-lookup"><span data-stu-id="517b6-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="517b6-161">0 - 50</span><span class="sxs-lookup"><span data-stu-id="517b6-161">0 - 50</span></span>            | <span data-ttu-id="517b6-162">30%</span><span class="sxs-lookup"><span data-stu-id="517b6-162">30%</span></span>      |
| <span data-ttu-id="517b6-163">50 - 100</span><span class="sxs-lookup"><span data-stu-id="517b6-163">50 - 100</span></span>          | <span data-ttu-id="517b6-164">20%</span><span class="sxs-lookup"><span data-stu-id="517b6-164">20%</span></span>      |
| <span data-ttu-id="517b6-165">100–0 (&gt;100)</span><span class="sxs-lookup"><span data-stu-id="517b6-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="517b6-166">10%</span><span class="sxs-lookup"><span data-stu-id="517b6-166">10%</span></span>      |

<span data-ttu-id="517b6-167">Aprēķina pamatā: **Rēķina bilances neto summa**</span><span class="sxs-lookup"><span data-stu-id="517b6-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="517b6-168">Aprēķina metode: **Intervāls** Pārdošanas rēķinā ir 2 rindas, un katrā rindā ir 4 lampas par 25,00 katra.</span><span class="sxs-lookup"><span data-stu-id="517b6-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="517b6-169">Rēķina bilances neto summa ir 4 x 25,00 + 4 x 25,00 = 200,00.</span><span class="sxs-lookup"><span data-stu-id="517b6-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="517b6-170">Nodoklis tiek aprēķināts šādi: Kopējais pārdošanas nodoklis = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Rēķina kopsumma = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="517b6-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="517b6-171"> Bruto summa uz rindu</span><span class="sxs-lookup"><span data-stu-id="517b6-171">Gross amount per line</span></span>

<span data-ttu-id="517b6-172">Atlasiet šo opciju, lai pārdošanas nodokļa likmes noteiktu, pamatojoties uz rindas vērtību, ietverot visus pārējos nodokļus attiecīgajai rindai.</span><span class="sxs-lookup"><span data-stu-id="517b6-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="517b6-173">Pārdošanas nodokļu grupā var būt tikai viens pārdošanas nodokļa kods ar šādu atlasi laukā Aprēķina pamatā.</span><span class="sxs-lookup"><span data-stu-id="517b6-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="517b6-174">Paraugs</span><span class="sxs-lookup"><span data-stu-id="517b6-174">Example</span></span>

<span data-ttu-id="517b6-175">Pārdošanas nodokļa likmes tiek iestatītas tālāk norādītajiem intervāliem.</span><span class="sxs-lookup"><span data-stu-id="517b6-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="517b6-176">Summa</span><span class="sxs-lookup"><span data-stu-id="517b6-176">Amount</span></span>             | <span data-ttu-id="517b6-177">Nodokļa likme</span><span class="sxs-lookup"><span data-stu-id="517b6-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="517b6-178">0 - 50</span><span class="sxs-lookup"><span data-stu-id="517b6-178">0 - 50</span></span>             | <span data-ttu-id="517b6-179">30%</span><span class="sxs-lookup"><span data-stu-id="517b6-179">30%</span></span>      |
| <span data-ttu-id="517b6-180">50 - 100</span><span class="sxs-lookup"><span data-stu-id="517b6-180">50 - 100</span></span>           | <span data-ttu-id="517b6-181">20%</span><span class="sxs-lookup"><span data-stu-id="517b6-181">20%</span></span>      |
| <span data-ttu-id="517b6-182">100–0 (&gt;100)</span><span class="sxs-lookup"><span data-stu-id="517b6-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="517b6-183">10%</span><span class="sxs-lookup"><span data-stu-id="517b6-183">10%</span></span>      |

<span data-ttu-id="517b6-184">Aprēķina pamatā: **Bruto summa uz rindu** Aprēķina metode: **Intervāls** Papildus ir aprēķināts vēl viens nodokļa kods speciālam nodoklim 5,00 par katru lampu.</span><span class="sxs-lookup"><span data-stu-id="517b6-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is an other tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="517b6-185">Nodokli pievieno neto summai pirms PVN aprēķina.</span><span class="sxs-lookup"><span data-stu-id="517b6-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="517b6-186">Jūs iegādājaties 8 lampas, kas maksā 25,00/gabalā.</span><span class="sxs-lookup"><span data-stu-id="517b6-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="517b6-187">Rēķina rindas neto summa ir 200,00.</span><span class="sxs-lookup"><span data-stu-id="517b6-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="517b6-188">Rēķina rindas bruto summa ir 8 x 25,00 + 8 x 5,00 = 240,00.</span><span class="sxs-lookup"><span data-stu-id="517b6-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="517b6-189">Nodoklis tiek aprēķināts šādi: Kopējais pārdošanas nodoklis = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Kopējais nodoklis = 5,00 x 8 = 40,00 Rēķina kopsumma = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="517b6-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="517b6-190">**Novirze**</span><span class="sxs-lookup"><span data-stu-id="517b6-190">**Variation**</span></span> 

<span data-ttu-id="517b6-191">Ja rēķins tiek izveidots, izmantojot 2 rēķina rindas ar 4 precēm katrā, rēķina rindas neto summa ir 100,00.</span><span class="sxs-lookup"><span data-stu-id="517b6-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="517b6-192">Bruto summa (iekļaujot nodokli 4 x 5,00) uz rēķina rindu būtu 120,00, un pārdošanas nodoklis tiek izveidots šādi: 1. pārdošanas nodokļa rēķina rinda = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 2. pārdošanas nodokļa rēķina rinda = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Kopējais pārdošanas nodoklis = 27,00 + 27,00 = 54,00 Kopējais nodoklis = 5,00 x 8 = 40,00 Rēķina kopsumma = 200,00 + 54,00 + 40,00 = 294,00</span><span class="sxs-lookup"><span data-stu-id="517b6-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="517b6-193"> Bruto summa uz vienību</span><span class="sxs-lookup"><span data-stu-id="517b6-193">Gross amount per unit</span></span>

<span data-ttu-id="517b6-194">Atlasiet šo opciju, lai noteiktu pārdošanas nodokļa likmes, pamatojoties uz vienības vērtību, ietverot pārējos nodokļus.</span><span class="sxs-lookup"><span data-stu-id="517b6-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="517b6-195">Pārdošanas nodokļu grupā var būt tikai viens pārdošanas nodokļa kods ar šādu atlasi laukā Aprēķina pamatā.</span><span class="sxs-lookup"><span data-stu-id="517b6-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="517b6-196">Paraugs</span><span class="sxs-lookup"><span data-stu-id="517b6-196">Example</span></span>

<span data-ttu-id="517b6-197">Pārdošanas nodokļa likmes tiek iestatītas tālāk norādītajiem intervāliem.</span><span class="sxs-lookup"><span data-stu-id="517b6-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="517b6-198">Summa</span><span class="sxs-lookup"><span data-stu-id="517b6-198">Amount</span></span>             | <span data-ttu-id="517b6-199">Nodokļa likme</span><span class="sxs-lookup"><span data-stu-id="517b6-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="517b6-200">0 - 50</span><span class="sxs-lookup"><span data-stu-id="517b6-200">0 - 50</span></span>             | <span data-ttu-id="517b6-201">30%</span><span class="sxs-lookup"><span data-stu-id="517b6-201">30%</span></span>      |
| <span data-ttu-id="517b6-202">50 - 100</span><span class="sxs-lookup"><span data-stu-id="517b6-202">50 - 100</span></span>           | <span data-ttu-id="517b6-203">20%</span><span class="sxs-lookup"><span data-stu-id="517b6-203">20%</span></span>      |
| <span data-ttu-id="517b6-204">100–0 (&gt;100)</span><span class="sxs-lookup"><span data-stu-id="517b6-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="517b6-205">10%</span><span class="sxs-lookup"><span data-stu-id="517b6-205">10%</span></span>      |

<span data-ttu-id="517b6-206">Aprēķina pamatā: **Bruto summa uz vienību** Pastāv speciāls nodoklis 5,00 par katru lampu.</span><span class="sxs-lookup"><span data-stu-id="517b6-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="517b6-207">Nodokli pievieno neto summai pirms PVN aprēķina.</span><span class="sxs-lookup"><span data-stu-id="517b6-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="517b6-208">Jūs iegādājaties 8 lampas, kas maksā 25,00/gabalā.</span><span class="sxs-lookup"><span data-stu-id="517b6-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="517b6-209">Vienības bruto summa ir 30,00.</span><span class="sxs-lookup"><span data-stu-id="517b6-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="517b6-210">Nodoklis tiek aprēķināts šādi: Pārdošanas nodoklis uz vienību = 30 x 30% = 9,00 Kopējais pārdošanas nodoklis = 9,00 x 8 = 72,00 Kopējais nodoklis = 5,00 x 8 = 40,00 Rēķina kopsumma = 200,00 + 72,00 + 40,00 = 312,00</span><span class="sxs-lookup"><span data-stu-id="517b6-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="517b6-211"> Rēķina kopsumma, iesk. pārējās pārdošanas nodokļa summas</span><span class="sxs-lookup"><span data-stu-id="517b6-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="517b6-212">Atlasiet šo opciju, lai pārdošanas nodokļa likmes noteiktu, pamatojoties uz rēķina kopējo vērtību, iekļaujot pārējos nodokļus.</span><span class="sxs-lookup"><span data-stu-id="517b6-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="517b6-213">Ja ir atlasīta šī lauka Aprēķina pamatā vērtība, PVN grupā var ietvert tikai vienu PVN kodu</span><span class="sxs-lookup"><span data-stu-id="517b6-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="517b6-214">Paraugs</span><span class="sxs-lookup"><span data-stu-id="517b6-214">Example</span></span>

<span data-ttu-id="517b6-215">Pārdošanas nodokļa likmes tiek iestatītas tālāk norādītajiem intervāliem.</span><span class="sxs-lookup"><span data-stu-id="517b6-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="517b6-216">Summa</span><span class="sxs-lookup"><span data-stu-id="517b6-216">Amount</span></span>             | <span data-ttu-id="517b6-217">Nodokļa likme</span><span class="sxs-lookup"><span data-stu-id="517b6-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="517b6-218">0 - 50</span><span class="sxs-lookup"><span data-stu-id="517b6-218">0 - 50</span></span>             | <span data-ttu-id="517b6-219">30%</span><span class="sxs-lookup"><span data-stu-id="517b6-219">30%</span></span>      |
| <span data-ttu-id="517b6-220">50 - 100</span><span class="sxs-lookup"><span data-stu-id="517b6-220">50 - 100</span></span>           | <span data-ttu-id="517b6-221">20%</span><span class="sxs-lookup"><span data-stu-id="517b6-221">20%</span></span>      |
| <span data-ttu-id="517b6-222">100–0 (&gt;100)</span><span class="sxs-lookup"><span data-stu-id="517b6-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="517b6-223">10%</span><span class="sxs-lookup"><span data-stu-id="517b6-223">10%</span></span>      |

<span data-ttu-id="517b6-224">Aprēķina pamatā: **Rēķina kopsumma, iesk. citas PVN summas** Aprēķina metode: **Intervāls** </span><span class="sxs-lookup"><span data-stu-id="517b6-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="517b6-225">Katra lampa ir aplikta ar īpašu nodokli 5,00.</span><span class="sxs-lookup"><span data-stu-id="517b6-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="517b6-226">Nodokli pievieno neto summai pirms PVN aprēķina.</span><span class="sxs-lookup"><span data-stu-id="517b6-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="517b6-227">Jūs iegādājaties 8 lampas, kas maksā 25,00/gabalā.</span><span class="sxs-lookup"><span data-stu-id="517b6-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="517b6-228">Rēķina neto summa ir 200,00.</span><span class="sxs-lookup"><span data-stu-id="517b6-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="517b6-229">Rēķina bruto summa ir 200,00 + (8 x 5,00) = 240,00.</span><span class="sxs-lookup"><span data-stu-id="517b6-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="517b6-230">Nodoklis tiek aprēķināts šādi: Kopējais pārdošanas nodoklis = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Kopējais nodoklis = 5,00 x 8 = 40,00 Rēķina kopsumma = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="517b6-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="517b6-231">Papildinformāciju skatiet tēmās [PVN kodu visas summas un intervāla aprēķināšanas opcijas](whole-amount-interval-options-sales-tax-codes.md) un [PVN aprēķina metodes laukā Izcelsme](sales-tax-calculation-methods-origin-field.md).</span><span class="sxs-lookup"><span data-stu-id="517b6-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>




