---
title: "Manuāls nolietojuma aprēķins"
description: "Šajā rakstā ir sniegts pārskats par manuālo nolietojuma metodi."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e43b9397dd4e362eff9d78f302732e6bcc53d1db
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="manual-depreciation"></a><span data-ttu-id="97c6f-103">Manuāls nolietojuma aprēķins</span><span class="sxs-lookup"><span data-stu-id="97c6f-103">Manual depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="97c6f-104">Šajā rakstā ir sniegts pārskats par manuālo nolietojuma metodi.</span><span class="sxs-lookup"><span data-stu-id="97c6f-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="97c6f-105">Kad iestatāt pamatlīdzekļa nolietojuma tabulu un atlasāt vērtību **Manuāls** laukā **Metode**, lapā **Nolietojuma tabulas**, šai nolietošanas tabulai piešķirto pamatlīdzekļu nolietojums tiek noteikts pēc procentuālā daudzuma, ko ievadāt katram kalendārā gada intervālam.</span><span class="sxs-lookup"><span data-stu-id="97c6f-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="97c6f-106">Intervāli, kuriem iestatāt procentuālo daudzumu, tiek grāmatoti atbilstoši vērībai, kuru atlasāt laukā **Perioda biežums**, kopsavilkuma cilnē **Vispārīgi**, kura atrodas lapā **Nolietojuma tabulas**.</span><span class="sxs-lookup"><span data-stu-id="97c6f-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="97c6f-107">Varat atlasīt šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="97c6f-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="97c6f-108">Reizi gadā</span><span class="sxs-lookup"><span data-stu-id="97c6f-108">Yearly</span></span>
-   <span data-ttu-id="97c6f-109">Reizi mēnesī</span><span class="sxs-lookup"><span data-stu-id="97c6f-109">Monthly</span></span>
-   <span data-ttu-id="97c6f-110">Reizi ceturksnī</span><span class="sxs-lookup"><span data-stu-id="97c6f-110">Quarterly</span></span>
-   <span data-ttu-id="97c6f-111">Reizi pusgadā</span><span class="sxs-lookup"><span data-stu-id="97c6f-111">Half-Yearly</span></span>
-   <span data-ttu-id="97c6f-112">Katru dienu</span><span class="sxs-lookup"><span data-stu-id="97c6f-112">Daily</span></span>

<span data-ttu-id="97c6f-113">Pēc perioda biežuma atlasīšanas noklikšķiniet uz **Manuālie grafiki** un iestatiet procentuālo daudzumu katram grāmatošanas intervālam.</span><span class="sxs-lookup"><span data-stu-id="97c6f-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="97c6f-114">Manuālie grafiki un grāmatošanas intervāli kopā nosaka nolietojuma summu, kā parādīts šajā rakstā tālāk iekļautajos piemēros.</span><span class="sxs-lookup"><span data-stu-id="97c6f-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="97c6f-115">Manuālais nolietojums vienmēr tiek aprēķināts kā procenti no iegādes cenas.</span><span class="sxs-lookup"><span data-stu-id="97c6f-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="97c6f-116">Attiecībā uz manuālo nolietojumu jūsu nolietojuma intervālos ievadītajiem procentuālajiem daudzumiem kopā nav jāveido 100 procenti.</span><span class="sxs-lookup"><span data-stu-id="97c6f-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="97c6f-117">Manuāls nolietojums ir elastīga nolietojuma metode, ko bieži lieto, lai lapā **Grāmatas** definētu specifisku nolietojuma tabulu, piemēram, neregulāru nolietojumu specifiskiem mērķiem (piemēram, nodokļiem).</span><span class="sxs-lookup"><span data-stu-id="97c6f-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="97c6f-118">Piemēri</span><span class="sxs-lookup"><span data-stu-id="97c6f-118">Examples</span></span>
<span data-ttu-id="97c6f-119">Iegādes cena: 11 000,00 Plānotā lūžņu vērtība: 1000,00 Nākamajā tabulā ir parādīti intervāli un procentuālie daudzumi, ko iestatāt lapā **Pamatlīdzekļu nolietojuma aprēķina tabulas**.</span><span class="sxs-lookup"><span data-stu-id="97c6f-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="97c6f-120">Intervāla numurs</span><span class="sxs-lookup"><span data-stu-id="97c6f-120">Interval number</span></span> | <span data-ttu-id="97c6f-121">Procenti</span><span class="sxs-lookup"><span data-stu-id="97c6f-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="97c6f-122">1</span><span class="sxs-lookup"><span data-stu-id="97c6f-122">1</span></span>               | <span data-ttu-id="97c6f-123">10,00</span><span class="sxs-lookup"><span data-stu-id="97c6f-123">10.00</span></span>      |
| <span data-ttu-id="97c6f-124">2</span><span class="sxs-lookup"><span data-stu-id="97c6f-124">2</span></span>               | <span data-ttu-id="97c6f-125">50,00</span><span class="sxs-lookup"><span data-stu-id="97c6f-125">50.00</span></span>      |
| <span data-ttu-id="97c6f-126">3</span><span class="sxs-lookup"><span data-stu-id="97c6f-126">3</span></span>               | <span data-ttu-id="97c6f-127">8,00</span><span class="sxs-lookup"><span data-stu-id="97c6f-127">8.00</span></span>       |

<span data-ttu-id="97c6f-128">Nākamajā tabulā ir parādīts, ka nolietojums tiek aprēķināts katram intervālam.</span><span class="sxs-lookup"><span data-stu-id="97c6f-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="97c6f-129">Intervāla numurs</span><span class="sxs-lookup"><span data-stu-id="97c6f-129">Interval number</span></span> | <span data-ttu-id="97c6f-130">Ikgadējā nolietojuma summas aprēķins</span><span class="sxs-lookup"><span data-stu-id="97c6f-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="97c6f-131">Atlikusī vērtība intervāla beigās</span><span class="sxs-lookup"><span data-stu-id="97c6f-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="97c6f-132">1</span><span class="sxs-lookup"><span data-stu-id="97c6f-132">1</span></span>                | <span data-ttu-id="97c6f-133">(11 000 – 1000)× 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="97c6f-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="97c6f-134">10 000 (11 000 – 1000)</span><span class="sxs-lookup"><span data-stu-id="97c6f-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="97c6f-135">2</span><span class="sxs-lookup"><span data-stu-id="97c6f-135">2</span></span>                | <span data-ttu-id="97c6f-136">(11 000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="97c6f-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="97c6f-137">5000 (10 000 – 5000)</span><span class="sxs-lookup"><span data-stu-id="97c6f-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="97c6f-138">3</span><span class="sxs-lookup"><span data-stu-id="97c6f-138">3</span></span>                | <span data-ttu-id="97c6f-139">(11 000 – 1000) × 8% = 800</span><span class="sxs-lookup"><span data-stu-id="97c6f-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="97c6f-140">4200 (5000 – 800)</span><span class="sxs-lookup"><span data-stu-id="97c6f-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="97c6f-141">Ja laukā**Perioda biežums** atlasāt vērtību **Reizi mēnesī**, jūs iestatāt 12 manuālus grafika intervālus.</span><span class="sxs-lookup"><span data-stu-id="97c6f-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="97c6f-142">Nākamajā tabulā ir parādītas nolietojuma summas pirmajiem diviem intervāliem.</span><span class="sxs-lookup"><span data-stu-id="97c6f-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="97c6f-143">Intervāls</span><span class="sxs-lookup"><span data-stu-id="97c6f-143">Interval</span></span> | <span data-ttu-id="97c6f-144">Nolietojuma summa</span><span class="sxs-lookup"><span data-stu-id="97c6f-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="97c6f-145">Janvāris</span><span class="sxs-lookup"><span data-stu-id="97c6f-145">January</span></span>  | <span data-ttu-id="97c6f-146">(11 000 – 1000)× 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="97c6f-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="97c6f-147">Februāris</span><span class="sxs-lookup"><span data-stu-id="97c6f-147">February</span></span> | <span data-ttu-id="97c6f-148">(11 000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="97c6f-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="97c6f-149">Ja atlasāt **lauka **Perioda biežums**** vērtību **Reizi pusgadā**, tiek iestatīti divi manuālā grafika intervāli.</span><span class="sxs-lookup"><span data-stu-id="97c6f-149">If you select **Half-Yearly** in the ****Period frequency** field**, you set up two manual schedule intervals.</span></span> <span data-ttu-id="97c6f-150">Nākamajā tabulā ir parādītas nolietojuma summas šiem diviem intervāliem.</span><span class="sxs-lookup"><span data-stu-id="97c6f-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="97c6f-151">Intervāls</span><span class="sxs-lookup"><span data-stu-id="97c6f-151">Interval</span></span>    | <span data-ttu-id="97c6f-152">Nolietojuma summa</span><span class="sxs-lookup"><span data-stu-id="97c6f-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="97c6f-153">30. jūnijs</span><span class="sxs-lookup"><span data-stu-id="97c6f-153">June 30</span></span>     | <span data-ttu-id="97c6f-154">(11 000 – 1000)× 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="97c6f-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="97c6f-155">31. decembris</span><span class="sxs-lookup"><span data-stu-id="97c6f-155">December 31</span></span> | <span data-ttu-id="97c6f-156">(11 000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="97c6f-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="97c6f-157">Intervālu procentuālo vērtību kopsummai nav jābūt 100.</span><span class="sxs-lookup"><span data-stu-id="97c6f-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="97c6f-158">Taču, ja lapā **Pamatlīdzekļu nolietojuma aprēķina tabula** esošā lauka**Uzkrātie procenti** vērtība nav **100**, tiek parādīts attiecīgs ziņojums.</span><span class="sxs-lookup"><span data-stu-id="97c6f-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>




