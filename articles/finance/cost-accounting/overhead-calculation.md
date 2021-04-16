---
title: Pieskaitāmo izmaksu aprēķins
description: Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2dddc22128621dc148a253cd568430587f294544
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822907"
---
# <a name="overhead-calculation"></a><span data-ttu-id="2d6b4-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="2d6b4-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d6b4-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="2d6b4-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="2d6b4-105">Term definition</span></span>
---------------

<span data-ttu-id="2d6b4-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="2d6b4-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="2d6b4-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="2d6b4-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="2d6b4-109">Īre</span><span class="sxs-lookup"><span data-stu-id="2d6b4-109">Rent</span></span>
-   <span data-ttu-id="2d6b4-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-110">Electricity</span></span>
-   <span data-ttu-id="2d6b4-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="2d6b4-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="2d6b4-112">Overhead calculation overview</span></span>
<span data-ttu-id="2d6b4-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="2d6b4-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="2d6b4-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="2d6b4-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="2d6b4-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="2d6b4-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="2d6b4-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="2d6b4-119">Version type</span></span>
-   <span data-ttu-id="2d6b4-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="2d6b4-120">Date and time</span></span>
-   <span data-ttu-id="2d6b4-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="2d6b4-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="2d6b4-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="2d6b4-122">Fiscal year</span></span>
-   <span data-ttu-id="2d6b4-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="2d6b4-123">Fiscal period</span></span>

<span data-ttu-id="2d6b4-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="2d6b4-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="2d6b4-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="2d6b4-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="2d6b4-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="2d6b4-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="2d6b4-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="2d6b4-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="2d6b4-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="2d6b4-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="2d6b4-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="2d6b4-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="2d6b4-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="2d6b4-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2d6b4-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2d6b4-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="2d6b4-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="2d6b4-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-140">Main account</span></span></th>
<th><span data-ttu-id="2d6b4-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="2d6b4-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-143">CC099</span><span class="sxs-lookup"><span data-stu-id="2d6b4-143">CC099</span></span></td>
<td><span data-ttu-id="2d6b4-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="2d6b4-144">Default cost center</span></span></td>
<td><span data-ttu-id="2d6b4-145">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-145">10001</span></span></td>
<td><span data-ttu-id="2d6b4-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-146">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="2d6b4-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="2d6b4-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="2d6b4-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="2d6b4-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="2d6b4-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="2d6b4-151">Define the cost behavior rule</span></span>

<span data-ttu-id="2d6b4-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="2d6b4-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="2d6b4-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="2d6b4-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="2d6b4-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="2d6b4-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="2d6b4-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="2d6b4-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="2d6b4-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="2d6b4-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2d6b4-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="2d6b4-160">Journal</span></span></th>
<th><span data-ttu-id="2d6b4-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="2d6b4-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="2d6b4-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="2d6b4-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="2d6b4-163">Versija</span><span class="sxs-lookup"><span data-stu-id="2d6b4-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-164">00001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-164">00001</span></span></td>
<td><span data-ttu-id="2d6b4-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="2d6b4-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="2d6b4-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="2d6b4-166">Fiscal</span></span></td>
<td><span data-ttu-id="2d6b4-167">2017</span><span class="sxs-lookup"><span data-stu-id="2d6b4-167">2017</span></span></td>
<td><span data-ttu-id="2d6b4-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-168">Period 1</span></span></td>
<td><span data-ttu-id="2d6b4-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="2d6b4-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="2d6b4-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2d6b4-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2d6b4-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2d6b4-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="2d6b4-173">Cost element</span></span></th>
<th><span data-ttu-id="2d6b4-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="2d6b4-174">Cost behavior</span></span></th>
<th><span data-ttu-id="2d6b4-175">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-177">CC099</span><span class="sxs-lookup"><span data-stu-id="2d6b4-177">CC099</span></span></td>
<td><span data-ttu-id="2d6b4-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="2d6b4-178">Default cost center</span></span></td>
<td><span data-ttu-id="2d6b4-179">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-179">10001</span></span></td>
<td><span data-ttu-id="2d6b4-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-180">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-181">Unclassified</span></span></td>
<td><span data-ttu-id="2d6b4-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="2d6b4-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="2d6b4-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2d6b4-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="2d6b4-185">Cost element</span></span></th>
<th><span data-ttu-id="2d6b4-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="2d6b4-186">Cost behavior</span></span></th>
<th><span data-ttu-id="2d6b4-187">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-187">Amount</span></span></th>
<th><span data-ttu-id="2d6b4-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-189">CC099</span><span class="sxs-lookup"><span data-stu-id="2d6b4-189">CC099</span></span></td>
<td><span data-ttu-id="2d6b4-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="2d6b4-190">Default cost center</span></span></td>
<td><span data-ttu-id="2d6b4-191">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-191">10001</span></span></td>
<td><span data-ttu-id="2d6b4-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-192">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-193">Unclassified</span></span></td>
<td><span data-ttu-id="2d6b4-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-194">10,000.00</span></span></td>
<td><span data-ttu-id="2d6b4-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-196">CC099</span><span class="sxs-lookup"><span data-stu-id="2d6b4-196">CC099</span></span></td>
<td><span data-ttu-id="2d6b4-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="2d6b4-197">Default cost center</span></span></td>
<td><span data-ttu-id="2d6b4-198">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-198">10001</span></span></td>
<td><span data-ttu-id="2d6b4-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-199">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-200">Unclassified</span></span></td>
<td><span data-ttu-id="2d6b4-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-201">-10,000.00</span></span></td>
<td><span data-ttu-id="2d6b4-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-203">CC099</span><span class="sxs-lookup"><span data-stu-id="2d6b4-203">CC099</span></span></td>
<td><span data-ttu-id="2d6b4-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="2d6b4-204">Default cost center</span></span></td>
<td><span data-ttu-id="2d6b4-205">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-205">10001</span></span></td>
<td><span data-ttu-id="2d6b4-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-206">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-207">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-208">1,000.00</span></span></td>
<td><span data-ttu-id="2d6b4-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-210">CC099</span><span class="sxs-lookup"><span data-stu-id="2d6b4-210">CC099</span></span></td>
<td><span data-ttu-id="2d6b4-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="2d6b4-211">Default cost center</span></span></td>
<td><span data-ttu-id="2d6b4-212">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-212">10001</span></span></td>
<td><span data-ttu-id="2d6b4-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-213">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-214">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-215">9,000.00</span></span></td>
<td><span data-ttu-id="2d6b4-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2d6b4-217">Sīkāku informāciju skatiet šeit: [Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="2d6b4-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="2d6b4-218">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="2d6b4-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="2d6b4-219">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="2d6b4-220">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="2d6b4-221">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="2d6b4-221">Define the cost distribution rule</span></span>

<span data-ttu-id="2d6b4-222">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="2d6b4-223">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="2d6b4-224">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="2d6b4-225">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="2d6b4-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="2d6b4-226">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="2d6b4-227">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-228">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-228">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="2d6b4-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-230">CC001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-230">CC001</span></span></td>
<td><span data-ttu-id="2d6b4-231">HR</span><span class="sxs-lookup"><span data-stu-id="2d6b4-231">HR</span></span></td>
<td><span data-ttu-id="2d6b4-232">1000</span><span class="sxs-lookup"><span data-stu-id="2d6b4-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-233">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-233">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-234">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-234">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-235">6,000</span><span class="sxs-lookup"><span data-stu-id="2d6b4-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-236">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-236">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-237">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-237">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-238">0</span><span class="sxs-lookup"><span data-stu-id="2d6b4-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2d6b4-239">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-240">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-240">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-241">Lielums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-241">Magnitude</span></span></th>
<th><span data-ttu-id="2d6b4-242">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="2d6b4-242">Allocation factor</span></span></th>
<th><span data-ttu-id="2d6b4-243">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-244">CC001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-244">CC001</span></span></td>
<td><span data-ttu-id="2d6b4-245">HR</span><span class="sxs-lookup"><span data-stu-id="2d6b4-245">HR</span></span></td>
<td><span data-ttu-id="2d6b4-246">1000</span><span class="sxs-lookup"><span data-stu-id="2d6b4-246">1,000</span></span></td>
<td><span data-ttu-id="2d6b4-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="2d6b4-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="2d6b4-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-249">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-249">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-250">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-250">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-251">6,000</span><span class="sxs-lookup"><span data-stu-id="2d6b4-251">6,000</span></span></td>
<td><span data-ttu-id="2d6b4-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="2d6b4-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="2d6b4-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-254">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-254">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-255">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-255">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-256">0</span><span class="sxs-lookup"><span data-stu-id="2d6b4-256">0</span></span></td>
<td><span data-ttu-id="2d6b4-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="2d6b4-258">0,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2d6b4-259">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="2d6b4-260">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-261">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-261">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-262">Formula</span><span class="sxs-lookup"><span data-stu-id="2d6b4-262">Formula</span></span></th>
<th><span data-ttu-id="2d6b4-263">Lielums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-263">Magnitude</span></span></th>
<th><span data-ttu-id="2d6b4-264">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="2d6b4-264">Allocation factor</span></span></th>
<th><span data-ttu-id="2d6b4-265">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-266">CC001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-266">CC001</span></span></td>
<td><span data-ttu-id="2d6b4-267">HR</span><span class="sxs-lookup"><span data-stu-id="2d6b4-267">HR</span></span></td>
<td><span data-ttu-id="2d6b4-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="2d6b4-269">1.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-269">1</span></span></td>
<td><span data-ttu-id="2d6b4-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="2d6b4-271">500,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-272">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-272">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-273">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-273">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="2d6b4-275">1.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-275">1</span></span></td>
<td><span data-ttu-id="2d6b4-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="2d6b4-277">500,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-278">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-278">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-279">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-279">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="2d6b4-281">0</span><span class="sxs-lookup"><span data-stu-id="2d6b4-281">0</span></span></td>
<td><span data-ttu-id="2d6b4-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="2d6b4-283">0,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="2d6b4-284">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="2d6b4-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2d6b4-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="2d6b4-285">Journal</span></span></th>
<th><span data-ttu-id="2d6b4-286">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="2d6b4-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="2d6b4-287">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="2d6b4-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="2d6b4-288">Versija</span><span class="sxs-lookup"><span data-stu-id="2d6b4-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-289">00002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-289">00002</span></span></td>
<td><span data-ttu-id="2d6b4-290">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="2d6b4-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="2d6b4-291">Finanšu</span><span class="sxs-lookup"><span data-stu-id="2d6b4-291">Fiscal</span></span></td>
<td><span data-ttu-id="2d6b4-292">2017</span><span class="sxs-lookup"><span data-stu-id="2d6b4-292">2017</span></span></td>
<td><span data-ttu-id="2d6b4-293">Periods 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-293">Period 1</span></span></td>
<td><span data-ttu-id="2d6b4-294">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="2d6b4-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="2d6b4-295">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2d6b4-296">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2d6b4-297">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2d6b4-298">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="2d6b4-298">Cost element</span></span></th>
<th><span data-ttu-id="2d6b4-299">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="2d6b4-299">Cost behavior</span></span></th>
<th><span data-ttu-id="2d6b4-300">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-301">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-302">CC099</span><span class="sxs-lookup"><span data-stu-id="2d6b4-302">CC099</span></span></td>
<td><span data-ttu-id="2d6b4-303">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="2d6b4-303">Default cost center</span></span></td>
<td><span data-ttu-id="2d6b4-304">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-304">10001</span></span></td>
<td><span data-ttu-id="2d6b4-305">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-305">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-306">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-306">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-308">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-309">CC099</span><span class="sxs-lookup"><span data-stu-id="2d6b4-309">CC099</span></span></td>
<td><span data-ttu-id="2d6b4-310">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="2d6b4-310">Default cost center</span></span></td>
<td><span data-ttu-id="2d6b4-311">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-311">10001</span></span></td>
<td><span data-ttu-id="2d6b4-312">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-312">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-313">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-313">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="2d6b4-315">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="2d6b4-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-316">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2d6b4-317">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="2d6b4-317">Cost element</span></span></th>
<th><span data-ttu-id="2d6b4-318">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="2d6b4-318">Cost behavior</span></span></th>
<th><span data-ttu-id="2d6b4-319">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-319">Amount</span></span></th>
<th><span data-ttu-id="2d6b4-320">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-321">CC099</span><span class="sxs-lookup"><span data-stu-id="2d6b4-321">CC099</span></span></td>
<td><span data-ttu-id="2d6b4-322">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="2d6b4-322">Default cost center</span></span></td>
<td><span data-ttu-id="2d6b4-323">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-323">10001</span></span></td>
<td><span data-ttu-id="2d6b4-324">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-324">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-325">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-325">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-326">-1000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-326">-1,000.00</span></span></td>
<td><span data-ttu-id="2d6b4-327">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-328">CC001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-328">CC001</span></span></td>
<td><span data-ttu-id="2d6b4-329">HR</span><span class="sxs-lookup"><span data-stu-id="2d6b4-329">HR</span></span></td>
<td><span data-ttu-id="2d6b4-330">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-330">10001</span></span></td>
<td><span data-ttu-id="2d6b4-331">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-331">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-332">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-332">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-333">500,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-333">500.00</span></span></td>
<td><span data-ttu-id="2d6b4-334">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-335">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-335">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-336">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-336">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-337">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-337">10001</span></span></td>
<td><span data-ttu-id="2d6b4-338">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-338">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-339">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-339">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-340">500,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-340">500.00</span></span></td>
<td><span data-ttu-id="2d6b4-341">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-342">CC099</span><span class="sxs-lookup"><span data-stu-id="2d6b4-342">CC099</span></span></td>
<td><span data-ttu-id="2d6b4-343">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="2d6b4-343">Default cost center</span></span></td>
<td><span data-ttu-id="2d6b4-344">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-344">10001</span></span></td>
<td><span data-ttu-id="2d6b4-345">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-345">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-346">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-346">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-347">-9,000.00</span></span></td>
<td><span data-ttu-id="2d6b4-348">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-349">CC001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-349">CC001</span></span></td>
<td><span data-ttu-id="2d6b4-350">HR</span><span class="sxs-lookup"><span data-stu-id="2d6b4-350">HR</span></span></td>
<td><span data-ttu-id="2d6b4-351">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-351">10001</span></span></td>
<td><span data-ttu-id="2d6b4-352">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-352">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-353">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-353">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="2d6b4-354">1,285.71</span></span></td>
<td><span data-ttu-id="2d6b4-355">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-356">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-356">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-357">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-357">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-358">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-358">10001</span></span></td>
<td><span data-ttu-id="2d6b4-359">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-359">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-360">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-360">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="2d6b4-361">7,714.29</span></span></td>
<td><span data-ttu-id="2d6b4-362">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2d6b4-363">Sīkāku informāciju skatiet šeit: [Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="2d6b4-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="2d6b4-364">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="2d6b4-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="2d6b4-365">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="2d6b4-366">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="2d6b4-367">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="2d6b4-367">Define the overhead rate</span></span>

<span data-ttu-id="2d6b4-368">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="2d6b4-369">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-370">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-370">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-371">Stundas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-372">Proj 1</span></span></td>
<td><span data-ttu-id="2d6b4-373">1. projekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-373">Project 1</span></span></td>
<td><span data-ttu-id="2d6b4-374">3.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-375">Proj 2</span></span></td>
<td><span data-ttu-id="2d6b4-376">2. projekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-376">Project 2</span></span></td>
<td><span data-ttu-id="2d6b4-377">1.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2d6b4-378">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-379">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-379">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-380">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="2d6b4-380">Cost element</span></span></th>
<th><span data-ttu-id="2d6b4-381">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="2d6b4-381">Cost behavior</span></span></th>
<th><span data-ttu-id="2d6b4-382">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="2d6b4-382">Units</span></span></th>
<th><span data-ttu-id="2d6b4-383">Likme</span><span class="sxs-lookup"><span data-stu-id="2d6b4-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-384">CC001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-384">CC001</span></span></td>
<td><span data-ttu-id="2d6b4-385">HR</span><span class="sxs-lookup"><span data-stu-id="2d6b4-385">HR</span></span></td>
<td><span data-ttu-id="2d6b4-386">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-386">10001</span></span></td>
<td><span data-ttu-id="2d6b4-387">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-387">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-388">1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-388">1</span></span></td>
<td><span data-ttu-id="2d6b4-389">10</span><span class="sxs-lookup"><span data-stu-id="2d6b4-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2d6b4-390">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-391">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-391">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-392">Lielums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-392">Magnitude</span></span></th>
<th><span data-ttu-id="2d6b4-393">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="2d6b4-393">Cost element</span></span></th>
<th><span data-ttu-id="2d6b4-394">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="2d6b4-394">Allocation factor</span></span></th>
<th><span data-ttu-id="2d6b4-395">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-396">Proj 1</span></span></td>
<td><span data-ttu-id="2d6b4-397">1. projekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-397">Project 1</span></span></td>
<td><span data-ttu-id="2d6b4-398">3.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-398">3</span></span></td>
<td><span data-ttu-id="2d6b4-399">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-399">10001</span></span></td>
<td><span data-ttu-id="2d6b4-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="2d6b4-401">30,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-402">Proj 2</span></span></td>
<td><span data-ttu-id="2d6b4-403">2. projekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-403">Project 2</span></span></td>
<td><span data-ttu-id="2d6b4-404">1.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-404">1</span></span></td>
<td><span data-ttu-id="2d6b4-405">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-405">10001</span></span></td>
<td><span data-ttu-id="2d6b4-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="2d6b4-407">10,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="2d6b4-408">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="2d6b4-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2d6b4-409">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="2d6b4-409">Journal</span></span></th>
<th><span data-ttu-id="2d6b4-410">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="2d6b4-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="2d6b4-411">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="2d6b4-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="2d6b4-412">Versija</span><span class="sxs-lookup"><span data-stu-id="2d6b4-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-413">00003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-413">00003</span></span></td>
<td><span data-ttu-id="2d6b4-414">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="2d6b4-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="2d6b4-415">Finanšu</span><span class="sxs-lookup"><span data-stu-id="2d6b4-415">Fiscal</span></span></td>
<td><span data-ttu-id="2d6b4-416">2017</span><span class="sxs-lookup"><span data-stu-id="2d6b4-416">2017</span></span></td>
<td><span data-ttu-id="2d6b4-417">Periods 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-417">Period 1</span></span></td>
<td><span data-ttu-id="2d6b4-418">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="2d6b4-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="2d6b4-419">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2d6b4-420">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2d6b4-421">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-421">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-422">Lielums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-423">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-424">Proj 1</span></span></td>
<td><span data-ttu-id="2d6b4-425">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="2d6b4-426">3,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-427">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-428">Proj 2</span></span></td>
<td><span data-ttu-id="2d6b4-429">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="2d6b4-430">1,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="2d6b4-431">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="2d6b4-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-432">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2d6b4-433">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="2d6b4-433">Cost element</span></span></th>
<th><span data-ttu-id="2d6b4-434">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="2d6b4-434">Cost behavior</span></span></th>
<th><span data-ttu-id="2d6b4-435">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-435">Amount</span></span></th>
<th><span data-ttu-id="2d6b4-436">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-437">CC0001</span></span></td>
<td><span data-ttu-id="2d6b4-438">HR</span><span class="sxs-lookup"><span data-stu-id="2d6b4-438">HR</span></span></td>
<td><span data-ttu-id="2d6b4-439">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-439">10001</span></span></td>
<td><span data-ttu-id="2d6b4-440">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-440">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-441">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-441">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-442">-30.00</span></span></td>
<td><span data-ttu-id="2d6b4-443">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-444">Proj 1</span></span></td>
<td><span data-ttu-id="2d6b4-445">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="2d6b4-446">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-446">10001</span></span></td>
<td><span data-ttu-id="2d6b4-447">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-447">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-448">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-448">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-449">30,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-449">30.00</span></span></td>
<td><span data-ttu-id="2d6b4-450">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-451">CC001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-451">CC001</span></span></td>
<td><span data-ttu-id="2d6b4-452">HR</span><span class="sxs-lookup"><span data-stu-id="2d6b4-452">HR</span></span></td>
<td><span data-ttu-id="2d6b4-453">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-453">10001</span></span></td>
<td><span data-ttu-id="2d6b4-454">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-454">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-455">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-455">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-456">-10.00</span></span></td>
<td><span data-ttu-id="2d6b4-457">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-458">Proj 2</span></span></td>
<td><span data-ttu-id="2d6b4-459">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="2d6b4-460">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-460">10001</span></span></td>
<td><span data-ttu-id="2d6b4-461">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-461">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-462">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-462">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-463">10,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-463">10.00</span></span></td>
<td><span data-ttu-id="2d6b4-464">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2d6b4-465">Sīkāku informāciju skatiet šeit: [Pieskaitāmo izmaksu aprēķina veikšana](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="2d6b4-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="2d6b4-466">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="2d6b4-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="2d6b4-467">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="2d6b4-468">Finance atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="2d6b4-469">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="2d6b4-470">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="2d6b4-471">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="2d6b4-472">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="2d6b4-473">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="2d6b4-474">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="2d6b4-475">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="2d6b4-475">Define the cost allocation</span></span>

<span data-ttu-id="2d6b4-476">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="2d6b4-477">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="2d6b4-478">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-479">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-479">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-480">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="2d6b4-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-481">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-481">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-482">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-482">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-483">35</span><span class="sxs-lookup"><span data-stu-id="2d6b4-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-484">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-484">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-485">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-485">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-486">55</span><span class="sxs-lookup"><span data-stu-id="2d6b4-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-487">CC004</span><span class="sxs-lookup"><span data-stu-id="2d6b4-487">CC004</span></span></td>
<td><span data-ttu-id="2d6b4-488">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="2d6b4-488">Packaging</span></span></td>
<td><span data-ttu-id="2d6b4-489">10.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2d6b4-490">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="2d6b4-491">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-492">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-492">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-493">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="2d6b4-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-494">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-494">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-495">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-495">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-496">65</span><span class="sxs-lookup"><span data-stu-id="2d6b4-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-497">CC004</span><span class="sxs-lookup"><span data-stu-id="2d6b4-497">CC004</span></span></td>
<td><span data-ttu-id="2d6b4-498">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="2d6b4-498">Packaging</span></span></td>
<td><span data-ttu-id="2d6b4-499">35</span><span class="sxs-lookup"><span data-stu-id="2d6b4-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2d6b4-500">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="2d6b4-501">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-502">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-502">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-503">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-504">Prod 1</span></span></td>
<td><span data-ttu-id="2d6b4-505">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-505">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-506">60</span><span class="sxs-lookup"><span data-stu-id="2d6b4-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-507">Prod 2</span></span></td>
<td><span data-ttu-id="2d6b4-508">2. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-508">Product 2</span></span></td>
<td><span data-ttu-id="2d6b4-509">20</span><span class="sxs-lookup"><span data-stu-id="2d6b4-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2d6b4-510">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="2d6b4-511">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-512">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-512">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-513">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-514">Prod 1</span></span></td>
<td><span data-ttu-id="2d6b4-515">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-515">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-516">80</span><span class="sxs-lookup"><span data-stu-id="2d6b4-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-517">Prod 2</span></span></td>
<td><span data-ttu-id="2d6b4-518">2. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-518">Product 2</span></span></td>
<td><span data-ttu-id="2d6b4-519">15</span><span class="sxs-lookup"><span data-stu-id="2d6b4-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="2d6b4-520">Statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="2d6b4-521">Sīkāku informāciju skatiet šeit: [Statistikas mēru nodrošinātāja veidne](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="2d6b4-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="2d6b4-522">Nākamajā tabulā ir parādīts rezultāts, ja tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījuma pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-523">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-523">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-524">Lielums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-524">Magnitude</span></span></th>
<th><span data-ttu-id="2d6b4-525">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="2d6b4-525">Allocation factor</span></span></th>
<th><span data-ttu-id="2d6b4-526">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-526">Amount</span></span></th>
<th><span data-ttu-id="2d6b4-527">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="2d6b4-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-528">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-528">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-529">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-529">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-530">35</span><span class="sxs-lookup"><span data-stu-id="2d6b4-530">35</span></span></td>
<td><span data-ttu-id="2d6b4-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="2d6b4-532">175.00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-532">175.00</span></span></td>
<td><span data-ttu-id="2d6b4-533">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-534">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-534">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-535">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-535">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-536">55</span><span class="sxs-lookup"><span data-stu-id="2d6b4-536">55</span></span></td>
<td><span data-ttu-id="2d6b4-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="2d6b4-538">275.00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-538">275.00</span></span></td>
<td><span data-ttu-id="2d6b4-539">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-540">CC004</span><span class="sxs-lookup"><span data-stu-id="2d6b4-540">CC004</span></span></td>
<td><span data-ttu-id="2d6b4-541">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="2d6b4-541">Packaging</span></span></td>
<td><span data-ttu-id="2d6b4-542">10.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-542">10</span></span></td>
<td><span data-ttu-id="2d6b4-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="2d6b4-544">50,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-544">50.00</span></span></td>
<td><span data-ttu-id="2d6b4-545">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-546">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-546">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-547">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-547">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-548">35</span><span class="sxs-lookup"><span data-stu-id="2d6b4-548">35</span></span></td>
<td><span data-ttu-id="2d6b4-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="2d6b4-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="2d6b4-550">436.00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-550">436.00</span></span></td>
<td><span data-ttu-id="2d6b4-551">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-552">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-552">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-553">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-553">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-554">55</span><span class="sxs-lookup"><span data-stu-id="2d6b4-554">55</span></span></td>
<td><span data-ttu-id="2d6b4-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="2d6b4-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="2d6b4-556">685.14</span><span class="sxs-lookup"><span data-stu-id="2d6b4-556">685.14</span></span></td>
<td><span data-ttu-id="2d6b4-557">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-558">CC004</span><span class="sxs-lookup"><span data-stu-id="2d6b4-558">CC004</span></span></td>
<td><span data-ttu-id="2d6b4-559">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="2d6b4-559">Packaging</span></span></td>
<td><span data-ttu-id="2d6b4-560">10.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-560">10</span></span></td>
<td><span data-ttu-id="2d6b4-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="2d6b4-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="2d6b4-562">124.57</span><span class="sxs-lookup"><span data-stu-id="2d6b4-562">124.57</span></span></td>
<td><span data-ttu-id="2d6b4-563">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2d6b4-564">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-565">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-565">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-566">Lielums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-566">Magnitude</span></span></th>
<th><span data-ttu-id="2d6b4-567">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="2d6b4-567">Allocation factor</span></span></th>
<th><span data-ttu-id="2d6b4-568">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-568">Amount</span></span></th>
<th><span data-ttu-id="2d6b4-569">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="2d6b4-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-570">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-570">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-571">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-571">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-572">65</span><span class="sxs-lookup"><span data-stu-id="2d6b4-572">65</span></span></td>
<td><span data-ttu-id="2d6b4-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="2d6b4-574">438.75</span><span class="sxs-lookup"><span data-stu-id="2d6b4-574">438.75</span></span></td>
<td><span data-ttu-id="2d6b4-575">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-576">CC004</span><span class="sxs-lookup"><span data-stu-id="2d6b4-576">CC004</span></span></td>
<td><span data-ttu-id="2d6b4-577">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="2d6b4-577">Packaging</span></span></td>
<td><span data-ttu-id="2d6b4-578">35</span><span class="sxs-lookup"><span data-stu-id="2d6b4-578">35</span></span></td>
<td><span data-ttu-id="2d6b4-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="2d6b4-580">236.25</span><span class="sxs-lookup"><span data-stu-id="2d6b4-580">236.25</span></span></td>
<td><span data-ttu-id="2d6b4-581">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-582">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-582">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-583">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-583">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-584">65</span><span class="sxs-lookup"><span data-stu-id="2d6b4-584">65</span></span></td>
<td><span data-ttu-id="2d6b4-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="2d6b4-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="2d6b4-586">5,297.69</span></span></td>
<td><span data-ttu-id="2d6b4-587">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-588">CC004</span><span class="sxs-lookup"><span data-stu-id="2d6b4-588">CC004</span></span></td>
<td><span data-ttu-id="2d6b4-589">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="2d6b4-589">Packaging</span></span></td>
<td><span data-ttu-id="2d6b4-590">35</span><span class="sxs-lookup"><span data-stu-id="2d6b4-590">35</span></span></td>
<td><span data-ttu-id="2d6b4-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="2d6b4-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="2d6b4-592">2,852.60</span></span></td>
<td><span data-ttu-id="2d6b4-593">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2d6b4-594">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-595">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-595">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-596">Lielums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-596">Magnitude</span></span></th>
<th><span data-ttu-id="2d6b4-597">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="2d6b4-597">Allocation factor</span></span></th>
<th><span data-ttu-id="2d6b4-598">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-598">Amount</span></span></th>
<th><span data-ttu-id="2d6b4-599">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="2d6b4-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-600">Prod 1</span></span></td>
<td><span data-ttu-id="2d6b4-601">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-601">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-602">60</span><span class="sxs-lookup"><span data-stu-id="2d6b4-602">60</span></span></td>
<td><span data-ttu-id="2d6b4-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="2d6b4-604">535.31</span><span class="sxs-lookup"><span data-stu-id="2d6b4-604">535.31</span></span></td>
<td><span data-ttu-id="2d6b4-605">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-606">Prod 2</span></span></td>
<td><span data-ttu-id="2d6b4-607">2. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-607">Product 2</span></span></td>
<td><span data-ttu-id="2d6b4-608">20.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-608">20</span></span></td>
<td><span data-ttu-id="2d6b4-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="2d6b4-610">178.44</span><span class="sxs-lookup"><span data-stu-id="2d6b4-610">178.44</span></span></td>
<td><span data-ttu-id="2d6b4-611">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-612">Prod 1</span></span></td>
<td><span data-ttu-id="2d6b4-613">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-613">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-614">60</span><span class="sxs-lookup"><span data-stu-id="2d6b4-614">60</span></span></td>
<td><span data-ttu-id="2d6b4-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="2d6b4-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="2d6b4-616">4,487.12</span></span></td>
<td><span data-ttu-id="2d6b4-617">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-618">Prod 2</span></span></td>
<td><span data-ttu-id="2d6b4-619">2. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-619">Product 2</span></span></td>
<td><span data-ttu-id="2d6b4-620">20.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-620">20</span></span></td>
<td><span data-ttu-id="2d6b4-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="2d6b4-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="2d6b4-622">1,495.71</span></span></td>
<td><span data-ttu-id="2d6b4-623">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2d6b4-624">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-625">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-625">Cost object</span></span></th>
<th><span data-ttu-id="2d6b4-626">Lielums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-626">Magnitude</span></span></th>
<th><span data-ttu-id="2d6b4-627">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="2d6b4-627">Allocation factor</span></span></th>
<th><span data-ttu-id="2d6b4-628">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-628">Amount</span></span></th>
<th><span data-ttu-id="2d6b4-629">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="2d6b4-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-630">Prod 1</span></span></td>
<td><span data-ttu-id="2d6b4-631">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-631">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-632">80</span><span class="sxs-lookup"><span data-stu-id="2d6b4-632">80</span></span></td>
<td><span data-ttu-id="2d6b4-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="2d6b4-634">241.05</span><span class="sxs-lookup"><span data-stu-id="2d6b4-634">241.05</span></span></td>
<td><span data-ttu-id="2d6b4-635">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-636">Prod 2</span></span></td>
<td><span data-ttu-id="2d6b4-637">2. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-637">Product 2</span></span></td>
<td><span data-ttu-id="2d6b4-638">15</span><span class="sxs-lookup"><span data-stu-id="2d6b4-638">15</span></span></td>
<td><span data-ttu-id="2d6b4-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="2d6b4-640">45.20</span><span class="sxs-lookup"><span data-stu-id="2d6b4-640">45.20</span></span></td>
<td><span data-ttu-id="2d6b4-641">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-642">Prod 1</span></span></td>
<td><span data-ttu-id="2d6b4-643">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-643">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-644">80</span><span class="sxs-lookup"><span data-stu-id="2d6b4-644">80</span></span></td>
<td><span data-ttu-id="2d6b4-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="2d6b4-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="2d6b4-646">2,507.09</span></span></td>
<td><span data-ttu-id="2d6b4-647">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-648">Prod 2</span></span></td>
<td><span data-ttu-id="2d6b4-649">2. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-649">Product 2</span></span></td>
<td><span data-ttu-id="2d6b4-650">15</span><span class="sxs-lookup"><span data-stu-id="2d6b4-650">15</span></span></td>
<td><span data-ttu-id="2d6b4-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="2d6b4-652">470.08</span><span class="sxs-lookup"><span data-stu-id="2d6b4-652">470.08</span></span></td>
<td><span data-ttu-id="2d6b4-653">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="2d6b4-654">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="2d6b4-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2d6b4-655">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="2d6b4-655">Journal</span></span></th>
<th><span data-ttu-id="2d6b4-656">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="2d6b4-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="2d6b4-657">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="2d6b4-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="2d6b4-658">Versija</span><span class="sxs-lookup"><span data-stu-id="2d6b4-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-659">00004</span><span class="sxs-lookup"><span data-stu-id="2d6b4-659">00004</span></span></td>
<td><span data-ttu-id="2d6b4-660">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="2d6b4-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="2d6b4-661">Finanšu</span><span class="sxs-lookup"><span data-stu-id="2d6b4-661">Fiscal</span></span></td>
<td><span data-ttu-id="2d6b4-662">2017</span><span class="sxs-lookup"><span data-stu-id="2d6b4-662">2017</span></span></td>
<td><span data-ttu-id="2d6b4-663">Periods 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-663">Period 1</span></span></td>
<td><span data-ttu-id="2d6b4-664">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="2d6b4-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="2d6b4-665">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2d6b4-666">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2d6b4-667">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2d6b4-668">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="2d6b4-668">Cost element</span></span></th>
<th><span data-ttu-id="2d6b4-669">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="2d6b4-669">Cost behavior</span></span></th>
<th><span data-ttu-id="2d6b4-670">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-671">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-672">CC001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-672">CC001</span></span></td>
<td><span data-ttu-id="2d6b4-673">HR</span><span class="sxs-lookup"><span data-stu-id="2d6b4-673">HR</span></span></td>
<td><span data-ttu-id="2d6b4-674">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-674">10001</span></span></td>
<td><span data-ttu-id="2d6b4-675">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-675">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-676">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-676">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-677">500,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-678">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-679">CC001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-679">CC001</span></span></td>
<td><span data-ttu-id="2d6b4-680">HR</span><span class="sxs-lookup"><span data-stu-id="2d6b4-680">HR</span></span></td>
<td><span data-ttu-id="2d6b4-681">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-681">10001</span></span></td>
<td><span data-ttu-id="2d6b4-682">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-682">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-683">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-683">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="2d6b4-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-685">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-686">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-686">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-687">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-687">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-688">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-688">10001</span></span></td>
<td><span data-ttu-id="2d6b4-689">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-689">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-690">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-690">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-691">675.00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-692">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-693">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-693">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-694">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-694">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-695">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-695">10001</span></span></td>
<td><span data-ttu-id="2d6b4-696">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-696">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-697">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-697">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="2d6b4-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-699">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-700">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-700">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-701">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-701">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-702">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-702">10001</span></span></td>
<td><span data-ttu-id="2d6b4-703">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-703">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-704">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-704">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-705">713.75</span><span class="sxs-lookup"><span data-stu-id="2d6b4-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-706">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-707">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-707">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-708">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-708">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-709">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-709">10001</span></span></td>
<td><span data-ttu-id="2d6b4-710">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-710">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-711">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-711">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="2d6b4-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-713">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-714">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-714">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-715">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="2d6b4-715">Packaging</span></span></td>
<td><span data-ttu-id="2d6b4-716">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-716">10001</span></span></td>
<td><span data-ttu-id="2d6b4-717">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-717">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-718">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-718">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-719">286.25</span><span class="sxs-lookup"><span data-stu-id="2d6b4-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-720">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-721">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-721">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-722">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="2d6b4-722">Packaging</span></span></td>
<td><span data-ttu-id="2d6b4-723">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-723">10001</span></span></td>
<td><span data-ttu-id="2d6b4-724">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-724">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-725">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-725">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="2d6b4-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-727">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-728">Prod 1</span></span></td>
<td><span data-ttu-id="2d6b4-729">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-729">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-730">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-730">10001</span></span></td>
<td><span data-ttu-id="2d6b4-731">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-731">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-732">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-732">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-733">776.36</span><span class="sxs-lookup"><span data-stu-id="2d6b4-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-734">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-735">Prod 1</span></span></td>
<td><span data-ttu-id="2d6b4-736">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-736">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-737">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-737">10001</span></span></td>
<td><span data-ttu-id="2d6b4-738">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-738">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-739">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-739">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="2d6b4-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-741">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-742">Prod 2</span></span></td>
<td><span data-ttu-id="2d6b4-743">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-743">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-744">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-744">10001</span></span></td>
<td><span data-ttu-id="2d6b4-745">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-745">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-746">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-746">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-747">223.64</span><span class="sxs-lookup"><span data-stu-id="2d6b4-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-748">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="2d6b4-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-749">Prod 2</span></span></td>
<td><span data-ttu-id="2d6b4-750">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-750">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-751">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-751">10001</span></span></td>
<td><span data-ttu-id="2d6b4-752">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-752">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-753">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-753">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="2d6b4-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="2d6b4-755">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="2d6b4-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2d6b4-756">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2d6b4-757">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="2d6b4-757">Cost element</span></span></th>
<th><span data-ttu-id="2d6b4-758">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="2d6b4-758">Cost behavior</span></span></th>
<th><span data-ttu-id="2d6b4-759">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-759">Amount</span></span></th>
<th><span data-ttu-id="2d6b4-760">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2d6b4-761">CC001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-761">CC001</span></span></td>
<td><span data-ttu-id="2d6b4-762">HR</span><span class="sxs-lookup"><span data-stu-id="2d6b4-762">HR</span></span></td>
<td><span data-ttu-id="2d6b4-763">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-763">10001</span></span></td>
<td><span data-ttu-id="2d6b4-764">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-764">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-765">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-765">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-766">-500.00</span></span></td>
<td><span data-ttu-id="2d6b4-767">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-768">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-768">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-769">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-769">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-770">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-770">10001</span></span></td>
<td><span data-ttu-id="2d6b4-771">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-771">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-772">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-772">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-773">175.00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-773">175.00</span></span></td>
<td><span data-ttu-id="2d6b4-774">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-775">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-775">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-776">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-776">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-777">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-777">10001</span></span></td>
<td><span data-ttu-id="2d6b4-778">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-778">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-779">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-779">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-780">275.00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-780">275.00</span></span></td>
<td><span data-ttu-id="2d6b4-781">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-782">CC004</span><span class="sxs-lookup"><span data-stu-id="2d6b4-782">CC004</span></span></td>
<td><span data-ttu-id="2d6b4-783">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="2d6b4-783">Packaging</span></span></td>
<td><span data-ttu-id="2d6b4-784">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-784">10001</span></span></td>
<td><span data-ttu-id="2d6b4-785">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-785">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-786">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-786">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-787">50,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-787">50,00</span></span></td>
<td><span data-ttu-id="2d6b4-788">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-789">CC001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-789">CC001</span></span></td>
<td><span data-ttu-id="2d6b4-790">HR</span><span class="sxs-lookup"><span data-stu-id="2d6b4-790">HR</span></span></td>
<td><span data-ttu-id="2d6b4-791">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-791">10001</span></span></td>
<td><span data-ttu-id="2d6b4-792">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-792">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-793">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-793">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="2d6b4-794">-1,245.71</span></span></td>
<td><span data-ttu-id="2d6b4-795">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-796">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-796">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-797">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-797">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-798">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-798">10001</span></span></td>
<td><span data-ttu-id="2d6b4-799">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-799">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-800">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-800">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-801">436.00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-801">436.00</span></span></td>
<td><span data-ttu-id="2d6b4-802">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-803">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-803">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-804">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-804">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-805">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-805">10001</span></span></td>
<td><span data-ttu-id="2d6b4-806">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-806">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-807">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-807">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-808">685.14</span><span class="sxs-lookup"><span data-stu-id="2d6b4-808">685.14</span></span></td>
<td><span data-ttu-id="2d6b4-809">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-810">CC004</span><span class="sxs-lookup"><span data-stu-id="2d6b4-810">CC004</span></span></td>
<td><span data-ttu-id="2d6b4-811">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="2d6b4-811">Packaging</span></span></td>
<td><span data-ttu-id="2d6b4-812">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-812">10001</span></span></td>
<td><span data-ttu-id="2d6b4-813">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-813">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-814">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-814">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-815">124.57</span><span class="sxs-lookup"><span data-stu-id="2d6b4-815">124.57</span></span></td>
<td><span data-ttu-id="2d6b4-816">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-817">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-817">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-818">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-818">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-819">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-819">10001</span></span></td>
<td><span data-ttu-id="2d6b4-820">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-820">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-821">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-821">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-822">-675.00</span></span></td>
<td><span data-ttu-id="2d6b4-823">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-824">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-824">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-825">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-825">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-826">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-826">10001</span></span></td>
<td><span data-ttu-id="2d6b4-827">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-827">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-828">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-828">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-829">438.75</span><span class="sxs-lookup"><span data-stu-id="2d6b4-829">438.75</span></span></td>
<td><span data-ttu-id="2d6b4-830">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-831">CC004</span><span class="sxs-lookup"><span data-stu-id="2d6b4-831">CC004</span></span></td>
<td><span data-ttu-id="2d6b4-832">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="2d6b4-832">Packaging</span></span></td>
<td><span data-ttu-id="2d6b4-833">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-833">10001</span></span></td>
<td><span data-ttu-id="2d6b4-834">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-834">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-835">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-835">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-836">236.25</span><span class="sxs-lookup"><span data-stu-id="2d6b4-836">236.25</span></span></td>
<td><span data-ttu-id="2d6b4-837">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-838">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-838">CC002</span></span></td>
<td><span data-ttu-id="2d6b4-839">Finanses</span><span class="sxs-lookup"><span data-stu-id="2d6b4-839">Finance</span></span></td>
<td><span data-ttu-id="2d6b4-840">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-840">10001</span></span></td>
<td><span data-ttu-id="2d6b4-841">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-841">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-842">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-842">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="2d6b4-843">-8,150.29</span></span></td>
<td><span data-ttu-id="2d6b4-844">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-845">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-845">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-846">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-846">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-847">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-847">10001</span></span></td>
<td><span data-ttu-id="2d6b4-848">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-848">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-849">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-849">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="2d6b4-850">5,297.69</span></span></td>
<td><span data-ttu-id="2d6b4-851">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-852">CC004</span><span class="sxs-lookup"><span data-stu-id="2d6b4-852">CC004</span></span></td>
<td><span data-ttu-id="2d6b4-853">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="2d6b4-853">Packaging</span></span></td>
<td><span data-ttu-id="2d6b4-854">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-854">10001</span></span></td>
<td><span data-ttu-id="2d6b4-855">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-855">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-856">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-856">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="2d6b4-857">2,852.60</span></span></td>
<td><span data-ttu-id="2d6b4-858">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-859">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-859">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-860">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-860">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-861">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-861">10001</span></span></td>
<td><span data-ttu-id="2d6b4-862">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-862">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-863">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-863">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="2d6b4-864">-713.75</span></span></td>
<td><span data-ttu-id="2d6b4-865">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-866">Prod 1</span></span></td>
<td><span data-ttu-id="2d6b4-867">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-867">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-868">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-868">10001</span></span></td>
<td><span data-ttu-id="2d6b4-869">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-869">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-870">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-870">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-871">535.31</span><span class="sxs-lookup"><span data-stu-id="2d6b4-871">535.31</span></span></td>
<td><span data-ttu-id="2d6b4-872">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-873">Prod 2</span></span></td>
<td><span data-ttu-id="2d6b4-874">2. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-874">Product 2</span></span></td>
<td><span data-ttu-id="2d6b4-875">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-875">10001</span></span></td>
<td><span data-ttu-id="2d6b4-876">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-876">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-877">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-877">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-878">178.44</span><span class="sxs-lookup"><span data-stu-id="2d6b4-878">178.44</span></span></td>
<td><span data-ttu-id="2d6b4-879">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-880">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-880">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-881">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-881">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-882">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-882">10001</span></span></td>
<td><span data-ttu-id="2d6b4-883">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-883">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-884">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-884">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="2d6b4-885">-5,982.83</span></span></td>
<td><span data-ttu-id="2d6b4-886">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-887">Prod 1</span></span></td>
<td><span data-ttu-id="2d6b4-888">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-888">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-889">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-889">10001</span></span></td>
<td><span data-ttu-id="2d6b4-890">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-890">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-891">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-891">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="2d6b4-892">4,487.12</span></span></td>
<td><span data-ttu-id="2d6b4-893">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-894">Prod 2</span></span></td>
<td><span data-ttu-id="2d6b4-895">2. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-895">Product 2</span></span></td>
<td><span data-ttu-id="2d6b4-896">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-896">10001</span></span></td>
<td><span data-ttu-id="2d6b4-897">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-897">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-898">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-898">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="2d6b4-899">1,495.71</span></span></td>
<td><span data-ttu-id="2d6b4-900">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-901">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-901">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-902">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-902">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-903">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-903">10001</span></span></td>
<td><span data-ttu-id="2d6b4-904">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-904">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-905">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-905">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="2d6b4-906">-286.25</span></span></td>
<td><span data-ttu-id="2d6b4-907">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-908">Prod 1</span></span></td>
<td><span data-ttu-id="2d6b4-909">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-909">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-910">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-910">10001</span></span></td>
<td><span data-ttu-id="2d6b4-911">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-911">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-912">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-912">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-913">241.05</span><span class="sxs-lookup"><span data-stu-id="2d6b4-913">241.05</span></span></td>
<td><span data-ttu-id="2d6b4-914">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-915">Prod 2</span></span></td>
<td><span data-ttu-id="2d6b4-916">2. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-916">Product 2</span></span></td>
<td><span data-ttu-id="2d6b4-917">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-917">10001</span></span></td>
<td><span data-ttu-id="2d6b4-918">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-918">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-919">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-919">Fixed cost</span></span></td>
<td><span data-ttu-id="2d6b4-920">45.20</span><span class="sxs-lookup"><span data-stu-id="2d6b4-920">45.20</span></span></td>
<td><span data-ttu-id="2d6b4-921">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-922">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-922">CC003</span></span></td>
<td><span data-ttu-id="2d6b4-923">Montāža</span><span class="sxs-lookup"><span data-stu-id="2d6b4-923">Assembly</span></span></td>
<td><span data-ttu-id="2d6b4-924">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-924">10001</span></span></td>
<td><span data-ttu-id="2d6b4-925">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-925">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-926">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-926">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="2d6b4-927">-2,977.17</span></span></td>
<td><span data-ttu-id="2d6b4-928">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-929">Prod 1</span></span></td>
<td><span data-ttu-id="2d6b4-930">1. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-930">Product 1</span></span></td>
<td><span data-ttu-id="2d6b4-931">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-931">10001</span></span></td>
<td><span data-ttu-id="2d6b4-932">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-932">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-933">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-933">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="2d6b4-934">2,507.09</span></span></td>
<td><span data-ttu-id="2d6b4-935">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2d6b4-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-936">Prod 2</span></span></td>
<td><span data-ttu-id="2d6b4-937">2. prece</span><span class="sxs-lookup"><span data-stu-id="2d6b4-937">Product 2</span></span></td>
<td><span data-ttu-id="2d6b4-938">10001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-938">10001</span></span></td>
<td><span data-ttu-id="2d6b4-939">Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-939">Electricity</span></span></td>
<td><span data-ttu-id="2d6b4-940">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-940">Variable cost</span></span></td>
<td><span data-ttu-id="2d6b4-941">470.08</span><span class="sxs-lookup"><span data-stu-id="2d6b4-941">470.08</span></span></td>
<td><span data-ttu-id="2d6b4-942">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="2d6b4-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="2d6b4-943">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="2d6b4-943">Conclusion</span></span>
<span data-ttu-id="2d6b4-944">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="2d6b4-945">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="2d6b4-946">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="2d6b4-947">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="2d6b4-948">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="2d6b4-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="2d6b4-949">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="2d6b4-950">Summa</span><span class="sxs-lookup"><span data-stu-id="2d6b4-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="2d6b4-951">CC099</span><span class="sxs-lookup"><span data-stu-id="2d6b4-951">CC099</span></span></th>
<th><span data-ttu-id="2d6b4-952">CC001</span><span class="sxs-lookup"><span data-stu-id="2d6b4-952">CC001</span></span></th>
<th><span data-ttu-id="2d6b4-953">CC002</span><span class="sxs-lookup"><span data-stu-id="2d6b4-953">CC002</span></span></th>
<th><span data-ttu-id="2d6b4-954">CC003</span><span class="sxs-lookup"><span data-stu-id="2d6b4-954">CC003</span></span></th>
<th><span data-ttu-id="2d6b4-955">CC004</span><span class="sxs-lookup"><span data-stu-id="2d6b4-955">CC004</span></span></th>
<th><span data-ttu-id="2d6b4-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-956">Proj 1</span></span></th>
<th><span data-ttu-id="2d6b4-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-957">Proj 2</span></span></th>
<th><span data-ttu-id="2d6b4-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2d6b4-958">Prod 1</span></span></th>
<th><span data-ttu-id="2d6b4-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2d6b4-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="2d6b4-960">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="2d6b4-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="2d6b4-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="2d6b4-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="2d6b4-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="2d6b4-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="2d6b4-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="2d6b4-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="2d6b4-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="2d6b4-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="2d6b4-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="2d6b4-970">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="2d6b4-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-971">0,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="2d6b4-972">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-973">0,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-974">0,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-975">0,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-976">0,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-977">0,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-978">776.36</span><span class="sxs-lookup"><span data-stu-id="2d6b4-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-979">223.64</span><span class="sxs-lookup"><span data-stu-id="2d6b4-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="2d6b4-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="2d6b4-981">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="2d6b4-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-982">000</span><span class="sxs-lookup"><span data-stu-id="2d6b4-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-983">0,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-984">0,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-985">0,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-986">0,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-987">30,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-988">10,00</span><span class="sxs-lookup"><span data-stu-id="2d6b4-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="2d6b4-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="2d6b4-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2d6b4-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="2d6b4-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="2d6b4-992">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="2d6b4-993">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="2d6b4-994">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="2d6b4-995">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="2d6b4-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="2d6b4-996">Plašāku informāciju skatiet [Izmaksu apkopojuma politika un pieskaitāmo izmaksu aprēķins](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="2d6b4-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]