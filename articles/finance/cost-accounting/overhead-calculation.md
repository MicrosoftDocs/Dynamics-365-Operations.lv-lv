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
ms.openlocfilehash: 882804141a6b520e2420343958c7a6b02a7e09ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208851"
---
# <a name="overhead-calculation"></a><span data-ttu-id="fadc8-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="fadc8-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fadc8-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="fadc8-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="fadc8-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="fadc8-105">Term definition</span></span>
---------------

<span data-ttu-id="fadc8-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="fadc8-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="fadc8-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="fadc8-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="fadc8-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="fadc8-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="fadc8-109">Īre</span><span class="sxs-lookup"><span data-stu-id="fadc8-109">Rent</span></span>
-   <span data-ttu-id="fadc8-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-110">Electricity</span></span>
-   <span data-ttu-id="fadc8-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="fadc8-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="fadc8-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="fadc8-112">Overhead calculation overview</span></span>
<span data-ttu-id="fadc8-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="fadc8-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="fadc8-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="fadc8-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="fadc8-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="fadc8-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="fadc8-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="fadc8-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="fadc8-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="fadc8-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="fadc8-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="fadc8-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="fadc8-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="fadc8-119">Version type</span></span>
-   <span data-ttu-id="fadc8-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="fadc8-120">Date and time</span></span>
-   <span data-ttu-id="fadc8-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="fadc8-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="fadc8-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="fadc8-122">Fiscal year</span></span>
-   <span data-ttu-id="fadc8-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="fadc8-123">Fiscal period</span></span>

<span data-ttu-id="fadc8-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="fadc8-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="fadc8-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="fadc8-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="fadc8-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="fadc8-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="fadc8-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="fadc8-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="fadc8-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="fadc8-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="fadc8-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="fadc8-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="fadc8-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="fadc8-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="fadc8-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="fadc8-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="fadc8-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="fadc8-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="fadc8-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="fadc8-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="fadc8-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="fadc8-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="fadc8-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="fadc8-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="fadc8-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="fadc8-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="fadc8-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fadc8-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fadc8-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="fadc8-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fadc8-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="fadc8-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="fadc8-140">Main account</span></span></th>
<th><span data-ttu-id="fadc8-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="fadc8-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="fadc8-143">CC099</span><span class="sxs-lookup"><span data-stu-id="fadc8-143">CC099</span></span></td>
<td><span data-ttu-id="fadc8-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fadc8-144">Default cost center</span></span></td>
<td><span data-ttu-id="fadc8-145">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-145">10001</span></span></td>
<td><span data-ttu-id="fadc8-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-146">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="fadc8-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="fadc8-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="fadc8-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="fadc8-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="fadc8-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="fadc8-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="fadc8-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="fadc8-151">Define the cost behavior rule</span></span>

<span data-ttu-id="fadc8-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="fadc8-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="fadc8-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="fadc8-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="fadc8-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="fadc8-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="fadc8-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="fadc8-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="fadc8-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="fadc8-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="fadc8-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="fadc8-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="fadc8-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="fadc8-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fadc8-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fadc8-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fadc8-160">Journal</span></span></th>
<th><span data-ttu-id="fadc8-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="fadc8-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="fadc8-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="fadc8-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="fadc8-163">Versija</span><span class="sxs-lookup"><span data-stu-id="fadc8-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-164">00001</span><span class="sxs-lookup"><span data-stu-id="fadc8-164">00001</span></span></td>
<td><span data-ttu-id="fadc8-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="fadc8-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="fadc8-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="fadc8-166">Fiscal</span></span></td>
<td><span data-ttu-id="fadc8-167">2017</span><span class="sxs-lookup"><span data-stu-id="fadc8-167">2017</span></span></td>
<td><span data-ttu-id="fadc8-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-168">Period 1</span></span></td>
<td><span data-ttu-id="fadc8-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="fadc8-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="fadc8-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="fadc8-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fadc8-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fadc8-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="fadc8-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fadc8-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fadc8-173">Cost element</span></span></th>
<th><span data-ttu-id="fadc8-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fadc8-174">Cost behavior</span></span></th>
<th><span data-ttu-id="fadc8-175">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="fadc8-177">CC099</span><span class="sxs-lookup"><span data-stu-id="fadc8-177">CC099</span></span></td>
<td><span data-ttu-id="fadc8-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fadc8-178">Default cost center</span></span></td>
<td><span data-ttu-id="fadc8-179">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-179">10001</span></span></td>
<td><span data-ttu-id="fadc8-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-180">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="fadc8-181">Unclassified</span></span></td>
<td><span data-ttu-id="fadc8-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="fadc8-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="fadc8-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fadc8-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fadc8-185">Cost element</span></span></th>
<th><span data-ttu-id="fadc8-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fadc8-186">Cost behavior</span></span></th>
<th><span data-ttu-id="fadc8-187">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-187">Amount</span></span></th>
<th><span data-ttu-id="fadc8-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fadc8-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-189">CC099</span><span class="sxs-lookup"><span data-stu-id="fadc8-189">CC099</span></span></td>
<td><span data-ttu-id="fadc8-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fadc8-190">Default cost center</span></span></td>
<td><span data-ttu-id="fadc8-191">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-191">10001</span></span></td>
<td><span data-ttu-id="fadc8-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-192">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="fadc8-193">Unclassified</span></span></td>
<td><span data-ttu-id="fadc8-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-194">10,000.00</span></span></td>
<td><span data-ttu-id="fadc8-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-196">CC099</span><span class="sxs-lookup"><span data-stu-id="fadc8-196">CC099</span></span></td>
<td><span data-ttu-id="fadc8-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fadc8-197">Default cost center</span></span></td>
<td><span data-ttu-id="fadc8-198">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-198">10001</span></span></td>
<td><span data-ttu-id="fadc8-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-199">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="fadc8-200">Unclassified</span></span></td>
<td><span data-ttu-id="fadc8-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-201">-10,000.00</span></span></td>
<td><span data-ttu-id="fadc8-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-203">CC099</span><span class="sxs-lookup"><span data-stu-id="fadc8-203">CC099</span></span></td>
<td><span data-ttu-id="fadc8-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fadc8-204">Default cost center</span></span></td>
<td><span data-ttu-id="fadc8-205">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-205">10001</span></span></td>
<td><span data-ttu-id="fadc8-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-206">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-207">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-208">1,000.00</span></span></td>
<td><span data-ttu-id="fadc8-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-210">CC099</span><span class="sxs-lookup"><span data-stu-id="fadc8-210">CC099</span></span></td>
<td><span data-ttu-id="fadc8-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fadc8-211">Default cost center</span></span></td>
<td><span data-ttu-id="fadc8-212">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-212">10001</span></span></td>
<td><span data-ttu-id="fadc8-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-213">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-214">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="fadc8-215">9,000.00</span></span></td>
<td><span data-ttu-id="fadc8-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fadc8-217">Sīkāku informāciju skatiet šeit: [Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="fadc8-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="fadc8-218">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="fadc8-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="fadc8-219">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="fadc8-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="fadc8-220">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="fadc8-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="fadc8-221">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="fadc8-221">Define the cost distribution rule</span></span>

<span data-ttu-id="fadc8-222">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="fadc8-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="fadc8-223">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="fadc8-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="fadc8-224">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="fadc8-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="fadc8-225">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="fadc8-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="fadc8-226">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="fadc8-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="fadc8-227">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="fadc8-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-228">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-228">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="fadc8-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-230">CC001</span><span class="sxs-lookup"><span data-stu-id="fadc8-230">CC001</span></span></td>
<td><span data-ttu-id="fadc8-231">HR</span><span class="sxs-lookup"><span data-stu-id="fadc8-231">HR</span></span></td>
<td><span data-ttu-id="fadc8-232">1000</span><span class="sxs-lookup"><span data-stu-id="fadc8-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-233">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-233">CC002</span></span></td>
<td><span data-ttu-id="fadc8-234">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-234">Finance</span></span></td>
<td><span data-ttu-id="fadc8-235">6,000</span><span class="sxs-lookup"><span data-stu-id="fadc8-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-236">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-236">CC003</span></span></td>
<td><span data-ttu-id="fadc8-237">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-237">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-238">0</span><span class="sxs-lookup"><span data-stu-id="fadc8-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fadc8-239">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="fadc8-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-240">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-240">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-241">Lielums</span><span class="sxs-lookup"><span data-stu-id="fadc8-241">Magnitude</span></span></th>
<th><span data-ttu-id="fadc8-242">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fadc8-242">Allocation factor</span></span></th>
<th><span data-ttu-id="fadc8-243">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-244">CC001</span><span class="sxs-lookup"><span data-stu-id="fadc8-244">CC001</span></span></td>
<td><span data-ttu-id="fadc8-245">HR</span><span class="sxs-lookup"><span data-stu-id="fadc8-245">HR</span></span></td>
<td><span data-ttu-id="fadc8-246">1000</span><span class="sxs-lookup"><span data-stu-id="fadc8-246">1,000</span></span></td>
<td><span data-ttu-id="fadc8-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="fadc8-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="fadc8-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-249">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-249">CC002</span></span></td>
<td><span data-ttu-id="fadc8-250">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-250">Finance</span></span></td>
<td><span data-ttu-id="fadc8-251">6,000</span><span class="sxs-lookup"><span data-stu-id="fadc8-251">6,000</span></span></td>
<td><span data-ttu-id="fadc8-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="fadc8-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="fadc8-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-254">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-254">CC003</span></span></td>
<td><span data-ttu-id="fadc8-255">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-255">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-256">0</span><span class="sxs-lookup"><span data-stu-id="fadc8-256">0</span></span></td>
<td><span data-ttu-id="fadc8-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="fadc8-258">0,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fadc8-259">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="fadc8-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="fadc8-260">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="fadc8-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-261">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-261">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-262">Formula</span><span class="sxs-lookup"><span data-stu-id="fadc8-262">Formula</span></span></th>
<th><span data-ttu-id="fadc8-263">Lielums</span><span class="sxs-lookup"><span data-stu-id="fadc8-263">Magnitude</span></span></th>
<th><span data-ttu-id="fadc8-264">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fadc8-264">Allocation factor</span></span></th>
<th><span data-ttu-id="fadc8-265">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-266">CC001</span><span class="sxs-lookup"><span data-stu-id="fadc8-266">CC001</span></span></td>
<td><span data-ttu-id="fadc8-267">HR</span><span class="sxs-lookup"><span data-stu-id="fadc8-267">HR</span></span></td>
<td><span data-ttu-id="fadc8-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="fadc8-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="fadc8-269">1.</span><span class="sxs-lookup"><span data-stu-id="fadc8-269">1</span></span></td>
<td><span data-ttu-id="fadc8-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="fadc8-271">500,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-272">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-272">CC002</span></span></td>
<td><span data-ttu-id="fadc8-273">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-273">Finance</span></span></td>
<td><span data-ttu-id="fadc8-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="fadc8-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="fadc8-275">1.</span><span class="sxs-lookup"><span data-stu-id="fadc8-275">1</span></span></td>
<td><span data-ttu-id="fadc8-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="fadc8-277">500,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-278">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-278">CC003</span></span></td>
<td><span data-ttu-id="fadc8-279">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-279">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="fadc8-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="fadc8-281">0</span><span class="sxs-lookup"><span data-stu-id="fadc8-281">0</span></span></td>
<td><span data-ttu-id="fadc8-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="fadc8-283">0,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="fadc8-284">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fadc8-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fadc8-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fadc8-285">Journal</span></span></th>
<th><span data-ttu-id="fadc8-286">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="fadc8-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="fadc8-287">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="fadc8-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="fadc8-288">Versija</span><span class="sxs-lookup"><span data-stu-id="fadc8-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-289">00002</span><span class="sxs-lookup"><span data-stu-id="fadc8-289">00002</span></span></td>
<td><span data-ttu-id="fadc8-290">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="fadc8-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="fadc8-291">Finanšu</span><span class="sxs-lookup"><span data-stu-id="fadc8-291">Fiscal</span></span></td>
<td><span data-ttu-id="fadc8-292">2017</span><span class="sxs-lookup"><span data-stu-id="fadc8-292">2017</span></span></td>
<td><span data-ttu-id="fadc8-293">Periods 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-293">Period 1</span></span></td>
<td><span data-ttu-id="fadc8-294">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="fadc8-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="fadc8-295">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="fadc8-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fadc8-296">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fadc8-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="fadc8-297">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fadc8-298">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fadc8-298">Cost element</span></span></th>
<th><span data-ttu-id="fadc8-299">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fadc8-299">Cost behavior</span></span></th>
<th><span data-ttu-id="fadc8-300">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-301">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-302">CC099</span><span class="sxs-lookup"><span data-stu-id="fadc8-302">CC099</span></span></td>
<td><span data-ttu-id="fadc8-303">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fadc8-303">Default cost center</span></span></td>
<td><span data-ttu-id="fadc8-304">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-304">10001</span></span></td>
<td><span data-ttu-id="fadc8-305">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-305">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-306">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-306">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-308">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-309">CC099</span><span class="sxs-lookup"><span data-stu-id="fadc8-309">CC099</span></span></td>
<td><span data-ttu-id="fadc8-310">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fadc8-310">Default cost center</span></span></td>
<td><span data-ttu-id="fadc8-311">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-311">10001</span></span></td>
<td><span data-ttu-id="fadc8-312">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-312">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-313">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-313">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="fadc8-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="fadc8-315">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="fadc8-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-316">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fadc8-317">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fadc8-317">Cost element</span></span></th>
<th><span data-ttu-id="fadc8-318">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fadc8-318">Cost behavior</span></span></th>
<th><span data-ttu-id="fadc8-319">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-319">Amount</span></span></th>
<th><span data-ttu-id="fadc8-320">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fadc8-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-321">CC099</span><span class="sxs-lookup"><span data-stu-id="fadc8-321">CC099</span></span></td>
<td><span data-ttu-id="fadc8-322">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fadc8-322">Default cost center</span></span></td>
<td><span data-ttu-id="fadc8-323">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-323">10001</span></span></td>
<td><span data-ttu-id="fadc8-324">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-324">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-325">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-325">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-326">-1000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-326">-1,000.00</span></span></td>
<td><span data-ttu-id="fadc8-327">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-328">CC001</span><span class="sxs-lookup"><span data-stu-id="fadc8-328">CC001</span></span></td>
<td><span data-ttu-id="fadc8-329">HR</span><span class="sxs-lookup"><span data-stu-id="fadc8-329">HR</span></span></td>
<td><span data-ttu-id="fadc8-330">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-330">10001</span></span></td>
<td><span data-ttu-id="fadc8-331">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-331">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-332">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-332">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-333">500,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-333">500.00</span></span></td>
<td><span data-ttu-id="fadc8-334">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-335">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-335">CC002</span></span></td>
<td><span data-ttu-id="fadc8-336">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-336">Finance</span></span></td>
<td><span data-ttu-id="fadc8-337">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-337">10001</span></span></td>
<td><span data-ttu-id="fadc8-338">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-338">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-339">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-339">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-340">500,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-340">500.00</span></span></td>
<td><span data-ttu-id="fadc8-341">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-342">CC099</span><span class="sxs-lookup"><span data-stu-id="fadc8-342">CC099</span></span></td>
<td><span data-ttu-id="fadc8-343">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fadc8-343">Default cost center</span></span></td>
<td><span data-ttu-id="fadc8-344">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-344">10001</span></span></td>
<td><span data-ttu-id="fadc8-345">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-345">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-346">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-346">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-347">-9,000.00</span></span></td>
<td><span data-ttu-id="fadc8-348">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-349">CC001</span><span class="sxs-lookup"><span data-stu-id="fadc8-349">CC001</span></span></td>
<td><span data-ttu-id="fadc8-350">HR</span><span class="sxs-lookup"><span data-stu-id="fadc8-350">HR</span></span></td>
<td><span data-ttu-id="fadc8-351">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-351">10001</span></span></td>
<td><span data-ttu-id="fadc8-352">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-352">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-353">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-353">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="fadc8-354">1,285.71</span></span></td>
<td><span data-ttu-id="fadc8-355">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-356">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-356">CC002</span></span></td>
<td><span data-ttu-id="fadc8-357">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-357">Finance</span></span></td>
<td><span data-ttu-id="fadc8-358">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-358">10001</span></span></td>
<td><span data-ttu-id="fadc8-359">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-359">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-360">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-360">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="fadc8-361">7,714.29</span></span></td>
<td><span data-ttu-id="fadc8-362">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fadc8-363">Sīkāku informāciju skatiet šeit: [Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="fadc8-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="fadc8-364">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="fadc8-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="fadc8-365">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="fadc8-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="fadc8-366">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="fadc8-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="fadc8-367">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="fadc8-367">Define the overhead rate</span></span>

<span data-ttu-id="fadc8-368">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="fadc8-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="fadc8-369">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="fadc8-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-370">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-370">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-371">Stundas</span><span class="sxs-lookup"><span data-stu-id="fadc8-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-372">Proj 1</span></span></td>
<td><span data-ttu-id="fadc8-373">1. projekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-373">Project 1</span></span></td>
<td><span data-ttu-id="fadc8-374">3.</span><span class="sxs-lookup"><span data-stu-id="fadc8-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-375">Proj 2</span></span></td>
<td><span data-ttu-id="fadc8-376">2. projekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-376">Project 2</span></span></td>
<td><span data-ttu-id="fadc8-377">1.</span><span class="sxs-lookup"><span data-stu-id="fadc8-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fadc8-378">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="fadc8-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-379">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-379">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-380">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fadc8-380">Cost element</span></span></th>
<th><span data-ttu-id="fadc8-381">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fadc8-381">Cost behavior</span></span></th>
<th><span data-ttu-id="fadc8-382">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="fadc8-382">Units</span></span></th>
<th><span data-ttu-id="fadc8-383">Likme</span><span class="sxs-lookup"><span data-stu-id="fadc8-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-384">CC001</span><span class="sxs-lookup"><span data-stu-id="fadc8-384">CC001</span></span></td>
<td><span data-ttu-id="fadc8-385">HR</span><span class="sxs-lookup"><span data-stu-id="fadc8-385">HR</span></span></td>
<td><span data-ttu-id="fadc8-386">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-386">10001</span></span></td>
<td><span data-ttu-id="fadc8-387">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-387">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-388">1</span><span class="sxs-lookup"><span data-stu-id="fadc8-388">1</span></span></td>
<td><span data-ttu-id="fadc8-389">10</span><span class="sxs-lookup"><span data-stu-id="fadc8-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fadc8-390">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="fadc8-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-391">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-391">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-392">Lielums</span><span class="sxs-lookup"><span data-stu-id="fadc8-392">Magnitude</span></span></th>
<th><span data-ttu-id="fadc8-393">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fadc8-393">Cost element</span></span></th>
<th><span data-ttu-id="fadc8-394">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fadc8-394">Allocation factor</span></span></th>
<th><span data-ttu-id="fadc8-395">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-396">Proj 1</span></span></td>
<td><span data-ttu-id="fadc8-397">1. projekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-397">Project 1</span></span></td>
<td><span data-ttu-id="fadc8-398">3.</span><span class="sxs-lookup"><span data-stu-id="fadc8-398">3</span></span></td>
<td><span data-ttu-id="fadc8-399">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-399">10001</span></span></td>
<td><span data-ttu-id="fadc8-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="fadc8-401">30,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-402">Proj 2</span></span></td>
<td><span data-ttu-id="fadc8-403">2. projekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-403">Project 2</span></span></td>
<td><span data-ttu-id="fadc8-404">1.</span><span class="sxs-lookup"><span data-stu-id="fadc8-404">1</span></span></td>
<td><span data-ttu-id="fadc8-405">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-405">10001</span></span></td>
<td><span data-ttu-id="fadc8-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="fadc8-407">10,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="fadc8-408">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fadc8-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fadc8-409">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fadc8-409">Journal</span></span></th>
<th><span data-ttu-id="fadc8-410">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="fadc8-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="fadc8-411">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="fadc8-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="fadc8-412">Versija</span><span class="sxs-lookup"><span data-stu-id="fadc8-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-413">00003</span><span class="sxs-lookup"><span data-stu-id="fadc8-413">00003</span></span></td>
<td><span data-ttu-id="fadc8-414">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="fadc8-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="fadc8-415">Finanšu</span><span class="sxs-lookup"><span data-stu-id="fadc8-415">Fiscal</span></span></td>
<td><span data-ttu-id="fadc8-416">2017</span><span class="sxs-lookup"><span data-stu-id="fadc8-416">2017</span></span></td>
<td><span data-ttu-id="fadc8-417">Periods 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-417">Period 1</span></span></td>
<td><span data-ttu-id="fadc8-418">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="fadc8-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="fadc8-419">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="fadc8-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fadc8-420">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fadc8-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="fadc8-421">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-421">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-422">Lielums</span><span class="sxs-lookup"><span data-stu-id="fadc8-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-423">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-424">Proj 1</span></span></td>
<td><span data-ttu-id="fadc8-425">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="fadc8-426">3,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-427">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-428">Proj 2</span></span></td>
<td><span data-ttu-id="fadc8-429">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="fadc8-430">1,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="fadc8-431">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="fadc8-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-432">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fadc8-433">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fadc8-433">Cost element</span></span></th>
<th><span data-ttu-id="fadc8-434">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fadc8-434">Cost behavior</span></span></th>
<th><span data-ttu-id="fadc8-435">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-435">Amount</span></span></th>
<th><span data-ttu-id="fadc8-436">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fadc8-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="fadc8-437">CC0001</span></span></td>
<td><span data-ttu-id="fadc8-438">HR</span><span class="sxs-lookup"><span data-stu-id="fadc8-438">HR</span></span></td>
<td><span data-ttu-id="fadc8-439">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-439">10001</span></span></td>
<td><span data-ttu-id="fadc8-440">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-440">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-441">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-441">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-442">-30.00</span></span></td>
<td><span data-ttu-id="fadc8-443">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-444">Proj 1</span></span></td>
<td><span data-ttu-id="fadc8-445">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="fadc8-446">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-446">10001</span></span></td>
<td><span data-ttu-id="fadc8-447">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-447">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-448">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-448">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-449">30,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-449">30.00</span></span></td>
<td><span data-ttu-id="fadc8-450">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-451">CC001</span><span class="sxs-lookup"><span data-stu-id="fadc8-451">CC001</span></span></td>
<td><span data-ttu-id="fadc8-452">HR</span><span class="sxs-lookup"><span data-stu-id="fadc8-452">HR</span></span></td>
<td><span data-ttu-id="fadc8-453">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-453">10001</span></span></td>
<td><span data-ttu-id="fadc8-454">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-454">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-455">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-455">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-456">-10.00</span></span></td>
<td><span data-ttu-id="fadc8-457">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-458">Proj 2</span></span></td>
<td><span data-ttu-id="fadc8-459">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="fadc8-460">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-460">10001</span></span></td>
<td><span data-ttu-id="fadc8-461">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-461">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-462">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-462">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-463">10,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-463">10.00</span></span></td>
<td><span data-ttu-id="fadc8-464">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fadc8-465">Sīkāku informāciju skatiet šeit: [Pieskaitāmo izmaksu aprēķina veikšana](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="fadc8-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="fadc8-466">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="fadc8-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="fadc8-467">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="fadc8-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="fadc8-468">Finance atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="fadc8-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="fadc8-469">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="fadc8-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="fadc8-470">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="fadc8-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="fadc8-471">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="fadc8-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="fadc8-472">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="fadc8-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="fadc8-473">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="fadc8-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="fadc8-474">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="fadc8-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="fadc8-475">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="fadc8-475">Define the cost allocation</span></span>

<span data-ttu-id="fadc8-476">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="fadc8-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="fadc8-477">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="fadc8-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="fadc8-478">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="fadc8-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-479">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-479">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-480">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="fadc8-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-481">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-481">CC002</span></span></td>
<td><span data-ttu-id="fadc8-482">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-482">Finance</span></span></td>
<td><span data-ttu-id="fadc8-483">35</span><span class="sxs-lookup"><span data-stu-id="fadc8-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-484">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-484">CC003</span></span></td>
<td><span data-ttu-id="fadc8-485">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-485">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-486">55</span><span class="sxs-lookup"><span data-stu-id="fadc8-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-487">CC004</span><span class="sxs-lookup"><span data-stu-id="fadc8-487">CC004</span></span></td>
<td><span data-ttu-id="fadc8-488">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fadc8-488">Packaging</span></span></td>
<td><span data-ttu-id="fadc8-489">10.</span><span class="sxs-lookup"><span data-stu-id="fadc8-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fadc8-490">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="fadc8-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="fadc8-491">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="fadc8-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-492">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-492">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-493">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="fadc8-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-494">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-494">CC003</span></span></td>
<td><span data-ttu-id="fadc8-495">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-495">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-496">65</span><span class="sxs-lookup"><span data-stu-id="fadc8-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-497">CC004</span><span class="sxs-lookup"><span data-stu-id="fadc8-497">CC004</span></span></td>
<td><span data-ttu-id="fadc8-498">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fadc8-498">Packaging</span></span></td>
<td><span data-ttu-id="fadc8-499">35</span><span class="sxs-lookup"><span data-stu-id="fadc8-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fadc8-500">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="fadc8-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="fadc8-501">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="fadc8-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-502">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-502">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-503">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="fadc8-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-504">Prod 1</span></span></td>
<td><span data-ttu-id="fadc8-505">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-505">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-506">60</span><span class="sxs-lookup"><span data-stu-id="fadc8-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-507">Prod 2</span></span></td>
<td><span data-ttu-id="fadc8-508">2. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-508">Product 2</span></span></td>
<td><span data-ttu-id="fadc8-509">20</span><span class="sxs-lookup"><span data-stu-id="fadc8-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fadc8-510">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="fadc8-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="fadc8-511">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="fadc8-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-512">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-512">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-513">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="fadc8-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-514">Prod 1</span></span></td>
<td><span data-ttu-id="fadc8-515">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-515">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-516">80</span><span class="sxs-lookup"><span data-stu-id="fadc8-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-517">Prod 2</span></span></td>
<td><span data-ttu-id="fadc8-518">2. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-518">Product 2</span></span></td>
<td><span data-ttu-id="fadc8-519">15</span><span class="sxs-lookup"><span data-stu-id="fadc8-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="fadc8-520">Statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="fadc8-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="fadc8-521">Sīkāku informāciju skatiet šeit: [Statistikas mēru nodrošinātāja veidne](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="fadc8-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="fadc8-522">Nākamajā tabulā ir parādīts rezultāts, ja tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījuma pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="fadc8-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-523">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-523">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-524">Lielums</span><span class="sxs-lookup"><span data-stu-id="fadc8-524">Magnitude</span></span></th>
<th><span data-ttu-id="fadc8-525">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fadc8-525">Allocation factor</span></span></th>
<th><span data-ttu-id="fadc8-526">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-526">Amount</span></span></th>
<th><span data-ttu-id="fadc8-527">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fadc8-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-528">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-528">CC002</span></span></td>
<td><span data-ttu-id="fadc8-529">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-529">Finance</span></span></td>
<td><span data-ttu-id="fadc8-530">35</span><span class="sxs-lookup"><span data-stu-id="fadc8-530">35</span></span></td>
<td><span data-ttu-id="fadc8-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="fadc8-532">175.00</span><span class="sxs-lookup"><span data-stu-id="fadc8-532">175.00</span></span></td>
<td><span data-ttu-id="fadc8-533">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-534">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-534">CC003</span></span></td>
<td><span data-ttu-id="fadc8-535">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-535">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-536">55</span><span class="sxs-lookup"><span data-stu-id="fadc8-536">55</span></span></td>
<td><span data-ttu-id="fadc8-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="fadc8-538">275.00</span><span class="sxs-lookup"><span data-stu-id="fadc8-538">275.00</span></span></td>
<td><span data-ttu-id="fadc8-539">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-540">CC004</span><span class="sxs-lookup"><span data-stu-id="fadc8-540">CC004</span></span></td>
<td><span data-ttu-id="fadc8-541">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fadc8-541">Packaging</span></span></td>
<td><span data-ttu-id="fadc8-542">10.</span><span class="sxs-lookup"><span data-stu-id="fadc8-542">10</span></span></td>
<td><span data-ttu-id="fadc8-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="fadc8-544">50,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-544">50.00</span></span></td>
<td><span data-ttu-id="fadc8-545">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-546">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-546">CC002</span></span></td>
<td><span data-ttu-id="fadc8-547">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-547">Finance</span></span></td>
<td><span data-ttu-id="fadc8-548">35</span><span class="sxs-lookup"><span data-stu-id="fadc8-548">35</span></span></td>
<td><span data-ttu-id="fadc8-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="fadc8-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="fadc8-550">436.00</span><span class="sxs-lookup"><span data-stu-id="fadc8-550">436.00</span></span></td>
<td><span data-ttu-id="fadc8-551">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-552">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-552">CC003</span></span></td>
<td><span data-ttu-id="fadc8-553">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-553">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-554">55</span><span class="sxs-lookup"><span data-stu-id="fadc8-554">55</span></span></td>
<td><span data-ttu-id="fadc8-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="fadc8-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="fadc8-556">685.14</span><span class="sxs-lookup"><span data-stu-id="fadc8-556">685.14</span></span></td>
<td><span data-ttu-id="fadc8-557">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-558">CC004</span><span class="sxs-lookup"><span data-stu-id="fadc8-558">CC004</span></span></td>
<td><span data-ttu-id="fadc8-559">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fadc8-559">Packaging</span></span></td>
<td><span data-ttu-id="fadc8-560">10.</span><span class="sxs-lookup"><span data-stu-id="fadc8-560">10</span></span></td>
<td><span data-ttu-id="fadc8-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="fadc8-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="fadc8-562">124.57</span><span class="sxs-lookup"><span data-stu-id="fadc8-562">124.57</span></span></td>
<td><span data-ttu-id="fadc8-563">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fadc8-564">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="fadc8-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-565">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-565">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-566">Lielums</span><span class="sxs-lookup"><span data-stu-id="fadc8-566">Magnitude</span></span></th>
<th><span data-ttu-id="fadc8-567">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fadc8-567">Allocation factor</span></span></th>
<th><span data-ttu-id="fadc8-568">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-568">Amount</span></span></th>
<th><span data-ttu-id="fadc8-569">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fadc8-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-570">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-570">CC003</span></span></td>
<td><span data-ttu-id="fadc8-571">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-571">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-572">65</span><span class="sxs-lookup"><span data-stu-id="fadc8-572">65</span></span></td>
<td><span data-ttu-id="fadc8-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="fadc8-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="fadc8-574">438.75</span><span class="sxs-lookup"><span data-stu-id="fadc8-574">438.75</span></span></td>
<td><span data-ttu-id="fadc8-575">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-576">CC004</span><span class="sxs-lookup"><span data-stu-id="fadc8-576">CC004</span></span></td>
<td><span data-ttu-id="fadc8-577">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fadc8-577">Packaging</span></span></td>
<td><span data-ttu-id="fadc8-578">35</span><span class="sxs-lookup"><span data-stu-id="fadc8-578">35</span></span></td>
<td><span data-ttu-id="fadc8-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="fadc8-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="fadc8-580">236.25</span><span class="sxs-lookup"><span data-stu-id="fadc8-580">236.25</span></span></td>
<td><span data-ttu-id="fadc8-581">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-582">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-582">CC003</span></span></td>
<td><span data-ttu-id="fadc8-583">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-583">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-584">65</span><span class="sxs-lookup"><span data-stu-id="fadc8-584">65</span></span></td>
<td><span data-ttu-id="fadc8-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="fadc8-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="fadc8-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="fadc8-586">5,297.69</span></span></td>
<td><span data-ttu-id="fadc8-587">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-588">CC004</span><span class="sxs-lookup"><span data-stu-id="fadc8-588">CC004</span></span></td>
<td><span data-ttu-id="fadc8-589">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fadc8-589">Packaging</span></span></td>
<td><span data-ttu-id="fadc8-590">35</span><span class="sxs-lookup"><span data-stu-id="fadc8-590">35</span></span></td>
<td><span data-ttu-id="fadc8-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="fadc8-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="fadc8-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="fadc8-592">2,852.60</span></span></td>
<td><span data-ttu-id="fadc8-593">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fadc8-594">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="fadc8-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-595">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-595">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-596">Lielums</span><span class="sxs-lookup"><span data-stu-id="fadc8-596">Magnitude</span></span></th>
<th><span data-ttu-id="fadc8-597">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fadc8-597">Allocation factor</span></span></th>
<th><span data-ttu-id="fadc8-598">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-598">Amount</span></span></th>
<th><span data-ttu-id="fadc8-599">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fadc8-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-600">Prod 1</span></span></td>
<td><span data-ttu-id="fadc8-601">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-601">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-602">60</span><span class="sxs-lookup"><span data-stu-id="fadc8-602">60</span></span></td>
<td><span data-ttu-id="fadc8-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="fadc8-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="fadc8-604">535.31</span><span class="sxs-lookup"><span data-stu-id="fadc8-604">535.31</span></span></td>
<td><span data-ttu-id="fadc8-605">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-606">Prod 2</span></span></td>
<td><span data-ttu-id="fadc8-607">2. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-607">Product 2</span></span></td>
<td><span data-ttu-id="fadc8-608">20.</span><span class="sxs-lookup"><span data-stu-id="fadc8-608">20</span></span></td>
<td><span data-ttu-id="fadc8-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="fadc8-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="fadc8-610">178.44</span><span class="sxs-lookup"><span data-stu-id="fadc8-610">178.44</span></span></td>
<td><span data-ttu-id="fadc8-611">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-612">Prod 1</span></span></td>
<td><span data-ttu-id="fadc8-613">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-613">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-614">60</span><span class="sxs-lookup"><span data-stu-id="fadc8-614">60</span></span></td>
<td><span data-ttu-id="fadc8-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="fadc8-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="fadc8-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="fadc8-616">4,487.12</span></span></td>
<td><span data-ttu-id="fadc8-617">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-618">Prod 2</span></span></td>
<td><span data-ttu-id="fadc8-619">2. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-619">Product 2</span></span></td>
<td><span data-ttu-id="fadc8-620">20.</span><span class="sxs-lookup"><span data-stu-id="fadc8-620">20</span></span></td>
<td><span data-ttu-id="fadc8-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="fadc8-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="fadc8-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="fadc8-622">1,495.71</span></span></td>
<td><span data-ttu-id="fadc8-623">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fadc8-624">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="fadc8-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-625">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-625">Cost object</span></span></th>
<th><span data-ttu-id="fadc8-626">Lielums</span><span class="sxs-lookup"><span data-stu-id="fadc8-626">Magnitude</span></span></th>
<th><span data-ttu-id="fadc8-627">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fadc8-627">Allocation factor</span></span></th>
<th><span data-ttu-id="fadc8-628">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-628">Amount</span></span></th>
<th><span data-ttu-id="fadc8-629">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fadc8-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-630">Prod 1</span></span></td>
<td><span data-ttu-id="fadc8-631">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-631">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-632">80</span><span class="sxs-lookup"><span data-stu-id="fadc8-632">80</span></span></td>
<td><span data-ttu-id="fadc8-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="fadc8-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="fadc8-634">241.05</span><span class="sxs-lookup"><span data-stu-id="fadc8-634">241.05</span></span></td>
<td><span data-ttu-id="fadc8-635">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-636">Prod 2</span></span></td>
<td><span data-ttu-id="fadc8-637">2. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-637">Product 2</span></span></td>
<td><span data-ttu-id="fadc8-638">15</span><span class="sxs-lookup"><span data-stu-id="fadc8-638">15</span></span></td>
<td><span data-ttu-id="fadc8-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="fadc8-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="fadc8-640">45.20</span><span class="sxs-lookup"><span data-stu-id="fadc8-640">45.20</span></span></td>
<td><span data-ttu-id="fadc8-641">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-642">Prod 1</span></span></td>
<td><span data-ttu-id="fadc8-643">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-643">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-644">80</span><span class="sxs-lookup"><span data-stu-id="fadc8-644">80</span></span></td>
<td><span data-ttu-id="fadc8-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="fadc8-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="fadc8-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="fadc8-646">2,507.09</span></span></td>
<td><span data-ttu-id="fadc8-647">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-648">Prod 2</span></span></td>
<td><span data-ttu-id="fadc8-649">2. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-649">Product 2</span></span></td>
<td><span data-ttu-id="fadc8-650">15</span><span class="sxs-lookup"><span data-stu-id="fadc8-650">15</span></span></td>
<td><span data-ttu-id="fadc8-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="fadc8-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="fadc8-652">470.08</span><span class="sxs-lookup"><span data-stu-id="fadc8-652">470.08</span></span></td>
<td><span data-ttu-id="fadc8-653">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="fadc8-654">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="fadc8-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fadc8-655">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fadc8-655">Journal</span></span></th>
<th><span data-ttu-id="fadc8-656">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="fadc8-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="fadc8-657">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="fadc8-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="fadc8-658">Versija</span><span class="sxs-lookup"><span data-stu-id="fadc8-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-659">00004</span><span class="sxs-lookup"><span data-stu-id="fadc8-659">00004</span></span></td>
<td><span data-ttu-id="fadc8-660">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="fadc8-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="fadc8-661">Finanšu</span><span class="sxs-lookup"><span data-stu-id="fadc8-661">Fiscal</span></span></td>
<td><span data-ttu-id="fadc8-662">2017</span><span class="sxs-lookup"><span data-stu-id="fadc8-662">2017</span></span></td>
<td><span data-ttu-id="fadc8-663">Periods 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-663">Period 1</span></span></td>
<td><span data-ttu-id="fadc8-664">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="fadc8-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="fadc8-665">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="fadc8-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fadc8-666">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fadc8-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="fadc8-667">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fadc8-668">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fadc8-668">Cost element</span></span></th>
<th><span data-ttu-id="fadc8-669">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fadc8-669">Cost behavior</span></span></th>
<th><span data-ttu-id="fadc8-670">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-671">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-672">CC001</span><span class="sxs-lookup"><span data-stu-id="fadc8-672">CC001</span></span></td>
<td><span data-ttu-id="fadc8-673">HR</span><span class="sxs-lookup"><span data-stu-id="fadc8-673">HR</span></span></td>
<td><span data-ttu-id="fadc8-674">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-674">10001</span></span></td>
<td><span data-ttu-id="fadc8-675">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-675">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-676">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-676">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-677">500,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-678">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-679">CC001</span><span class="sxs-lookup"><span data-stu-id="fadc8-679">CC001</span></span></td>
<td><span data-ttu-id="fadc8-680">HR</span><span class="sxs-lookup"><span data-stu-id="fadc8-680">HR</span></span></td>
<td><span data-ttu-id="fadc8-681">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-681">10001</span></span></td>
<td><span data-ttu-id="fadc8-682">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-682">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-683">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-683">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="fadc8-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-685">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-686">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-686">CC002</span></span></td>
<td><span data-ttu-id="fadc8-687">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-687">Finance</span></span></td>
<td><span data-ttu-id="fadc8-688">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-688">10001</span></span></td>
<td><span data-ttu-id="fadc8-689">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-689">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-690">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-690">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-691">675.00</span><span class="sxs-lookup"><span data-stu-id="fadc8-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-692">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-693">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-693">CC002</span></span></td>
<td><span data-ttu-id="fadc8-694">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-694">Finance</span></span></td>
<td><span data-ttu-id="fadc8-695">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-695">10001</span></span></td>
<td><span data-ttu-id="fadc8-696">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-696">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-697">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-697">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="fadc8-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-699">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-700">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-700">CC003</span></span></td>
<td><span data-ttu-id="fadc8-701">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-701">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-702">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-702">10001</span></span></td>
<td><span data-ttu-id="fadc8-703">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-703">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-704">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-704">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-705">713.75</span><span class="sxs-lookup"><span data-stu-id="fadc8-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-706">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-707">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-707">CC003</span></span></td>
<td><span data-ttu-id="fadc8-708">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-708">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-709">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-709">10001</span></span></td>
<td><span data-ttu-id="fadc8-710">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-710">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-711">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-711">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="fadc8-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-713">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-714">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-714">CC003</span></span></td>
<td><span data-ttu-id="fadc8-715">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fadc8-715">Packaging</span></span></td>
<td><span data-ttu-id="fadc8-716">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-716">10001</span></span></td>
<td><span data-ttu-id="fadc8-717">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-717">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-718">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-718">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-719">286.25</span><span class="sxs-lookup"><span data-stu-id="fadc8-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-720">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-721">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-721">CC003</span></span></td>
<td><span data-ttu-id="fadc8-722">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fadc8-722">Packaging</span></span></td>
<td><span data-ttu-id="fadc8-723">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-723">10001</span></span></td>
<td><span data-ttu-id="fadc8-724">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-724">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-725">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-725">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="fadc8-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-727">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-728">Prod 1</span></span></td>
<td><span data-ttu-id="fadc8-729">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-729">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-730">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-730">10001</span></span></td>
<td><span data-ttu-id="fadc8-731">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-731">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-732">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-732">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-733">776.36</span><span class="sxs-lookup"><span data-stu-id="fadc8-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-734">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-735">Prod 1</span></span></td>
<td><span data-ttu-id="fadc8-736">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-736">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-737">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-737">10001</span></span></td>
<td><span data-ttu-id="fadc8-738">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-738">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-739">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-739">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="fadc8-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-741">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-742">Prod 2</span></span></td>
<td><span data-ttu-id="fadc8-743">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-743">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-744">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-744">10001</span></span></td>
<td><span data-ttu-id="fadc8-745">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-745">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-746">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-746">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-747">223.64</span><span class="sxs-lookup"><span data-stu-id="fadc8-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-748">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="fadc8-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-749">Prod 2</span></span></td>
<td><span data-ttu-id="fadc8-750">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-750">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-751">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-751">10001</span></span></td>
<td><span data-ttu-id="fadc8-752">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-752">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-753">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-753">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="fadc8-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="fadc8-755">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="fadc8-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fadc8-756">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fadc8-757">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fadc8-757">Cost element</span></span></th>
<th><span data-ttu-id="fadc8-758">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fadc8-758">Cost behavior</span></span></th>
<th><span data-ttu-id="fadc8-759">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-759">Amount</span></span></th>
<th><span data-ttu-id="fadc8-760">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fadc8-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fadc8-761">CC001</span><span class="sxs-lookup"><span data-stu-id="fadc8-761">CC001</span></span></td>
<td><span data-ttu-id="fadc8-762">HR</span><span class="sxs-lookup"><span data-stu-id="fadc8-762">HR</span></span></td>
<td><span data-ttu-id="fadc8-763">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-763">10001</span></span></td>
<td><span data-ttu-id="fadc8-764">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-764">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-765">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-765">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-766">-500.00</span></span></td>
<td><span data-ttu-id="fadc8-767">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-768">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-768">CC002</span></span></td>
<td><span data-ttu-id="fadc8-769">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-769">Finance</span></span></td>
<td><span data-ttu-id="fadc8-770">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-770">10001</span></span></td>
<td><span data-ttu-id="fadc8-771">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-771">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-772">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-772">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-773">175.00</span><span class="sxs-lookup"><span data-stu-id="fadc8-773">175.00</span></span></td>
<td><span data-ttu-id="fadc8-774">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-775">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-775">CC003</span></span></td>
<td><span data-ttu-id="fadc8-776">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-776">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-777">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-777">10001</span></span></td>
<td><span data-ttu-id="fadc8-778">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-778">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-779">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-779">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-780">275.00</span><span class="sxs-lookup"><span data-stu-id="fadc8-780">275.00</span></span></td>
<td><span data-ttu-id="fadc8-781">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-782">CC004</span><span class="sxs-lookup"><span data-stu-id="fadc8-782">CC004</span></span></td>
<td><span data-ttu-id="fadc8-783">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fadc8-783">Packaging</span></span></td>
<td><span data-ttu-id="fadc8-784">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-784">10001</span></span></td>
<td><span data-ttu-id="fadc8-785">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-785">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-786">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-786">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-787">50,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-787">50,00</span></span></td>
<td><span data-ttu-id="fadc8-788">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-789">CC001</span><span class="sxs-lookup"><span data-stu-id="fadc8-789">CC001</span></span></td>
<td><span data-ttu-id="fadc8-790">HR</span><span class="sxs-lookup"><span data-stu-id="fadc8-790">HR</span></span></td>
<td><span data-ttu-id="fadc8-791">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-791">10001</span></span></td>
<td><span data-ttu-id="fadc8-792">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-792">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-793">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-793">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="fadc8-794">-1,245.71</span></span></td>
<td><span data-ttu-id="fadc8-795">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-796">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-796">CC002</span></span></td>
<td><span data-ttu-id="fadc8-797">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-797">Finance</span></span></td>
<td><span data-ttu-id="fadc8-798">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-798">10001</span></span></td>
<td><span data-ttu-id="fadc8-799">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-799">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-800">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-800">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-801">436.00</span><span class="sxs-lookup"><span data-stu-id="fadc8-801">436.00</span></span></td>
<td><span data-ttu-id="fadc8-802">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-803">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-803">CC003</span></span></td>
<td><span data-ttu-id="fadc8-804">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-804">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-805">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-805">10001</span></span></td>
<td><span data-ttu-id="fadc8-806">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-806">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-807">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-807">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-808">685.14</span><span class="sxs-lookup"><span data-stu-id="fadc8-808">685.14</span></span></td>
<td><span data-ttu-id="fadc8-809">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-810">CC004</span><span class="sxs-lookup"><span data-stu-id="fadc8-810">CC004</span></span></td>
<td><span data-ttu-id="fadc8-811">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fadc8-811">Packaging</span></span></td>
<td><span data-ttu-id="fadc8-812">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-812">10001</span></span></td>
<td><span data-ttu-id="fadc8-813">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-813">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-814">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-814">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-815">124.57</span><span class="sxs-lookup"><span data-stu-id="fadc8-815">124.57</span></span></td>
<td><span data-ttu-id="fadc8-816">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-817">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-817">CC002</span></span></td>
<td><span data-ttu-id="fadc8-818">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-818">Finance</span></span></td>
<td><span data-ttu-id="fadc8-819">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-819">10001</span></span></td>
<td><span data-ttu-id="fadc8-820">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-820">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-821">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-821">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-822">-675.00</span></span></td>
<td><span data-ttu-id="fadc8-823">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-824">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-824">CC003</span></span></td>
<td><span data-ttu-id="fadc8-825">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-825">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-826">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-826">10001</span></span></td>
<td><span data-ttu-id="fadc8-827">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-827">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-828">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-828">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-829">438.75</span><span class="sxs-lookup"><span data-stu-id="fadc8-829">438.75</span></span></td>
<td><span data-ttu-id="fadc8-830">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-831">CC004</span><span class="sxs-lookup"><span data-stu-id="fadc8-831">CC004</span></span></td>
<td><span data-ttu-id="fadc8-832">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fadc8-832">Packaging</span></span></td>
<td><span data-ttu-id="fadc8-833">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-833">10001</span></span></td>
<td><span data-ttu-id="fadc8-834">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-834">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-835">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-835">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-836">236.25</span><span class="sxs-lookup"><span data-stu-id="fadc8-836">236.25</span></span></td>
<td><span data-ttu-id="fadc8-837">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-838">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-838">CC002</span></span></td>
<td><span data-ttu-id="fadc8-839">Finanses</span><span class="sxs-lookup"><span data-stu-id="fadc8-839">Finance</span></span></td>
<td><span data-ttu-id="fadc8-840">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-840">10001</span></span></td>
<td><span data-ttu-id="fadc8-841">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-841">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-842">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-842">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="fadc8-843">-8,150.29</span></span></td>
<td><span data-ttu-id="fadc8-844">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-845">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-845">CC003</span></span></td>
<td><span data-ttu-id="fadc8-846">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-846">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-847">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-847">10001</span></span></td>
<td><span data-ttu-id="fadc8-848">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-848">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-849">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-849">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="fadc8-850">5,297.69</span></span></td>
<td><span data-ttu-id="fadc8-851">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-852">CC004</span><span class="sxs-lookup"><span data-stu-id="fadc8-852">CC004</span></span></td>
<td><span data-ttu-id="fadc8-853">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fadc8-853">Packaging</span></span></td>
<td><span data-ttu-id="fadc8-854">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-854">10001</span></span></td>
<td><span data-ttu-id="fadc8-855">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-855">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-856">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-856">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="fadc8-857">2,852.60</span></span></td>
<td><span data-ttu-id="fadc8-858">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-859">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-859">CC003</span></span></td>
<td><span data-ttu-id="fadc8-860">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-860">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-861">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-861">10001</span></span></td>
<td><span data-ttu-id="fadc8-862">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-862">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-863">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-863">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="fadc8-864">-713.75</span></span></td>
<td><span data-ttu-id="fadc8-865">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-866">Prod 1</span></span></td>
<td><span data-ttu-id="fadc8-867">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-867">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-868">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-868">10001</span></span></td>
<td><span data-ttu-id="fadc8-869">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-869">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-870">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-870">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-871">535.31</span><span class="sxs-lookup"><span data-stu-id="fadc8-871">535.31</span></span></td>
<td><span data-ttu-id="fadc8-872">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-873">Prod 2</span></span></td>
<td><span data-ttu-id="fadc8-874">2. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-874">Product 2</span></span></td>
<td><span data-ttu-id="fadc8-875">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-875">10001</span></span></td>
<td><span data-ttu-id="fadc8-876">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-876">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-877">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-877">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-878">178.44</span><span class="sxs-lookup"><span data-stu-id="fadc8-878">178.44</span></span></td>
<td><span data-ttu-id="fadc8-879">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-880">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-880">CC003</span></span></td>
<td><span data-ttu-id="fadc8-881">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-881">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-882">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-882">10001</span></span></td>
<td><span data-ttu-id="fadc8-883">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-883">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-884">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-884">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="fadc8-885">-5,982.83</span></span></td>
<td><span data-ttu-id="fadc8-886">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-887">Prod 1</span></span></td>
<td><span data-ttu-id="fadc8-888">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-888">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-889">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-889">10001</span></span></td>
<td><span data-ttu-id="fadc8-890">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-890">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-891">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-891">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="fadc8-892">4,487.12</span></span></td>
<td><span data-ttu-id="fadc8-893">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-894">Prod 2</span></span></td>
<td><span data-ttu-id="fadc8-895">2. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-895">Product 2</span></span></td>
<td><span data-ttu-id="fadc8-896">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-896">10001</span></span></td>
<td><span data-ttu-id="fadc8-897">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-897">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-898">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-898">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="fadc8-899">1,495.71</span></span></td>
<td><span data-ttu-id="fadc8-900">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-901">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-901">CC003</span></span></td>
<td><span data-ttu-id="fadc8-902">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-902">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-903">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-903">10001</span></span></td>
<td><span data-ttu-id="fadc8-904">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-904">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-905">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-905">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="fadc8-906">-286.25</span></span></td>
<td><span data-ttu-id="fadc8-907">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-908">Prod 1</span></span></td>
<td><span data-ttu-id="fadc8-909">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-909">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-910">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-910">10001</span></span></td>
<td><span data-ttu-id="fadc8-911">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-911">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-912">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-912">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-913">241.05</span><span class="sxs-lookup"><span data-stu-id="fadc8-913">241.05</span></span></td>
<td><span data-ttu-id="fadc8-914">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-915">Prod 2</span></span></td>
<td><span data-ttu-id="fadc8-916">2. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-916">Product 2</span></span></td>
<td><span data-ttu-id="fadc8-917">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-917">10001</span></span></td>
<td><span data-ttu-id="fadc8-918">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-918">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-919">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-919">Fixed cost</span></span></td>
<td><span data-ttu-id="fadc8-920">45.20</span><span class="sxs-lookup"><span data-stu-id="fadc8-920">45.20</span></span></td>
<td><span data-ttu-id="fadc8-921">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-922">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-922">CC003</span></span></td>
<td><span data-ttu-id="fadc8-923">Montāža</span><span class="sxs-lookup"><span data-stu-id="fadc8-923">Assembly</span></span></td>
<td><span data-ttu-id="fadc8-924">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-924">10001</span></span></td>
<td><span data-ttu-id="fadc8-925">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-925">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-926">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-926">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="fadc8-927">-2,977.17</span></span></td>
<td><span data-ttu-id="fadc8-928">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-929">Prod 1</span></span></td>
<td><span data-ttu-id="fadc8-930">1. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-930">Product 1</span></span></td>
<td><span data-ttu-id="fadc8-931">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-931">10001</span></span></td>
<td><span data-ttu-id="fadc8-932">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-932">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-933">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-933">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="fadc8-934">2,507.09</span></span></td>
<td><span data-ttu-id="fadc8-935">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fadc8-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-936">Prod 2</span></span></td>
<td><span data-ttu-id="fadc8-937">2. prece</span><span class="sxs-lookup"><span data-stu-id="fadc8-937">Product 2</span></span></td>
<td><span data-ttu-id="fadc8-938">10001</span><span class="sxs-lookup"><span data-stu-id="fadc8-938">10001</span></span></td>
<td><span data-ttu-id="fadc8-939">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-939">Electricity</span></span></td>
<td><span data-ttu-id="fadc8-940">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-940">Variable cost</span></span></td>
<td><span data-ttu-id="fadc8-941">470.08</span><span class="sxs-lookup"><span data-stu-id="fadc8-941">470.08</span></span></td>
<td><span data-ttu-id="fadc8-942">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fadc8-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="fadc8-943">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="fadc8-943">Conclusion</span></span>
<span data-ttu-id="fadc8-944">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="fadc8-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="fadc8-945">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="fadc8-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="fadc8-946">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="fadc8-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="fadc8-947">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="fadc8-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="fadc8-948">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fadc8-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="fadc8-949">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fadc8-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="fadc8-950">Summa</span><span class="sxs-lookup"><span data-stu-id="fadc8-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="fadc8-951">CC099</span><span class="sxs-lookup"><span data-stu-id="fadc8-951">CC099</span></span></th>
<th><span data-ttu-id="fadc8-952">CC001</span><span class="sxs-lookup"><span data-stu-id="fadc8-952">CC001</span></span></th>
<th><span data-ttu-id="fadc8-953">CC002</span><span class="sxs-lookup"><span data-stu-id="fadc8-953">CC002</span></span></th>
<th><span data-ttu-id="fadc8-954">CC003</span><span class="sxs-lookup"><span data-stu-id="fadc8-954">CC003</span></span></th>
<th><span data-ttu-id="fadc8-955">CC004</span><span class="sxs-lookup"><span data-stu-id="fadc8-955">CC004</span></span></th>
<th><span data-ttu-id="fadc8-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-956">Proj 1</span></span></th>
<th><span data-ttu-id="fadc8-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-957">Proj 2</span></span></th>
<th><span data-ttu-id="fadc8-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fadc8-958">Prod 1</span></span></th>
<th><span data-ttu-id="fadc8-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fadc8-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="fadc8-960">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="fadc8-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="fadc8-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="fadc8-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="fadc8-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="fadc8-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="fadc8-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="fadc8-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="fadc8-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="fadc8-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="fadc8-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="fadc8-970">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="fadc8-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-971">0,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="fadc8-972">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-973">0,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-974">0,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-975">0,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-976">0,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-977">0,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-978">776.36</span><span class="sxs-lookup"><span data-stu-id="fadc8-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-979">223.64</span><span class="sxs-lookup"><span data-stu-id="fadc8-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="fadc8-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="fadc8-981">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fadc8-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-982">000</span><span class="sxs-lookup"><span data-stu-id="fadc8-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-983">0,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-984">0,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-985">0,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-986">0,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-987">30,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-988">10,00</span><span class="sxs-lookup"><span data-stu-id="fadc8-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="fadc8-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="fadc8-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fadc8-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="fadc8-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="fadc8-992">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="fadc8-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="fadc8-993">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="fadc8-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="fadc8-994">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="fadc8-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="fadc8-995">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="fadc8-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="fadc8-996">Plašāku informāciju skatiet [Izmaksu apkopojuma politika un pieskaitāmo izmaksu aprēķins](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="fadc8-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]