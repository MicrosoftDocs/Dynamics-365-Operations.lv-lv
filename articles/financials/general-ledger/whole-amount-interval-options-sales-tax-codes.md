---
title: "PVN kodu visas summas un intervāla aprēķināšanas opcijas"
description: "Šajā raksta ir aprakstītas lauka Aprēķina metode opcijas, kas attiecas uz PVN kodiem, un izskaidrots kā tiek aprēķināts intervālu un visu summu PVN."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6ac0e2abcb5dce58ad16737a0ef689ceaeb50c44
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="4f471-103">PVN kodu visas summas un intervāla aprēķināšanas opcijas</span><span class="sxs-lookup"><span data-stu-id="4f471-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]



<span data-ttu-id="4f471-104">Šajā raksta ir aprakstītas lauka Aprēķina metode opcijas, kas attiecas uz PVN kodiem, un izskaidrots kā tiek aprēķināts intervālu un visu summu PVN.</span><span class="sxs-lookup"><span data-stu-id="4f471-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="4f471-105">Varat iestatīt PVN kodu tā, lai tas tiktu aprēķināts, pamatojoties uz visu summu vai intervāla summu.</span><span class="sxs-lookup"><span data-stu-id="4f471-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="4f471-106">Izmantojiet lauku Aprēķina metode lapas PVN kodi kopsavilkuma cilnē Aprēķins, lai atlasītu, kā aprēķināt PVN kodu.</span><span class="sxs-lookup"><span data-stu-id="4f471-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
-   <span data-ttu-id="4f471-107">Visa summa — nodokļa likme tiek lietota visai apliekamajai summai.</span><span class="sxs-lookup"><span data-stu-id="4f471-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
-   <span data-ttu-id="4f471-108">Intervāls — apliekamā summa tiek sadalīta daļās, katra no kurām atbilst diapazonam ar noteiktu PVN likmi.</span><span class="sxs-lookup"><span data-stu-id="4f471-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="4f471-109">Summas daļa, kas atbilst noteiktam intervālam, tiek aplikta ar nodokļiem saskaņā ar šī intervāla nodokļa likmi.</span><span class="sxs-lookup"><span data-stu-id="4f471-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="4f471-110">PVN likme ir summa no visiem nodokļu daudzumiem, kas tiek aprēķināti katram daudzuma intervālam.</span><span class="sxs-lookup"><span data-stu-id="4f471-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
> [!NOTE]                                                                                                                              
> <span data-ttu-id="4f471-111">Opcija Intervāls ir pieejama tikai tad, ja lapas Virsgrāmatas parametri apgabalā PVN ir atlasīta lauka Aprēķina metode vērtība Rinda.</span><span class="sxs-lookup"><span data-stu-id="4f471-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="4f471-112">Intervālus var iestatīt lapā PVN koda vērtības, ievadot minimālā un maksimālā ierobežojuma summu katrai nodokļa likmei.</span><span class="sxs-lookup"><span data-stu-id="4f471-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="4f471-113">Lai nodokļi tiktu aprēķināti visai apliekamajai summai neatkarīgi no atlasītās aprēķina metodes, intervāliem ir jāatbilst tālāk norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="4f471-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="4f471-114">Pirmā intervāla minimālā ierobežojuma vērtībai ir jābūt nulle.</span><span class="sxs-lookup"><span data-stu-id="4f471-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="4f471-115">Pēdējā intervāla maksimālā ierobežojuma vērtībai ir jābūt nulle, kas norāda bezgalību.</span><span class="sxs-lookup"><span data-stu-id="4f471-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="4f471-116">Intervāla maksimālā ierobežojuma vērtībai ir jābūt vienādai ar nākamā intervāla minimālā ierobežojuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="4f471-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="4f471-117">Ja summa ir vienāda ar iepriekšējā intervāla maksimālā ierobežojuma vērtību un nākamā intervāla minimālā ierobežojuma vērtību, summai tiek lietota pirmā intervāla PVN likme.</span><span class="sxs-lookup"><span data-stu-id="4f471-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="4f471-118">Ja summa neatbilst intervāliem, kas ir definēti ar maksimālā un minimālā ierobežojuma vērtībām, tiek lietota PVN likme nulle.</span><span class="sxs-lookup"><span data-stu-id="4f471-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="4f471-119">Piemērs: visas summas aprēķina metode</span><span class="sxs-lookup"><span data-stu-id="4f471-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="4f471-120">Lapā PVN koda vērtības tiek iestatītas PVN likmes tālāk norādītajos intervālos.</span><span class="sxs-lookup"><span data-stu-id="4f471-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>
|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="4f471-121">**Minimālā robeža**</span><span class="sxs-lookup"><span data-stu-id="4f471-121">**Minimum limit**</span></span> | <span data-ttu-id="4f471-122">**Maksimālā robeža**</span><span class="sxs-lookup"><span data-stu-id="4f471-122">**Maximum limit**</span></span> | <span data-ttu-id="4f471-123">**Nodokļa likme**</span><span class="sxs-lookup"><span data-stu-id="4f471-123">**Tax rate**</span></span> |
| <span data-ttu-id="4f471-124">0,00</span><span class="sxs-lookup"><span data-stu-id="4f471-124">0.00</span></span>              | <span data-ttu-id="4f471-125">50,00</span><span class="sxs-lookup"><span data-stu-id="4f471-125">50.00</span></span>             | <span data-ttu-id="4f471-126">30%</span><span class="sxs-lookup"><span data-stu-id="4f471-126">30%</span></span>          |
| <span data-ttu-id="4f471-127">50,00</span><span class="sxs-lookup"><span data-stu-id="4f471-127">50.00</span></span>             | <span data-ttu-id="4f471-128">100,00</span><span class="sxs-lookup"><span data-stu-id="4f471-128">100.00</span></span>            | <span data-ttu-id="4f471-129">20%</span><span class="sxs-lookup"><span data-stu-id="4f471-129">20%</span></span>          |
| <span data-ttu-id="4f471-130">100,00</span><span class="sxs-lookup"><span data-stu-id="4f471-130">100.00</span></span>            | <span data-ttu-id="4f471-131">0,00</span><span class="sxs-lookup"><span data-stu-id="4f471-131">0.00</span></span>              | <span data-ttu-id="4f471-132">10%</span><span class="sxs-lookup"><span data-stu-id="4f471-132">10%</span></span>          |

<span data-ttu-id="4f471-133">PVN tiek aprēķināts visai apliekamajai summai.</span><span class="sxs-lookup"><span data-stu-id="4f471-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="4f471-134">Apliekamā summa (cena)</span><span class="sxs-lookup"><span data-stu-id="4f471-134">Taxable amount (price)</span></span> | <span data-ttu-id="4f471-135">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="4f471-135">Calculation</span></span>    | <span data-ttu-id="4f471-136">PVN</span><span class="sxs-lookup"><span data-stu-id="4f471-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="4f471-137">35,00</span><span class="sxs-lookup"><span data-stu-id="4f471-137">35.00</span></span>                  | <span data-ttu-id="4f471-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="4f471-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="4f471-139">10,50</span><span class="sxs-lookup"><span data-stu-id="4f471-139">10.50</span></span>     |
| <span data-ttu-id="4f471-140">50,00</span><span class="sxs-lookup"><span data-stu-id="4f471-140">50.00</span></span>                  | <span data-ttu-id="4f471-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="4f471-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="4f471-142">15,00</span><span class="sxs-lookup"><span data-stu-id="4f471-142">15.00</span></span>     |
| <span data-ttu-id="4f471-143">85,00</span><span class="sxs-lookup"><span data-stu-id="4f471-143">85.00</span></span>                  | <span data-ttu-id="4f471-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="4f471-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="4f471-145">17,00</span><span class="sxs-lookup"><span data-stu-id="4f471-145">17.00</span></span>     |
| <span data-ttu-id="4f471-146">305,00</span><span class="sxs-lookup"><span data-stu-id="4f471-146">305.00</span></span>                 | <span data-ttu-id="4f471-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="4f471-147">305.00 \* 0.10</span></span> | <span data-ttu-id="4f471-148">30,50</span><span class="sxs-lookup"><span data-stu-id="4f471-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="4f471-149"> Piemērs: intervāla aprēķina metode</span><span class="sxs-lookup"><span data-stu-id="4f471-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="4f471-150">Lapā Vērtības tiek iestatītas PVN likmes tālāk norādītajos intervālos.</span><span class="sxs-lookup"><span data-stu-id="4f471-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="4f471-151">**Minimālā robeža**</span><span class="sxs-lookup"><span data-stu-id="4f471-151">**Minimum limit**</span></span> | <span data-ttu-id="4f471-152">**Maksimālā robeža**</span><span class="sxs-lookup"><span data-stu-id="4f471-152">**Maximum limit**</span></span> | <span data-ttu-id="4f471-153">**Nodokļa likme**</span><span class="sxs-lookup"><span data-stu-id="4f471-153">**Tax rate**</span></span> |
| <span data-ttu-id="4f471-154">0,00</span><span class="sxs-lookup"><span data-stu-id="4f471-154">0.00</span></span>              | <span data-ttu-id="4f471-155">50,00</span><span class="sxs-lookup"><span data-stu-id="4f471-155">50.00</span></span>             | <span data-ttu-id="4f471-156">30%</span><span class="sxs-lookup"><span data-stu-id="4f471-156">30%</span></span>          |
| <span data-ttu-id="4f471-157">50,00</span><span class="sxs-lookup"><span data-stu-id="4f471-157">50.00</span></span>             | <span data-ttu-id="4f471-158">100,00</span><span class="sxs-lookup"><span data-stu-id="4f471-158">100.00</span></span>            | <span data-ttu-id="4f471-159">20%</span><span class="sxs-lookup"><span data-stu-id="4f471-159">20%</span></span>          |
| <span data-ttu-id="4f471-160">100,00</span><span class="sxs-lookup"><span data-stu-id="4f471-160">100.00</span></span>            | <span data-ttu-id="4f471-161">0,00</span><span class="sxs-lookup"><span data-stu-id="4f471-161">0.00</span></span>              | <span data-ttu-id="4f471-162">10%</span><span class="sxs-lookup"><span data-stu-id="4f471-162">10%</span></span>          |

<span data-ttu-id="4f471-163">PVN likme ir summa no visiem nodokļu daudzumiem, kas tiek aprēķināti katram daudzuma intervālam.</span><span class="sxs-lookup"><span data-stu-id="4f471-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="4f471-164">Apliekamā summa (cena)</span><span class="sxs-lookup"><span data-stu-id="4f471-164">Taxable amount (price)</span></span> | <span data-ttu-id="4f471-165">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="4f471-165">Calculation</span></span>                                                               | <span data-ttu-id="4f471-166">PVN</span><span class="sxs-lookup"><span data-stu-id="4f471-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4f471-167">35,00</span><span class="sxs-lookup"><span data-stu-id="4f471-167">35.00</span></span>                  | <span data-ttu-id="4f471-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="4f471-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="4f471-169">10,50</span><span class="sxs-lookup"><span data-stu-id="4f471-169">10.50</span></span>     |
| <span data-ttu-id="4f471-170">50,00</span><span class="sxs-lookup"><span data-stu-id="4f471-170">50.00</span></span>                  | <span data-ttu-id="4f471-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="4f471-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="4f471-172">15,00</span><span class="sxs-lookup"><span data-stu-id="4f471-172">15.00</span></span>     |
| <span data-ttu-id="4f471-173">85,00</span><span class="sxs-lookup"><span data-stu-id="4f471-173">85.00</span></span>                  | <span data-ttu-id="4f471-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="4f471-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="4f471-175">22,00</span><span class="sxs-lookup"><span data-stu-id="4f471-175">22.00</span></span>     |
| <span data-ttu-id="4f471-176">305,00</span><span class="sxs-lookup"><span data-stu-id="4f471-176">305.00</span></span>                 | <span data-ttu-id="4f471-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="4f471-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="4f471-178">45,50</span><span class="sxs-lookup"><span data-stu-id="4f471-178">45.50</span></span>     |

 

<span data-ttu-id="4f471-179">Papildinformāciju skatiet tēmā [PVN likmes noteikšana atkarībā no laukiem Aprēķina pamatā un Aprēķina metode](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="4f471-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>






