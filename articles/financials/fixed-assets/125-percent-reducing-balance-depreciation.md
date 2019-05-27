---
title: 125 procentu atlikuma bilances aprēķināšanas metode
description: Šajā rakstā ir sniegts pārskats par 125 procentu degresīvās nolietojuma aprēķināšanas metodi.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7af5413376a98c3b2b7ded46c757c9156a3fadf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555700"
---
# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="ad1ce-103">125 procentu atlikuma bilances aprēķināšanas metode</span><span class="sxs-lookup"><span data-stu-id="ad1ce-103">125 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad1ce-104">Šajā rakstā ir sniegts pārskats par 125 procentu degresīvās nolietojuma aprēķināšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="ad1ce-105">Iestatot pamatlīdzekļa nolietojuma tabulu un atlasot **125% atlikumu bilance** laukā **Metode**, lapā **Nolietojuma tabulas**, nolietojuma tabulai piešķirtā pamatlīdzekļa nolietojuma procenti ir vienādi visos nolietojuma periodos.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="ad1ce-106">Šī procentu likme tiek aprēķināta, pamatojoties uz pamatlīdzekļa lietošanas ilgumu.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="ad1ce-107">Piemēram, ja pamatlīdzekļa lietošanas ilgums ir pieci gadi, tiks aprēķināta procentu likme 25 procenti (125% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="ad1ce-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="ad1ce-108">Lai iestatītu 125 % atlikumu bilanci, jāatlasa arī opcijas laukā **Nolietojuma aprēķina gads**, kā arī laukā **Perioda biežums**, lapā **Nolietojuma tabulas**.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ad1ce-109">Laukā **Perioda biežums** pieejamās opcijas ir atkarīgas no vērtības, kas ir atlasīta laukā **Nolietojuma aprēķina gads**.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="ad1ce-110">Nolietojuma aprēķināšanas gada atlasīšana</span><span class="sxs-lookup"><span data-stu-id="ad1ce-110">Select a depreciation year</span></span>
<span data-ttu-id="ad1ce-111">Lapā **Nolietojuma tabulas** laukā **Nolietojuma aprēķina gads** varat atlasīt **Kalendārs** vai **Finanšu**.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ad1ce-112">Noklusējuma vērtība ir **Kalendārs**.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="ad1ce-113">Jūsu atlase nosaka, kādas opcijas ir pieejamas laukā **Periodu biežums**.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="ad1ce-114">Šis lauks nosaka nolietojuma uzkrājuma grāmatošanas datumus un summas kalendārā gada laikā.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="ad1ce-115">Kalendārs</span><span class="sxs-lookup"><span data-stu-id="ad1ce-115">Calendar</span></span>

<span data-ttu-id="ad1ce-116">Laukā **Nolietojuma aprēķina gads** varat paturēt noklusējuma vērtību **Kalendārs**.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="ad1ce-117">Opcija **Kalendārs** nolietojuma bāzi atjaunina katru gadu 1. janvārī.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="ad1ce-118">Parasti nolietojuma bāze ir atlikusī vērtība mīnus lūžņu vērtība.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="ad1ce-119">Tālāk šajā tēmā redzamajos piemēros nolietojuma bāze ir aprēķinu kolonnas pirmās izteiksmes skaitītājs.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="ad1ce-120">Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Kalendārs**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ad1ce-121">**Reizi gadā** grāmato summu 31. decembrī.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="ad1ce-122">**Reizi mēnesī** grāmato mēneša summu katra kalendārā mēneša beigās.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="ad1ce-123">**Reizi ceturksnī** grāmato ceturkšņa summu katra kalendārā ceturkšņa beigās (31. martā, 30. jūnijā, 30. septembrī un 31. decembrī).</span><span class="sxs-lookup"><span data-stu-id="ad1ce-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="ad1ce-124">**Reizi pusgadā** — grāmato pusgada summu katrā kalendārajā pusgadā (30. jūnijā un 31. decembrī).</span><span class="sxs-lookup"><span data-stu-id="ad1ce-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="ad1ce-125">**Reizi dienā** — grāmato nolietojuma summu ikdienas nolietojuma metodei, izmantojot vienu transakciju katrai dienai.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="ad1ce-126">Finanšu</span><span class="sxs-lookup"><span data-stu-id="ad1ce-126">Fiscal</span></span>

<span data-ttu-id="ad1ce-127">Ja atlasāt lauka **Nolietojuma aprēķina gads** vērtību **Finanšu**, tad 125% regresīvais nolietojums tiek aprēķināts, pamatojoties uz finanšu gadu finanšu kalendāram, kas ir norādīts šai grāmatai, vai finanšu kalendāram, kas ir atlasīts lapā **Virsgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="ad1ce-128">Finanšu kalendāri tiek iestatīti lapā **Finanšu kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="ad1ce-129">Piemēram, finanšu gadam no 1. jūlija līdz 30. jūnijam nolietojuma aprēķins sākas 1. jūlijā.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="ad1ce-130">Finanšu gads var būt garāks vai īsāks par 12 mēnešiem.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="ad1ce-131">Nolietojums tiek automātiski pielāgots katram periodam, un nākamā finanšu gada garumu nosaka periodu iestatījumi lapā **Finanšu kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="ad1ce-132">Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Finanšu**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ad1ce-133">**Reizi gadā** finanšu gada aprēķinātā nolietojuma kopsumma tiek iegrāmatota finanšu gada pēdējā datumā kā viena summa.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="ad1ce-134">**Finanšu periods** — grāmato finanšu gadam aprēķinātā nolietojuma kopsummu.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="ad1ce-135">Šī summa tiek uzkrāta finanšu periodos, kas ir definēti lapā **Finanšu kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="ad1ce-136">125% atlikumu bilances piemērs</span><span class="sxs-lookup"><span data-stu-id="ad1ce-136">Example of 125% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="ad1ce-137">Iegādes vērtība</span><span class="sxs-lookup"><span data-stu-id="ad1ce-137">Acquisition cost</span></span>               | <span data-ttu-id="ad1ce-138">11 000</span><span class="sxs-lookup"><span data-stu-id="ad1ce-138">11,000</span></span> |
| <span data-ttu-id="ad1ce-139">Lūžņu vērtība</span><span class="sxs-lookup"><span data-stu-id="ad1ce-139">Salvage value</span></span>                  | <span data-ttu-id="ad1ce-140">1000</span><span class="sxs-lookup"><span data-stu-id="ad1ce-140">1,000</span></span>  |
| <span data-ttu-id="ad1ce-141">Nolietojuma bāze</span><span class="sxs-lookup"><span data-stu-id="ad1ce-141">Depreciation base</span></span>              | <span data-ttu-id="ad1ce-142">10 000</span><span class="sxs-lookup"><span data-stu-id="ad1ce-142">10,000</span></span> |
| <span data-ttu-id="ad1ce-143">Lietošanas ilgums gados</span><span class="sxs-lookup"><span data-stu-id="ad1ce-143">Service life years</span></span>             | <span data-ttu-id="ad1ce-144">5.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-144">5</span></span>      |
| <span data-ttu-id="ad1ce-145">Gada nolietojuma procenti</span><span class="sxs-lookup"><span data-stu-id="ad1ce-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="ad1ce-146">25%</span><span class="sxs-lookup"><span data-stu-id="ad1ce-146">25%</span></span>    |

<span data-ttu-id="ad1ce-147">125 % atlikumu bilances metode dala 125 procentus ar lietošanas ilguma gadiem.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="ad1ce-148">Šie procenti tiek reizināti ar pamatlīdzekļa atlikušo vērtību, lai noteiktu gada nolietojuma summu.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="ad1ce-149">Periods</span><span class="sxs-lookup"><span data-stu-id="ad1ce-149">Period</span></span> | <span data-ttu-id="ad1ce-150">Ikgadējā nolietojuma summas aprēķins</span><span class="sxs-lookup"><span data-stu-id="ad1ce-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="ad1ce-151">Atlikusī vērtība</span><span class="sxs-lookup"><span data-stu-id="ad1ce-151">Book value</span></span>                    | <span data-ttu-id="ad1ce-152">Atlikusī vērtība gada beigās</span><span class="sxs-lookup"><span data-stu-id="ad1ce-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="ad1ce-153">1. gads</span><span class="sxs-lookup"><span data-stu-id="ad1ce-153">Year 1</span></span> | <span data-ttu-id="ad1ce-154">(11000 – 1000) × 25% = 2500</span><span class="sxs-lookup"><span data-stu-id="ad1ce-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="ad1ce-155">(11000 – 2500) = 8500</span><span class="sxs-lookup"><span data-stu-id="ad1ce-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="ad1ce-156">(11000 – 1000 – 2500) = 7500</span><span class="sxs-lookup"><span data-stu-id="ad1ce-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="ad1ce-157">2. gads</span><span class="sxs-lookup"><span data-stu-id="ad1ce-157">Year 2</span></span> | <span data-ttu-id="ad1ce-158">7500 × 25% = 1875</span><span class="sxs-lookup"><span data-stu-id="ad1ce-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="ad1ce-159">(8500 – 1875) = 6625</span><span class="sxs-lookup"><span data-stu-id="ad1ce-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="ad1ce-160">(7500 – 1875) = 5625</span><span class="sxs-lookup"><span data-stu-id="ad1ce-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="ad1ce-161">3. gads</span><span class="sxs-lookup"><span data-stu-id="ad1ce-161">Year 3</span></span> | <span data-ttu-id="ad1ce-162">5625 × 25% = 1406,25</span><span class="sxs-lookup"><span data-stu-id="ad1ce-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="ad1ce-163">(6625 – 1406,25) = 5218,75</span><span class="sxs-lookup"><span data-stu-id="ad1ce-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="ad1ce-164">(5625 – 1406,25) = 4218,75</span><span class="sxs-lookup"><span data-stu-id="ad1ce-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="ad1ce-165">Kad summa, kas tiek aprēķināta, izmantojot 125% degresīvo nolietojuma aprēķināšanas metodi, kļūst mazāka par summu, kas tiktu aprēķināta, izmantojot lineāro metodi, atlikušā kalpošanas laika aprēķināšanai parasti tiek izmantota lineārā metode.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



