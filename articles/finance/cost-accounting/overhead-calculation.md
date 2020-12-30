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
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445700"
---
# <a name="overhead-calculation"></a><span data-ttu-id="299bb-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="299bb-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="299bb-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="299bb-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="299bb-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="299bb-105">Term definition</span></span>
---------------

<span data-ttu-id="299bb-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="299bb-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="299bb-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="299bb-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="299bb-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="299bb-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="299bb-109">Īre</span><span class="sxs-lookup"><span data-stu-id="299bb-109">Rent</span></span>
-   <span data-ttu-id="299bb-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-110">Electricity</span></span>
-   <span data-ttu-id="299bb-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="299bb-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="299bb-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="299bb-112">Overhead calculation overview</span></span>
<span data-ttu-id="299bb-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="299bb-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="299bb-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="299bb-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="299bb-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="299bb-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="299bb-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="299bb-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="299bb-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="299bb-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="299bb-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="299bb-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="299bb-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="299bb-119">Version type</span></span>
-   <span data-ttu-id="299bb-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="299bb-120">Date and time</span></span>
-   <span data-ttu-id="299bb-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="299bb-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="299bb-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="299bb-122">Fiscal year</span></span>
-   <span data-ttu-id="299bb-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="299bb-123">Fiscal period</span></span>

<span data-ttu-id="299bb-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="299bb-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="299bb-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="299bb-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="299bb-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="299bb-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="299bb-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="299bb-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="299bb-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="299bb-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="299bb-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="299bb-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="299bb-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="299bb-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="299bb-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="299bb-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="299bb-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="299bb-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="299bb-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="299bb-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="299bb-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="299bb-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="299bb-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="299bb-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="299bb-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="299bb-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="299bb-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="299bb-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="299bb-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="299bb-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="299bb-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="299bb-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="299bb-140">Main account</span></span></th>
<th><span data-ttu-id="299bb-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="299bb-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="299bb-143">CC099</span><span class="sxs-lookup"><span data-stu-id="299bb-143">CC099</span></span></td>
<td><span data-ttu-id="299bb-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="299bb-144">Default cost center</span></span></td>
<td><span data-ttu-id="299bb-145">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-145">10001</span></span></td>
<td><span data-ttu-id="299bb-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-146">Electricity</span></span></td>
<td><span data-ttu-id="299bb-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="299bb-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="299bb-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="299bb-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="299bb-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="299bb-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="299bb-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="299bb-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="299bb-151">Define the cost behavior rule</span></span>

<span data-ttu-id="299bb-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="299bb-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="299bb-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="299bb-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="299bb-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="299bb-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="299bb-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="299bb-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="299bb-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="299bb-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="299bb-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="299bb-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="299bb-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="299bb-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="299bb-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="299bb-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="299bb-160">Journal</span></span></th>
<th><span data-ttu-id="299bb-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="299bb-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="299bb-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="299bb-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="299bb-163">Versija</span><span class="sxs-lookup"><span data-stu-id="299bb-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-164">00001</span><span class="sxs-lookup"><span data-stu-id="299bb-164">00001</span></span></td>
<td><span data-ttu-id="299bb-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="299bb-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="299bb-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="299bb-166">Fiscal</span></span></td>
<td><span data-ttu-id="299bb-167">2017</span><span class="sxs-lookup"><span data-stu-id="299bb-167">2017</span></span></td>
<td><span data-ttu-id="299bb-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="299bb-168">Period 1</span></span></td>
<td><span data-ttu-id="299bb-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="299bb-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="299bb-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="299bb-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="299bb-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="299bb-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="299bb-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="299bb-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="299bb-173">Cost element</span></span></th>
<th><span data-ttu-id="299bb-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="299bb-174">Cost behavior</span></span></th>
<th><span data-ttu-id="299bb-175">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="299bb-177">CC099</span><span class="sxs-lookup"><span data-stu-id="299bb-177">CC099</span></span></td>
<td><span data-ttu-id="299bb-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="299bb-178">Default cost center</span></span></td>
<td><span data-ttu-id="299bb-179">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-179">10001</span></span></td>
<td><span data-ttu-id="299bb-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-180">Electricity</span></span></td>
<td><span data-ttu-id="299bb-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="299bb-181">Unclassified</span></span></td>
<td><span data-ttu-id="299bb-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="299bb-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="299bb-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="299bb-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="299bb-185">Cost element</span></span></th>
<th><span data-ttu-id="299bb-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="299bb-186">Cost behavior</span></span></th>
<th><span data-ttu-id="299bb-187">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-187">Amount</span></span></th>
<th><span data-ttu-id="299bb-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="299bb-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-189">CC099</span><span class="sxs-lookup"><span data-stu-id="299bb-189">CC099</span></span></td>
<td><span data-ttu-id="299bb-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="299bb-190">Default cost center</span></span></td>
<td><span data-ttu-id="299bb-191">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-191">10001</span></span></td>
<td><span data-ttu-id="299bb-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-192">Electricity</span></span></td>
<td><span data-ttu-id="299bb-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="299bb-193">Unclassified</span></span></td>
<td><span data-ttu-id="299bb-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-194">10,000.00</span></span></td>
<td><span data-ttu-id="299bb-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-196">CC099</span><span class="sxs-lookup"><span data-stu-id="299bb-196">CC099</span></span></td>
<td><span data-ttu-id="299bb-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="299bb-197">Default cost center</span></span></td>
<td><span data-ttu-id="299bb-198">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-198">10001</span></span></td>
<td><span data-ttu-id="299bb-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-199">Electricity</span></span></td>
<td><span data-ttu-id="299bb-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="299bb-200">Unclassified</span></span></td>
<td><span data-ttu-id="299bb-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-201">-10,000.00</span></span></td>
<td><span data-ttu-id="299bb-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-203">CC099</span><span class="sxs-lookup"><span data-stu-id="299bb-203">CC099</span></span></td>
<td><span data-ttu-id="299bb-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="299bb-204">Default cost center</span></span></td>
<td><span data-ttu-id="299bb-205">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-205">10001</span></span></td>
<td><span data-ttu-id="299bb-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-206">Electricity</span></span></td>
<td><span data-ttu-id="299bb-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-207">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-208">1,000.00</span></span></td>
<td><span data-ttu-id="299bb-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-210">CC099</span><span class="sxs-lookup"><span data-stu-id="299bb-210">CC099</span></span></td>
<td><span data-ttu-id="299bb-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="299bb-211">Default cost center</span></span></td>
<td><span data-ttu-id="299bb-212">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-212">10001</span></span></td>
<td><span data-ttu-id="299bb-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-213">Electricity</span></span></td>
<td><span data-ttu-id="299bb-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-214">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="299bb-215">9,000.00</span></span></td>
<td><span data-ttu-id="299bb-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="299bb-217">Sīkāku informāciju skatiet šeit: [Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="299bb-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="299bb-218">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="299bb-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="299bb-219">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="299bb-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="299bb-220">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="299bb-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="299bb-221">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="299bb-221">Define the cost distribution rule</span></span>

<span data-ttu-id="299bb-222">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="299bb-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="299bb-223">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="299bb-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="299bb-224">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="299bb-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="299bb-225">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="299bb-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="299bb-226">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="299bb-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="299bb-227">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="299bb-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-228">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-228">Cost object</span></span></th>
<th><span data-ttu-id="299bb-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="299bb-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-230">CC001</span><span class="sxs-lookup"><span data-stu-id="299bb-230">CC001</span></span></td>
<td><span data-ttu-id="299bb-231">HR</span><span class="sxs-lookup"><span data-stu-id="299bb-231">HR</span></span></td>
<td><span data-ttu-id="299bb-232">1000</span><span class="sxs-lookup"><span data-stu-id="299bb-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-233">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-233">CC002</span></span></td>
<td><span data-ttu-id="299bb-234">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-234">Finance</span></span></td>
<td><span data-ttu-id="299bb-235">6,000</span><span class="sxs-lookup"><span data-stu-id="299bb-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-236">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-236">CC003</span></span></td>
<td><span data-ttu-id="299bb-237">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-237">Assembly</span></span></td>
<td><span data-ttu-id="299bb-238">0</span><span class="sxs-lookup"><span data-stu-id="299bb-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="299bb-239">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="299bb-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-240">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-240">Cost object</span></span></th>
<th><span data-ttu-id="299bb-241">Lielums</span><span class="sxs-lookup"><span data-stu-id="299bb-241">Magnitude</span></span></th>
<th><span data-ttu-id="299bb-242">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="299bb-242">Allocation factor</span></span></th>
<th><span data-ttu-id="299bb-243">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-244">CC001</span><span class="sxs-lookup"><span data-stu-id="299bb-244">CC001</span></span></td>
<td><span data-ttu-id="299bb-245">HR</span><span class="sxs-lookup"><span data-stu-id="299bb-245">HR</span></span></td>
<td><span data-ttu-id="299bb-246">1000</span><span class="sxs-lookup"><span data-stu-id="299bb-246">1,000</span></span></td>
<td><span data-ttu-id="299bb-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="299bb-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="299bb-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-249">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-249">CC002</span></span></td>
<td><span data-ttu-id="299bb-250">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-250">Finance</span></span></td>
<td><span data-ttu-id="299bb-251">6,000</span><span class="sxs-lookup"><span data-stu-id="299bb-251">6,000</span></span></td>
<td><span data-ttu-id="299bb-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="299bb-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="299bb-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-254">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-254">CC003</span></span></td>
<td><span data-ttu-id="299bb-255">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-255">Assembly</span></span></td>
<td><span data-ttu-id="299bb-256">0</span><span class="sxs-lookup"><span data-stu-id="299bb-256">0</span></span></td>
<td><span data-ttu-id="299bb-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="299bb-258">0,00</span><span class="sxs-lookup"><span data-stu-id="299bb-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="299bb-259">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="299bb-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="299bb-260">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="299bb-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-261">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-261">Cost object</span></span></th>
<th><span data-ttu-id="299bb-262">Formula</span><span class="sxs-lookup"><span data-stu-id="299bb-262">Formula</span></span></th>
<th><span data-ttu-id="299bb-263">Lielums</span><span class="sxs-lookup"><span data-stu-id="299bb-263">Magnitude</span></span></th>
<th><span data-ttu-id="299bb-264">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="299bb-264">Allocation factor</span></span></th>
<th><span data-ttu-id="299bb-265">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-266">CC001</span><span class="sxs-lookup"><span data-stu-id="299bb-266">CC001</span></span></td>
<td><span data-ttu-id="299bb-267">HR</span><span class="sxs-lookup"><span data-stu-id="299bb-267">HR</span></span></td>
<td><span data-ttu-id="299bb-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="299bb-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="299bb-269">1.</span><span class="sxs-lookup"><span data-stu-id="299bb-269">1</span></span></td>
<td><span data-ttu-id="299bb-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="299bb-271">500,00</span><span class="sxs-lookup"><span data-stu-id="299bb-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-272">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-272">CC002</span></span></td>
<td><span data-ttu-id="299bb-273">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-273">Finance</span></span></td>
<td><span data-ttu-id="299bb-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="299bb-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="299bb-275">1.</span><span class="sxs-lookup"><span data-stu-id="299bb-275">1</span></span></td>
<td><span data-ttu-id="299bb-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="299bb-277">500,00</span><span class="sxs-lookup"><span data-stu-id="299bb-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-278">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-278">CC003</span></span></td>
<td><span data-ttu-id="299bb-279">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-279">Assembly</span></span></td>
<td><span data-ttu-id="299bb-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="299bb-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="299bb-281">0</span><span class="sxs-lookup"><span data-stu-id="299bb-281">0</span></span></td>
<td><span data-ttu-id="299bb-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="299bb-283">0,00</span><span class="sxs-lookup"><span data-stu-id="299bb-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="299bb-284">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="299bb-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="299bb-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="299bb-285">Journal</span></span></th>
<th><span data-ttu-id="299bb-286">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="299bb-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="299bb-287">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="299bb-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="299bb-288">Versija</span><span class="sxs-lookup"><span data-stu-id="299bb-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-289">00002</span><span class="sxs-lookup"><span data-stu-id="299bb-289">00002</span></span></td>
<td><span data-ttu-id="299bb-290">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="299bb-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="299bb-291">Finanšu</span><span class="sxs-lookup"><span data-stu-id="299bb-291">Fiscal</span></span></td>
<td><span data-ttu-id="299bb-292">2017</span><span class="sxs-lookup"><span data-stu-id="299bb-292">2017</span></span></td>
<td><span data-ttu-id="299bb-293">Periods 1</span><span class="sxs-lookup"><span data-stu-id="299bb-293">Period 1</span></span></td>
<td><span data-ttu-id="299bb-294">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="299bb-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="299bb-295">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="299bb-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="299bb-296">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="299bb-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="299bb-297">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="299bb-298">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="299bb-298">Cost element</span></span></th>
<th><span data-ttu-id="299bb-299">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="299bb-299">Cost behavior</span></span></th>
<th><span data-ttu-id="299bb-300">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-301">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-302">CC099</span><span class="sxs-lookup"><span data-stu-id="299bb-302">CC099</span></span></td>
<td><span data-ttu-id="299bb-303">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="299bb-303">Default cost center</span></span></td>
<td><span data-ttu-id="299bb-304">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-304">10001</span></span></td>
<td><span data-ttu-id="299bb-305">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-305">Electricity</span></span></td>
<td><span data-ttu-id="299bb-306">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-306">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-308">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-309">CC099</span><span class="sxs-lookup"><span data-stu-id="299bb-309">CC099</span></span></td>
<td><span data-ttu-id="299bb-310">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="299bb-310">Default cost center</span></span></td>
<td><span data-ttu-id="299bb-311">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-311">10001</span></span></td>
<td><span data-ttu-id="299bb-312">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-312">Electricity</span></span></td>
<td><span data-ttu-id="299bb-313">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-313">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="299bb-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="299bb-315">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="299bb-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-316">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="299bb-317">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="299bb-317">Cost element</span></span></th>
<th><span data-ttu-id="299bb-318">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="299bb-318">Cost behavior</span></span></th>
<th><span data-ttu-id="299bb-319">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-319">Amount</span></span></th>
<th><span data-ttu-id="299bb-320">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="299bb-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-321">CC099</span><span class="sxs-lookup"><span data-stu-id="299bb-321">CC099</span></span></td>
<td><span data-ttu-id="299bb-322">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="299bb-322">Default cost center</span></span></td>
<td><span data-ttu-id="299bb-323">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-323">10001</span></span></td>
<td><span data-ttu-id="299bb-324">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-324">Electricity</span></span></td>
<td><span data-ttu-id="299bb-325">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-325">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-326">-1000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-326">-1,000.00</span></span></td>
<td><span data-ttu-id="299bb-327">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-328">CC001</span><span class="sxs-lookup"><span data-stu-id="299bb-328">CC001</span></span></td>
<td><span data-ttu-id="299bb-329">HR</span><span class="sxs-lookup"><span data-stu-id="299bb-329">HR</span></span></td>
<td><span data-ttu-id="299bb-330">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-330">10001</span></span></td>
<td><span data-ttu-id="299bb-331">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-331">Electricity</span></span></td>
<td><span data-ttu-id="299bb-332">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-332">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-333">500,00</span><span class="sxs-lookup"><span data-stu-id="299bb-333">500.00</span></span></td>
<td><span data-ttu-id="299bb-334">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-335">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-335">CC002</span></span></td>
<td><span data-ttu-id="299bb-336">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-336">Finance</span></span></td>
<td><span data-ttu-id="299bb-337">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-337">10001</span></span></td>
<td><span data-ttu-id="299bb-338">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-338">Electricity</span></span></td>
<td><span data-ttu-id="299bb-339">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-339">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-340">500,00</span><span class="sxs-lookup"><span data-stu-id="299bb-340">500.00</span></span></td>
<td><span data-ttu-id="299bb-341">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-342">CC099</span><span class="sxs-lookup"><span data-stu-id="299bb-342">CC099</span></span></td>
<td><span data-ttu-id="299bb-343">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="299bb-343">Default cost center</span></span></td>
<td><span data-ttu-id="299bb-344">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-344">10001</span></span></td>
<td><span data-ttu-id="299bb-345">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-345">Electricity</span></span></td>
<td><span data-ttu-id="299bb-346">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-346">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="299bb-347">-9,000.00</span></span></td>
<td><span data-ttu-id="299bb-348">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-349">CC001</span><span class="sxs-lookup"><span data-stu-id="299bb-349">CC001</span></span></td>
<td><span data-ttu-id="299bb-350">HR</span><span class="sxs-lookup"><span data-stu-id="299bb-350">HR</span></span></td>
<td><span data-ttu-id="299bb-351">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-351">10001</span></span></td>
<td><span data-ttu-id="299bb-352">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-352">Electricity</span></span></td>
<td><span data-ttu-id="299bb-353">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-353">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="299bb-354">1,285.71</span></span></td>
<td><span data-ttu-id="299bb-355">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-356">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-356">CC002</span></span></td>
<td><span data-ttu-id="299bb-357">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-357">Finance</span></span></td>
<td><span data-ttu-id="299bb-358">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-358">10001</span></span></td>
<td><span data-ttu-id="299bb-359">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-359">Electricity</span></span></td>
<td><span data-ttu-id="299bb-360">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-360">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="299bb-361">7,714.29</span></span></td>
<td><span data-ttu-id="299bb-362">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="299bb-363">Sīkāku informāciju skatiet šeit: [Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="299bb-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="299bb-364">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="299bb-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="299bb-365">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="299bb-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="299bb-366">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="299bb-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="299bb-367">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="299bb-367">Define the overhead rate</span></span>

<span data-ttu-id="299bb-368">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="299bb-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="299bb-369">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="299bb-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-370">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-370">Cost object</span></span></th>
<th><span data-ttu-id="299bb-371">Stundas</span><span class="sxs-lookup"><span data-stu-id="299bb-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="299bb-372">Proj 1</span></span></td>
<td><span data-ttu-id="299bb-373">1. projekts</span><span class="sxs-lookup"><span data-stu-id="299bb-373">Project 1</span></span></td>
<td><span data-ttu-id="299bb-374">3.</span><span class="sxs-lookup"><span data-stu-id="299bb-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="299bb-375">Proj 2</span></span></td>
<td><span data-ttu-id="299bb-376">2. projekts</span><span class="sxs-lookup"><span data-stu-id="299bb-376">Project 2</span></span></td>
<td><span data-ttu-id="299bb-377">1.</span><span class="sxs-lookup"><span data-stu-id="299bb-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="299bb-378">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="299bb-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-379">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-379">Cost object</span></span></th>
<th><span data-ttu-id="299bb-380">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="299bb-380">Cost element</span></span></th>
<th><span data-ttu-id="299bb-381">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="299bb-381">Cost behavior</span></span></th>
<th><span data-ttu-id="299bb-382">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="299bb-382">Units</span></span></th>
<th><span data-ttu-id="299bb-383">Likme</span><span class="sxs-lookup"><span data-stu-id="299bb-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-384">CC001</span><span class="sxs-lookup"><span data-stu-id="299bb-384">CC001</span></span></td>
<td><span data-ttu-id="299bb-385">HR</span><span class="sxs-lookup"><span data-stu-id="299bb-385">HR</span></span></td>
<td><span data-ttu-id="299bb-386">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-386">10001</span></span></td>
<td><span data-ttu-id="299bb-387">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-387">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-388">1</span><span class="sxs-lookup"><span data-stu-id="299bb-388">1</span></span></td>
<td><span data-ttu-id="299bb-389">10</span><span class="sxs-lookup"><span data-stu-id="299bb-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="299bb-390">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="299bb-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-391">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-391">Cost object</span></span></th>
<th><span data-ttu-id="299bb-392">Lielums</span><span class="sxs-lookup"><span data-stu-id="299bb-392">Magnitude</span></span></th>
<th><span data-ttu-id="299bb-393">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="299bb-393">Cost element</span></span></th>
<th><span data-ttu-id="299bb-394">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="299bb-394">Allocation factor</span></span></th>
<th><span data-ttu-id="299bb-395">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="299bb-396">Proj 1</span></span></td>
<td><span data-ttu-id="299bb-397">1. projekts</span><span class="sxs-lookup"><span data-stu-id="299bb-397">Project 1</span></span></td>
<td><span data-ttu-id="299bb-398">3.</span><span class="sxs-lookup"><span data-stu-id="299bb-398">3</span></span></td>
<td><span data-ttu-id="299bb-399">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-399">10001</span></span></td>
<td><span data-ttu-id="299bb-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="299bb-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="299bb-401">30,00</span><span class="sxs-lookup"><span data-stu-id="299bb-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="299bb-402">Proj 2</span></span></td>
<td><span data-ttu-id="299bb-403">2. projekts</span><span class="sxs-lookup"><span data-stu-id="299bb-403">Project 2</span></span></td>
<td><span data-ttu-id="299bb-404">1.</span><span class="sxs-lookup"><span data-stu-id="299bb-404">1</span></span></td>
<td><span data-ttu-id="299bb-405">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-405">10001</span></span></td>
<td><span data-ttu-id="299bb-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="299bb-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="299bb-407">10,00</span><span class="sxs-lookup"><span data-stu-id="299bb-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="299bb-408">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="299bb-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="299bb-409">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="299bb-409">Journal</span></span></th>
<th><span data-ttu-id="299bb-410">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="299bb-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="299bb-411">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="299bb-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="299bb-412">Versija</span><span class="sxs-lookup"><span data-stu-id="299bb-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-413">00003</span><span class="sxs-lookup"><span data-stu-id="299bb-413">00003</span></span></td>
<td><span data-ttu-id="299bb-414">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="299bb-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="299bb-415">Finanšu</span><span class="sxs-lookup"><span data-stu-id="299bb-415">Fiscal</span></span></td>
<td><span data-ttu-id="299bb-416">2017</span><span class="sxs-lookup"><span data-stu-id="299bb-416">2017</span></span></td>
<td><span data-ttu-id="299bb-417">Periods 1</span><span class="sxs-lookup"><span data-stu-id="299bb-417">Period 1</span></span></td>
<td><span data-ttu-id="299bb-418">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="299bb-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="299bb-419">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="299bb-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="299bb-420">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="299bb-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="299bb-421">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-421">Cost object</span></span></th>
<th><span data-ttu-id="299bb-422">Lielums</span><span class="sxs-lookup"><span data-stu-id="299bb-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-423">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="299bb-424">Proj 1</span></span></td>
<td><span data-ttu-id="299bb-425">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="299bb-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="299bb-426">3,00</span><span class="sxs-lookup"><span data-stu-id="299bb-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-427">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="299bb-428">Proj 2</span></span></td>
<td><span data-ttu-id="299bb-429">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="299bb-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="299bb-430">1,00</span><span class="sxs-lookup"><span data-stu-id="299bb-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="299bb-431">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="299bb-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-432">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="299bb-433">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="299bb-433">Cost element</span></span></th>
<th><span data-ttu-id="299bb-434">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="299bb-434">Cost behavior</span></span></th>
<th><span data-ttu-id="299bb-435">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-435">Amount</span></span></th>
<th><span data-ttu-id="299bb-436">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="299bb-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="299bb-437">CC0001</span></span></td>
<td><span data-ttu-id="299bb-438">HR</span><span class="sxs-lookup"><span data-stu-id="299bb-438">HR</span></span></td>
<td><span data-ttu-id="299bb-439">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-439">10001</span></span></td>
<td><span data-ttu-id="299bb-440">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-440">Electricity</span></span></td>
<td><span data-ttu-id="299bb-441">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-441">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="299bb-442">-30.00</span></span></td>
<td><span data-ttu-id="299bb-443">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="299bb-444">Proj 1</span></span></td>
<td><span data-ttu-id="299bb-445">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="299bb-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="299bb-446">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-446">10001</span></span></td>
<td><span data-ttu-id="299bb-447">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-447">Electricity</span></span></td>
<td><span data-ttu-id="299bb-448">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-448">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-449">30,00</span><span class="sxs-lookup"><span data-stu-id="299bb-449">30.00</span></span></td>
<td><span data-ttu-id="299bb-450">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-451">CC001</span><span class="sxs-lookup"><span data-stu-id="299bb-451">CC001</span></span></td>
<td><span data-ttu-id="299bb-452">HR</span><span class="sxs-lookup"><span data-stu-id="299bb-452">HR</span></span></td>
<td><span data-ttu-id="299bb-453">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-453">10001</span></span></td>
<td><span data-ttu-id="299bb-454">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-454">Electricity</span></span></td>
<td><span data-ttu-id="299bb-455">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-455">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="299bb-456">-10.00</span></span></td>
<td><span data-ttu-id="299bb-457">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="299bb-458">Proj 2</span></span></td>
<td><span data-ttu-id="299bb-459">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="299bb-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="299bb-460">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-460">10001</span></span></td>
<td><span data-ttu-id="299bb-461">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-461">Electricity</span></span></td>
<td><span data-ttu-id="299bb-462">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-462">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-463">10,00</span><span class="sxs-lookup"><span data-stu-id="299bb-463">10.00</span></span></td>
<td><span data-ttu-id="299bb-464">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="299bb-465">Sīkāku informāciju skatiet šeit: [Pieskaitāmo izmaksu aprēķina veikšana](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="299bb-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="299bb-466">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="299bb-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="299bb-467">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="299bb-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="299bb-468">Finance atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="299bb-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="299bb-469">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="299bb-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="299bb-470">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="299bb-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="299bb-471">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="299bb-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="299bb-472">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="299bb-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="299bb-473">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="299bb-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="299bb-474">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="299bb-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="299bb-475">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="299bb-475">Define the cost allocation</span></span>

<span data-ttu-id="299bb-476">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="299bb-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="299bb-477">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="299bb-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="299bb-478">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="299bb-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-479">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-479">Cost object</span></span></th>
<th><span data-ttu-id="299bb-480">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="299bb-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-481">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-481">CC002</span></span></td>
<td><span data-ttu-id="299bb-482">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-482">Finance</span></span></td>
<td><span data-ttu-id="299bb-483">35</span><span class="sxs-lookup"><span data-stu-id="299bb-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-484">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-484">CC003</span></span></td>
<td><span data-ttu-id="299bb-485">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-485">Assembly</span></span></td>
<td><span data-ttu-id="299bb-486">55</span><span class="sxs-lookup"><span data-stu-id="299bb-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-487">CC004</span><span class="sxs-lookup"><span data-stu-id="299bb-487">CC004</span></span></td>
<td><span data-ttu-id="299bb-488">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="299bb-488">Packaging</span></span></td>
<td><span data-ttu-id="299bb-489">10.</span><span class="sxs-lookup"><span data-stu-id="299bb-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="299bb-490">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="299bb-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="299bb-491">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="299bb-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-492">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-492">Cost object</span></span></th>
<th><span data-ttu-id="299bb-493">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="299bb-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-494">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-494">CC003</span></span></td>
<td><span data-ttu-id="299bb-495">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-495">Assembly</span></span></td>
<td><span data-ttu-id="299bb-496">65</span><span class="sxs-lookup"><span data-stu-id="299bb-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-497">CC004</span><span class="sxs-lookup"><span data-stu-id="299bb-497">CC004</span></span></td>
<td><span data-ttu-id="299bb-498">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="299bb-498">Packaging</span></span></td>
<td><span data-ttu-id="299bb-499">35</span><span class="sxs-lookup"><span data-stu-id="299bb-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="299bb-500">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="299bb-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="299bb-501">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="299bb-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-502">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-502">Cost object</span></span></th>
<th><span data-ttu-id="299bb-503">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="299bb-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="299bb-504">Prod 1</span></span></td>
<td><span data-ttu-id="299bb-505">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-505">Product 1</span></span></td>
<td><span data-ttu-id="299bb-506">60</span><span class="sxs-lookup"><span data-stu-id="299bb-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="299bb-507">Prod 2</span></span></td>
<td><span data-ttu-id="299bb-508">2. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-508">Product 2</span></span></td>
<td><span data-ttu-id="299bb-509">20</span><span class="sxs-lookup"><span data-stu-id="299bb-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="299bb-510">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="299bb-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="299bb-511">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="299bb-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-512">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-512">Cost object</span></span></th>
<th><span data-ttu-id="299bb-513">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="299bb-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="299bb-514">Prod 1</span></span></td>
<td><span data-ttu-id="299bb-515">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-515">Product 1</span></span></td>
<td><span data-ttu-id="299bb-516">80</span><span class="sxs-lookup"><span data-stu-id="299bb-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="299bb-517">Prod 2</span></span></td>
<td><span data-ttu-id="299bb-518">2. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-518">Product 2</span></span></td>
<td><span data-ttu-id="299bb-519">15</span><span class="sxs-lookup"><span data-stu-id="299bb-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="299bb-520">Statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="299bb-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="299bb-521">Sīkāku informāciju skatiet šeit: [Statistikas mēru nodrošinātāja veidne](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="299bb-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="299bb-522">Nākamajā tabulā ir parādīts rezultāts, ja tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījuma pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="299bb-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-523">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-523">Cost object</span></span></th>
<th><span data-ttu-id="299bb-524">Lielums</span><span class="sxs-lookup"><span data-stu-id="299bb-524">Magnitude</span></span></th>
<th><span data-ttu-id="299bb-525">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="299bb-525">Allocation factor</span></span></th>
<th><span data-ttu-id="299bb-526">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-526">Amount</span></span></th>
<th><span data-ttu-id="299bb-527">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="299bb-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-528">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-528">CC002</span></span></td>
<td><span data-ttu-id="299bb-529">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-529">Finance</span></span></td>
<td><span data-ttu-id="299bb-530">35</span><span class="sxs-lookup"><span data-stu-id="299bb-530">35</span></span></td>
<td><span data-ttu-id="299bb-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="299bb-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="299bb-532">175.00</span><span class="sxs-lookup"><span data-stu-id="299bb-532">175.00</span></span></td>
<td><span data-ttu-id="299bb-533">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-534">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-534">CC003</span></span></td>
<td><span data-ttu-id="299bb-535">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-535">Assembly</span></span></td>
<td><span data-ttu-id="299bb-536">55</span><span class="sxs-lookup"><span data-stu-id="299bb-536">55</span></span></td>
<td><span data-ttu-id="299bb-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="299bb-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="299bb-538">275.00</span><span class="sxs-lookup"><span data-stu-id="299bb-538">275.00</span></span></td>
<td><span data-ttu-id="299bb-539">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-540">CC004</span><span class="sxs-lookup"><span data-stu-id="299bb-540">CC004</span></span></td>
<td><span data-ttu-id="299bb-541">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="299bb-541">Packaging</span></span></td>
<td><span data-ttu-id="299bb-542">10.</span><span class="sxs-lookup"><span data-stu-id="299bb-542">10</span></span></td>
<td><span data-ttu-id="299bb-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="299bb-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="299bb-544">50,00</span><span class="sxs-lookup"><span data-stu-id="299bb-544">50.00</span></span></td>
<td><span data-ttu-id="299bb-545">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-546">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-546">CC002</span></span></td>
<td><span data-ttu-id="299bb-547">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-547">Finance</span></span></td>
<td><span data-ttu-id="299bb-548">35</span><span class="sxs-lookup"><span data-stu-id="299bb-548">35</span></span></td>
<td><span data-ttu-id="299bb-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="299bb-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="299bb-550">436.00</span><span class="sxs-lookup"><span data-stu-id="299bb-550">436.00</span></span></td>
<td><span data-ttu-id="299bb-551">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-552">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-552">CC003</span></span></td>
<td><span data-ttu-id="299bb-553">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-553">Assembly</span></span></td>
<td><span data-ttu-id="299bb-554">55</span><span class="sxs-lookup"><span data-stu-id="299bb-554">55</span></span></td>
<td><span data-ttu-id="299bb-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="299bb-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="299bb-556">685.14</span><span class="sxs-lookup"><span data-stu-id="299bb-556">685.14</span></span></td>
<td><span data-ttu-id="299bb-557">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-558">CC004</span><span class="sxs-lookup"><span data-stu-id="299bb-558">CC004</span></span></td>
<td><span data-ttu-id="299bb-559">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="299bb-559">Packaging</span></span></td>
<td><span data-ttu-id="299bb-560">10.</span><span class="sxs-lookup"><span data-stu-id="299bb-560">10</span></span></td>
<td><span data-ttu-id="299bb-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="299bb-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="299bb-562">124.57</span><span class="sxs-lookup"><span data-stu-id="299bb-562">124.57</span></span></td>
<td><span data-ttu-id="299bb-563">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="299bb-564">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="299bb-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-565">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-565">Cost object</span></span></th>
<th><span data-ttu-id="299bb-566">Lielums</span><span class="sxs-lookup"><span data-stu-id="299bb-566">Magnitude</span></span></th>
<th><span data-ttu-id="299bb-567">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="299bb-567">Allocation factor</span></span></th>
<th><span data-ttu-id="299bb-568">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-568">Amount</span></span></th>
<th><span data-ttu-id="299bb-569">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="299bb-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-570">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-570">CC003</span></span></td>
<td><span data-ttu-id="299bb-571">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-571">Assembly</span></span></td>
<td><span data-ttu-id="299bb-572">65</span><span class="sxs-lookup"><span data-stu-id="299bb-572">65</span></span></td>
<td><span data-ttu-id="299bb-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="299bb-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="299bb-574">438.75</span><span class="sxs-lookup"><span data-stu-id="299bb-574">438.75</span></span></td>
<td><span data-ttu-id="299bb-575">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-576">CC004</span><span class="sxs-lookup"><span data-stu-id="299bb-576">CC004</span></span></td>
<td><span data-ttu-id="299bb-577">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="299bb-577">Packaging</span></span></td>
<td><span data-ttu-id="299bb-578">35</span><span class="sxs-lookup"><span data-stu-id="299bb-578">35</span></span></td>
<td><span data-ttu-id="299bb-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="299bb-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="299bb-580">236.25</span><span class="sxs-lookup"><span data-stu-id="299bb-580">236.25</span></span></td>
<td><span data-ttu-id="299bb-581">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-582">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-582">CC003</span></span></td>
<td><span data-ttu-id="299bb-583">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-583">Assembly</span></span></td>
<td><span data-ttu-id="299bb-584">65</span><span class="sxs-lookup"><span data-stu-id="299bb-584">65</span></span></td>
<td><span data-ttu-id="299bb-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="299bb-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="299bb-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="299bb-586">5,297.69</span></span></td>
<td><span data-ttu-id="299bb-587">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-588">CC004</span><span class="sxs-lookup"><span data-stu-id="299bb-588">CC004</span></span></td>
<td><span data-ttu-id="299bb-589">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="299bb-589">Packaging</span></span></td>
<td><span data-ttu-id="299bb-590">35</span><span class="sxs-lookup"><span data-stu-id="299bb-590">35</span></span></td>
<td><span data-ttu-id="299bb-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="299bb-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="299bb-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="299bb-592">2,852.60</span></span></td>
<td><span data-ttu-id="299bb-593">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="299bb-594">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="299bb-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-595">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-595">Cost object</span></span></th>
<th><span data-ttu-id="299bb-596">Lielums</span><span class="sxs-lookup"><span data-stu-id="299bb-596">Magnitude</span></span></th>
<th><span data-ttu-id="299bb-597">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="299bb-597">Allocation factor</span></span></th>
<th><span data-ttu-id="299bb-598">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-598">Amount</span></span></th>
<th><span data-ttu-id="299bb-599">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="299bb-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="299bb-600">Prod 1</span></span></td>
<td><span data-ttu-id="299bb-601">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-601">Product 1</span></span></td>
<td><span data-ttu-id="299bb-602">60</span><span class="sxs-lookup"><span data-stu-id="299bb-602">60</span></span></td>
<td><span data-ttu-id="299bb-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="299bb-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="299bb-604">535.31</span><span class="sxs-lookup"><span data-stu-id="299bb-604">535.31</span></span></td>
<td><span data-ttu-id="299bb-605">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="299bb-606">Prod 2</span></span></td>
<td><span data-ttu-id="299bb-607">2. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-607">Product 2</span></span></td>
<td><span data-ttu-id="299bb-608">20.</span><span class="sxs-lookup"><span data-stu-id="299bb-608">20</span></span></td>
<td><span data-ttu-id="299bb-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="299bb-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="299bb-610">178.44</span><span class="sxs-lookup"><span data-stu-id="299bb-610">178.44</span></span></td>
<td><span data-ttu-id="299bb-611">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="299bb-612">Prod 1</span></span></td>
<td><span data-ttu-id="299bb-613">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-613">Product 1</span></span></td>
<td><span data-ttu-id="299bb-614">60</span><span class="sxs-lookup"><span data-stu-id="299bb-614">60</span></span></td>
<td><span data-ttu-id="299bb-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="299bb-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="299bb-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="299bb-616">4,487.12</span></span></td>
<td><span data-ttu-id="299bb-617">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="299bb-618">Prod 2</span></span></td>
<td><span data-ttu-id="299bb-619">2. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-619">Product 2</span></span></td>
<td><span data-ttu-id="299bb-620">20.</span><span class="sxs-lookup"><span data-stu-id="299bb-620">20</span></span></td>
<td><span data-ttu-id="299bb-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="299bb-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="299bb-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="299bb-622">1,495.71</span></span></td>
<td><span data-ttu-id="299bb-623">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="299bb-624">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="299bb-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-625">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-625">Cost object</span></span></th>
<th><span data-ttu-id="299bb-626">Lielums</span><span class="sxs-lookup"><span data-stu-id="299bb-626">Magnitude</span></span></th>
<th><span data-ttu-id="299bb-627">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="299bb-627">Allocation factor</span></span></th>
<th><span data-ttu-id="299bb-628">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-628">Amount</span></span></th>
<th><span data-ttu-id="299bb-629">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="299bb-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="299bb-630">Prod 1</span></span></td>
<td><span data-ttu-id="299bb-631">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-631">Product 1</span></span></td>
<td><span data-ttu-id="299bb-632">80</span><span class="sxs-lookup"><span data-stu-id="299bb-632">80</span></span></td>
<td><span data-ttu-id="299bb-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="299bb-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="299bb-634">241.05</span><span class="sxs-lookup"><span data-stu-id="299bb-634">241.05</span></span></td>
<td><span data-ttu-id="299bb-635">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="299bb-636">Prod 2</span></span></td>
<td><span data-ttu-id="299bb-637">2. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-637">Product 2</span></span></td>
<td><span data-ttu-id="299bb-638">15</span><span class="sxs-lookup"><span data-stu-id="299bb-638">15</span></span></td>
<td><span data-ttu-id="299bb-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="299bb-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="299bb-640">45.20</span><span class="sxs-lookup"><span data-stu-id="299bb-640">45.20</span></span></td>
<td><span data-ttu-id="299bb-641">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="299bb-642">Prod 1</span></span></td>
<td><span data-ttu-id="299bb-643">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-643">Product 1</span></span></td>
<td><span data-ttu-id="299bb-644">80</span><span class="sxs-lookup"><span data-stu-id="299bb-644">80</span></span></td>
<td><span data-ttu-id="299bb-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="299bb-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="299bb-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="299bb-646">2,507.09</span></span></td>
<td><span data-ttu-id="299bb-647">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="299bb-648">Prod 2</span></span></td>
<td><span data-ttu-id="299bb-649">2. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-649">Product 2</span></span></td>
<td><span data-ttu-id="299bb-650">15</span><span class="sxs-lookup"><span data-stu-id="299bb-650">15</span></span></td>
<td><span data-ttu-id="299bb-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="299bb-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="299bb-652">470.08</span><span class="sxs-lookup"><span data-stu-id="299bb-652">470.08</span></span></td>
<td><span data-ttu-id="299bb-653">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="299bb-654">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="299bb-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="299bb-655">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="299bb-655">Journal</span></span></th>
<th><span data-ttu-id="299bb-656">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="299bb-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="299bb-657">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="299bb-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="299bb-658">Versija</span><span class="sxs-lookup"><span data-stu-id="299bb-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-659">00004</span><span class="sxs-lookup"><span data-stu-id="299bb-659">00004</span></span></td>
<td><span data-ttu-id="299bb-660">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="299bb-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="299bb-661">Finanšu</span><span class="sxs-lookup"><span data-stu-id="299bb-661">Fiscal</span></span></td>
<td><span data-ttu-id="299bb-662">2017</span><span class="sxs-lookup"><span data-stu-id="299bb-662">2017</span></span></td>
<td><span data-ttu-id="299bb-663">Periods 1</span><span class="sxs-lookup"><span data-stu-id="299bb-663">Period 1</span></span></td>
<td><span data-ttu-id="299bb-664">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="299bb-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="299bb-665">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="299bb-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="299bb-666">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="299bb-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="299bb-667">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="299bb-668">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="299bb-668">Cost element</span></span></th>
<th><span data-ttu-id="299bb-669">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="299bb-669">Cost behavior</span></span></th>
<th><span data-ttu-id="299bb-670">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-671">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-672">CC001</span><span class="sxs-lookup"><span data-stu-id="299bb-672">CC001</span></span></td>
<td><span data-ttu-id="299bb-673">HR</span><span class="sxs-lookup"><span data-stu-id="299bb-673">HR</span></span></td>
<td><span data-ttu-id="299bb-674">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-674">10001</span></span></td>
<td><span data-ttu-id="299bb-675">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-675">Electricity</span></span></td>
<td><span data-ttu-id="299bb-676">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-676">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-677">500,00</span><span class="sxs-lookup"><span data-stu-id="299bb-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-678">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-679">CC001</span><span class="sxs-lookup"><span data-stu-id="299bb-679">CC001</span></span></td>
<td><span data-ttu-id="299bb-680">HR</span><span class="sxs-lookup"><span data-stu-id="299bb-680">HR</span></span></td>
<td><span data-ttu-id="299bb-681">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-681">10001</span></span></td>
<td><span data-ttu-id="299bb-682">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-682">Electricity</span></span></td>
<td><span data-ttu-id="299bb-683">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-683">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="299bb-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-685">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-686">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-686">CC002</span></span></td>
<td><span data-ttu-id="299bb-687">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-687">Finance</span></span></td>
<td><span data-ttu-id="299bb-688">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-688">10001</span></span></td>
<td><span data-ttu-id="299bb-689">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-689">Electricity</span></span></td>
<td><span data-ttu-id="299bb-690">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-690">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-691">675.00</span><span class="sxs-lookup"><span data-stu-id="299bb-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-692">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-693">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-693">CC002</span></span></td>
<td><span data-ttu-id="299bb-694">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-694">Finance</span></span></td>
<td><span data-ttu-id="299bb-695">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-695">10001</span></span></td>
<td><span data-ttu-id="299bb-696">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-696">Electricity</span></span></td>
<td><span data-ttu-id="299bb-697">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-697">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="299bb-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-699">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-700">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-700">CC003</span></span></td>
<td><span data-ttu-id="299bb-701">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-701">Assembly</span></span></td>
<td><span data-ttu-id="299bb-702">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-702">10001</span></span></td>
<td><span data-ttu-id="299bb-703">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-703">Electricity</span></span></td>
<td><span data-ttu-id="299bb-704">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-704">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-705">713.75</span><span class="sxs-lookup"><span data-stu-id="299bb-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-706">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-707">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-707">CC003</span></span></td>
<td><span data-ttu-id="299bb-708">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-708">Assembly</span></span></td>
<td><span data-ttu-id="299bb-709">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-709">10001</span></span></td>
<td><span data-ttu-id="299bb-710">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-710">Electricity</span></span></td>
<td><span data-ttu-id="299bb-711">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-711">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="299bb-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-713">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-714">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-714">CC003</span></span></td>
<td><span data-ttu-id="299bb-715">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="299bb-715">Packaging</span></span></td>
<td><span data-ttu-id="299bb-716">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-716">10001</span></span></td>
<td><span data-ttu-id="299bb-717">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-717">Electricity</span></span></td>
<td><span data-ttu-id="299bb-718">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-718">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-719">286.25</span><span class="sxs-lookup"><span data-stu-id="299bb-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-720">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-721">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-721">CC003</span></span></td>
<td><span data-ttu-id="299bb-722">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="299bb-722">Packaging</span></span></td>
<td><span data-ttu-id="299bb-723">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-723">10001</span></span></td>
<td><span data-ttu-id="299bb-724">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-724">Electricity</span></span></td>
<td><span data-ttu-id="299bb-725">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-725">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="299bb-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-727">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="299bb-728">Prod 1</span></span></td>
<td><span data-ttu-id="299bb-729">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-729">Product 1</span></span></td>
<td><span data-ttu-id="299bb-730">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-730">10001</span></span></td>
<td><span data-ttu-id="299bb-731">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-731">Electricity</span></span></td>
<td><span data-ttu-id="299bb-732">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-732">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-733">776.36</span><span class="sxs-lookup"><span data-stu-id="299bb-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-734">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="299bb-735">Prod 1</span></span></td>
<td><span data-ttu-id="299bb-736">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-736">Product 1</span></span></td>
<td><span data-ttu-id="299bb-737">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-737">10001</span></span></td>
<td><span data-ttu-id="299bb-738">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-738">Electricity</span></span></td>
<td><span data-ttu-id="299bb-739">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-739">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="299bb-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-741">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="299bb-742">Prod 2</span></span></td>
<td><span data-ttu-id="299bb-743">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-743">Product 1</span></span></td>
<td><span data-ttu-id="299bb-744">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-744">10001</span></span></td>
<td><span data-ttu-id="299bb-745">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-745">Electricity</span></span></td>
<td><span data-ttu-id="299bb-746">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-746">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-747">223.64</span><span class="sxs-lookup"><span data-stu-id="299bb-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-748">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="299bb-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="299bb-749">Prod 2</span></span></td>
<td><span data-ttu-id="299bb-750">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-750">Product 1</span></span></td>
<td><span data-ttu-id="299bb-751">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-751">10001</span></span></td>
<td><span data-ttu-id="299bb-752">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-752">Electricity</span></span></td>
<td><span data-ttu-id="299bb-753">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-753">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="299bb-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="299bb-755">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="299bb-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="299bb-756">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="299bb-757">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="299bb-757">Cost element</span></span></th>
<th><span data-ttu-id="299bb-758">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="299bb-758">Cost behavior</span></span></th>
<th><span data-ttu-id="299bb-759">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-759">Amount</span></span></th>
<th><span data-ttu-id="299bb-760">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="299bb-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="299bb-761">CC001</span><span class="sxs-lookup"><span data-stu-id="299bb-761">CC001</span></span></td>
<td><span data-ttu-id="299bb-762">HR</span><span class="sxs-lookup"><span data-stu-id="299bb-762">HR</span></span></td>
<td><span data-ttu-id="299bb-763">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-763">10001</span></span></td>
<td><span data-ttu-id="299bb-764">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-764">Electricity</span></span></td>
<td><span data-ttu-id="299bb-765">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-765">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="299bb-766">-500.00</span></span></td>
<td><span data-ttu-id="299bb-767">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-768">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-768">CC002</span></span></td>
<td><span data-ttu-id="299bb-769">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-769">Finance</span></span></td>
<td><span data-ttu-id="299bb-770">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-770">10001</span></span></td>
<td><span data-ttu-id="299bb-771">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-771">Electricity</span></span></td>
<td><span data-ttu-id="299bb-772">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-772">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-773">175.00</span><span class="sxs-lookup"><span data-stu-id="299bb-773">175.00</span></span></td>
<td><span data-ttu-id="299bb-774">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-775">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-775">CC003</span></span></td>
<td><span data-ttu-id="299bb-776">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-776">Assembly</span></span></td>
<td><span data-ttu-id="299bb-777">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-777">10001</span></span></td>
<td><span data-ttu-id="299bb-778">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-778">Electricity</span></span></td>
<td><span data-ttu-id="299bb-779">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-779">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-780">275.00</span><span class="sxs-lookup"><span data-stu-id="299bb-780">275.00</span></span></td>
<td><span data-ttu-id="299bb-781">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-782">CC004</span><span class="sxs-lookup"><span data-stu-id="299bb-782">CC004</span></span></td>
<td><span data-ttu-id="299bb-783">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="299bb-783">Packaging</span></span></td>
<td><span data-ttu-id="299bb-784">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-784">10001</span></span></td>
<td><span data-ttu-id="299bb-785">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-785">Electricity</span></span></td>
<td><span data-ttu-id="299bb-786">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-786">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-787">50,00</span><span class="sxs-lookup"><span data-stu-id="299bb-787">50,00</span></span></td>
<td><span data-ttu-id="299bb-788">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-789">CC001</span><span class="sxs-lookup"><span data-stu-id="299bb-789">CC001</span></span></td>
<td><span data-ttu-id="299bb-790">HR</span><span class="sxs-lookup"><span data-stu-id="299bb-790">HR</span></span></td>
<td><span data-ttu-id="299bb-791">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-791">10001</span></span></td>
<td><span data-ttu-id="299bb-792">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-792">Electricity</span></span></td>
<td><span data-ttu-id="299bb-793">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-793">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="299bb-794">-1,245.71</span></span></td>
<td><span data-ttu-id="299bb-795">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-796">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-796">CC002</span></span></td>
<td><span data-ttu-id="299bb-797">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-797">Finance</span></span></td>
<td><span data-ttu-id="299bb-798">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-798">10001</span></span></td>
<td><span data-ttu-id="299bb-799">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-799">Electricity</span></span></td>
<td><span data-ttu-id="299bb-800">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-800">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-801">436.00</span><span class="sxs-lookup"><span data-stu-id="299bb-801">436.00</span></span></td>
<td><span data-ttu-id="299bb-802">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-803">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-803">CC003</span></span></td>
<td><span data-ttu-id="299bb-804">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-804">Assembly</span></span></td>
<td><span data-ttu-id="299bb-805">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-805">10001</span></span></td>
<td><span data-ttu-id="299bb-806">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-806">Electricity</span></span></td>
<td><span data-ttu-id="299bb-807">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-807">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-808">685.14</span><span class="sxs-lookup"><span data-stu-id="299bb-808">685.14</span></span></td>
<td><span data-ttu-id="299bb-809">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-810">CC004</span><span class="sxs-lookup"><span data-stu-id="299bb-810">CC004</span></span></td>
<td><span data-ttu-id="299bb-811">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="299bb-811">Packaging</span></span></td>
<td><span data-ttu-id="299bb-812">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-812">10001</span></span></td>
<td><span data-ttu-id="299bb-813">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-813">Electricity</span></span></td>
<td><span data-ttu-id="299bb-814">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-814">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-815">124.57</span><span class="sxs-lookup"><span data-stu-id="299bb-815">124.57</span></span></td>
<td><span data-ttu-id="299bb-816">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-817">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-817">CC002</span></span></td>
<td><span data-ttu-id="299bb-818">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-818">Finance</span></span></td>
<td><span data-ttu-id="299bb-819">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-819">10001</span></span></td>
<td><span data-ttu-id="299bb-820">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-820">Electricity</span></span></td>
<td><span data-ttu-id="299bb-821">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-821">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="299bb-822">-675.00</span></span></td>
<td><span data-ttu-id="299bb-823">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-824">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-824">CC003</span></span></td>
<td><span data-ttu-id="299bb-825">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-825">Assembly</span></span></td>
<td><span data-ttu-id="299bb-826">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-826">10001</span></span></td>
<td><span data-ttu-id="299bb-827">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-827">Electricity</span></span></td>
<td><span data-ttu-id="299bb-828">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-828">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-829">438.75</span><span class="sxs-lookup"><span data-stu-id="299bb-829">438.75</span></span></td>
<td><span data-ttu-id="299bb-830">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-831">CC004</span><span class="sxs-lookup"><span data-stu-id="299bb-831">CC004</span></span></td>
<td><span data-ttu-id="299bb-832">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="299bb-832">Packaging</span></span></td>
<td><span data-ttu-id="299bb-833">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-833">10001</span></span></td>
<td><span data-ttu-id="299bb-834">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-834">Electricity</span></span></td>
<td><span data-ttu-id="299bb-835">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-835">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-836">236.25</span><span class="sxs-lookup"><span data-stu-id="299bb-836">236.25</span></span></td>
<td><span data-ttu-id="299bb-837">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-838">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-838">CC002</span></span></td>
<td><span data-ttu-id="299bb-839">Finanses</span><span class="sxs-lookup"><span data-stu-id="299bb-839">Finance</span></span></td>
<td><span data-ttu-id="299bb-840">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-840">10001</span></span></td>
<td><span data-ttu-id="299bb-841">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-841">Electricity</span></span></td>
<td><span data-ttu-id="299bb-842">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-842">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="299bb-843">-8,150.29</span></span></td>
<td><span data-ttu-id="299bb-844">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-845">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-845">CC003</span></span></td>
<td><span data-ttu-id="299bb-846">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-846">Assembly</span></span></td>
<td><span data-ttu-id="299bb-847">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-847">10001</span></span></td>
<td><span data-ttu-id="299bb-848">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-848">Electricity</span></span></td>
<td><span data-ttu-id="299bb-849">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-849">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="299bb-850">5,297.69</span></span></td>
<td><span data-ttu-id="299bb-851">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-852">CC004</span><span class="sxs-lookup"><span data-stu-id="299bb-852">CC004</span></span></td>
<td><span data-ttu-id="299bb-853">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="299bb-853">Packaging</span></span></td>
<td><span data-ttu-id="299bb-854">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-854">10001</span></span></td>
<td><span data-ttu-id="299bb-855">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-855">Electricity</span></span></td>
<td><span data-ttu-id="299bb-856">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-856">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="299bb-857">2,852.60</span></span></td>
<td><span data-ttu-id="299bb-858">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-859">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-859">CC003</span></span></td>
<td><span data-ttu-id="299bb-860">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-860">Assembly</span></span></td>
<td><span data-ttu-id="299bb-861">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-861">10001</span></span></td>
<td><span data-ttu-id="299bb-862">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-862">Electricity</span></span></td>
<td><span data-ttu-id="299bb-863">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-863">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="299bb-864">-713.75</span></span></td>
<td><span data-ttu-id="299bb-865">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="299bb-866">Prod 1</span></span></td>
<td><span data-ttu-id="299bb-867">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-867">Product 1</span></span></td>
<td><span data-ttu-id="299bb-868">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-868">10001</span></span></td>
<td><span data-ttu-id="299bb-869">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-869">Electricity</span></span></td>
<td><span data-ttu-id="299bb-870">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-870">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-871">535.31</span><span class="sxs-lookup"><span data-stu-id="299bb-871">535.31</span></span></td>
<td><span data-ttu-id="299bb-872">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="299bb-873">Prod 2</span></span></td>
<td><span data-ttu-id="299bb-874">2. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-874">Product 2</span></span></td>
<td><span data-ttu-id="299bb-875">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-875">10001</span></span></td>
<td><span data-ttu-id="299bb-876">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-876">Electricity</span></span></td>
<td><span data-ttu-id="299bb-877">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-877">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-878">178.44</span><span class="sxs-lookup"><span data-stu-id="299bb-878">178.44</span></span></td>
<td><span data-ttu-id="299bb-879">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-880">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-880">CC003</span></span></td>
<td><span data-ttu-id="299bb-881">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-881">Assembly</span></span></td>
<td><span data-ttu-id="299bb-882">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-882">10001</span></span></td>
<td><span data-ttu-id="299bb-883">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-883">Electricity</span></span></td>
<td><span data-ttu-id="299bb-884">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-884">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="299bb-885">-5,982.83</span></span></td>
<td><span data-ttu-id="299bb-886">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="299bb-887">Prod 1</span></span></td>
<td><span data-ttu-id="299bb-888">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-888">Product 1</span></span></td>
<td><span data-ttu-id="299bb-889">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-889">10001</span></span></td>
<td><span data-ttu-id="299bb-890">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-890">Electricity</span></span></td>
<td><span data-ttu-id="299bb-891">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-891">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="299bb-892">4,487.12</span></span></td>
<td><span data-ttu-id="299bb-893">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="299bb-894">Prod 2</span></span></td>
<td><span data-ttu-id="299bb-895">2. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-895">Product 2</span></span></td>
<td><span data-ttu-id="299bb-896">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-896">10001</span></span></td>
<td><span data-ttu-id="299bb-897">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-897">Electricity</span></span></td>
<td><span data-ttu-id="299bb-898">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-898">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="299bb-899">1,495.71</span></span></td>
<td><span data-ttu-id="299bb-900">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-901">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-901">CC003</span></span></td>
<td><span data-ttu-id="299bb-902">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-902">Assembly</span></span></td>
<td><span data-ttu-id="299bb-903">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-903">10001</span></span></td>
<td><span data-ttu-id="299bb-904">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-904">Electricity</span></span></td>
<td><span data-ttu-id="299bb-905">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-905">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="299bb-906">-286.25</span></span></td>
<td><span data-ttu-id="299bb-907">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="299bb-908">Prod 1</span></span></td>
<td><span data-ttu-id="299bb-909">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-909">Product 1</span></span></td>
<td><span data-ttu-id="299bb-910">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-910">10001</span></span></td>
<td><span data-ttu-id="299bb-911">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-911">Electricity</span></span></td>
<td><span data-ttu-id="299bb-912">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-912">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-913">241.05</span><span class="sxs-lookup"><span data-stu-id="299bb-913">241.05</span></span></td>
<td><span data-ttu-id="299bb-914">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="299bb-915">Prod 2</span></span></td>
<td><span data-ttu-id="299bb-916">2. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-916">Product 2</span></span></td>
<td><span data-ttu-id="299bb-917">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-917">10001</span></span></td>
<td><span data-ttu-id="299bb-918">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-918">Electricity</span></span></td>
<td><span data-ttu-id="299bb-919">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-919">Fixed cost</span></span></td>
<td><span data-ttu-id="299bb-920">45.20</span><span class="sxs-lookup"><span data-stu-id="299bb-920">45.20</span></span></td>
<td><span data-ttu-id="299bb-921">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-922">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-922">CC003</span></span></td>
<td><span data-ttu-id="299bb-923">Montāža</span><span class="sxs-lookup"><span data-stu-id="299bb-923">Assembly</span></span></td>
<td><span data-ttu-id="299bb-924">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-924">10001</span></span></td>
<td><span data-ttu-id="299bb-925">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-925">Electricity</span></span></td>
<td><span data-ttu-id="299bb-926">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-926">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="299bb-927">-2,977.17</span></span></td>
<td><span data-ttu-id="299bb-928">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="299bb-929">Prod 1</span></span></td>
<td><span data-ttu-id="299bb-930">1. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-930">Product 1</span></span></td>
<td><span data-ttu-id="299bb-931">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-931">10001</span></span></td>
<td><span data-ttu-id="299bb-932">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-932">Electricity</span></span></td>
<td><span data-ttu-id="299bb-933">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-933">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="299bb-934">2,507.09</span></span></td>
<td><span data-ttu-id="299bb-935">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="299bb-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="299bb-936">Prod 2</span></span></td>
<td><span data-ttu-id="299bb-937">2. prece</span><span class="sxs-lookup"><span data-stu-id="299bb-937">Product 2</span></span></td>
<td><span data-ttu-id="299bb-938">10001</span><span class="sxs-lookup"><span data-stu-id="299bb-938">10001</span></span></td>
<td><span data-ttu-id="299bb-939">Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-939">Electricity</span></span></td>
<td><span data-ttu-id="299bb-940">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-940">Variable cost</span></span></td>
<td><span data-ttu-id="299bb-941">470.08</span><span class="sxs-lookup"><span data-stu-id="299bb-941">470.08</span></span></td>
<td><span data-ttu-id="299bb-942">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="299bb-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="299bb-943">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="299bb-943">Conclusion</span></span>
<span data-ttu-id="299bb-944">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="299bb-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="299bb-945">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="299bb-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="299bb-946">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="299bb-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="299bb-947">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="299bb-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="299bb-948">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="299bb-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="299bb-949">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="299bb-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="299bb-950">Summa</span><span class="sxs-lookup"><span data-stu-id="299bb-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="299bb-951">CC099</span><span class="sxs-lookup"><span data-stu-id="299bb-951">CC099</span></span></th>
<th><span data-ttu-id="299bb-952">CC001</span><span class="sxs-lookup"><span data-stu-id="299bb-952">CC001</span></span></th>
<th><span data-ttu-id="299bb-953">CC002</span><span class="sxs-lookup"><span data-stu-id="299bb-953">CC002</span></span></th>
<th><span data-ttu-id="299bb-954">CC003</span><span class="sxs-lookup"><span data-stu-id="299bb-954">CC003</span></span></th>
<th><span data-ttu-id="299bb-955">CC004</span><span class="sxs-lookup"><span data-stu-id="299bb-955">CC004</span></span></th>
<th><span data-ttu-id="299bb-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="299bb-956">Proj 1</span></span></th>
<th><span data-ttu-id="299bb-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="299bb-957">Proj 2</span></span></th>
<th><span data-ttu-id="299bb-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="299bb-958">Prod 1</span></span></th>
<th><span data-ttu-id="299bb-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="299bb-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="299bb-960">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="299bb-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="299bb-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="299bb-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="299bb-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="299bb-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="299bb-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="299bb-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="299bb-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="299bb-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="299bb-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="299bb-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="299bb-970">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="299bb-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-971">0,00</span><span class="sxs-lookup"><span data-stu-id="299bb-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="299bb-972">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-973">0,00</span><span class="sxs-lookup"><span data-stu-id="299bb-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-974">0,00</span><span class="sxs-lookup"><span data-stu-id="299bb-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-975">0,00</span><span class="sxs-lookup"><span data-stu-id="299bb-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-976">0,00</span><span class="sxs-lookup"><span data-stu-id="299bb-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-977">0,00</span><span class="sxs-lookup"><span data-stu-id="299bb-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="299bb-978">776.36</span><span class="sxs-lookup"><span data-stu-id="299bb-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-979">223.64</span><span class="sxs-lookup"><span data-stu-id="299bb-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="299bb-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="299bb-981">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="299bb-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-982">000</span><span class="sxs-lookup"><span data-stu-id="299bb-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-983">0,00</span><span class="sxs-lookup"><span data-stu-id="299bb-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-984">0,00</span><span class="sxs-lookup"><span data-stu-id="299bb-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-985">0,00</span><span class="sxs-lookup"><span data-stu-id="299bb-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-986">0,00</span><span class="sxs-lookup"><span data-stu-id="299bb-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-987">30,00</span><span class="sxs-lookup"><span data-stu-id="299bb-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-988">10,00</span><span class="sxs-lookup"><span data-stu-id="299bb-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="299bb-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="299bb-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="299bb-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="299bb-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="299bb-992">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="299bb-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="299bb-993">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="299bb-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="299bb-994">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="299bb-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="299bb-995">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="299bb-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="299bb-996">Plašāku informāciju skatiet [Izmaksu apkopojuma politika un pieskaitāmo izmaksu aprēķins](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="299bb-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



