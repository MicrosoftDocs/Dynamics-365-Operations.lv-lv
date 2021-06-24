---
title: Procentu likmju iestatīšana interešu kodam
description: Procentu kodi satur iestatījumus, kas nosaka, kad procenti tiek aprēķināti un kā tie tiek aprēķināti nokavētiem kontiem.
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc986ea752d1482f618401058f7a0b18f13efd5f
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188714"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="c5664-103">Procentu likmju iestatīšana interešu kodam</span><span class="sxs-lookup"><span data-stu-id="c5664-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5664-104">Procentu kodi satur iestatījumus, kas nosaka, kad procenti tiek aprēķināti un kā tie tiek aprēķināti nokavētiem kontiem.</span><span class="sxs-lookup"><span data-stu-id="c5664-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="c5664-105">Varat iestatīt vienu procentu kodu un piemērot to vairākiem debitora grāmatošanas profiliem, norēķinu kodiem vai noteiktām rēķina rindām.</span><span class="sxs-lookup"><span data-stu-id="c5664-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="c5664-106">Mainoties procentu kodu detaļām, visas funkcijas, kuras lieto kodu, automātiski veiks izmaiņas jaunos darījumos.</span><span class="sxs-lookup"><span data-stu-id="c5664-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="c5664-107">Katram procentu kodam varat uzstādīt divu veidu likmes.</span><span class="sxs-lookup"><span data-stu-id="c5664-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="c5664-108">Likmes procentu ieņēmumiem — tie ir ieņēmumi, kas ir nopelnīti, iekasējot procentus no rēķiniem vai rēķinu paziņojumiem.</span><span class="sxs-lookup"><span data-stu-id="c5664-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="c5664-109">Likmes procentu maksājumiem — tie pārstāv izmaksas, kas ir samaksāti par procentiem kredīta notās.</span><span class="sxs-lookup"><span data-stu-id="c5664-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="c5664-110">Abi šie likmju veidi var eksistēt vienlaicīgi vienā un tajā pašā procentu kodā.</span><span class="sxs-lookup"><span data-stu-id="c5664-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="c5664-111">Procentu likmes pamatā var būt trīs aprēķinu veidi.</span><span class="sxs-lookup"><span data-stu-id="c5664-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="c5664-112">Procentu likme pēc procentuālā daudzuma.</span><span class="sxs-lookup"><span data-stu-id="c5664-112">Interest by percentage.</span></span>
-   <span data-ttu-id="c5664-113">Procentu likme pēc summas.</span><span class="sxs-lookup"><span data-stu-id="c5664-113">Interest by amount.</span></span>
-   <span data-ttu-id="c5664-114">Procentu likme pēc diapazona, kas ir izteikts kā viens procentuāls daudzums vai summa.</span><span class="sxs-lookup"><span data-stu-id="c5664-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="c5664-115">Kad procentu kods tiek izmantots, lai aprēķinātu procentus, tiek izveidots atsevišķs procentu paziņojums katrai procentu likmei, kas ir spēkā laika posmā, kad maksājums pārsniedz darījuma apmaksas datumu.</span><span class="sxs-lookup"><span data-stu-id="c5664-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="c5664-116">Izmantojiet cilni **Ienākumi** lapā **Procentu kods**, lai iestatītu procentu likmes procentiem, ko nopelnāt, iekasējot procentus.</span><span class="sxs-lookup"><span data-stu-id="c5664-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="c5664-117">Izmantojiet cilni **Maksājumi**, lai iestatītu procentu likmes tiem procentiem, ko maksājat jūs.</span><span class="sxs-lookup"><span data-stu-id="c5664-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="c5664-118">Uz procentuālu daudzumu balstītas procentu likmes</span><span class="sxs-lookup"><span data-stu-id="c5664-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="c5664-119">Varat iestatīt procentu likmes, kas aprēķina noteiktu procentu.</span><span class="sxs-lookup"><span data-stu-id="c5664-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="c5664-120">Procentu summa attiecas uz visām valūtām.</span><span class="sxs-lookup"><span data-stu-id="c5664-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="c5664-121">Iespējams ievadīt neobligātus procentu summas ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="c5664-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="c5664-122">Vienums **Procenti** ir atlasīts laukā **Aprēķināt procentus, pamatojoties uz**, kurš atrodas lapā **Iestatīt procentu kodus**.</span><span class="sxs-lookup"><span data-stu-id="c5664-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="c5664-123">Piemēram, lai iestatītu procentu kodu, kas novērtē 5 procentu soda naudu par katriem diviem mēnešiem, kuros rēķina maksājums pārsniedz transakcijas izpildes datumu, laukā **Aprēķināt procentus ik pēc šāda laikposma** ir jāievada 2 un jāatlasa **Mēnesis**.</span><span class="sxs-lookup"><span data-stu-id="c5664-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="c5664-124">Jaunais algoritms procentu paziņojuma aprēķināšanai ir pievienots, izmantojot līdzekļu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="c5664-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="c5664-125">Lai lietotu šo algoritmu, iespējojiet līdzekli **(GBL) Ļauj aprēķināt procentus par dienu kā gada procentus, dalītus ar 365**.</span><span class="sxs-lookup"><span data-stu-id="c5664-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="c5664-126">Papildinformāciju par šā līdzekļa iespējošanu skatiet rakstā [Pārskats par līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c5664-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="c5664-127">Procentu paziņojuma summas aprēķina formula ir šāda:</span><span class="sxs-lookup"><span data-stu-id="c5664-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="c5664-128">Procentu paziņojuma summa = maksājamā summa \* gada procenti % / 365 \* nokavēto dienu skaits</span><span class="sxs-lookup"><span data-stu-id="c5664-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="c5664-129">Šis līdzeklis ir pieejams versijā 10.0.18 vai jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="c5664-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="c5664-130">Uz summām balstītas procentu likmes</span><span class="sxs-lookup"><span data-stu-id="c5664-130">Interest rates based on amounts</span></span>
<span data-ttu-id="c5664-131">Varat iestatīt procentu likmes, kas aprēķina norādīto summu pēc valūtām.</span><span class="sxs-lookup"><span data-stu-id="c5664-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="c5664-132">Procentu summa tiek norādīta katrai valūtai procentu kodā.</span><span class="sxs-lookup"><span data-stu-id="c5664-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="c5664-133">Iespējams ievadīt neobligātus procentu summas ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="c5664-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="c5664-134">Vienums **Summa** ir atlasīts laukā **Aprēķināt procentus, pamatojoties uz**, kurš atrodas lapā **Iestatīt procentu kodus**.</span><span class="sxs-lookup"><span data-stu-id="c5664-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="c5664-135">Piemēram, lai iestatītu procentu kodu, kas novērtē 25,00 soda naudu par katrām 20 dienām, kurās rēķina maksājums pārsniedz transakcijas izpildes datumu, laukā **Aprēķināt procentus ik pēc šāda laikposma** ir jāievada 20 un ir jāatlasa vienums **Diena**.</span><span class="sxs-lookup"><span data-stu-id="c5664-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="c5664-136">Uz diapazoniem balstītas procentu likmes</span><span class="sxs-lookup"><span data-stu-id="c5664-136">Interest rates based on ranges</span></span>
<span data-ttu-id="c5664-137">Varat iestatīt procentu likmes, kas svārstās atkarībā no nokavētās maksājuma summas, nokavēto dienu skaita vai nokavēto mēnešu skaita.</span><span class="sxs-lookup"><span data-stu-id="c5664-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="c5664-138">Varat lietot cilni **Ieņēmumi pēc valūtas**, lai katrai valūtai definētu konkrētus procentu iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="c5664-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="c5664-139">Šeit jūs arī definējat diapazonu.</span><span class="sxs-lookup"><span data-stu-id="c5664-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="c5664-140">Izmantojiet pogu **Diapazoni**, lai pievienotu rindas, kas apzīmē diapazonus, kurus vēlaties iestatīt.</span><span class="sxs-lookup"><span data-stu-id="c5664-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="c5664-141">Vērtība **No** apzīmē diapazona sākumu, un skaitlis **Procentu vērtība** apzīmē procentuālu daudzumu vai summu, atkarībā no atlases laukā **Aprēķināt procentus, pamatojoties uz**, lapā **Iestatīt procentu kodus**.</span><span class="sxs-lookup"><span data-stu-id="c5664-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="c5664-142">1. piemērs: procenti pēc diapazona = summa</span><span class="sxs-lookup"><span data-stu-id="c5664-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="c5664-143">Iestatiet procentu kodu, kas novērtē procentus vienu reizi katrus trīs mēnešus, par kuriem rēķina maksājums pārsniedz darījuma izpildes datumu.</span><span class="sxs-lookup"><span data-stu-id="c5664-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="c5664-144">Aprēķini jābalsta uz soda naudas vērtību procentos saskaņā ar pakāpeniskajiem summu intervāliem.</span><span class="sxs-lookup"><span data-stu-id="c5664-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="c5664-145">Procentu vērtība būs 1 procents rēķina summām līdz 1000,00, 2 procenti summām no 1001,00 līdz 5000,00 un 3 procenti summām, kas lielākas par 5000,00.</span><span class="sxs-lookup"><span data-stu-id="c5664-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="c5664-146">Iestatiet procentu kodu lauku vērtības, kā tālāk norādīts.</span><span class="sxs-lookup"><span data-stu-id="c5664-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="c5664-147">**Lauka nosaukums**</span><span class="sxs-lookup"><span data-stu-id="c5664-147">**Field name**</span></span>                  | <span data-ttu-id="c5664-148">**Lauka vērtība**</span><span class="sxs-lookup"><span data-stu-id="c5664-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="c5664-149">**Soda naudas kods**</span><span class="sxs-lookup"><span data-stu-id="c5664-149">**Interest code**</span></span>               | <span data-ttu-id="c5664-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="c5664-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="c5664-151">**Aprēķināt procentus ik pēc šāda laikposma:**</span><span class="sxs-lookup"><span data-stu-id="c5664-151">**Calculate interest every**</span></span>    | <span data-ttu-id="c5664-152">3/Mēnesis</span><span class="sxs-lookup"><span data-stu-id="c5664-152">3/Month</span></span>         |
| <span data-ttu-id="c5664-153">**Procenti pēc diapazona**</span><span class="sxs-lookup"><span data-stu-id="c5664-153">**Interest by range**</span></span>           | <span data-ttu-id="c5664-154">Summa</span><span class="sxs-lookup"><span data-stu-id="c5664-154">Amount</span></span>          |
| <span data-ttu-id="c5664-155">**Aprēķināt procentus, pamatojoties uz**</span><span class="sxs-lookup"><span data-stu-id="c5664-155">**Calculate interest based on**</span></span> | <span data-ttu-id="c5664-156">Procenti</span><span class="sxs-lookup"><span data-stu-id="c5664-156">Percentage</span></span>      |

<span data-ttu-id="c5664-157">Iestatiet diapazona informāciju, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="c5664-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="c5664-158">**No vērtības**</span><span class="sxs-lookup"><span data-stu-id="c5664-158">**From value**</span></span> | <span data-ttu-id="c5664-159">**Procentu vērtība**</span><span class="sxs-lookup"><span data-stu-id="c5664-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="c5664-160">0</span><span class="sxs-lookup"><span data-stu-id="c5664-160">0</span></span>              | <span data-ttu-id="c5664-161">1.</span><span class="sxs-lookup"><span data-stu-id="c5664-161">1</span></span>                  |
| <span data-ttu-id="c5664-162">1,001</span><span class="sxs-lookup"><span data-stu-id="c5664-162">1,001</span></span>          | <span data-ttu-id="c5664-163">2.</span><span class="sxs-lookup"><span data-stu-id="c5664-163">2</span></span>                  |
| <span data-ttu-id="c5664-164">5,001</span><span class="sxs-lookup"><span data-stu-id="c5664-164">5,001</span></span>          | <span data-ttu-id="c5664-165">3.</span><span class="sxs-lookup"><span data-stu-id="c5664-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="c5664-166">2. piemērs: procenti pēc diapazona = dienas</span><span class="sxs-lookup"><span data-stu-id="c5664-166">Example 2: Interest by range = Days</span></span>

<span data-ttu-id="c5664-167">Iestatiet procentu kodu, kas novērtē procentus vienu reizi katras 15 dienas, par kurām rēķina maksājums pārsniedz darījuma izpildes datumu.</span><span class="sxs-lookup"><span data-stu-id="c5664-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="c5664-168">Aprēķini jābalsta uz soda naudas vērtību summā saskaņā ar pakāpeniskajiem dienu intervāliem.</span><span class="sxs-lookup"><span data-stu-id="c5664-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="c5664-169">Procentu vērtība būs 10,00 15 dienas pirmajās 60 dienās, 15,00 15 dienas no 61 līdz 90 dienām, un 20,00 15 dienas, sākot no 91 dienas.</span><span class="sxs-lookup"><span data-stu-id="c5664-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="c5664-170">Iestatiet procentu kodu lauku vērtības, kā tālāk norādīts.</span><span class="sxs-lookup"><span data-stu-id="c5664-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="c5664-171">**Lauka nosaukums**</span><span class="sxs-lookup"><span data-stu-id="c5664-171">**Field name**</span></span>                  | <span data-ttu-id="c5664-172">**Lauka vērtība**</span><span class="sxs-lookup"><span data-stu-id="c5664-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="c5664-173">**Soda naudas kods**</span><span class="sxs-lookup"><span data-stu-id="c5664-173">**Interest code**</span></span>               | <span data-ttu-id="c5664-174">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="c5664-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="c5664-175">**Aprēķināt procentus ik pēc šāda laikposma:**</span><span class="sxs-lookup"><span data-stu-id="c5664-175">**Calculate interest every**</span></span>    | <span data-ttu-id="c5664-176">15/Diena</span><span class="sxs-lookup"><span data-stu-id="c5664-176">15/Day</span></span>          |
| <span data-ttu-id="c5664-177">**Procenti pēc diapazona**</span><span class="sxs-lookup"><span data-stu-id="c5664-177">**Interest by range**</span></span>           | <span data-ttu-id="c5664-178">Dienas</span><span class="sxs-lookup"><span data-stu-id="c5664-178">Days</span></span>            |
| <span data-ttu-id="c5664-179">**Aprēķināt procentus, pamatojoties uz**</span><span class="sxs-lookup"><span data-stu-id="c5664-179">**Calculate interest based on**</span></span> | <span data-ttu-id="c5664-180">Summa</span><span class="sxs-lookup"><span data-stu-id="c5664-180">Amount</span></span>          |

<span data-ttu-id="c5664-181">Iestatiet diapazona informāciju, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="c5664-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="c5664-182">**No vērtības**</span><span class="sxs-lookup"><span data-stu-id="c5664-182">**From value**</span></span> | <span data-ttu-id="c5664-183">**Procentu vērtība**</span><span class="sxs-lookup"><span data-stu-id="c5664-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="c5664-184">0</span><span class="sxs-lookup"><span data-stu-id="c5664-184">0</span></span>              | <span data-ttu-id="c5664-185">10.</span><span class="sxs-lookup"><span data-stu-id="c5664-185">10</span></span>                 |
| <span data-ttu-id="c5664-186">61</span><span class="sxs-lookup"><span data-stu-id="c5664-186">61</span></span>             | <span data-ttu-id="c5664-187">15.</span><span class="sxs-lookup"><span data-stu-id="c5664-187">15</span></span>                 |
| <span data-ttu-id="c5664-188">91</span><span class="sxs-lookup"><span data-stu-id="c5664-188">91</span></span>             | <span data-ttu-id="c5664-189">20.</span><span class="sxs-lookup"><span data-stu-id="c5664-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="c5664-190">3. piemērs: procenti pēc diapazona = mēneši</span><span class="sxs-lookup"><span data-stu-id="c5664-190">Example 3: Interest by range = Months</span></span>

<span data-ttu-id="c5664-191">Iestatiet procentu kodu, kas novērtē procentus vienu reizi katru mēnesi, par kuru rēķina maksājums pārsniedz darījuma izpildes datumu.</span><span class="sxs-lookup"><span data-stu-id="c5664-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="c5664-192">Aprēķini jābalsta uz soda naudas vērtību procentos saskaņā ar pakāpeniskajiem mēnešu intervāliem.</span><span class="sxs-lookup"><span data-stu-id="c5664-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="c5664-193">Procentu vērtība būs 1,5 procenti mēnesī par pirmajiem trim nokavētajiem mēnešiem, 2,0 procenti mēnesī par nākamajiem trim mēnešiem un 2,5 procenti mēnesī pēc pirmajiem sešiem mēnešiem.</span><span class="sxs-lookup"><span data-stu-id="c5664-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="c5664-194">Iestatiet procentu kodu lauku vērtības, kā tālāk norādīts.</span><span class="sxs-lookup"><span data-stu-id="c5664-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="c5664-195">**Lauka nosaukums**</span><span class="sxs-lookup"><span data-stu-id="c5664-195">**Field name**</span></span>                  | <span data-ttu-id="c5664-196">**Lauka vērtība**</span><span class="sxs-lookup"><span data-stu-id="c5664-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="c5664-197">**Soda naudas kods**</span><span class="sxs-lookup"><span data-stu-id="c5664-197">**Interest code**</span></span>               | <span data-ttu-id="c5664-198">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="c5664-198">1M%ByMth</span></span>        |
| <span data-ttu-id="c5664-199">**Aprēķināt procentus ik pēc šāda laikposma:**</span><span class="sxs-lookup"><span data-stu-id="c5664-199">**Calculate interest every**</span></span>    | <span data-ttu-id="c5664-200">1/Mēnesis</span><span class="sxs-lookup"><span data-stu-id="c5664-200">1/Month</span></span>         |
| <span data-ttu-id="c5664-201">**Procenti pēc diapazona**</span><span class="sxs-lookup"><span data-stu-id="c5664-201">**Interest by range**</span></span>           | <span data-ttu-id="c5664-202">Mēneši</span><span class="sxs-lookup"><span data-stu-id="c5664-202">Months</span></span>          |
| <span data-ttu-id="c5664-203">**Aprēķināt procentus, pamatojoties uz**</span><span class="sxs-lookup"><span data-stu-id="c5664-203">**Calculate interest based on**</span></span> | <span data-ttu-id="c5664-204">Procenti</span><span class="sxs-lookup"><span data-stu-id="c5664-204">Percentage</span></span>      |

<span data-ttu-id="c5664-205">Iestatiet diapazona informāciju, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="c5664-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="c5664-206">**No vērtības**</span><span class="sxs-lookup"><span data-stu-id="c5664-206">**From value**</span></span> | <span data-ttu-id="c5664-207">**Procentu vērtība**</span><span class="sxs-lookup"><span data-stu-id="c5664-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="c5664-208">0</span><span class="sxs-lookup"><span data-stu-id="c5664-208">0</span></span>              | <span data-ttu-id="c5664-209">1.5</span><span class="sxs-lookup"><span data-stu-id="c5664-209">1.5</span></span>                |
| <span data-ttu-id="c5664-210">4.</span><span class="sxs-lookup"><span data-stu-id="c5664-210">4</span></span>              | <span data-ttu-id="c5664-211">2.</span><span class="sxs-lookup"><span data-stu-id="c5664-211">2</span></span>                  |
| <span data-ttu-id="c5664-212">7.</span><span class="sxs-lookup"><span data-stu-id="c5664-212">7</span></span>              | <span data-ttu-id="c5664-213">2,5</span><span class="sxs-lookup"><span data-stu-id="c5664-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="c5664-214">Jaunas versijas</span><span class="sxs-lookup"><span data-stu-id="c5664-214">New versions</span></span>
<span data-ttu-id="c5664-215">Procentu kodiem ir spēkā stāšanās datums.</span><span class="sxs-lookup"><span data-stu-id="c5664-215">Interest codes are date effective.</span></span> <span data-ttu-id="c5664-216">Ja procentu likmi vēlaties mainīt, varat izveidot **jaunu versiju**, kas ir spēkā no nākotnes datuma.</span><span class="sxs-lookup"><span data-stu-id="c5664-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="c5664-217">Lai skatītu citādas versijas, varat izmantot izvēlnes vienumu **No datuma**, lai atlasītu robeždatuma.</span><span class="sxs-lookup"><span data-stu-id="c5664-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="c5664-218">Varat arī atlasīt vienumu **Rādīt visus ierakstus**, lai skatītu visus procentu kodus lapā.</span><span class="sxs-lookup"><span data-stu-id="c5664-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
