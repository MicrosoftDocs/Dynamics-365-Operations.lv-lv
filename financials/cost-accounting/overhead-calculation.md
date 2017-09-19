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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 9e13fc9fa7e51a1299ca8698f581de979b680a7b
ms.openlocfilehash: a8c867ba49b95af2816fe8294059307e974c0a81
ms.contentlocale: lv-lv
ms.lasthandoff: 09/18/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="9667c-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="9667c-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9667c-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="9667c-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="9667c-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="9667c-105">Term definition</span></span>
---------------

<span data-ttu-id="9667c-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="9667c-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="9667c-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="9667c-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="9667c-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="9667c-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="9667c-109">Īre</span><span class="sxs-lookup"><span data-stu-id="9667c-109">Rent</span></span>
-   <span data-ttu-id="9667c-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-110">Electricity</span></span>
-   <span data-ttu-id="9667c-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="9667c-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="9667c-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="9667c-112">Overhead calculation overview</span></span>
<span data-ttu-id="9667c-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="9667c-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="9667c-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="9667c-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="9667c-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="9667c-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="9667c-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="9667c-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="9667c-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="9667c-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="9667c-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="9667c-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="9667c-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="9667c-119">Version type</span></span>
-   <span data-ttu-id="9667c-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="9667c-120">Date and time</span></span>
-   <span data-ttu-id="9667c-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="9667c-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="9667c-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="9667c-122">Fiscal year</span></span>
-   <span data-ttu-id="9667c-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="9667c-123">Fiscal period</span></span>

<span data-ttu-id="9667c-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="9667c-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="9667c-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="9667c-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="9667c-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="9667c-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="9667c-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="9667c-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="9667c-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="9667c-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="9667c-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="9667c-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="9667c-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="9667c-130">Therefore, you always have full traceability.</span></span> 
<span data-ttu-id="9667c-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="9667c-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="9667c-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="9667c-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="9667c-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="9667c-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="9667c-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="9667c-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="9667c-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="9667c-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="9667c-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="9667c-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="9667c-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9667c-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="9667c-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9667c-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="9667c-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="9667c-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="9667c-140">Main account</span></span></th>
<th><span data-ttu-id="9667c-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="9667c-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="9667c-143">CC099</span><span class="sxs-lookup"><span data-stu-id="9667c-143">CC099</span></span></td>
<td><span data-ttu-id="9667c-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="9667c-144">Default cost center</span></span></td>
<td><span data-ttu-id="9667c-145">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-145">10001</span></span></td>
<td><span data-ttu-id="9667c-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-146">Electricity</span></span></td>
<td><span data-ttu-id="9667c-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="9667c-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="9667c-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="9667c-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="9667c-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="9667c-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="9667c-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="9667c-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="9667c-151">Define the cost behavior rule</span></span>

<span data-ttu-id="9667c-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="9667c-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="9667c-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="9667c-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="9667c-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="9667c-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="9667c-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="9667c-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="9667c-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="9667c-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="9667c-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="9667c-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="9667c-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="9667c-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="9667c-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9667c-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="9667c-160">Journal</span></span></th>
<th><span data-ttu-id="9667c-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="9667c-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9667c-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="9667c-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9667c-163">Versija</span><span class="sxs-lookup"><span data-stu-id="9667c-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-164">00001</span><span class="sxs-lookup"><span data-stu-id="9667c-164">00001</span></span></td>
<td><span data-ttu-id="9667c-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="9667c-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="9667c-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="9667c-166">Fiscal</span></span></td>
<td><span data-ttu-id="9667c-167">2017</span><span class="sxs-lookup"><span data-stu-id="9667c-167">2017</span></span></td>
<td><span data-ttu-id="9667c-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="9667c-168">Period 1</span></span></td>
<td><span data-ttu-id="9667c-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="9667c-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="9667c-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="9667c-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9667c-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="9667c-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9667c-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9667c-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="9667c-173">Cost element</span></span></th>
<th><span data-ttu-id="9667c-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="9667c-174">Cost behavior</span></span></th>
<th><span data-ttu-id="9667c-175">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="9667c-177">CC099</span><span class="sxs-lookup"><span data-stu-id="9667c-177">CC099</span></span></td>
<td><span data-ttu-id="9667c-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="9667c-178">Default cost center</span></span></td>
<td><span data-ttu-id="9667c-179">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-179">10001</span></span></td>
<td><span data-ttu-id="9667c-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-180">Electricity</span></span></td>
<td><span data-ttu-id="9667c-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="9667c-181">Unclassified</span></span></td>
<td><span data-ttu-id="9667c-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9667c-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="9667c-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9667c-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="9667c-185">Cost element</span></span></th>
<th><span data-ttu-id="9667c-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="9667c-186">Cost behavior</span></span></th>
<th><span data-ttu-id="9667c-187">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-187">Amount</span></span></th>
<th><span data-ttu-id="9667c-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="9667c-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-189">CC099</span><span class="sxs-lookup"><span data-stu-id="9667c-189">CC099</span></span></td>
<td><span data-ttu-id="9667c-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="9667c-190">Default cost center</span></span></td>
<td><span data-ttu-id="9667c-191">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-191">10001</span></span></td>
<td><span data-ttu-id="9667c-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-192">Electricity</span></span></td>
<td><span data-ttu-id="9667c-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="9667c-193">Unclassified</span></span></td>
<td><span data-ttu-id="9667c-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-194">10,000.00</span></span></td>
<td><span data-ttu-id="9667c-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-196">CC099</span><span class="sxs-lookup"><span data-stu-id="9667c-196">CC099</span></span></td>
<td><span data-ttu-id="9667c-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="9667c-197">Default cost center</span></span></td>
<td><span data-ttu-id="9667c-198">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-198">10001</span></span></td>
<td><span data-ttu-id="9667c-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-199">Electricity</span></span></td>
<td><span data-ttu-id="9667c-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="9667c-200">Unclassified</span></span></td>
<td><span data-ttu-id="9667c-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-201">-10,000.00</span></span></td>
<td><span data-ttu-id="9667c-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-203">CC099</span><span class="sxs-lookup"><span data-stu-id="9667c-203">CC099</span></span></td>
<td><span data-ttu-id="9667c-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="9667c-204">Default cost center</span></span></td>
<td><span data-ttu-id="9667c-205">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-205">10001</span></span></td>
<td><span data-ttu-id="9667c-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-206">Electricity</span></span></td>
<td><span data-ttu-id="9667c-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-207">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-208">1,000.00</span></span></td>
<td><span data-ttu-id="9667c-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-210">CC099</span><span class="sxs-lookup"><span data-stu-id="9667c-210">CC099</span></span></td>
<td><span data-ttu-id="9667c-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="9667c-211">Default cost center</span></span></td>
<td><span data-ttu-id="9667c-212">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-212">10001</span></span></td>
<td><span data-ttu-id="9667c-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-213">Electricity</span></span></td>
<td><span data-ttu-id="9667c-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-214">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="9667c-215">9,000.00</span></span></td>
<td><span data-ttu-id="9667c-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-217">Detalizētu informāciju par izmaksu uzvedību skatiet sadaļā Izmaksu uzvedības politika.</span><span class="sxs-lookup"><span data-stu-id="9667c-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="9667c-218">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)</span><span class="sxs-lookup"><span data-stu-id="9667c-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="9667c-219">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="9667c-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="9667c-220">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="9667c-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="9667c-221">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="9667c-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="9667c-222">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="9667c-222">Define the cost distribution rule</span></span>

<span data-ttu-id="9667c-223">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="9667c-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="9667c-224">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="9667c-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="9667c-225">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="9667c-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="9667c-226">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="9667c-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="9667c-227">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="9667c-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="9667c-228">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="9667c-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-229">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-229">Cost object</span></span></th>
<th><span data-ttu-id="9667c-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="9667c-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-231">CC001</span><span class="sxs-lookup"><span data-stu-id="9667c-231">CC001</span></span></td>
<td><span data-ttu-id="9667c-232">HR</span><span class="sxs-lookup"><span data-stu-id="9667c-232">HR</span></span></td>
<td><span data-ttu-id="9667c-233">1000</span><span class="sxs-lookup"><span data-stu-id="9667c-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-234">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-234">CC002</span></span></td>
<td><span data-ttu-id="9667c-235">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-235">Finance</span></span></td>
<td><span data-ttu-id="9667c-236">6,000</span><span class="sxs-lookup"><span data-stu-id="9667c-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-237">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-237">CC003</span></span></td>
<td><span data-ttu-id="9667c-238">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-238">Assembly</span></span></td>
<td><span data-ttu-id="9667c-239">0</span><span class="sxs-lookup"><span data-stu-id="9667c-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-240">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="9667c-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-241">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-241">Cost object</span></span></th>
<th><span data-ttu-id="9667c-242">Lielums</span><span class="sxs-lookup"><span data-stu-id="9667c-242">Magnitude</span></span></th>
<th><span data-ttu-id="9667c-243">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="9667c-243">Allocation factor</span></span></th>
<th><span data-ttu-id="9667c-244">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-245">CC001</span><span class="sxs-lookup"><span data-stu-id="9667c-245">CC001</span></span></td>
<td><span data-ttu-id="9667c-246">HR</span><span class="sxs-lookup"><span data-stu-id="9667c-246">HR</span></span></td>
<td><span data-ttu-id="9667c-247">1000</span><span class="sxs-lookup"><span data-stu-id="9667c-247">1,000</span></span></td>
<td><span data-ttu-id="9667c-248">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="9667c-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="9667c-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-250">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-250">CC002</span></span></td>
<td><span data-ttu-id="9667c-251">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-251">Finance</span></span></td>
<td><span data-ttu-id="9667c-252">6,000</span><span class="sxs-lookup"><span data-stu-id="9667c-252">6,000</span></span></td>
<td><span data-ttu-id="9667c-253">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="9667c-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="9667c-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-255">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-255">CC003</span></span></td>
<td><span data-ttu-id="9667c-256">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-256">Assembly</span></span></td>
<td><span data-ttu-id="9667c-257">0</span><span class="sxs-lookup"><span data-stu-id="9667c-257">0</span></span></td>
<td><span data-ttu-id="9667c-258">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="9667c-259">0,00</span><span class="sxs-lookup"><span data-stu-id="9667c-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-260">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="9667c-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="9667c-261">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="9667c-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-262">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-262">Cost object</span></span></th>
<th><span data-ttu-id="9667c-263">Formula</span><span class="sxs-lookup"><span data-stu-id="9667c-263">Formula</span></span></th>
<th><span data-ttu-id="9667c-264">Lielums</span><span class="sxs-lookup"><span data-stu-id="9667c-264">Magnitude</span></span></th>
<th><span data-ttu-id="9667c-265">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="9667c-265">Allocation factor</span></span></th>
<th><span data-ttu-id="9667c-266">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-267">CC001</span><span class="sxs-lookup"><span data-stu-id="9667c-267">CC001</span></span></td>
<td><span data-ttu-id="9667c-268">HR</span><span class="sxs-lookup"><span data-stu-id="9667c-268">HR</span></span></td>
<td><span data-ttu-id="9667c-269">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="9667c-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="9667c-270">1.</span><span class="sxs-lookup"><span data-stu-id="9667c-270">1</span></span></td>
<td><span data-ttu-id="9667c-271">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="9667c-272">500,00</span><span class="sxs-lookup"><span data-stu-id="9667c-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-273">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-273">CC002</span></span></td>
<td><span data-ttu-id="9667c-274">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-274">Finance</span></span></td>
<td><span data-ttu-id="9667c-275">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="9667c-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="9667c-276">1.</span><span class="sxs-lookup"><span data-stu-id="9667c-276">1</span></span></td>
<td><span data-ttu-id="9667c-277">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="9667c-278">500,00</span><span class="sxs-lookup"><span data-stu-id="9667c-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-279">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-279">CC003</span></span></td>
<td><span data-ttu-id="9667c-280">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-280">Assembly</span></span></td>
<td><span data-ttu-id="9667c-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="9667c-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="9667c-282">0</span><span class="sxs-lookup"><span data-stu-id="9667c-282">0</span></span></td>
<td><span data-ttu-id="9667c-283">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="9667c-284">0,00</span><span class="sxs-lookup"><span data-stu-id="9667c-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="9667c-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="9667c-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9667c-286">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="9667c-286">Journal</span></span></th>
<th><span data-ttu-id="9667c-287">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="9667c-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9667c-288">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="9667c-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9667c-289">Versija</span><span class="sxs-lookup"><span data-stu-id="9667c-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-290">00002</span><span class="sxs-lookup"><span data-stu-id="9667c-290">00002</span></span></td>
<td><span data-ttu-id="9667c-291">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="9667c-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="9667c-292">Finanšu</span><span class="sxs-lookup"><span data-stu-id="9667c-292">Fiscal</span></span></td>
<td><span data-ttu-id="9667c-293">2017</span><span class="sxs-lookup"><span data-stu-id="9667c-293">2017</span></span></td>
<td><span data-ttu-id="9667c-294">Periods 1</span><span class="sxs-lookup"><span data-stu-id="9667c-294">Period 1</span></span></td>
<td><span data-ttu-id="9667c-295">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="9667c-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="9667c-296">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="9667c-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9667c-297">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="9667c-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9667c-298">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9667c-299">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="9667c-299">Cost element</span></span></th>
<th><span data-ttu-id="9667c-300">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="9667c-300">Cost behavior</span></span></th>
<th><span data-ttu-id="9667c-301">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-302">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-303">CC099</span><span class="sxs-lookup"><span data-stu-id="9667c-303">CC099</span></span></td>
<td><span data-ttu-id="9667c-304">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="9667c-304">Default cost center</span></span></td>
<td><span data-ttu-id="9667c-305">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-305">10001</span></span></td>
<td><span data-ttu-id="9667c-306">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-306">Electricity</span></span></td>
<td><span data-ttu-id="9667c-307">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-307">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-308">1000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-309">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-310">CC099</span><span class="sxs-lookup"><span data-stu-id="9667c-310">CC099</span></span></td>
<td><span data-ttu-id="9667c-311">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="9667c-311">Default cost center</span></span></td>
<td><span data-ttu-id="9667c-312">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-312">10001</span></span></td>
<td><span data-ttu-id="9667c-313">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-313">Electricity</span></span></td>
<td><span data-ttu-id="9667c-314">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-314">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="9667c-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9667c-316">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="9667c-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-317">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9667c-318">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="9667c-318">Cost element</span></span></th>
<th><span data-ttu-id="9667c-319">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="9667c-319">Cost behavior</span></span></th>
<th><span data-ttu-id="9667c-320">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-320">Amount</span></span></th>
<th><span data-ttu-id="9667c-321">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="9667c-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-322">CC099</span><span class="sxs-lookup"><span data-stu-id="9667c-322">CC099</span></span></td>
<td><span data-ttu-id="9667c-323">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="9667c-323">Default cost center</span></span></td>
<td><span data-ttu-id="9667c-324">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-324">10001</span></span></td>
<td><span data-ttu-id="9667c-325">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-325">Electricity</span></span></td>
<td><span data-ttu-id="9667c-326">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-326">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-327">-1000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-327">-1,000.00</span></span></td>
<td><span data-ttu-id="9667c-328">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-329">CC001</span><span class="sxs-lookup"><span data-stu-id="9667c-329">CC001</span></span></td>
<td><span data-ttu-id="9667c-330">HR</span><span class="sxs-lookup"><span data-stu-id="9667c-330">HR</span></span></td>
<td><span data-ttu-id="9667c-331">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-331">10001</span></span></td>
<td><span data-ttu-id="9667c-332">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-332">Electricity</span></span></td>
<td><span data-ttu-id="9667c-333">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-333">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-334">500,00</span><span class="sxs-lookup"><span data-stu-id="9667c-334">500.00</span></span></td>
<td><span data-ttu-id="9667c-335">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-336">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-336">CC002</span></span></td>
<td><span data-ttu-id="9667c-337">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-337">Finance</span></span></td>
<td><span data-ttu-id="9667c-338">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-338">10001</span></span></td>
<td><span data-ttu-id="9667c-339">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-339">Electricity</span></span></td>
<td><span data-ttu-id="9667c-340">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-340">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-341">500,00</span><span class="sxs-lookup"><span data-stu-id="9667c-341">500.00</span></span></td>
<td><span data-ttu-id="9667c-342">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-343">CC099</span><span class="sxs-lookup"><span data-stu-id="9667c-343">CC099</span></span></td>
<td><span data-ttu-id="9667c-344">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="9667c-344">Default cost center</span></span></td>
<td><span data-ttu-id="9667c-345">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-345">10001</span></span></td>
<td><span data-ttu-id="9667c-346">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-346">Electricity</span></span></td>
<td><span data-ttu-id="9667c-347">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-347">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-348">-9000,00</span><span class="sxs-lookup"><span data-stu-id="9667c-348">-9,000.00</span></span></td>
<td><span data-ttu-id="9667c-349">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-350">CC001</span><span class="sxs-lookup"><span data-stu-id="9667c-350">CC001</span></span></td>
<td><span data-ttu-id="9667c-351">HR</span><span class="sxs-lookup"><span data-stu-id="9667c-351">HR</span></span></td>
<td><span data-ttu-id="9667c-352">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-352">10001</span></span></td>
<td><span data-ttu-id="9667c-353">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-353">Electricity</span></span></td>
<td><span data-ttu-id="9667c-354">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-354">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="9667c-355">1,285.71</span></span></td>
<td><span data-ttu-id="9667c-356">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-357">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-357">CC002</span></span></td>
<td><span data-ttu-id="9667c-358">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-358">Finance</span></span></td>
<td><span data-ttu-id="9667c-359">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-359">10001</span></span></td>
<td><span data-ttu-id="9667c-360">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-360">Electricity</span></span></td>
<td><span data-ttu-id="9667c-361">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-361">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="9667c-362">7,714.29</span></span></td>
<td><span data-ttu-id="9667c-363">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-364">Detalizētu informāciju par izmaksu sadali un sadalījuma pamatiem skatiet sadaļā Izmaksu sadales politika un Sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="9667c-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="9667c-365">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)</span><span class="sxs-lookup"><span data-stu-id="9667c-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="9667c-366">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="9667c-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="9667c-367">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="9667c-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="9667c-368">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="9667c-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="9667c-369">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="9667c-369">Define the overhead rate</span></span>

<span data-ttu-id="9667c-370">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="9667c-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="9667c-371">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="9667c-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-372">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-372">Cost object</span></span></th>
<th><span data-ttu-id="9667c-373">Stundas</span><span class="sxs-lookup"><span data-stu-id="9667c-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="9667c-374">Proj 1</span></span></td>
<td><span data-ttu-id="9667c-375">1. projekts</span><span class="sxs-lookup"><span data-stu-id="9667c-375">Project 1</span></span></td>
<td><span data-ttu-id="9667c-376">3.</span><span class="sxs-lookup"><span data-stu-id="9667c-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="9667c-377">Proj 2</span></span></td>
<td><span data-ttu-id="9667c-378">2. projekts</span><span class="sxs-lookup"><span data-stu-id="9667c-378">Project 2</span></span></td>
<td><span data-ttu-id="9667c-379">1.</span><span class="sxs-lookup"><span data-stu-id="9667c-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-380">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="9667c-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-381">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-381">Cost object</span></span></th>
<th><span data-ttu-id="9667c-382">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="9667c-382">Cost element</span></span></th>
<th><span data-ttu-id="9667c-383">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="9667c-383">Cost behavior</span></span></th>
<th><span data-ttu-id="9667c-384">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="9667c-384">Units</span></span></th>
<th><span data-ttu-id="9667c-385">Likme</span><span class="sxs-lookup"><span data-stu-id="9667c-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-386">CC001</span><span class="sxs-lookup"><span data-stu-id="9667c-386">CC001</span></span></td>
<td><span data-ttu-id="9667c-387">HR</span><span class="sxs-lookup"><span data-stu-id="9667c-387">HR</span></span></td>
<td><span data-ttu-id="9667c-388">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-388">10001</span></span></td>
<td><span data-ttu-id="9667c-389">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-389">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-390">1</span><span class="sxs-lookup"><span data-stu-id="9667c-390">1</span></span></td>
<td><span data-ttu-id="9667c-391">10</span><span class="sxs-lookup"><span data-stu-id="9667c-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-392">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="9667c-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-393">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-393">Cost object</span></span></th>
<th><span data-ttu-id="9667c-394">Lielums</span><span class="sxs-lookup"><span data-stu-id="9667c-394">Magnitude</span></span></th>
<th><span data-ttu-id="9667c-395">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="9667c-395">Cost element</span></span></th>
<th><span data-ttu-id="9667c-396">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="9667c-396">Allocation factor</span></span></th>
<th><span data-ttu-id="9667c-397">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="9667c-398">Proj 1</span></span></td>
<td><span data-ttu-id="9667c-399">1. projekts</span><span class="sxs-lookup"><span data-stu-id="9667c-399">Project 1</span></span></td>
<td><span data-ttu-id="9667c-400">3.</span><span class="sxs-lookup"><span data-stu-id="9667c-400">3</span></span></td>
<td><span data-ttu-id="9667c-401">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-401">10001</span></span></td>
<td><span data-ttu-id="9667c-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="9667c-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="9667c-403">30,00</span><span class="sxs-lookup"><span data-stu-id="9667c-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="9667c-404">Proj 2</span></span></td>
<td><span data-ttu-id="9667c-405">2. projekts</span><span class="sxs-lookup"><span data-stu-id="9667c-405">Project 2</span></span></td>
<td><span data-ttu-id="9667c-406">1.</span><span class="sxs-lookup"><span data-stu-id="9667c-406">1</span></span></td>
<td><span data-ttu-id="9667c-407">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-407">10001</span></span></td>
<td><span data-ttu-id="9667c-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="9667c-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="9667c-409">10,00</span><span class="sxs-lookup"><span data-stu-id="9667c-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="9667c-410">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="9667c-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9667c-411">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="9667c-411">Journal</span></span></th>
<th><span data-ttu-id="9667c-412">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="9667c-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9667c-413">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="9667c-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9667c-414">Versija</span><span class="sxs-lookup"><span data-stu-id="9667c-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-415">00003</span><span class="sxs-lookup"><span data-stu-id="9667c-415">00003</span></span></td>
<td><span data-ttu-id="9667c-416">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="9667c-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="9667c-417">Finanšu</span><span class="sxs-lookup"><span data-stu-id="9667c-417">Fiscal</span></span></td>
<td><span data-ttu-id="9667c-418">2017</span><span class="sxs-lookup"><span data-stu-id="9667c-418">2017</span></span></td>
<td><span data-ttu-id="9667c-419">Periods 1</span><span class="sxs-lookup"><span data-stu-id="9667c-419">Period 1</span></span></td>
<td><span data-ttu-id="9667c-420">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="9667c-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="9667c-421">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="9667c-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9667c-422">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="9667c-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9667c-423">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-423">Cost object</span></span></th>
<th><span data-ttu-id="9667c-424">Lielums</span><span class="sxs-lookup"><span data-stu-id="9667c-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-425">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="9667c-426">Proj 1</span></span></td>
<td><span data-ttu-id="9667c-427">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="9667c-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="9667c-428">3,00</span><span class="sxs-lookup"><span data-stu-id="9667c-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-429">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="9667c-430">Proj 2</span></span></td>
<td><span data-ttu-id="9667c-431">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="9667c-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="9667c-432">1,00</span><span class="sxs-lookup"><span data-stu-id="9667c-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9667c-433">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="9667c-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-434">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9667c-435">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="9667c-435">Cost element</span></span></th>
<th><span data-ttu-id="9667c-436">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="9667c-436">Cost behavior</span></span></th>
<th><span data-ttu-id="9667c-437">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-437">Amount</span></span></th>
<th><span data-ttu-id="9667c-438">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="9667c-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="9667c-439">CC0001</span></span></td>
<td><span data-ttu-id="9667c-440">HR</span><span class="sxs-lookup"><span data-stu-id="9667c-440">HR</span></span></td>
<td><span data-ttu-id="9667c-441">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-441">10001</span></span></td>
<td><span data-ttu-id="9667c-442">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-442">Electricity</span></span></td>
<td><span data-ttu-id="9667c-443">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-443">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="9667c-444">-30.00</span></span></td>
<td><span data-ttu-id="9667c-445">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="9667c-446">Proj 1</span></span></td>
<td><span data-ttu-id="9667c-447">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="9667c-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="9667c-448">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-448">10001</span></span></td>
<td><span data-ttu-id="9667c-449">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-449">Electricity</span></span></td>
<td><span data-ttu-id="9667c-450">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-450">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-451">30,00</span><span class="sxs-lookup"><span data-stu-id="9667c-451">30.00</span></span></td>
<td><span data-ttu-id="9667c-452">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-453">CC001</span><span class="sxs-lookup"><span data-stu-id="9667c-453">CC001</span></span></td>
<td><span data-ttu-id="9667c-454">HR</span><span class="sxs-lookup"><span data-stu-id="9667c-454">HR</span></span></td>
<td><span data-ttu-id="9667c-455">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-455">10001</span></span></td>
<td><span data-ttu-id="9667c-456">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-456">Electricity</span></span></td>
<td><span data-ttu-id="9667c-457">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-457">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="9667c-458">-10.00</span></span></td>
<td><span data-ttu-id="9667c-459">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="9667c-460">Proj 2</span></span></td>
<td><span data-ttu-id="9667c-461">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="9667c-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="9667c-462">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-462">10001</span></span></td>
<td><span data-ttu-id="9667c-463">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-463">Electricity</span></span></td>
<td><span data-ttu-id="9667c-464">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-464">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-465">10,00</span><span class="sxs-lookup"><span data-stu-id="9667c-465">10.00</span></span></td>
<td><span data-ttu-id="9667c-466">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-467">Detalizētu informāciju par pieskaitāmo izmaksu likmes politiku skatiet sadaļā Pieskaitāmo izmaksu likmes politika un Sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="9667c-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="9667c-468">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)</span><span class="sxs-lookup"><span data-stu-id="9667c-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="9667c-469">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="9667c-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="9667c-470">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="9667c-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="9667c-471">Finance and Operations atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="9667c-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="9667c-472">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="9667c-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="9667c-473">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="9667c-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="9667c-474">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="9667c-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="9667c-475">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="9667c-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="9667c-476">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="9667c-476">The allocation order is controlled by the cost control unit.</span></span> <span data-ttu-id="9667c-477">[![Savstarpējā metode](./media/reciprocal-method.png)]</span><span class="sxs-lookup"><span data-stu-id="9667c-477">[![Reciprocal method](./media/reciprocal-method.png)]</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="9667c-478">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="9667c-478">Define the cost allocation</span></span>

<span data-ttu-id="9667c-479">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="9667c-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="9667c-480">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="9667c-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="9667c-481">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="9667c-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-482">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-482">Cost object</span></span></th>
<th><span data-ttu-id="9667c-483">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="9667c-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-484">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-484">CC002</span></span></td>
<td><span data-ttu-id="9667c-485">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-485">Finance</span></span></td>
<td><span data-ttu-id="9667c-486">35</span><span class="sxs-lookup"><span data-stu-id="9667c-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-487">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-487">CC003</span></span></td>
<td><span data-ttu-id="9667c-488">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-488">Assembly</span></span></td>
<td><span data-ttu-id="9667c-489">55</span><span class="sxs-lookup"><span data-stu-id="9667c-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-490">CC004</span><span class="sxs-lookup"><span data-stu-id="9667c-490">CC004</span></span></td>
<td><span data-ttu-id="9667c-491">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="9667c-491">Packaging</span></span></td>
<td><span data-ttu-id="9667c-492">10.</span><span class="sxs-lookup"><span data-stu-id="9667c-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-493">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="9667c-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="9667c-494">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="9667c-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-495">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-495">Cost object</span></span></th>
<th><span data-ttu-id="9667c-496">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="9667c-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-497">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-497">CC003</span></span></td>
<td><span data-ttu-id="9667c-498">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-498">Assembly</span></span></td>
<td><span data-ttu-id="9667c-499">65</span><span class="sxs-lookup"><span data-stu-id="9667c-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-500">CC004</span><span class="sxs-lookup"><span data-stu-id="9667c-500">CC004</span></span></td>
<td><span data-ttu-id="9667c-501">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="9667c-501">Packaging</span></span></td>
<td><span data-ttu-id="9667c-502">35</span><span class="sxs-lookup"><span data-stu-id="9667c-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-503">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="9667c-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="9667c-504">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="9667c-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-505">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-505">Cost object</span></span></th>
<th><span data-ttu-id="9667c-506">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="9667c-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9667c-507">Prod 1</span></span></td>
<td><span data-ttu-id="9667c-508">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-508">Product 1</span></span></td>
<td><span data-ttu-id="9667c-509">60</span><span class="sxs-lookup"><span data-stu-id="9667c-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9667c-510">Prod 2</span></span></td>
<td><span data-ttu-id="9667c-511">2. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-511">Product 2</span></span></td>
<td><span data-ttu-id="9667c-512">20</span><span class="sxs-lookup"><span data-stu-id="9667c-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-513">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="9667c-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="9667c-514">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="9667c-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-515">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-515">Cost object</span></span></th>
<th><span data-ttu-id="9667c-516">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="9667c-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9667c-517">Prod 1</span></span></td>
<td><span data-ttu-id="9667c-518">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-518">Product 1</span></span></td>
<td><span data-ttu-id="9667c-519">80</span><span class="sxs-lookup"><span data-stu-id="9667c-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9667c-520">Prod 2</span></span></td>
<td><span data-ttu-id="9667c-521">2. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-521">Product 2</span></span></td>
<td><span data-ttu-id="9667c-522">15.</span><span class="sxs-lookup"><span data-stu-id="9667c-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-523">**Piezīme.** Sistēmā Finance and Operations statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="9667c-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="9667c-524">Plašāku informāciju par statistisko mēru nodrošinātājiem skatiet sadaļā Statistisko mēru nodrošinātāja veidnes.</span><span class="sxs-lookup"><span data-stu-id="9667c-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="9667c-525">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.) Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="9667c-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-526">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-526">Cost object</span></span></th>
<th><span data-ttu-id="9667c-527">Lielums</span><span class="sxs-lookup"><span data-stu-id="9667c-527">Magnitude</span></span></th>
<th><span data-ttu-id="9667c-528">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="9667c-528">Allocation factor</span></span></th>
<th><span data-ttu-id="9667c-529">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-529">Amount</span></span></th>
<th><span data-ttu-id="9667c-530">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="9667c-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-531">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-531">CC002</span></span></td>
<td><span data-ttu-id="9667c-532">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-532">Finance</span></span></td>
<td><span data-ttu-id="9667c-533">35</span><span class="sxs-lookup"><span data-stu-id="9667c-533">35</span></span></td>
<td><span data-ttu-id="9667c-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="9667c-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="9667c-535">175.00</span><span class="sxs-lookup"><span data-stu-id="9667c-535">175.00</span></span></td>
<td><span data-ttu-id="9667c-536">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-537">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-537">CC003</span></span></td>
<td><span data-ttu-id="9667c-538">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-538">Assembly</span></span></td>
<td><span data-ttu-id="9667c-539">55</span><span class="sxs-lookup"><span data-stu-id="9667c-539">55</span></span></td>
<td><span data-ttu-id="9667c-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="9667c-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="9667c-541">275.00</span><span class="sxs-lookup"><span data-stu-id="9667c-541">275.00</span></span></td>
<td><span data-ttu-id="9667c-542">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-543">CC004</span><span class="sxs-lookup"><span data-stu-id="9667c-543">CC004</span></span></td>
<td><span data-ttu-id="9667c-544">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="9667c-544">Packaging</span></span></td>
<td><span data-ttu-id="9667c-545">10.</span><span class="sxs-lookup"><span data-stu-id="9667c-545">10</span></span></td>
<td><span data-ttu-id="9667c-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="9667c-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="9667c-547">50,00</span><span class="sxs-lookup"><span data-stu-id="9667c-547">50.00</span></span></td>
<td><span data-ttu-id="9667c-548">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-549">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-549">CC002</span></span></td>
<td><span data-ttu-id="9667c-550">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-550">Finance</span></span></td>
<td><span data-ttu-id="9667c-551">35</span><span class="sxs-lookup"><span data-stu-id="9667c-551">35</span></span></td>
<td><span data-ttu-id="9667c-552">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="9667c-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="9667c-553">436.00</span><span class="sxs-lookup"><span data-stu-id="9667c-553">436.00</span></span></td>
<td><span data-ttu-id="9667c-554">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-555">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-555">CC003</span></span></td>
<td><span data-ttu-id="9667c-556">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-556">Assembly</span></span></td>
<td><span data-ttu-id="9667c-557">55</span><span class="sxs-lookup"><span data-stu-id="9667c-557">55</span></span></td>
<td><span data-ttu-id="9667c-558">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="9667c-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="9667c-559">685.14</span><span class="sxs-lookup"><span data-stu-id="9667c-559">685.14</span></span></td>
<td><span data-ttu-id="9667c-560">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-561">CC004</span><span class="sxs-lookup"><span data-stu-id="9667c-561">CC004</span></span></td>
<td><span data-ttu-id="9667c-562">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="9667c-562">Packaging</span></span></td>
<td><span data-ttu-id="9667c-563">10.</span><span class="sxs-lookup"><span data-stu-id="9667c-563">10</span></span></td>
<td><span data-ttu-id="9667c-564">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="9667c-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="9667c-565">124.57</span><span class="sxs-lookup"><span data-stu-id="9667c-565">124.57</span></span></td>
<td><span data-ttu-id="9667c-566">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-567">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="9667c-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-568">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-568">Cost object</span></span></th>
<th><span data-ttu-id="9667c-569">Lielums</span><span class="sxs-lookup"><span data-stu-id="9667c-569">Magnitude</span></span></th>
<th><span data-ttu-id="9667c-570">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="9667c-570">Allocation factor</span></span></th>
<th><span data-ttu-id="9667c-571">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-571">Amount</span></span></th>
<th><span data-ttu-id="9667c-572">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="9667c-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-573">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-573">CC003</span></span></td>
<td><span data-ttu-id="9667c-574">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-574">Assembly</span></span></td>
<td><span data-ttu-id="9667c-575">65</span><span class="sxs-lookup"><span data-stu-id="9667c-575">65</span></span></td>
<td><span data-ttu-id="9667c-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="9667c-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="9667c-577">438.75</span><span class="sxs-lookup"><span data-stu-id="9667c-577">438.75</span></span></td>
<td><span data-ttu-id="9667c-578">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-579">CC004</span><span class="sxs-lookup"><span data-stu-id="9667c-579">CC004</span></span></td>
<td><span data-ttu-id="9667c-580">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="9667c-580">Packaging</span></span></td>
<td><span data-ttu-id="9667c-581">35</span><span class="sxs-lookup"><span data-stu-id="9667c-581">35</span></span></td>
<td><span data-ttu-id="9667c-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="9667c-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="9667c-583">236.25</span><span class="sxs-lookup"><span data-stu-id="9667c-583">236.25</span></span></td>
<td><span data-ttu-id="9667c-584">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-585">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-585">CC003</span></span></td>
<td><span data-ttu-id="9667c-586">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-586">Assembly</span></span></td>
<td><span data-ttu-id="9667c-587">65</span><span class="sxs-lookup"><span data-stu-id="9667c-587">65</span></span></td>
<td><span data-ttu-id="9667c-588">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="9667c-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="9667c-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="9667c-589">5,297.69</span></span></td>
<td><span data-ttu-id="9667c-590">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-591">CC004</span><span class="sxs-lookup"><span data-stu-id="9667c-591">CC004</span></span></td>
<td><span data-ttu-id="9667c-592">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="9667c-592">Packaging</span></span></td>
<td><span data-ttu-id="9667c-593">35</span><span class="sxs-lookup"><span data-stu-id="9667c-593">35</span></span></td>
<td><span data-ttu-id="9667c-594">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="9667c-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="9667c-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="9667c-595">2,852.60</span></span></td>
<td><span data-ttu-id="9667c-596">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-597">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="9667c-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-598">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-598">Cost object</span></span></th>
<th><span data-ttu-id="9667c-599">Lielums</span><span class="sxs-lookup"><span data-stu-id="9667c-599">Magnitude</span></span></th>
<th><span data-ttu-id="9667c-600">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="9667c-600">Allocation factor</span></span></th>
<th><span data-ttu-id="9667c-601">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-601">Amount</span></span></th>
<th><span data-ttu-id="9667c-602">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="9667c-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9667c-603">Prod 1</span></span></td>
<td><span data-ttu-id="9667c-604">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-604">Product 1</span></span></td>
<td><span data-ttu-id="9667c-605">60</span><span class="sxs-lookup"><span data-stu-id="9667c-605">60</span></span></td>
<td><span data-ttu-id="9667c-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="9667c-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="9667c-607">535.31</span><span class="sxs-lookup"><span data-stu-id="9667c-607">535.31</span></span></td>
<td><span data-ttu-id="9667c-608">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9667c-609">Prod 2</span></span></td>
<td><span data-ttu-id="9667c-610">2. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-610">Product 2</span></span></td>
<td><span data-ttu-id="9667c-611">20.</span><span class="sxs-lookup"><span data-stu-id="9667c-611">20</span></span></td>
<td><span data-ttu-id="9667c-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="9667c-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="9667c-613">178.44</span><span class="sxs-lookup"><span data-stu-id="9667c-613">178.44</span></span></td>
<td><span data-ttu-id="9667c-614">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9667c-615">Prod 1</span></span></td>
<td><span data-ttu-id="9667c-616">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-616">Product 1</span></span></td>
<td><span data-ttu-id="9667c-617">60</span><span class="sxs-lookup"><span data-stu-id="9667c-617">60</span></span></td>
<td><span data-ttu-id="9667c-618">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="9667c-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="9667c-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="9667c-619">4,487.12</span></span></td>
<td><span data-ttu-id="9667c-620">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9667c-621">Prod 2</span></span></td>
<td><span data-ttu-id="9667c-622">2. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-622">Product 2</span></span></td>
<td><span data-ttu-id="9667c-623">20.</span><span class="sxs-lookup"><span data-stu-id="9667c-623">20</span></span></td>
<td><span data-ttu-id="9667c-624">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="9667c-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="9667c-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="9667c-625">1,495.71</span></span></td>
<td><span data-ttu-id="9667c-626">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9667c-627">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="9667c-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-628">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-628">Cost object</span></span></th>
<th><span data-ttu-id="9667c-629">Lielums</span><span class="sxs-lookup"><span data-stu-id="9667c-629">Magnitude</span></span></th>
<th><span data-ttu-id="9667c-630">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="9667c-630">Allocation factor</span></span></th>
<th><span data-ttu-id="9667c-631">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-631">Amount</span></span></th>
<th><span data-ttu-id="9667c-632">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="9667c-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9667c-633">Prod 1</span></span></td>
<td><span data-ttu-id="9667c-634">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-634">Product 1</span></span></td>
<td><span data-ttu-id="9667c-635">80</span><span class="sxs-lookup"><span data-stu-id="9667c-635">80</span></span></td>
<td><span data-ttu-id="9667c-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="9667c-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="9667c-637">241.05</span><span class="sxs-lookup"><span data-stu-id="9667c-637">241.05</span></span></td>
<td><span data-ttu-id="9667c-638">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9667c-639">Prod 2</span></span></td>
<td><span data-ttu-id="9667c-640">2. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-640">Product 2</span></span></td>
<td><span data-ttu-id="9667c-641">15</span><span class="sxs-lookup"><span data-stu-id="9667c-641">15</span></span></td>
<td><span data-ttu-id="9667c-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="9667c-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="9667c-643">45.20</span><span class="sxs-lookup"><span data-stu-id="9667c-643">45.20</span></span></td>
<td><span data-ttu-id="9667c-644">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9667c-645">Prod 1</span></span></td>
<td><span data-ttu-id="9667c-646">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-646">Product 1</span></span></td>
<td><span data-ttu-id="9667c-647">80</span><span class="sxs-lookup"><span data-stu-id="9667c-647">80</span></span></td>
<td><span data-ttu-id="9667c-648">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="9667c-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="9667c-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="9667c-649">2,507.09</span></span></td>
<td><span data-ttu-id="9667c-650">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9667c-651">Prod 2</span></span></td>
<td><span data-ttu-id="9667c-652">2. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-652">Product 2</span></span></td>
<td><span data-ttu-id="9667c-653">15</span><span class="sxs-lookup"><span data-stu-id="9667c-653">15</span></span></td>
<td><span data-ttu-id="9667c-654">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="9667c-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="9667c-655">470.08</span><span class="sxs-lookup"><span data-stu-id="9667c-655">470.08</span></span></td>
<td><span data-ttu-id="9667c-656">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="9667c-657">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="9667c-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9667c-658">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="9667c-658">Journal</span></span></th>
<th><span data-ttu-id="9667c-659">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="9667c-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9667c-660">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="9667c-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9667c-661">Versija</span><span class="sxs-lookup"><span data-stu-id="9667c-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-662">00004</span><span class="sxs-lookup"><span data-stu-id="9667c-662">00004</span></span></td>
<td><span data-ttu-id="9667c-663">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="9667c-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="9667c-664">Finanšu</span><span class="sxs-lookup"><span data-stu-id="9667c-664">Fiscal</span></span></td>
<td><span data-ttu-id="9667c-665">2017</span><span class="sxs-lookup"><span data-stu-id="9667c-665">2017</span></span></td>
<td><span data-ttu-id="9667c-666">Periods 1</span><span class="sxs-lookup"><span data-stu-id="9667c-666">Period 1</span></span></td>
<td><span data-ttu-id="9667c-667">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="9667c-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="9667c-668">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="9667c-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9667c-669">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="9667c-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9667c-670">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9667c-671">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="9667c-671">Cost element</span></span></th>
<th><span data-ttu-id="9667c-672">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="9667c-672">Cost behavior</span></span></th>
<th><span data-ttu-id="9667c-673">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-674">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-675">CC001</span><span class="sxs-lookup"><span data-stu-id="9667c-675">CC001</span></span></td>
<td><span data-ttu-id="9667c-676">HR</span><span class="sxs-lookup"><span data-stu-id="9667c-676">HR</span></span></td>
<td><span data-ttu-id="9667c-677">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-677">10001</span></span></td>
<td><span data-ttu-id="9667c-678">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-678">Electricity</span></span></td>
<td><span data-ttu-id="9667c-679">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-679">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-680">500,00</span><span class="sxs-lookup"><span data-stu-id="9667c-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-681">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-682">CC001</span><span class="sxs-lookup"><span data-stu-id="9667c-682">CC001</span></span></td>
<td><span data-ttu-id="9667c-683">HR</span><span class="sxs-lookup"><span data-stu-id="9667c-683">HR</span></span></td>
<td><span data-ttu-id="9667c-684">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-684">10001</span></span></td>
<td><span data-ttu-id="9667c-685">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-685">Electricity</span></span></td>
<td><span data-ttu-id="9667c-686">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-686">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="9667c-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-688">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-689">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-689">CC002</span></span></td>
<td><span data-ttu-id="9667c-690">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-690">Finance</span></span></td>
<td><span data-ttu-id="9667c-691">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-691">10001</span></span></td>
<td><span data-ttu-id="9667c-692">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-692">Electricity</span></span></td>
<td><span data-ttu-id="9667c-693">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-693">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-694">675.00</span><span class="sxs-lookup"><span data-stu-id="9667c-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-695">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-696">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-696">CC002</span></span></td>
<td><span data-ttu-id="9667c-697">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-697">Finance</span></span></td>
<td><span data-ttu-id="9667c-698">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-698">10001</span></span></td>
<td><span data-ttu-id="9667c-699">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-699">Electricity</span></span></td>
<td><span data-ttu-id="9667c-700">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-700">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="9667c-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-702">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-703">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-703">CC003</span></span></td>
<td><span data-ttu-id="9667c-704">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-704">Assembly</span></span></td>
<td><span data-ttu-id="9667c-705">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-705">10001</span></span></td>
<td><span data-ttu-id="9667c-706">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-706">Electricity</span></span></td>
<td><span data-ttu-id="9667c-707">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-707">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-708">713.75</span><span class="sxs-lookup"><span data-stu-id="9667c-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-709">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-710">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-710">CC003</span></span></td>
<td><span data-ttu-id="9667c-711">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-711">Assembly</span></span></td>
<td><span data-ttu-id="9667c-712">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-712">10001</span></span></td>
<td><span data-ttu-id="9667c-713">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-713">Electricity</span></span></td>
<td><span data-ttu-id="9667c-714">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-714">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="9667c-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-716">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-717">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-717">CC003</span></span></td>
<td><span data-ttu-id="9667c-718">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="9667c-718">Packaging</span></span></td>
<td><span data-ttu-id="9667c-719">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-719">10001</span></span></td>
<td><span data-ttu-id="9667c-720">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-720">Electricity</span></span></td>
<td><span data-ttu-id="9667c-721">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-721">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-722">286.25</span><span class="sxs-lookup"><span data-stu-id="9667c-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-723">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-724">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-724">CC003</span></span></td>
<td><span data-ttu-id="9667c-725">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="9667c-725">Packaging</span></span></td>
<td><span data-ttu-id="9667c-726">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-726">10001</span></span></td>
<td><span data-ttu-id="9667c-727">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-727">Electricity</span></span></td>
<td><span data-ttu-id="9667c-728">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-728">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="9667c-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-730">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9667c-731">Prod 1</span></span></td>
<td><span data-ttu-id="9667c-732">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-732">Product 1</span></span></td>
<td><span data-ttu-id="9667c-733">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-733">10001</span></span></td>
<td><span data-ttu-id="9667c-734">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-734">Electricity</span></span></td>
<td><span data-ttu-id="9667c-735">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-735">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-736">776.36</span><span class="sxs-lookup"><span data-stu-id="9667c-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-737">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9667c-738">Prod 1</span></span></td>
<td><span data-ttu-id="9667c-739">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-739">Product 1</span></span></td>
<td><span data-ttu-id="9667c-740">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-740">10001</span></span></td>
<td><span data-ttu-id="9667c-741">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-741">Electricity</span></span></td>
<td><span data-ttu-id="9667c-742">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-742">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="9667c-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-744">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9667c-745">Prod 2</span></span></td>
<td><span data-ttu-id="9667c-746">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-746">Product 1</span></span></td>
<td><span data-ttu-id="9667c-747">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-747">10001</span></span></td>
<td><span data-ttu-id="9667c-748">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-748">Electricity</span></span></td>
<td><span data-ttu-id="9667c-749">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-749">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-750">223.64</span><span class="sxs-lookup"><span data-stu-id="9667c-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-751">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="9667c-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9667c-752">Prod 2</span></span></td>
<td><span data-ttu-id="9667c-753">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-753">Product 1</span></span></td>
<td><span data-ttu-id="9667c-754">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-754">10001</span></span></td>
<td><span data-ttu-id="9667c-755">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-755">Electricity</span></span></td>
<td><span data-ttu-id="9667c-756">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-756">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="9667c-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9667c-758">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="9667c-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9667c-759">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9667c-760">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="9667c-760">Cost element</span></span></th>
<th><span data-ttu-id="9667c-761">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="9667c-761">Cost behavior</span></span></th>
<th><span data-ttu-id="9667c-762">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-762">Amount</span></span></th>
<th><span data-ttu-id="9667c-763">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="9667c-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9667c-764">CC001</span><span class="sxs-lookup"><span data-stu-id="9667c-764">CC001</span></span></td>
<td><span data-ttu-id="9667c-765">HR</span><span class="sxs-lookup"><span data-stu-id="9667c-765">HR</span></span></td>
<td><span data-ttu-id="9667c-766">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-766">10001</span></span></td>
<td><span data-ttu-id="9667c-767">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-767">Electricity</span></span></td>
<td><span data-ttu-id="9667c-768">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-768">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="9667c-769">-500.00</span></span></td>
<td><span data-ttu-id="9667c-770">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-771">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-771">CC002</span></span></td>
<td><span data-ttu-id="9667c-772">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-772">Finance</span></span></td>
<td><span data-ttu-id="9667c-773">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-773">10001</span></span></td>
<td><span data-ttu-id="9667c-774">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-774">Electricity</span></span></td>
<td><span data-ttu-id="9667c-775">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-775">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-776">175.00</span><span class="sxs-lookup"><span data-stu-id="9667c-776">175.00</span></span></td>
<td><span data-ttu-id="9667c-777">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-778">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-778">CC003</span></span></td>
<td><span data-ttu-id="9667c-779">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-779">Assembly</span></span></td>
<td><span data-ttu-id="9667c-780">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-780">10001</span></span></td>
<td><span data-ttu-id="9667c-781">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-781">Electricity</span></span></td>
<td><span data-ttu-id="9667c-782">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-782">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-783">275.00</span><span class="sxs-lookup"><span data-stu-id="9667c-783">275.00</span></span></td>
<td><span data-ttu-id="9667c-784">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-785">CC004</span><span class="sxs-lookup"><span data-stu-id="9667c-785">CC004</span></span></td>
<td><span data-ttu-id="9667c-786">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="9667c-786">Packaging</span></span></td>
<td><span data-ttu-id="9667c-787">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-787">10001</span></span></td>
<td><span data-ttu-id="9667c-788">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-788">Electricity</span></span></td>
<td><span data-ttu-id="9667c-789">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-789">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-790">50,00</span><span class="sxs-lookup"><span data-stu-id="9667c-790">50,00</span></span></td>
<td><span data-ttu-id="9667c-791">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-792">CC001</span><span class="sxs-lookup"><span data-stu-id="9667c-792">CC001</span></span></td>
<td><span data-ttu-id="9667c-793">HR</span><span class="sxs-lookup"><span data-stu-id="9667c-793">HR</span></span></td>
<td><span data-ttu-id="9667c-794">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-794">10001</span></span></td>
<td><span data-ttu-id="9667c-795">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-795">Electricity</span></span></td>
<td><span data-ttu-id="9667c-796">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-796">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-797">-1245,71</span><span class="sxs-lookup"><span data-stu-id="9667c-797">-1,245.71</span></span></td>
<td><span data-ttu-id="9667c-798">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-799">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-799">CC002</span></span></td>
<td><span data-ttu-id="9667c-800">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-800">Finance</span></span></td>
<td><span data-ttu-id="9667c-801">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-801">10001</span></span></td>
<td><span data-ttu-id="9667c-802">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-802">Electricity</span></span></td>
<td><span data-ttu-id="9667c-803">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-803">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-804">436.00</span><span class="sxs-lookup"><span data-stu-id="9667c-804">436.00</span></span></td>
<td><span data-ttu-id="9667c-805">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-806">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-806">CC003</span></span></td>
<td><span data-ttu-id="9667c-807">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-807">Assembly</span></span></td>
<td><span data-ttu-id="9667c-808">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-808">10001</span></span></td>
<td><span data-ttu-id="9667c-809">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-809">Electricity</span></span></td>
<td><span data-ttu-id="9667c-810">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-810">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-811">685.14</span><span class="sxs-lookup"><span data-stu-id="9667c-811">685.14</span></span></td>
<td><span data-ttu-id="9667c-812">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-813">CC004</span><span class="sxs-lookup"><span data-stu-id="9667c-813">CC004</span></span></td>
<td><span data-ttu-id="9667c-814">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="9667c-814">Packaging</span></span></td>
<td><span data-ttu-id="9667c-815">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-815">10001</span></span></td>
<td><span data-ttu-id="9667c-816">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-816">Electricity</span></span></td>
<td><span data-ttu-id="9667c-817">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-817">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-818">124.57</span><span class="sxs-lookup"><span data-stu-id="9667c-818">124.57</span></span></td>
<td><span data-ttu-id="9667c-819">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-820">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-820">CC002</span></span></td>
<td><span data-ttu-id="9667c-821">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-821">Finance</span></span></td>
<td><span data-ttu-id="9667c-822">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-822">10001</span></span></td>
<td><span data-ttu-id="9667c-823">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-823">Electricity</span></span></td>
<td><span data-ttu-id="9667c-824">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-824">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="9667c-825">-675.00</span></span></td>
<td><span data-ttu-id="9667c-826">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-827">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-827">CC003</span></span></td>
<td><span data-ttu-id="9667c-828">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-828">Assembly</span></span></td>
<td><span data-ttu-id="9667c-829">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-829">10001</span></span></td>
<td><span data-ttu-id="9667c-830">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-830">Electricity</span></span></td>
<td><span data-ttu-id="9667c-831">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-831">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-832">438.75</span><span class="sxs-lookup"><span data-stu-id="9667c-832">438.75</span></span></td>
<td><span data-ttu-id="9667c-833">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-834">CC004</span><span class="sxs-lookup"><span data-stu-id="9667c-834">CC004</span></span></td>
<td><span data-ttu-id="9667c-835">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="9667c-835">Packaging</span></span></td>
<td><span data-ttu-id="9667c-836">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-836">10001</span></span></td>
<td><span data-ttu-id="9667c-837">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-837">Electricity</span></span></td>
<td><span data-ttu-id="9667c-838">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-838">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-839">236.25</span><span class="sxs-lookup"><span data-stu-id="9667c-839">236.25</span></span></td>
<td><span data-ttu-id="9667c-840">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-841">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-841">CC002</span></span></td>
<td><span data-ttu-id="9667c-842">Finanses</span><span class="sxs-lookup"><span data-stu-id="9667c-842">Finance</span></span></td>
<td><span data-ttu-id="9667c-843">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-843">10001</span></span></td>
<td><span data-ttu-id="9667c-844">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-844">Electricity</span></span></td>
<td><span data-ttu-id="9667c-845">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-845">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-846">-8150,29</span><span class="sxs-lookup"><span data-stu-id="9667c-846">-8,150.29</span></span></td>
<td><span data-ttu-id="9667c-847">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-848">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-848">CC003</span></span></td>
<td><span data-ttu-id="9667c-849">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-849">Assembly</span></span></td>
<td><span data-ttu-id="9667c-850">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-850">10001</span></span></td>
<td><span data-ttu-id="9667c-851">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-851">Electricity</span></span></td>
<td><span data-ttu-id="9667c-852">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-852">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="9667c-853">5,297.69</span></span></td>
<td><span data-ttu-id="9667c-854">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-855">CC004</span><span class="sxs-lookup"><span data-stu-id="9667c-855">CC004</span></span></td>
<td><span data-ttu-id="9667c-856">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="9667c-856">Packaging</span></span></td>
<td><span data-ttu-id="9667c-857">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-857">10001</span></span></td>
<td><span data-ttu-id="9667c-858">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-858">Electricity</span></span></td>
<td><span data-ttu-id="9667c-859">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-859">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="9667c-860">2,852.60</span></span></td>
<td><span data-ttu-id="9667c-861">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-862">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-862">CC003</span></span></td>
<td><span data-ttu-id="9667c-863">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-863">Assembly</span></span></td>
<td><span data-ttu-id="9667c-864">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-864">10001</span></span></td>
<td><span data-ttu-id="9667c-865">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-865">Electricity</span></span></td>
<td><span data-ttu-id="9667c-866">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-866">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="9667c-867">-713.75</span></span></td>
<td><span data-ttu-id="9667c-868">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9667c-869">Prod 1</span></span></td>
<td><span data-ttu-id="9667c-870">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-870">Product 1</span></span></td>
<td><span data-ttu-id="9667c-871">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-871">10001</span></span></td>
<td><span data-ttu-id="9667c-872">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-872">Electricity</span></span></td>
<td><span data-ttu-id="9667c-873">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-873">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-874">535.31</span><span class="sxs-lookup"><span data-stu-id="9667c-874">535.31</span></span></td>
<td><span data-ttu-id="9667c-875">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9667c-876">Prod 2</span></span></td>
<td><span data-ttu-id="9667c-877">2. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-877">Product 2</span></span></td>
<td><span data-ttu-id="9667c-878">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-878">10001</span></span></td>
<td><span data-ttu-id="9667c-879">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-879">Electricity</span></span></td>
<td><span data-ttu-id="9667c-880">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-880">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-881">178.44</span><span class="sxs-lookup"><span data-stu-id="9667c-881">178.44</span></span></td>
<td><span data-ttu-id="9667c-882">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-883">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-883">CC003</span></span></td>
<td><span data-ttu-id="9667c-884">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-884">Assembly</span></span></td>
<td><span data-ttu-id="9667c-885">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-885">10001</span></span></td>
<td><span data-ttu-id="9667c-886">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-886">Electricity</span></span></td>
<td><span data-ttu-id="9667c-887">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-887">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-888">-5982,83</span><span class="sxs-lookup"><span data-stu-id="9667c-888">-5,982.83</span></span></td>
<td><span data-ttu-id="9667c-889">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9667c-890">Prod 1</span></span></td>
<td><span data-ttu-id="9667c-891">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-891">Product 1</span></span></td>
<td><span data-ttu-id="9667c-892">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-892">10001</span></span></td>
<td><span data-ttu-id="9667c-893">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-893">Electricity</span></span></td>
<td><span data-ttu-id="9667c-894">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-894">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="9667c-895">4,487.12</span></span></td>
<td><span data-ttu-id="9667c-896">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9667c-897">Prod 2</span></span></td>
<td><span data-ttu-id="9667c-898">2. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-898">Product 2</span></span></td>
<td><span data-ttu-id="9667c-899">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-899">10001</span></span></td>
<td><span data-ttu-id="9667c-900">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-900">Electricity</span></span></td>
<td><span data-ttu-id="9667c-901">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-901">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="9667c-902">1,495.71</span></span></td>
<td><span data-ttu-id="9667c-903">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-904">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-904">CC003</span></span></td>
<td><span data-ttu-id="9667c-905">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-905">Assembly</span></span></td>
<td><span data-ttu-id="9667c-906">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-906">10001</span></span></td>
<td><span data-ttu-id="9667c-907">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-907">Electricity</span></span></td>
<td><span data-ttu-id="9667c-908">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-908">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="9667c-909">-286.25</span></span></td>
<td><span data-ttu-id="9667c-910">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9667c-911">Prod 1</span></span></td>
<td><span data-ttu-id="9667c-912">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-912">Product 1</span></span></td>
<td><span data-ttu-id="9667c-913">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-913">10001</span></span></td>
<td><span data-ttu-id="9667c-914">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-914">Electricity</span></span></td>
<td><span data-ttu-id="9667c-915">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-915">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-916">241.05</span><span class="sxs-lookup"><span data-stu-id="9667c-916">241.05</span></span></td>
<td><span data-ttu-id="9667c-917">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9667c-918">Prod 2</span></span></td>
<td><span data-ttu-id="9667c-919">2. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-919">Product 2</span></span></td>
<td><span data-ttu-id="9667c-920">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-920">10001</span></span></td>
<td><span data-ttu-id="9667c-921">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-921">Electricity</span></span></td>
<td><span data-ttu-id="9667c-922">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-922">Fixed cost</span></span></td>
<td><span data-ttu-id="9667c-923">45.20</span><span class="sxs-lookup"><span data-stu-id="9667c-923">45.20</span></span></td>
<td><span data-ttu-id="9667c-924">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-925">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-925">CC003</span></span></td>
<td><span data-ttu-id="9667c-926">Montāža</span><span class="sxs-lookup"><span data-stu-id="9667c-926">Assembly</span></span></td>
<td><span data-ttu-id="9667c-927">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-927">10001</span></span></td>
<td><span data-ttu-id="9667c-928">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-928">Electricity</span></span></td>
<td><span data-ttu-id="9667c-929">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-929">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-930">-2977,17</span><span class="sxs-lookup"><span data-stu-id="9667c-930">-2,977.17</span></span></td>
<td><span data-ttu-id="9667c-931">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9667c-932">Prod 1</span></span></td>
<td><span data-ttu-id="9667c-933">1. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-933">Product 1</span></span></td>
<td><span data-ttu-id="9667c-934">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-934">10001</span></span></td>
<td><span data-ttu-id="9667c-935">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-935">Electricity</span></span></td>
<td><span data-ttu-id="9667c-936">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-936">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="9667c-937">2,507.09</span></span></td>
<td><span data-ttu-id="9667c-938">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9667c-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9667c-939">Prod 2</span></span></td>
<td><span data-ttu-id="9667c-940">2. prece</span><span class="sxs-lookup"><span data-stu-id="9667c-940">Product 2</span></span></td>
<td><span data-ttu-id="9667c-941">10001</span><span class="sxs-lookup"><span data-stu-id="9667c-941">10001</span></span></td>
<td><span data-ttu-id="9667c-942">Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-942">Electricity</span></span></td>
<td><span data-ttu-id="9667c-943">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-943">Variable cost</span></span></td>
<td><span data-ttu-id="9667c-944">470.08</span><span class="sxs-lookup"><span data-stu-id="9667c-944">470.08</span></span></td>
<td><span data-ttu-id="9667c-945">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="9667c-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="9667c-946">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="9667c-946">Conclusion</span></span>
<span data-ttu-id="9667c-947">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="9667c-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="9667c-948">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="9667c-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="9667c-949">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="9667c-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="9667c-950">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="9667c-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="9667c-951">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="9667c-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="9667c-952">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="9667c-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="9667c-953">Summa</span><span class="sxs-lookup"><span data-stu-id="9667c-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9667c-954">CC099</span><span class="sxs-lookup"><span data-stu-id="9667c-954">CC099</span></span></th>
<th><span data-ttu-id="9667c-955">CC001</span><span class="sxs-lookup"><span data-stu-id="9667c-955">CC001</span></span></th>
<th><span data-ttu-id="9667c-956">CC002</span><span class="sxs-lookup"><span data-stu-id="9667c-956">CC002</span></span></th>
<th><span data-ttu-id="9667c-957">CC003</span><span class="sxs-lookup"><span data-stu-id="9667c-957">CC003</span></span></th>
<th><span data-ttu-id="9667c-958">CC004</span><span class="sxs-lookup"><span data-stu-id="9667c-958">CC004</span></span></th>
<th><span data-ttu-id="9667c-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="9667c-959">Proj 1</span></span></th>
<th><span data-ttu-id="9667c-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="9667c-960">Proj 2</span></span></th>
<th><span data-ttu-id="9667c-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9667c-961">Prod 1</span></span></th>
<th><span data-ttu-id="9667c-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9667c-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="9667c-963">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="9667c-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="9667c-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="9667c-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="9667c-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="9667c-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="9667c-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="9667c-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="9667c-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="9667c-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="9667c-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="9667c-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="9667c-973">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="9667c-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-974">0,00</span><span class="sxs-lookup"><span data-stu-id="9667c-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="9667c-975">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-976">0,00</span><span class="sxs-lookup"><span data-stu-id="9667c-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-977">0,00</span><span class="sxs-lookup"><span data-stu-id="9667c-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-978">0,00</span><span class="sxs-lookup"><span data-stu-id="9667c-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-979">0,00</span><span class="sxs-lookup"><span data-stu-id="9667c-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-980">0,00</span><span class="sxs-lookup"><span data-stu-id="9667c-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="9667c-981">776.36</span><span class="sxs-lookup"><span data-stu-id="9667c-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-982">223.64</span><span class="sxs-lookup"><span data-stu-id="9667c-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="9667c-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="9667c-984">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="9667c-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-985">000</span><span class="sxs-lookup"><span data-stu-id="9667c-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-986">0,00</span><span class="sxs-lookup"><span data-stu-id="9667c-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-987">0,00</span><span class="sxs-lookup"><span data-stu-id="9667c-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-988">0,00</span><span class="sxs-lookup"><span data-stu-id="9667c-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-989">0,00</span><span class="sxs-lookup"><span data-stu-id="9667c-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-990">30,00</span><span class="sxs-lookup"><span data-stu-id="9667c-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-991">10,00</span><span class="sxs-lookup"><span data-stu-id="9667c-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="9667c-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="9667c-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9667c-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="9667c-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9667c-995">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="9667c-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="9667c-996">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="9667c-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="9667c-997">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="9667c-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="9667c-998">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="9667c-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="9667c-999">Papildinformāciju skatiet sadaļā Izmaksu apkopošanas politika.</span><span class="sxs-lookup"><span data-stu-id="9667c-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="9667c-1000">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)</span><span class="sxs-lookup"><span data-stu-id="9667c-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




