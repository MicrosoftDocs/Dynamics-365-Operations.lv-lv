---
title: "175 procentu degresīvā nolietojuma aprēķināšanas metode"
description: "Šajā tēmā ir sniegts pārskats par 175 procentu degresīvā nolietojuma aprēķināšanas metodi."
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a61e743898e3e65c0012a7aeb9837e55e9143d01
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="ee0ad-103">175 procentu degresīvā nolietojuma aprēķināšanas metode</span><span class="sxs-lookup"><span data-stu-id="ee0ad-103">175 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ee0ad-104">Šajā tēmā ir sniegts pārskats par 175 procentu degresīvā nolietojuma aprēķināšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="ee0ad-105">Ja iestatāt pamatlīdzekļa nolietojuma tabulu un atlasāt lauka **Metode** vērtību **175% atlikumu bilance** lapā **Nolietojuma tabulas**, pamatlīdzekļiem, kam ir piešķirta šī nolietojuma tabula, tiek izmantota vienāda nolietojuma procentu likme katrā nolietojuma periodā.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="ee0ad-106">Lai iestatītu 175 % atlikumu bilanci, jāatlasa arī opcijas laukā **Nolietojuma aprēķina gads**, kā arī laukā **Perioda biežums**, lapā **Nolietojuma tabulas**.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ee0ad-107">Laukā **Perioda biežums** pieejamās opcijas ir atkarīgas no vērtības, kas ir atlasīta laukā **Nolietojuma aprēķina gads**.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="ee0ad-108">Nolietojuma aprēķināšanas gada atlasīšana</span><span class="sxs-lookup"><span data-stu-id="ee0ad-108">Select a depreciation year</span></span>
<span data-ttu-id="ee0ad-109">Lapā **Nolietojuma tabulas** laukā **Nolietojuma aprēķina gads** varat atlasīt **Kalendārs** vai **Finanšu**.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ee0ad-110">Noklusējuma vērtība ir **Kalendārs**.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="ee0ad-111">Jūsu atlase nosaka, kādas opcijas ir pieejamas laukā **Periodu biežums**.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="ee0ad-112">Šis lauks nosaka nolietojuma uzkrājuma grāmatošanas datumus un summas kalendārā gada laikā.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="ee0ad-113">Kalendārs</span><span class="sxs-lookup"><span data-stu-id="ee0ad-113">Calendar</span></span>

<span data-ttu-id="ee0ad-114">Laukā **Nolietojuma aprēķina gads** varat paturēt noklusējuma vērtību **Kalendārs**.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="ee0ad-115">Opcija **Kalendārs** nolietojuma bāzi atjaunina katru gadu 1. janvārī.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="ee0ad-116">Parasti nolietojuma bāze ir atlikusī vērtība mīnus lūžņu vērtība.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="ee0ad-117">Tālāk šajā tēmā redzamajos piemēros nolietojuma bāze ir aprēķinu kolonnas pirmās izteiksmes skaitītājs.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="ee0ad-118">Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Kalendārs**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ee0ad-119">**Reizi gadā** grāmato summu 31. decembrī.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="ee0ad-120">**Reizi mēnesī** grāmato mēneša summu katra kalendārā mēneša beigās.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="ee0ad-121">**Reizi ceturksnī** grāmato ceturkšņa summu katra kalendārā ceturkšņa beigās (31. martā, 30. jūnijā, 30. septembrī un 31. decembrī).</span><span class="sxs-lookup"><span data-stu-id="ee0ad-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="ee0ad-122">**Reizi pusgadā** — grāmato pusgada summu katrā kalendārajā pusgadā (30. jūnijā un 31. decembrī).</span><span class="sxs-lookup"><span data-stu-id="ee0ad-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="ee0ad-123">**Reizi dienā** — grāmato nolietojuma summu ikdienas nolietojuma metodei, izmantojot vienu transakciju katrai dienai.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="ee0ad-124">Finanšu</span><span class="sxs-lookup"><span data-stu-id="ee0ad-124">Fiscal</span></span>

<span data-ttu-id="ee0ad-125">Ja atlasāt lauka **Nolietojuma aprēķina gads** vērtību **Finanšu**, tad 175% regresīvā nolietojuma bilance tiek aprēķināta, pamatojoties uz finanšu gadu finanšu kalendāram, kas ir norādīts šai grāmatai, vai finanšu kalendāram, kas ir atlasīts lapā **Virsgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="ee0ad-126">Finanšu kalendāri tiek iestatīti lapā **Finanšu kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="ee0ad-127">Papildinformāciju skatiet rakstā [Finanšu kalendāri, finanšu gadi un periodi](..\budgeting\fiscal-calendars-fiscal-years-periods.md).</span><span class="sxs-lookup"><span data-stu-id="ee0ad-127">For more information, see [Fiscal calendars, fiscal years, and periods](..\budgeting\fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="ee0ad-128">Piemēram, finanšu gadam no 1. jūlija līdz 30. jūnijam nolietojuma aprēķins sākas 1. jūlijā.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="ee0ad-129">Finanšu gads var būt garāks vai īsāks par 12 mēnešiem.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="ee0ad-130">Nolietojums tiek automātiski pielāgots katram periodam, un nākamā finanšu gada garumu nosaka periodu iestatījumi lapā **Finanšu kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="ee0ad-131">Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Finanšu**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ee0ad-132">**Reizi gadā** — grāmato nolietojuma kopsummu, kas finanšu gadam tiek aprēķināta attiecīgā finanšu gada pēdējā datumā.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="ee0ad-133">**Finanšu periods** — aprēķina finanšu gadam aprēķināto nolietojuma kopsummu.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="ee0ad-134">Šī summa tiek uzkrāta finanšu periodos, kas ir definēti lapā **Finanšu kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="ee0ad-135">Atlikuma samazinošā nolietojuma par 175% piemērs</span><span class="sxs-lookup"><span data-stu-id="ee0ad-135">Example of 175% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="ee0ad-136">Iegādes vērtība</span><span class="sxs-lookup"><span data-stu-id="ee0ad-136">Acquisition cost</span></span>               | <span data-ttu-id="ee0ad-137">11 000</span><span class="sxs-lookup"><span data-stu-id="ee0ad-137">11,000</span></span> |
| <span data-ttu-id="ee0ad-138">Lūžņu vērtība</span><span class="sxs-lookup"><span data-stu-id="ee0ad-138">Salvage value</span></span>                  | <span data-ttu-id="ee0ad-139">1000</span><span class="sxs-lookup"><span data-stu-id="ee0ad-139">1,000</span></span>  |
| <span data-ttu-id="ee0ad-140">Nolietojuma bāze</span><span class="sxs-lookup"><span data-stu-id="ee0ad-140">Depreciation base</span></span>              | <span data-ttu-id="ee0ad-141">10 000</span><span class="sxs-lookup"><span data-stu-id="ee0ad-141">10,000</span></span> |
| <span data-ttu-id="ee0ad-142">Lietošanas ilgums gados</span><span class="sxs-lookup"><span data-stu-id="ee0ad-142">Service life years</span></span>             | <span data-ttu-id="ee0ad-143">5.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-143">5</span></span>      |
| <span data-ttu-id="ee0ad-144">Gada nolietojuma procenti</span><span class="sxs-lookup"><span data-stu-id="ee0ad-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="ee0ad-145">35%</span><span class="sxs-lookup"><span data-stu-id="ee0ad-145">35%</span></span>    |

<span data-ttu-id="ee0ad-146">Izmantojot 175% degresīvā nolietojuma aprēķināšanas metodi, 175 procenti tiek dalīti ar lietošanas ilgumu gados.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="ee0ad-147">Šie procenti tiek reizināti ar pamatlīdzekļa atlikušo vērtību, lai noteiktu gada nolietojuma summu.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="ee0ad-148">Periods</span><span class="sxs-lookup"><span data-stu-id="ee0ad-148">Period</span></span> | <span data-ttu-id="ee0ad-149">Ikgadējā nolietojuma summas aprēķins</span><span class="sxs-lookup"><span data-stu-id="ee0ad-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="ee0ad-150">Atlikusī vērtība</span><span class="sxs-lookup"><span data-stu-id="ee0ad-150">Book value</span></span>                  | <span data-ttu-id="ee0ad-151">Atlikusī vērtība gada beigās</span><span class="sxs-lookup"><span data-stu-id="ee0ad-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="ee0ad-152">1. gads</span><span class="sxs-lookup"><span data-stu-id="ee0ad-152">Year 1</span></span> | <span data-ttu-id="ee0ad-153">(11 000 – 1000) × 35% = 3500</span><span class="sxs-lookup"><span data-stu-id="ee0ad-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="ee0ad-154">11 000 – 3500 = 7500</span><span class="sxs-lookup"><span data-stu-id="ee0ad-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="ee0ad-155">11 000 – 1000 – 3500 = 6500</span><span class="sxs-lookup"><span data-stu-id="ee0ad-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="ee0ad-156">2. gads</span><span class="sxs-lookup"><span data-stu-id="ee0ad-156">Year 2</span></span> | <span data-ttu-id="ee0ad-157">6500 × 35% = 2275</span><span class="sxs-lookup"><span data-stu-id="ee0ad-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="ee0ad-158">7500 – 2275 = 5225</span><span class="sxs-lookup"><span data-stu-id="ee0ad-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="ee0ad-159">6500 – 2275 = 4225</span><span class="sxs-lookup"><span data-stu-id="ee0ad-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="ee0ad-160">3. gads</span><span class="sxs-lookup"><span data-stu-id="ee0ad-160">Year 3</span></span> | <span data-ttu-id="ee0ad-161">4225 × 35% = 1478,75</span><span class="sxs-lookup"><span data-stu-id="ee0ad-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="ee0ad-162">5225 – 1478,75 = 3746,25</span><span class="sxs-lookup"><span data-stu-id="ee0ad-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="ee0ad-163">4225 – 1478,75 = 2746,25</span><span class="sxs-lookup"><span data-stu-id="ee0ad-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="ee0ad-164">Kad summa, kas tiek aprēķināta, izmantojot 175% degresīvo nolietojuma aprēķināšanas metodi, kļūst mazāka par summu, kas rastos, lietojot lineāro metodi, atlikušā kalpošanas laika aprēķināšanai parasti notiek konversija uz lineāro metodi.</span><span class="sxs-lookup"><span data-stu-id="ee0ad-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




