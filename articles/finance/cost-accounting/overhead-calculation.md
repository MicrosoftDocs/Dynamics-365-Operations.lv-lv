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
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976479"
---
# <a name="overhead-calculation"></a><span data-ttu-id="04c44-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="04c44-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04c44-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="04c44-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="04c44-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="04c44-105">Term definition</span></span>
---------------

<span data-ttu-id="04c44-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="04c44-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="04c44-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="04c44-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="04c44-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="04c44-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="04c44-109">Īre</span><span class="sxs-lookup"><span data-stu-id="04c44-109">Rent</span></span>
-   <span data-ttu-id="04c44-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-110">Electricity</span></span>
-   <span data-ttu-id="04c44-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="04c44-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="04c44-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="04c44-112">Overhead calculation overview</span></span>
<span data-ttu-id="04c44-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="04c44-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="04c44-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="04c44-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="04c44-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="04c44-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="04c44-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="04c44-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="04c44-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="04c44-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="04c44-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="04c44-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="04c44-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="04c44-119">Version type</span></span>
-   <span data-ttu-id="04c44-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="04c44-120">Date and time</span></span>
-   <span data-ttu-id="04c44-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="04c44-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="04c44-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="04c44-122">Fiscal year</span></span>
-   <span data-ttu-id="04c44-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="04c44-123">Fiscal period</span></span>

<span data-ttu-id="04c44-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="04c44-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="04c44-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="04c44-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="04c44-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="04c44-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="04c44-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="04c44-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="04c44-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="04c44-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="04c44-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="04c44-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="04c44-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="04c44-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="04c44-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="04c44-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="04c44-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="04c44-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="04c44-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="04c44-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="04c44-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="04c44-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="04c44-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="04c44-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="04c44-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="04c44-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="04c44-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04c44-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="04c44-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="04c44-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="04c44-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="04c44-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="04c44-140">Main account</span></span></th>
<th><span data-ttu-id="04c44-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="04c44-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="04c44-143">CC099</span><span class="sxs-lookup"><span data-stu-id="04c44-143">CC099</span></span></td>
<td><span data-ttu-id="04c44-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="04c44-144">Default cost center</span></span></td>
<td><span data-ttu-id="04c44-145">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-145">10001</span></span></td>
<td><span data-ttu-id="04c44-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-146">Electricity</span></span></td>
<td><span data-ttu-id="04c44-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="04c44-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="04c44-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="04c44-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="04c44-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="04c44-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="04c44-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="04c44-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="04c44-151">Define the cost behavior rule</span></span>

<span data-ttu-id="04c44-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="04c44-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="04c44-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="04c44-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="04c44-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="04c44-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="04c44-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="04c44-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="04c44-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="04c44-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="04c44-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="04c44-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="04c44-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="04c44-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="04c44-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04c44-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="04c44-160">Journal</span></span></th>
<th><span data-ttu-id="04c44-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="04c44-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="04c44-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="04c44-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="04c44-163">Versija</span><span class="sxs-lookup"><span data-stu-id="04c44-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-164">00001</span><span class="sxs-lookup"><span data-stu-id="04c44-164">00001</span></span></td>
<td><span data-ttu-id="04c44-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="04c44-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="04c44-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="04c44-166">Fiscal</span></span></td>
<td><span data-ttu-id="04c44-167">2017</span><span class="sxs-lookup"><span data-stu-id="04c44-167">2017</span></span></td>
<td><span data-ttu-id="04c44-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="04c44-168">Period 1</span></span></td>
<td><span data-ttu-id="04c44-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="04c44-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="04c44-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="04c44-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04c44-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="04c44-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="04c44-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04c44-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="04c44-173">Cost element</span></span></th>
<th><span data-ttu-id="04c44-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="04c44-174">Cost behavior</span></span></th>
<th><span data-ttu-id="04c44-175">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="04c44-177">CC099</span><span class="sxs-lookup"><span data-stu-id="04c44-177">CC099</span></span></td>
<td><span data-ttu-id="04c44-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="04c44-178">Default cost center</span></span></td>
<td><span data-ttu-id="04c44-179">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-179">10001</span></span></td>
<td><span data-ttu-id="04c44-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-180">Electricity</span></span></td>
<td><span data-ttu-id="04c44-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="04c44-181">Unclassified</span></span></td>
<td><span data-ttu-id="04c44-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="04c44-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="04c44-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04c44-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="04c44-185">Cost element</span></span></th>
<th><span data-ttu-id="04c44-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="04c44-186">Cost behavior</span></span></th>
<th><span data-ttu-id="04c44-187">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-187">Amount</span></span></th>
<th><span data-ttu-id="04c44-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="04c44-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-189">CC099</span><span class="sxs-lookup"><span data-stu-id="04c44-189">CC099</span></span></td>
<td><span data-ttu-id="04c44-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="04c44-190">Default cost center</span></span></td>
<td><span data-ttu-id="04c44-191">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-191">10001</span></span></td>
<td><span data-ttu-id="04c44-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-192">Electricity</span></span></td>
<td><span data-ttu-id="04c44-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="04c44-193">Unclassified</span></span></td>
<td><span data-ttu-id="04c44-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-194">10,000.00</span></span></td>
<td><span data-ttu-id="04c44-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-196">CC099</span><span class="sxs-lookup"><span data-stu-id="04c44-196">CC099</span></span></td>
<td><span data-ttu-id="04c44-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="04c44-197">Default cost center</span></span></td>
<td><span data-ttu-id="04c44-198">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-198">10001</span></span></td>
<td><span data-ttu-id="04c44-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-199">Electricity</span></span></td>
<td><span data-ttu-id="04c44-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="04c44-200">Unclassified</span></span></td>
<td><span data-ttu-id="04c44-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-201">-10,000.00</span></span></td>
<td><span data-ttu-id="04c44-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-203">CC099</span><span class="sxs-lookup"><span data-stu-id="04c44-203">CC099</span></span></td>
<td><span data-ttu-id="04c44-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="04c44-204">Default cost center</span></span></td>
<td><span data-ttu-id="04c44-205">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-205">10001</span></span></td>
<td><span data-ttu-id="04c44-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-206">Electricity</span></span></td>
<td><span data-ttu-id="04c44-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-207">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-208">1,000.00</span></span></td>
<td><span data-ttu-id="04c44-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-210">CC099</span><span class="sxs-lookup"><span data-stu-id="04c44-210">CC099</span></span></td>
<td><span data-ttu-id="04c44-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="04c44-211">Default cost center</span></span></td>
<td><span data-ttu-id="04c44-212">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-212">10001</span></span></td>
<td><span data-ttu-id="04c44-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-213">Electricity</span></span></td>
<td><span data-ttu-id="04c44-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-214">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="04c44-215">9,000.00</span></span></td>
<td><span data-ttu-id="04c44-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04c44-217">Sīkāku informāciju skatiet šeit: [Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="04c44-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="04c44-218">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="04c44-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="04c44-219">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="04c44-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="04c44-220">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="04c44-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="04c44-221">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="04c44-221">Define the cost distribution rule</span></span>

<span data-ttu-id="04c44-222">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="04c44-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="04c44-223">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="04c44-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="04c44-224">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="04c44-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="04c44-225">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="04c44-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="04c44-226">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="04c44-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="04c44-227">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="04c44-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-228">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-228">Cost object</span></span></th>
<th><span data-ttu-id="04c44-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="04c44-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-230">CC001</span><span class="sxs-lookup"><span data-stu-id="04c44-230">CC001</span></span></td>
<td><span data-ttu-id="04c44-231">HR</span><span class="sxs-lookup"><span data-stu-id="04c44-231">HR</span></span></td>
<td><span data-ttu-id="04c44-232">1000</span><span class="sxs-lookup"><span data-stu-id="04c44-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-233">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-233">CC002</span></span></td>
<td><span data-ttu-id="04c44-234">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-234">Finance</span></span></td>
<td><span data-ttu-id="04c44-235">6,000</span><span class="sxs-lookup"><span data-stu-id="04c44-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-236">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-236">CC003</span></span></td>
<td><span data-ttu-id="04c44-237">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-237">Assembly</span></span></td>
<td><span data-ttu-id="04c44-238">0</span><span class="sxs-lookup"><span data-stu-id="04c44-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04c44-239">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="04c44-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-240">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-240">Cost object</span></span></th>
<th><span data-ttu-id="04c44-241">Lielums</span><span class="sxs-lookup"><span data-stu-id="04c44-241">Magnitude</span></span></th>
<th><span data-ttu-id="04c44-242">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="04c44-242">Allocation factor</span></span></th>
<th><span data-ttu-id="04c44-243">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-244">CC001</span><span class="sxs-lookup"><span data-stu-id="04c44-244">CC001</span></span></td>
<td><span data-ttu-id="04c44-245">HR</span><span class="sxs-lookup"><span data-stu-id="04c44-245">HR</span></span></td>
<td><span data-ttu-id="04c44-246">1000</span><span class="sxs-lookup"><span data-stu-id="04c44-246">1,000</span></span></td>
<td><span data-ttu-id="04c44-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="04c44-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="04c44-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-249">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-249">CC002</span></span></td>
<td><span data-ttu-id="04c44-250">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-250">Finance</span></span></td>
<td><span data-ttu-id="04c44-251">6,000</span><span class="sxs-lookup"><span data-stu-id="04c44-251">6,000</span></span></td>
<td><span data-ttu-id="04c44-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="04c44-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="04c44-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-254">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-254">CC003</span></span></td>
<td><span data-ttu-id="04c44-255">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-255">Assembly</span></span></td>
<td><span data-ttu-id="04c44-256">0</span><span class="sxs-lookup"><span data-stu-id="04c44-256">0</span></span></td>
<td><span data-ttu-id="04c44-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="04c44-258">0,00</span><span class="sxs-lookup"><span data-stu-id="04c44-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04c44-259">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="04c44-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="04c44-260">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="04c44-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-261">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-261">Cost object</span></span></th>
<th><span data-ttu-id="04c44-262">Formula</span><span class="sxs-lookup"><span data-stu-id="04c44-262">Formula</span></span></th>
<th><span data-ttu-id="04c44-263">Lielums</span><span class="sxs-lookup"><span data-stu-id="04c44-263">Magnitude</span></span></th>
<th><span data-ttu-id="04c44-264">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="04c44-264">Allocation factor</span></span></th>
<th><span data-ttu-id="04c44-265">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-266">CC001</span><span class="sxs-lookup"><span data-stu-id="04c44-266">CC001</span></span></td>
<td><span data-ttu-id="04c44-267">HR</span><span class="sxs-lookup"><span data-stu-id="04c44-267">HR</span></span></td>
<td><span data-ttu-id="04c44-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="04c44-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="04c44-269">1.</span><span class="sxs-lookup"><span data-stu-id="04c44-269">1</span></span></td>
<td><span data-ttu-id="04c44-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="04c44-271">500,00</span><span class="sxs-lookup"><span data-stu-id="04c44-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-272">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-272">CC002</span></span></td>
<td><span data-ttu-id="04c44-273">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-273">Finance</span></span></td>
<td><span data-ttu-id="04c44-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="04c44-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="04c44-275">1.</span><span class="sxs-lookup"><span data-stu-id="04c44-275">1</span></span></td>
<td><span data-ttu-id="04c44-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="04c44-277">500,00</span><span class="sxs-lookup"><span data-stu-id="04c44-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-278">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-278">CC003</span></span></td>
<td><span data-ttu-id="04c44-279">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-279">Assembly</span></span></td>
<td><span data-ttu-id="04c44-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="04c44-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="04c44-281">0</span><span class="sxs-lookup"><span data-stu-id="04c44-281">0</span></span></td>
<td><span data-ttu-id="04c44-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="04c44-283">0,00</span><span class="sxs-lookup"><span data-stu-id="04c44-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="04c44-284">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="04c44-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04c44-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="04c44-285">Journal</span></span></th>
<th><span data-ttu-id="04c44-286">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="04c44-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="04c44-287">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="04c44-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="04c44-288">Versija</span><span class="sxs-lookup"><span data-stu-id="04c44-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-289">00002</span><span class="sxs-lookup"><span data-stu-id="04c44-289">00002</span></span></td>
<td><span data-ttu-id="04c44-290">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="04c44-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="04c44-291">Finanšu</span><span class="sxs-lookup"><span data-stu-id="04c44-291">Fiscal</span></span></td>
<td><span data-ttu-id="04c44-292">2017</span><span class="sxs-lookup"><span data-stu-id="04c44-292">2017</span></span></td>
<td><span data-ttu-id="04c44-293">Periods 1</span><span class="sxs-lookup"><span data-stu-id="04c44-293">Period 1</span></span></td>
<td><span data-ttu-id="04c44-294">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="04c44-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="04c44-295">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="04c44-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04c44-296">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="04c44-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="04c44-297">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04c44-298">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="04c44-298">Cost element</span></span></th>
<th><span data-ttu-id="04c44-299">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="04c44-299">Cost behavior</span></span></th>
<th><span data-ttu-id="04c44-300">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-301">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-302">CC099</span><span class="sxs-lookup"><span data-stu-id="04c44-302">CC099</span></span></td>
<td><span data-ttu-id="04c44-303">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="04c44-303">Default cost center</span></span></td>
<td><span data-ttu-id="04c44-304">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-304">10001</span></span></td>
<td><span data-ttu-id="04c44-305">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-305">Electricity</span></span></td>
<td><span data-ttu-id="04c44-306">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-306">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-308">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-309">CC099</span><span class="sxs-lookup"><span data-stu-id="04c44-309">CC099</span></span></td>
<td><span data-ttu-id="04c44-310">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="04c44-310">Default cost center</span></span></td>
<td><span data-ttu-id="04c44-311">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-311">10001</span></span></td>
<td><span data-ttu-id="04c44-312">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-312">Electricity</span></span></td>
<td><span data-ttu-id="04c44-313">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-313">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="04c44-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="04c44-315">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="04c44-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-316">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04c44-317">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="04c44-317">Cost element</span></span></th>
<th><span data-ttu-id="04c44-318">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="04c44-318">Cost behavior</span></span></th>
<th><span data-ttu-id="04c44-319">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-319">Amount</span></span></th>
<th><span data-ttu-id="04c44-320">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="04c44-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-321">CC099</span><span class="sxs-lookup"><span data-stu-id="04c44-321">CC099</span></span></td>
<td><span data-ttu-id="04c44-322">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="04c44-322">Default cost center</span></span></td>
<td><span data-ttu-id="04c44-323">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-323">10001</span></span></td>
<td><span data-ttu-id="04c44-324">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-324">Electricity</span></span></td>
<td><span data-ttu-id="04c44-325">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-325">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-326">-1000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-326">-1,000.00</span></span></td>
<td><span data-ttu-id="04c44-327">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-328">CC001</span><span class="sxs-lookup"><span data-stu-id="04c44-328">CC001</span></span></td>
<td><span data-ttu-id="04c44-329">HR</span><span class="sxs-lookup"><span data-stu-id="04c44-329">HR</span></span></td>
<td><span data-ttu-id="04c44-330">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-330">10001</span></span></td>
<td><span data-ttu-id="04c44-331">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-331">Electricity</span></span></td>
<td><span data-ttu-id="04c44-332">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-332">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-333">500,00</span><span class="sxs-lookup"><span data-stu-id="04c44-333">500.00</span></span></td>
<td><span data-ttu-id="04c44-334">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-335">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-335">CC002</span></span></td>
<td><span data-ttu-id="04c44-336">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-336">Finance</span></span></td>
<td><span data-ttu-id="04c44-337">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-337">10001</span></span></td>
<td><span data-ttu-id="04c44-338">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-338">Electricity</span></span></td>
<td><span data-ttu-id="04c44-339">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-339">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-340">500,00</span><span class="sxs-lookup"><span data-stu-id="04c44-340">500.00</span></span></td>
<td><span data-ttu-id="04c44-341">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-342">CC099</span><span class="sxs-lookup"><span data-stu-id="04c44-342">CC099</span></span></td>
<td><span data-ttu-id="04c44-343">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="04c44-343">Default cost center</span></span></td>
<td><span data-ttu-id="04c44-344">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-344">10001</span></span></td>
<td><span data-ttu-id="04c44-345">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-345">Electricity</span></span></td>
<td><span data-ttu-id="04c44-346">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-346">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="04c44-347">-9,000.00</span></span></td>
<td><span data-ttu-id="04c44-348">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-349">CC001</span><span class="sxs-lookup"><span data-stu-id="04c44-349">CC001</span></span></td>
<td><span data-ttu-id="04c44-350">HR</span><span class="sxs-lookup"><span data-stu-id="04c44-350">HR</span></span></td>
<td><span data-ttu-id="04c44-351">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-351">10001</span></span></td>
<td><span data-ttu-id="04c44-352">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-352">Electricity</span></span></td>
<td><span data-ttu-id="04c44-353">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-353">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="04c44-354">1,285.71</span></span></td>
<td><span data-ttu-id="04c44-355">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-356">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-356">CC002</span></span></td>
<td><span data-ttu-id="04c44-357">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-357">Finance</span></span></td>
<td><span data-ttu-id="04c44-358">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-358">10001</span></span></td>
<td><span data-ttu-id="04c44-359">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-359">Electricity</span></span></td>
<td><span data-ttu-id="04c44-360">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-360">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="04c44-361">7,714.29</span></span></td>
<td><span data-ttu-id="04c44-362">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04c44-363">Sīkāku informāciju skatiet šeit: [Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="04c44-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="04c44-364">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="04c44-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="04c44-365">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="04c44-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="04c44-366">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="04c44-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="04c44-367">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="04c44-367">Define the overhead rate</span></span>

<span data-ttu-id="04c44-368">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="04c44-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="04c44-369">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="04c44-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-370">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-370">Cost object</span></span></th>
<th><span data-ttu-id="04c44-371">Stundas</span><span class="sxs-lookup"><span data-stu-id="04c44-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="04c44-372">Proj 1</span></span></td>
<td><span data-ttu-id="04c44-373">1. projekts</span><span class="sxs-lookup"><span data-stu-id="04c44-373">Project 1</span></span></td>
<td><span data-ttu-id="04c44-374">3.</span><span class="sxs-lookup"><span data-stu-id="04c44-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="04c44-375">Proj 2</span></span></td>
<td><span data-ttu-id="04c44-376">2. projekts</span><span class="sxs-lookup"><span data-stu-id="04c44-376">Project 2</span></span></td>
<td><span data-ttu-id="04c44-377">1.</span><span class="sxs-lookup"><span data-stu-id="04c44-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04c44-378">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="04c44-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-379">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-379">Cost object</span></span></th>
<th><span data-ttu-id="04c44-380">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="04c44-380">Cost element</span></span></th>
<th><span data-ttu-id="04c44-381">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="04c44-381">Cost behavior</span></span></th>
<th><span data-ttu-id="04c44-382">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="04c44-382">Units</span></span></th>
<th><span data-ttu-id="04c44-383">Likme</span><span class="sxs-lookup"><span data-stu-id="04c44-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-384">CC001</span><span class="sxs-lookup"><span data-stu-id="04c44-384">CC001</span></span></td>
<td><span data-ttu-id="04c44-385">HR</span><span class="sxs-lookup"><span data-stu-id="04c44-385">HR</span></span></td>
<td><span data-ttu-id="04c44-386">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-386">10001</span></span></td>
<td><span data-ttu-id="04c44-387">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-387">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-388">1</span><span class="sxs-lookup"><span data-stu-id="04c44-388">1</span></span></td>
<td><span data-ttu-id="04c44-389">10</span><span class="sxs-lookup"><span data-stu-id="04c44-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04c44-390">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="04c44-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-391">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-391">Cost object</span></span></th>
<th><span data-ttu-id="04c44-392">Lielums</span><span class="sxs-lookup"><span data-stu-id="04c44-392">Magnitude</span></span></th>
<th><span data-ttu-id="04c44-393">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="04c44-393">Cost element</span></span></th>
<th><span data-ttu-id="04c44-394">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="04c44-394">Allocation factor</span></span></th>
<th><span data-ttu-id="04c44-395">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="04c44-396">Proj 1</span></span></td>
<td><span data-ttu-id="04c44-397">1. projekts</span><span class="sxs-lookup"><span data-stu-id="04c44-397">Project 1</span></span></td>
<td><span data-ttu-id="04c44-398">3.</span><span class="sxs-lookup"><span data-stu-id="04c44-398">3</span></span></td>
<td><span data-ttu-id="04c44-399">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-399">10001</span></span></td>
<td><span data-ttu-id="04c44-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="04c44-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="04c44-401">30,00</span><span class="sxs-lookup"><span data-stu-id="04c44-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="04c44-402">Proj 2</span></span></td>
<td><span data-ttu-id="04c44-403">2. projekts</span><span class="sxs-lookup"><span data-stu-id="04c44-403">Project 2</span></span></td>
<td><span data-ttu-id="04c44-404">1.</span><span class="sxs-lookup"><span data-stu-id="04c44-404">1</span></span></td>
<td><span data-ttu-id="04c44-405">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-405">10001</span></span></td>
<td><span data-ttu-id="04c44-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="04c44-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="04c44-407">10,00</span><span class="sxs-lookup"><span data-stu-id="04c44-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="04c44-408">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="04c44-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04c44-409">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="04c44-409">Journal</span></span></th>
<th><span data-ttu-id="04c44-410">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="04c44-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="04c44-411">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="04c44-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="04c44-412">Versija</span><span class="sxs-lookup"><span data-stu-id="04c44-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-413">00003</span><span class="sxs-lookup"><span data-stu-id="04c44-413">00003</span></span></td>
<td><span data-ttu-id="04c44-414">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="04c44-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="04c44-415">Finanšu</span><span class="sxs-lookup"><span data-stu-id="04c44-415">Fiscal</span></span></td>
<td><span data-ttu-id="04c44-416">2017</span><span class="sxs-lookup"><span data-stu-id="04c44-416">2017</span></span></td>
<td><span data-ttu-id="04c44-417">Periods 1</span><span class="sxs-lookup"><span data-stu-id="04c44-417">Period 1</span></span></td>
<td><span data-ttu-id="04c44-418">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="04c44-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="04c44-419">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="04c44-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04c44-420">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="04c44-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="04c44-421">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-421">Cost object</span></span></th>
<th><span data-ttu-id="04c44-422">Lielums</span><span class="sxs-lookup"><span data-stu-id="04c44-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-423">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="04c44-424">Proj 1</span></span></td>
<td><span data-ttu-id="04c44-425">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="04c44-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="04c44-426">3,00</span><span class="sxs-lookup"><span data-stu-id="04c44-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-427">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="04c44-428">Proj 2</span></span></td>
<td><span data-ttu-id="04c44-429">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="04c44-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="04c44-430">1,00</span><span class="sxs-lookup"><span data-stu-id="04c44-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="04c44-431">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="04c44-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-432">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04c44-433">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="04c44-433">Cost element</span></span></th>
<th><span data-ttu-id="04c44-434">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="04c44-434">Cost behavior</span></span></th>
<th><span data-ttu-id="04c44-435">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-435">Amount</span></span></th>
<th><span data-ttu-id="04c44-436">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="04c44-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="04c44-437">CC0001</span></span></td>
<td><span data-ttu-id="04c44-438">HR</span><span class="sxs-lookup"><span data-stu-id="04c44-438">HR</span></span></td>
<td><span data-ttu-id="04c44-439">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-439">10001</span></span></td>
<td><span data-ttu-id="04c44-440">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-440">Electricity</span></span></td>
<td><span data-ttu-id="04c44-441">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-441">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="04c44-442">-30.00</span></span></td>
<td><span data-ttu-id="04c44-443">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="04c44-444">Proj 1</span></span></td>
<td><span data-ttu-id="04c44-445">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="04c44-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="04c44-446">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-446">10001</span></span></td>
<td><span data-ttu-id="04c44-447">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-447">Electricity</span></span></td>
<td><span data-ttu-id="04c44-448">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-448">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-449">30,00</span><span class="sxs-lookup"><span data-stu-id="04c44-449">30.00</span></span></td>
<td><span data-ttu-id="04c44-450">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-451">CC001</span><span class="sxs-lookup"><span data-stu-id="04c44-451">CC001</span></span></td>
<td><span data-ttu-id="04c44-452">HR</span><span class="sxs-lookup"><span data-stu-id="04c44-452">HR</span></span></td>
<td><span data-ttu-id="04c44-453">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-453">10001</span></span></td>
<td><span data-ttu-id="04c44-454">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-454">Electricity</span></span></td>
<td><span data-ttu-id="04c44-455">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-455">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="04c44-456">-10.00</span></span></td>
<td><span data-ttu-id="04c44-457">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="04c44-458">Proj 2</span></span></td>
<td><span data-ttu-id="04c44-459">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="04c44-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="04c44-460">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-460">10001</span></span></td>
<td><span data-ttu-id="04c44-461">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-461">Electricity</span></span></td>
<td><span data-ttu-id="04c44-462">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-462">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-463">10,00</span><span class="sxs-lookup"><span data-stu-id="04c44-463">10.00</span></span></td>
<td><span data-ttu-id="04c44-464">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04c44-465">Sīkāku informāciju skatiet šeit: [Pieskaitāmo izmaksu aprēķina veikšana](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="04c44-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="04c44-466">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="04c44-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="04c44-467">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="04c44-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="04c44-468">Finance atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="04c44-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="04c44-469">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="04c44-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="04c44-470">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="04c44-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="04c44-471">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="04c44-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="04c44-472">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="04c44-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="04c44-473">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="04c44-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="04c44-474">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="04c44-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="04c44-475">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="04c44-475">Define the cost allocation</span></span>

<span data-ttu-id="04c44-476">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="04c44-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="04c44-477">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="04c44-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="04c44-478">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="04c44-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-479">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-479">Cost object</span></span></th>
<th><span data-ttu-id="04c44-480">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="04c44-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-481">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-481">CC002</span></span></td>
<td><span data-ttu-id="04c44-482">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-482">Finance</span></span></td>
<td><span data-ttu-id="04c44-483">35</span><span class="sxs-lookup"><span data-stu-id="04c44-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-484">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-484">CC003</span></span></td>
<td><span data-ttu-id="04c44-485">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-485">Assembly</span></span></td>
<td><span data-ttu-id="04c44-486">55</span><span class="sxs-lookup"><span data-stu-id="04c44-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-487">CC004</span><span class="sxs-lookup"><span data-stu-id="04c44-487">CC004</span></span></td>
<td><span data-ttu-id="04c44-488">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="04c44-488">Packaging</span></span></td>
<td><span data-ttu-id="04c44-489">10.</span><span class="sxs-lookup"><span data-stu-id="04c44-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04c44-490">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="04c44-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="04c44-491">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="04c44-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-492">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-492">Cost object</span></span></th>
<th><span data-ttu-id="04c44-493">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="04c44-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-494">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-494">CC003</span></span></td>
<td><span data-ttu-id="04c44-495">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-495">Assembly</span></span></td>
<td><span data-ttu-id="04c44-496">65</span><span class="sxs-lookup"><span data-stu-id="04c44-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-497">CC004</span><span class="sxs-lookup"><span data-stu-id="04c44-497">CC004</span></span></td>
<td><span data-ttu-id="04c44-498">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="04c44-498">Packaging</span></span></td>
<td><span data-ttu-id="04c44-499">35</span><span class="sxs-lookup"><span data-stu-id="04c44-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04c44-500">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="04c44-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="04c44-501">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="04c44-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-502">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-502">Cost object</span></span></th>
<th><span data-ttu-id="04c44-503">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="04c44-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="04c44-504">Prod 1</span></span></td>
<td><span data-ttu-id="04c44-505">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-505">Product 1</span></span></td>
<td><span data-ttu-id="04c44-506">60</span><span class="sxs-lookup"><span data-stu-id="04c44-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="04c44-507">Prod 2</span></span></td>
<td><span data-ttu-id="04c44-508">2. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-508">Product 2</span></span></td>
<td><span data-ttu-id="04c44-509">20</span><span class="sxs-lookup"><span data-stu-id="04c44-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04c44-510">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="04c44-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="04c44-511">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="04c44-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-512">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-512">Cost object</span></span></th>
<th><span data-ttu-id="04c44-513">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="04c44-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="04c44-514">Prod 1</span></span></td>
<td><span data-ttu-id="04c44-515">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-515">Product 1</span></span></td>
<td><span data-ttu-id="04c44-516">80</span><span class="sxs-lookup"><span data-stu-id="04c44-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="04c44-517">Prod 2</span></span></td>
<td><span data-ttu-id="04c44-518">2. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-518">Product 2</span></span></td>
<td><span data-ttu-id="04c44-519">15</span><span class="sxs-lookup"><span data-stu-id="04c44-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="04c44-520">Statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="04c44-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="04c44-521">Sīkāku informāciju skatiet šeit: [Statistikas mēru nodrošinātāja veidne](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="04c44-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="04c44-522">Nākamajā tabulā ir parādīts rezultāts, ja tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījuma pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="04c44-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-523">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-523">Cost object</span></span></th>
<th><span data-ttu-id="04c44-524">Lielums</span><span class="sxs-lookup"><span data-stu-id="04c44-524">Magnitude</span></span></th>
<th><span data-ttu-id="04c44-525">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="04c44-525">Allocation factor</span></span></th>
<th><span data-ttu-id="04c44-526">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-526">Amount</span></span></th>
<th><span data-ttu-id="04c44-527">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="04c44-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-528">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-528">CC002</span></span></td>
<td><span data-ttu-id="04c44-529">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-529">Finance</span></span></td>
<td><span data-ttu-id="04c44-530">35</span><span class="sxs-lookup"><span data-stu-id="04c44-530">35</span></span></td>
<td><span data-ttu-id="04c44-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="04c44-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="04c44-532">175.00</span><span class="sxs-lookup"><span data-stu-id="04c44-532">175.00</span></span></td>
<td><span data-ttu-id="04c44-533">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-534">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-534">CC003</span></span></td>
<td><span data-ttu-id="04c44-535">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-535">Assembly</span></span></td>
<td><span data-ttu-id="04c44-536">55</span><span class="sxs-lookup"><span data-stu-id="04c44-536">55</span></span></td>
<td><span data-ttu-id="04c44-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="04c44-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="04c44-538">275.00</span><span class="sxs-lookup"><span data-stu-id="04c44-538">275.00</span></span></td>
<td><span data-ttu-id="04c44-539">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-540">CC004</span><span class="sxs-lookup"><span data-stu-id="04c44-540">CC004</span></span></td>
<td><span data-ttu-id="04c44-541">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="04c44-541">Packaging</span></span></td>
<td><span data-ttu-id="04c44-542">10.</span><span class="sxs-lookup"><span data-stu-id="04c44-542">10</span></span></td>
<td><span data-ttu-id="04c44-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="04c44-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="04c44-544">50,00</span><span class="sxs-lookup"><span data-stu-id="04c44-544">50.00</span></span></td>
<td><span data-ttu-id="04c44-545">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-546">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-546">CC002</span></span></td>
<td><span data-ttu-id="04c44-547">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-547">Finance</span></span></td>
<td><span data-ttu-id="04c44-548">35</span><span class="sxs-lookup"><span data-stu-id="04c44-548">35</span></span></td>
<td><span data-ttu-id="04c44-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="04c44-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="04c44-550">436.00</span><span class="sxs-lookup"><span data-stu-id="04c44-550">436.00</span></span></td>
<td><span data-ttu-id="04c44-551">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-552">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-552">CC003</span></span></td>
<td><span data-ttu-id="04c44-553">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-553">Assembly</span></span></td>
<td><span data-ttu-id="04c44-554">55</span><span class="sxs-lookup"><span data-stu-id="04c44-554">55</span></span></td>
<td><span data-ttu-id="04c44-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="04c44-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="04c44-556">685.14</span><span class="sxs-lookup"><span data-stu-id="04c44-556">685.14</span></span></td>
<td><span data-ttu-id="04c44-557">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-558">CC004</span><span class="sxs-lookup"><span data-stu-id="04c44-558">CC004</span></span></td>
<td><span data-ttu-id="04c44-559">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="04c44-559">Packaging</span></span></td>
<td><span data-ttu-id="04c44-560">10.</span><span class="sxs-lookup"><span data-stu-id="04c44-560">10</span></span></td>
<td><span data-ttu-id="04c44-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="04c44-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="04c44-562">124.57</span><span class="sxs-lookup"><span data-stu-id="04c44-562">124.57</span></span></td>
<td><span data-ttu-id="04c44-563">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04c44-564">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="04c44-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-565">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-565">Cost object</span></span></th>
<th><span data-ttu-id="04c44-566">Lielums</span><span class="sxs-lookup"><span data-stu-id="04c44-566">Magnitude</span></span></th>
<th><span data-ttu-id="04c44-567">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="04c44-567">Allocation factor</span></span></th>
<th><span data-ttu-id="04c44-568">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-568">Amount</span></span></th>
<th><span data-ttu-id="04c44-569">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="04c44-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-570">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-570">CC003</span></span></td>
<td><span data-ttu-id="04c44-571">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-571">Assembly</span></span></td>
<td><span data-ttu-id="04c44-572">65</span><span class="sxs-lookup"><span data-stu-id="04c44-572">65</span></span></td>
<td><span data-ttu-id="04c44-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="04c44-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="04c44-574">438.75</span><span class="sxs-lookup"><span data-stu-id="04c44-574">438.75</span></span></td>
<td><span data-ttu-id="04c44-575">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-576">CC004</span><span class="sxs-lookup"><span data-stu-id="04c44-576">CC004</span></span></td>
<td><span data-ttu-id="04c44-577">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="04c44-577">Packaging</span></span></td>
<td><span data-ttu-id="04c44-578">35</span><span class="sxs-lookup"><span data-stu-id="04c44-578">35</span></span></td>
<td><span data-ttu-id="04c44-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="04c44-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="04c44-580">236.25</span><span class="sxs-lookup"><span data-stu-id="04c44-580">236.25</span></span></td>
<td><span data-ttu-id="04c44-581">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-582">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-582">CC003</span></span></td>
<td><span data-ttu-id="04c44-583">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-583">Assembly</span></span></td>
<td><span data-ttu-id="04c44-584">65</span><span class="sxs-lookup"><span data-stu-id="04c44-584">65</span></span></td>
<td><span data-ttu-id="04c44-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="04c44-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="04c44-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="04c44-586">5,297.69</span></span></td>
<td><span data-ttu-id="04c44-587">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-588">CC004</span><span class="sxs-lookup"><span data-stu-id="04c44-588">CC004</span></span></td>
<td><span data-ttu-id="04c44-589">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="04c44-589">Packaging</span></span></td>
<td><span data-ttu-id="04c44-590">35</span><span class="sxs-lookup"><span data-stu-id="04c44-590">35</span></span></td>
<td><span data-ttu-id="04c44-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="04c44-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="04c44-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="04c44-592">2,852.60</span></span></td>
<td><span data-ttu-id="04c44-593">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04c44-594">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="04c44-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-595">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-595">Cost object</span></span></th>
<th><span data-ttu-id="04c44-596">Lielums</span><span class="sxs-lookup"><span data-stu-id="04c44-596">Magnitude</span></span></th>
<th><span data-ttu-id="04c44-597">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="04c44-597">Allocation factor</span></span></th>
<th><span data-ttu-id="04c44-598">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-598">Amount</span></span></th>
<th><span data-ttu-id="04c44-599">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="04c44-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="04c44-600">Prod 1</span></span></td>
<td><span data-ttu-id="04c44-601">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-601">Product 1</span></span></td>
<td><span data-ttu-id="04c44-602">60</span><span class="sxs-lookup"><span data-stu-id="04c44-602">60</span></span></td>
<td><span data-ttu-id="04c44-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="04c44-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="04c44-604">535.31</span><span class="sxs-lookup"><span data-stu-id="04c44-604">535.31</span></span></td>
<td><span data-ttu-id="04c44-605">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="04c44-606">Prod 2</span></span></td>
<td><span data-ttu-id="04c44-607">2. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-607">Product 2</span></span></td>
<td><span data-ttu-id="04c44-608">20.</span><span class="sxs-lookup"><span data-stu-id="04c44-608">20</span></span></td>
<td><span data-ttu-id="04c44-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="04c44-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="04c44-610">178.44</span><span class="sxs-lookup"><span data-stu-id="04c44-610">178.44</span></span></td>
<td><span data-ttu-id="04c44-611">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="04c44-612">Prod 1</span></span></td>
<td><span data-ttu-id="04c44-613">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-613">Product 1</span></span></td>
<td><span data-ttu-id="04c44-614">60</span><span class="sxs-lookup"><span data-stu-id="04c44-614">60</span></span></td>
<td><span data-ttu-id="04c44-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="04c44-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="04c44-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="04c44-616">4,487.12</span></span></td>
<td><span data-ttu-id="04c44-617">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="04c44-618">Prod 2</span></span></td>
<td><span data-ttu-id="04c44-619">2. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-619">Product 2</span></span></td>
<td><span data-ttu-id="04c44-620">20.</span><span class="sxs-lookup"><span data-stu-id="04c44-620">20</span></span></td>
<td><span data-ttu-id="04c44-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="04c44-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="04c44-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="04c44-622">1,495.71</span></span></td>
<td><span data-ttu-id="04c44-623">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04c44-624">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="04c44-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-625">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-625">Cost object</span></span></th>
<th><span data-ttu-id="04c44-626">Lielums</span><span class="sxs-lookup"><span data-stu-id="04c44-626">Magnitude</span></span></th>
<th><span data-ttu-id="04c44-627">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="04c44-627">Allocation factor</span></span></th>
<th><span data-ttu-id="04c44-628">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-628">Amount</span></span></th>
<th><span data-ttu-id="04c44-629">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="04c44-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="04c44-630">Prod 1</span></span></td>
<td><span data-ttu-id="04c44-631">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-631">Product 1</span></span></td>
<td><span data-ttu-id="04c44-632">80</span><span class="sxs-lookup"><span data-stu-id="04c44-632">80</span></span></td>
<td><span data-ttu-id="04c44-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="04c44-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="04c44-634">241.05</span><span class="sxs-lookup"><span data-stu-id="04c44-634">241.05</span></span></td>
<td><span data-ttu-id="04c44-635">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="04c44-636">Prod 2</span></span></td>
<td><span data-ttu-id="04c44-637">2. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-637">Product 2</span></span></td>
<td><span data-ttu-id="04c44-638">15</span><span class="sxs-lookup"><span data-stu-id="04c44-638">15</span></span></td>
<td><span data-ttu-id="04c44-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="04c44-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="04c44-640">45.20</span><span class="sxs-lookup"><span data-stu-id="04c44-640">45.20</span></span></td>
<td><span data-ttu-id="04c44-641">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="04c44-642">Prod 1</span></span></td>
<td><span data-ttu-id="04c44-643">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-643">Product 1</span></span></td>
<td><span data-ttu-id="04c44-644">80</span><span class="sxs-lookup"><span data-stu-id="04c44-644">80</span></span></td>
<td><span data-ttu-id="04c44-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="04c44-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="04c44-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="04c44-646">2,507.09</span></span></td>
<td><span data-ttu-id="04c44-647">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="04c44-648">Prod 2</span></span></td>
<td><span data-ttu-id="04c44-649">2. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-649">Product 2</span></span></td>
<td><span data-ttu-id="04c44-650">15</span><span class="sxs-lookup"><span data-stu-id="04c44-650">15</span></span></td>
<td><span data-ttu-id="04c44-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="04c44-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="04c44-652">470.08</span><span class="sxs-lookup"><span data-stu-id="04c44-652">470.08</span></span></td>
<td><span data-ttu-id="04c44-653">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="04c44-654">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="04c44-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04c44-655">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="04c44-655">Journal</span></span></th>
<th><span data-ttu-id="04c44-656">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="04c44-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="04c44-657">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="04c44-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="04c44-658">Versija</span><span class="sxs-lookup"><span data-stu-id="04c44-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-659">00004</span><span class="sxs-lookup"><span data-stu-id="04c44-659">00004</span></span></td>
<td><span data-ttu-id="04c44-660">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="04c44-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="04c44-661">Finanšu</span><span class="sxs-lookup"><span data-stu-id="04c44-661">Fiscal</span></span></td>
<td><span data-ttu-id="04c44-662">2017</span><span class="sxs-lookup"><span data-stu-id="04c44-662">2017</span></span></td>
<td><span data-ttu-id="04c44-663">Periods 1</span><span class="sxs-lookup"><span data-stu-id="04c44-663">Period 1</span></span></td>
<td><span data-ttu-id="04c44-664">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="04c44-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="04c44-665">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="04c44-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04c44-666">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="04c44-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="04c44-667">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04c44-668">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="04c44-668">Cost element</span></span></th>
<th><span data-ttu-id="04c44-669">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="04c44-669">Cost behavior</span></span></th>
<th><span data-ttu-id="04c44-670">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-671">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-672">CC001</span><span class="sxs-lookup"><span data-stu-id="04c44-672">CC001</span></span></td>
<td><span data-ttu-id="04c44-673">HR</span><span class="sxs-lookup"><span data-stu-id="04c44-673">HR</span></span></td>
<td><span data-ttu-id="04c44-674">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-674">10001</span></span></td>
<td><span data-ttu-id="04c44-675">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-675">Electricity</span></span></td>
<td><span data-ttu-id="04c44-676">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-676">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-677">500,00</span><span class="sxs-lookup"><span data-stu-id="04c44-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-678">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-679">CC001</span><span class="sxs-lookup"><span data-stu-id="04c44-679">CC001</span></span></td>
<td><span data-ttu-id="04c44-680">HR</span><span class="sxs-lookup"><span data-stu-id="04c44-680">HR</span></span></td>
<td><span data-ttu-id="04c44-681">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-681">10001</span></span></td>
<td><span data-ttu-id="04c44-682">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-682">Electricity</span></span></td>
<td><span data-ttu-id="04c44-683">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-683">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="04c44-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-685">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-686">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-686">CC002</span></span></td>
<td><span data-ttu-id="04c44-687">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-687">Finance</span></span></td>
<td><span data-ttu-id="04c44-688">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-688">10001</span></span></td>
<td><span data-ttu-id="04c44-689">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-689">Electricity</span></span></td>
<td><span data-ttu-id="04c44-690">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-690">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-691">675.00</span><span class="sxs-lookup"><span data-stu-id="04c44-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-692">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-693">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-693">CC002</span></span></td>
<td><span data-ttu-id="04c44-694">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-694">Finance</span></span></td>
<td><span data-ttu-id="04c44-695">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-695">10001</span></span></td>
<td><span data-ttu-id="04c44-696">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-696">Electricity</span></span></td>
<td><span data-ttu-id="04c44-697">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-697">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="04c44-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-699">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-700">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-700">CC003</span></span></td>
<td><span data-ttu-id="04c44-701">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-701">Assembly</span></span></td>
<td><span data-ttu-id="04c44-702">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-702">10001</span></span></td>
<td><span data-ttu-id="04c44-703">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-703">Electricity</span></span></td>
<td><span data-ttu-id="04c44-704">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-704">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-705">713.75</span><span class="sxs-lookup"><span data-stu-id="04c44-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-706">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-707">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-707">CC003</span></span></td>
<td><span data-ttu-id="04c44-708">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-708">Assembly</span></span></td>
<td><span data-ttu-id="04c44-709">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-709">10001</span></span></td>
<td><span data-ttu-id="04c44-710">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-710">Electricity</span></span></td>
<td><span data-ttu-id="04c44-711">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-711">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="04c44-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-713">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-714">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-714">CC003</span></span></td>
<td><span data-ttu-id="04c44-715">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="04c44-715">Packaging</span></span></td>
<td><span data-ttu-id="04c44-716">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-716">10001</span></span></td>
<td><span data-ttu-id="04c44-717">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-717">Electricity</span></span></td>
<td><span data-ttu-id="04c44-718">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-718">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-719">286.25</span><span class="sxs-lookup"><span data-stu-id="04c44-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-720">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-721">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-721">CC003</span></span></td>
<td><span data-ttu-id="04c44-722">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="04c44-722">Packaging</span></span></td>
<td><span data-ttu-id="04c44-723">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-723">10001</span></span></td>
<td><span data-ttu-id="04c44-724">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-724">Electricity</span></span></td>
<td><span data-ttu-id="04c44-725">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-725">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="04c44-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-727">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="04c44-728">Prod 1</span></span></td>
<td><span data-ttu-id="04c44-729">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-729">Product 1</span></span></td>
<td><span data-ttu-id="04c44-730">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-730">10001</span></span></td>
<td><span data-ttu-id="04c44-731">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-731">Electricity</span></span></td>
<td><span data-ttu-id="04c44-732">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-732">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-733">776.36</span><span class="sxs-lookup"><span data-stu-id="04c44-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-734">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="04c44-735">Prod 1</span></span></td>
<td><span data-ttu-id="04c44-736">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-736">Product 1</span></span></td>
<td><span data-ttu-id="04c44-737">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-737">10001</span></span></td>
<td><span data-ttu-id="04c44-738">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-738">Electricity</span></span></td>
<td><span data-ttu-id="04c44-739">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-739">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="04c44-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-741">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="04c44-742">Prod 2</span></span></td>
<td><span data-ttu-id="04c44-743">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-743">Product 1</span></span></td>
<td><span data-ttu-id="04c44-744">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-744">10001</span></span></td>
<td><span data-ttu-id="04c44-745">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-745">Electricity</span></span></td>
<td><span data-ttu-id="04c44-746">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-746">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-747">223.64</span><span class="sxs-lookup"><span data-stu-id="04c44-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-748">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="04c44-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="04c44-749">Prod 2</span></span></td>
<td><span data-ttu-id="04c44-750">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-750">Product 1</span></span></td>
<td><span data-ttu-id="04c44-751">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-751">10001</span></span></td>
<td><span data-ttu-id="04c44-752">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-752">Electricity</span></span></td>
<td><span data-ttu-id="04c44-753">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-753">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="04c44-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="04c44-755">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="04c44-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04c44-756">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04c44-757">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="04c44-757">Cost element</span></span></th>
<th><span data-ttu-id="04c44-758">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="04c44-758">Cost behavior</span></span></th>
<th><span data-ttu-id="04c44-759">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-759">Amount</span></span></th>
<th><span data-ttu-id="04c44-760">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="04c44-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04c44-761">CC001</span><span class="sxs-lookup"><span data-stu-id="04c44-761">CC001</span></span></td>
<td><span data-ttu-id="04c44-762">HR</span><span class="sxs-lookup"><span data-stu-id="04c44-762">HR</span></span></td>
<td><span data-ttu-id="04c44-763">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-763">10001</span></span></td>
<td><span data-ttu-id="04c44-764">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-764">Electricity</span></span></td>
<td><span data-ttu-id="04c44-765">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-765">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="04c44-766">-500.00</span></span></td>
<td><span data-ttu-id="04c44-767">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-768">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-768">CC002</span></span></td>
<td><span data-ttu-id="04c44-769">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-769">Finance</span></span></td>
<td><span data-ttu-id="04c44-770">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-770">10001</span></span></td>
<td><span data-ttu-id="04c44-771">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-771">Electricity</span></span></td>
<td><span data-ttu-id="04c44-772">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-772">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-773">175.00</span><span class="sxs-lookup"><span data-stu-id="04c44-773">175.00</span></span></td>
<td><span data-ttu-id="04c44-774">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-775">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-775">CC003</span></span></td>
<td><span data-ttu-id="04c44-776">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-776">Assembly</span></span></td>
<td><span data-ttu-id="04c44-777">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-777">10001</span></span></td>
<td><span data-ttu-id="04c44-778">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-778">Electricity</span></span></td>
<td><span data-ttu-id="04c44-779">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-779">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-780">275.00</span><span class="sxs-lookup"><span data-stu-id="04c44-780">275.00</span></span></td>
<td><span data-ttu-id="04c44-781">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-782">CC004</span><span class="sxs-lookup"><span data-stu-id="04c44-782">CC004</span></span></td>
<td><span data-ttu-id="04c44-783">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="04c44-783">Packaging</span></span></td>
<td><span data-ttu-id="04c44-784">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-784">10001</span></span></td>
<td><span data-ttu-id="04c44-785">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-785">Electricity</span></span></td>
<td><span data-ttu-id="04c44-786">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-786">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-787">50,00</span><span class="sxs-lookup"><span data-stu-id="04c44-787">50,00</span></span></td>
<td><span data-ttu-id="04c44-788">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-789">CC001</span><span class="sxs-lookup"><span data-stu-id="04c44-789">CC001</span></span></td>
<td><span data-ttu-id="04c44-790">HR</span><span class="sxs-lookup"><span data-stu-id="04c44-790">HR</span></span></td>
<td><span data-ttu-id="04c44-791">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-791">10001</span></span></td>
<td><span data-ttu-id="04c44-792">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-792">Electricity</span></span></td>
<td><span data-ttu-id="04c44-793">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-793">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="04c44-794">-1,245.71</span></span></td>
<td><span data-ttu-id="04c44-795">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-796">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-796">CC002</span></span></td>
<td><span data-ttu-id="04c44-797">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-797">Finance</span></span></td>
<td><span data-ttu-id="04c44-798">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-798">10001</span></span></td>
<td><span data-ttu-id="04c44-799">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-799">Electricity</span></span></td>
<td><span data-ttu-id="04c44-800">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-800">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-801">436.00</span><span class="sxs-lookup"><span data-stu-id="04c44-801">436.00</span></span></td>
<td><span data-ttu-id="04c44-802">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-803">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-803">CC003</span></span></td>
<td><span data-ttu-id="04c44-804">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-804">Assembly</span></span></td>
<td><span data-ttu-id="04c44-805">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-805">10001</span></span></td>
<td><span data-ttu-id="04c44-806">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-806">Electricity</span></span></td>
<td><span data-ttu-id="04c44-807">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-807">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-808">685.14</span><span class="sxs-lookup"><span data-stu-id="04c44-808">685.14</span></span></td>
<td><span data-ttu-id="04c44-809">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-810">CC004</span><span class="sxs-lookup"><span data-stu-id="04c44-810">CC004</span></span></td>
<td><span data-ttu-id="04c44-811">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="04c44-811">Packaging</span></span></td>
<td><span data-ttu-id="04c44-812">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-812">10001</span></span></td>
<td><span data-ttu-id="04c44-813">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-813">Electricity</span></span></td>
<td><span data-ttu-id="04c44-814">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-814">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-815">124.57</span><span class="sxs-lookup"><span data-stu-id="04c44-815">124.57</span></span></td>
<td><span data-ttu-id="04c44-816">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-817">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-817">CC002</span></span></td>
<td><span data-ttu-id="04c44-818">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-818">Finance</span></span></td>
<td><span data-ttu-id="04c44-819">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-819">10001</span></span></td>
<td><span data-ttu-id="04c44-820">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-820">Electricity</span></span></td>
<td><span data-ttu-id="04c44-821">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-821">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="04c44-822">-675.00</span></span></td>
<td><span data-ttu-id="04c44-823">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-824">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-824">CC003</span></span></td>
<td><span data-ttu-id="04c44-825">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-825">Assembly</span></span></td>
<td><span data-ttu-id="04c44-826">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-826">10001</span></span></td>
<td><span data-ttu-id="04c44-827">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-827">Electricity</span></span></td>
<td><span data-ttu-id="04c44-828">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-828">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-829">438.75</span><span class="sxs-lookup"><span data-stu-id="04c44-829">438.75</span></span></td>
<td><span data-ttu-id="04c44-830">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-831">CC004</span><span class="sxs-lookup"><span data-stu-id="04c44-831">CC004</span></span></td>
<td><span data-ttu-id="04c44-832">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="04c44-832">Packaging</span></span></td>
<td><span data-ttu-id="04c44-833">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-833">10001</span></span></td>
<td><span data-ttu-id="04c44-834">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-834">Electricity</span></span></td>
<td><span data-ttu-id="04c44-835">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-835">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-836">236.25</span><span class="sxs-lookup"><span data-stu-id="04c44-836">236.25</span></span></td>
<td><span data-ttu-id="04c44-837">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-838">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-838">CC002</span></span></td>
<td><span data-ttu-id="04c44-839">Finanses</span><span class="sxs-lookup"><span data-stu-id="04c44-839">Finance</span></span></td>
<td><span data-ttu-id="04c44-840">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-840">10001</span></span></td>
<td><span data-ttu-id="04c44-841">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-841">Electricity</span></span></td>
<td><span data-ttu-id="04c44-842">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-842">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="04c44-843">-8,150.29</span></span></td>
<td><span data-ttu-id="04c44-844">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-845">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-845">CC003</span></span></td>
<td><span data-ttu-id="04c44-846">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-846">Assembly</span></span></td>
<td><span data-ttu-id="04c44-847">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-847">10001</span></span></td>
<td><span data-ttu-id="04c44-848">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-848">Electricity</span></span></td>
<td><span data-ttu-id="04c44-849">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-849">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="04c44-850">5,297.69</span></span></td>
<td><span data-ttu-id="04c44-851">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-852">CC004</span><span class="sxs-lookup"><span data-stu-id="04c44-852">CC004</span></span></td>
<td><span data-ttu-id="04c44-853">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="04c44-853">Packaging</span></span></td>
<td><span data-ttu-id="04c44-854">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-854">10001</span></span></td>
<td><span data-ttu-id="04c44-855">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-855">Electricity</span></span></td>
<td><span data-ttu-id="04c44-856">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-856">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="04c44-857">2,852.60</span></span></td>
<td><span data-ttu-id="04c44-858">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-859">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-859">CC003</span></span></td>
<td><span data-ttu-id="04c44-860">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-860">Assembly</span></span></td>
<td><span data-ttu-id="04c44-861">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-861">10001</span></span></td>
<td><span data-ttu-id="04c44-862">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-862">Electricity</span></span></td>
<td><span data-ttu-id="04c44-863">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-863">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="04c44-864">-713.75</span></span></td>
<td><span data-ttu-id="04c44-865">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="04c44-866">Prod 1</span></span></td>
<td><span data-ttu-id="04c44-867">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-867">Product 1</span></span></td>
<td><span data-ttu-id="04c44-868">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-868">10001</span></span></td>
<td><span data-ttu-id="04c44-869">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-869">Electricity</span></span></td>
<td><span data-ttu-id="04c44-870">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-870">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-871">535.31</span><span class="sxs-lookup"><span data-stu-id="04c44-871">535.31</span></span></td>
<td><span data-ttu-id="04c44-872">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="04c44-873">Prod 2</span></span></td>
<td><span data-ttu-id="04c44-874">2. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-874">Product 2</span></span></td>
<td><span data-ttu-id="04c44-875">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-875">10001</span></span></td>
<td><span data-ttu-id="04c44-876">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-876">Electricity</span></span></td>
<td><span data-ttu-id="04c44-877">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-877">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-878">178.44</span><span class="sxs-lookup"><span data-stu-id="04c44-878">178.44</span></span></td>
<td><span data-ttu-id="04c44-879">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-880">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-880">CC003</span></span></td>
<td><span data-ttu-id="04c44-881">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-881">Assembly</span></span></td>
<td><span data-ttu-id="04c44-882">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-882">10001</span></span></td>
<td><span data-ttu-id="04c44-883">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-883">Electricity</span></span></td>
<td><span data-ttu-id="04c44-884">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-884">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="04c44-885">-5,982.83</span></span></td>
<td><span data-ttu-id="04c44-886">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="04c44-887">Prod 1</span></span></td>
<td><span data-ttu-id="04c44-888">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-888">Product 1</span></span></td>
<td><span data-ttu-id="04c44-889">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-889">10001</span></span></td>
<td><span data-ttu-id="04c44-890">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-890">Electricity</span></span></td>
<td><span data-ttu-id="04c44-891">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-891">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="04c44-892">4,487.12</span></span></td>
<td><span data-ttu-id="04c44-893">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="04c44-894">Prod 2</span></span></td>
<td><span data-ttu-id="04c44-895">2. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-895">Product 2</span></span></td>
<td><span data-ttu-id="04c44-896">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-896">10001</span></span></td>
<td><span data-ttu-id="04c44-897">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-897">Electricity</span></span></td>
<td><span data-ttu-id="04c44-898">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-898">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="04c44-899">1,495.71</span></span></td>
<td><span data-ttu-id="04c44-900">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-901">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-901">CC003</span></span></td>
<td><span data-ttu-id="04c44-902">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-902">Assembly</span></span></td>
<td><span data-ttu-id="04c44-903">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-903">10001</span></span></td>
<td><span data-ttu-id="04c44-904">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-904">Electricity</span></span></td>
<td><span data-ttu-id="04c44-905">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-905">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="04c44-906">-286.25</span></span></td>
<td><span data-ttu-id="04c44-907">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="04c44-908">Prod 1</span></span></td>
<td><span data-ttu-id="04c44-909">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-909">Product 1</span></span></td>
<td><span data-ttu-id="04c44-910">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-910">10001</span></span></td>
<td><span data-ttu-id="04c44-911">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-911">Electricity</span></span></td>
<td><span data-ttu-id="04c44-912">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-912">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-913">241.05</span><span class="sxs-lookup"><span data-stu-id="04c44-913">241.05</span></span></td>
<td><span data-ttu-id="04c44-914">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="04c44-915">Prod 2</span></span></td>
<td><span data-ttu-id="04c44-916">2. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-916">Product 2</span></span></td>
<td><span data-ttu-id="04c44-917">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-917">10001</span></span></td>
<td><span data-ttu-id="04c44-918">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-918">Electricity</span></span></td>
<td><span data-ttu-id="04c44-919">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-919">Fixed cost</span></span></td>
<td><span data-ttu-id="04c44-920">45.20</span><span class="sxs-lookup"><span data-stu-id="04c44-920">45.20</span></span></td>
<td><span data-ttu-id="04c44-921">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-922">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-922">CC003</span></span></td>
<td><span data-ttu-id="04c44-923">Montāža</span><span class="sxs-lookup"><span data-stu-id="04c44-923">Assembly</span></span></td>
<td><span data-ttu-id="04c44-924">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-924">10001</span></span></td>
<td><span data-ttu-id="04c44-925">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-925">Electricity</span></span></td>
<td><span data-ttu-id="04c44-926">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-926">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="04c44-927">-2,977.17</span></span></td>
<td><span data-ttu-id="04c44-928">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="04c44-929">Prod 1</span></span></td>
<td><span data-ttu-id="04c44-930">1. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-930">Product 1</span></span></td>
<td><span data-ttu-id="04c44-931">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-931">10001</span></span></td>
<td><span data-ttu-id="04c44-932">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-932">Electricity</span></span></td>
<td><span data-ttu-id="04c44-933">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-933">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="04c44-934">2,507.09</span></span></td>
<td><span data-ttu-id="04c44-935">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04c44-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="04c44-936">Prod 2</span></span></td>
<td><span data-ttu-id="04c44-937">2. prece</span><span class="sxs-lookup"><span data-stu-id="04c44-937">Product 2</span></span></td>
<td><span data-ttu-id="04c44-938">10001</span><span class="sxs-lookup"><span data-stu-id="04c44-938">10001</span></span></td>
<td><span data-ttu-id="04c44-939">Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-939">Electricity</span></span></td>
<td><span data-ttu-id="04c44-940">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-940">Variable cost</span></span></td>
<td><span data-ttu-id="04c44-941">470.08</span><span class="sxs-lookup"><span data-stu-id="04c44-941">470.08</span></span></td>
<td><span data-ttu-id="04c44-942">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="04c44-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="04c44-943">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="04c44-943">Conclusion</span></span>
<span data-ttu-id="04c44-944">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="04c44-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="04c44-945">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="04c44-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="04c44-946">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="04c44-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="04c44-947">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="04c44-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="04c44-948">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="04c44-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="04c44-949">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="04c44-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="04c44-950">Summa</span><span class="sxs-lookup"><span data-stu-id="04c44-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="04c44-951">CC099</span><span class="sxs-lookup"><span data-stu-id="04c44-951">CC099</span></span></th>
<th><span data-ttu-id="04c44-952">CC001</span><span class="sxs-lookup"><span data-stu-id="04c44-952">CC001</span></span></th>
<th><span data-ttu-id="04c44-953">CC002</span><span class="sxs-lookup"><span data-stu-id="04c44-953">CC002</span></span></th>
<th><span data-ttu-id="04c44-954">CC003</span><span class="sxs-lookup"><span data-stu-id="04c44-954">CC003</span></span></th>
<th><span data-ttu-id="04c44-955">CC004</span><span class="sxs-lookup"><span data-stu-id="04c44-955">CC004</span></span></th>
<th><span data-ttu-id="04c44-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="04c44-956">Proj 1</span></span></th>
<th><span data-ttu-id="04c44-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="04c44-957">Proj 2</span></span></th>
<th><span data-ttu-id="04c44-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="04c44-958">Prod 1</span></span></th>
<th><span data-ttu-id="04c44-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="04c44-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="04c44-960">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="04c44-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="04c44-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="04c44-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="04c44-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="04c44-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="04c44-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="04c44-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="04c44-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="04c44-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="04c44-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="04c44-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="04c44-970">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="04c44-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-971">0,00</span><span class="sxs-lookup"><span data-stu-id="04c44-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="04c44-972">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-973">0,00</span><span class="sxs-lookup"><span data-stu-id="04c44-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-974">0,00</span><span class="sxs-lookup"><span data-stu-id="04c44-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-975">0,00</span><span class="sxs-lookup"><span data-stu-id="04c44-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-976">0,00</span><span class="sxs-lookup"><span data-stu-id="04c44-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-977">0,00</span><span class="sxs-lookup"><span data-stu-id="04c44-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="04c44-978">776.36</span><span class="sxs-lookup"><span data-stu-id="04c44-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-979">223.64</span><span class="sxs-lookup"><span data-stu-id="04c44-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="04c44-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="04c44-981">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="04c44-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-982">000</span><span class="sxs-lookup"><span data-stu-id="04c44-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-983">0,00</span><span class="sxs-lookup"><span data-stu-id="04c44-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-984">0,00</span><span class="sxs-lookup"><span data-stu-id="04c44-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-985">0,00</span><span class="sxs-lookup"><span data-stu-id="04c44-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-986">0,00</span><span class="sxs-lookup"><span data-stu-id="04c44-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-987">30,00</span><span class="sxs-lookup"><span data-stu-id="04c44-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-988">10,00</span><span class="sxs-lookup"><span data-stu-id="04c44-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="04c44-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="04c44-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04c44-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="04c44-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="04c44-992">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="04c44-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="04c44-993">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="04c44-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="04c44-994">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="04c44-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="04c44-995">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="04c44-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="04c44-996">Plašāku informāciju skatiet [Izmaksu apkopojuma politika un pieskaitāmo izmaksu aprēķins](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="04c44-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



