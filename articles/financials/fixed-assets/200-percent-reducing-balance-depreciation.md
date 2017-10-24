---
title: "200 procentu atlikuma bilances aprēķināšanas metode"
description: "Šajā rakstā ir sniegts pārskats par 200 procentu degresīvās nolietojuma aprēķināšanas metodi."
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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 46afd002a370a43c9e1d2fb7cc5e61ece9033be9
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="31527-103">200 procentu atlikuma bilances aprēķināšanas metode</span><span class="sxs-lookup"><span data-stu-id="31527-103">200 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="31527-104">Šajā rakstā ir sniegts pārskats par 200 procentu degresīvās nolietojuma aprēķināšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="31527-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="31527-105">Ja iestatāt pamatlīdzekļa nolietojuma tabulu un atlasāt lauka **Metode** vērtību **200% atlikumu bilance** lapā **Nolietojuma tabulas**, pamatlīdzekļiem, kam ir piešķirta šī nolietojuma tabula, tiek izmantota vienāda nolietojuma procentu likme katrā nolietojuma periodā.</span><span class="sxs-lookup"><span data-stu-id="31527-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="31527-106">Procentu likme tiek aprēķināta, pamatojoties uz pamatlīdzekļa lietošanas ilgumu.</span><span class="sxs-lookup"><span data-stu-id="31527-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="31527-107">Piemēram, ja pamatlīdzekļa lietošanas ilgums ir pieci gadi, tiek aprēķināta procentu likme 40 procenti (200% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="31527-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="31527-108">Šī metode ir zināma kā dubultdegresīvā nolietojuma aprēķina metode.</span><span class="sxs-lookup"><span data-stu-id="31527-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="31527-109">Lai iestatītu 200 % atlikumu bilanci, jāatlasa arī opcijas laukā **Nolietojuma aprēķina gads**, kā arī laukā **Perioda biežums**, lapā **Nolietojuma tabulas**.</span><span class="sxs-lookup"><span data-stu-id="31527-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="31527-110">Laukā **Perioda biežums** pieejamās opcijas atšķiras atkarībā no vērtības, ko esat atlasījis laukā **Nolietojuma aprēķina gads**.</span><span class="sxs-lookup"><span data-stu-id="31527-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="31527-111">Nolietojuma aprēķināšanas gada atlasīšana</span><span class="sxs-lookup"><span data-stu-id="31527-111">Select a depreciation year</span></span>
<span data-ttu-id="31527-112">Lapā **Nolietojuma tabulas** laukā **Nolietojuma aprēķina gads** varat atlasīt **Kalendārs** vai **Finanšu**.</span><span class="sxs-lookup"><span data-stu-id="31527-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="31527-113">Noklusējuma vērtība ir **Kalendārs**.</span><span class="sxs-lookup"><span data-stu-id="31527-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="31527-114">Jūsu atlase nosaka, kādas opcijas ir pieejamas laukā **Periodu biežums**.</span><span class="sxs-lookup"><span data-stu-id="31527-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="31527-115">Šis lauks nosaka nolietojuma uzkrājuma grāmatošanas datumus un summas kalendārā gada laikā.</span><span class="sxs-lookup"><span data-stu-id="31527-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="31527-116">Kalendārs</span><span class="sxs-lookup"><span data-stu-id="31527-116">Calendar</span></span>

<span data-ttu-id="31527-117">Laukā **Nolietojuma aprēķina gads** varat paturēt noklusējuma vērtību **Kalendārs**.</span><span class="sxs-lookup"><span data-stu-id="31527-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="31527-118">Opcija **Kalendārs** nolietojuma bāzi atjaunina katru gadu 1. janvārī.</span><span class="sxs-lookup"><span data-stu-id="31527-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="31527-119">Parasti nolietojums ir atlikusī vērtība mīnus lūžņu vērtība.</span><span class="sxs-lookup"><span data-stu-id="31527-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="31527-120">Tālāk šajā tēmā redzamajos piemēros nolietojuma bāze ir aprēķinu kolonnas pirmās izteiksmes skaitītājs.</span><span class="sxs-lookup"><span data-stu-id="31527-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="31527-121">Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Kalendārs**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="31527-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="31527-122">**Reizi gadā** grāmato summu 31. decembrī.</span><span class="sxs-lookup"><span data-stu-id="31527-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="31527-123">**Reizi mēnesī** grāmato mēneša summu katra kalendārā mēneša beigās.</span><span class="sxs-lookup"><span data-stu-id="31527-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="31527-124">**Reizi ceturksnī** grāmato ceturkšņa summu katra kalendārā ceturkšņa beigās (31. martā, 30. jūnijā, 30. septembrī un 31. decembrī).</span><span class="sxs-lookup"><span data-stu-id="31527-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="31527-125">**Reizi pusgadā** — grāmato pusgada summu katrā kalendārajā pusgadā (30. jūnijā un 31. decembrī).</span><span class="sxs-lookup"><span data-stu-id="31527-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="31527-126">**Reizi dienā** — grāmato nolietojuma summu ikdienas nolietojuma metodei, izmantojot vienu transakciju katrai dienai.</span><span class="sxs-lookup"><span data-stu-id="31527-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="31527-127">Finanšu</span><span class="sxs-lookup"><span data-stu-id="31527-127">Fiscal</span></span>

<span data-ttu-id="31527-128">Ja atlasāt lauka **Nolietojuma aprēķina gads** vērtību **Finanšu**, tad 200 % regresīvā nolietojuma bilance tiek aprēķināta, pamatojoties uz finanšu gadu finanšu kalendāram, kas ir norādīts šai grāmatai, vai finanšu kalendāram, kas ir atlasīts lapā **Virsgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="31527-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="31527-129">Finanšu kalendāri tiek iestatīti lapā **Finanšu kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="31527-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="31527-130">Piemēram, finanšu gadam no 1. jūlija līdz 30. jūnijam nolietojuma aprēķins sākas 1. jūlijā.</span><span class="sxs-lookup"><span data-stu-id="31527-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="31527-131">Finanšu gads var būt garāks vai īsāks par 12 mēnešiem.</span><span class="sxs-lookup"><span data-stu-id="31527-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="31527-132">Nolietojums tiek pielāgots katram periodam.</span><span class="sxs-lookup"><span data-stu-id="31527-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="31527-133">Nākamā finanšu gada garumu nosaka periodu iestatījumi lapā **Finanšu kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="31527-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="31527-134">Ja ir atlasīta nolietojuma aprēķināšanas gada opcija **Finanšu**, laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="31527-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="31527-135">**Reizi gadā** finanšu gada aprēķinātā nolietojuma kopsumma tiek iegrāmatota finanšu gada pēdējā datumā kā viena summa.</span><span class="sxs-lookup"><span data-stu-id="31527-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="31527-136">**Finanšu periods** — grāmato finanšu gadam aprēķinātā nolietojuma kopsummu.</span><span class="sxs-lookup"><span data-stu-id="31527-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="31527-137">Šī summa tiek uzkrāta finanšu periodos, kas ir definēti lapā **Finanšu kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="31527-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="31527-138">200%  atlikumu bilances piemērs</span><span class="sxs-lookup"><span data-stu-id="31527-138">Example of 200% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="31527-139">Iegādes vērtība</span><span class="sxs-lookup"><span data-stu-id="31527-139">Acquisition cost</span></span>               | <span data-ttu-id="31527-140">11 000</span><span class="sxs-lookup"><span data-stu-id="31527-140">11,000</span></span> |
| <span data-ttu-id="31527-141">Lūžņu vērtība</span><span class="sxs-lookup"><span data-stu-id="31527-141">Salvage value</span></span>                  | <span data-ttu-id="31527-142">1000</span><span class="sxs-lookup"><span data-stu-id="31527-142">1, 000</span></span> |
| <span data-ttu-id="31527-143">Nolietojuma bāze</span><span class="sxs-lookup"><span data-stu-id="31527-143">Depreciation base</span></span>              | <span data-ttu-id="31527-144">10 000</span><span class="sxs-lookup"><span data-stu-id="31527-144">10,000</span></span> |
| <span data-ttu-id="31527-145">Lietošanas ilgums gados</span><span class="sxs-lookup"><span data-stu-id="31527-145">Service life years</span></span>             | <span data-ttu-id="31527-146">5.</span><span class="sxs-lookup"><span data-stu-id="31527-146">5</span></span>      |
| <span data-ttu-id="31527-147">Gada nolietojuma procenti</span><span class="sxs-lookup"><span data-stu-id="31527-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="31527-148">40%</span><span class="sxs-lookup"><span data-stu-id="31527-148">40%</span></span>    |

<span data-ttu-id="31527-149">Izmantojot 200% atlikumu bilances metodi, 200 procenti tiek dalīti ar lietošanas ilgumu gados.</span><span class="sxs-lookup"><span data-stu-id="31527-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="31527-150">Šie procenti tiek reizināti ar pamatlīdzekļa atlikušo vērtību, lai noteiktu gada nolietojuma summu.</span><span class="sxs-lookup"><span data-stu-id="31527-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="31527-151">Periods</span><span class="sxs-lookup"><span data-stu-id="31527-151">Period</span></span> | <span data-ttu-id="31527-152">Ikgadējā nolietojuma summas aprēķins</span><span class="sxs-lookup"><span data-stu-id="31527-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="31527-153">Atlikusī vērtība</span><span class="sxs-lookup"><span data-stu-id="31527-153">Book value</span></span>             | <span data-ttu-id="31527-154">Atlikusī vērtība gada beigās</span><span class="sxs-lookup"><span data-stu-id="31527-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="31527-155">1. gads</span><span class="sxs-lookup"><span data-stu-id="31527-155">Year 1</span></span> | <span data-ttu-id="31527-156">(11 000 – 1000) × 40% = 4000</span><span class="sxs-lookup"><span data-stu-id="31527-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="31527-157">11 000 – 4000 = 7000</span><span class="sxs-lookup"><span data-stu-id="31527-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="31527-158">11 000 – 1000 – 4000 = 6000</span><span class="sxs-lookup"><span data-stu-id="31527-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="31527-159">2. gads</span><span class="sxs-lookup"><span data-stu-id="31527-159">Year 2</span></span> | <span data-ttu-id="31527-160">6000 × 40% = 2400</span><span class="sxs-lookup"><span data-stu-id="31527-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="31527-161">7000 – 2400 = 4600</span><span class="sxs-lookup"><span data-stu-id="31527-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="31527-162">6000 – 2400 = 3600</span><span class="sxs-lookup"><span data-stu-id="31527-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="31527-163">3. gads</span><span class="sxs-lookup"><span data-stu-id="31527-163">Year 3</span></span> | <span data-ttu-id="31527-164">3600 × 40% = 1440</span><span class="sxs-lookup"><span data-stu-id="31527-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="31527-165">4600 – 1440 = 3160</span><span class="sxs-lookup"><span data-stu-id="31527-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="31527-166">3600 – 1440 = 2160</span><span class="sxs-lookup"><span data-stu-id="31527-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="31527-167">Kad summa, kas tiek aprēķināta, izmantojot 200% degresīvo nolietojuma aprēķināšanas metodi, kļūst mazāka par summu, kas rastos, lietojot lineāro metodi, atlikušā kalpošanas laika aprēķināšanai parasti notiek konversija uz lineāro metodi.</span><span class="sxs-lookup"><span data-stu-id="31527-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




