---
title: "Degresīvā nolietojuma aprēķināšanas metode"
description: "Šajā rakstā ir sniegts pārskats par degresīvās nolietojuma aprēķināšanas metodi."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 94bd18697c5074deb17980d4354dc0e690233f6f
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="reduce-balance-depreciation"></a><span data-ttu-id="b0a9f-103">Degresīvā nolietojuma aprēķināšanas metode</span><span class="sxs-lookup"><span data-stu-id="b0a9f-103">Reduce balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0a9f-104">Šajā rakstā ir sniegts pārskats par degresīvās nolietojuma aprēķināšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="b0a9f-105">Iestatot pamatlīdzekļa nolietojuma profilu un nolietojuma profilu lapas metodes laukā atlasot Degresīvais nolietojums, līdzekļiem, kuriem piešķirts šis nolietojuma profils, nolietojuma procenti ir vienādi visos nolietojuma periodos.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="b0a9f-106">Lai iestatītu degresīvo nolietojuma aprēķināšanas metodi, jāveic atlase arī kopsavilkuma cilnes Vispārīgi laukos lapā Nolietojuma profili.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="b0a9f-107">Sākumā atlasiet gadu laukā Nolietojuma gads.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="b0a9f-108">Atkarībā no atlases, laukā Perioda biežums tiek parādītas dažādas opcijas, kas izskaidrotas tālākajās sadaļās.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="b0a9f-109">Jāievada arī vērtība nolietojuma profila laukā Procenti.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="b0a9f-110">Atlasot opciju Pilns nolietojums, atlikusī nolietojuma bāze tiek ņemta pēdējā nolietojuma periodā un var būt liela summa.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="b0a9f-111">Dažas valstis/reģioni neizmanto pārslēgšanos uz lineāro metodi.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="b0a9f-112">Pārslēgšanās notiek tad, ja alternatīvās nolietojuma aprēķina metodes summa ir lielāka par primārā nolietojuma profila summu vai vienāda ar to, un izmantotā nolietojuma summa būs alternatīvās metodes summa.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="b0a9f-113">Tā kā, pamatojoties uz procentuālo aprēķinu, pamatlīdzeklis nekad nebūs pilnīgi nolietots, pilnīgam līdzekļa nolietojumam jāatlasa opcija Pilns nolietojums.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="b0a9f-114">Nolietojuma aprēķināšanas gada atlasīšana</span><span class="sxs-lookup"><span data-stu-id="b0a9f-114">Select a depreciation year</span></span>
<span data-ttu-id="b0a9f-115">Nolietojuma profilu lapas laukā Nolietojuma aprēķina gads varat atlasīt Kalendārs vai Finanšu.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="b0a9f-116">Atlase nosaka opcijas, kas pieejamas laukā Periodu biežums.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="b0a9f-117">Noklusējuma opcija ir Kalendārs.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="b0a9f-118">Kalendārs</span><span class="sxs-lookup"><span data-stu-id="b0a9f-118">Calendar</span></span>

<span data-ttu-id="b0a9f-119">Opcija Kalendārs atjaunina nolietojuma bāzi (parasti atlikusī vērtība mīnus lūžņu vērtība) katra gada 1. janvārī.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="b0a9f-120">Tālāk tekstā minētajā degresīvās nolietojuma aprēķināšanas metodes piemērā nolietojuma bāze ir aprēķinu pirmās izteiksmes skaitītājs aprēķina kolonnā.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="b0a9f-121">Atlasot opciju Kalendārs, laukā Periodu biežums ir četras opcijas, kas nosaka nolietojuma uzkrājuma grāmatošanas datumus un summas kalendārā gada laikā:</span><span class="sxs-lookup"><span data-stu-id="b0a9f-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="b0a9f-122">ikgadējs grāmatojums 31. decembrī,</span><span class="sxs-lookup"><span data-stu-id="b0a9f-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="b0a9f-123">ikmēneša grāmatojums par mēneša summu katra kalendārā mēneša beigās,</span><span class="sxs-lookup"><span data-stu-id="b0a9f-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="b0a9f-124">katra ceturkšņa grāmatojums par ceturkšņa summu katra kalendārā ceturkšņa beigās (31. marts, 30. jūnijs, 30. septembris un 31. decembris),</span><span class="sxs-lookup"><span data-stu-id="b0a9f-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="b0a9f-125">pusgada grāmatojums par pusgada summu katra kalendārā pusgada beigās (30. jūnijs un 31. decembris),</span><span class="sxs-lookup"><span data-stu-id="b0a9f-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="b0a9f-126">ikdienas grāmatojums par nolietojuma summu ikdienas nolietojuma metodei, izmantojot vienu transakciju katrai dienai.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="b0a9f-127">Piemēram, ja atlasāt Reizi gadā, gada nolietojums tiek grāmatots tikai vienu reizi, katra gada 31. decembrī.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="b0a9f-128">Ja atlasāt Reizi mēnesī, ikmēneša nolietojums tiek grāmatots katru mēnesi kā 1/12 daļa no ikgadējās nolietojuma summas.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="b0a9f-129">Finanšu</span><span class="sxs-lookup"><span data-stu-id="b0a9f-129">Fiscal</span></span>

<span data-ttu-id="b0a9f-130">Ja laukā Nolietojuma aprēķina gads atlasāt Finanšu, tiek izmantota lineārā nolietojuma metode.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="b0a9f-131">Tā tiek aprēķināta, pamatojoties uz finanšu gadu, kas iestatīts lapā Finanšu kalendāri tam finanšu kalendāram, kas atlasīts Virsgrāmatas lapā.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="b0a9f-132">Piemēram, finanšu gadam no 1. jūlija līdz 30. jūnijam nolietojuma aprēķins sākas 1. jūlijā.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="b0a9f-133">Finanšu gads var būt garāks vai īsāks par 12 mēnešiem.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="b0a9f-134">Nolietojums tiek pielāgots katram finanšu periodam.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="b0a9f-135">Nākamā finanšu gada garums tiek noteikts, balstoties uz finanšu periodiem, kurus iestatāt jauna finanšu gada izveidē lapā Finanšu kalendāri.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="b0a9f-136">Atlasot opciju Finanšu, laukā Periodu biežums ir pieejamas tālāk uzskaitītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="b0a9f-137">Ikgadēji grāmatojumi, kad finanšu gada aprēķinātā nolietojuma kopsumma tiek iegrāmatota finanšu gada pēdējā datumā kā viena summa.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="b0a9f-138">Finanšu perioda grāmatojumi, kad iegrāmato visu aprēķināto finanšu gada nolietojuma summu, kas uzkrāta finanšu periodos, kuri ir definēti virsgrāmatas lapā atlasītajā finanšu kalendārā vai finanšu kalendārā, kurš ir atlasīts pamatlīdzekļa grāmatai.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="b0a9f-139">Degresīvā nolietojuma aprēķināšanas piemērs</span><span class="sxs-lookup"><span data-stu-id="b0a9f-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="b0a9f-140">Pieņemsim, ka pamatlīdzekļa iegādes cena ir 11 000, lūžņu vērtība ir 1000 un nolietojuma procentuālais koeficients ir 30.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="b0a9f-141">Izmantojot degresīvās nolietojuma aprēķināšanas metodi, 30 procenti no nolietojuma bāzes (atlikusī vērtība mīnus lūžņu vērtība) tiek aprēķināti iepriekšējā nolietojuma perioda beigās.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="b0a9f-142">Nolietojuma aprēķins pirmajiem trim gadiem ir parādīts tabulā.</span><span class="sxs-lookup"><span data-stu-id="b0a9f-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="b0a9f-143">Periods</span><span class="sxs-lookup"><span data-stu-id="b0a9f-143">Period</span></span> | <span data-ttu-id="b0a9f-144">Ikgada nolietojuma summas aprēķins</span><span class="sxs-lookup"><span data-stu-id="b0a9f-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="b0a9f-145">Atlikusī vērtība gada beigās</span><span class="sxs-lookup"><span data-stu-id="b0a9f-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="b0a9f-146">1. gads</span><span class="sxs-lookup"><span data-stu-id="b0a9f-146">Year 1</span></span> | <span data-ttu-id="b0a9f-147">(11 000 – 1000) \* 30% = 3000</span><span class="sxs-lookup"><span data-stu-id="b0a9f-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="b0a9f-148">(11000 - 1000) - 3000 = 7000</span><span class="sxs-lookup"><span data-stu-id="b0a9f-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="b0a9f-149">2. gads</span><span class="sxs-lookup"><span data-stu-id="b0a9f-149">Year 2</span></span> | <span data-ttu-id="b0a9f-150">(7000 – 1000) \* 30% = 1800</span><span class="sxs-lookup"><span data-stu-id="b0a9f-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="b0a9f-151">(7000 -1800) = 5200</span><span class="sxs-lookup"><span data-stu-id="b0a9f-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="b0a9f-152">3. gads</span><span class="sxs-lookup"><span data-stu-id="b0a9f-152">Year 3</span></span> | <span data-ttu-id="b0a9f-153">(5200 – 1000) \* 30% = 1260</span><span class="sxs-lookup"><span data-stu-id="b0a9f-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="b0a9f-154">(5200 - 1260) = 3940</span><span class="sxs-lookup"><span data-stu-id="b0a9f-154">(5,200 - 1,260) = 3,940</span></span>               |


-






