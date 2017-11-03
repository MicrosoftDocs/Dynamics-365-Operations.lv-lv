---
title: "150 procentu degresīvā nolietojuma aprēķināšanas metode"
description: "Šajā rakstā ir sniegts pārskats par 150 procentu degresīvās nolietojuma aprēķināšanas metodi."
author: saraschi2
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
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b35b8ea652ccb06c45b8091cc7f57e849e1a5915
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="c9450-103">150 procentu degresīvā nolietojuma aprēķināšanas metode</span><span class="sxs-lookup"><span data-stu-id="c9450-103">150 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c9450-104">Šajā rakstā ir sniegts pārskats par 150 procentu degresīvās nolietojuma aprēķināšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="c9450-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="c9450-105">Ja iestatāt pamatlīdzekļa nolietojuma tabulu un atlasāt lauka **Metode** vērtību **150% atlikumu bilance** lapā **Nolietojuma tabulas**, pamatlīdzekļiem, kam ir piešķirta šī nolietojuma tabula, tiek izmantota vienāda nolietojuma procentu likme katrā nolietojuma periodā.</span><span class="sxs-lookup"><span data-stu-id="c9450-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="c9450-106">Šī procentu likme tiek aprēķināta, pamatojoties uz pamatlīdzekļa lietošanas ilgumu.</span><span class="sxs-lookup"><span data-stu-id="c9450-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="c9450-107">Piemēram, ja līdzekļa lietošanas ilgums ir pieci gadi, tiek aprēķināta procentu likme 30 procenti (150% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="c9450-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="c9450-108">Lai iestatītu 150 % atlikumu bilanci, jāatlasa arī opcijas laukā **Nolietojuma aprēķina gads**, kā arī laukā **Perioda biežums**, lapā **Nolietojuma tabulas**.</span><span class="sxs-lookup"><span data-stu-id="c9450-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="c9450-109">Laukā **Perioda biežums** pieejamās opcijas ir atkarīgas no vērtības, kas ir atlasīta laukā **Nolietojuma aprēķina gads**.</span><span class="sxs-lookup"><span data-stu-id="c9450-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="c9450-110">Nolietojuma aprēķina gada atlase</span><span class="sxs-lookup"><span data-stu-id="c9450-110">Selection of depreciation year</span></span>
<span data-ttu-id="c9450-111">Lapā **Nolietojuma tabulas** laukā **Nolietojuma aprēķina gads** varat atlasīt **Kalendārs** vai **Finanšu**.</span><span class="sxs-lookup"><span data-stu-id="c9450-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="c9450-112">Noklusējuma vērtība ir **Kalendārs**.</span><span class="sxs-lookup"><span data-stu-id="c9450-112">The default value is **Calendar**.</span></span> <span data-ttu-id="c9450-113">Jūsu atlase nosaka, kādas opcijas ir pieejamas laukā **Periodu biežums**.</span><span class="sxs-lookup"><span data-stu-id="c9450-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="c9450-114">Šis lauks nosaka nolietojuma uzkrājuma grāmatošanas datumus un summas kalendārā gada laikā.</span><span class="sxs-lookup"><span data-stu-id="c9450-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="c9450-115">Kalendārs</span><span class="sxs-lookup"><span data-stu-id="c9450-115">Calendar</span></span>

<span data-ttu-id="c9450-116">Laukā **Nolietojuma aprēķina gads** varat paturēt noklusējuma vērtību **Kalendārs**.</span><span class="sxs-lookup"><span data-stu-id="c9450-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="c9450-117">Opcija **Kalendārs** nolietojuma bāzi atjaunina katru gadu 1. janvārī.</span><span class="sxs-lookup"><span data-stu-id="c9450-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="c9450-118">Parasti nolietojuma bāze ir atlikusī vērtība mīnus lūžņu vērtība.</span><span class="sxs-lookup"><span data-stu-id="c9450-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="c9450-119">Tālāk šajā tēmā redzamajos piemēros nolietojuma bāze ir aprēķinu kolonnas pirmās izteiksmes skaitītājs.</span><span class="sxs-lookup"><span data-stu-id="c9450-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="c9450-120">Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Kalendārs**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="c9450-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="c9450-121">**Reizi gadā** grāmato summu 31. decembrī.</span><span class="sxs-lookup"><span data-stu-id="c9450-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="c9450-122">**Reizi mēnesī** grāmato mēneša summu katra kalendārā mēneša beigās.</span><span class="sxs-lookup"><span data-stu-id="c9450-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="c9450-123">**Reizi ceturksnī** grāmato ceturkšņa summu katra kalendārā ceturkšņa beigās (31. martā, 30. jūnijā, 30. septembrī un 31. decembrī).</span><span class="sxs-lookup"><span data-stu-id="c9450-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="c9450-124">**Reizi pusgadā** — grāmato pusgada summu katrā kalendārajā pusgadā (30. jūnijā un 31. decembrī).</span><span class="sxs-lookup"><span data-stu-id="c9450-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="c9450-125">**Reizi dienā** — grāmato nolietojuma summu ikdienas nolietojuma metodei, izmantojot vienu transakciju katrai dienai.</span><span class="sxs-lookup"><span data-stu-id="c9450-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="c9450-126">Finanšu</span><span class="sxs-lookup"><span data-stu-id="c9450-126">Fiscal</span></span>

<span data-ttu-id="c9450-127">Ja atlasāt lauka **Nolietojuma aprēķina gads** vērtību **Finanšu**, tad 150% regresīvā nolietojuma bilance tiek aprēķināta, pamatojoties uz finanšu gadu finanšu kalendāram, kas ir norādīts šai grāmatai, vai finanšu kalendāram, kas ir atlasīts lapā **Virsgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="c9450-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="c9450-128">Finanšu kalendāri tiek iestatīti lapā **Finanšu kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="c9450-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="c9450-129">Piemēram, finanšu gadam no 1. jūlija līdz 30. jūnijam nolietojuma aprēķins sākas 1. jūlijā.</span><span class="sxs-lookup"><span data-stu-id="c9450-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="c9450-130">Finanšu gads var būt garāks vai īsāks par 12 mēnešiem.</span><span class="sxs-lookup"><span data-stu-id="c9450-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="c9450-131">Nolietojums tiek pielāgots katram periodam.</span><span class="sxs-lookup"><span data-stu-id="c9450-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="c9450-132">Nākamā finanšu gada garumu nosaka periodu iestatījumi lapā **Finanšu kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="c9450-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="c9450-133">Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Finanšu**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="c9450-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="c9450-134">**Reizi gadā** — grāmato nolietojuma kopsummu, kas finanšu gadam tiek aprēķināta attiecīgā finanšu gada pēdējā datumā.</span><span class="sxs-lookup"><span data-stu-id="c9450-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="c9450-135">**Finanšu periods** — grāmato finanšu gadam aprēķinātā nolietojuma kopsummu.</span><span class="sxs-lookup"><span data-stu-id="c9450-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="c9450-136">Šī summa tiek uzkrāta finanšu periodos, kas ir definēti lapā **Finanšu kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="c9450-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="c9450-137">150% atlikumu bilances piemērs</span><span class="sxs-lookup"><span data-stu-id="c9450-137">Example of 150% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="c9450-138">Iegādes vērtība</span><span class="sxs-lookup"><span data-stu-id="c9450-138">Acquisition cost</span></span>               | <span data-ttu-id="c9450-139">11 000</span><span class="sxs-lookup"><span data-stu-id="c9450-139">11,000</span></span> |
| <span data-ttu-id="c9450-140">Lūžņu vērtība</span><span class="sxs-lookup"><span data-stu-id="c9450-140">Salvage value</span></span>                  | <span data-ttu-id="c9450-141">1000</span><span class="sxs-lookup"><span data-stu-id="c9450-141">1,000</span></span>  |
| <span data-ttu-id="c9450-142">Nolietojuma bāze</span><span class="sxs-lookup"><span data-stu-id="c9450-142">Depreciation base</span></span>              | <span data-ttu-id="c9450-143">10 000</span><span class="sxs-lookup"><span data-stu-id="c9450-143">10,000</span></span> |
| <span data-ttu-id="c9450-144">Lietošanas ilgums gados</span><span class="sxs-lookup"><span data-stu-id="c9450-144">Service life years</span></span>             | <span data-ttu-id="c9450-145">5.</span><span class="sxs-lookup"><span data-stu-id="c9450-145">5</span></span>      |
| <span data-ttu-id="c9450-146">Gada nolietojuma procenti</span><span class="sxs-lookup"><span data-stu-id="c9450-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="c9450-147">30%</span><span class="sxs-lookup"><span data-stu-id="c9450-147">30%</span></span>    |

<span data-ttu-id="c9450-148">Izmantojot 150% atlikumu bilances metodi, 150 procenti tiek dalīti ar lietošanas ilgumu gados.</span><span class="sxs-lookup"><span data-stu-id="c9450-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="c9450-149">Šie procenti tiek reizināti ar pamatlīdzekļa atlikušo vērtību, lai noteiktu gada nolietojuma summu.</span><span class="sxs-lookup"><span data-stu-id="c9450-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="c9450-150">Periods</span><span class="sxs-lookup"><span data-stu-id="c9450-150">Period</span></span> | <span data-ttu-id="c9450-151">Ikgadējā nolietojuma summas aprēķins</span><span class="sxs-lookup"><span data-stu-id="c9450-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="c9450-152">Atlikusī vērtība</span><span class="sxs-lookup"><span data-stu-id="c9450-152">Book value</span></span>             | <span data-ttu-id="c9450-153">Atlikusī vērtība gada beigās</span><span class="sxs-lookup"><span data-stu-id="c9450-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="c9450-154">1. gads</span><span class="sxs-lookup"><span data-stu-id="c9450-154">Year 1</span></span> | <span data-ttu-id="c9450-155">(11 000 – 1000) × 30% = 3000</span><span class="sxs-lookup"><span data-stu-id="c9450-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="c9450-156">11 000 – 3000 = 8000</span><span class="sxs-lookup"><span data-stu-id="c9450-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="c9450-157">11 000 – 1000 – 3000 = 7000</span><span class="sxs-lookup"><span data-stu-id="c9450-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="c9450-158">2. gads</span><span class="sxs-lookup"><span data-stu-id="c9450-158">Year 2</span></span> | <span data-ttu-id="c9450-159">7000 × 30% = 2100</span><span class="sxs-lookup"><span data-stu-id="c9450-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="c9450-160">8000 – 2100 = 5900</span><span class="sxs-lookup"><span data-stu-id="c9450-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="c9450-161">7000 – 2100 = 4900</span><span class="sxs-lookup"><span data-stu-id="c9450-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="c9450-162">3. gads</span><span class="sxs-lookup"><span data-stu-id="c9450-162">Year 3</span></span> | <span data-ttu-id="c9450-163">4900 × 30% = 1470</span><span class="sxs-lookup"><span data-stu-id="c9450-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="c9450-164">5900 – 1470 = 4430</span><span class="sxs-lookup"><span data-stu-id="c9450-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="c9450-165">4900 – 1470 = 3430</span><span class="sxs-lookup"><span data-stu-id="c9450-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="c9450-166">Kad summa, kas tiek aprēķināta, izmantojot 150% degresīvo nolietojuma aprēķināšanas metodi, kļūst mazāka par summu, kas rastos, lietojot lineāro metodi, atlikušā kalpošanas laika aprēķināšanai parasti notiek konversija uz lineāro metodi.</span><span class="sxs-lookup"><span data-stu-id="c9450-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




