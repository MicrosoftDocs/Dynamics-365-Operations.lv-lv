---
title: Procentu likmju iestatīšana interešu kodam
description: Procentu kodi satur iestatījumus, kas nosaka, kad procenti tiek aprēķināti un kā tie tiek aprēķināti nokavētiem kontiem.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ca43503ecbe8e814958576e46ced10bfe9ad49
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188997"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="b08d8-103">Procentu likmju iestatīšana interešu kodam</span><span class="sxs-lookup"><span data-stu-id="b08d8-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b08d8-104">Procentu kodi satur iestatījumus, kas nosaka, kad procenti tiek aprēķināti un kā tie tiek aprēķināti nokavētiem kontiem.</span><span class="sxs-lookup"><span data-stu-id="b08d8-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="b08d8-105">Varat iestatīt vienu procentu kodu un piemērot to vairākiem debitora grāmatošanas profiliem, norēķinu kodiem vai noteiktām rēķina rindām.</span><span class="sxs-lookup"><span data-stu-id="b08d8-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="b08d8-106">Mainoties procentu kodu detaļām, visas funkcijas, kuras lieto kodu, automātiski veiks izmaiņas jaunos darījumos.</span><span class="sxs-lookup"><span data-stu-id="b08d8-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="b08d8-107">Katram procentu kodam varat uzstādīt divu veidu likmes.</span><span class="sxs-lookup"><span data-stu-id="b08d8-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="b08d8-108">Likmes procentu ieņēmumiem — tie ir ieņēmumi, kas ir nopelnīti, iekasējot procentus no rēķiniem vai rēķinu paziņojumiem.</span><span class="sxs-lookup"><span data-stu-id="b08d8-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="b08d8-109">Likmes procentu maksājumiem — tie pārstāv izmaksas, kas ir samaksāti par procentiem kredīta notās.</span><span class="sxs-lookup"><span data-stu-id="b08d8-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="b08d8-110">Abi šie likmju veidi var eksistēt vienlaicīgi vienā un tajā pašā procentu kodā.</span><span class="sxs-lookup"><span data-stu-id="b08d8-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="b08d8-111">Procentu likmes pamatā var būt trīs aprēķinu veidi.</span><span class="sxs-lookup"><span data-stu-id="b08d8-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="b08d8-112">Procentu likme pēc procentuālā daudzuma.</span><span class="sxs-lookup"><span data-stu-id="b08d8-112">Interest by percentage.</span></span>
-   <span data-ttu-id="b08d8-113">Procentu likme pēc summas.</span><span class="sxs-lookup"><span data-stu-id="b08d8-113">Interest by amount.</span></span>
-   <span data-ttu-id="b08d8-114">Procentu likme pēc diapazona, kas ir izteikts kā viens procentuāls daudzums vai summa.</span><span class="sxs-lookup"><span data-stu-id="b08d8-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="b08d8-115">Kad procentu kods tiek izmantots, lai aprēķinātu procentus, tiek izveidots atsevišķs procentu paziņojums katrai procentu likmei, kas ir spēkā laika posmā, kad maksājums pārsniedz darījuma apmaksas datumu.</span><span class="sxs-lookup"><span data-stu-id="b08d8-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="b08d8-116">Izmantojiet cilni **Ienākumi** lapā **Procentu kods**, lai iestatītu procentu likmes procentiem, ko nopelnāt, iekasējot procentus.</span><span class="sxs-lookup"><span data-stu-id="b08d8-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="b08d8-117">Izmantojiet cilni **Maksājumi**, lai iestatītu procentu likmes tiem procentiem, ko maksājat jūs.</span><span class="sxs-lookup"><span data-stu-id="b08d8-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="b08d8-118">Uz procentuālu daudzumu balstītas procentu likmes</span><span class="sxs-lookup"><span data-stu-id="b08d8-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="b08d8-119">Varat iestatīt procentu likmes, kas aprēķina noteiktu procentu.</span><span class="sxs-lookup"><span data-stu-id="b08d8-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="b08d8-120">Procentu summa attiecas uz visām valūtām.</span><span class="sxs-lookup"><span data-stu-id="b08d8-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="b08d8-121">Iespējams ievadīt neobligātus procentu summas ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="b08d8-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="b08d8-122">Vienums <strong>Procenti</strong> ir atlasīts laukā <strong>Aprēķināt procentus, pamatojoties uz</strong>, kurš atrodas lapā <strong>Iestatīt procentu kodus</strong>.</span><span class="sxs-lookup"><span data-stu-id="b08d8-122"><strong>Percentage</strong> is selected\*\* <strong>in the \*\*Calculate interest based on</strong> field on the <strong>Set up Interest codes</strong> page.</span></span>

<span data-ttu-id="b08d8-123">Piemēram, lai iestatītu procentu kodu, kas novērtē 5 procentu soda naudu par katriem diviem mēnešiem, kuros rēķina maksājums pārsniedz transakcijas izpildes datumu, laukā **Aprēķināt procentus ik pēc šāda laikposma** ir jāievada 2 un jāatlasa **Mēnesis**.</span><span class="sxs-lookup"><span data-stu-id="b08d8-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="b08d8-124">Uz summām balstītas procentu likmes</span><span class="sxs-lookup"><span data-stu-id="b08d8-124">Interest rates based on amounts</span></span>
<span data-ttu-id="b08d8-125">Varat iestatīt procentu likmes, kas aprēķina norādīto summu pēc valūtām.</span><span class="sxs-lookup"><span data-stu-id="b08d8-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="b08d8-126">Procentu summa tiek norādīta katrai valūtai procentu kodā.</span><span class="sxs-lookup"><span data-stu-id="b08d8-126">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="b08d8-127">Iespējams ievadīt neobligātus procentu summas ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="b08d8-127">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="b08d8-128">Vienums **Summa** ir atlasīts laukā **Aprēķināt procentus, pamatojoties uz**, kurš atrodas lapā **Iestatīt procentu kodus**.</span><span class="sxs-lookup"><span data-stu-id="b08d8-128">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="b08d8-129">Piemēram, lai iestatītu procentu kodu, kas novērtē 25,00 soda naudu par katrām 20 dienām, kurās rēķina maksājums pārsniedz transakcijas izpildes datumu, laukā **Aprēķināt procentus ik pēc šāda laikposma** ir jāievada 20 un ir jāatlasa vienums **Diena**.</span><span class="sxs-lookup"><span data-stu-id="b08d8-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="b08d8-130">Uz diapazoniem balstītas procentu likmes</span><span class="sxs-lookup"><span data-stu-id="b08d8-130">Interest rates based on ranges</span></span>
<span data-ttu-id="b08d8-131">Varat iestatīt procentu likmes, kas svārstās atkarībā no nokavētās maksājuma summas, nokavēto dienu skaita vai nokavēto mēnešu skaita.</span><span class="sxs-lookup"><span data-stu-id="b08d8-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="b08d8-132">Varat lietot cilni **Ieņēmumi pēc valūtas**, lai katrai valūtai definētu konkrētus procentu iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="b08d8-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="b08d8-133">Šeit jūs arī definējat diapazonu.</span><span class="sxs-lookup"><span data-stu-id="b08d8-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="b08d8-134">Izmantojiet pogu **Diapazoni**, lai pievienotu rindas, kas apzīmē diapazonus, kurus vēlaties iestatīt.</span><span class="sxs-lookup"><span data-stu-id="b08d8-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="b08d8-135">Vērtība **No** apzīmē diapazona sākumu, un skaitlis **Procentu vērtība** apzīmē procentuālu daudzumu vai summu, atkarībā no atlases laukā **Aprēķināt procentus, pamatojoties uz**, lapā **Iestatīt procentu kodus**.</span><span class="sxs-lookup"><span data-stu-id="b08d8-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="b08d8-136">1. piemērs: procenti pēc diapazona = summa</span><span class="sxs-lookup"><span data-stu-id="b08d8-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="b08d8-137">Iestatiet procentu kodu, kas novērtē procentus vienu reizi katrus trīs mēnešus, par kuriem rēķina maksājums pārsniedz darījuma izpildes datumu.</span><span class="sxs-lookup"><span data-stu-id="b08d8-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="b08d8-138">Aprēķini jābalsta uz soda naudas vērtību procentos saskaņā ar pakāpeniskajiem summu intervāliem.</span><span class="sxs-lookup"><span data-stu-id="b08d8-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="b08d8-139">Procentu vērtība būs 1 procents rēķina summām līdz 1000,00, 2 procenti summām no 1001,00 līdz 5000,00 un 3 procenti summām, kas lielākas par 5000,00.</span><span class="sxs-lookup"><span data-stu-id="b08d8-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="b08d8-140">Iestatiet procentu kodu lauku vērtības, kā tālāk norādīts.</span><span class="sxs-lookup"><span data-stu-id="b08d8-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="b08d8-141">**Lauka nosaukums**</span><span class="sxs-lookup"><span data-stu-id="b08d8-141">**Field name**</span></span>                  | <span data-ttu-id="b08d8-142">**Lauka vērtība**</span><span class="sxs-lookup"><span data-stu-id="b08d8-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="b08d8-143">**Soda naudas kods**</span><span class="sxs-lookup"><span data-stu-id="b08d8-143">**Interest code**</span></span>               | <span data-ttu-id="b08d8-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="b08d8-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="b08d8-145">**Aprēķināt procentus ik pēc šāda laikposma:**</span><span class="sxs-lookup"><span data-stu-id="b08d8-145">**Calculate interest every**</span></span>    | <span data-ttu-id="b08d8-146">3/Mēnesis</span><span class="sxs-lookup"><span data-stu-id="b08d8-146">3/Month</span></span>         |
| <span data-ttu-id="b08d8-147">**Procenti pēc diapazona**</span><span class="sxs-lookup"><span data-stu-id="b08d8-147">**Interest by range**</span></span>           | <span data-ttu-id="b08d8-148">Summa</span><span class="sxs-lookup"><span data-stu-id="b08d8-148">Amount</span></span>          |
| <span data-ttu-id="b08d8-149">**Aprēķināt procentus, pamatojoties uz**</span><span class="sxs-lookup"><span data-stu-id="b08d8-149">**Calculate interest based on**</span></span> | <span data-ttu-id="b08d8-150">Procenti</span><span class="sxs-lookup"><span data-stu-id="b08d8-150">Percentage</span></span>      |

<span data-ttu-id="b08d8-151">Iestatiet diapazona informāciju, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="b08d8-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="b08d8-152">**No vērtības**</span><span class="sxs-lookup"><span data-stu-id="b08d8-152">**From value**</span></span> | <span data-ttu-id="b08d8-153">**Procentu vērtība**</span><span class="sxs-lookup"><span data-stu-id="b08d8-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="b08d8-154">0</span><span class="sxs-lookup"><span data-stu-id="b08d8-154">0</span></span>              | <span data-ttu-id="b08d8-155">1.</span><span class="sxs-lookup"><span data-stu-id="b08d8-155">1</span></span>                  |
| <span data-ttu-id="b08d8-156">1,001</span><span class="sxs-lookup"><span data-stu-id="b08d8-156">1,001</span></span>          | <span data-ttu-id="b08d8-157">2.</span><span class="sxs-lookup"><span data-stu-id="b08d8-157">2</span></span>                  |
| <span data-ttu-id="b08d8-158">5,001</span><span class="sxs-lookup"><span data-stu-id="b08d8-158">5,001</span></span>          | <span data-ttu-id="b08d8-159">3.</span><span class="sxs-lookup"><span data-stu-id="b08d8-159">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="b08d8-160">2. piemērs: procenti pēc diapazona = dienas</span><span class="sxs-lookup"><span data-stu-id="b08d8-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="b08d8-161">Iestatiet procentu kodu, kas novērtē procentus vienu reizi katras 15 dienas, par kurām rēķina maksājums pārsniedz darījuma izpildes datumu.</span><span class="sxs-lookup"><span data-stu-id="b08d8-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="b08d8-162">Aprēķini jābalsta uz soda naudas vērtību summā saskaņā ar pakāpeniskajiem dienu intervāliem.</span><span class="sxs-lookup"><span data-stu-id="b08d8-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="b08d8-163">Procentu vērtība būs 10,00 15 dienas pirmajās 60 dienās, 15,00 15 dienas no 61 līdz 90 dienām, un 20,00 15 dienas, sākot no 91 dienas.</span><span class="sxs-lookup"><span data-stu-id="b08d8-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="b08d8-164">Iestatiet procentu kodu lauku vērtības, kā tālāk norādīts.</span><span class="sxs-lookup"><span data-stu-id="b08d8-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="b08d8-165">**Lauka nosaukums**</span><span class="sxs-lookup"><span data-stu-id="b08d8-165">**Field name**</span></span>                  | <span data-ttu-id="b08d8-166">**Lauka vērtība**</span><span class="sxs-lookup"><span data-stu-id="b08d8-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="b08d8-167">**Soda naudas kods**</span><span class="sxs-lookup"><span data-stu-id="b08d8-167">**Interest code**</span></span>               | <span data-ttu-id="b08d8-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="b08d8-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="b08d8-169">**Aprēķināt procentus ik pēc šāda laikposma:**</span><span class="sxs-lookup"><span data-stu-id="b08d8-169">**Calculate interest every**</span></span>    | <span data-ttu-id="b08d8-170">15/Diena</span><span class="sxs-lookup"><span data-stu-id="b08d8-170">15/Day</span></span>          |
| <span data-ttu-id="b08d8-171">**Procenti pēc diapazona**</span><span class="sxs-lookup"><span data-stu-id="b08d8-171">**Interest by range**</span></span>           | <span data-ttu-id="b08d8-172">Dienas</span><span class="sxs-lookup"><span data-stu-id="b08d8-172">Days</span></span>            |
| <span data-ttu-id="b08d8-173">**Aprēķināt procentus, pamatojoties uz**</span><span class="sxs-lookup"><span data-stu-id="b08d8-173">**Calculate interest based on**</span></span> | <span data-ttu-id="b08d8-174">Summa</span><span class="sxs-lookup"><span data-stu-id="b08d8-174">Amount</span></span>          |

<span data-ttu-id="b08d8-175">Iestatiet diapazona informāciju, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="b08d8-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="b08d8-176">**No vērtības**</span><span class="sxs-lookup"><span data-stu-id="b08d8-176">**From value**</span></span> | <span data-ttu-id="b08d8-177">**Procentu vērtība**</span><span class="sxs-lookup"><span data-stu-id="b08d8-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="b08d8-178">0</span><span class="sxs-lookup"><span data-stu-id="b08d8-178">0</span></span>              | <span data-ttu-id="b08d8-179">10.</span><span class="sxs-lookup"><span data-stu-id="b08d8-179">10</span></span>                 |
| <span data-ttu-id="b08d8-180">61</span><span class="sxs-lookup"><span data-stu-id="b08d8-180">61</span></span>             | <span data-ttu-id="b08d8-181">15.</span><span class="sxs-lookup"><span data-stu-id="b08d8-181">15</span></span>                 |
| <span data-ttu-id="b08d8-182">91</span><span class="sxs-lookup"><span data-stu-id="b08d8-182">91</span></span>             | <span data-ttu-id="b08d8-183">20.</span><span class="sxs-lookup"><span data-stu-id="b08d8-183">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="b08d8-184">3. piemērs: procenti pēc diapazona = mēneši</span><span class="sxs-lookup"><span data-stu-id="b08d8-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="b08d8-185">Iestatiet procentu kodu, kas novērtē procentus vienu reizi katru mēnesi, par kuru rēķina maksājums pārsniedz darījuma izpildes datumu.</span><span class="sxs-lookup"><span data-stu-id="b08d8-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="b08d8-186">Aprēķini jābalsta uz soda naudas vērtību procentos saskaņā ar pakāpeniskajiem mēnešu intervāliem.</span><span class="sxs-lookup"><span data-stu-id="b08d8-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="b08d8-187">Procentu vērtība būs 1,5 procenti mēnesī par pirmajiem trim nokavētajiem mēnešiem, 2,0 procenti mēnesī par nākamajiem trim mēnešiem un 2,5 procenti mēnesī pēc pirmajiem sešiem mēnešiem.</span><span class="sxs-lookup"><span data-stu-id="b08d8-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="b08d8-188">Iestatiet procentu kodu lauku vērtības, kā tālāk norādīts.</span><span class="sxs-lookup"><span data-stu-id="b08d8-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="b08d8-189">**Lauka nosaukums**</span><span class="sxs-lookup"><span data-stu-id="b08d8-189">**Field name**</span></span>                  | <span data-ttu-id="b08d8-190">**Lauka vērtība**</span><span class="sxs-lookup"><span data-stu-id="b08d8-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="b08d8-191">**Soda naudas kods**</span><span class="sxs-lookup"><span data-stu-id="b08d8-191">**Interest code**</span></span>               | <span data-ttu-id="b08d8-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="b08d8-192">1M%ByMth</span></span>        |
| <span data-ttu-id="b08d8-193">**Aprēķināt procentus ik pēc šāda laikposma:**</span><span class="sxs-lookup"><span data-stu-id="b08d8-193">**Calculate interest every**</span></span>    | <span data-ttu-id="b08d8-194">1/Mēnesis</span><span class="sxs-lookup"><span data-stu-id="b08d8-194">1/Month</span></span>         |
| <span data-ttu-id="b08d8-195">**Procenti pēc diapazona**</span><span class="sxs-lookup"><span data-stu-id="b08d8-195">**Interest by range**</span></span>           | <span data-ttu-id="b08d8-196">Mēneši</span><span class="sxs-lookup"><span data-stu-id="b08d8-196">Months</span></span>          |
| <span data-ttu-id="b08d8-197">**Aprēķināt procentus, pamatojoties uz**</span><span class="sxs-lookup"><span data-stu-id="b08d8-197">**Calculate interest based on**</span></span> | <span data-ttu-id="b08d8-198">Procenti</span><span class="sxs-lookup"><span data-stu-id="b08d8-198">Percentage</span></span>      |

<span data-ttu-id="b08d8-199">Iestatiet diapazona informāciju, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="b08d8-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="b08d8-200">**No vērtības**</span><span class="sxs-lookup"><span data-stu-id="b08d8-200">**From value**</span></span> | <span data-ttu-id="b08d8-201">**Procentu vērtība**</span><span class="sxs-lookup"><span data-stu-id="b08d8-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="b08d8-202">0</span><span class="sxs-lookup"><span data-stu-id="b08d8-202">0</span></span>              | <span data-ttu-id="b08d8-203">1.5</span><span class="sxs-lookup"><span data-stu-id="b08d8-203">1.5</span></span>                |
| <span data-ttu-id="b08d8-204">4.</span><span class="sxs-lookup"><span data-stu-id="b08d8-204">4</span></span>              | <span data-ttu-id="b08d8-205">2.</span><span class="sxs-lookup"><span data-stu-id="b08d8-205">2</span></span>                  |
| <span data-ttu-id="b08d8-206">7.</span><span class="sxs-lookup"><span data-stu-id="b08d8-206">7</span></span>              | <span data-ttu-id="b08d8-207">2,5</span><span class="sxs-lookup"><span data-stu-id="b08d8-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="b08d8-208">Jaunas versijas</span><span class="sxs-lookup"><span data-stu-id="b08d8-208">New versions</span></span>
<span data-ttu-id="b08d8-209">Procentu kodiem ir spēkā stāšanās datums.</span><span class="sxs-lookup"><span data-stu-id="b08d8-209">Interest codes are date effective.</span></span> <span data-ttu-id="b08d8-210">Ja procentu likmi vēlaties mainīt, varat izveidot **jaunu versiju**, kas ir spēkā no nākotnes datuma.</span><span class="sxs-lookup"><span data-stu-id="b08d8-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="b08d8-211">Lai skatītu citādas versijas, varat izmantot izvēlnes vienumu **No datuma**, lai atlasītu robeždatuma.</span><span class="sxs-lookup"><span data-stu-id="b08d8-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="b08d8-212">Varat arī atlasīt vienumu **Rādīt visus ierakstus**, lai skatītu visus procentu kodus lapā.</span><span class="sxs-lookup"><span data-stu-id="b08d8-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>



