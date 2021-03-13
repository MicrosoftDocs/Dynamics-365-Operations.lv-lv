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
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d60248f2bd6774b2e9afdb3632b6eb31d67349ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009522"
---
# <a name="overhead-calculation"></a><span data-ttu-id="e8870-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="e8870-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8870-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="e8870-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="e8870-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="e8870-105">Term definition</span></span>
---------------

<span data-ttu-id="e8870-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="e8870-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="e8870-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="e8870-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="e8870-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="e8870-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="e8870-109">Īre</span><span class="sxs-lookup"><span data-stu-id="e8870-109">Rent</span></span>
-   <span data-ttu-id="e8870-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-110">Electricity</span></span>
-   <span data-ttu-id="e8870-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="e8870-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="e8870-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="e8870-112">Overhead calculation overview</span></span>
<span data-ttu-id="e8870-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="e8870-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="e8870-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="e8870-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="e8870-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="e8870-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="e8870-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="e8870-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="e8870-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="e8870-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="e8870-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="e8870-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="e8870-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="e8870-119">Version type</span></span>
-   <span data-ttu-id="e8870-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="e8870-120">Date and time</span></span>
-   <span data-ttu-id="e8870-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="e8870-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="e8870-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="e8870-122">Fiscal year</span></span>
-   <span data-ttu-id="e8870-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="e8870-123">Fiscal period</span></span>

<span data-ttu-id="e8870-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="e8870-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="e8870-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="e8870-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="e8870-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="e8870-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="e8870-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="e8870-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="e8870-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="e8870-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="e8870-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="e8870-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="e8870-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="e8870-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="e8870-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="e8870-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="e8870-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="e8870-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="e8870-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="e8870-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="e8870-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="e8870-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="e8870-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="e8870-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="e8870-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="e8870-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="e8870-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e8870-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="e8870-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e8870-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="e8870-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="e8870-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="e8870-140">Main account</span></span></th>
<th><span data-ttu-id="e8870-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="e8870-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="e8870-143">CC099</span><span class="sxs-lookup"><span data-stu-id="e8870-143">CC099</span></span></td>
<td><span data-ttu-id="e8870-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="e8870-144">Default cost center</span></span></td>
<td><span data-ttu-id="e8870-145">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-145">10001</span></span></td>
<td><span data-ttu-id="e8870-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-146">Electricity</span></span></td>
<td><span data-ttu-id="e8870-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="e8870-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="e8870-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="e8870-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="e8870-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="e8870-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="e8870-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="e8870-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="e8870-151">Define the cost behavior rule</span></span>

<span data-ttu-id="e8870-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="e8870-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="e8870-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="e8870-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="e8870-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="e8870-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="e8870-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="e8870-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="e8870-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="e8870-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="e8870-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="e8870-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="e8870-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="e8870-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="e8870-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e8870-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="e8870-160">Journal</span></span></th>
<th><span data-ttu-id="e8870-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="e8870-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e8870-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="e8870-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e8870-163">Versija</span><span class="sxs-lookup"><span data-stu-id="e8870-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-164">00001</span><span class="sxs-lookup"><span data-stu-id="e8870-164">00001</span></span></td>
<td><span data-ttu-id="e8870-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="e8870-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="e8870-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="e8870-166">Fiscal</span></span></td>
<td><span data-ttu-id="e8870-167">2017</span><span class="sxs-lookup"><span data-stu-id="e8870-167">2017</span></span></td>
<td><span data-ttu-id="e8870-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="e8870-168">Period 1</span></span></td>
<td><span data-ttu-id="e8870-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="e8870-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e8870-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="e8870-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e8870-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="e8870-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e8870-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e8870-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="e8870-173">Cost element</span></span></th>
<th><span data-ttu-id="e8870-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="e8870-174">Cost behavior</span></span></th>
<th><span data-ttu-id="e8870-175">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="e8870-177">CC099</span><span class="sxs-lookup"><span data-stu-id="e8870-177">CC099</span></span></td>
<td><span data-ttu-id="e8870-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="e8870-178">Default cost center</span></span></td>
<td><span data-ttu-id="e8870-179">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-179">10001</span></span></td>
<td><span data-ttu-id="e8870-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-180">Electricity</span></span></td>
<td><span data-ttu-id="e8870-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="e8870-181">Unclassified</span></span></td>
<td><span data-ttu-id="e8870-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e8870-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="e8870-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e8870-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="e8870-185">Cost element</span></span></th>
<th><span data-ttu-id="e8870-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="e8870-186">Cost behavior</span></span></th>
<th><span data-ttu-id="e8870-187">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-187">Amount</span></span></th>
<th><span data-ttu-id="e8870-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="e8870-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-189">CC099</span><span class="sxs-lookup"><span data-stu-id="e8870-189">CC099</span></span></td>
<td><span data-ttu-id="e8870-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="e8870-190">Default cost center</span></span></td>
<td><span data-ttu-id="e8870-191">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-191">10001</span></span></td>
<td><span data-ttu-id="e8870-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-192">Electricity</span></span></td>
<td><span data-ttu-id="e8870-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="e8870-193">Unclassified</span></span></td>
<td><span data-ttu-id="e8870-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-194">10,000.00</span></span></td>
<td><span data-ttu-id="e8870-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-196">CC099</span><span class="sxs-lookup"><span data-stu-id="e8870-196">CC099</span></span></td>
<td><span data-ttu-id="e8870-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="e8870-197">Default cost center</span></span></td>
<td><span data-ttu-id="e8870-198">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-198">10001</span></span></td>
<td><span data-ttu-id="e8870-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-199">Electricity</span></span></td>
<td><span data-ttu-id="e8870-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="e8870-200">Unclassified</span></span></td>
<td><span data-ttu-id="e8870-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-201">-10,000.00</span></span></td>
<td><span data-ttu-id="e8870-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-203">CC099</span><span class="sxs-lookup"><span data-stu-id="e8870-203">CC099</span></span></td>
<td><span data-ttu-id="e8870-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="e8870-204">Default cost center</span></span></td>
<td><span data-ttu-id="e8870-205">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-205">10001</span></span></td>
<td><span data-ttu-id="e8870-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-206">Electricity</span></span></td>
<td><span data-ttu-id="e8870-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-207">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-208">1,000.00</span></span></td>
<td><span data-ttu-id="e8870-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-210">CC099</span><span class="sxs-lookup"><span data-stu-id="e8870-210">CC099</span></span></td>
<td><span data-ttu-id="e8870-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="e8870-211">Default cost center</span></span></td>
<td><span data-ttu-id="e8870-212">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-212">10001</span></span></td>
<td><span data-ttu-id="e8870-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-213">Electricity</span></span></td>
<td><span data-ttu-id="e8870-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-214">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="e8870-215">9,000.00</span></span></td>
<td><span data-ttu-id="e8870-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8870-217">Sīkāku informāciju skatiet šeit: [Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="e8870-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="e8870-218">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="e8870-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="e8870-219">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="e8870-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="e8870-220">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="e8870-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="e8870-221">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="e8870-221">Define the cost distribution rule</span></span>

<span data-ttu-id="e8870-222">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="e8870-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="e8870-223">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="e8870-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="e8870-224">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="e8870-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="e8870-225">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="e8870-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="e8870-226">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="e8870-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="e8870-227">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="e8870-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-228">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-228">Cost object</span></span></th>
<th><span data-ttu-id="e8870-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="e8870-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-230">CC001</span><span class="sxs-lookup"><span data-stu-id="e8870-230">CC001</span></span></td>
<td><span data-ttu-id="e8870-231">HR</span><span class="sxs-lookup"><span data-stu-id="e8870-231">HR</span></span></td>
<td><span data-ttu-id="e8870-232">1000</span><span class="sxs-lookup"><span data-stu-id="e8870-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-233">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-233">CC002</span></span></td>
<td><span data-ttu-id="e8870-234">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-234">Finance</span></span></td>
<td><span data-ttu-id="e8870-235">6,000</span><span class="sxs-lookup"><span data-stu-id="e8870-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-236">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-236">CC003</span></span></td>
<td><span data-ttu-id="e8870-237">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-237">Assembly</span></span></td>
<td><span data-ttu-id="e8870-238">0</span><span class="sxs-lookup"><span data-stu-id="e8870-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8870-239">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="e8870-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-240">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-240">Cost object</span></span></th>
<th><span data-ttu-id="e8870-241">Lielums</span><span class="sxs-lookup"><span data-stu-id="e8870-241">Magnitude</span></span></th>
<th><span data-ttu-id="e8870-242">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="e8870-242">Allocation factor</span></span></th>
<th><span data-ttu-id="e8870-243">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-244">CC001</span><span class="sxs-lookup"><span data-stu-id="e8870-244">CC001</span></span></td>
<td><span data-ttu-id="e8870-245">HR</span><span class="sxs-lookup"><span data-stu-id="e8870-245">HR</span></span></td>
<td><span data-ttu-id="e8870-246">1000</span><span class="sxs-lookup"><span data-stu-id="e8870-246">1,000</span></span></td>
<td><span data-ttu-id="e8870-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e8870-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e8870-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-249">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-249">CC002</span></span></td>
<td><span data-ttu-id="e8870-250">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-250">Finance</span></span></td>
<td><span data-ttu-id="e8870-251">6,000</span><span class="sxs-lookup"><span data-stu-id="e8870-251">6,000</span></span></td>
<td><span data-ttu-id="e8870-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e8870-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e8870-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-254">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-254">CC003</span></span></td>
<td><span data-ttu-id="e8870-255">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-255">Assembly</span></span></td>
<td><span data-ttu-id="e8870-256">0</span><span class="sxs-lookup"><span data-stu-id="e8870-256">0</span></span></td>
<td><span data-ttu-id="e8870-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e8870-258">0,00</span><span class="sxs-lookup"><span data-stu-id="e8870-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8870-259">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="e8870-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="e8870-260">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="e8870-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-261">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-261">Cost object</span></span></th>
<th><span data-ttu-id="e8870-262">Formula</span><span class="sxs-lookup"><span data-stu-id="e8870-262">Formula</span></span></th>
<th><span data-ttu-id="e8870-263">Lielums</span><span class="sxs-lookup"><span data-stu-id="e8870-263">Magnitude</span></span></th>
<th><span data-ttu-id="e8870-264">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="e8870-264">Allocation factor</span></span></th>
<th><span data-ttu-id="e8870-265">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-266">CC001</span><span class="sxs-lookup"><span data-stu-id="e8870-266">CC001</span></span></td>
<td><span data-ttu-id="e8870-267">HR</span><span class="sxs-lookup"><span data-stu-id="e8870-267">HR</span></span></td>
<td><span data-ttu-id="e8870-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e8870-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e8870-269">1.</span><span class="sxs-lookup"><span data-stu-id="e8870-269">1</span></span></td>
<td><span data-ttu-id="e8870-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e8870-271">500,00</span><span class="sxs-lookup"><span data-stu-id="e8870-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-272">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-272">CC002</span></span></td>
<td><span data-ttu-id="e8870-273">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-273">Finance</span></span></td>
<td><span data-ttu-id="e8870-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e8870-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e8870-275">1.</span><span class="sxs-lookup"><span data-stu-id="e8870-275">1</span></span></td>
<td><span data-ttu-id="e8870-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e8870-277">500,00</span><span class="sxs-lookup"><span data-stu-id="e8870-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-278">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-278">CC003</span></span></td>
<td><span data-ttu-id="e8870-279">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-279">Assembly</span></span></td>
<td><span data-ttu-id="e8870-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e8870-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e8870-281">0</span><span class="sxs-lookup"><span data-stu-id="e8870-281">0</span></span></td>
<td><span data-ttu-id="e8870-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e8870-283">0,00</span><span class="sxs-lookup"><span data-stu-id="e8870-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e8870-284">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="e8870-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e8870-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="e8870-285">Journal</span></span></th>
<th><span data-ttu-id="e8870-286">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="e8870-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e8870-287">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="e8870-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e8870-288">Versija</span><span class="sxs-lookup"><span data-stu-id="e8870-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-289">00002</span><span class="sxs-lookup"><span data-stu-id="e8870-289">00002</span></span></td>
<td><span data-ttu-id="e8870-290">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="e8870-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="e8870-291">Finanšu</span><span class="sxs-lookup"><span data-stu-id="e8870-291">Fiscal</span></span></td>
<td><span data-ttu-id="e8870-292">2017</span><span class="sxs-lookup"><span data-stu-id="e8870-292">2017</span></span></td>
<td><span data-ttu-id="e8870-293">Periods 1</span><span class="sxs-lookup"><span data-stu-id="e8870-293">Period 1</span></span></td>
<td><span data-ttu-id="e8870-294">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="e8870-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e8870-295">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="e8870-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e8870-296">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="e8870-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e8870-297">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e8870-298">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="e8870-298">Cost element</span></span></th>
<th><span data-ttu-id="e8870-299">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="e8870-299">Cost behavior</span></span></th>
<th><span data-ttu-id="e8870-300">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-301">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-302">CC099</span><span class="sxs-lookup"><span data-stu-id="e8870-302">CC099</span></span></td>
<td><span data-ttu-id="e8870-303">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="e8870-303">Default cost center</span></span></td>
<td><span data-ttu-id="e8870-304">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-304">10001</span></span></td>
<td><span data-ttu-id="e8870-305">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-305">Electricity</span></span></td>
<td><span data-ttu-id="e8870-306">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-306">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-308">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-309">CC099</span><span class="sxs-lookup"><span data-stu-id="e8870-309">CC099</span></span></td>
<td><span data-ttu-id="e8870-310">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="e8870-310">Default cost center</span></span></td>
<td><span data-ttu-id="e8870-311">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-311">10001</span></span></td>
<td><span data-ttu-id="e8870-312">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-312">Electricity</span></span></td>
<td><span data-ttu-id="e8870-313">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-313">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="e8870-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e8870-315">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="e8870-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-316">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e8870-317">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="e8870-317">Cost element</span></span></th>
<th><span data-ttu-id="e8870-318">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="e8870-318">Cost behavior</span></span></th>
<th><span data-ttu-id="e8870-319">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-319">Amount</span></span></th>
<th><span data-ttu-id="e8870-320">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="e8870-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-321">CC099</span><span class="sxs-lookup"><span data-stu-id="e8870-321">CC099</span></span></td>
<td><span data-ttu-id="e8870-322">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="e8870-322">Default cost center</span></span></td>
<td><span data-ttu-id="e8870-323">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-323">10001</span></span></td>
<td><span data-ttu-id="e8870-324">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-324">Electricity</span></span></td>
<td><span data-ttu-id="e8870-325">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-325">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-326">-1000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-326">-1,000.00</span></span></td>
<td><span data-ttu-id="e8870-327">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-328">CC001</span><span class="sxs-lookup"><span data-stu-id="e8870-328">CC001</span></span></td>
<td><span data-ttu-id="e8870-329">HR</span><span class="sxs-lookup"><span data-stu-id="e8870-329">HR</span></span></td>
<td><span data-ttu-id="e8870-330">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-330">10001</span></span></td>
<td><span data-ttu-id="e8870-331">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-331">Electricity</span></span></td>
<td><span data-ttu-id="e8870-332">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-332">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-333">500,00</span><span class="sxs-lookup"><span data-stu-id="e8870-333">500.00</span></span></td>
<td><span data-ttu-id="e8870-334">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-335">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-335">CC002</span></span></td>
<td><span data-ttu-id="e8870-336">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-336">Finance</span></span></td>
<td><span data-ttu-id="e8870-337">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-337">10001</span></span></td>
<td><span data-ttu-id="e8870-338">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-338">Electricity</span></span></td>
<td><span data-ttu-id="e8870-339">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-339">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-340">500,00</span><span class="sxs-lookup"><span data-stu-id="e8870-340">500.00</span></span></td>
<td><span data-ttu-id="e8870-341">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-342">CC099</span><span class="sxs-lookup"><span data-stu-id="e8870-342">CC099</span></span></td>
<td><span data-ttu-id="e8870-343">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="e8870-343">Default cost center</span></span></td>
<td><span data-ttu-id="e8870-344">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-344">10001</span></span></td>
<td><span data-ttu-id="e8870-345">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-345">Electricity</span></span></td>
<td><span data-ttu-id="e8870-346">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-346">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="e8870-347">-9,000.00</span></span></td>
<td><span data-ttu-id="e8870-348">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-349">CC001</span><span class="sxs-lookup"><span data-stu-id="e8870-349">CC001</span></span></td>
<td><span data-ttu-id="e8870-350">HR</span><span class="sxs-lookup"><span data-stu-id="e8870-350">HR</span></span></td>
<td><span data-ttu-id="e8870-351">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-351">10001</span></span></td>
<td><span data-ttu-id="e8870-352">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-352">Electricity</span></span></td>
<td><span data-ttu-id="e8870-353">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-353">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e8870-354">1,285.71</span></span></td>
<td><span data-ttu-id="e8870-355">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-356">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-356">CC002</span></span></td>
<td><span data-ttu-id="e8870-357">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-357">Finance</span></span></td>
<td><span data-ttu-id="e8870-358">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-358">10001</span></span></td>
<td><span data-ttu-id="e8870-359">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-359">Electricity</span></span></td>
<td><span data-ttu-id="e8870-360">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-360">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e8870-361">7,714.29</span></span></td>
<td><span data-ttu-id="e8870-362">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8870-363">Sīkāku informāciju skatiet šeit: [Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="e8870-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="e8870-364">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="e8870-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="e8870-365">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="e8870-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="e8870-366">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="e8870-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="e8870-367">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="e8870-367">Define the overhead rate</span></span>

<span data-ttu-id="e8870-368">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="e8870-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="e8870-369">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="e8870-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-370">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-370">Cost object</span></span></th>
<th><span data-ttu-id="e8870-371">Stundas</span><span class="sxs-lookup"><span data-stu-id="e8870-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e8870-372">Proj 1</span></span></td>
<td><span data-ttu-id="e8870-373">1. projekts</span><span class="sxs-lookup"><span data-stu-id="e8870-373">Project 1</span></span></td>
<td><span data-ttu-id="e8870-374">3.</span><span class="sxs-lookup"><span data-stu-id="e8870-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e8870-375">Proj 2</span></span></td>
<td><span data-ttu-id="e8870-376">2. projekts</span><span class="sxs-lookup"><span data-stu-id="e8870-376">Project 2</span></span></td>
<td><span data-ttu-id="e8870-377">1.</span><span class="sxs-lookup"><span data-stu-id="e8870-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8870-378">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="e8870-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-379">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-379">Cost object</span></span></th>
<th><span data-ttu-id="e8870-380">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="e8870-380">Cost element</span></span></th>
<th><span data-ttu-id="e8870-381">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="e8870-381">Cost behavior</span></span></th>
<th><span data-ttu-id="e8870-382">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="e8870-382">Units</span></span></th>
<th><span data-ttu-id="e8870-383">Likme</span><span class="sxs-lookup"><span data-stu-id="e8870-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-384">CC001</span><span class="sxs-lookup"><span data-stu-id="e8870-384">CC001</span></span></td>
<td><span data-ttu-id="e8870-385">HR</span><span class="sxs-lookup"><span data-stu-id="e8870-385">HR</span></span></td>
<td><span data-ttu-id="e8870-386">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-386">10001</span></span></td>
<td><span data-ttu-id="e8870-387">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-387">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-388">1</span><span class="sxs-lookup"><span data-stu-id="e8870-388">1</span></span></td>
<td><span data-ttu-id="e8870-389">10</span><span class="sxs-lookup"><span data-stu-id="e8870-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8870-390">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="e8870-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-391">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-391">Cost object</span></span></th>
<th><span data-ttu-id="e8870-392">Lielums</span><span class="sxs-lookup"><span data-stu-id="e8870-392">Magnitude</span></span></th>
<th><span data-ttu-id="e8870-393">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="e8870-393">Cost element</span></span></th>
<th><span data-ttu-id="e8870-394">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="e8870-394">Allocation factor</span></span></th>
<th><span data-ttu-id="e8870-395">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e8870-396">Proj 1</span></span></td>
<td><span data-ttu-id="e8870-397">1. projekts</span><span class="sxs-lookup"><span data-stu-id="e8870-397">Project 1</span></span></td>
<td><span data-ttu-id="e8870-398">3.</span><span class="sxs-lookup"><span data-stu-id="e8870-398">3</span></span></td>
<td><span data-ttu-id="e8870-399">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-399">10001</span></span></td>
<td><span data-ttu-id="e8870-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e8870-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e8870-401">30,00</span><span class="sxs-lookup"><span data-stu-id="e8870-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e8870-402">Proj 2</span></span></td>
<td><span data-ttu-id="e8870-403">2. projekts</span><span class="sxs-lookup"><span data-stu-id="e8870-403">Project 2</span></span></td>
<td><span data-ttu-id="e8870-404">1.</span><span class="sxs-lookup"><span data-stu-id="e8870-404">1</span></span></td>
<td><span data-ttu-id="e8870-405">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-405">10001</span></span></td>
<td><span data-ttu-id="e8870-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e8870-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e8870-407">10,00</span><span class="sxs-lookup"><span data-stu-id="e8870-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e8870-408">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="e8870-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e8870-409">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="e8870-409">Journal</span></span></th>
<th><span data-ttu-id="e8870-410">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="e8870-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e8870-411">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="e8870-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e8870-412">Versija</span><span class="sxs-lookup"><span data-stu-id="e8870-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-413">00003</span><span class="sxs-lookup"><span data-stu-id="e8870-413">00003</span></span></td>
<td><span data-ttu-id="e8870-414">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="e8870-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="e8870-415">Finanšu</span><span class="sxs-lookup"><span data-stu-id="e8870-415">Fiscal</span></span></td>
<td><span data-ttu-id="e8870-416">2017</span><span class="sxs-lookup"><span data-stu-id="e8870-416">2017</span></span></td>
<td><span data-ttu-id="e8870-417">Periods 1</span><span class="sxs-lookup"><span data-stu-id="e8870-417">Period 1</span></span></td>
<td><span data-ttu-id="e8870-418">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="e8870-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="e8870-419">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="e8870-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e8870-420">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="e8870-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e8870-421">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-421">Cost object</span></span></th>
<th><span data-ttu-id="e8870-422">Lielums</span><span class="sxs-lookup"><span data-stu-id="e8870-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-423">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e8870-424">Proj 1</span></span></td>
<td><span data-ttu-id="e8870-425">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="e8870-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e8870-426">3,00</span><span class="sxs-lookup"><span data-stu-id="e8870-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-427">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e8870-428">Proj 2</span></span></td>
<td><span data-ttu-id="e8870-429">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="e8870-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e8870-430">1,00</span><span class="sxs-lookup"><span data-stu-id="e8870-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e8870-431">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="e8870-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-432">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e8870-433">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="e8870-433">Cost element</span></span></th>
<th><span data-ttu-id="e8870-434">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="e8870-434">Cost behavior</span></span></th>
<th><span data-ttu-id="e8870-435">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-435">Amount</span></span></th>
<th><span data-ttu-id="e8870-436">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="e8870-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="e8870-437">CC0001</span></span></td>
<td><span data-ttu-id="e8870-438">HR</span><span class="sxs-lookup"><span data-stu-id="e8870-438">HR</span></span></td>
<td><span data-ttu-id="e8870-439">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-439">10001</span></span></td>
<td><span data-ttu-id="e8870-440">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-440">Electricity</span></span></td>
<td><span data-ttu-id="e8870-441">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-441">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="e8870-442">-30.00</span></span></td>
<td><span data-ttu-id="e8870-443">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e8870-444">Proj 1</span></span></td>
<td><span data-ttu-id="e8870-445">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="e8870-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e8870-446">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-446">10001</span></span></td>
<td><span data-ttu-id="e8870-447">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-447">Electricity</span></span></td>
<td><span data-ttu-id="e8870-448">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-448">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-449">30,00</span><span class="sxs-lookup"><span data-stu-id="e8870-449">30.00</span></span></td>
<td><span data-ttu-id="e8870-450">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-451">CC001</span><span class="sxs-lookup"><span data-stu-id="e8870-451">CC001</span></span></td>
<td><span data-ttu-id="e8870-452">HR</span><span class="sxs-lookup"><span data-stu-id="e8870-452">HR</span></span></td>
<td><span data-ttu-id="e8870-453">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-453">10001</span></span></td>
<td><span data-ttu-id="e8870-454">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-454">Electricity</span></span></td>
<td><span data-ttu-id="e8870-455">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-455">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="e8870-456">-10.00</span></span></td>
<td><span data-ttu-id="e8870-457">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e8870-458">Proj 2</span></span></td>
<td><span data-ttu-id="e8870-459">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="e8870-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e8870-460">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-460">10001</span></span></td>
<td><span data-ttu-id="e8870-461">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-461">Electricity</span></span></td>
<td><span data-ttu-id="e8870-462">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-462">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-463">10,00</span><span class="sxs-lookup"><span data-stu-id="e8870-463">10.00</span></span></td>
<td><span data-ttu-id="e8870-464">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8870-465">Sīkāku informāciju skatiet šeit: [Pieskaitāmo izmaksu aprēķina veikšana](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="e8870-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="e8870-466">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="e8870-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="e8870-467">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="e8870-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="e8870-468">Finance atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="e8870-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="e8870-469">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="e8870-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="e8870-470">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="e8870-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="e8870-471">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="e8870-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="e8870-472">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="e8870-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="e8870-473">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="e8870-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="e8870-474">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="e8870-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="e8870-475">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="e8870-475">Define the cost allocation</span></span>

<span data-ttu-id="e8870-476">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="e8870-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="e8870-477">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="e8870-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="e8870-478">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="e8870-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-479">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-479">Cost object</span></span></th>
<th><span data-ttu-id="e8870-480">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="e8870-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-481">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-481">CC002</span></span></td>
<td><span data-ttu-id="e8870-482">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-482">Finance</span></span></td>
<td><span data-ttu-id="e8870-483">35</span><span class="sxs-lookup"><span data-stu-id="e8870-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-484">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-484">CC003</span></span></td>
<td><span data-ttu-id="e8870-485">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-485">Assembly</span></span></td>
<td><span data-ttu-id="e8870-486">55</span><span class="sxs-lookup"><span data-stu-id="e8870-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-487">CC004</span><span class="sxs-lookup"><span data-stu-id="e8870-487">CC004</span></span></td>
<td><span data-ttu-id="e8870-488">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="e8870-488">Packaging</span></span></td>
<td><span data-ttu-id="e8870-489">10.</span><span class="sxs-lookup"><span data-stu-id="e8870-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8870-490">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="e8870-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="e8870-491">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="e8870-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-492">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-492">Cost object</span></span></th>
<th><span data-ttu-id="e8870-493">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="e8870-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-494">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-494">CC003</span></span></td>
<td><span data-ttu-id="e8870-495">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-495">Assembly</span></span></td>
<td><span data-ttu-id="e8870-496">65</span><span class="sxs-lookup"><span data-stu-id="e8870-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-497">CC004</span><span class="sxs-lookup"><span data-stu-id="e8870-497">CC004</span></span></td>
<td><span data-ttu-id="e8870-498">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="e8870-498">Packaging</span></span></td>
<td><span data-ttu-id="e8870-499">35</span><span class="sxs-lookup"><span data-stu-id="e8870-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8870-500">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="e8870-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="e8870-501">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="e8870-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-502">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-502">Cost object</span></span></th>
<th><span data-ttu-id="e8870-503">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="e8870-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e8870-504">Prod 1</span></span></td>
<td><span data-ttu-id="e8870-505">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-505">Product 1</span></span></td>
<td><span data-ttu-id="e8870-506">60</span><span class="sxs-lookup"><span data-stu-id="e8870-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e8870-507">Prod 2</span></span></td>
<td><span data-ttu-id="e8870-508">2. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-508">Product 2</span></span></td>
<td><span data-ttu-id="e8870-509">20</span><span class="sxs-lookup"><span data-stu-id="e8870-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8870-510">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="e8870-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="e8870-511">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="e8870-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-512">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-512">Cost object</span></span></th>
<th><span data-ttu-id="e8870-513">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="e8870-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e8870-514">Prod 1</span></span></td>
<td><span data-ttu-id="e8870-515">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-515">Product 1</span></span></td>
<td><span data-ttu-id="e8870-516">80</span><span class="sxs-lookup"><span data-stu-id="e8870-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e8870-517">Prod 2</span></span></td>
<td><span data-ttu-id="e8870-518">2. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-518">Product 2</span></span></td>
<td><span data-ttu-id="e8870-519">15</span><span class="sxs-lookup"><span data-stu-id="e8870-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e8870-520">Statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="e8870-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="e8870-521">Sīkāku informāciju skatiet šeit: [Statistikas mēru nodrošinātāja veidne](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="e8870-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="e8870-522">Nākamajā tabulā ir parādīts rezultāts, ja tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījuma pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="e8870-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-523">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-523">Cost object</span></span></th>
<th><span data-ttu-id="e8870-524">Lielums</span><span class="sxs-lookup"><span data-stu-id="e8870-524">Magnitude</span></span></th>
<th><span data-ttu-id="e8870-525">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="e8870-525">Allocation factor</span></span></th>
<th><span data-ttu-id="e8870-526">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-526">Amount</span></span></th>
<th><span data-ttu-id="e8870-527">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="e8870-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-528">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-528">CC002</span></span></td>
<td><span data-ttu-id="e8870-529">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-529">Finance</span></span></td>
<td><span data-ttu-id="e8870-530">35</span><span class="sxs-lookup"><span data-stu-id="e8870-530">35</span></span></td>
<td><span data-ttu-id="e8870-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e8870-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e8870-532">175.00</span><span class="sxs-lookup"><span data-stu-id="e8870-532">175.00</span></span></td>
<td><span data-ttu-id="e8870-533">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-534">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-534">CC003</span></span></td>
<td><span data-ttu-id="e8870-535">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-535">Assembly</span></span></td>
<td><span data-ttu-id="e8870-536">55</span><span class="sxs-lookup"><span data-stu-id="e8870-536">55</span></span></td>
<td><span data-ttu-id="e8870-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e8870-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e8870-538">275.00</span><span class="sxs-lookup"><span data-stu-id="e8870-538">275.00</span></span></td>
<td><span data-ttu-id="e8870-539">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-540">CC004</span><span class="sxs-lookup"><span data-stu-id="e8870-540">CC004</span></span></td>
<td><span data-ttu-id="e8870-541">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="e8870-541">Packaging</span></span></td>
<td><span data-ttu-id="e8870-542">10.</span><span class="sxs-lookup"><span data-stu-id="e8870-542">10</span></span></td>
<td><span data-ttu-id="e8870-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e8870-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e8870-544">50,00</span><span class="sxs-lookup"><span data-stu-id="e8870-544">50.00</span></span></td>
<td><span data-ttu-id="e8870-545">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-546">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-546">CC002</span></span></td>
<td><span data-ttu-id="e8870-547">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-547">Finance</span></span></td>
<td><span data-ttu-id="e8870-548">35</span><span class="sxs-lookup"><span data-stu-id="e8870-548">35</span></span></td>
<td><span data-ttu-id="e8870-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="e8870-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e8870-550">436.00</span><span class="sxs-lookup"><span data-stu-id="e8870-550">436.00</span></span></td>
<td><span data-ttu-id="e8870-551">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-552">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-552">CC003</span></span></td>
<td><span data-ttu-id="e8870-553">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-553">Assembly</span></span></td>
<td><span data-ttu-id="e8870-554">55</span><span class="sxs-lookup"><span data-stu-id="e8870-554">55</span></span></td>
<td><span data-ttu-id="e8870-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="e8870-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e8870-556">685.14</span><span class="sxs-lookup"><span data-stu-id="e8870-556">685.14</span></span></td>
<td><span data-ttu-id="e8870-557">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-558">CC004</span><span class="sxs-lookup"><span data-stu-id="e8870-558">CC004</span></span></td>
<td><span data-ttu-id="e8870-559">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="e8870-559">Packaging</span></span></td>
<td><span data-ttu-id="e8870-560">10.</span><span class="sxs-lookup"><span data-stu-id="e8870-560">10</span></span></td>
<td><span data-ttu-id="e8870-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="e8870-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e8870-562">124.57</span><span class="sxs-lookup"><span data-stu-id="e8870-562">124.57</span></span></td>
<td><span data-ttu-id="e8870-563">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8870-564">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="e8870-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-565">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-565">Cost object</span></span></th>
<th><span data-ttu-id="e8870-566">Lielums</span><span class="sxs-lookup"><span data-stu-id="e8870-566">Magnitude</span></span></th>
<th><span data-ttu-id="e8870-567">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="e8870-567">Allocation factor</span></span></th>
<th><span data-ttu-id="e8870-568">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-568">Amount</span></span></th>
<th><span data-ttu-id="e8870-569">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="e8870-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-570">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-570">CC003</span></span></td>
<td><span data-ttu-id="e8870-571">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-571">Assembly</span></span></td>
<td><span data-ttu-id="e8870-572">65</span><span class="sxs-lookup"><span data-stu-id="e8870-572">65</span></span></td>
<td><span data-ttu-id="e8870-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e8870-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e8870-574">438.75</span><span class="sxs-lookup"><span data-stu-id="e8870-574">438.75</span></span></td>
<td><span data-ttu-id="e8870-575">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-576">CC004</span><span class="sxs-lookup"><span data-stu-id="e8870-576">CC004</span></span></td>
<td><span data-ttu-id="e8870-577">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="e8870-577">Packaging</span></span></td>
<td><span data-ttu-id="e8870-578">35</span><span class="sxs-lookup"><span data-stu-id="e8870-578">35</span></span></td>
<td><span data-ttu-id="e8870-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e8870-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e8870-580">236.25</span><span class="sxs-lookup"><span data-stu-id="e8870-580">236.25</span></span></td>
<td><span data-ttu-id="e8870-581">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-582">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-582">CC003</span></span></td>
<td><span data-ttu-id="e8870-583">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-583">Assembly</span></span></td>
<td><span data-ttu-id="e8870-584">65</span><span class="sxs-lookup"><span data-stu-id="e8870-584">65</span></span></td>
<td><span data-ttu-id="e8870-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e8870-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e8870-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e8870-586">5,297.69</span></span></td>
<td><span data-ttu-id="e8870-587">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-588">CC004</span><span class="sxs-lookup"><span data-stu-id="e8870-588">CC004</span></span></td>
<td><span data-ttu-id="e8870-589">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="e8870-589">Packaging</span></span></td>
<td><span data-ttu-id="e8870-590">35</span><span class="sxs-lookup"><span data-stu-id="e8870-590">35</span></span></td>
<td><span data-ttu-id="e8870-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e8870-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e8870-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e8870-592">2,852.60</span></span></td>
<td><span data-ttu-id="e8870-593">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8870-594">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="e8870-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-595">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-595">Cost object</span></span></th>
<th><span data-ttu-id="e8870-596">Lielums</span><span class="sxs-lookup"><span data-stu-id="e8870-596">Magnitude</span></span></th>
<th><span data-ttu-id="e8870-597">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="e8870-597">Allocation factor</span></span></th>
<th><span data-ttu-id="e8870-598">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-598">Amount</span></span></th>
<th><span data-ttu-id="e8870-599">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="e8870-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e8870-600">Prod 1</span></span></td>
<td><span data-ttu-id="e8870-601">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-601">Product 1</span></span></td>
<td><span data-ttu-id="e8870-602">60</span><span class="sxs-lookup"><span data-stu-id="e8870-602">60</span></span></td>
<td><span data-ttu-id="e8870-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e8870-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e8870-604">535.31</span><span class="sxs-lookup"><span data-stu-id="e8870-604">535.31</span></span></td>
<td><span data-ttu-id="e8870-605">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e8870-606">Prod 2</span></span></td>
<td><span data-ttu-id="e8870-607">2. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-607">Product 2</span></span></td>
<td><span data-ttu-id="e8870-608">20.</span><span class="sxs-lookup"><span data-stu-id="e8870-608">20</span></span></td>
<td><span data-ttu-id="e8870-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e8870-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e8870-610">178.44</span><span class="sxs-lookup"><span data-stu-id="e8870-610">178.44</span></span></td>
<td><span data-ttu-id="e8870-611">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e8870-612">Prod 1</span></span></td>
<td><span data-ttu-id="e8870-613">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-613">Product 1</span></span></td>
<td><span data-ttu-id="e8870-614">60</span><span class="sxs-lookup"><span data-stu-id="e8870-614">60</span></span></td>
<td><span data-ttu-id="e8870-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e8870-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e8870-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e8870-616">4,487.12</span></span></td>
<td><span data-ttu-id="e8870-617">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e8870-618">Prod 2</span></span></td>
<td><span data-ttu-id="e8870-619">2. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-619">Product 2</span></span></td>
<td><span data-ttu-id="e8870-620">20.</span><span class="sxs-lookup"><span data-stu-id="e8870-620">20</span></span></td>
<td><span data-ttu-id="e8870-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e8870-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e8870-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e8870-622">1,495.71</span></span></td>
<td><span data-ttu-id="e8870-623">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e8870-624">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="e8870-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-625">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-625">Cost object</span></span></th>
<th><span data-ttu-id="e8870-626">Lielums</span><span class="sxs-lookup"><span data-stu-id="e8870-626">Magnitude</span></span></th>
<th><span data-ttu-id="e8870-627">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="e8870-627">Allocation factor</span></span></th>
<th><span data-ttu-id="e8870-628">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-628">Amount</span></span></th>
<th><span data-ttu-id="e8870-629">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="e8870-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e8870-630">Prod 1</span></span></td>
<td><span data-ttu-id="e8870-631">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-631">Product 1</span></span></td>
<td><span data-ttu-id="e8870-632">80</span><span class="sxs-lookup"><span data-stu-id="e8870-632">80</span></span></td>
<td><span data-ttu-id="e8870-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e8870-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e8870-634">241.05</span><span class="sxs-lookup"><span data-stu-id="e8870-634">241.05</span></span></td>
<td><span data-ttu-id="e8870-635">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e8870-636">Prod 2</span></span></td>
<td><span data-ttu-id="e8870-637">2. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-637">Product 2</span></span></td>
<td><span data-ttu-id="e8870-638">15</span><span class="sxs-lookup"><span data-stu-id="e8870-638">15</span></span></td>
<td><span data-ttu-id="e8870-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e8870-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e8870-640">45.20</span><span class="sxs-lookup"><span data-stu-id="e8870-640">45.20</span></span></td>
<td><span data-ttu-id="e8870-641">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e8870-642">Prod 1</span></span></td>
<td><span data-ttu-id="e8870-643">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-643">Product 1</span></span></td>
<td><span data-ttu-id="e8870-644">80</span><span class="sxs-lookup"><span data-stu-id="e8870-644">80</span></span></td>
<td><span data-ttu-id="e8870-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e8870-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e8870-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e8870-646">2,507.09</span></span></td>
<td><span data-ttu-id="e8870-647">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e8870-648">Prod 2</span></span></td>
<td><span data-ttu-id="e8870-649">2. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-649">Product 2</span></span></td>
<td><span data-ttu-id="e8870-650">15</span><span class="sxs-lookup"><span data-stu-id="e8870-650">15</span></span></td>
<td><span data-ttu-id="e8870-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e8870-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e8870-652">470.08</span><span class="sxs-lookup"><span data-stu-id="e8870-652">470.08</span></span></td>
<td><span data-ttu-id="e8870-653">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e8870-654">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="e8870-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e8870-655">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="e8870-655">Journal</span></span></th>
<th><span data-ttu-id="e8870-656">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="e8870-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e8870-657">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="e8870-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e8870-658">Versija</span><span class="sxs-lookup"><span data-stu-id="e8870-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-659">00004</span><span class="sxs-lookup"><span data-stu-id="e8870-659">00004</span></span></td>
<td><span data-ttu-id="e8870-660">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="e8870-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="e8870-661">Finanšu</span><span class="sxs-lookup"><span data-stu-id="e8870-661">Fiscal</span></span></td>
<td><span data-ttu-id="e8870-662">2017</span><span class="sxs-lookup"><span data-stu-id="e8870-662">2017</span></span></td>
<td><span data-ttu-id="e8870-663">Periods 1</span><span class="sxs-lookup"><span data-stu-id="e8870-663">Period 1</span></span></td>
<td><span data-ttu-id="e8870-664">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="e8870-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="e8870-665">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="e8870-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e8870-666">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="e8870-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e8870-667">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e8870-668">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="e8870-668">Cost element</span></span></th>
<th><span data-ttu-id="e8870-669">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="e8870-669">Cost behavior</span></span></th>
<th><span data-ttu-id="e8870-670">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-671">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-672">CC001</span><span class="sxs-lookup"><span data-stu-id="e8870-672">CC001</span></span></td>
<td><span data-ttu-id="e8870-673">HR</span><span class="sxs-lookup"><span data-stu-id="e8870-673">HR</span></span></td>
<td><span data-ttu-id="e8870-674">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-674">10001</span></span></td>
<td><span data-ttu-id="e8870-675">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-675">Electricity</span></span></td>
<td><span data-ttu-id="e8870-676">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-676">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-677">500,00</span><span class="sxs-lookup"><span data-stu-id="e8870-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-678">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-679">CC001</span><span class="sxs-lookup"><span data-stu-id="e8870-679">CC001</span></span></td>
<td><span data-ttu-id="e8870-680">HR</span><span class="sxs-lookup"><span data-stu-id="e8870-680">HR</span></span></td>
<td><span data-ttu-id="e8870-681">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-681">10001</span></span></td>
<td><span data-ttu-id="e8870-682">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-682">Electricity</span></span></td>
<td><span data-ttu-id="e8870-683">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-683">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="e8870-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-685">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-686">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-686">CC002</span></span></td>
<td><span data-ttu-id="e8870-687">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-687">Finance</span></span></td>
<td><span data-ttu-id="e8870-688">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-688">10001</span></span></td>
<td><span data-ttu-id="e8870-689">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-689">Electricity</span></span></td>
<td><span data-ttu-id="e8870-690">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-690">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-691">675.00</span><span class="sxs-lookup"><span data-stu-id="e8870-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-692">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-693">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-693">CC002</span></span></td>
<td><span data-ttu-id="e8870-694">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-694">Finance</span></span></td>
<td><span data-ttu-id="e8870-695">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-695">10001</span></span></td>
<td><span data-ttu-id="e8870-696">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-696">Electricity</span></span></td>
<td><span data-ttu-id="e8870-697">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-697">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="e8870-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-699">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-700">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-700">CC003</span></span></td>
<td><span data-ttu-id="e8870-701">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-701">Assembly</span></span></td>
<td><span data-ttu-id="e8870-702">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-702">10001</span></span></td>
<td><span data-ttu-id="e8870-703">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-703">Electricity</span></span></td>
<td><span data-ttu-id="e8870-704">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-704">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-705">713.75</span><span class="sxs-lookup"><span data-stu-id="e8870-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-706">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-707">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-707">CC003</span></span></td>
<td><span data-ttu-id="e8870-708">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-708">Assembly</span></span></td>
<td><span data-ttu-id="e8870-709">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-709">10001</span></span></td>
<td><span data-ttu-id="e8870-710">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-710">Electricity</span></span></td>
<td><span data-ttu-id="e8870-711">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-711">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="e8870-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-713">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-714">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-714">CC003</span></span></td>
<td><span data-ttu-id="e8870-715">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="e8870-715">Packaging</span></span></td>
<td><span data-ttu-id="e8870-716">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-716">10001</span></span></td>
<td><span data-ttu-id="e8870-717">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-717">Electricity</span></span></td>
<td><span data-ttu-id="e8870-718">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-718">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-719">286.25</span><span class="sxs-lookup"><span data-stu-id="e8870-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-720">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-721">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-721">CC003</span></span></td>
<td><span data-ttu-id="e8870-722">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="e8870-722">Packaging</span></span></td>
<td><span data-ttu-id="e8870-723">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-723">10001</span></span></td>
<td><span data-ttu-id="e8870-724">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-724">Electricity</span></span></td>
<td><span data-ttu-id="e8870-725">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-725">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="e8870-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-727">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e8870-728">Prod 1</span></span></td>
<td><span data-ttu-id="e8870-729">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-729">Product 1</span></span></td>
<td><span data-ttu-id="e8870-730">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-730">10001</span></span></td>
<td><span data-ttu-id="e8870-731">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-731">Electricity</span></span></td>
<td><span data-ttu-id="e8870-732">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-732">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-733">776.36</span><span class="sxs-lookup"><span data-stu-id="e8870-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-734">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e8870-735">Prod 1</span></span></td>
<td><span data-ttu-id="e8870-736">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-736">Product 1</span></span></td>
<td><span data-ttu-id="e8870-737">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-737">10001</span></span></td>
<td><span data-ttu-id="e8870-738">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-738">Electricity</span></span></td>
<td><span data-ttu-id="e8870-739">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-739">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e8870-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-741">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e8870-742">Prod 2</span></span></td>
<td><span data-ttu-id="e8870-743">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-743">Product 1</span></span></td>
<td><span data-ttu-id="e8870-744">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-744">10001</span></span></td>
<td><span data-ttu-id="e8870-745">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-745">Electricity</span></span></td>
<td><span data-ttu-id="e8870-746">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-746">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-747">223.64</span><span class="sxs-lookup"><span data-stu-id="e8870-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-748">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="e8870-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e8870-749">Prod 2</span></span></td>
<td><span data-ttu-id="e8870-750">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-750">Product 1</span></span></td>
<td><span data-ttu-id="e8870-751">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-751">10001</span></span></td>
<td><span data-ttu-id="e8870-752">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-752">Electricity</span></span></td>
<td><span data-ttu-id="e8870-753">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-753">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e8870-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e8870-755">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="e8870-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e8870-756">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e8870-757">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="e8870-757">Cost element</span></span></th>
<th><span data-ttu-id="e8870-758">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="e8870-758">Cost behavior</span></span></th>
<th><span data-ttu-id="e8870-759">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-759">Amount</span></span></th>
<th><span data-ttu-id="e8870-760">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="e8870-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e8870-761">CC001</span><span class="sxs-lookup"><span data-stu-id="e8870-761">CC001</span></span></td>
<td><span data-ttu-id="e8870-762">HR</span><span class="sxs-lookup"><span data-stu-id="e8870-762">HR</span></span></td>
<td><span data-ttu-id="e8870-763">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-763">10001</span></span></td>
<td><span data-ttu-id="e8870-764">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-764">Electricity</span></span></td>
<td><span data-ttu-id="e8870-765">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-765">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="e8870-766">-500.00</span></span></td>
<td><span data-ttu-id="e8870-767">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-768">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-768">CC002</span></span></td>
<td><span data-ttu-id="e8870-769">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-769">Finance</span></span></td>
<td><span data-ttu-id="e8870-770">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-770">10001</span></span></td>
<td><span data-ttu-id="e8870-771">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-771">Electricity</span></span></td>
<td><span data-ttu-id="e8870-772">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-772">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-773">175.00</span><span class="sxs-lookup"><span data-stu-id="e8870-773">175.00</span></span></td>
<td><span data-ttu-id="e8870-774">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-775">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-775">CC003</span></span></td>
<td><span data-ttu-id="e8870-776">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-776">Assembly</span></span></td>
<td><span data-ttu-id="e8870-777">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-777">10001</span></span></td>
<td><span data-ttu-id="e8870-778">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-778">Electricity</span></span></td>
<td><span data-ttu-id="e8870-779">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-779">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-780">275.00</span><span class="sxs-lookup"><span data-stu-id="e8870-780">275.00</span></span></td>
<td><span data-ttu-id="e8870-781">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-782">CC004</span><span class="sxs-lookup"><span data-stu-id="e8870-782">CC004</span></span></td>
<td><span data-ttu-id="e8870-783">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="e8870-783">Packaging</span></span></td>
<td><span data-ttu-id="e8870-784">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-784">10001</span></span></td>
<td><span data-ttu-id="e8870-785">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-785">Electricity</span></span></td>
<td><span data-ttu-id="e8870-786">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-786">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-787">50,00</span><span class="sxs-lookup"><span data-stu-id="e8870-787">50,00</span></span></td>
<td><span data-ttu-id="e8870-788">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-789">CC001</span><span class="sxs-lookup"><span data-stu-id="e8870-789">CC001</span></span></td>
<td><span data-ttu-id="e8870-790">HR</span><span class="sxs-lookup"><span data-stu-id="e8870-790">HR</span></span></td>
<td><span data-ttu-id="e8870-791">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-791">10001</span></span></td>
<td><span data-ttu-id="e8870-792">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-792">Electricity</span></span></td>
<td><span data-ttu-id="e8870-793">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-793">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="e8870-794">-1,245.71</span></span></td>
<td><span data-ttu-id="e8870-795">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-796">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-796">CC002</span></span></td>
<td><span data-ttu-id="e8870-797">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-797">Finance</span></span></td>
<td><span data-ttu-id="e8870-798">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-798">10001</span></span></td>
<td><span data-ttu-id="e8870-799">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-799">Electricity</span></span></td>
<td><span data-ttu-id="e8870-800">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-800">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-801">436.00</span><span class="sxs-lookup"><span data-stu-id="e8870-801">436.00</span></span></td>
<td><span data-ttu-id="e8870-802">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-803">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-803">CC003</span></span></td>
<td><span data-ttu-id="e8870-804">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-804">Assembly</span></span></td>
<td><span data-ttu-id="e8870-805">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-805">10001</span></span></td>
<td><span data-ttu-id="e8870-806">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-806">Electricity</span></span></td>
<td><span data-ttu-id="e8870-807">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-807">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-808">685.14</span><span class="sxs-lookup"><span data-stu-id="e8870-808">685.14</span></span></td>
<td><span data-ttu-id="e8870-809">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-810">CC004</span><span class="sxs-lookup"><span data-stu-id="e8870-810">CC004</span></span></td>
<td><span data-ttu-id="e8870-811">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="e8870-811">Packaging</span></span></td>
<td><span data-ttu-id="e8870-812">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-812">10001</span></span></td>
<td><span data-ttu-id="e8870-813">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-813">Electricity</span></span></td>
<td><span data-ttu-id="e8870-814">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-814">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-815">124.57</span><span class="sxs-lookup"><span data-stu-id="e8870-815">124.57</span></span></td>
<td><span data-ttu-id="e8870-816">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-817">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-817">CC002</span></span></td>
<td><span data-ttu-id="e8870-818">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-818">Finance</span></span></td>
<td><span data-ttu-id="e8870-819">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-819">10001</span></span></td>
<td><span data-ttu-id="e8870-820">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-820">Electricity</span></span></td>
<td><span data-ttu-id="e8870-821">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-821">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="e8870-822">-675.00</span></span></td>
<td><span data-ttu-id="e8870-823">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-824">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-824">CC003</span></span></td>
<td><span data-ttu-id="e8870-825">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-825">Assembly</span></span></td>
<td><span data-ttu-id="e8870-826">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-826">10001</span></span></td>
<td><span data-ttu-id="e8870-827">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-827">Electricity</span></span></td>
<td><span data-ttu-id="e8870-828">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-828">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-829">438.75</span><span class="sxs-lookup"><span data-stu-id="e8870-829">438.75</span></span></td>
<td><span data-ttu-id="e8870-830">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-831">CC004</span><span class="sxs-lookup"><span data-stu-id="e8870-831">CC004</span></span></td>
<td><span data-ttu-id="e8870-832">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="e8870-832">Packaging</span></span></td>
<td><span data-ttu-id="e8870-833">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-833">10001</span></span></td>
<td><span data-ttu-id="e8870-834">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-834">Electricity</span></span></td>
<td><span data-ttu-id="e8870-835">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-835">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-836">236.25</span><span class="sxs-lookup"><span data-stu-id="e8870-836">236.25</span></span></td>
<td><span data-ttu-id="e8870-837">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-838">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-838">CC002</span></span></td>
<td><span data-ttu-id="e8870-839">Finanses</span><span class="sxs-lookup"><span data-stu-id="e8870-839">Finance</span></span></td>
<td><span data-ttu-id="e8870-840">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-840">10001</span></span></td>
<td><span data-ttu-id="e8870-841">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-841">Electricity</span></span></td>
<td><span data-ttu-id="e8870-842">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-842">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="e8870-843">-8,150.29</span></span></td>
<td><span data-ttu-id="e8870-844">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-845">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-845">CC003</span></span></td>
<td><span data-ttu-id="e8870-846">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-846">Assembly</span></span></td>
<td><span data-ttu-id="e8870-847">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-847">10001</span></span></td>
<td><span data-ttu-id="e8870-848">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-848">Electricity</span></span></td>
<td><span data-ttu-id="e8870-849">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-849">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e8870-850">5,297.69</span></span></td>
<td><span data-ttu-id="e8870-851">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-852">CC004</span><span class="sxs-lookup"><span data-stu-id="e8870-852">CC004</span></span></td>
<td><span data-ttu-id="e8870-853">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="e8870-853">Packaging</span></span></td>
<td><span data-ttu-id="e8870-854">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-854">10001</span></span></td>
<td><span data-ttu-id="e8870-855">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-855">Electricity</span></span></td>
<td><span data-ttu-id="e8870-856">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-856">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e8870-857">2,852.60</span></span></td>
<td><span data-ttu-id="e8870-858">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-859">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-859">CC003</span></span></td>
<td><span data-ttu-id="e8870-860">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-860">Assembly</span></span></td>
<td><span data-ttu-id="e8870-861">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-861">10001</span></span></td>
<td><span data-ttu-id="e8870-862">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-862">Electricity</span></span></td>
<td><span data-ttu-id="e8870-863">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-863">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="e8870-864">-713.75</span></span></td>
<td><span data-ttu-id="e8870-865">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e8870-866">Prod 1</span></span></td>
<td><span data-ttu-id="e8870-867">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-867">Product 1</span></span></td>
<td><span data-ttu-id="e8870-868">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-868">10001</span></span></td>
<td><span data-ttu-id="e8870-869">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-869">Electricity</span></span></td>
<td><span data-ttu-id="e8870-870">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-870">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-871">535.31</span><span class="sxs-lookup"><span data-stu-id="e8870-871">535.31</span></span></td>
<td><span data-ttu-id="e8870-872">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e8870-873">Prod 2</span></span></td>
<td><span data-ttu-id="e8870-874">2. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-874">Product 2</span></span></td>
<td><span data-ttu-id="e8870-875">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-875">10001</span></span></td>
<td><span data-ttu-id="e8870-876">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-876">Electricity</span></span></td>
<td><span data-ttu-id="e8870-877">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-877">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-878">178.44</span><span class="sxs-lookup"><span data-stu-id="e8870-878">178.44</span></span></td>
<td><span data-ttu-id="e8870-879">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-880">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-880">CC003</span></span></td>
<td><span data-ttu-id="e8870-881">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-881">Assembly</span></span></td>
<td><span data-ttu-id="e8870-882">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-882">10001</span></span></td>
<td><span data-ttu-id="e8870-883">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-883">Electricity</span></span></td>
<td><span data-ttu-id="e8870-884">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-884">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="e8870-885">-5,982.83</span></span></td>
<td><span data-ttu-id="e8870-886">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e8870-887">Prod 1</span></span></td>
<td><span data-ttu-id="e8870-888">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-888">Product 1</span></span></td>
<td><span data-ttu-id="e8870-889">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-889">10001</span></span></td>
<td><span data-ttu-id="e8870-890">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-890">Electricity</span></span></td>
<td><span data-ttu-id="e8870-891">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-891">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e8870-892">4,487.12</span></span></td>
<td><span data-ttu-id="e8870-893">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e8870-894">Prod 2</span></span></td>
<td><span data-ttu-id="e8870-895">2. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-895">Product 2</span></span></td>
<td><span data-ttu-id="e8870-896">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-896">10001</span></span></td>
<td><span data-ttu-id="e8870-897">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-897">Electricity</span></span></td>
<td><span data-ttu-id="e8870-898">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-898">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e8870-899">1,495.71</span></span></td>
<td><span data-ttu-id="e8870-900">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-901">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-901">CC003</span></span></td>
<td><span data-ttu-id="e8870-902">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-902">Assembly</span></span></td>
<td><span data-ttu-id="e8870-903">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-903">10001</span></span></td>
<td><span data-ttu-id="e8870-904">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-904">Electricity</span></span></td>
<td><span data-ttu-id="e8870-905">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-905">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="e8870-906">-286.25</span></span></td>
<td><span data-ttu-id="e8870-907">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e8870-908">Prod 1</span></span></td>
<td><span data-ttu-id="e8870-909">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-909">Product 1</span></span></td>
<td><span data-ttu-id="e8870-910">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-910">10001</span></span></td>
<td><span data-ttu-id="e8870-911">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-911">Electricity</span></span></td>
<td><span data-ttu-id="e8870-912">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-912">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-913">241.05</span><span class="sxs-lookup"><span data-stu-id="e8870-913">241.05</span></span></td>
<td><span data-ttu-id="e8870-914">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e8870-915">Prod 2</span></span></td>
<td><span data-ttu-id="e8870-916">2. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-916">Product 2</span></span></td>
<td><span data-ttu-id="e8870-917">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-917">10001</span></span></td>
<td><span data-ttu-id="e8870-918">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-918">Electricity</span></span></td>
<td><span data-ttu-id="e8870-919">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-919">Fixed cost</span></span></td>
<td><span data-ttu-id="e8870-920">45.20</span><span class="sxs-lookup"><span data-stu-id="e8870-920">45.20</span></span></td>
<td><span data-ttu-id="e8870-921">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-922">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-922">CC003</span></span></td>
<td><span data-ttu-id="e8870-923">Montāža</span><span class="sxs-lookup"><span data-stu-id="e8870-923">Assembly</span></span></td>
<td><span data-ttu-id="e8870-924">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-924">10001</span></span></td>
<td><span data-ttu-id="e8870-925">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-925">Electricity</span></span></td>
<td><span data-ttu-id="e8870-926">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-926">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="e8870-927">-2,977.17</span></span></td>
<td><span data-ttu-id="e8870-928">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e8870-929">Prod 1</span></span></td>
<td><span data-ttu-id="e8870-930">1. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-930">Product 1</span></span></td>
<td><span data-ttu-id="e8870-931">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-931">10001</span></span></td>
<td><span data-ttu-id="e8870-932">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-932">Electricity</span></span></td>
<td><span data-ttu-id="e8870-933">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-933">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e8870-934">2,507.09</span></span></td>
<td><span data-ttu-id="e8870-935">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e8870-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e8870-936">Prod 2</span></span></td>
<td><span data-ttu-id="e8870-937">2. prece</span><span class="sxs-lookup"><span data-stu-id="e8870-937">Product 2</span></span></td>
<td><span data-ttu-id="e8870-938">10001</span><span class="sxs-lookup"><span data-stu-id="e8870-938">10001</span></span></td>
<td><span data-ttu-id="e8870-939">Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-939">Electricity</span></span></td>
<td><span data-ttu-id="e8870-940">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-940">Variable cost</span></span></td>
<td><span data-ttu-id="e8870-941">470.08</span><span class="sxs-lookup"><span data-stu-id="e8870-941">470.08</span></span></td>
<td><span data-ttu-id="e8870-942">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="e8870-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="e8870-943">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="e8870-943">Conclusion</span></span>
<span data-ttu-id="e8870-944">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="e8870-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="e8870-945">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="e8870-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="e8870-946">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="e8870-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="e8870-947">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="e8870-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="e8870-948">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="e8870-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="e8870-949">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="e8870-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="e8870-950">Summa</span><span class="sxs-lookup"><span data-stu-id="e8870-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e8870-951">CC099</span><span class="sxs-lookup"><span data-stu-id="e8870-951">CC099</span></span></th>
<th><span data-ttu-id="e8870-952">CC001</span><span class="sxs-lookup"><span data-stu-id="e8870-952">CC001</span></span></th>
<th><span data-ttu-id="e8870-953">CC002</span><span class="sxs-lookup"><span data-stu-id="e8870-953">CC002</span></span></th>
<th><span data-ttu-id="e8870-954">CC003</span><span class="sxs-lookup"><span data-stu-id="e8870-954">CC003</span></span></th>
<th><span data-ttu-id="e8870-955">CC004</span><span class="sxs-lookup"><span data-stu-id="e8870-955">CC004</span></span></th>
<th><span data-ttu-id="e8870-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e8870-956">Proj 1</span></span></th>
<th><span data-ttu-id="e8870-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e8870-957">Proj 2</span></span></th>
<th><span data-ttu-id="e8870-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e8870-958">Prod 1</span></span></th>
<th><span data-ttu-id="e8870-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e8870-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="e8870-960">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="e8870-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e8870-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e8870-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e8870-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e8870-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e8870-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="e8870-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="e8870-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="e8870-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="e8870-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e8870-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="e8870-970">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="e8870-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-971">0,00</span><span class="sxs-lookup"><span data-stu-id="e8870-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="e8870-972">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-973">0,00</span><span class="sxs-lookup"><span data-stu-id="e8870-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-974">0,00</span><span class="sxs-lookup"><span data-stu-id="e8870-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-975">0,00</span><span class="sxs-lookup"><span data-stu-id="e8870-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-976">0,00</span><span class="sxs-lookup"><span data-stu-id="e8870-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-977">0,00</span><span class="sxs-lookup"><span data-stu-id="e8870-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e8870-978">776.36</span><span class="sxs-lookup"><span data-stu-id="e8870-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-979">223.64</span><span class="sxs-lookup"><span data-stu-id="e8870-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e8870-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="e8870-981">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="e8870-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-982">000</span><span class="sxs-lookup"><span data-stu-id="e8870-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-983">0,00</span><span class="sxs-lookup"><span data-stu-id="e8870-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-984">0,00</span><span class="sxs-lookup"><span data-stu-id="e8870-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-985">0,00</span><span class="sxs-lookup"><span data-stu-id="e8870-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-986">0,00</span><span class="sxs-lookup"><span data-stu-id="e8870-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-987">30,00</span><span class="sxs-lookup"><span data-stu-id="e8870-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-988">10,00</span><span class="sxs-lookup"><span data-stu-id="e8870-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e8870-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e8870-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e8870-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e8870-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e8870-992">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="e8870-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="e8870-993">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="e8870-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="e8870-994">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="e8870-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="e8870-995">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="e8870-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="e8870-996">Plašāku informāciju skatiet [Izmaksu apkopojuma politika un pieskaitāmo izmaksu aprēķins](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="e8870-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



