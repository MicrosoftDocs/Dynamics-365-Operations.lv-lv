---
title: PVN kodu visas summas un intervāla aprēķināšanas opcijas
description: Šajā raksta ir aprakstītas lauka Aprēķina metode opcijas, kas attiecas uz PVN kodiem, un izskaidrots kā tiek aprēķināts intervālu un visu summu PVN.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3e18eac934eb109e8f3f509b2bd78f76dd5f74d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980918"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="e12b7-103">PVN kodu visas summas un intervāla aprēķināšanas opcijas</span><span class="sxs-lookup"><span data-stu-id="e12b7-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e12b7-104">Šajā raksta ir aprakstītas lauka Aprēķina metode opcijas, kas attiecas uz PVN kodiem, un izskaidrots kā tiek aprēķināts intervālu un visu summu PVN.</span><span class="sxs-lookup"><span data-stu-id="e12b7-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="e12b7-105">Varat iestatīt PVN kodu tā, lai tas tiktu aprēķināts, pamatojoties uz visu summu vai intervāla summu.</span><span class="sxs-lookup"><span data-stu-id="e12b7-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="e12b7-106">Izmantojiet lauku Aprēķina metode lapas PVN kodi kopsavilkuma cilnē Aprēķins, lai atlasītu, kā aprēķināt PVN kodu.</span><span class="sxs-lookup"><span data-stu-id="e12b7-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="e12b7-107">Visa summa — nodokļa likme tiek lietota visai apliekamajai summai.</span><span class="sxs-lookup"><span data-stu-id="e12b7-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="e12b7-108">Intervāls — apliekamā summa tiek sadalīta daļās, katra no kurām atbilst diapazonam ar noteiktu PVN likmi.</span><span class="sxs-lookup"><span data-stu-id="e12b7-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="e12b7-109">Summas daļa, kas atbilst noteiktam intervālam, tiek aplikta ar nodokļiem saskaņā ar šī intervāla nodokļa likmi.</span><span class="sxs-lookup"><span data-stu-id="e12b7-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="e12b7-110">PVN likme ir summa no visiem nodokļu daudzumiem, kas tiek aprēķināti katram daudzuma intervālam.</span><span class="sxs-lookup"><span data-stu-id="e12b7-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="e12b7-111">Opcija Intervāls ir pieejama tikai tad, ja lapas Virsgrāmatas parametri apgabalā PVN ir atlasīta lauka Aprēķina metode vērtība Rinda.</span><span class="sxs-lookup"><span data-stu-id="e12b7-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="e12b7-112">Intervālus var iestatīt lapā PVN koda vērtības, ievadot minimālā un maksimālā ierobežojuma summu katrai nodokļa likmei.</span><span class="sxs-lookup"><span data-stu-id="e12b7-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="e12b7-113">Lai nodokļi tiktu aprēķināti visai apliekamajai summai neatkarīgi no atlasītās aprēķina metodes, intervāliem ir jāatbilst tālāk norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="e12b7-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="e12b7-114">Pirmā intervāla minimālā ierobežojuma vērtībai ir jābūt nulle.</span><span class="sxs-lookup"><span data-stu-id="e12b7-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="e12b7-115">Pēdējā intervāla maksimālā ierobežojuma vērtībai ir jābūt nulle, kas norāda bezgalību.</span><span class="sxs-lookup"><span data-stu-id="e12b7-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="e12b7-116">Intervāla maksimālā ierobežojuma vērtībai ir jābūt vienādai ar nākamā intervāla minimālā ierobežojuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="e12b7-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="e12b7-117">Ja summa ir vienāda ar iepriekšējā intervāla maksimālā ierobežojuma vērtību un nākamā intervāla minimālā ierobežojuma vērtību, summai tiek lietota pirmā intervāla PVN likme.</span><span class="sxs-lookup"><span data-stu-id="e12b7-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="e12b7-118">Ja summa neatbilst intervāliem, kas ir definēti ar maksimālā un minimālā ierobežojuma vērtībām, tiek lietota PVN likme nulle.</span><span class="sxs-lookup"><span data-stu-id="e12b7-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="e12b7-119">Piemērs: visas summas aprēķina metode</span><span class="sxs-lookup"><span data-stu-id="e12b7-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="e12b7-120">Lapā PVN koda vērtības tiek iestatītas PVN likmes tālāk norādītajos intervālos.</span><span class="sxs-lookup"><span data-stu-id="e12b7-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="e12b7-121">**Minimālā robeža**</span><span class="sxs-lookup"><span data-stu-id="e12b7-121">**Minimum limit**</span></span> | <span data-ttu-id="e12b7-122">**Maksimālā robeža**</span><span class="sxs-lookup"><span data-stu-id="e12b7-122">**Maximum limit**</span></span> | <span data-ttu-id="e12b7-123">**Nodokļa likme**</span><span class="sxs-lookup"><span data-stu-id="e12b7-123">**Tax rate**</span></span> |
| <span data-ttu-id="e12b7-124">0,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-124">0.00</span></span>              | <span data-ttu-id="e12b7-125">50,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-125">50.00</span></span>             | <span data-ttu-id="e12b7-126">30%</span><span class="sxs-lookup"><span data-stu-id="e12b7-126">30%</span></span>          |
| <span data-ttu-id="e12b7-127">50,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-127">50.00</span></span>             | <span data-ttu-id="e12b7-128">100,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-128">100.00</span></span>            | <span data-ttu-id="e12b7-129">20%</span><span class="sxs-lookup"><span data-stu-id="e12b7-129">20%</span></span>          |
| <span data-ttu-id="e12b7-130">100,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-130">100.00</span></span>            | <span data-ttu-id="e12b7-131">0,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-131">0.00</span></span>              | <span data-ttu-id="e12b7-132">10%</span><span class="sxs-lookup"><span data-stu-id="e12b7-132">10%</span></span>          |

<span data-ttu-id="e12b7-133">PVN tiek aprēķināts visai apliekamajai summai.</span><span class="sxs-lookup"><span data-stu-id="e12b7-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="e12b7-134">Apliekamā summa (cena)</span><span class="sxs-lookup"><span data-stu-id="e12b7-134">Taxable amount (price)</span></span> | <span data-ttu-id="e12b7-135">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="e12b7-135">Calculation</span></span>    | <span data-ttu-id="e12b7-136">PVN</span><span class="sxs-lookup"><span data-stu-id="e12b7-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="e12b7-137">35,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-137">35.00</span></span>                  | <span data-ttu-id="e12b7-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="e12b7-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="e12b7-139">10,50</span><span class="sxs-lookup"><span data-stu-id="e12b7-139">10.50</span></span>     |
| <span data-ttu-id="e12b7-140">50,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-140">50.00</span></span>                  | <span data-ttu-id="e12b7-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="e12b7-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="e12b7-142">15,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-142">15.00</span></span>     |
| <span data-ttu-id="e12b7-143">85,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-143">85.00</span></span>                  | <span data-ttu-id="e12b7-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="e12b7-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="e12b7-145">17,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-145">17.00</span></span>     |
| <span data-ttu-id="e12b7-146">305,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-146">305.00</span></span>                 | <span data-ttu-id="e12b7-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="e12b7-147">305.00 \* 0.10</span></span> | <span data-ttu-id="e12b7-148">30,50</span><span class="sxs-lookup"><span data-stu-id="e12b7-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="e12b7-149"> Piemērs: intervāla aprēķina metode</span><span class="sxs-lookup"><span data-stu-id="e12b7-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="e12b7-150">Lapā Vērtības tiek iestatītas PVN likmes tālāk norādītajos intervālos.</span><span class="sxs-lookup"><span data-stu-id="e12b7-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="e12b7-151">**Minimālā robeža**</span><span class="sxs-lookup"><span data-stu-id="e12b7-151">**Minimum limit**</span></span> | <span data-ttu-id="e12b7-152">**Maksimālā robeža**</span><span class="sxs-lookup"><span data-stu-id="e12b7-152">**Maximum limit**</span></span> | <span data-ttu-id="e12b7-153">**Nodokļa likme**</span><span class="sxs-lookup"><span data-stu-id="e12b7-153">**Tax rate**</span></span> |
| <span data-ttu-id="e12b7-154">0,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-154">0.00</span></span>              | <span data-ttu-id="e12b7-155">50,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-155">50.00</span></span>             | <span data-ttu-id="e12b7-156">30%</span><span class="sxs-lookup"><span data-stu-id="e12b7-156">30%</span></span>          |
| <span data-ttu-id="e12b7-157">50,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-157">50.00</span></span>             | <span data-ttu-id="e12b7-158">100,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-158">100.00</span></span>            | <span data-ttu-id="e12b7-159">20%</span><span class="sxs-lookup"><span data-stu-id="e12b7-159">20%</span></span>          |
| <span data-ttu-id="e12b7-160">100,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-160">100.00</span></span>            | <span data-ttu-id="e12b7-161">0,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-161">0.00</span></span>              | <span data-ttu-id="e12b7-162">10%</span><span class="sxs-lookup"><span data-stu-id="e12b7-162">10%</span></span>          |

<span data-ttu-id="e12b7-163">PVN likme ir summa no visiem nodokļu daudzumiem, kas tiek aprēķināti katram daudzuma intervālam.</span><span class="sxs-lookup"><span data-stu-id="e12b7-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="e12b7-164">Apliekamā summa (cena)</span><span class="sxs-lookup"><span data-stu-id="e12b7-164">Taxable amount (price)</span></span> | <span data-ttu-id="e12b7-165">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="e12b7-165">Calculation</span></span>                                                               | <span data-ttu-id="e12b7-166">PVN</span><span class="sxs-lookup"><span data-stu-id="e12b7-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e12b7-167">35,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-167">35.00</span></span>                  | <span data-ttu-id="e12b7-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="e12b7-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="e12b7-169">10,50</span><span class="sxs-lookup"><span data-stu-id="e12b7-169">10.50</span></span>     |
| <span data-ttu-id="e12b7-170">50,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-170">50.00</span></span>                  | <span data-ttu-id="e12b7-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="e12b7-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="e12b7-172">15,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-172">15.00</span></span>     |
| <span data-ttu-id="e12b7-173">85,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-173">85.00</span></span>                  | <span data-ttu-id="e12b7-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="e12b7-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="e12b7-175">22,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-175">22.00</span></span>     |
| <span data-ttu-id="e12b7-176">305,00</span><span class="sxs-lookup"><span data-stu-id="e12b7-176">305.00</span></span>                 | <span data-ttu-id="e12b7-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="e12b7-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="e12b7-178">45.50</span><span class="sxs-lookup"><span data-stu-id="e12b7-178">45.50</span></span>     |



<span data-ttu-id="e12b7-179">Papildinformāciju skatiet [Nodokļu likmes, kuru pamatā ir maržinālā bāze un aprēķināšanas metodes](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="e12b7-179">For more information, see [Sales tax rates based on the Marginal base and Calculation methods](marginal-base-field.md).</span></span>





