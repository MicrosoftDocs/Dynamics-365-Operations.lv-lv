---
title: Pieskaitāmo izmaksu aprēķins
description: Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc6ad48ef80aa01739129b59cc1133d0a1930f24
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759476"
---
# <a name="overhead-calculation"></a><span data-ttu-id="abbb6-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="abbb6-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="abbb6-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="abbb6-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="abbb6-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="abbb6-105">Term definition</span></span>
---------------

<span data-ttu-id="abbb6-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="abbb6-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="abbb6-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="abbb6-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="abbb6-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="abbb6-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="abbb6-109">Īre</span><span class="sxs-lookup"><span data-stu-id="abbb6-109">Rent</span></span>
-   <span data-ttu-id="abbb6-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-110">Electricity</span></span>
-   <span data-ttu-id="abbb6-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="abbb6-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="abbb6-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="abbb6-112">Overhead calculation overview</span></span>
<span data-ttu-id="abbb6-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="abbb6-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="abbb6-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="abbb6-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="abbb6-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="abbb6-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="abbb6-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="abbb6-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="abbb6-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="abbb6-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="abbb6-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="abbb6-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="abbb6-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="abbb6-119">Version type</span></span>
-   <span data-ttu-id="abbb6-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="abbb6-120">Date and time</span></span>
-   <span data-ttu-id="abbb6-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="abbb6-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="abbb6-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="abbb6-122">Fiscal year</span></span>
-   <span data-ttu-id="abbb6-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="abbb6-123">Fiscal period</span></span>

<span data-ttu-id="abbb6-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="abbb6-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="abbb6-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="abbb6-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="abbb6-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="abbb6-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="abbb6-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="abbb6-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="abbb6-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="abbb6-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="abbb6-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="abbb6-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="abbb6-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="abbb6-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="abbb6-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="abbb6-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="abbb6-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="abbb6-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="abbb6-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="abbb6-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="abbb6-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="abbb6-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="abbb6-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="abbb6-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="abbb6-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="abbb6-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="abbb6-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="abbb6-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="abbb6-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="abbb6-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="abbb6-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="abbb6-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="abbb6-140">Main account</span></span></th>
<th><span data-ttu-id="abbb6-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="abbb6-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="abbb6-143">CC099</span><span class="sxs-lookup"><span data-stu-id="abbb6-143">CC099</span></span></td>
<td><span data-ttu-id="abbb6-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="abbb6-144">Default cost center</span></span></td>
<td><span data-ttu-id="abbb6-145">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-145">10001</span></span></td>
<td><span data-ttu-id="abbb6-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-146">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="abbb6-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="abbb6-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="abbb6-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="abbb6-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="abbb6-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="abbb6-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="abbb6-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="abbb6-151">Define the cost behavior rule</span></span>

<span data-ttu-id="abbb6-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="abbb6-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="abbb6-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="abbb6-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="abbb6-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="abbb6-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="abbb6-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="abbb6-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="abbb6-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="abbb6-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="abbb6-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="abbb6-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="abbb6-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="abbb6-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="abbb6-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="abbb6-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="abbb6-160">Journal</span></span></th>
<th><span data-ttu-id="abbb6-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="abbb6-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="abbb6-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="abbb6-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="abbb6-163">Versija</span><span class="sxs-lookup"><span data-stu-id="abbb6-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-164">00001</span><span class="sxs-lookup"><span data-stu-id="abbb6-164">00001</span></span></td>
<td><span data-ttu-id="abbb6-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="abbb6-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="abbb6-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="abbb6-166">Fiscal</span></span></td>
<td><span data-ttu-id="abbb6-167">2017</span><span class="sxs-lookup"><span data-stu-id="abbb6-167">2017</span></span></td>
<td><span data-ttu-id="abbb6-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-168">Period 1</span></span></td>
<td><span data-ttu-id="abbb6-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="abbb6-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="abbb6-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="abbb6-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="abbb6-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="abbb6-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="abbb6-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="abbb6-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="abbb6-173">Cost element</span></span></th>
<th><span data-ttu-id="abbb6-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="abbb6-174">Cost behavior</span></span></th>
<th><span data-ttu-id="abbb6-175">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="abbb6-177">CC099</span><span class="sxs-lookup"><span data-stu-id="abbb6-177">CC099</span></span></td>
<td><span data-ttu-id="abbb6-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="abbb6-178">Default cost center</span></span></td>
<td><span data-ttu-id="abbb6-179">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-179">10001</span></span></td>
<td><span data-ttu-id="abbb6-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-180">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="abbb6-181">Unclassified</span></span></td>
<td><span data-ttu-id="abbb6-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="abbb6-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="abbb6-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="abbb6-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="abbb6-185">Cost element</span></span></th>
<th><span data-ttu-id="abbb6-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="abbb6-186">Cost behavior</span></span></th>
<th><span data-ttu-id="abbb6-187">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-187">Amount</span></span></th>
<th><span data-ttu-id="abbb6-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="abbb6-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-189">CC099</span><span class="sxs-lookup"><span data-stu-id="abbb6-189">CC099</span></span></td>
<td><span data-ttu-id="abbb6-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="abbb6-190">Default cost center</span></span></td>
<td><span data-ttu-id="abbb6-191">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-191">10001</span></span></td>
<td><span data-ttu-id="abbb6-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-192">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="abbb6-193">Unclassified</span></span></td>
<td><span data-ttu-id="abbb6-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-194">10,000.00</span></span></td>
<td><span data-ttu-id="abbb6-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-196">CC099</span><span class="sxs-lookup"><span data-stu-id="abbb6-196">CC099</span></span></td>
<td><span data-ttu-id="abbb6-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="abbb6-197">Default cost center</span></span></td>
<td><span data-ttu-id="abbb6-198">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-198">10001</span></span></td>
<td><span data-ttu-id="abbb6-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-199">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="abbb6-200">Unclassified</span></span></td>
<td><span data-ttu-id="abbb6-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-201">-10,000.00</span></span></td>
<td><span data-ttu-id="abbb6-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-203">CC099</span><span class="sxs-lookup"><span data-stu-id="abbb6-203">CC099</span></span></td>
<td><span data-ttu-id="abbb6-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="abbb6-204">Default cost center</span></span></td>
<td><span data-ttu-id="abbb6-205">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-205">10001</span></span></td>
<td><span data-ttu-id="abbb6-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-206">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-207">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-208">1,000.00</span></span></td>
<td><span data-ttu-id="abbb6-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-210">CC099</span><span class="sxs-lookup"><span data-stu-id="abbb6-210">CC099</span></span></td>
<td><span data-ttu-id="abbb6-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="abbb6-211">Default cost center</span></span></td>
<td><span data-ttu-id="abbb6-212">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-212">10001</span></span></td>
<td><span data-ttu-id="abbb6-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-213">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-214">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="abbb6-215">9,000.00</span></span></td>
<td><span data-ttu-id="abbb6-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abbb6-217">Sīkāku informāciju skatiet šeit: [Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="abbb6-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="abbb6-218">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="abbb6-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="abbb6-219">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="abbb6-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="abbb6-220">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="abbb6-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="abbb6-221">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="abbb6-221">Define the cost distribution rule</span></span>

<span data-ttu-id="abbb6-222">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="abbb6-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="abbb6-223">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="abbb6-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="abbb6-224">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="abbb6-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="abbb6-225">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="abbb6-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="abbb6-226">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="abbb6-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="abbb6-227">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="abbb6-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-228">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-228">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="abbb6-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-230">CC001</span><span class="sxs-lookup"><span data-stu-id="abbb6-230">CC001</span></span></td>
<td><span data-ttu-id="abbb6-231">HR</span><span class="sxs-lookup"><span data-stu-id="abbb6-231">HR</span></span></td>
<td><span data-ttu-id="abbb6-232">1000</span><span class="sxs-lookup"><span data-stu-id="abbb6-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-233">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-233">CC002</span></span></td>
<td><span data-ttu-id="abbb6-234">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-234">Finance</span></span></td>
<td><span data-ttu-id="abbb6-235">6,000</span><span class="sxs-lookup"><span data-stu-id="abbb6-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-236">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-236">CC003</span></span></td>
<td><span data-ttu-id="abbb6-237">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-237">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-238">0</span><span class="sxs-lookup"><span data-stu-id="abbb6-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abbb6-239">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="abbb6-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-240">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-240">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-241">Lielums</span><span class="sxs-lookup"><span data-stu-id="abbb6-241">Magnitude</span></span></th>
<th><span data-ttu-id="abbb6-242">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="abbb6-242">Allocation factor</span></span></th>
<th><span data-ttu-id="abbb6-243">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-244">CC001</span><span class="sxs-lookup"><span data-stu-id="abbb6-244">CC001</span></span></td>
<td><span data-ttu-id="abbb6-245">HR</span><span class="sxs-lookup"><span data-stu-id="abbb6-245">HR</span></span></td>
<td><span data-ttu-id="abbb6-246">1000</span><span class="sxs-lookup"><span data-stu-id="abbb6-246">1,000</span></span></td>
<td><span data-ttu-id="abbb6-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="abbb6-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="abbb6-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-249">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-249">CC002</span></span></td>
<td><span data-ttu-id="abbb6-250">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-250">Finance</span></span></td>
<td><span data-ttu-id="abbb6-251">6,000</span><span class="sxs-lookup"><span data-stu-id="abbb6-251">6,000</span></span></td>
<td><span data-ttu-id="abbb6-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="abbb6-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="abbb6-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-254">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-254">CC003</span></span></td>
<td><span data-ttu-id="abbb6-255">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-255">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-256">0</span><span class="sxs-lookup"><span data-stu-id="abbb6-256">0</span></span></td>
<td><span data-ttu-id="abbb6-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="abbb6-258">0,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abbb6-259">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="abbb6-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="abbb6-260">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="abbb6-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-261">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-261">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-262">Formula</span><span class="sxs-lookup"><span data-stu-id="abbb6-262">Formula</span></span></th>
<th><span data-ttu-id="abbb6-263">Lielums</span><span class="sxs-lookup"><span data-stu-id="abbb6-263">Magnitude</span></span></th>
<th><span data-ttu-id="abbb6-264">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="abbb6-264">Allocation factor</span></span></th>
<th><span data-ttu-id="abbb6-265">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-266">CC001</span><span class="sxs-lookup"><span data-stu-id="abbb6-266">CC001</span></span></td>
<td><span data-ttu-id="abbb6-267">HR</span><span class="sxs-lookup"><span data-stu-id="abbb6-267">HR</span></span></td>
<td><span data-ttu-id="abbb6-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="abbb6-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="abbb6-269">1.</span><span class="sxs-lookup"><span data-stu-id="abbb6-269">1</span></span></td>
<td><span data-ttu-id="abbb6-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="abbb6-271">500,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-272">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-272">CC002</span></span></td>
<td><span data-ttu-id="abbb6-273">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-273">Finance</span></span></td>
<td><span data-ttu-id="abbb6-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="abbb6-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="abbb6-275">1.</span><span class="sxs-lookup"><span data-stu-id="abbb6-275">1</span></span></td>
<td><span data-ttu-id="abbb6-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="abbb6-277">500,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-278">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-278">CC003</span></span></td>
<td><span data-ttu-id="abbb6-279">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-279">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="abbb6-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="abbb6-281">0</span><span class="sxs-lookup"><span data-stu-id="abbb6-281">0</span></span></td>
<td><span data-ttu-id="abbb6-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="abbb6-283">0,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="abbb6-284">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="abbb6-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="abbb6-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="abbb6-285">Journal</span></span></th>
<th><span data-ttu-id="abbb6-286">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="abbb6-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="abbb6-287">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="abbb6-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="abbb6-288">Versija</span><span class="sxs-lookup"><span data-stu-id="abbb6-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-289">00002</span><span class="sxs-lookup"><span data-stu-id="abbb6-289">00002</span></span></td>
<td><span data-ttu-id="abbb6-290">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="abbb6-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="abbb6-291">Finanšu</span><span class="sxs-lookup"><span data-stu-id="abbb6-291">Fiscal</span></span></td>
<td><span data-ttu-id="abbb6-292">2017</span><span class="sxs-lookup"><span data-stu-id="abbb6-292">2017</span></span></td>
<td><span data-ttu-id="abbb6-293">Periods 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-293">Period 1</span></span></td>
<td><span data-ttu-id="abbb6-294">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="abbb6-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="abbb6-295">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="abbb6-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="abbb6-296">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="abbb6-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="abbb6-297">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="abbb6-298">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="abbb6-298">Cost element</span></span></th>
<th><span data-ttu-id="abbb6-299">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="abbb6-299">Cost behavior</span></span></th>
<th><span data-ttu-id="abbb6-300">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-301">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-302">CC099</span><span class="sxs-lookup"><span data-stu-id="abbb6-302">CC099</span></span></td>
<td><span data-ttu-id="abbb6-303">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="abbb6-303">Default cost center</span></span></td>
<td><span data-ttu-id="abbb6-304">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-304">10001</span></span></td>
<td><span data-ttu-id="abbb6-305">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-305">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-306">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-306">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-308">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-309">CC099</span><span class="sxs-lookup"><span data-stu-id="abbb6-309">CC099</span></span></td>
<td><span data-ttu-id="abbb6-310">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="abbb6-310">Default cost center</span></span></td>
<td><span data-ttu-id="abbb6-311">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-311">10001</span></span></td>
<td><span data-ttu-id="abbb6-312">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-312">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-313">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-313">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="abbb6-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="abbb6-315">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="abbb6-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-316">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="abbb6-317">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="abbb6-317">Cost element</span></span></th>
<th><span data-ttu-id="abbb6-318">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="abbb6-318">Cost behavior</span></span></th>
<th><span data-ttu-id="abbb6-319">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-319">Amount</span></span></th>
<th><span data-ttu-id="abbb6-320">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="abbb6-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-321">CC099</span><span class="sxs-lookup"><span data-stu-id="abbb6-321">CC099</span></span></td>
<td><span data-ttu-id="abbb6-322">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="abbb6-322">Default cost center</span></span></td>
<td><span data-ttu-id="abbb6-323">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-323">10001</span></span></td>
<td><span data-ttu-id="abbb6-324">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-324">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-325">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-325">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-326">-1000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-326">-1,000.00</span></span></td>
<td><span data-ttu-id="abbb6-327">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-328">CC001</span><span class="sxs-lookup"><span data-stu-id="abbb6-328">CC001</span></span></td>
<td><span data-ttu-id="abbb6-329">HR</span><span class="sxs-lookup"><span data-stu-id="abbb6-329">HR</span></span></td>
<td><span data-ttu-id="abbb6-330">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-330">10001</span></span></td>
<td><span data-ttu-id="abbb6-331">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-331">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-332">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-332">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-333">500,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-333">500.00</span></span></td>
<td><span data-ttu-id="abbb6-334">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-335">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-335">CC002</span></span></td>
<td><span data-ttu-id="abbb6-336">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-336">Finance</span></span></td>
<td><span data-ttu-id="abbb6-337">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-337">10001</span></span></td>
<td><span data-ttu-id="abbb6-338">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-338">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-339">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-339">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-340">500,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-340">500.00</span></span></td>
<td><span data-ttu-id="abbb6-341">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-342">CC099</span><span class="sxs-lookup"><span data-stu-id="abbb6-342">CC099</span></span></td>
<td><span data-ttu-id="abbb6-343">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="abbb6-343">Default cost center</span></span></td>
<td><span data-ttu-id="abbb6-344">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-344">10001</span></span></td>
<td><span data-ttu-id="abbb6-345">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-345">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-346">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-346">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-347">-9,000.00</span></span></td>
<td><span data-ttu-id="abbb6-348">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-349">CC001</span><span class="sxs-lookup"><span data-stu-id="abbb6-349">CC001</span></span></td>
<td><span data-ttu-id="abbb6-350">HR</span><span class="sxs-lookup"><span data-stu-id="abbb6-350">HR</span></span></td>
<td><span data-ttu-id="abbb6-351">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-351">10001</span></span></td>
<td><span data-ttu-id="abbb6-352">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-352">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-353">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-353">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="abbb6-354">1,285.71</span></span></td>
<td><span data-ttu-id="abbb6-355">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-356">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-356">CC002</span></span></td>
<td><span data-ttu-id="abbb6-357">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-357">Finance</span></span></td>
<td><span data-ttu-id="abbb6-358">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-358">10001</span></span></td>
<td><span data-ttu-id="abbb6-359">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-359">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-360">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-360">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="abbb6-361">7,714.29</span></span></td>
<td><span data-ttu-id="abbb6-362">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abbb6-363">Sīkāku informāciju skatiet šeit: [Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="abbb6-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="abbb6-364">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="abbb6-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="abbb6-365">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="abbb6-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="abbb6-366">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="abbb6-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="abbb6-367">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="abbb6-367">Define the overhead rate</span></span>

<span data-ttu-id="abbb6-368">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="abbb6-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="abbb6-369">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="abbb6-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-370">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-370">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-371">Stundas</span><span class="sxs-lookup"><span data-stu-id="abbb6-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-372">Proj 1</span></span></td>
<td><span data-ttu-id="abbb6-373">1. projekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-373">Project 1</span></span></td>
<td><span data-ttu-id="abbb6-374">3.</span><span class="sxs-lookup"><span data-stu-id="abbb6-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-375">Proj 2</span></span></td>
<td><span data-ttu-id="abbb6-376">2. projekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-376">Project 2</span></span></td>
<td><span data-ttu-id="abbb6-377">1.</span><span class="sxs-lookup"><span data-stu-id="abbb6-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abbb6-378">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="abbb6-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-379">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-379">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-380">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="abbb6-380">Cost element</span></span></th>
<th><span data-ttu-id="abbb6-381">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="abbb6-381">Cost behavior</span></span></th>
<th><span data-ttu-id="abbb6-382">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="abbb6-382">Units</span></span></th>
<th><span data-ttu-id="abbb6-383">Likme</span><span class="sxs-lookup"><span data-stu-id="abbb6-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-384">CC001</span><span class="sxs-lookup"><span data-stu-id="abbb6-384">CC001</span></span></td>
<td><span data-ttu-id="abbb6-385">HR</span><span class="sxs-lookup"><span data-stu-id="abbb6-385">HR</span></span></td>
<td><span data-ttu-id="abbb6-386">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-386">10001</span></span></td>
<td><span data-ttu-id="abbb6-387">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-387">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-388">1</span><span class="sxs-lookup"><span data-stu-id="abbb6-388">1</span></span></td>
<td><span data-ttu-id="abbb6-389">10</span><span class="sxs-lookup"><span data-stu-id="abbb6-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abbb6-390">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="abbb6-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-391">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-391">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-392">Lielums</span><span class="sxs-lookup"><span data-stu-id="abbb6-392">Magnitude</span></span></th>
<th><span data-ttu-id="abbb6-393">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="abbb6-393">Cost element</span></span></th>
<th><span data-ttu-id="abbb6-394">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="abbb6-394">Allocation factor</span></span></th>
<th><span data-ttu-id="abbb6-395">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-396">Proj 1</span></span></td>
<td><span data-ttu-id="abbb6-397">1. projekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-397">Project 1</span></span></td>
<td><span data-ttu-id="abbb6-398">3.</span><span class="sxs-lookup"><span data-stu-id="abbb6-398">3</span></span></td>
<td><span data-ttu-id="abbb6-399">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-399">10001</span></span></td>
<td><span data-ttu-id="abbb6-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="abbb6-401">30,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-402">Proj 2</span></span></td>
<td><span data-ttu-id="abbb6-403">2. projekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-403">Project 2</span></span></td>
<td><span data-ttu-id="abbb6-404">1.</span><span class="sxs-lookup"><span data-stu-id="abbb6-404">1</span></span></td>
<td><span data-ttu-id="abbb6-405">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-405">10001</span></span></td>
<td><span data-ttu-id="abbb6-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="abbb6-407">10,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="abbb6-408">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="abbb6-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="abbb6-409">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="abbb6-409">Journal</span></span></th>
<th><span data-ttu-id="abbb6-410">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="abbb6-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="abbb6-411">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="abbb6-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="abbb6-412">Versija</span><span class="sxs-lookup"><span data-stu-id="abbb6-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-413">00003</span><span class="sxs-lookup"><span data-stu-id="abbb6-413">00003</span></span></td>
<td><span data-ttu-id="abbb6-414">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="abbb6-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="abbb6-415">Finanšu</span><span class="sxs-lookup"><span data-stu-id="abbb6-415">Fiscal</span></span></td>
<td><span data-ttu-id="abbb6-416">2017</span><span class="sxs-lookup"><span data-stu-id="abbb6-416">2017</span></span></td>
<td><span data-ttu-id="abbb6-417">Periods 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-417">Period 1</span></span></td>
<td><span data-ttu-id="abbb6-418">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="abbb6-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="abbb6-419">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="abbb6-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="abbb6-420">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="abbb6-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="abbb6-421">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-421">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-422">Lielums</span><span class="sxs-lookup"><span data-stu-id="abbb6-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-423">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-424">Proj 1</span></span></td>
<td><span data-ttu-id="abbb6-425">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="abbb6-426">3,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-427">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-428">Proj 2</span></span></td>
<td><span data-ttu-id="abbb6-429">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="abbb6-430">1,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="abbb6-431">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="abbb6-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-432">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="abbb6-433">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="abbb6-433">Cost element</span></span></th>
<th><span data-ttu-id="abbb6-434">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="abbb6-434">Cost behavior</span></span></th>
<th><span data-ttu-id="abbb6-435">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-435">Amount</span></span></th>
<th><span data-ttu-id="abbb6-436">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="abbb6-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="abbb6-437">CC0001</span></span></td>
<td><span data-ttu-id="abbb6-438">HR</span><span class="sxs-lookup"><span data-stu-id="abbb6-438">HR</span></span></td>
<td><span data-ttu-id="abbb6-439">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-439">10001</span></span></td>
<td><span data-ttu-id="abbb6-440">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-440">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-441">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-441">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-442">-30.00</span></span></td>
<td><span data-ttu-id="abbb6-443">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-444">Proj 1</span></span></td>
<td><span data-ttu-id="abbb6-445">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="abbb6-446">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-446">10001</span></span></td>
<td><span data-ttu-id="abbb6-447">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-447">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-448">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-448">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-449">30,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-449">30.00</span></span></td>
<td><span data-ttu-id="abbb6-450">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-451">CC001</span><span class="sxs-lookup"><span data-stu-id="abbb6-451">CC001</span></span></td>
<td><span data-ttu-id="abbb6-452">HR</span><span class="sxs-lookup"><span data-stu-id="abbb6-452">HR</span></span></td>
<td><span data-ttu-id="abbb6-453">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-453">10001</span></span></td>
<td><span data-ttu-id="abbb6-454">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-454">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-455">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-455">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-456">-10.00</span></span></td>
<td><span data-ttu-id="abbb6-457">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-458">Proj 2</span></span></td>
<td><span data-ttu-id="abbb6-459">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="abbb6-460">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-460">10001</span></span></td>
<td><span data-ttu-id="abbb6-461">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-461">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-462">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-462">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-463">10,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-463">10.00</span></span></td>
<td><span data-ttu-id="abbb6-464">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abbb6-465">Sīkāku informāciju skatiet šeit: [Pieskaitāmo izmaksu aprēķina veikšana](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="abbb6-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="abbb6-466">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="abbb6-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="abbb6-467">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="abbb6-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="abbb6-468">Finance atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="abbb6-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="abbb6-469">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="abbb6-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="abbb6-470">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="abbb6-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="abbb6-471">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="abbb6-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="abbb6-472">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="abbb6-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="abbb6-473">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="abbb6-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="abbb6-474">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="abbb6-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="abbb6-475">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="abbb6-475">Define the cost allocation</span></span>

<span data-ttu-id="abbb6-476">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="abbb6-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="abbb6-477">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="abbb6-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="abbb6-478">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="abbb6-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-479">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-479">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-480">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="abbb6-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-481">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-481">CC002</span></span></td>
<td><span data-ttu-id="abbb6-482">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-482">Finance</span></span></td>
<td><span data-ttu-id="abbb6-483">35</span><span class="sxs-lookup"><span data-stu-id="abbb6-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-484">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-484">CC003</span></span></td>
<td><span data-ttu-id="abbb6-485">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-485">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-486">55</span><span class="sxs-lookup"><span data-stu-id="abbb6-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-487">CC004</span><span class="sxs-lookup"><span data-stu-id="abbb6-487">CC004</span></span></td>
<td><span data-ttu-id="abbb6-488">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="abbb6-488">Packaging</span></span></td>
<td><span data-ttu-id="abbb6-489">10.</span><span class="sxs-lookup"><span data-stu-id="abbb6-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abbb6-490">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="abbb6-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="abbb6-491">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="abbb6-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-492">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-492">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-493">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="abbb6-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-494">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-494">CC003</span></span></td>
<td><span data-ttu-id="abbb6-495">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-495">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-496">65</span><span class="sxs-lookup"><span data-stu-id="abbb6-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-497">CC004</span><span class="sxs-lookup"><span data-stu-id="abbb6-497">CC004</span></span></td>
<td><span data-ttu-id="abbb6-498">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="abbb6-498">Packaging</span></span></td>
<td><span data-ttu-id="abbb6-499">35</span><span class="sxs-lookup"><span data-stu-id="abbb6-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abbb6-500">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="abbb6-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="abbb6-501">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="abbb6-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-502">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-502">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-503">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="abbb6-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-504">Prod 1</span></span></td>
<td><span data-ttu-id="abbb6-505">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-505">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-506">60</span><span class="sxs-lookup"><span data-stu-id="abbb6-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-507">Prod 2</span></span></td>
<td><span data-ttu-id="abbb6-508">2. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-508">Product 2</span></span></td>
<td><span data-ttu-id="abbb6-509">20</span><span class="sxs-lookup"><span data-stu-id="abbb6-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abbb6-510">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="abbb6-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="abbb6-511">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="abbb6-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-512">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-512">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-513">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="abbb6-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-514">Prod 1</span></span></td>
<td><span data-ttu-id="abbb6-515">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-515">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-516">80</span><span class="sxs-lookup"><span data-stu-id="abbb6-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-517">Prod 2</span></span></td>
<td><span data-ttu-id="abbb6-518">2. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-518">Product 2</span></span></td>
<td><span data-ttu-id="abbb6-519">15</span><span class="sxs-lookup"><span data-stu-id="abbb6-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="abbb6-520">Statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="abbb6-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="abbb6-521">Sīkāku informāciju skatiet šeit: [Statistikas mēru nodrošinātāja veidne](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="abbb6-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="abbb6-522">Nākamajā tabulā ir parādīts rezultāts, ja tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījuma pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="abbb6-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-523">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-523">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-524">Lielums</span><span class="sxs-lookup"><span data-stu-id="abbb6-524">Magnitude</span></span></th>
<th><span data-ttu-id="abbb6-525">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="abbb6-525">Allocation factor</span></span></th>
<th><span data-ttu-id="abbb6-526">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-526">Amount</span></span></th>
<th><span data-ttu-id="abbb6-527">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="abbb6-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-528">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-528">CC002</span></span></td>
<td><span data-ttu-id="abbb6-529">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-529">Finance</span></span></td>
<td><span data-ttu-id="abbb6-530">35</span><span class="sxs-lookup"><span data-stu-id="abbb6-530">35</span></span></td>
<td><span data-ttu-id="abbb6-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="abbb6-532">175.00</span><span class="sxs-lookup"><span data-stu-id="abbb6-532">175.00</span></span></td>
<td><span data-ttu-id="abbb6-533">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-534">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-534">CC003</span></span></td>
<td><span data-ttu-id="abbb6-535">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-535">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-536">55</span><span class="sxs-lookup"><span data-stu-id="abbb6-536">55</span></span></td>
<td><span data-ttu-id="abbb6-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="abbb6-538">275.00</span><span class="sxs-lookup"><span data-stu-id="abbb6-538">275.00</span></span></td>
<td><span data-ttu-id="abbb6-539">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-540">CC004</span><span class="sxs-lookup"><span data-stu-id="abbb6-540">CC004</span></span></td>
<td><span data-ttu-id="abbb6-541">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="abbb6-541">Packaging</span></span></td>
<td><span data-ttu-id="abbb6-542">10.</span><span class="sxs-lookup"><span data-stu-id="abbb6-542">10</span></span></td>
<td><span data-ttu-id="abbb6-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="abbb6-544">50,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-544">50.00</span></span></td>
<td><span data-ttu-id="abbb6-545">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-546">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-546">CC002</span></span></td>
<td><span data-ttu-id="abbb6-547">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-547">Finance</span></span></td>
<td><span data-ttu-id="abbb6-548">35</span><span class="sxs-lookup"><span data-stu-id="abbb6-548">35</span></span></td>
<td><span data-ttu-id="abbb6-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="abbb6-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="abbb6-550">436.00</span><span class="sxs-lookup"><span data-stu-id="abbb6-550">436.00</span></span></td>
<td><span data-ttu-id="abbb6-551">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-552">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-552">CC003</span></span></td>
<td><span data-ttu-id="abbb6-553">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-553">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-554">55</span><span class="sxs-lookup"><span data-stu-id="abbb6-554">55</span></span></td>
<td><span data-ttu-id="abbb6-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="abbb6-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="abbb6-556">685.14</span><span class="sxs-lookup"><span data-stu-id="abbb6-556">685.14</span></span></td>
<td><span data-ttu-id="abbb6-557">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-558">CC004</span><span class="sxs-lookup"><span data-stu-id="abbb6-558">CC004</span></span></td>
<td><span data-ttu-id="abbb6-559">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="abbb6-559">Packaging</span></span></td>
<td><span data-ttu-id="abbb6-560">10.</span><span class="sxs-lookup"><span data-stu-id="abbb6-560">10</span></span></td>
<td><span data-ttu-id="abbb6-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="abbb6-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="abbb6-562">124.57</span><span class="sxs-lookup"><span data-stu-id="abbb6-562">124.57</span></span></td>
<td><span data-ttu-id="abbb6-563">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abbb6-564">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="abbb6-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-565">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-565">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-566">Lielums</span><span class="sxs-lookup"><span data-stu-id="abbb6-566">Magnitude</span></span></th>
<th><span data-ttu-id="abbb6-567">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="abbb6-567">Allocation factor</span></span></th>
<th><span data-ttu-id="abbb6-568">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-568">Amount</span></span></th>
<th><span data-ttu-id="abbb6-569">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="abbb6-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-570">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-570">CC003</span></span></td>
<td><span data-ttu-id="abbb6-571">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-571">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-572">65</span><span class="sxs-lookup"><span data-stu-id="abbb6-572">65</span></span></td>
<td><span data-ttu-id="abbb6-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="abbb6-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="abbb6-574">438.75</span><span class="sxs-lookup"><span data-stu-id="abbb6-574">438.75</span></span></td>
<td><span data-ttu-id="abbb6-575">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-576">CC004</span><span class="sxs-lookup"><span data-stu-id="abbb6-576">CC004</span></span></td>
<td><span data-ttu-id="abbb6-577">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="abbb6-577">Packaging</span></span></td>
<td><span data-ttu-id="abbb6-578">35</span><span class="sxs-lookup"><span data-stu-id="abbb6-578">35</span></span></td>
<td><span data-ttu-id="abbb6-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="abbb6-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="abbb6-580">236.25</span><span class="sxs-lookup"><span data-stu-id="abbb6-580">236.25</span></span></td>
<td><span data-ttu-id="abbb6-581">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-582">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-582">CC003</span></span></td>
<td><span data-ttu-id="abbb6-583">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-583">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-584">65</span><span class="sxs-lookup"><span data-stu-id="abbb6-584">65</span></span></td>
<td><span data-ttu-id="abbb6-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="abbb6-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="abbb6-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="abbb6-586">5,297.69</span></span></td>
<td><span data-ttu-id="abbb6-587">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-588">CC004</span><span class="sxs-lookup"><span data-stu-id="abbb6-588">CC004</span></span></td>
<td><span data-ttu-id="abbb6-589">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="abbb6-589">Packaging</span></span></td>
<td><span data-ttu-id="abbb6-590">35</span><span class="sxs-lookup"><span data-stu-id="abbb6-590">35</span></span></td>
<td><span data-ttu-id="abbb6-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="abbb6-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="abbb6-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="abbb6-592">2,852.60</span></span></td>
<td><span data-ttu-id="abbb6-593">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abbb6-594">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="abbb6-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-595">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-595">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-596">Lielums</span><span class="sxs-lookup"><span data-stu-id="abbb6-596">Magnitude</span></span></th>
<th><span data-ttu-id="abbb6-597">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="abbb6-597">Allocation factor</span></span></th>
<th><span data-ttu-id="abbb6-598">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-598">Amount</span></span></th>
<th><span data-ttu-id="abbb6-599">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="abbb6-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-600">Prod 1</span></span></td>
<td><span data-ttu-id="abbb6-601">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-601">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-602">60</span><span class="sxs-lookup"><span data-stu-id="abbb6-602">60</span></span></td>
<td><span data-ttu-id="abbb6-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="abbb6-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="abbb6-604">535.31</span><span class="sxs-lookup"><span data-stu-id="abbb6-604">535.31</span></span></td>
<td><span data-ttu-id="abbb6-605">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-606">Prod 2</span></span></td>
<td><span data-ttu-id="abbb6-607">2. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-607">Product 2</span></span></td>
<td><span data-ttu-id="abbb6-608">20.</span><span class="sxs-lookup"><span data-stu-id="abbb6-608">20</span></span></td>
<td><span data-ttu-id="abbb6-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="abbb6-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="abbb6-610">178.44</span><span class="sxs-lookup"><span data-stu-id="abbb6-610">178.44</span></span></td>
<td><span data-ttu-id="abbb6-611">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-612">Prod 1</span></span></td>
<td><span data-ttu-id="abbb6-613">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-613">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-614">60</span><span class="sxs-lookup"><span data-stu-id="abbb6-614">60</span></span></td>
<td><span data-ttu-id="abbb6-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="abbb6-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="abbb6-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="abbb6-616">4,487.12</span></span></td>
<td><span data-ttu-id="abbb6-617">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-618">Prod 2</span></span></td>
<td><span data-ttu-id="abbb6-619">2. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-619">Product 2</span></span></td>
<td><span data-ttu-id="abbb6-620">20.</span><span class="sxs-lookup"><span data-stu-id="abbb6-620">20</span></span></td>
<td><span data-ttu-id="abbb6-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="abbb6-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="abbb6-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="abbb6-622">1,495.71</span></span></td>
<td><span data-ttu-id="abbb6-623">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abbb6-624">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="abbb6-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-625">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-625">Cost object</span></span></th>
<th><span data-ttu-id="abbb6-626">Lielums</span><span class="sxs-lookup"><span data-stu-id="abbb6-626">Magnitude</span></span></th>
<th><span data-ttu-id="abbb6-627">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="abbb6-627">Allocation factor</span></span></th>
<th><span data-ttu-id="abbb6-628">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-628">Amount</span></span></th>
<th><span data-ttu-id="abbb6-629">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="abbb6-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-630">Prod 1</span></span></td>
<td><span data-ttu-id="abbb6-631">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-631">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-632">80</span><span class="sxs-lookup"><span data-stu-id="abbb6-632">80</span></span></td>
<td><span data-ttu-id="abbb6-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="abbb6-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="abbb6-634">241.05</span><span class="sxs-lookup"><span data-stu-id="abbb6-634">241.05</span></span></td>
<td><span data-ttu-id="abbb6-635">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-636">Prod 2</span></span></td>
<td><span data-ttu-id="abbb6-637">2. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-637">Product 2</span></span></td>
<td><span data-ttu-id="abbb6-638">15</span><span class="sxs-lookup"><span data-stu-id="abbb6-638">15</span></span></td>
<td><span data-ttu-id="abbb6-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="abbb6-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="abbb6-640">45.20</span><span class="sxs-lookup"><span data-stu-id="abbb6-640">45.20</span></span></td>
<td><span data-ttu-id="abbb6-641">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-642">Prod 1</span></span></td>
<td><span data-ttu-id="abbb6-643">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-643">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-644">80</span><span class="sxs-lookup"><span data-stu-id="abbb6-644">80</span></span></td>
<td><span data-ttu-id="abbb6-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="abbb6-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="abbb6-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="abbb6-646">2,507.09</span></span></td>
<td><span data-ttu-id="abbb6-647">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-648">Prod 2</span></span></td>
<td><span data-ttu-id="abbb6-649">2. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-649">Product 2</span></span></td>
<td><span data-ttu-id="abbb6-650">15</span><span class="sxs-lookup"><span data-stu-id="abbb6-650">15</span></span></td>
<td><span data-ttu-id="abbb6-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="abbb6-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="abbb6-652">470.08</span><span class="sxs-lookup"><span data-stu-id="abbb6-652">470.08</span></span></td>
<td><span data-ttu-id="abbb6-653">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="abbb6-654">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="abbb6-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="abbb6-655">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="abbb6-655">Journal</span></span></th>
<th><span data-ttu-id="abbb6-656">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="abbb6-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="abbb6-657">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="abbb6-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="abbb6-658">Versija</span><span class="sxs-lookup"><span data-stu-id="abbb6-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-659">00004</span><span class="sxs-lookup"><span data-stu-id="abbb6-659">00004</span></span></td>
<td><span data-ttu-id="abbb6-660">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="abbb6-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="abbb6-661">Finanšu</span><span class="sxs-lookup"><span data-stu-id="abbb6-661">Fiscal</span></span></td>
<td><span data-ttu-id="abbb6-662">2017</span><span class="sxs-lookup"><span data-stu-id="abbb6-662">2017</span></span></td>
<td><span data-ttu-id="abbb6-663">Periods 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-663">Period 1</span></span></td>
<td><span data-ttu-id="abbb6-664">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="abbb6-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="abbb6-665">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="abbb6-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="abbb6-666">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="abbb6-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="abbb6-667">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="abbb6-668">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="abbb6-668">Cost element</span></span></th>
<th><span data-ttu-id="abbb6-669">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="abbb6-669">Cost behavior</span></span></th>
<th><span data-ttu-id="abbb6-670">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-671">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-672">CC001</span><span class="sxs-lookup"><span data-stu-id="abbb6-672">CC001</span></span></td>
<td><span data-ttu-id="abbb6-673">HR</span><span class="sxs-lookup"><span data-stu-id="abbb6-673">HR</span></span></td>
<td><span data-ttu-id="abbb6-674">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-674">10001</span></span></td>
<td><span data-ttu-id="abbb6-675">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-675">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-676">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-676">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-677">500,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-678">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-679">CC001</span><span class="sxs-lookup"><span data-stu-id="abbb6-679">CC001</span></span></td>
<td><span data-ttu-id="abbb6-680">HR</span><span class="sxs-lookup"><span data-stu-id="abbb6-680">HR</span></span></td>
<td><span data-ttu-id="abbb6-681">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-681">10001</span></span></td>
<td><span data-ttu-id="abbb6-682">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-682">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-683">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-683">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="abbb6-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-685">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-686">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-686">CC002</span></span></td>
<td><span data-ttu-id="abbb6-687">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-687">Finance</span></span></td>
<td><span data-ttu-id="abbb6-688">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-688">10001</span></span></td>
<td><span data-ttu-id="abbb6-689">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-689">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-690">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-690">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-691">675.00</span><span class="sxs-lookup"><span data-stu-id="abbb6-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-692">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-693">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-693">CC002</span></span></td>
<td><span data-ttu-id="abbb6-694">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-694">Finance</span></span></td>
<td><span data-ttu-id="abbb6-695">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-695">10001</span></span></td>
<td><span data-ttu-id="abbb6-696">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-696">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-697">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-697">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="abbb6-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-699">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-700">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-700">CC003</span></span></td>
<td><span data-ttu-id="abbb6-701">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-701">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-702">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-702">10001</span></span></td>
<td><span data-ttu-id="abbb6-703">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-703">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-704">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-704">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-705">713.75</span><span class="sxs-lookup"><span data-stu-id="abbb6-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-706">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-707">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-707">CC003</span></span></td>
<td><span data-ttu-id="abbb6-708">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-708">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-709">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-709">10001</span></span></td>
<td><span data-ttu-id="abbb6-710">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-710">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-711">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-711">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="abbb6-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-713">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-714">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-714">CC003</span></span></td>
<td><span data-ttu-id="abbb6-715">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="abbb6-715">Packaging</span></span></td>
<td><span data-ttu-id="abbb6-716">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-716">10001</span></span></td>
<td><span data-ttu-id="abbb6-717">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-717">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-718">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-718">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-719">286.25</span><span class="sxs-lookup"><span data-stu-id="abbb6-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-720">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-721">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-721">CC003</span></span></td>
<td><span data-ttu-id="abbb6-722">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="abbb6-722">Packaging</span></span></td>
<td><span data-ttu-id="abbb6-723">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-723">10001</span></span></td>
<td><span data-ttu-id="abbb6-724">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-724">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-725">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-725">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="abbb6-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-727">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-728">Prod 1</span></span></td>
<td><span data-ttu-id="abbb6-729">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-729">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-730">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-730">10001</span></span></td>
<td><span data-ttu-id="abbb6-731">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-731">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-732">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-732">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-733">776.36</span><span class="sxs-lookup"><span data-stu-id="abbb6-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-734">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-735">Prod 1</span></span></td>
<td><span data-ttu-id="abbb6-736">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-736">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-737">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-737">10001</span></span></td>
<td><span data-ttu-id="abbb6-738">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-738">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-739">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-739">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="abbb6-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-741">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-742">Prod 2</span></span></td>
<td><span data-ttu-id="abbb6-743">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-743">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-744">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-744">10001</span></span></td>
<td><span data-ttu-id="abbb6-745">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-745">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-746">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-746">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-747">223.64</span><span class="sxs-lookup"><span data-stu-id="abbb6-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-748">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="abbb6-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-749">Prod 2</span></span></td>
<td><span data-ttu-id="abbb6-750">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-750">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-751">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-751">10001</span></span></td>
<td><span data-ttu-id="abbb6-752">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-752">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-753">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-753">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="abbb6-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="abbb6-755">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="abbb6-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="abbb6-756">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="abbb6-757">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="abbb6-757">Cost element</span></span></th>
<th><span data-ttu-id="abbb6-758">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="abbb6-758">Cost behavior</span></span></th>
<th><span data-ttu-id="abbb6-759">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-759">Amount</span></span></th>
<th><span data-ttu-id="abbb6-760">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="abbb6-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="abbb6-761">CC001</span><span class="sxs-lookup"><span data-stu-id="abbb6-761">CC001</span></span></td>
<td><span data-ttu-id="abbb6-762">HR</span><span class="sxs-lookup"><span data-stu-id="abbb6-762">HR</span></span></td>
<td><span data-ttu-id="abbb6-763">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-763">10001</span></span></td>
<td><span data-ttu-id="abbb6-764">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-764">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-765">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-765">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-766">-500.00</span></span></td>
<td><span data-ttu-id="abbb6-767">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-768">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-768">CC002</span></span></td>
<td><span data-ttu-id="abbb6-769">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-769">Finance</span></span></td>
<td><span data-ttu-id="abbb6-770">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-770">10001</span></span></td>
<td><span data-ttu-id="abbb6-771">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-771">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-772">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-772">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-773">175.00</span><span class="sxs-lookup"><span data-stu-id="abbb6-773">175.00</span></span></td>
<td><span data-ttu-id="abbb6-774">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-775">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-775">CC003</span></span></td>
<td><span data-ttu-id="abbb6-776">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-776">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-777">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-777">10001</span></span></td>
<td><span data-ttu-id="abbb6-778">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-778">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-779">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-779">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-780">275.00</span><span class="sxs-lookup"><span data-stu-id="abbb6-780">275.00</span></span></td>
<td><span data-ttu-id="abbb6-781">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-782">CC004</span><span class="sxs-lookup"><span data-stu-id="abbb6-782">CC004</span></span></td>
<td><span data-ttu-id="abbb6-783">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="abbb6-783">Packaging</span></span></td>
<td><span data-ttu-id="abbb6-784">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-784">10001</span></span></td>
<td><span data-ttu-id="abbb6-785">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-785">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-786">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-786">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-787">50,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-787">50,00</span></span></td>
<td><span data-ttu-id="abbb6-788">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-789">CC001</span><span class="sxs-lookup"><span data-stu-id="abbb6-789">CC001</span></span></td>
<td><span data-ttu-id="abbb6-790">HR</span><span class="sxs-lookup"><span data-stu-id="abbb6-790">HR</span></span></td>
<td><span data-ttu-id="abbb6-791">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-791">10001</span></span></td>
<td><span data-ttu-id="abbb6-792">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-792">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-793">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-793">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="abbb6-794">-1,245.71</span></span></td>
<td><span data-ttu-id="abbb6-795">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-796">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-796">CC002</span></span></td>
<td><span data-ttu-id="abbb6-797">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-797">Finance</span></span></td>
<td><span data-ttu-id="abbb6-798">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-798">10001</span></span></td>
<td><span data-ttu-id="abbb6-799">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-799">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-800">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-800">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-801">436.00</span><span class="sxs-lookup"><span data-stu-id="abbb6-801">436.00</span></span></td>
<td><span data-ttu-id="abbb6-802">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-803">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-803">CC003</span></span></td>
<td><span data-ttu-id="abbb6-804">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-804">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-805">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-805">10001</span></span></td>
<td><span data-ttu-id="abbb6-806">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-806">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-807">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-807">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-808">685.14</span><span class="sxs-lookup"><span data-stu-id="abbb6-808">685.14</span></span></td>
<td><span data-ttu-id="abbb6-809">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-810">CC004</span><span class="sxs-lookup"><span data-stu-id="abbb6-810">CC004</span></span></td>
<td><span data-ttu-id="abbb6-811">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="abbb6-811">Packaging</span></span></td>
<td><span data-ttu-id="abbb6-812">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-812">10001</span></span></td>
<td><span data-ttu-id="abbb6-813">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-813">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-814">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-814">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-815">124.57</span><span class="sxs-lookup"><span data-stu-id="abbb6-815">124.57</span></span></td>
<td><span data-ttu-id="abbb6-816">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-817">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-817">CC002</span></span></td>
<td><span data-ttu-id="abbb6-818">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-818">Finance</span></span></td>
<td><span data-ttu-id="abbb6-819">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-819">10001</span></span></td>
<td><span data-ttu-id="abbb6-820">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-820">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-821">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-821">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-822">-675.00</span></span></td>
<td><span data-ttu-id="abbb6-823">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-824">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-824">CC003</span></span></td>
<td><span data-ttu-id="abbb6-825">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-825">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-826">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-826">10001</span></span></td>
<td><span data-ttu-id="abbb6-827">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-827">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-828">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-828">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-829">438.75</span><span class="sxs-lookup"><span data-stu-id="abbb6-829">438.75</span></span></td>
<td><span data-ttu-id="abbb6-830">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-831">CC004</span><span class="sxs-lookup"><span data-stu-id="abbb6-831">CC004</span></span></td>
<td><span data-ttu-id="abbb6-832">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="abbb6-832">Packaging</span></span></td>
<td><span data-ttu-id="abbb6-833">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-833">10001</span></span></td>
<td><span data-ttu-id="abbb6-834">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-834">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-835">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-835">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-836">236.25</span><span class="sxs-lookup"><span data-stu-id="abbb6-836">236.25</span></span></td>
<td><span data-ttu-id="abbb6-837">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-838">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-838">CC002</span></span></td>
<td><span data-ttu-id="abbb6-839">Finanses</span><span class="sxs-lookup"><span data-stu-id="abbb6-839">Finance</span></span></td>
<td><span data-ttu-id="abbb6-840">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-840">10001</span></span></td>
<td><span data-ttu-id="abbb6-841">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-841">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-842">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-842">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="abbb6-843">-8,150.29</span></span></td>
<td><span data-ttu-id="abbb6-844">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-845">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-845">CC003</span></span></td>
<td><span data-ttu-id="abbb6-846">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-846">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-847">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-847">10001</span></span></td>
<td><span data-ttu-id="abbb6-848">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-848">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-849">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-849">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="abbb6-850">5,297.69</span></span></td>
<td><span data-ttu-id="abbb6-851">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-852">CC004</span><span class="sxs-lookup"><span data-stu-id="abbb6-852">CC004</span></span></td>
<td><span data-ttu-id="abbb6-853">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="abbb6-853">Packaging</span></span></td>
<td><span data-ttu-id="abbb6-854">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-854">10001</span></span></td>
<td><span data-ttu-id="abbb6-855">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-855">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-856">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-856">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="abbb6-857">2,852.60</span></span></td>
<td><span data-ttu-id="abbb6-858">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-859">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-859">CC003</span></span></td>
<td><span data-ttu-id="abbb6-860">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-860">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-861">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-861">10001</span></span></td>
<td><span data-ttu-id="abbb6-862">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-862">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-863">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-863">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="abbb6-864">-713.75</span></span></td>
<td><span data-ttu-id="abbb6-865">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-866">Prod 1</span></span></td>
<td><span data-ttu-id="abbb6-867">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-867">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-868">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-868">10001</span></span></td>
<td><span data-ttu-id="abbb6-869">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-869">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-870">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-870">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-871">535.31</span><span class="sxs-lookup"><span data-stu-id="abbb6-871">535.31</span></span></td>
<td><span data-ttu-id="abbb6-872">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-873">Prod 2</span></span></td>
<td><span data-ttu-id="abbb6-874">2. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-874">Product 2</span></span></td>
<td><span data-ttu-id="abbb6-875">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-875">10001</span></span></td>
<td><span data-ttu-id="abbb6-876">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-876">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-877">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-877">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-878">178.44</span><span class="sxs-lookup"><span data-stu-id="abbb6-878">178.44</span></span></td>
<td><span data-ttu-id="abbb6-879">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-880">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-880">CC003</span></span></td>
<td><span data-ttu-id="abbb6-881">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-881">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-882">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-882">10001</span></span></td>
<td><span data-ttu-id="abbb6-883">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-883">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-884">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-884">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="abbb6-885">-5,982.83</span></span></td>
<td><span data-ttu-id="abbb6-886">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-887">Prod 1</span></span></td>
<td><span data-ttu-id="abbb6-888">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-888">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-889">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-889">10001</span></span></td>
<td><span data-ttu-id="abbb6-890">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-890">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-891">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-891">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="abbb6-892">4,487.12</span></span></td>
<td><span data-ttu-id="abbb6-893">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-894">Prod 2</span></span></td>
<td><span data-ttu-id="abbb6-895">2. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-895">Product 2</span></span></td>
<td><span data-ttu-id="abbb6-896">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-896">10001</span></span></td>
<td><span data-ttu-id="abbb6-897">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-897">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-898">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-898">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="abbb6-899">1,495.71</span></span></td>
<td><span data-ttu-id="abbb6-900">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-901">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-901">CC003</span></span></td>
<td><span data-ttu-id="abbb6-902">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-902">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-903">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-903">10001</span></span></td>
<td><span data-ttu-id="abbb6-904">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-904">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-905">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-905">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="abbb6-906">-286.25</span></span></td>
<td><span data-ttu-id="abbb6-907">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-908">Prod 1</span></span></td>
<td><span data-ttu-id="abbb6-909">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-909">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-910">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-910">10001</span></span></td>
<td><span data-ttu-id="abbb6-911">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-911">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-912">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-912">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-913">241.05</span><span class="sxs-lookup"><span data-stu-id="abbb6-913">241.05</span></span></td>
<td><span data-ttu-id="abbb6-914">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-915">Prod 2</span></span></td>
<td><span data-ttu-id="abbb6-916">2. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-916">Product 2</span></span></td>
<td><span data-ttu-id="abbb6-917">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-917">10001</span></span></td>
<td><span data-ttu-id="abbb6-918">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-918">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-919">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-919">Fixed cost</span></span></td>
<td><span data-ttu-id="abbb6-920">45.20</span><span class="sxs-lookup"><span data-stu-id="abbb6-920">45.20</span></span></td>
<td><span data-ttu-id="abbb6-921">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-922">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-922">CC003</span></span></td>
<td><span data-ttu-id="abbb6-923">Montāža</span><span class="sxs-lookup"><span data-stu-id="abbb6-923">Assembly</span></span></td>
<td><span data-ttu-id="abbb6-924">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-924">10001</span></span></td>
<td><span data-ttu-id="abbb6-925">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-925">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-926">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-926">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="abbb6-927">-2,977.17</span></span></td>
<td><span data-ttu-id="abbb6-928">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-929">Prod 1</span></span></td>
<td><span data-ttu-id="abbb6-930">1. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-930">Product 1</span></span></td>
<td><span data-ttu-id="abbb6-931">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-931">10001</span></span></td>
<td><span data-ttu-id="abbb6-932">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-932">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-933">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-933">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="abbb6-934">2,507.09</span></span></td>
<td><span data-ttu-id="abbb6-935">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="abbb6-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-936">Prod 2</span></span></td>
<td><span data-ttu-id="abbb6-937">2. prece</span><span class="sxs-lookup"><span data-stu-id="abbb6-937">Product 2</span></span></td>
<td><span data-ttu-id="abbb6-938">10001</span><span class="sxs-lookup"><span data-stu-id="abbb6-938">10001</span></span></td>
<td><span data-ttu-id="abbb6-939">Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-939">Electricity</span></span></td>
<td><span data-ttu-id="abbb6-940">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-940">Variable cost</span></span></td>
<td><span data-ttu-id="abbb6-941">470.08</span><span class="sxs-lookup"><span data-stu-id="abbb6-941">470.08</span></span></td>
<td><span data-ttu-id="abbb6-942">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="abbb6-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="abbb6-943">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="abbb6-943">Conclusion</span></span>
<span data-ttu-id="abbb6-944">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="abbb6-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="abbb6-945">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="abbb6-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="abbb6-946">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="abbb6-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="abbb6-947">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="abbb6-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="abbb6-948">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="abbb6-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="abbb6-949">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="abbb6-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="abbb6-950">Summa</span><span class="sxs-lookup"><span data-stu-id="abbb6-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="abbb6-951">CC099</span><span class="sxs-lookup"><span data-stu-id="abbb6-951">CC099</span></span></th>
<th><span data-ttu-id="abbb6-952">CC001</span><span class="sxs-lookup"><span data-stu-id="abbb6-952">CC001</span></span></th>
<th><span data-ttu-id="abbb6-953">CC002</span><span class="sxs-lookup"><span data-stu-id="abbb6-953">CC002</span></span></th>
<th><span data-ttu-id="abbb6-954">CC003</span><span class="sxs-lookup"><span data-stu-id="abbb6-954">CC003</span></span></th>
<th><span data-ttu-id="abbb6-955">CC004</span><span class="sxs-lookup"><span data-stu-id="abbb6-955">CC004</span></span></th>
<th><span data-ttu-id="abbb6-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-956">Proj 1</span></span></th>
<th><span data-ttu-id="abbb6-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-957">Proj 2</span></span></th>
<th><span data-ttu-id="abbb6-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="abbb6-958">Prod 1</span></span></th>
<th><span data-ttu-id="abbb6-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="abbb6-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="abbb6-960">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="abbb6-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="abbb6-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="abbb6-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="abbb6-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="abbb6-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="abbb6-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="abbb6-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="abbb6-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="abbb6-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="abbb6-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="abbb6-970">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="abbb6-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-971">0,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-971">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="abbb6-972">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-973">0,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-974">0,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-975">0,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-976">0,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-977">0,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-978">776.36</span><span class="sxs-lookup"><span data-stu-id="abbb6-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-979">223.64</span><span class="sxs-lookup"><span data-stu-id="abbb6-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="abbb6-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="abbb6-981">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="abbb6-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-982">000</span><span class="sxs-lookup"><span data-stu-id="abbb6-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-983">0,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-984">0,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-985">0,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-986">0,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-987">30,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-988">10,00</span><span class="sxs-lookup"><span data-stu-id="abbb6-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="abbb6-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="abbb6-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="abbb6-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="abbb6-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="abbb6-992">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="abbb6-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="abbb6-993">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="abbb6-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="abbb6-994">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="abbb6-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="abbb6-995">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="abbb6-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="abbb6-996">Plašāku informāciju skatiet [Izmaksu apkopojuma politika un pieskaitāmo izmaksu aprēķins](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="abbb6-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



