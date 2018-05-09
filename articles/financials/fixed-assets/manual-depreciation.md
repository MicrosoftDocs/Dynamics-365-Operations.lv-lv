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
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0bef7a0b74b4dc671cc926ed247268c9b1f1d755
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="manual-depreciation"></a><span data-ttu-id="92178-103">Manuāls nolietojuma aprēķins</span><span class="sxs-lookup"><span data-stu-id="92178-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92178-104">Šajā rakstā ir sniegts pārskats par manuālo nolietojuma metodi.</span><span class="sxs-lookup"><span data-stu-id="92178-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="92178-105">Kad iestatāt pamatlīdzekļa nolietojuma tabulu un atlasāt vērtību **Manuāls** laukā **Metode**, lapā **Nolietojuma tabulas**, šai nolietošanas tabulai piešķirto pamatlīdzekļu nolietojums tiek noteikts pēc procentuālā daudzuma, ko ievadāt katram kalendārā gada intervālam.</span><span class="sxs-lookup"><span data-stu-id="92178-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="92178-106">Intervāli, kuriem iestatāt procentuālo daudzumu, tiek grāmatoti atbilstoši vērībai, kuru atlasāt laukā **Perioda biežums**, kopsavilkuma cilnē **Vispārīgi**, kura atrodas lapā **Nolietojuma tabulas**.</span><span class="sxs-lookup"><span data-stu-id="92178-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="92178-107">Varat atlasīt šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="92178-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="92178-108">Reizi gadā</span><span class="sxs-lookup"><span data-stu-id="92178-108">Yearly</span></span>
-   <span data-ttu-id="92178-109">Reizi mēnesī</span><span class="sxs-lookup"><span data-stu-id="92178-109">Monthly</span></span>
-   <span data-ttu-id="92178-110">Reizi ceturksnī</span><span class="sxs-lookup"><span data-stu-id="92178-110">Quarterly</span></span>
-   <span data-ttu-id="92178-111">Reizi pusgadā</span><span class="sxs-lookup"><span data-stu-id="92178-111">Half-Yearly</span></span>
-   <span data-ttu-id="92178-112">Katru dienu</span><span class="sxs-lookup"><span data-stu-id="92178-112">Daily</span></span>

<span data-ttu-id="92178-113">Pēc perioda biežuma atlasīšanas noklikšķiniet uz **Manuālie grafiki** un iestatiet procentuālo daudzumu katram grāmatošanas intervālam.</span><span class="sxs-lookup"><span data-stu-id="92178-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="92178-114">Manuālie grafiki un grāmatošanas intervāli kopā nosaka nolietojuma summu, kā parādīts šajā rakstā tālāk iekļautajos piemēros.</span><span class="sxs-lookup"><span data-stu-id="92178-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="92178-115">Manuālais nolietojums vienmēr tiek aprēķināts kā procenti no iegādes cenas.</span><span class="sxs-lookup"><span data-stu-id="92178-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="92178-116">Attiecībā uz manuālo nolietojumu jūsu nolietojuma intervālos ievadītajiem procentuālajiem daudzumiem kopā nav jāveido 100 procenti.</span><span class="sxs-lookup"><span data-stu-id="92178-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="92178-117">Manuāls nolietojums ir elastīga nolietojuma metode, ko bieži lieto, lai lapā **Grāmatas** definētu specifisku nolietojuma tabulu, piemēram, neregulāru nolietojumu specifiskiem mērķiem (piemēram, nodokļiem).</span><span class="sxs-lookup"><span data-stu-id="92178-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="92178-118">Piemēri</span><span class="sxs-lookup"><span data-stu-id="92178-118">Examples</span></span>
<span data-ttu-id="92178-119">Iegādes cena: 11 000,00 Plānotā lūžņu vērtība: 1000,00 Nākamajā tabulā ir parādīti intervāli un procentuālie daudzumi, ko iestatāt lapā **Pamatlīdzekļu nolietojuma aprēķina tabulas**.</span><span class="sxs-lookup"><span data-stu-id="92178-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="92178-120">Intervāla numurs</span><span class="sxs-lookup"><span data-stu-id="92178-120">Interval number</span></span> | <span data-ttu-id="92178-121">Procenti</span><span class="sxs-lookup"><span data-stu-id="92178-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="92178-122">1</span><span class="sxs-lookup"><span data-stu-id="92178-122">1</span></span>               | <span data-ttu-id="92178-123">10,00</span><span class="sxs-lookup"><span data-stu-id="92178-123">10.00</span></span>      |
| <span data-ttu-id="92178-124">2</span><span class="sxs-lookup"><span data-stu-id="92178-124">2</span></span>               | <span data-ttu-id="92178-125">50,00</span><span class="sxs-lookup"><span data-stu-id="92178-125">50.00</span></span>      |
| <span data-ttu-id="92178-126">3</span><span class="sxs-lookup"><span data-stu-id="92178-126">3</span></span>               | <span data-ttu-id="92178-127">8,00</span><span class="sxs-lookup"><span data-stu-id="92178-127">8.00</span></span>       |

<span data-ttu-id="92178-128">Nākamajā tabulā ir parādīts, ka nolietojums tiek aprēķināts katram intervālam.</span><span class="sxs-lookup"><span data-stu-id="92178-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="92178-129">Intervāla numurs</span><span class="sxs-lookup"><span data-stu-id="92178-129">Interval number</span></span> | <span data-ttu-id="92178-130">Ikgadējā nolietojuma summas aprēķins</span><span class="sxs-lookup"><span data-stu-id="92178-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="92178-131">Atlikusī vērtība intervāla beigās</span><span class="sxs-lookup"><span data-stu-id="92178-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="92178-132">1</span><span class="sxs-lookup"><span data-stu-id="92178-132">1</span></span>                | <span data-ttu-id="92178-133">(11 000 – 1000)× 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="92178-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="92178-134">10 000 (11 000 – 1000)</span><span class="sxs-lookup"><span data-stu-id="92178-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="92178-135">2</span><span class="sxs-lookup"><span data-stu-id="92178-135">2</span></span>                | <span data-ttu-id="92178-136">(11 000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="92178-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="92178-137">5000 (10 000 – 5000)</span><span class="sxs-lookup"><span data-stu-id="92178-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="92178-138">3</span><span class="sxs-lookup"><span data-stu-id="92178-138">3</span></span>                | <span data-ttu-id="92178-139">(11 000 – 1000) × 8% = 800</span><span class="sxs-lookup"><span data-stu-id="92178-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="92178-140">4200 (5000 – 800)</span><span class="sxs-lookup"><span data-stu-id="92178-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="92178-141">Ja laukā**Perioda biežums** atlasāt vērtību **Reizi mēnesī**, jūs iestatāt 12 manuālus grafika intervālus.</span><span class="sxs-lookup"><span data-stu-id="92178-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="92178-142">Nākamajā tabulā ir parādītas nolietojuma summas pirmajiem diviem intervāliem.</span><span class="sxs-lookup"><span data-stu-id="92178-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="92178-143">Intervāls</span><span class="sxs-lookup"><span data-stu-id="92178-143">Interval</span></span> | <span data-ttu-id="92178-144">Nolietojuma summa</span><span class="sxs-lookup"><span data-stu-id="92178-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="92178-145">Janvāris</span><span class="sxs-lookup"><span data-stu-id="92178-145">January</span></span>  | <span data-ttu-id="92178-146">(11 000 – 1000)× 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="92178-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="92178-147">Februāris</span><span class="sxs-lookup"><span data-stu-id="92178-147">February</span></span> | <span data-ttu-id="92178-148">(11 000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="92178-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="92178-149">Ja atlasāt lauka <strong>Perioda biežums</strong> vērtību *<strong><em>Reizi pusgadā</em>* </strong>, tiek iestatīti divi manuālā grafika intervāli.</span><span class="sxs-lookup"><span data-stu-id="92178-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="92178-150">Nākamajā tabulā ir parādītas nolietojuma summas šiem diviem intervāliem.</span><span class="sxs-lookup"><span data-stu-id="92178-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="92178-151">Intervāls</span><span class="sxs-lookup"><span data-stu-id="92178-151">Interval</span></span>    | <span data-ttu-id="92178-152">Nolietojuma summa</span><span class="sxs-lookup"><span data-stu-id="92178-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="92178-153">30. jūnijs</span><span class="sxs-lookup"><span data-stu-id="92178-153">June 30</span></span>     | <span data-ttu-id="92178-154">(11 000 – 1000)× 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="92178-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="92178-155">31. decembris</span><span class="sxs-lookup"><span data-stu-id="92178-155">December 31</span></span> | <span data-ttu-id="92178-156">(11 000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="92178-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="92178-157">Intervālu procentuālo vērtību kopsummai nav jābūt 100.</span><span class="sxs-lookup"><span data-stu-id="92178-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="92178-158">Taču, ja lapā **Pamatlīdzekļu nolietojuma aprēķina tabula** esošā lauka**Uzkrātie procenti** vērtība nav **100**, tiek parādīts attiecīgs ziņojums.</span><span class="sxs-lookup"><span data-stu-id="92178-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>




