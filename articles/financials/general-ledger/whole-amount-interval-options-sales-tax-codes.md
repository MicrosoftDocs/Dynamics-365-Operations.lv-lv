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
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d16ea19a6d3cfea325281f301e0502bb051381d9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "344068"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="00d6e-103">PVN kodu visas summas un intervāla aprēķināšanas opcijas</span><span class="sxs-lookup"><span data-stu-id="00d6e-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="00d6e-104">Šajā raksta ir aprakstītas lauka Aprēķina metode opcijas, kas attiecas uz PVN kodiem, un izskaidrots kā tiek aprēķināts intervālu un visu summu PVN.</span><span class="sxs-lookup"><span data-stu-id="00d6e-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="00d6e-105">Varat iestatīt PVN kodu tā, lai tas tiktu aprēķināts, pamatojoties uz visu summu vai intervāla summu.</span><span class="sxs-lookup"><span data-stu-id="00d6e-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="00d6e-106">Izmantojiet lauku Aprēķina metode lapas PVN kodi kopsavilkuma cilnē Aprēķins, lai atlasītu, kā aprēķināt PVN kodu.</span><span class="sxs-lookup"><span data-stu-id="00d6e-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="00d6e-107">Visa summa — nodokļa likme tiek lietota visai apliekamajai summai.</span><span class="sxs-lookup"><span data-stu-id="00d6e-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="00d6e-108">Intervāls — apliekamā summa tiek sadalīta daļās, katra no kurām atbilst diapazonam ar noteiktu PVN likmi.</span><span class="sxs-lookup"><span data-stu-id="00d6e-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="00d6e-109">Summas daļa, kas atbilst noteiktam intervālam, tiek aplikta ar nodokļiem saskaņā ar šī intervāla nodokļa likmi.</span><span class="sxs-lookup"><span data-stu-id="00d6e-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="00d6e-110">PVN likme ir summa no visiem nodokļu daudzumiem, kas tiek aprēķināti katram daudzuma intervālam.</span><span class="sxs-lookup"><span data-stu-id="00d6e-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="00d6e-111">Opcija Intervāls ir pieejama tikai tad, ja lapas Virsgrāmatas parametri apgabalā PVN ir atlasīta lauka Aprēķina metode vērtība Rinda.</span><span class="sxs-lookup"><span data-stu-id="00d6e-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="00d6e-112">Intervālus var iestatīt lapā PVN koda vērtības, ievadot minimālā un maksimālā ierobežojuma summu katrai nodokļa likmei.</span><span class="sxs-lookup"><span data-stu-id="00d6e-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="00d6e-113">Lai nodokļi tiktu aprēķināti visai apliekamajai summai neatkarīgi no atlasītās aprēķina metodes, intervāliem ir jāatbilst tālāk norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="00d6e-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="00d6e-114">Pirmā intervāla minimālā ierobežojuma vērtībai ir jābūt nulle.</span><span class="sxs-lookup"><span data-stu-id="00d6e-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="00d6e-115">Pēdējā intervāla maksimālā ierobežojuma vērtībai ir jābūt nulle, kas norāda bezgalību.</span><span class="sxs-lookup"><span data-stu-id="00d6e-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="00d6e-116">Intervāla maksimālā ierobežojuma vērtībai ir jābūt vienādai ar nākamā intervāla minimālā ierobežojuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="00d6e-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="00d6e-117">Ja summa ir vienāda ar iepriekšējā intervāla maksimālā ierobežojuma vērtību un nākamā intervāla minimālā ierobežojuma vērtību, summai tiek lietota pirmā intervāla PVN likme.</span><span class="sxs-lookup"><span data-stu-id="00d6e-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="00d6e-118">Ja summa neatbilst intervāliem, kas ir definēti ar maksimālā un minimālā ierobežojuma vērtībām, tiek lietota PVN likme nulle.</span><span class="sxs-lookup"><span data-stu-id="00d6e-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="00d6e-119">Piemērs: visas summas aprēķina metode</span><span class="sxs-lookup"><span data-stu-id="00d6e-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="00d6e-120">Lapā PVN koda vērtības tiek iestatītas PVN likmes tālāk norādītajos intervālos.</span><span class="sxs-lookup"><span data-stu-id="00d6e-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="00d6e-121">**Minimālā robeža**</span><span class="sxs-lookup"><span data-stu-id="00d6e-121">**Minimum limit**</span></span> | <span data-ttu-id="00d6e-122">**Maksimālā robeža**</span><span class="sxs-lookup"><span data-stu-id="00d6e-122">**Maximum limit**</span></span> | <span data-ttu-id="00d6e-123">**Nodokļa likme**</span><span class="sxs-lookup"><span data-stu-id="00d6e-123">**Tax rate**</span></span> |
| <span data-ttu-id="00d6e-124">0,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-124">0.00</span></span>              | <span data-ttu-id="00d6e-125">50,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-125">50.00</span></span>             | <span data-ttu-id="00d6e-126">30%</span><span class="sxs-lookup"><span data-stu-id="00d6e-126">30%</span></span>          |
| <span data-ttu-id="00d6e-127">50,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-127">50.00</span></span>             | <span data-ttu-id="00d6e-128">100,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-128">100.00</span></span>            | <span data-ttu-id="00d6e-129">20%</span><span class="sxs-lookup"><span data-stu-id="00d6e-129">20%</span></span>          |
| <span data-ttu-id="00d6e-130">100,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-130">100.00</span></span>            | <span data-ttu-id="00d6e-131">0,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-131">0.00</span></span>              | <span data-ttu-id="00d6e-132">10%</span><span class="sxs-lookup"><span data-stu-id="00d6e-132">10%</span></span>          |

<span data-ttu-id="00d6e-133">PVN tiek aprēķināts visai apliekamajai summai.</span><span class="sxs-lookup"><span data-stu-id="00d6e-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="00d6e-134">Apliekamā summa (cena)</span><span class="sxs-lookup"><span data-stu-id="00d6e-134">Taxable amount (price)</span></span> | <span data-ttu-id="00d6e-135">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="00d6e-135">Calculation</span></span>    | <span data-ttu-id="00d6e-136">PVN</span><span class="sxs-lookup"><span data-stu-id="00d6e-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="00d6e-137">35,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-137">35.00</span></span>                  | <span data-ttu-id="00d6e-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="00d6e-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="00d6e-139">10,50</span><span class="sxs-lookup"><span data-stu-id="00d6e-139">10.50</span></span>     |
| <span data-ttu-id="00d6e-140">50,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-140">50.00</span></span>                  | <span data-ttu-id="00d6e-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="00d6e-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="00d6e-142">15,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-142">15.00</span></span>     |
| <span data-ttu-id="00d6e-143">85,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-143">85.00</span></span>                  | <span data-ttu-id="00d6e-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="00d6e-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="00d6e-145">17,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-145">17.00</span></span>     |
| <span data-ttu-id="00d6e-146">305,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-146">305.00</span></span>                 | <span data-ttu-id="00d6e-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="00d6e-147">305.00 \* 0.10</span></span> | <span data-ttu-id="00d6e-148">30,50</span><span class="sxs-lookup"><span data-stu-id="00d6e-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="00d6e-149"> Piemērs: intervāla aprēķina metode</span><span class="sxs-lookup"><span data-stu-id="00d6e-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="00d6e-150">Lapā Vērtības tiek iestatītas PVN likmes tālāk norādītajos intervālos.</span><span class="sxs-lookup"><span data-stu-id="00d6e-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="00d6e-151">**Minimālā robeža**</span><span class="sxs-lookup"><span data-stu-id="00d6e-151">**Minimum limit**</span></span> | <span data-ttu-id="00d6e-152">**Maksimālā robeža**</span><span class="sxs-lookup"><span data-stu-id="00d6e-152">**Maximum limit**</span></span> | <span data-ttu-id="00d6e-153">**Nodokļa likme**</span><span class="sxs-lookup"><span data-stu-id="00d6e-153">**Tax rate**</span></span> |
| <span data-ttu-id="00d6e-154">0,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-154">0.00</span></span>              | <span data-ttu-id="00d6e-155">50,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-155">50.00</span></span>             | <span data-ttu-id="00d6e-156">30%</span><span class="sxs-lookup"><span data-stu-id="00d6e-156">30%</span></span>          |
| <span data-ttu-id="00d6e-157">50,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-157">50.00</span></span>             | <span data-ttu-id="00d6e-158">100,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-158">100.00</span></span>            | <span data-ttu-id="00d6e-159">20%</span><span class="sxs-lookup"><span data-stu-id="00d6e-159">20%</span></span>          |
| <span data-ttu-id="00d6e-160">100,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-160">100.00</span></span>            | <span data-ttu-id="00d6e-161">0,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-161">0.00</span></span>              | <span data-ttu-id="00d6e-162">10%</span><span class="sxs-lookup"><span data-stu-id="00d6e-162">10%</span></span>          |

<span data-ttu-id="00d6e-163">PVN likme ir summa no visiem nodokļu daudzumiem, kas tiek aprēķināti katram daudzuma intervālam.</span><span class="sxs-lookup"><span data-stu-id="00d6e-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="00d6e-164">Apliekamā summa (cena)</span><span class="sxs-lookup"><span data-stu-id="00d6e-164">Taxable amount (price)</span></span> | <span data-ttu-id="00d6e-165">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="00d6e-165">Calculation</span></span>                                                               | <span data-ttu-id="00d6e-166">PVN</span><span class="sxs-lookup"><span data-stu-id="00d6e-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="00d6e-167">35,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-167">35.00</span></span>                  | <span data-ttu-id="00d6e-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="00d6e-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="00d6e-169">10,50</span><span class="sxs-lookup"><span data-stu-id="00d6e-169">10.50</span></span>     |
| <span data-ttu-id="00d6e-170">50,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-170">50.00</span></span>                  | <span data-ttu-id="00d6e-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="00d6e-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="00d6e-172">15,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-172">15.00</span></span>     |
| <span data-ttu-id="00d6e-173">85,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-173">85.00</span></span>                  | <span data-ttu-id="00d6e-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="00d6e-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="00d6e-175">22,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-175">22.00</span></span>     |
| <span data-ttu-id="00d6e-176">305,00</span><span class="sxs-lookup"><span data-stu-id="00d6e-176">305.00</span></span>                 | <span data-ttu-id="00d6e-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="00d6e-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="00d6e-178">45,50</span><span class="sxs-lookup"><span data-stu-id="00d6e-178">45.50</span></span>     |



<span data-ttu-id="00d6e-179">Papildinformāciju skatiet tēmā [PVN likmes noteikšana atkarībā no laukiem Aprēķina pamatā un Aprēķina metode](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="00d6e-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>





