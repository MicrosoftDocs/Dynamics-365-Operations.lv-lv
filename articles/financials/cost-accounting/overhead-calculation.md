---
title: "Pieskaitāmo izmaksu aprēķins"
description: "Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 549e9b4b073a4e93dd3a1dd52dd6f43e7420a31b
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="96261-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="96261-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="96261-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="96261-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="96261-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="96261-105">Term definition</span></span>
---------------

<span data-ttu-id="96261-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="96261-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="96261-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="96261-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="96261-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="96261-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="96261-109">Īre</span><span class="sxs-lookup"><span data-stu-id="96261-109">Rent</span></span>
-   <span data-ttu-id="96261-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-110">Electricity</span></span>
-   <span data-ttu-id="96261-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="96261-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="96261-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="96261-112">Overhead calculation overview</span></span>
<span data-ttu-id="96261-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="96261-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="96261-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="96261-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="96261-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="96261-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="96261-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="96261-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="96261-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="96261-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="96261-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="96261-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="96261-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="96261-119">Version type</span></span>
-   <span data-ttu-id="96261-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="96261-120">Date and time</span></span>
-   <span data-ttu-id="96261-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="96261-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="96261-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="96261-122">Fiscal year</span></span>
-   <span data-ttu-id="96261-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="96261-123">Fiscal period</span></span>

<span data-ttu-id="96261-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="96261-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="96261-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="96261-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="96261-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="96261-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="96261-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="96261-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="96261-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="96261-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="96261-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="96261-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="96261-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="96261-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="96261-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="96261-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="96261-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="96261-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="96261-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="96261-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="96261-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="96261-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="96261-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="96261-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="96261-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="96261-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="96261-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="96261-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="96261-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="96261-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="96261-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="96261-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="96261-140">Main account</span></span></th>
<th><span data-ttu-id="96261-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="96261-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="96261-143">CC099</span><span class="sxs-lookup"><span data-stu-id="96261-143">CC099</span></span></td>
<td><span data-ttu-id="96261-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="96261-144">Default cost center</span></span></td>
<td><span data-ttu-id="96261-145">10001</span><span class="sxs-lookup"><span data-stu-id="96261-145">10001</span></span></td>
<td><span data-ttu-id="96261-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-146">Electricity</span></span></td>
<td><span data-ttu-id="96261-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="96261-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="96261-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="96261-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="96261-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="96261-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="96261-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="96261-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="96261-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="96261-151">Define the cost behavior rule</span></span>

<span data-ttu-id="96261-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="96261-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="96261-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="96261-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="96261-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="96261-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="96261-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="96261-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="96261-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="96261-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="96261-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="96261-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="96261-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="96261-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="96261-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="96261-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="96261-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="96261-160">Journal</span></span></th>
<th><span data-ttu-id="96261-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="96261-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="96261-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="96261-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="96261-163">Versija</span><span class="sxs-lookup"><span data-stu-id="96261-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-164">00001</span><span class="sxs-lookup"><span data-stu-id="96261-164">00001</span></span></td>
<td><span data-ttu-id="96261-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="96261-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="96261-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="96261-166">Fiscal</span></span></td>
<td><span data-ttu-id="96261-167">2017</span><span class="sxs-lookup"><span data-stu-id="96261-167">2017</span></span></td>
<td><span data-ttu-id="96261-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="96261-168">Period 1</span></span></td>
<td><span data-ttu-id="96261-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="96261-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="96261-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="96261-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="96261-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="96261-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="96261-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="96261-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="96261-173">Cost element</span></span></th>
<th><span data-ttu-id="96261-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="96261-174">Cost behavior</span></span></th>
<th><span data-ttu-id="96261-175">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="96261-177">CC099</span><span class="sxs-lookup"><span data-stu-id="96261-177">CC099</span></span></td>
<td><span data-ttu-id="96261-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="96261-178">Default cost center</span></span></td>
<td><span data-ttu-id="96261-179">10001</span><span class="sxs-lookup"><span data-stu-id="96261-179">10001</span></span></td>
<td><span data-ttu-id="96261-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-180">Electricity</span></span></td>
<td><span data-ttu-id="96261-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="96261-181">Unclassified</span></span></td>
<td><span data-ttu-id="96261-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="96261-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="96261-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="96261-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="96261-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="96261-185">Cost element</span></span></th>
<th><span data-ttu-id="96261-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="96261-186">Cost behavior</span></span></th>
<th><span data-ttu-id="96261-187">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-187">Amount</span></span></th>
<th><span data-ttu-id="96261-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="96261-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-189">CC099</span><span class="sxs-lookup"><span data-stu-id="96261-189">CC099</span></span></td>
<td><span data-ttu-id="96261-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="96261-190">Default cost center</span></span></td>
<td><span data-ttu-id="96261-191">10001</span><span class="sxs-lookup"><span data-stu-id="96261-191">10001</span></span></td>
<td><span data-ttu-id="96261-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-192">Electricity</span></span></td>
<td><span data-ttu-id="96261-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="96261-193">Unclassified</span></span></td>
<td><span data-ttu-id="96261-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="96261-194">10,000.00</span></span></td>
<td><span data-ttu-id="96261-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-196">CC099</span><span class="sxs-lookup"><span data-stu-id="96261-196">CC099</span></span></td>
<td><span data-ttu-id="96261-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="96261-197">Default cost center</span></span></td>
<td><span data-ttu-id="96261-198">10001</span><span class="sxs-lookup"><span data-stu-id="96261-198">10001</span></span></td>
<td><span data-ttu-id="96261-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-199">Electricity</span></span></td>
<td><span data-ttu-id="96261-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="96261-200">Unclassified</span></span></td>
<td><span data-ttu-id="96261-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="96261-201">-10,000.00</span></span></td>
<td><span data-ttu-id="96261-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-203">CC099</span><span class="sxs-lookup"><span data-stu-id="96261-203">CC099</span></span></td>
<td><span data-ttu-id="96261-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="96261-204">Default cost center</span></span></td>
<td><span data-ttu-id="96261-205">10001</span><span class="sxs-lookup"><span data-stu-id="96261-205">10001</span></span></td>
<td><span data-ttu-id="96261-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-206">Electricity</span></span></td>
<td><span data-ttu-id="96261-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-207">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="96261-208">1,000.00</span></span></td>
<td><span data-ttu-id="96261-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-210">CC099</span><span class="sxs-lookup"><span data-stu-id="96261-210">CC099</span></span></td>
<td><span data-ttu-id="96261-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="96261-211">Default cost center</span></span></td>
<td><span data-ttu-id="96261-212">10001</span><span class="sxs-lookup"><span data-stu-id="96261-212">10001</span></span></td>
<td><span data-ttu-id="96261-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-213">Electricity</span></span></td>
<td><span data-ttu-id="96261-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-214">Variable cost</span></span></td>
<td><span data-ttu-id="96261-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="96261-215">9,000.00</span></span></td>
<td><span data-ttu-id="96261-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-217">Detalizētu informāciju par izmaksu uzvedību skatiet sadaļā Izmaksu uzvedības politika.</span><span class="sxs-lookup"><span data-stu-id="96261-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="96261-218">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)</span><span class="sxs-lookup"><span data-stu-id="96261-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="96261-219">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="96261-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="96261-220">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="96261-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="96261-221">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="96261-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="96261-222">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="96261-222">Define the cost distribution rule</span></span>

<span data-ttu-id="96261-223">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="96261-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="96261-224">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="96261-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="96261-225">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="96261-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="96261-226">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="96261-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="96261-227">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="96261-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="96261-228">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="96261-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-229">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-229">Cost object</span></span></th>
<th><span data-ttu-id="96261-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="96261-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-231">CC001</span><span class="sxs-lookup"><span data-stu-id="96261-231">CC001</span></span></td>
<td><span data-ttu-id="96261-232">HR</span><span class="sxs-lookup"><span data-stu-id="96261-232">HR</span></span></td>
<td><span data-ttu-id="96261-233">1000</span><span class="sxs-lookup"><span data-stu-id="96261-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-234">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-234">CC002</span></span></td>
<td><span data-ttu-id="96261-235">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-235">Finance</span></span></td>
<td><span data-ttu-id="96261-236">6,000</span><span class="sxs-lookup"><span data-stu-id="96261-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-237">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-237">CC003</span></span></td>
<td><span data-ttu-id="96261-238">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-238">Assembly</span></span></td>
<td><span data-ttu-id="96261-239">0</span><span class="sxs-lookup"><span data-stu-id="96261-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-240">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="96261-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-241">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-241">Cost object</span></span></th>
<th><span data-ttu-id="96261-242">Lielums</span><span class="sxs-lookup"><span data-stu-id="96261-242">Magnitude</span></span></th>
<th><span data-ttu-id="96261-243">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="96261-243">Allocation factor</span></span></th>
<th><span data-ttu-id="96261-244">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-245">CC001</span><span class="sxs-lookup"><span data-stu-id="96261-245">CC001</span></span></td>
<td><span data-ttu-id="96261-246">HR</span><span class="sxs-lookup"><span data-stu-id="96261-246">HR</span></span></td>
<td><span data-ttu-id="96261-247">1000</span><span class="sxs-lookup"><span data-stu-id="96261-247">1,000</span></span></td>
<td><span data-ttu-id="96261-248">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="96261-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="96261-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="96261-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-250">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-250">CC002</span></span></td>
<td><span data-ttu-id="96261-251">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-251">Finance</span></span></td>
<td><span data-ttu-id="96261-252">6,000</span><span class="sxs-lookup"><span data-stu-id="96261-252">6,000</span></span></td>
<td><span data-ttu-id="96261-253">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="96261-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="96261-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="96261-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-255">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-255">CC003</span></span></td>
<td><span data-ttu-id="96261-256">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-256">Assembly</span></span></td>
<td><span data-ttu-id="96261-257">0</span><span class="sxs-lookup"><span data-stu-id="96261-257">0</span></span></td>
<td><span data-ttu-id="96261-258">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="96261-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="96261-259">0,00</span><span class="sxs-lookup"><span data-stu-id="96261-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-260">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="96261-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="96261-261">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="96261-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-262">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-262">Cost object</span></span></th>
<th><span data-ttu-id="96261-263">Formula</span><span class="sxs-lookup"><span data-stu-id="96261-263">Formula</span></span></th>
<th><span data-ttu-id="96261-264">Lielums</span><span class="sxs-lookup"><span data-stu-id="96261-264">Magnitude</span></span></th>
<th><span data-ttu-id="96261-265">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="96261-265">Allocation factor</span></span></th>
<th><span data-ttu-id="96261-266">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-267">CC001</span><span class="sxs-lookup"><span data-stu-id="96261-267">CC001</span></span></td>
<td><span data-ttu-id="96261-268">HR</span><span class="sxs-lookup"><span data-stu-id="96261-268">HR</span></span></td>
<td><span data-ttu-id="96261-269">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="96261-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="96261-270">1.</span><span class="sxs-lookup"><span data-stu-id="96261-270">1</span></span></td>
<td><span data-ttu-id="96261-271">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="96261-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="96261-272">500,00</span><span class="sxs-lookup"><span data-stu-id="96261-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-273">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-273">CC002</span></span></td>
<td><span data-ttu-id="96261-274">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-274">Finance</span></span></td>
<td><span data-ttu-id="96261-275">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="96261-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="96261-276">1.</span><span class="sxs-lookup"><span data-stu-id="96261-276">1</span></span></td>
<td><span data-ttu-id="96261-277">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="96261-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="96261-278">500,00</span><span class="sxs-lookup"><span data-stu-id="96261-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-279">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-279">CC003</span></span></td>
<td><span data-ttu-id="96261-280">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-280">Assembly</span></span></td>
<td><span data-ttu-id="96261-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="96261-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="96261-282">0</span><span class="sxs-lookup"><span data-stu-id="96261-282">0</span></span></td>
<td><span data-ttu-id="96261-283">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="96261-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="96261-284">0,00</span><span class="sxs-lookup"><span data-stu-id="96261-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="96261-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="96261-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="96261-286">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="96261-286">Journal</span></span></th>
<th><span data-ttu-id="96261-287">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="96261-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="96261-288">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="96261-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="96261-289">Versija</span><span class="sxs-lookup"><span data-stu-id="96261-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-290">00002</span><span class="sxs-lookup"><span data-stu-id="96261-290">00002</span></span></td>
<td><span data-ttu-id="96261-291">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="96261-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="96261-292">Finanšu</span><span class="sxs-lookup"><span data-stu-id="96261-292">Fiscal</span></span></td>
<td><span data-ttu-id="96261-293">2017</span><span class="sxs-lookup"><span data-stu-id="96261-293">2017</span></span></td>
<td><span data-ttu-id="96261-294">Periods 1</span><span class="sxs-lookup"><span data-stu-id="96261-294">Period 1</span></span></td>
<td><span data-ttu-id="96261-295">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="96261-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="96261-296">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="96261-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="96261-297">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="96261-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="96261-298">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="96261-299">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="96261-299">Cost element</span></span></th>
<th><span data-ttu-id="96261-300">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="96261-300">Cost behavior</span></span></th>
<th><span data-ttu-id="96261-301">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-302">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-303">CC099</span><span class="sxs-lookup"><span data-stu-id="96261-303">CC099</span></span></td>
<td><span data-ttu-id="96261-304">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="96261-304">Default cost center</span></span></td>
<td><span data-ttu-id="96261-305">10001</span><span class="sxs-lookup"><span data-stu-id="96261-305">10001</span></span></td>
<td><span data-ttu-id="96261-306">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-306">Electricity</span></span></td>
<td><span data-ttu-id="96261-307">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-307">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-308">1000,00</span><span class="sxs-lookup"><span data-stu-id="96261-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-309">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-310">CC099</span><span class="sxs-lookup"><span data-stu-id="96261-310">CC099</span></span></td>
<td><span data-ttu-id="96261-311">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="96261-311">Default cost center</span></span></td>
<td><span data-ttu-id="96261-312">10001</span><span class="sxs-lookup"><span data-stu-id="96261-312">10001</span></span></td>
<td><span data-ttu-id="96261-313">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-313">Electricity</span></span></td>
<td><span data-ttu-id="96261-314">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-314">Variable cost</span></span></td>
<td><span data-ttu-id="96261-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="96261-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="96261-316">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="96261-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-317">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="96261-318">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="96261-318">Cost element</span></span></th>
<th><span data-ttu-id="96261-319">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="96261-319">Cost behavior</span></span></th>
<th><span data-ttu-id="96261-320">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-320">Amount</span></span></th>
<th><span data-ttu-id="96261-321">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="96261-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-322">CC099</span><span class="sxs-lookup"><span data-stu-id="96261-322">CC099</span></span></td>
<td><span data-ttu-id="96261-323">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="96261-323">Default cost center</span></span></td>
<td><span data-ttu-id="96261-324">10001</span><span class="sxs-lookup"><span data-stu-id="96261-324">10001</span></span></td>
<td><span data-ttu-id="96261-325">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-325">Electricity</span></span></td>
<td><span data-ttu-id="96261-326">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-326">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-327">-1000,00</span><span class="sxs-lookup"><span data-stu-id="96261-327">-1,000.00</span></span></td>
<td><span data-ttu-id="96261-328">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-329">CC001</span><span class="sxs-lookup"><span data-stu-id="96261-329">CC001</span></span></td>
<td><span data-ttu-id="96261-330">HR</span><span class="sxs-lookup"><span data-stu-id="96261-330">HR</span></span></td>
<td><span data-ttu-id="96261-331">10001</span><span class="sxs-lookup"><span data-stu-id="96261-331">10001</span></span></td>
<td><span data-ttu-id="96261-332">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-332">Electricity</span></span></td>
<td><span data-ttu-id="96261-333">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-333">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-334">500,00</span><span class="sxs-lookup"><span data-stu-id="96261-334">500.00</span></span></td>
<td><span data-ttu-id="96261-335">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-336">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-336">CC002</span></span></td>
<td><span data-ttu-id="96261-337">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-337">Finance</span></span></td>
<td><span data-ttu-id="96261-338">10001</span><span class="sxs-lookup"><span data-stu-id="96261-338">10001</span></span></td>
<td><span data-ttu-id="96261-339">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-339">Electricity</span></span></td>
<td><span data-ttu-id="96261-340">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-340">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-341">500,00</span><span class="sxs-lookup"><span data-stu-id="96261-341">500.00</span></span></td>
<td><span data-ttu-id="96261-342">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-343">CC099</span><span class="sxs-lookup"><span data-stu-id="96261-343">CC099</span></span></td>
<td><span data-ttu-id="96261-344">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="96261-344">Default cost center</span></span></td>
<td><span data-ttu-id="96261-345">10001</span><span class="sxs-lookup"><span data-stu-id="96261-345">10001</span></span></td>
<td><span data-ttu-id="96261-346">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-346">Electricity</span></span></td>
<td><span data-ttu-id="96261-347">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-347">Variable cost</span></span></td>
<td><span data-ttu-id="96261-348">-9000,00</span><span class="sxs-lookup"><span data-stu-id="96261-348">-9,000.00</span></span></td>
<td><span data-ttu-id="96261-349">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-350">CC001</span><span class="sxs-lookup"><span data-stu-id="96261-350">CC001</span></span></td>
<td><span data-ttu-id="96261-351">HR</span><span class="sxs-lookup"><span data-stu-id="96261-351">HR</span></span></td>
<td><span data-ttu-id="96261-352">10001</span><span class="sxs-lookup"><span data-stu-id="96261-352">10001</span></span></td>
<td><span data-ttu-id="96261-353">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-353">Electricity</span></span></td>
<td><span data-ttu-id="96261-354">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-354">Variable cost</span></span></td>
<td><span data-ttu-id="96261-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="96261-355">1,285.71</span></span></td>
<td><span data-ttu-id="96261-356">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-357">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-357">CC002</span></span></td>
<td><span data-ttu-id="96261-358">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-358">Finance</span></span></td>
<td><span data-ttu-id="96261-359">10001</span><span class="sxs-lookup"><span data-stu-id="96261-359">10001</span></span></td>
<td><span data-ttu-id="96261-360">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-360">Electricity</span></span></td>
<td><span data-ttu-id="96261-361">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-361">Variable cost</span></span></td>
<td><span data-ttu-id="96261-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="96261-362">7,714.29</span></span></td>
<td><span data-ttu-id="96261-363">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-364">Detalizētu informāciju par izmaksu sadali un sadalījuma pamatiem skatiet sadaļā Izmaksu sadales politika un Sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="96261-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="96261-365">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)</span><span class="sxs-lookup"><span data-stu-id="96261-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="96261-366">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="96261-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="96261-367">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="96261-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="96261-368">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="96261-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="96261-369">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="96261-369">Define the overhead rate</span></span>

<span data-ttu-id="96261-370">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="96261-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="96261-371">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="96261-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-372">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-372">Cost object</span></span></th>
<th><span data-ttu-id="96261-373">Stundas</span><span class="sxs-lookup"><span data-stu-id="96261-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="96261-374">Proj 1</span></span></td>
<td><span data-ttu-id="96261-375">1. projekts</span><span class="sxs-lookup"><span data-stu-id="96261-375">Project 1</span></span></td>
<td><span data-ttu-id="96261-376">3.</span><span class="sxs-lookup"><span data-stu-id="96261-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="96261-377">Proj 2</span></span></td>
<td><span data-ttu-id="96261-378">2. projekts</span><span class="sxs-lookup"><span data-stu-id="96261-378">Project 2</span></span></td>
<td><span data-ttu-id="96261-379">1.</span><span class="sxs-lookup"><span data-stu-id="96261-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-380">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="96261-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-381">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-381">Cost object</span></span></th>
<th><span data-ttu-id="96261-382">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="96261-382">Cost element</span></span></th>
<th><span data-ttu-id="96261-383">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="96261-383">Cost behavior</span></span></th>
<th><span data-ttu-id="96261-384">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="96261-384">Units</span></span></th>
<th><span data-ttu-id="96261-385">Likme</span><span class="sxs-lookup"><span data-stu-id="96261-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-386">CC001</span><span class="sxs-lookup"><span data-stu-id="96261-386">CC001</span></span></td>
<td><span data-ttu-id="96261-387">HR</span><span class="sxs-lookup"><span data-stu-id="96261-387">HR</span></span></td>
<td><span data-ttu-id="96261-388">10001</span><span class="sxs-lookup"><span data-stu-id="96261-388">10001</span></span></td>
<td><span data-ttu-id="96261-389">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-389">Variable cost</span></span></td>
<td><span data-ttu-id="96261-390">1</span><span class="sxs-lookup"><span data-stu-id="96261-390">1</span></span></td>
<td><span data-ttu-id="96261-391">10</span><span class="sxs-lookup"><span data-stu-id="96261-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-392">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="96261-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-393">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-393">Cost object</span></span></th>
<th><span data-ttu-id="96261-394">Lielums</span><span class="sxs-lookup"><span data-stu-id="96261-394">Magnitude</span></span></th>
<th><span data-ttu-id="96261-395">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="96261-395">Cost element</span></span></th>
<th><span data-ttu-id="96261-396">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="96261-396">Allocation factor</span></span></th>
<th><span data-ttu-id="96261-397">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="96261-398">Proj 1</span></span></td>
<td><span data-ttu-id="96261-399">1. projekts</span><span class="sxs-lookup"><span data-stu-id="96261-399">Project 1</span></span></td>
<td><span data-ttu-id="96261-400">3.</span><span class="sxs-lookup"><span data-stu-id="96261-400">3</span></span></td>
<td><span data-ttu-id="96261-401">10001</span><span class="sxs-lookup"><span data-stu-id="96261-401">10001</span></span></td>
<td><span data-ttu-id="96261-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="96261-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="96261-403">30,00</span><span class="sxs-lookup"><span data-stu-id="96261-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="96261-404">Proj 2</span></span></td>
<td><span data-ttu-id="96261-405">2. projekts</span><span class="sxs-lookup"><span data-stu-id="96261-405">Project 2</span></span></td>
<td><span data-ttu-id="96261-406">1.</span><span class="sxs-lookup"><span data-stu-id="96261-406">1</span></span></td>
<td><span data-ttu-id="96261-407">10001</span><span class="sxs-lookup"><span data-stu-id="96261-407">10001</span></span></td>
<td><span data-ttu-id="96261-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="96261-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="96261-409">10,00</span><span class="sxs-lookup"><span data-stu-id="96261-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="96261-410">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="96261-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="96261-411">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="96261-411">Journal</span></span></th>
<th><span data-ttu-id="96261-412">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="96261-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="96261-413">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="96261-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="96261-414">Versija</span><span class="sxs-lookup"><span data-stu-id="96261-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-415">00003</span><span class="sxs-lookup"><span data-stu-id="96261-415">00003</span></span></td>
<td><span data-ttu-id="96261-416">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="96261-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="96261-417">Finanšu</span><span class="sxs-lookup"><span data-stu-id="96261-417">Fiscal</span></span></td>
<td><span data-ttu-id="96261-418">2017</span><span class="sxs-lookup"><span data-stu-id="96261-418">2017</span></span></td>
<td><span data-ttu-id="96261-419">Periods 1</span><span class="sxs-lookup"><span data-stu-id="96261-419">Period 1</span></span></td>
<td><span data-ttu-id="96261-420">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="96261-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="96261-421">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="96261-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="96261-422">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="96261-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="96261-423">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-423">Cost object</span></span></th>
<th><span data-ttu-id="96261-424">Lielums</span><span class="sxs-lookup"><span data-stu-id="96261-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-425">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="96261-426">Proj 1</span></span></td>
<td><span data-ttu-id="96261-427">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="96261-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="96261-428">3,00</span><span class="sxs-lookup"><span data-stu-id="96261-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-429">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="96261-430">Proj 2</span></span></td>
<td><span data-ttu-id="96261-431">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="96261-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="96261-432">1,00</span><span class="sxs-lookup"><span data-stu-id="96261-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="96261-433">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="96261-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-434">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="96261-435">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="96261-435">Cost element</span></span></th>
<th><span data-ttu-id="96261-436">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="96261-436">Cost behavior</span></span></th>
<th><span data-ttu-id="96261-437">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-437">Amount</span></span></th>
<th><span data-ttu-id="96261-438">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="96261-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="96261-439">CC0001</span></span></td>
<td><span data-ttu-id="96261-440">HR</span><span class="sxs-lookup"><span data-stu-id="96261-440">HR</span></span></td>
<td><span data-ttu-id="96261-441">10001</span><span class="sxs-lookup"><span data-stu-id="96261-441">10001</span></span></td>
<td><span data-ttu-id="96261-442">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-442">Electricity</span></span></td>
<td><span data-ttu-id="96261-443">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-443">Variable cost</span></span></td>
<td><span data-ttu-id="96261-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="96261-444">-30.00</span></span></td>
<td><span data-ttu-id="96261-445">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="96261-446">Proj 1</span></span></td>
<td><span data-ttu-id="96261-447">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="96261-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="96261-448">10001</span><span class="sxs-lookup"><span data-stu-id="96261-448">10001</span></span></td>
<td><span data-ttu-id="96261-449">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-449">Electricity</span></span></td>
<td><span data-ttu-id="96261-450">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-450">Variable cost</span></span></td>
<td><span data-ttu-id="96261-451">30,00</span><span class="sxs-lookup"><span data-stu-id="96261-451">30.00</span></span></td>
<td><span data-ttu-id="96261-452">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-453">CC001</span><span class="sxs-lookup"><span data-stu-id="96261-453">CC001</span></span></td>
<td><span data-ttu-id="96261-454">HR</span><span class="sxs-lookup"><span data-stu-id="96261-454">HR</span></span></td>
<td><span data-ttu-id="96261-455">10001</span><span class="sxs-lookup"><span data-stu-id="96261-455">10001</span></span></td>
<td><span data-ttu-id="96261-456">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-456">Electricity</span></span></td>
<td><span data-ttu-id="96261-457">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-457">Variable cost</span></span></td>
<td><span data-ttu-id="96261-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="96261-458">-10.00</span></span></td>
<td><span data-ttu-id="96261-459">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="96261-460">Proj 2</span></span></td>
<td><span data-ttu-id="96261-461">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="96261-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="96261-462">10001</span><span class="sxs-lookup"><span data-stu-id="96261-462">10001</span></span></td>
<td><span data-ttu-id="96261-463">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-463">Electricity</span></span></td>
<td><span data-ttu-id="96261-464">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-464">Variable cost</span></span></td>
<td><span data-ttu-id="96261-465">10,00</span><span class="sxs-lookup"><span data-stu-id="96261-465">10.00</span></span></td>
<td><span data-ttu-id="96261-466">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-467">Detalizētu informāciju par pieskaitāmo izmaksu likmes politiku skatiet sadaļā Pieskaitāmo izmaksu likmes politika un Sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="96261-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="96261-468">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)</span><span class="sxs-lookup"><span data-stu-id="96261-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="96261-469">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="96261-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="96261-470">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="96261-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="96261-471">Finance and Operations atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="96261-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="96261-472">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="96261-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="96261-473">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="96261-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="96261-474">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="96261-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="96261-475">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="96261-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="96261-476">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="96261-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="96261-477">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="96261-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="96261-478">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="96261-478">Define the cost allocation</span></span>

<span data-ttu-id="96261-479">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="96261-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="96261-480">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="96261-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="96261-481">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="96261-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-482">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-482">Cost object</span></span></th>
<th><span data-ttu-id="96261-483">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="96261-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-484">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-484">CC002</span></span></td>
<td><span data-ttu-id="96261-485">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-485">Finance</span></span></td>
<td><span data-ttu-id="96261-486">35</span><span class="sxs-lookup"><span data-stu-id="96261-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-487">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-487">CC003</span></span></td>
<td><span data-ttu-id="96261-488">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-488">Assembly</span></span></td>
<td><span data-ttu-id="96261-489">55</span><span class="sxs-lookup"><span data-stu-id="96261-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-490">CC004</span><span class="sxs-lookup"><span data-stu-id="96261-490">CC004</span></span></td>
<td><span data-ttu-id="96261-491">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="96261-491">Packaging</span></span></td>
<td><span data-ttu-id="96261-492">10.</span><span class="sxs-lookup"><span data-stu-id="96261-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-493">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="96261-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="96261-494">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="96261-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-495">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-495">Cost object</span></span></th>
<th><span data-ttu-id="96261-496">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="96261-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-497">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-497">CC003</span></span></td>
<td><span data-ttu-id="96261-498">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-498">Assembly</span></span></td>
<td><span data-ttu-id="96261-499">65</span><span class="sxs-lookup"><span data-stu-id="96261-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-500">CC004</span><span class="sxs-lookup"><span data-stu-id="96261-500">CC004</span></span></td>
<td><span data-ttu-id="96261-501">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="96261-501">Packaging</span></span></td>
<td><span data-ttu-id="96261-502">35</span><span class="sxs-lookup"><span data-stu-id="96261-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-503">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="96261-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="96261-504">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="96261-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-505">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-505">Cost object</span></span></th>
<th><span data-ttu-id="96261-506">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="96261-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="96261-507">Prod 1</span></span></td>
<td><span data-ttu-id="96261-508">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-508">Product 1</span></span></td>
<td><span data-ttu-id="96261-509">60</span><span class="sxs-lookup"><span data-stu-id="96261-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="96261-510">Prod 2</span></span></td>
<td><span data-ttu-id="96261-511">2. prece</span><span class="sxs-lookup"><span data-stu-id="96261-511">Product 2</span></span></td>
<td><span data-ttu-id="96261-512">20</span><span class="sxs-lookup"><span data-stu-id="96261-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-513">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="96261-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="96261-514">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="96261-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-515">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-515">Cost object</span></span></th>
<th><span data-ttu-id="96261-516">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="96261-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="96261-517">Prod 1</span></span></td>
<td><span data-ttu-id="96261-518">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-518">Product 1</span></span></td>
<td><span data-ttu-id="96261-519">80</span><span class="sxs-lookup"><span data-stu-id="96261-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="96261-520">Prod 2</span></span></td>
<td><span data-ttu-id="96261-521">2. prece</span><span class="sxs-lookup"><span data-stu-id="96261-521">Product 2</span></span></td>
<td><span data-ttu-id="96261-522">15.</span><span class="sxs-lookup"><span data-stu-id="96261-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-523">**Piezīme.** Sistēmā Finance and Operations statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="96261-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="96261-524">Plašāku informāciju par statistisko mēru nodrošinātājiem skatiet sadaļā Statistisko mēru nodrošinātāja veidnes.</span><span class="sxs-lookup"><span data-stu-id="96261-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="96261-525">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.) Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="96261-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-526">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-526">Cost object</span></span></th>
<th><span data-ttu-id="96261-527">Lielums</span><span class="sxs-lookup"><span data-stu-id="96261-527">Magnitude</span></span></th>
<th><span data-ttu-id="96261-528">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="96261-528">Allocation factor</span></span></th>
<th><span data-ttu-id="96261-529">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-529">Amount</span></span></th>
<th><span data-ttu-id="96261-530">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="96261-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-531">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-531">CC002</span></span></td>
<td><span data-ttu-id="96261-532">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-532">Finance</span></span></td>
<td><span data-ttu-id="96261-533">35</span><span class="sxs-lookup"><span data-stu-id="96261-533">35</span></span></td>
<td><span data-ttu-id="96261-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="96261-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="96261-535">175.00</span><span class="sxs-lookup"><span data-stu-id="96261-535">175.00</span></span></td>
<td><span data-ttu-id="96261-536">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-537">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-537">CC003</span></span></td>
<td><span data-ttu-id="96261-538">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-538">Assembly</span></span></td>
<td><span data-ttu-id="96261-539">55</span><span class="sxs-lookup"><span data-stu-id="96261-539">55</span></span></td>
<td><span data-ttu-id="96261-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="96261-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="96261-541">275.00</span><span class="sxs-lookup"><span data-stu-id="96261-541">275.00</span></span></td>
<td><span data-ttu-id="96261-542">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-543">CC004</span><span class="sxs-lookup"><span data-stu-id="96261-543">CC004</span></span></td>
<td><span data-ttu-id="96261-544">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="96261-544">Packaging</span></span></td>
<td><span data-ttu-id="96261-545">10.</span><span class="sxs-lookup"><span data-stu-id="96261-545">10</span></span></td>
<td><span data-ttu-id="96261-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="96261-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="96261-547">50,00</span><span class="sxs-lookup"><span data-stu-id="96261-547">50.00</span></span></td>
<td><span data-ttu-id="96261-548">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-549">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-549">CC002</span></span></td>
<td><span data-ttu-id="96261-550">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-550">Finance</span></span></td>
<td><span data-ttu-id="96261-551">35</span><span class="sxs-lookup"><span data-stu-id="96261-551">35</span></span></td>
<td><span data-ttu-id="96261-552">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="96261-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="96261-553">436.00</span><span class="sxs-lookup"><span data-stu-id="96261-553">436.00</span></span></td>
<td><span data-ttu-id="96261-554">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-555">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-555">CC003</span></span></td>
<td><span data-ttu-id="96261-556">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-556">Assembly</span></span></td>
<td><span data-ttu-id="96261-557">55</span><span class="sxs-lookup"><span data-stu-id="96261-557">55</span></span></td>
<td><span data-ttu-id="96261-558">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="96261-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="96261-559">685.14</span><span class="sxs-lookup"><span data-stu-id="96261-559">685.14</span></span></td>
<td><span data-ttu-id="96261-560">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-561">CC004</span><span class="sxs-lookup"><span data-stu-id="96261-561">CC004</span></span></td>
<td><span data-ttu-id="96261-562">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="96261-562">Packaging</span></span></td>
<td><span data-ttu-id="96261-563">10.</span><span class="sxs-lookup"><span data-stu-id="96261-563">10</span></span></td>
<td><span data-ttu-id="96261-564">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="96261-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="96261-565">124.57</span><span class="sxs-lookup"><span data-stu-id="96261-565">124.57</span></span></td>
<td><span data-ttu-id="96261-566">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-567">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="96261-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-568">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-568">Cost object</span></span></th>
<th><span data-ttu-id="96261-569">Lielums</span><span class="sxs-lookup"><span data-stu-id="96261-569">Magnitude</span></span></th>
<th><span data-ttu-id="96261-570">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="96261-570">Allocation factor</span></span></th>
<th><span data-ttu-id="96261-571">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-571">Amount</span></span></th>
<th><span data-ttu-id="96261-572">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="96261-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-573">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-573">CC003</span></span></td>
<td><span data-ttu-id="96261-574">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-574">Assembly</span></span></td>
<td><span data-ttu-id="96261-575">65</span><span class="sxs-lookup"><span data-stu-id="96261-575">65</span></span></td>
<td><span data-ttu-id="96261-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="96261-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="96261-577">438.75</span><span class="sxs-lookup"><span data-stu-id="96261-577">438.75</span></span></td>
<td><span data-ttu-id="96261-578">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-579">CC004</span><span class="sxs-lookup"><span data-stu-id="96261-579">CC004</span></span></td>
<td><span data-ttu-id="96261-580">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="96261-580">Packaging</span></span></td>
<td><span data-ttu-id="96261-581">35</span><span class="sxs-lookup"><span data-stu-id="96261-581">35</span></span></td>
<td><span data-ttu-id="96261-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="96261-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="96261-583">236.25</span><span class="sxs-lookup"><span data-stu-id="96261-583">236.25</span></span></td>
<td><span data-ttu-id="96261-584">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-585">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-585">CC003</span></span></td>
<td><span data-ttu-id="96261-586">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-586">Assembly</span></span></td>
<td><span data-ttu-id="96261-587">65</span><span class="sxs-lookup"><span data-stu-id="96261-587">65</span></span></td>
<td><span data-ttu-id="96261-588">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="96261-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="96261-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="96261-589">5,297.69</span></span></td>
<td><span data-ttu-id="96261-590">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-591">CC004</span><span class="sxs-lookup"><span data-stu-id="96261-591">CC004</span></span></td>
<td><span data-ttu-id="96261-592">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="96261-592">Packaging</span></span></td>
<td><span data-ttu-id="96261-593">35</span><span class="sxs-lookup"><span data-stu-id="96261-593">35</span></span></td>
<td><span data-ttu-id="96261-594">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="96261-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="96261-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="96261-595">2,852.60</span></span></td>
<td><span data-ttu-id="96261-596">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-597">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="96261-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-598">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-598">Cost object</span></span></th>
<th><span data-ttu-id="96261-599">Lielums</span><span class="sxs-lookup"><span data-stu-id="96261-599">Magnitude</span></span></th>
<th><span data-ttu-id="96261-600">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="96261-600">Allocation factor</span></span></th>
<th><span data-ttu-id="96261-601">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-601">Amount</span></span></th>
<th><span data-ttu-id="96261-602">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="96261-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="96261-603">Prod 1</span></span></td>
<td><span data-ttu-id="96261-604">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-604">Product 1</span></span></td>
<td><span data-ttu-id="96261-605">60</span><span class="sxs-lookup"><span data-stu-id="96261-605">60</span></span></td>
<td><span data-ttu-id="96261-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="96261-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="96261-607">535.31</span><span class="sxs-lookup"><span data-stu-id="96261-607">535.31</span></span></td>
<td><span data-ttu-id="96261-608">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="96261-609">Prod 2</span></span></td>
<td><span data-ttu-id="96261-610">2. prece</span><span class="sxs-lookup"><span data-stu-id="96261-610">Product 2</span></span></td>
<td><span data-ttu-id="96261-611">20.</span><span class="sxs-lookup"><span data-stu-id="96261-611">20</span></span></td>
<td><span data-ttu-id="96261-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="96261-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="96261-613">178.44</span><span class="sxs-lookup"><span data-stu-id="96261-613">178.44</span></span></td>
<td><span data-ttu-id="96261-614">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="96261-615">Prod 1</span></span></td>
<td><span data-ttu-id="96261-616">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-616">Product 1</span></span></td>
<td><span data-ttu-id="96261-617">60</span><span class="sxs-lookup"><span data-stu-id="96261-617">60</span></span></td>
<td><span data-ttu-id="96261-618">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="96261-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="96261-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="96261-619">4,487.12</span></span></td>
<td><span data-ttu-id="96261-620">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="96261-621">Prod 2</span></span></td>
<td><span data-ttu-id="96261-622">2. prece</span><span class="sxs-lookup"><span data-stu-id="96261-622">Product 2</span></span></td>
<td><span data-ttu-id="96261-623">20.</span><span class="sxs-lookup"><span data-stu-id="96261-623">20</span></span></td>
<td><span data-ttu-id="96261-624">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="96261-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="96261-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="96261-625">1,495.71</span></span></td>
<td><span data-ttu-id="96261-626">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96261-627">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="96261-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-628">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-628">Cost object</span></span></th>
<th><span data-ttu-id="96261-629">Lielums</span><span class="sxs-lookup"><span data-stu-id="96261-629">Magnitude</span></span></th>
<th><span data-ttu-id="96261-630">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="96261-630">Allocation factor</span></span></th>
<th><span data-ttu-id="96261-631">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-631">Amount</span></span></th>
<th><span data-ttu-id="96261-632">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="96261-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="96261-633">Prod 1</span></span></td>
<td><span data-ttu-id="96261-634">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-634">Product 1</span></span></td>
<td><span data-ttu-id="96261-635">80</span><span class="sxs-lookup"><span data-stu-id="96261-635">80</span></span></td>
<td><span data-ttu-id="96261-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="96261-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="96261-637">241.05</span><span class="sxs-lookup"><span data-stu-id="96261-637">241.05</span></span></td>
<td><span data-ttu-id="96261-638">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="96261-639">Prod 2</span></span></td>
<td><span data-ttu-id="96261-640">2. prece</span><span class="sxs-lookup"><span data-stu-id="96261-640">Product 2</span></span></td>
<td><span data-ttu-id="96261-641">15</span><span class="sxs-lookup"><span data-stu-id="96261-641">15</span></span></td>
<td><span data-ttu-id="96261-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="96261-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="96261-643">45.20</span><span class="sxs-lookup"><span data-stu-id="96261-643">45.20</span></span></td>
<td><span data-ttu-id="96261-644">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="96261-645">Prod 1</span></span></td>
<td><span data-ttu-id="96261-646">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-646">Product 1</span></span></td>
<td><span data-ttu-id="96261-647">80</span><span class="sxs-lookup"><span data-stu-id="96261-647">80</span></span></td>
<td><span data-ttu-id="96261-648">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="96261-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="96261-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="96261-649">2,507.09</span></span></td>
<td><span data-ttu-id="96261-650">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="96261-651">Prod 2</span></span></td>
<td><span data-ttu-id="96261-652">2. prece</span><span class="sxs-lookup"><span data-stu-id="96261-652">Product 2</span></span></td>
<td><span data-ttu-id="96261-653">15</span><span class="sxs-lookup"><span data-stu-id="96261-653">15</span></span></td>
<td><span data-ttu-id="96261-654">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="96261-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="96261-655">470.08</span><span class="sxs-lookup"><span data-stu-id="96261-655">470.08</span></span></td>
<td><span data-ttu-id="96261-656">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="96261-657">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="96261-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="96261-658">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="96261-658">Journal</span></span></th>
<th><span data-ttu-id="96261-659">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="96261-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="96261-660">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="96261-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="96261-661">Versija</span><span class="sxs-lookup"><span data-stu-id="96261-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-662">00004</span><span class="sxs-lookup"><span data-stu-id="96261-662">00004</span></span></td>
<td><span data-ttu-id="96261-663">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="96261-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="96261-664">Finanšu</span><span class="sxs-lookup"><span data-stu-id="96261-664">Fiscal</span></span></td>
<td><span data-ttu-id="96261-665">2017</span><span class="sxs-lookup"><span data-stu-id="96261-665">2017</span></span></td>
<td><span data-ttu-id="96261-666">Periods 1</span><span class="sxs-lookup"><span data-stu-id="96261-666">Period 1</span></span></td>
<td><span data-ttu-id="96261-667">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="96261-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="96261-668">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="96261-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="96261-669">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="96261-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="96261-670">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="96261-671">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="96261-671">Cost element</span></span></th>
<th><span data-ttu-id="96261-672">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="96261-672">Cost behavior</span></span></th>
<th><span data-ttu-id="96261-673">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-674">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-675">CC001</span><span class="sxs-lookup"><span data-stu-id="96261-675">CC001</span></span></td>
<td><span data-ttu-id="96261-676">HR</span><span class="sxs-lookup"><span data-stu-id="96261-676">HR</span></span></td>
<td><span data-ttu-id="96261-677">10001</span><span class="sxs-lookup"><span data-stu-id="96261-677">10001</span></span></td>
<td><span data-ttu-id="96261-678">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-678">Electricity</span></span></td>
<td><span data-ttu-id="96261-679">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-679">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-680">500,00</span><span class="sxs-lookup"><span data-stu-id="96261-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-681">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-682">CC001</span><span class="sxs-lookup"><span data-stu-id="96261-682">CC001</span></span></td>
<td><span data-ttu-id="96261-683">HR</span><span class="sxs-lookup"><span data-stu-id="96261-683">HR</span></span></td>
<td><span data-ttu-id="96261-684">10001</span><span class="sxs-lookup"><span data-stu-id="96261-684">10001</span></span></td>
<td><span data-ttu-id="96261-685">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-685">Electricity</span></span></td>
<td><span data-ttu-id="96261-686">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-686">Variable cost</span></span></td>
<td><span data-ttu-id="96261-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="96261-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-688">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-689">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-689">CC002</span></span></td>
<td><span data-ttu-id="96261-690">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-690">Finance</span></span></td>
<td><span data-ttu-id="96261-691">10001</span><span class="sxs-lookup"><span data-stu-id="96261-691">10001</span></span></td>
<td><span data-ttu-id="96261-692">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-692">Electricity</span></span></td>
<td><span data-ttu-id="96261-693">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-693">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-694">675.00</span><span class="sxs-lookup"><span data-stu-id="96261-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-695">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-696">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-696">CC002</span></span></td>
<td><span data-ttu-id="96261-697">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-697">Finance</span></span></td>
<td><span data-ttu-id="96261-698">10001</span><span class="sxs-lookup"><span data-stu-id="96261-698">10001</span></span></td>
<td><span data-ttu-id="96261-699">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-699">Electricity</span></span></td>
<td><span data-ttu-id="96261-700">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-700">Variable cost</span></span></td>
<td><span data-ttu-id="96261-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="96261-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-702">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-703">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-703">CC003</span></span></td>
<td><span data-ttu-id="96261-704">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-704">Assembly</span></span></td>
<td><span data-ttu-id="96261-705">10001</span><span class="sxs-lookup"><span data-stu-id="96261-705">10001</span></span></td>
<td><span data-ttu-id="96261-706">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-706">Electricity</span></span></td>
<td><span data-ttu-id="96261-707">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-707">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-708">713.75</span><span class="sxs-lookup"><span data-stu-id="96261-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-709">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-710">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-710">CC003</span></span></td>
<td><span data-ttu-id="96261-711">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-711">Assembly</span></span></td>
<td><span data-ttu-id="96261-712">10001</span><span class="sxs-lookup"><span data-stu-id="96261-712">10001</span></span></td>
<td><span data-ttu-id="96261-713">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-713">Electricity</span></span></td>
<td><span data-ttu-id="96261-714">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-714">Variable cost</span></span></td>
<td><span data-ttu-id="96261-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="96261-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-716">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-717">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-717">CC003</span></span></td>
<td><span data-ttu-id="96261-718">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="96261-718">Packaging</span></span></td>
<td><span data-ttu-id="96261-719">10001</span><span class="sxs-lookup"><span data-stu-id="96261-719">10001</span></span></td>
<td><span data-ttu-id="96261-720">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-720">Electricity</span></span></td>
<td><span data-ttu-id="96261-721">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-721">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-722">286.25</span><span class="sxs-lookup"><span data-stu-id="96261-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-723">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-724">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-724">CC003</span></span></td>
<td><span data-ttu-id="96261-725">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="96261-725">Packaging</span></span></td>
<td><span data-ttu-id="96261-726">10001</span><span class="sxs-lookup"><span data-stu-id="96261-726">10001</span></span></td>
<td><span data-ttu-id="96261-727">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-727">Electricity</span></span></td>
<td><span data-ttu-id="96261-728">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-728">Variable cost</span></span></td>
<td><span data-ttu-id="96261-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="96261-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-730">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="96261-731">Prod 1</span></span></td>
<td><span data-ttu-id="96261-732">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-732">Product 1</span></span></td>
<td><span data-ttu-id="96261-733">10001</span><span class="sxs-lookup"><span data-stu-id="96261-733">10001</span></span></td>
<td><span data-ttu-id="96261-734">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-734">Electricity</span></span></td>
<td><span data-ttu-id="96261-735">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-735">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-736">776.36</span><span class="sxs-lookup"><span data-stu-id="96261-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-737">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="96261-738">Prod 1</span></span></td>
<td><span data-ttu-id="96261-739">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-739">Product 1</span></span></td>
<td><span data-ttu-id="96261-740">10001</span><span class="sxs-lookup"><span data-stu-id="96261-740">10001</span></span></td>
<td><span data-ttu-id="96261-741">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-741">Electricity</span></span></td>
<td><span data-ttu-id="96261-742">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-742">Variable cost</span></span></td>
<td><span data-ttu-id="96261-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="96261-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-744">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="96261-745">Prod 2</span></span></td>
<td><span data-ttu-id="96261-746">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-746">Product 1</span></span></td>
<td><span data-ttu-id="96261-747">10001</span><span class="sxs-lookup"><span data-stu-id="96261-747">10001</span></span></td>
<td><span data-ttu-id="96261-748">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-748">Electricity</span></span></td>
<td><span data-ttu-id="96261-749">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-749">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-750">223.64</span><span class="sxs-lookup"><span data-stu-id="96261-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-751">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="96261-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="96261-752">Prod 2</span></span></td>
<td><span data-ttu-id="96261-753">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-753">Product 1</span></span></td>
<td><span data-ttu-id="96261-754">10001</span><span class="sxs-lookup"><span data-stu-id="96261-754">10001</span></span></td>
<td><span data-ttu-id="96261-755">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-755">Electricity</span></span></td>
<td><span data-ttu-id="96261-756">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-756">Variable cost</span></span></td>
<td><span data-ttu-id="96261-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="96261-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="96261-758">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="96261-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="96261-759">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="96261-760">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="96261-760">Cost element</span></span></th>
<th><span data-ttu-id="96261-761">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="96261-761">Cost behavior</span></span></th>
<th><span data-ttu-id="96261-762">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-762">Amount</span></span></th>
<th><span data-ttu-id="96261-763">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="96261-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="96261-764">CC001</span><span class="sxs-lookup"><span data-stu-id="96261-764">CC001</span></span></td>
<td><span data-ttu-id="96261-765">HR</span><span class="sxs-lookup"><span data-stu-id="96261-765">HR</span></span></td>
<td><span data-ttu-id="96261-766">10001</span><span class="sxs-lookup"><span data-stu-id="96261-766">10001</span></span></td>
<td><span data-ttu-id="96261-767">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-767">Electricity</span></span></td>
<td><span data-ttu-id="96261-768">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-768">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="96261-769">-500.00</span></span></td>
<td><span data-ttu-id="96261-770">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-771">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-771">CC002</span></span></td>
<td><span data-ttu-id="96261-772">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-772">Finance</span></span></td>
<td><span data-ttu-id="96261-773">10001</span><span class="sxs-lookup"><span data-stu-id="96261-773">10001</span></span></td>
<td><span data-ttu-id="96261-774">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-774">Electricity</span></span></td>
<td><span data-ttu-id="96261-775">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-775">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-776">175.00</span><span class="sxs-lookup"><span data-stu-id="96261-776">175.00</span></span></td>
<td><span data-ttu-id="96261-777">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-778">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-778">CC003</span></span></td>
<td><span data-ttu-id="96261-779">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-779">Assembly</span></span></td>
<td><span data-ttu-id="96261-780">10001</span><span class="sxs-lookup"><span data-stu-id="96261-780">10001</span></span></td>
<td><span data-ttu-id="96261-781">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-781">Electricity</span></span></td>
<td><span data-ttu-id="96261-782">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-782">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-783">275.00</span><span class="sxs-lookup"><span data-stu-id="96261-783">275.00</span></span></td>
<td><span data-ttu-id="96261-784">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-785">CC004</span><span class="sxs-lookup"><span data-stu-id="96261-785">CC004</span></span></td>
<td><span data-ttu-id="96261-786">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="96261-786">Packaging</span></span></td>
<td><span data-ttu-id="96261-787">10001</span><span class="sxs-lookup"><span data-stu-id="96261-787">10001</span></span></td>
<td><span data-ttu-id="96261-788">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-788">Electricity</span></span></td>
<td><span data-ttu-id="96261-789">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-789">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-790">50,00</span><span class="sxs-lookup"><span data-stu-id="96261-790">50,00</span></span></td>
<td><span data-ttu-id="96261-791">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-792">CC001</span><span class="sxs-lookup"><span data-stu-id="96261-792">CC001</span></span></td>
<td><span data-ttu-id="96261-793">HR</span><span class="sxs-lookup"><span data-stu-id="96261-793">HR</span></span></td>
<td><span data-ttu-id="96261-794">10001</span><span class="sxs-lookup"><span data-stu-id="96261-794">10001</span></span></td>
<td><span data-ttu-id="96261-795">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-795">Electricity</span></span></td>
<td><span data-ttu-id="96261-796">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-796">Variable cost</span></span></td>
<td><span data-ttu-id="96261-797">-1245,71</span><span class="sxs-lookup"><span data-stu-id="96261-797">-1,245.71</span></span></td>
<td><span data-ttu-id="96261-798">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-799">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-799">CC002</span></span></td>
<td><span data-ttu-id="96261-800">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-800">Finance</span></span></td>
<td><span data-ttu-id="96261-801">10001</span><span class="sxs-lookup"><span data-stu-id="96261-801">10001</span></span></td>
<td><span data-ttu-id="96261-802">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-802">Electricity</span></span></td>
<td><span data-ttu-id="96261-803">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-803">Variable cost</span></span></td>
<td><span data-ttu-id="96261-804">436.00</span><span class="sxs-lookup"><span data-stu-id="96261-804">436.00</span></span></td>
<td><span data-ttu-id="96261-805">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-806">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-806">CC003</span></span></td>
<td><span data-ttu-id="96261-807">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-807">Assembly</span></span></td>
<td><span data-ttu-id="96261-808">10001</span><span class="sxs-lookup"><span data-stu-id="96261-808">10001</span></span></td>
<td><span data-ttu-id="96261-809">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-809">Electricity</span></span></td>
<td><span data-ttu-id="96261-810">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-810">Variable cost</span></span></td>
<td><span data-ttu-id="96261-811">685.14</span><span class="sxs-lookup"><span data-stu-id="96261-811">685.14</span></span></td>
<td><span data-ttu-id="96261-812">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-813">CC004</span><span class="sxs-lookup"><span data-stu-id="96261-813">CC004</span></span></td>
<td><span data-ttu-id="96261-814">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="96261-814">Packaging</span></span></td>
<td><span data-ttu-id="96261-815">10001</span><span class="sxs-lookup"><span data-stu-id="96261-815">10001</span></span></td>
<td><span data-ttu-id="96261-816">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-816">Electricity</span></span></td>
<td><span data-ttu-id="96261-817">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-817">Variable cost</span></span></td>
<td><span data-ttu-id="96261-818">124.57</span><span class="sxs-lookup"><span data-stu-id="96261-818">124.57</span></span></td>
<td><span data-ttu-id="96261-819">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-820">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-820">CC002</span></span></td>
<td><span data-ttu-id="96261-821">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-821">Finance</span></span></td>
<td><span data-ttu-id="96261-822">10001</span><span class="sxs-lookup"><span data-stu-id="96261-822">10001</span></span></td>
<td><span data-ttu-id="96261-823">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-823">Electricity</span></span></td>
<td><span data-ttu-id="96261-824">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-824">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="96261-825">-675.00</span></span></td>
<td><span data-ttu-id="96261-826">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-827">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-827">CC003</span></span></td>
<td><span data-ttu-id="96261-828">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-828">Assembly</span></span></td>
<td><span data-ttu-id="96261-829">10001</span><span class="sxs-lookup"><span data-stu-id="96261-829">10001</span></span></td>
<td><span data-ttu-id="96261-830">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-830">Electricity</span></span></td>
<td><span data-ttu-id="96261-831">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-831">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-832">438.75</span><span class="sxs-lookup"><span data-stu-id="96261-832">438.75</span></span></td>
<td><span data-ttu-id="96261-833">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-834">CC004</span><span class="sxs-lookup"><span data-stu-id="96261-834">CC004</span></span></td>
<td><span data-ttu-id="96261-835">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="96261-835">Packaging</span></span></td>
<td><span data-ttu-id="96261-836">10001</span><span class="sxs-lookup"><span data-stu-id="96261-836">10001</span></span></td>
<td><span data-ttu-id="96261-837">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-837">Electricity</span></span></td>
<td><span data-ttu-id="96261-838">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-838">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-839">236.25</span><span class="sxs-lookup"><span data-stu-id="96261-839">236.25</span></span></td>
<td><span data-ttu-id="96261-840">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-841">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-841">CC002</span></span></td>
<td><span data-ttu-id="96261-842">Finanses</span><span class="sxs-lookup"><span data-stu-id="96261-842">Finance</span></span></td>
<td><span data-ttu-id="96261-843">10001</span><span class="sxs-lookup"><span data-stu-id="96261-843">10001</span></span></td>
<td><span data-ttu-id="96261-844">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-844">Electricity</span></span></td>
<td><span data-ttu-id="96261-845">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-845">Variable cost</span></span></td>
<td><span data-ttu-id="96261-846">-8150,29</span><span class="sxs-lookup"><span data-stu-id="96261-846">-8,150.29</span></span></td>
<td><span data-ttu-id="96261-847">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-848">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-848">CC003</span></span></td>
<td><span data-ttu-id="96261-849">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-849">Assembly</span></span></td>
<td><span data-ttu-id="96261-850">10001</span><span class="sxs-lookup"><span data-stu-id="96261-850">10001</span></span></td>
<td><span data-ttu-id="96261-851">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-851">Electricity</span></span></td>
<td><span data-ttu-id="96261-852">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-852">Variable cost</span></span></td>
<td><span data-ttu-id="96261-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="96261-853">5,297.69</span></span></td>
<td><span data-ttu-id="96261-854">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-855">CC004</span><span class="sxs-lookup"><span data-stu-id="96261-855">CC004</span></span></td>
<td><span data-ttu-id="96261-856">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="96261-856">Packaging</span></span></td>
<td><span data-ttu-id="96261-857">10001</span><span class="sxs-lookup"><span data-stu-id="96261-857">10001</span></span></td>
<td><span data-ttu-id="96261-858">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-858">Electricity</span></span></td>
<td><span data-ttu-id="96261-859">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-859">Variable cost</span></span></td>
<td><span data-ttu-id="96261-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="96261-860">2,852.60</span></span></td>
<td><span data-ttu-id="96261-861">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-862">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-862">CC003</span></span></td>
<td><span data-ttu-id="96261-863">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-863">Assembly</span></span></td>
<td><span data-ttu-id="96261-864">10001</span><span class="sxs-lookup"><span data-stu-id="96261-864">10001</span></span></td>
<td><span data-ttu-id="96261-865">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-865">Electricity</span></span></td>
<td><span data-ttu-id="96261-866">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-866">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="96261-867">-713.75</span></span></td>
<td><span data-ttu-id="96261-868">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="96261-869">Prod 1</span></span></td>
<td><span data-ttu-id="96261-870">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-870">Product 1</span></span></td>
<td><span data-ttu-id="96261-871">10001</span><span class="sxs-lookup"><span data-stu-id="96261-871">10001</span></span></td>
<td><span data-ttu-id="96261-872">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-872">Electricity</span></span></td>
<td><span data-ttu-id="96261-873">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-873">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-874">535.31</span><span class="sxs-lookup"><span data-stu-id="96261-874">535.31</span></span></td>
<td><span data-ttu-id="96261-875">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="96261-876">Prod 2</span></span></td>
<td><span data-ttu-id="96261-877">2. prece</span><span class="sxs-lookup"><span data-stu-id="96261-877">Product 2</span></span></td>
<td><span data-ttu-id="96261-878">10001</span><span class="sxs-lookup"><span data-stu-id="96261-878">10001</span></span></td>
<td><span data-ttu-id="96261-879">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-879">Electricity</span></span></td>
<td><span data-ttu-id="96261-880">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-880">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-881">178.44</span><span class="sxs-lookup"><span data-stu-id="96261-881">178.44</span></span></td>
<td><span data-ttu-id="96261-882">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-883">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-883">CC003</span></span></td>
<td><span data-ttu-id="96261-884">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-884">Assembly</span></span></td>
<td><span data-ttu-id="96261-885">10001</span><span class="sxs-lookup"><span data-stu-id="96261-885">10001</span></span></td>
<td><span data-ttu-id="96261-886">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-886">Electricity</span></span></td>
<td><span data-ttu-id="96261-887">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-887">Variable cost</span></span></td>
<td><span data-ttu-id="96261-888">-5982,83</span><span class="sxs-lookup"><span data-stu-id="96261-888">-5,982.83</span></span></td>
<td><span data-ttu-id="96261-889">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="96261-890">Prod 1</span></span></td>
<td><span data-ttu-id="96261-891">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-891">Product 1</span></span></td>
<td><span data-ttu-id="96261-892">10001</span><span class="sxs-lookup"><span data-stu-id="96261-892">10001</span></span></td>
<td><span data-ttu-id="96261-893">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-893">Electricity</span></span></td>
<td><span data-ttu-id="96261-894">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-894">Variable cost</span></span></td>
<td><span data-ttu-id="96261-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="96261-895">4,487.12</span></span></td>
<td><span data-ttu-id="96261-896">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="96261-897">Prod 2</span></span></td>
<td><span data-ttu-id="96261-898">2. prece</span><span class="sxs-lookup"><span data-stu-id="96261-898">Product 2</span></span></td>
<td><span data-ttu-id="96261-899">10001</span><span class="sxs-lookup"><span data-stu-id="96261-899">10001</span></span></td>
<td><span data-ttu-id="96261-900">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-900">Electricity</span></span></td>
<td><span data-ttu-id="96261-901">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-901">Variable cost</span></span></td>
<td><span data-ttu-id="96261-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="96261-902">1,495.71</span></span></td>
<td><span data-ttu-id="96261-903">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-904">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-904">CC003</span></span></td>
<td><span data-ttu-id="96261-905">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-905">Assembly</span></span></td>
<td><span data-ttu-id="96261-906">10001</span><span class="sxs-lookup"><span data-stu-id="96261-906">10001</span></span></td>
<td><span data-ttu-id="96261-907">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-907">Electricity</span></span></td>
<td><span data-ttu-id="96261-908">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-908">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="96261-909">-286.25</span></span></td>
<td><span data-ttu-id="96261-910">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="96261-911">Prod 1</span></span></td>
<td><span data-ttu-id="96261-912">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-912">Product 1</span></span></td>
<td><span data-ttu-id="96261-913">10001</span><span class="sxs-lookup"><span data-stu-id="96261-913">10001</span></span></td>
<td><span data-ttu-id="96261-914">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-914">Electricity</span></span></td>
<td><span data-ttu-id="96261-915">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-915">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-916">241.05</span><span class="sxs-lookup"><span data-stu-id="96261-916">241.05</span></span></td>
<td><span data-ttu-id="96261-917">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="96261-918">Prod 2</span></span></td>
<td><span data-ttu-id="96261-919">2. prece</span><span class="sxs-lookup"><span data-stu-id="96261-919">Product 2</span></span></td>
<td><span data-ttu-id="96261-920">10001</span><span class="sxs-lookup"><span data-stu-id="96261-920">10001</span></span></td>
<td><span data-ttu-id="96261-921">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-921">Electricity</span></span></td>
<td><span data-ttu-id="96261-922">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-922">Fixed cost</span></span></td>
<td><span data-ttu-id="96261-923">45.20</span><span class="sxs-lookup"><span data-stu-id="96261-923">45.20</span></span></td>
<td><span data-ttu-id="96261-924">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-925">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-925">CC003</span></span></td>
<td><span data-ttu-id="96261-926">Montāža</span><span class="sxs-lookup"><span data-stu-id="96261-926">Assembly</span></span></td>
<td><span data-ttu-id="96261-927">10001</span><span class="sxs-lookup"><span data-stu-id="96261-927">10001</span></span></td>
<td><span data-ttu-id="96261-928">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-928">Electricity</span></span></td>
<td><span data-ttu-id="96261-929">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-929">Variable cost</span></span></td>
<td><span data-ttu-id="96261-930">-2977,17</span><span class="sxs-lookup"><span data-stu-id="96261-930">-2,977.17</span></span></td>
<td><span data-ttu-id="96261-931">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="96261-932">Prod 1</span></span></td>
<td><span data-ttu-id="96261-933">1. prece</span><span class="sxs-lookup"><span data-stu-id="96261-933">Product 1</span></span></td>
<td><span data-ttu-id="96261-934">10001</span><span class="sxs-lookup"><span data-stu-id="96261-934">10001</span></span></td>
<td><span data-ttu-id="96261-935">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-935">Electricity</span></span></td>
<td><span data-ttu-id="96261-936">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-936">Variable cost</span></span></td>
<td><span data-ttu-id="96261-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="96261-937">2,507.09</span></span></td>
<td><span data-ttu-id="96261-938">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="96261-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="96261-939">Prod 2</span></span></td>
<td><span data-ttu-id="96261-940">2. prece</span><span class="sxs-lookup"><span data-stu-id="96261-940">Product 2</span></span></td>
<td><span data-ttu-id="96261-941">10001</span><span class="sxs-lookup"><span data-stu-id="96261-941">10001</span></span></td>
<td><span data-ttu-id="96261-942">Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-942">Electricity</span></span></td>
<td><span data-ttu-id="96261-943">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-943">Variable cost</span></span></td>
<td><span data-ttu-id="96261-944">470.08</span><span class="sxs-lookup"><span data-stu-id="96261-944">470.08</span></span></td>
<td><span data-ttu-id="96261-945">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="96261-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="96261-946">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="96261-946">Conclusion</span></span>
<span data-ttu-id="96261-947">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="96261-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="96261-948">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="96261-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="96261-949">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="96261-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="96261-950">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="96261-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="96261-951">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="96261-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="96261-952">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="96261-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="96261-953">Summa</span><span class="sxs-lookup"><span data-stu-id="96261-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="96261-954">CC099</span><span class="sxs-lookup"><span data-stu-id="96261-954">CC099</span></span></th>
<th><span data-ttu-id="96261-955">CC001</span><span class="sxs-lookup"><span data-stu-id="96261-955">CC001</span></span></th>
<th><span data-ttu-id="96261-956">CC002</span><span class="sxs-lookup"><span data-stu-id="96261-956">CC002</span></span></th>
<th><span data-ttu-id="96261-957">CC003</span><span class="sxs-lookup"><span data-stu-id="96261-957">CC003</span></span></th>
<th><span data-ttu-id="96261-958">CC004</span><span class="sxs-lookup"><span data-stu-id="96261-958">CC004</span></span></th>
<th><span data-ttu-id="96261-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="96261-959">Proj 1</span></span></th>
<th><span data-ttu-id="96261-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="96261-960">Proj 2</span></span></th>
<th><span data-ttu-id="96261-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="96261-961">Prod 1</span></span></th>
<th><span data-ttu-id="96261-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="96261-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="96261-963">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="96261-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="96261-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="96261-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="96261-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="96261-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="96261-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="96261-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="96261-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="96261-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="96261-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="96261-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="96261-973">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="96261-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-974">0,00</span><span class="sxs-lookup"><span data-stu-id="96261-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="96261-975">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-976">0,00</span><span class="sxs-lookup"><span data-stu-id="96261-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-977">0,00</span><span class="sxs-lookup"><span data-stu-id="96261-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-978">0,00</span><span class="sxs-lookup"><span data-stu-id="96261-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-979">0,00</span><span class="sxs-lookup"><span data-stu-id="96261-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-980">0,00</span><span class="sxs-lookup"><span data-stu-id="96261-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="96261-981">776.36</span><span class="sxs-lookup"><span data-stu-id="96261-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-982">223.64</span><span class="sxs-lookup"><span data-stu-id="96261-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="96261-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="96261-984">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="96261-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-985">000</span><span class="sxs-lookup"><span data-stu-id="96261-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-986">0,00</span><span class="sxs-lookup"><span data-stu-id="96261-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-987">0,00</span><span class="sxs-lookup"><span data-stu-id="96261-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-988">0,00</span><span class="sxs-lookup"><span data-stu-id="96261-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-989">0,00</span><span class="sxs-lookup"><span data-stu-id="96261-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-990">30,00</span><span class="sxs-lookup"><span data-stu-id="96261-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-991">10,00</span><span class="sxs-lookup"><span data-stu-id="96261-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="96261-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="96261-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="96261-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="96261-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="96261-995">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="96261-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="96261-996">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="96261-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="96261-997">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="96261-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="96261-998">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="96261-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="96261-999">Papildinformāciju skatiet sadaļā Izmaksu apkopošanas politika.</span><span class="sxs-lookup"><span data-stu-id="96261-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="96261-1000">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)</span><span class="sxs-lookup"><span data-stu-id="96261-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




