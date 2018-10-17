---
title: "Pieskaitāmo izmaksu aprēķins"
description: "Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai."
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: lv-lv
ms.lasthandoff: 10/05/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="98818-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="98818-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98818-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="98818-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="98818-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="98818-105">Term definition</span></span>
---------------

<span data-ttu-id="98818-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="98818-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="98818-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="98818-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="98818-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="98818-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="98818-109">Īre</span><span class="sxs-lookup"><span data-stu-id="98818-109">Rent</span></span>
-   <span data-ttu-id="98818-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-110">Electricity</span></span>
-   <span data-ttu-id="98818-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="98818-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="98818-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="98818-112">Overhead calculation overview</span></span>
<span data-ttu-id="98818-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="98818-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="98818-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="98818-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="98818-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="98818-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="98818-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="98818-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="98818-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="98818-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="98818-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="98818-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="98818-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="98818-119">Version type</span></span>
-   <span data-ttu-id="98818-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="98818-120">Date and time</span></span>
-   <span data-ttu-id="98818-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="98818-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="98818-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="98818-122">Fiscal year</span></span>
-   <span data-ttu-id="98818-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="98818-123">Fiscal period</span></span>

<span data-ttu-id="98818-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="98818-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="98818-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="98818-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="98818-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="98818-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="98818-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="98818-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="98818-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="98818-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="98818-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="98818-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="98818-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="98818-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="98818-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="98818-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="98818-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="98818-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="98818-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="98818-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="98818-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="98818-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="98818-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="98818-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="98818-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="98818-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="98818-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="98818-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="98818-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="98818-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="98818-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="98818-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="98818-140">Main account</span></span></th>
<th><span data-ttu-id="98818-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="98818-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="98818-143">CC099</span><span class="sxs-lookup"><span data-stu-id="98818-143">CC099</span></span></td>
<td><span data-ttu-id="98818-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="98818-144">Default cost center</span></span></td>
<td><span data-ttu-id="98818-145">10001</span><span class="sxs-lookup"><span data-stu-id="98818-145">10001</span></span></td>
<td><span data-ttu-id="98818-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-146">Electricity</span></span></td>
<td><span data-ttu-id="98818-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="98818-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="98818-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="98818-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="98818-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="98818-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="98818-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="98818-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="98818-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="98818-151">Define the cost behavior rule</span></span>

<span data-ttu-id="98818-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="98818-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="98818-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="98818-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="98818-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="98818-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="98818-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="98818-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="98818-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="98818-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="98818-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="98818-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="98818-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="98818-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="98818-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="98818-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="98818-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="98818-160">Journal</span></span></th>
<th><span data-ttu-id="98818-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="98818-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="98818-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="98818-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="98818-163">Versija</span><span class="sxs-lookup"><span data-stu-id="98818-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-164">00001</span><span class="sxs-lookup"><span data-stu-id="98818-164">00001</span></span></td>
<td><span data-ttu-id="98818-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="98818-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="98818-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="98818-166">Fiscal</span></span></td>
<td><span data-ttu-id="98818-167">2017</span><span class="sxs-lookup"><span data-stu-id="98818-167">2017</span></span></td>
<td><span data-ttu-id="98818-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="98818-168">Period 1</span></span></td>
<td><span data-ttu-id="98818-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="98818-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="98818-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="98818-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="98818-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="98818-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="98818-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="98818-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="98818-173">Cost element</span></span></th>
<th><span data-ttu-id="98818-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="98818-174">Cost behavior</span></span></th>
<th><span data-ttu-id="98818-175">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="98818-177">CC099</span><span class="sxs-lookup"><span data-stu-id="98818-177">CC099</span></span></td>
<td><span data-ttu-id="98818-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="98818-178">Default cost center</span></span></td>
<td><span data-ttu-id="98818-179">10001</span><span class="sxs-lookup"><span data-stu-id="98818-179">10001</span></span></td>
<td><span data-ttu-id="98818-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-180">Electricity</span></span></td>
<td><span data-ttu-id="98818-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="98818-181">Unclassified</span></span></td>
<td><span data-ttu-id="98818-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="98818-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="98818-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="98818-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="98818-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="98818-185">Cost element</span></span></th>
<th><span data-ttu-id="98818-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="98818-186">Cost behavior</span></span></th>
<th><span data-ttu-id="98818-187">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-187">Amount</span></span></th>
<th><span data-ttu-id="98818-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="98818-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-189">CC099</span><span class="sxs-lookup"><span data-stu-id="98818-189">CC099</span></span></td>
<td><span data-ttu-id="98818-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="98818-190">Default cost center</span></span></td>
<td><span data-ttu-id="98818-191">10001</span><span class="sxs-lookup"><span data-stu-id="98818-191">10001</span></span></td>
<td><span data-ttu-id="98818-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-192">Electricity</span></span></td>
<td><span data-ttu-id="98818-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="98818-193">Unclassified</span></span></td>
<td><span data-ttu-id="98818-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="98818-194">10,000.00</span></span></td>
<td><span data-ttu-id="98818-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-196">CC099</span><span class="sxs-lookup"><span data-stu-id="98818-196">CC099</span></span></td>
<td><span data-ttu-id="98818-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="98818-197">Default cost center</span></span></td>
<td><span data-ttu-id="98818-198">10001</span><span class="sxs-lookup"><span data-stu-id="98818-198">10001</span></span></td>
<td><span data-ttu-id="98818-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-199">Electricity</span></span></td>
<td><span data-ttu-id="98818-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="98818-200">Unclassified</span></span></td>
<td><span data-ttu-id="98818-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="98818-201">-10,000.00</span></span></td>
<td><span data-ttu-id="98818-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-203">CC099</span><span class="sxs-lookup"><span data-stu-id="98818-203">CC099</span></span></td>
<td><span data-ttu-id="98818-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="98818-204">Default cost center</span></span></td>
<td><span data-ttu-id="98818-205">10001</span><span class="sxs-lookup"><span data-stu-id="98818-205">10001</span></span></td>
<td><span data-ttu-id="98818-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-206">Electricity</span></span></td>
<td><span data-ttu-id="98818-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-207">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="98818-208">1,000.00</span></span></td>
<td><span data-ttu-id="98818-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-210">CC099</span><span class="sxs-lookup"><span data-stu-id="98818-210">CC099</span></span></td>
<td><span data-ttu-id="98818-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="98818-211">Default cost center</span></span></td>
<td><span data-ttu-id="98818-212">10001</span><span class="sxs-lookup"><span data-stu-id="98818-212">10001</span></span></td>
<td><span data-ttu-id="98818-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-213">Electricity</span></span></td>
<td><span data-ttu-id="98818-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-214">Variable cost</span></span></td>
<td><span data-ttu-id="98818-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="98818-215">9,000.00</span></span></td>
<td><span data-ttu-id="98818-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98818-217">Sīkāku informāciju skatiet šeit: [Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="98818-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="98818-218">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="98818-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="98818-219">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="98818-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="98818-220">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="98818-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="98818-221">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="98818-221">Define the cost distribution rule</span></span>

<span data-ttu-id="98818-222">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="98818-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="98818-223">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="98818-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="98818-224">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="98818-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="98818-225">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="98818-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="98818-226">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="98818-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="98818-227">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="98818-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-228">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-228">Cost object</span></span></th>
<th><span data-ttu-id="98818-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="98818-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-230">CC001</span><span class="sxs-lookup"><span data-stu-id="98818-230">CC001</span></span></td>
<td><span data-ttu-id="98818-231">HR</span><span class="sxs-lookup"><span data-stu-id="98818-231">HR</span></span></td>
<td><span data-ttu-id="98818-232">1000</span><span class="sxs-lookup"><span data-stu-id="98818-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-233">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-233">CC002</span></span></td>
<td><span data-ttu-id="98818-234">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-234">Finance</span></span></td>
<td><span data-ttu-id="98818-235">6,000</span><span class="sxs-lookup"><span data-stu-id="98818-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-236">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-236">CC003</span></span></td>
<td><span data-ttu-id="98818-237">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-237">Assembly</span></span></td>
<td><span data-ttu-id="98818-238">0</span><span class="sxs-lookup"><span data-stu-id="98818-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98818-239">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="98818-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-240">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-240">Cost object</span></span></th>
<th><span data-ttu-id="98818-241">Lielums</span><span class="sxs-lookup"><span data-stu-id="98818-241">Magnitude</span></span></th>
<th><span data-ttu-id="98818-242">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="98818-242">Allocation factor</span></span></th>
<th><span data-ttu-id="98818-243">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-244">CC001</span><span class="sxs-lookup"><span data-stu-id="98818-244">CC001</span></span></td>
<td><span data-ttu-id="98818-245">HR</span><span class="sxs-lookup"><span data-stu-id="98818-245">HR</span></span></td>
<td><span data-ttu-id="98818-246">1000</span><span class="sxs-lookup"><span data-stu-id="98818-246">1,000</span></span></td>
<td><span data-ttu-id="98818-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="98818-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="98818-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="98818-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-249">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-249">CC002</span></span></td>
<td><span data-ttu-id="98818-250">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-250">Finance</span></span></td>
<td><span data-ttu-id="98818-251">6,000</span><span class="sxs-lookup"><span data-stu-id="98818-251">6,000</span></span></td>
<td><span data-ttu-id="98818-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="98818-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="98818-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="98818-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-254">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-254">CC003</span></span></td>
<td><span data-ttu-id="98818-255">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-255">Assembly</span></span></td>
<td><span data-ttu-id="98818-256">0</span><span class="sxs-lookup"><span data-stu-id="98818-256">0</span></span></td>
<td><span data-ttu-id="98818-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="98818-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="98818-258">0,00</span><span class="sxs-lookup"><span data-stu-id="98818-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98818-259">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="98818-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="98818-260">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="98818-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-261">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-261">Cost object</span></span></th>
<th><span data-ttu-id="98818-262">Formula</span><span class="sxs-lookup"><span data-stu-id="98818-262">Formula</span></span></th>
<th><span data-ttu-id="98818-263">Lielums</span><span class="sxs-lookup"><span data-stu-id="98818-263">Magnitude</span></span></th>
<th><span data-ttu-id="98818-264">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="98818-264">Allocation factor</span></span></th>
<th><span data-ttu-id="98818-265">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-266">CC001</span><span class="sxs-lookup"><span data-stu-id="98818-266">CC001</span></span></td>
<td><span data-ttu-id="98818-267">HR</span><span class="sxs-lookup"><span data-stu-id="98818-267">HR</span></span></td>
<td><span data-ttu-id="98818-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="98818-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="98818-269">1.</span><span class="sxs-lookup"><span data-stu-id="98818-269">1</span></span></td>
<td><span data-ttu-id="98818-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="98818-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="98818-271">500,00</span><span class="sxs-lookup"><span data-stu-id="98818-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-272">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-272">CC002</span></span></td>
<td><span data-ttu-id="98818-273">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-273">Finance</span></span></td>
<td><span data-ttu-id="98818-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="98818-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="98818-275">1.</span><span class="sxs-lookup"><span data-stu-id="98818-275">1</span></span></td>
<td><span data-ttu-id="98818-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="98818-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="98818-277">500,00</span><span class="sxs-lookup"><span data-stu-id="98818-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-278">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-278">CC003</span></span></td>
<td><span data-ttu-id="98818-279">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-279">Assembly</span></span></td>
<td><span data-ttu-id="98818-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="98818-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="98818-281">0</span><span class="sxs-lookup"><span data-stu-id="98818-281">0</span></span></td>
<td><span data-ttu-id="98818-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="98818-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="98818-283">0,00</span><span class="sxs-lookup"><span data-stu-id="98818-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="98818-284">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="98818-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="98818-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="98818-285">Journal</span></span></th>
<th><span data-ttu-id="98818-286">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="98818-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="98818-287">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="98818-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="98818-288">Versija</span><span class="sxs-lookup"><span data-stu-id="98818-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-289">00002</span><span class="sxs-lookup"><span data-stu-id="98818-289">00002</span></span></td>
<td><span data-ttu-id="98818-290">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="98818-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="98818-291">Finanšu</span><span class="sxs-lookup"><span data-stu-id="98818-291">Fiscal</span></span></td>
<td><span data-ttu-id="98818-292">2017</span><span class="sxs-lookup"><span data-stu-id="98818-292">2017</span></span></td>
<td><span data-ttu-id="98818-293">Periods 1</span><span class="sxs-lookup"><span data-stu-id="98818-293">Period 1</span></span></td>
<td><span data-ttu-id="98818-294">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="98818-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="98818-295">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="98818-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="98818-296">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="98818-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="98818-297">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="98818-298">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="98818-298">Cost element</span></span></th>
<th><span data-ttu-id="98818-299">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="98818-299">Cost behavior</span></span></th>
<th><span data-ttu-id="98818-300">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-301">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-302">CC099</span><span class="sxs-lookup"><span data-stu-id="98818-302">CC099</span></span></td>
<td><span data-ttu-id="98818-303">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="98818-303">Default cost center</span></span></td>
<td><span data-ttu-id="98818-304">10001</span><span class="sxs-lookup"><span data-stu-id="98818-304">10001</span></span></td>
<td><span data-ttu-id="98818-305">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-305">Electricity</span></span></td>
<td><span data-ttu-id="98818-306">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-306">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="98818-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-308">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-309">CC099</span><span class="sxs-lookup"><span data-stu-id="98818-309">CC099</span></span></td>
<td><span data-ttu-id="98818-310">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="98818-310">Default cost center</span></span></td>
<td><span data-ttu-id="98818-311">10001</span><span class="sxs-lookup"><span data-stu-id="98818-311">10001</span></span></td>
<td><span data-ttu-id="98818-312">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-312">Electricity</span></span></td>
<td><span data-ttu-id="98818-313">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-313">Variable cost</span></span></td>
<td><span data-ttu-id="98818-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="98818-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="98818-315">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="98818-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-316">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="98818-317">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="98818-317">Cost element</span></span></th>
<th><span data-ttu-id="98818-318">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="98818-318">Cost behavior</span></span></th>
<th><span data-ttu-id="98818-319">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-319">Amount</span></span></th>
<th><span data-ttu-id="98818-320">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="98818-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-321">CC099</span><span class="sxs-lookup"><span data-stu-id="98818-321">CC099</span></span></td>
<td><span data-ttu-id="98818-322">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="98818-322">Default cost center</span></span></td>
<td><span data-ttu-id="98818-323">10001</span><span class="sxs-lookup"><span data-stu-id="98818-323">10001</span></span></td>
<td><span data-ttu-id="98818-324">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-324">Electricity</span></span></td>
<td><span data-ttu-id="98818-325">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-325">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-326">-1000,00</span><span class="sxs-lookup"><span data-stu-id="98818-326">-1,000.00</span></span></td>
<td><span data-ttu-id="98818-327">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-328">CC001</span><span class="sxs-lookup"><span data-stu-id="98818-328">CC001</span></span></td>
<td><span data-ttu-id="98818-329">HR</span><span class="sxs-lookup"><span data-stu-id="98818-329">HR</span></span></td>
<td><span data-ttu-id="98818-330">10001</span><span class="sxs-lookup"><span data-stu-id="98818-330">10001</span></span></td>
<td><span data-ttu-id="98818-331">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-331">Electricity</span></span></td>
<td><span data-ttu-id="98818-332">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-332">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-333">500,00</span><span class="sxs-lookup"><span data-stu-id="98818-333">500.00</span></span></td>
<td><span data-ttu-id="98818-334">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-335">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-335">CC002</span></span></td>
<td><span data-ttu-id="98818-336">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-336">Finance</span></span></td>
<td><span data-ttu-id="98818-337">10001</span><span class="sxs-lookup"><span data-stu-id="98818-337">10001</span></span></td>
<td><span data-ttu-id="98818-338">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-338">Electricity</span></span></td>
<td><span data-ttu-id="98818-339">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-339">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-340">500,00</span><span class="sxs-lookup"><span data-stu-id="98818-340">500.00</span></span></td>
<td><span data-ttu-id="98818-341">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-342">CC099</span><span class="sxs-lookup"><span data-stu-id="98818-342">CC099</span></span></td>
<td><span data-ttu-id="98818-343">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="98818-343">Default cost center</span></span></td>
<td><span data-ttu-id="98818-344">10001</span><span class="sxs-lookup"><span data-stu-id="98818-344">10001</span></span></td>
<td><span data-ttu-id="98818-345">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-345">Electricity</span></span></td>
<td><span data-ttu-id="98818-346">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-346">Variable cost</span></span></td>
<td><span data-ttu-id="98818-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="98818-347">-9,000.00</span></span></td>
<td><span data-ttu-id="98818-348">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-349">CC001</span><span class="sxs-lookup"><span data-stu-id="98818-349">CC001</span></span></td>
<td><span data-ttu-id="98818-350">HR</span><span class="sxs-lookup"><span data-stu-id="98818-350">HR</span></span></td>
<td><span data-ttu-id="98818-351">10001</span><span class="sxs-lookup"><span data-stu-id="98818-351">10001</span></span></td>
<td><span data-ttu-id="98818-352">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-352">Electricity</span></span></td>
<td><span data-ttu-id="98818-353">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-353">Variable cost</span></span></td>
<td><span data-ttu-id="98818-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="98818-354">1,285.71</span></span></td>
<td><span data-ttu-id="98818-355">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-356">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-356">CC002</span></span></td>
<td><span data-ttu-id="98818-357">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-357">Finance</span></span></td>
<td><span data-ttu-id="98818-358">10001</span><span class="sxs-lookup"><span data-stu-id="98818-358">10001</span></span></td>
<td><span data-ttu-id="98818-359">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-359">Electricity</span></span></td>
<td><span data-ttu-id="98818-360">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-360">Variable cost</span></span></td>
<td><span data-ttu-id="98818-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="98818-361">7,714.29</span></span></td>
<td><span data-ttu-id="98818-362">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98818-363">Sīkāku informāciju skatiet šeit: [Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="98818-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="98818-364">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="98818-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="98818-365">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="98818-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="98818-366">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="98818-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="98818-367">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="98818-367">Define the overhead rate</span></span>

<span data-ttu-id="98818-368">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="98818-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="98818-369">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="98818-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-370">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-370">Cost object</span></span></th>
<th><span data-ttu-id="98818-371">Stundas</span><span class="sxs-lookup"><span data-stu-id="98818-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="98818-372">Proj 1</span></span></td>
<td><span data-ttu-id="98818-373">1. projekts</span><span class="sxs-lookup"><span data-stu-id="98818-373">Project 1</span></span></td>
<td><span data-ttu-id="98818-374">3.</span><span class="sxs-lookup"><span data-stu-id="98818-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="98818-375">Proj 2</span></span></td>
<td><span data-ttu-id="98818-376">2. projekts</span><span class="sxs-lookup"><span data-stu-id="98818-376">Project 2</span></span></td>
<td><span data-ttu-id="98818-377">1.</span><span class="sxs-lookup"><span data-stu-id="98818-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98818-378">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="98818-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-379">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-379">Cost object</span></span></th>
<th><span data-ttu-id="98818-380">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="98818-380">Cost element</span></span></th>
<th><span data-ttu-id="98818-381">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="98818-381">Cost behavior</span></span></th>
<th><span data-ttu-id="98818-382">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="98818-382">Units</span></span></th>
<th><span data-ttu-id="98818-383">Likme</span><span class="sxs-lookup"><span data-stu-id="98818-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-384">CC001</span><span class="sxs-lookup"><span data-stu-id="98818-384">CC001</span></span></td>
<td><span data-ttu-id="98818-385">HR</span><span class="sxs-lookup"><span data-stu-id="98818-385">HR</span></span></td>
<td><span data-ttu-id="98818-386">10001</span><span class="sxs-lookup"><span data-stu-id="98818-386">10001</span></span></td>
<td><span data-ttu-id="98818-387">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-387">Variable cost</span></span></td>
<td><span data-ttu-id="98818-388">1</span><span class="sxs-lookup"><span data-stu-id="98818-388">1</span></span></td>
<td><span data-ttu-id="98818-389">10</span><span class="sxs-lookup"><span data-stu-id="98818-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98818-390">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="98818-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-391">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-391">Cost object</span></span></th>
<th><span data-ttu-id="98818-392">Lielums</span><span class="sxs-lookup"><span data-stu-id="98818-392">Magnitude</span></span></th>
<th><span data-ttu-id="98818-393">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="98818-393">Cost element</span></span></th>
<th><span data-ttu-id="98818-394">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="98818-394">Allocation factor</span></span></th>
<th><span data-ttu-id="98818-395">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="98818-396">Proj 1</span></span></td>
<td><span data-ttu-id="98818-397">1. projekts</span><span class="sxs-lookup"><span data-stu-id="98818-397">Project 1</span></span></td>
<td><span data-ttu-id="98818-398">3.</span><span class="sxs-lookup"><span data-stu-id="98818-398">3</span></span></td>
<td><span data-ttu-id="98818-399">10001</span><span class="sxs-lookup"><span data-stu-id="98818-399">10001</span></span></td>
<td><span data-ttu-id="98818-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="98818-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="98818-401">30,00</span><span class="sxs-lookup"><span data-stu-id="98818-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="98818-402">Proj 2</span></span></td>
<td><span data-ttu-id="98818-403">2. projekts</span><span class="sxs-lookup"><span data-stu-id="98818-403">Project 2</span></span></td>
<td><span data-ttu-id="98818-404">1.</span><span class="sxs-lookup"><span data-stu-id="98818-404">1</span></span></td>
<td><span data-ttu-id="98818-405">10001</span><span class="sxs-lookup"><span data-stu-id="98818-405">10001</span></span></td>
<td><span data-ttu-id="98818-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="98818-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="98818-407">10,00</span><span class="sxs-lookup"><span data-stu-id="98818-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="98818-408">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="98818-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="98818-409">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="98818-409">Journal</span></span></th>
<th><span data-ttu-id="98818-410">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="98818-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="98818-411">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="98818-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="98818-412">Versija</span><span class="sxs-lookup"><span data-stu-id="98818-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-413">00003</span><span class="sxs-lookup"><span data-stu-id="98818-413">00003</span></span></td>
<td><span data-ttu-id="98818-414">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="98818-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="98818-415">Finanšu</span><span class="sxs-lookup"><span data-stu-id="98818-415">Fiscal</span></span></td>
<td><span data-ttu-id="98818-416">2017</span><span class="sxs-lookup"><span data-stu-id="98818-416">2017</span></span></td>
<td><span data-ttu-id="98818-417">Periods 1</span><span class="sxs-lookup"><span data-stu-id="98818-417">Period 1</span></span></td>
<td><span data-ttu-id="98818-418">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="98818-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="98818-419">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="98818-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="98818-420">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="98818-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="98818-421">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-421">Cost object</span></span></th>
<th><span data-ttu-id="98818-422">Lielums</span><span class="sxs-lookup"><span data-stu-id="98818-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-423">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="98818-424">Proj 1</span></span></td>
<td><span data-ttu-id="98818-425">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="98818-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="98818-426">3,00</span><span class="sxs-lookup"><span data-stu-id="98818-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-427">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="98818-428">Proj 2</span></span></td>
<td><span data-ttu-id="98818-429">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="98818-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="98818-430">1,00</span><span class="sxs-lookup"><span data-stu-id="98818-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="98818-431">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="98818-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-432">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="98818-433">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="98818-433">Cost element</span></span></th>
<th><span data-ttu-id="98818-434">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="98818-434">Cost behavior</span></span></th>
<th><span data-ttu-id="98818-435">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-435">Amount</span></span></th>
<th><span data-ttu-id="98818-436">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="98818-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="98818-437">CC0001</span></span></td>
<td><span data-ttu-id="98818-438">HR</span><span class="sxs-lookup"><span data-stu-id="98818-438">HR</span></span></td>
<td><span data-ttu-id="98818-439">10001</span><span class="sxs-lookup"><span data-stu-id="98818-439">10001</span></span></td>
<td><span data-ttu-id="98818-440">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-440">Electricity</span></span></td>
<td><span data-ttu-id="98818-441">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-441">Variable cost</span></span></td>
<td><span data-ttu-id="98818-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="98818-442">-30.00</span></span></td>
<td><span data-ttu-id="98818-443">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="98818-444">Proj 1</span></span></td>
<td><span data-ttu-id="98818-445">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="98818-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="98818-446">10001</span><span class="sxs-lookup"><span data-stu-id="98818-446">10001</span></span></td>
<td><span data-ttu-id="98818-447">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-447">Electricity</span></span></td>
<td><span data-ttu-id="98818-448">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-448">Variable cost</span></span></td>
<td><span data-ttu-id="98818-449">30,00</span><span class="sxs-lookup"><span data-stu-id="98818-449">30.00</span></span></td>
<td><span data-ttu-id="98818-450">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-451">CC001</span><span class="sxs-lookup"><span data-stu-id="98818-451">CC001</span></span></td>
<td><span data-ttu-id="98818-452">HR</span><span class="sxs-lookup"><span data-stu-id="98818-452">HR</span></span></td>
<td><span data-ttu-id="98818-453">10001</span><span class="sxs-lookup"><span data-stu-id="98818-453">10001</span></span></td>
<td><span data-ttu-id="98818-454">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-454">Electricity</span></span></td>
<td><span data-ttu-id="98818-455">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-455">Variable cost</span></span></td>
<td><span data-ttu-id="98818-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="98818-456">-10.00</span></span></td>
<td><span data-ttu-id="98818-457">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="98818-458">Proj 2</span></span></td>
<td><span data-ttu-id="98818-459">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="98818-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="98818-460">10001</span><span class="sxs-lookup"><span data-stu-id="98818-460">10001</span></span></td>
<td><span data-ttu-id="98818-461">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-461">Electricity</span></span></td>
<td><span data-ttu-id="98818-462">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-462">Variable cost</span></span></td>
<td><span data-ttu-id="98818-463">10,00</span><span class="sxs-lookup"><span data-stu-id="98818-463">10.00</span></span></td>
<td><span data-ttu-id="98818-464">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98818-465">Sīkāku informāciju skatiet šeit: [Pieskaitāmo izmaksu aprēķina veikšana](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="98818-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="98818-466">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="98818-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="98818-467">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="98818-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="98818-468">Finance and Operations atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="98818-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="98818-469">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="98818-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="98818-470">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="98818-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="98818-471">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="98818-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="98818-472">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="98818-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="98818-473">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="98818-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="98818-474">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="98818-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="98818-475">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="98818-475">Define the cost allocation</span></span>

<span data-ttu-id="98818-476">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="98818-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="98818-477">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="98818-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="98818-478">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="98818-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-479">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-479">Cost object</span></span></th>
<th><span data-ttu-id="98818-480">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="98818-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-481">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-481">CC002</span></span></td>
<td><span data-ttu-id="98818-482">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-482">Finance</span></span></td>
<td><span data-ttu-id="98818-483">35</span><span class="sxs-lookup"><span data-stu-id="98818-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-484">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-484">CC003</span></span></td>
<td><span data-ttu-id="98818-485">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-485">Assembly</span></span></td>
<td><span data-ttu-id="98818-486">55</span><span class="sxs-lookup"><span data-stu-id="98818-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-487">CC004</span><span class="sxs-lookup"><span data-stu-id="98818-487">CC004</span></span></td>
<td><span data-ttu-id="98818-488">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="98818-488">Packaging</span></span></td>
<td><span data-ttu-id="98818-489">10.</span><span class="sxs-lookup"><span data-stu-id="98818-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98818-490">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="98818-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="98818-491">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="98818-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-492">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-492">Cost object</span></span></th>
<th><span data-ttu-id="98818-493">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="98818-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-494">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-494">CC003</span></span></td>
<td><span data-ttu-id="98818-495">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-495">Assembly</span></span></td>
<td><span data-ttu-id="98818-496">65</span><span class="sxs-lookup"><span data-stu-id="98818-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-497">CC004</span><span class="sxs-lookup"><span data-stu-id="98818-497">CC004</span></span></td>
<td><span data-ttu-id="98818-498">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="98818-498">Packaging</span></span></td>
<td><span data-ttu-id="98818-499">35</span><span class="sxs-lookup"><span data-stu-id="98818-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98818-500">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="98818-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="98818-501">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="98818-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-502">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-502">Cost object</span></span></th>
<th><span data-ttu-id="98818-503">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="98818-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="98818-504">Prod 1</span></span></td>
<td><span data-ttu-id="98818-505">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-505">Product 1</span></span></td>
<td><span data-ttu-id="98818-506">60</span><span class="sxs-lookup"><span data-stu-id="98818-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="98818-507">Prod 2</span></span></td>
<td><span data-ttu-id="98818-508">2. prece</span><span class="sxs-lookup"><span data-stu-id="98818-508">Product 2</span></span></td>
<td><span data-ttu-id="98818-509">20</span><span class="sxs-lookup"><span data-stu-id="98818-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98818-510">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="98818-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="98818-511">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="98818-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-512">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-512">Cost object</span></span></th>
<th><span data-ttu-id="98818-513">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="98818-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="98818-514">Prod 1</span></span></td>
<td><span data-ttu-id="98818-515">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-515">Product 1</span></span></td>
<td><span data-ttu-id="98818-516">80</span><span class="sxs-lookup"><span data-stu-id="98818-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="98818-517">Prod 2</span></span></td>
<td><span data-ttu-id="98818-518">2. prece</span><span class="sxs-lookup"><span data-stu-id="98818-518">Product 2</span></span></td>
<td><span data-ttu-id="98818-519">15.</span><span class="sxs-lookup"><span data-stu-id="98818-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="98818-520">Sistēmā Finance and Operations statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="98818-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="98818-521">Sīkāku informāciju skatiet šeit: [Statistikas mēru nodrošinātāja veidne](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="98818-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="98818-522">Nākamajā tabulā ir parādīts rezultāts, ja tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījuma pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="98818-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-523">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-523">Cost object</span></span></th>
<th><span data-ttu-id="98818-524">Lielums</span><span class="sxs-lookup"><span data-stu-id="98818-524">Magnitude</span></span></th>
<th><span data-ttu-id="98818-525">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="98818-525">Allocation factor</span></span></th>
<th><span data-ttu-id="98818-526">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-526">Amount</span></span></th>
<th><span data-ttu-id="98818-527">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="98818-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-528">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-528">CC002</span></span></td>
<td><span data-ttu-id="98818-529">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-529">Finance</span></span></td>
<td><span data-ttu-id="98818-530">35</span><span class="sxs-lookup"><span data-stu-id="98818-530">35</span></span></td>
<td><span data-ttu-id="98818-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="98818-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="98818-532">175.00</span><span class="sxs-lookup"><span data-stu-id="98818-532">175.00</span></span></td>
<td><span data-ttu-id="98818-533">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-534">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-534">CC003</span></span></td>
<td><span data-ttu-id="98818-535">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-535">Assembly</span></span></td>
<td><span data-ttu-id="98818-536">55</span><span class="sxs-lookup"><span data-stu-id="98818-536">55</span></span></td>
<td><span data-ttu-id="98818-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="98818-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="98818-538">275.00</span><span class="sxs-lookup"><span data-stu-id="98818-538">275.00</span></span></td>
<td><span data-ttu-id="98818-539">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-540">CC004</span><span class="sxs-lookup"><span data-stu-id="98818-540">CC004</span></span></td>
<td><span data-ttu-id="98818-541">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="98818-541">Packaging</span></span></td>
<td><span data-ttu-id="98818-542">10.</span><span class="sxs-lookup"><span data-stu-id="98818-542">10</span></span></td>
<td><span data-ttu-id="98818-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="98818-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="98818-544">50,00</span><span class="sxs-lookup"><span data-stu-id="98818-544">50.00</span></span></td>
<td><span data-ttu-id="98818-545">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-546">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-546">CC002</span></span></td>
<td><span data-ttu-id="98818-547">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-547">Finance</span></span></td>
<td><span data-ttu-id="98818-548">35</span><span class="sxs-lookup"><span data-stu-id="98818-548">35</span></span></td>
<td><span data-ttu-id="98818-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="98818-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="98818-550">436.00</span><span class="sxs-lookup"><span data-stu-id="98818-550">436.00</span></span></td>
<td><span data-ttu-id="98818-551">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-552">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-552">CC003</span></span></td>
<td><span data-ttu-id="98818-553">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-553">Assembly</span></span></td>
<td><span data-ttu-id="98818-554">55</span><span class="sxs-lookup"><span data-stu-id="98818-554">55</span></span></td>
<td><span data-ttu-id="98818-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="98818-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="98818-556">685.14</span><span class="sxs-lookup"><span data-stu-id="98818-556">685.14</span></span></td>
<td><span data-ttu-id="98818-557">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-558">CC004</span><span class="sxs-lookup"><span data-stu-id="98818-558">CC004</span></span></td>
<td><span data-ttu-id="98818-559">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="98818-559">Packaging</span></span></td>
<td><span data-ttu-id="98818-560">10.</span><span class="sxs-lookup"><span data-stu-id="98818-560">10</span></span></td>
<td><span data-ttu-id="98818-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="98818-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="98818-562">124.57</span><span class="sxs-lookup"><span data-stu-id="98818-562">124.57</span></span></td>
<td><span data-ttu-id="98818-563">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98818-564">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="98818-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-565">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-565">Cost object</span></span></th>
<th><span data-ttu-id="98818-566">Lielums</span><span class="sxs-lookup"><span data-stu-id="98818-566">Magnitude</span></span></th>
<th><span data-ttu-id="98818-567">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="98818-567">Allocation factor</span></span></th>
<th><span data-ttu-id="98818-568">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-568">Amount</span></span></th>
<th><span data-ttu-id="98818-569">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="98818-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-570">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-570">CC003</span></span></td>
<td><span data-ttu-id="98818-571">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-571">Assembly</span></span></td>
<td><span data-ttu-id="98818-572">65</span><span class="sxs-lookup"><span data-stu-id="98818-572">65</span></span></td>
<td><span data-ttu-id="98818-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="98818-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="98818-574">438.75</span><span class="sxs-lookup"><span data-stu-id="98818-574">438.75</span></span></td>
<td><span data-ttu-id="98818-575">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-576">CC004</span><span class="sxs-lookup"><span data-stu-id="98818-576">CC004</span></span></td>
<td><span data-ttu-id="98818-577">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="98818-577">Packaging</span></span></td>
<td><span data-ttu-id="98818-578">35</span><span class="sxs-lookup"><span data-stu-id="98818-578">35</span></span></td>
<td><span data-ttu-id="98818-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="98818-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="98818-580">236.25</span><span class="sxs-lookup"><span data-stu-id="98818-580">236.25</span></span></td>
<td><span data-ttu-id="98818-581">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-582">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-582">CC003</span></span></td>
<td><span data-ttu-id="98818-583">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-583">Assembly</span></span></td>
<td><span data-ttu-id="98818-584">65</span><span class="sxs-lookup"><span data-stu-id="98818-584">65</span></span></td>
<td><span data-ttu-id="98818-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="98818-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="98818-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="98818-586">5,297.69</span></span></td>
<td><span data-ttu-id="98818-587">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-588">CC004</span><span class="sxs-lookup"><span data-stu-id="98818-588">CC004</span></span></td>
<td><span data-ttu-id="98818-589">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="98818-589">Packaging</span></span></td>
<td><span data-ttu-id="98818-590">35</span><span class="sxs-lookup"><span data-stu-id="98818-590">35</span></span></td>
<td><span data-ttu-id="98818-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="98818-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="98818-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="98818-592">2,852.60</span></span></td>
<td><span data-ttu-id="98818-593">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98818-594">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="98818-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-595">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-595">Cost object</span></span></th>
<th><span data-ttu-id="98818-596">Lielums</span><span class="sxs-lookup"><span data-stu-id="98818-596">Magnitude</span></span></th>
<th><span data-ttu-id="98818-597">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="98818-597">Allocation factor</span></span></th>
<th><span data-ttu-id="98818-598">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-598">Amount</span></span></th>
<th><span data-ttu-id="98818-599">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="98818-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="98818-600">Prod 1</span></span></td>
<td><span data-ttu-id="98818-601">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-601">Product 1</span></span></td>
<td><span data-ttu-id="98818-602">60</span><span class="sxs-lookup"><span data-stu-id="98818-602">60</span></span></td>
<td><span data-ttu-id="98818-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="98818-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="98818-604">535.31</span><span class="sxs-lookup"><span data-stu-id="98818-604">535.31</span></span></td>
<td><span data-ttu-id="98818-605">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="98818-606">Prod 2</span></span></td>
<td><span data-ttu-id="98818-607">2. prece</span><span class="sxs-lookup"><span data-stu-id="98818-607">Product 2</span></span></td>
<td><span data-ttu-id="98818-608">20.</span><span class="sxs-lookup"><span data-stu-id="98818-608">20</span></span></td>
<td><span data-ttu-id="98818-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="98818-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="98818-610">178.44</span><span class="sxs-lookup"><span data-stu-id="98818-610">178.44</span></span></td>
<td><span data-ttu-id="98818-611">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="98818-612">Prod 1</span></span></td>
<td><span data-ttu-id="98818-613">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-613">Product 1</span></span></td>
<td><span data-ttu-id="98818-614">60</span><span class="sxs-lookup"><span data-stu-id="98818-614">60</span></span></td>
<td><span data-ttu-id="98818-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="98818-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="98818-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="98818-616">4,487.12</span></span></td>
<td><span data-ttu-id="98818-617">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="98818-618">Prod 2</span></span></td>
<td><span data-ttu-id="98818-619">2. prece</span><span class="sxs-lookup"><span data-stu-id="98818-619">Product 2</span></span></td>
<td><span data-ttu-id="98818-620">20.</span><span class="sxs-lookup"><span data-stu-id="98818-620">20</span></span></td>
<td><span data-ttu-id="98818-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="98818-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="98818-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="98818-622">1,495.71</span></span></td>
<td><span data-ttu-id="98818-623">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98818-624">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="98818-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-625">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-625">Cost object</span></span></th>
<th><span data-ttu-id="98818-626">Lielums</span><span class="sxs-lookup"><span data-stu-id="98818-626">Magnitude</span></span></th>
<th><span data-ttu-id="98818-627">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="98818-627">Allocation factor</span></span></th>
<th><span data-ttu-id="98818-628">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-628">Amount</span></span></th>
<th><span data-ttu-id="98818-629">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="98818-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="98818-630">Prod 1</span></span></td>
<td><span data-ttu-id="98818-631">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-631">Product 1</span></span></td>
<td><span data-ttu-id="98818-632">80</span><span class="sxs-lookup"><span data-stu-id="98818-632">80</span></span></td>
<td><span data-ttu-id="98818-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="98818-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="98818-634">241.05</span><span class="sxs-lookup"><span data-stu-id="98818-634">241.05</span></span></td>
<td><span data-ttu-id="98818-635">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="98818-636">Prod 2</span></span></td>
<td><span data-ttu-id="98818-637">2. prece</span><span class="sxs-lookup"><span data-stu-id="98818-637">Product 2</span></span></td>
<td><span data-ttu-id="98818-638">15</span><span class="sxs-lookup"><span data-stu-id="98818-638">15</span></span></td>
<td><span data-ttu-id="98818-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="98818-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="98818-640">45.20</span><span class="sxs-lookup"><span data-stu-id="98818-640">45.20</span></span></td>
<td><span data-ttu-id="98818-641">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="98818-642">Prod 1</span></span></td>
<td><span data-ttu-id="98818-643">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-643">Product 1</span></span></td>
<td><span data-ttu-id="98818-644">80</span><span class="sxs-lookup"><span data-stu-id="98818-644">80</span></span></td>
<td><span data-ttu-id="98818-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="98818-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="98818-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="98818-646">2,507.09</span></span></td>
<td><span data-ttu-id="98818-647">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="98818-648">Prod 2</span></span></td>
<td><span data-ttu-id="98818-649">2. prece</span><span class="sxs-lookup"><span data-stu-id="98818-649">Product 2</span></span></td>
<td><span data-ttu-id="98818-650">15</span><span class="sxs-lookup"><span data-stu-id="98818-650">15</span></span></td>
<td><span data-ttu-id="98818-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="98818-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="98818-652">470.08</span><span class="sxs-lookup"><span data-stu-id="98818-652">470.08</span></span></td>
<td><span data-ttu-id="98818-653">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="98818-654">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="98818-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="98818-655">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="98818-655">Journal</span></span></th>
<th><span data-ttu-id="98818-656">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="98818-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="98818-657">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="98818-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="98818-658">Versija</span><span class="sxs-lookup"><span data-stu-id="98818-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-659">00004</span><span class="sxs-lookup"><span data-stu-id="98818-659">00004</span></span></td>
<td><span data-ttu-id="98818-660">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="98818-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="98818-661">Finanšu</span><span class="sxs-lookup"><span data-stu-id="98818-661">Fiscal</span></span></td>
<td><span data-ttu-id="98818-662">2017</span><span class="sxs-lookup"><span data-stu-id="98818-662">2017</span></span></td>
<td><span data-ttu-id="98818-663">Periods 1</span><span class="sxs-lookup"><span data-stu-id="98818-663">Period 1</span></span></td>
<td><span data-ttu-id="98818-664">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="98818-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="98818-665">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="98818-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="98818-666">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="98818-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="98818-667">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="98818-668">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="98818-668">Cost element</span></span></th>
<th><span data-ttu-id="98818-669">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="98818-669">Cost behavior</span></span></th>
<th><span data-ttu-id="98818-670">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-671">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-672">CC001</span><span class="sxs-lookup"><span data-stu-id="98818-672">CC001</span></span></td>
<td><span data-ttu-id="98818-673">HR</span><span class="sxs-lookup"><span data-stu-id="98818-673">HR</span></span></td>
<td><span data-ttu-id="98818-674">10001</span><span class="sxs-lookup"><span data-stu-id="98818-674">10001</span></span></td>
<td><span data-ttu-id="98818-675">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-675">Electricity</span></span></td>
<td><span data-ttu-id="98818-676">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-676">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-677">500,00</span><span class="sxs-lookup"><span data-stu-id="98818-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-678">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-679">CC001</span><span class="sxs-lookup"><span data-stu-id="98818-679">CC001</span></span></td>
<td><span data-ttu-id="98818-680">HR</span><span class="sxs-lookup"><span data-stu-id="98818-680">HR</span></span></td>
<td><span data-ttu-id="98818-681">10001</span><span class="sxs-lookup"><span data-stu-id="98818-681">10001</span></span></td>
<td><span data-ttu-id="98818-682">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-682">Electricity</span></span></td>
<td><span data-ttu-id="98818-683">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-683">Variable cost</span></span></td>
<td><span data-ttu-id="98818-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="98818-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-685">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-686">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-686">CC002</span></span></td>
<td><span data-ttu-id="98818-687">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-687">Finance</span></span></td>
<td><span data-ttu-id="98818-688">10001</span><span class="sxs-lookup"><span data-stu-id="98818-688">10001</span></span></td>
<td><span data-ttu-id="98818-689">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-689">Electricity</span></span></td>
<td><span data-ttu-id="98818-690">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-690">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-691">675.00</span><span class="sxs-lookup"><span data-stu-id="98818-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-692">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-693">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-693">CC002</span></span></td>
<td><span data-ttu-id="98818-694">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-694">Finance</span></span></td>
<td><span data-ttu-id="98818-695">10001</span><span class="sxs-lookup"><span data-stu-id="98818-695">10001</span></span></td>
<td><span data-ttu-id="98818-696">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-696">Electricity</span></span></td>
<td><span data-ttu-id="98818-697">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-697">Variable cost</span></span></td>
<td><span data-ttu-id="98818-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="98818-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-699">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-700">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-700">CC003</span></span></td>
<td><span data-ttu-id="98818-701">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-701">Assembly</span></span></td>
<td><span data-ttu-id="98818-702">10001</span><span class="sxs-lookup"><span data-stu-id="98818-702">10001</span></span></td>
<td><span data-ttu-id="98818-703">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-703">Electricity</span></span></td>
<td><span data-ttu-id="98818-704">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-704">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-705">713.75</span><span class="sxs-lookup"><span data-stu-id="98818-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-706">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-707">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-707">CC003</span></span></td>
<td><span data-ttu-id="98818-708">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-708">Assembly</span></span></td>
<td><span data-ttu-id="98818-709">10001</span><span class="sxs-lookup"><span data-stu-id="98818-709">10001</span></span></td>
<td><span data-ttu-id="98818-710">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-710">Electricity</span></span></td>
<td><span data-ttu-id="98818-711">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-711">Variable cost</span></span></td>
<td><span data-ttu-id="98818-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="98818-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-713">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-714">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-714">CC003</span></span></td>
<td><span data-ttu-id="98818-715">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="98818-715">Packaging</span></span></td>
<td><span data-ttu-id="98818-716">10001</span><span class="sxs-lookup"><span data-stu-id="98818-716">10001</span></span></td>
<td><span data-ttu-id="98818-717">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-717">Electricity</span></span></td>
<td><span data-ttu-id="98818-718">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-718">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-719">286.25</span><span class="sxs-lookup"><span data-stu-id="98818-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-720">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-721">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-721">CC003</span></span></td>
<td><span data-ttu-id="98818-722">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="98818-722">Packaging</span></span></td>
<td><span data-ttu-id="98818-723">10001</span><span class="sxs-lookup"><span data-stu-id="98818-723">10001</span></span></td>
<td><span data-ttu-id="98818-724">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-724">Electricity</span></span></td>
<td><span data-ttu-id="98818-725">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-725">Variable cost</span></span></td>
<td><span data-ttu-id="98818-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="98818-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-727">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="98818-728">Prod 1</span></span></td>
<td><span data-ttu-id="98818-729">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-729">Product 1</span></span></td>
<td><span data-ttu-id="98818-730">10001</span><span class="sxs-lookup"><span data-stu-id="98818-730">10001</span></span></td>
<td><span data-ttu-id="98818-731">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-731">Electricity</span></span></td>
<td><span data-ttu-id="98818-732">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-732">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-733">776.36</span><span class="sxs-lookup"><span data-stu-id="98818-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-734">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="98818-735">Prod 1</span></span></td>
<td><span data-ttu-id="98818-736">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-736">Product 1</span></span></td>
<td><span data-ttu-id="98818-737">10001</span><span class="sxs-lookup"><span data-stu-id="98818-737">10001</span></span></td>
<td><span data-ttu-id="98818-738">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-738">Electricity</span></span></td>
<td><span data-ttu-id="98818-739">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-739">Variable cost</span></span></td>
<td><span data-ttu-id="98818-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="98818-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-741">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="98818-742">Prod 2</span></span></td>
<td><span data-ttu-id="98818-743">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-743">Product 1</span></span></td>
<td><span data-ttu-id="98818-744">10001</span><span class="sxs-lookup"><span data-stu-id="98818-744">10001</span></span></td>
<td><span data-ttu-id="98818-745">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-745">Electricity</span></span></td>
<td><span data-ttu-id="98818-746">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-746">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-747">223.64</span><span class="sxs-lookup"><span data-stu-id="98818-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-748">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="98818-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="98818-749">Prod 2</span></span></td>
<td><span data-ttu-id="98818-750">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-750">Product 1</span></span></td>
<td><span data-ttu-id="98818-751">10001</span><span class="sxs-lookup"><span data-stu-id="98818-751">10001</span></span></td>
<td><span data-ttu-id="98818-752">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-752">Electricity</span></span></td>
<td><span data-ttu-id="98818-753">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-753">Variable cost</span></span></td>
<td><span data-ttu-id="98818-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="98818-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="98818-755">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="98818-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="98818-756">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="98818-757">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="98818-757">Cost element</span></span></th>
<th><span data-ttu-id="98818-758">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="98818-758">Cost behavior</span></span></th>
<th><span data-ttu-id="98818-759">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-759">Amount</span></span></th>
<th><span data-ttu-id="98818-760">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="98818-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98818-761">CC001</span><span class="sxs-lookup"><span data-stu-id="98818-761">CC001</span></span></td>
<td><span data-ttu-id="98818-762">HR</span><span class="sxs-lookup"><span data-stu-id="98818-762">HR</span></span></td>
<td><span data-ttu-id="98818-763">10001</span><span class="sxs-lookup"><span data-stu-id="98818-763">10001</span></span></td>
<td><span data-ttu-id="98818-764">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-764">Electricity</span></span></td>
<td><span data-ttu-id="98818-765">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-765">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="98818-766">-500.00</span></span></td>
<td><span data-ttu-id="98818-767">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-768">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-768">CC002</span></span></td>
<td><span data-ttu-id="98818-769">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-769">Finance</span></span></td>
<td><span data-ttu-id="98818-770">10001</span><span class="sxs-lookup"><span data-stu-id="98818-770">10001</span></span></td>
<td><span data-ttu-id="98818-771">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-771">Electricity</span></span></td>
<td><span data-ttu-id="98818-772">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-772">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-773">175.00</span><span class="sxs-lookup"><span data-stu-id="98818-773">175.00</span></span></td>
<td><span data-ttu-id="98818-774">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-775">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-775">CC003</span></span></td>
<td><span data-ttu-id="98818-776">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-776">Assembly</span></span></td>
<td><span data-ttu-id="98818-777">10001</span><span class="sxs-lookup"><span data-stu-id="98818-777">10001</span></span></td>
<td><span data-ttu-id="98818-778">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-778">Electricity</span></span></td>
<td><span data-ttu-id="98818-779">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-779">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-780">275.00</span><span class="sxs-lookup"><span data-stu-id="98818-780">275.00</span></span></td>
<td><span data-ttu-id="98818-781">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-782">CC004</span><span class="sxs-lookup"><span data-stu-id="98818-782">CC004</span></span></td>
<td><span data-ttu-id="98818-783">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="98818-783">Packaging</span></span></td>
<td><span data-ttu-id="98818-784">10001</span><span class="sxs-lookup"><span data-stu-id="98818-784">10001</span></span></td>
<td><span data-ttu-id="98818-785">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-785">Electricity</span></span></td>
<td><span data-ttu-id="98818-786">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-786">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-787">50,00</span><span class="sxs-lookup"><span data-stu-id="98818-787">50,00</span></span></td>
<td><span data-ttu-id="98818-788">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-789">CC001</span><span class="sxs-lookup"><span data-stu-id="98818-789">CC001</span></span></td>
<td><span data-ttu-id="98818-790">HR</span><span class="sxs-lookup"><span data-stu-id="98818-790">HR</span></span></td>
<td><span data-ttu-id="98818-791">10001</span><span class="sxs-lookup"><span data-stu-id="98818-791">10001</span></span></td>
<td><span data-ttu-id="98818-792">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-792">Electricity</span></span></td>
<td><span data-ttu-id="98818-793">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-793">Variable cost</span></span></td>
<td><span data-ttu-id="98818-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="98818-794">-1,245.71</span></span></td>
<td><span data-ttu-id="98818-795">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-796">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-796">CC002</span></span></td>
<td><span data-ttu-id="98818-797">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-797">Finance</span></span></td>
<td><span data-ttu-id="98818-798">10001</span><span class="sxs-lookup"><span data-stu-id="98818-798">10001</span></span></td>
<td><span data-ttu-id="98818-799">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-799">Electricity</span></span></td>
<td><span data-ttu-id="98818-800">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-800">Variable cost</span></span></td>
<td><span data-ttu-id="98818-801">436.00</span><span class="sxs-lookup"><span data-stu-id="98818-801">436.00</span></span></td>
<td><span data-ttu-id="98818-802">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-803">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-803">CC003</span></span></td>
<td><span data-ttu-id="98818-804">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-804">Assembly</span></span></td>
<td><span data-ttu-id="98818-805">10001</span><span class="sxs-lookup"><span data-stu-id="98818-805">10001</span></span></td>
<td><span data-ttu-id="98818-806">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-806">Electricity</span></span></td>
<td><span data-ttu-id="98818-807">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-807">Variable cost</span></span></td>
<td><span data-ttu-id="98818-808">685.14</span><span class="sxs-lookup"><span data-stu-id="98818-808">685.14</span></span></td>
<td><span data-ttu-id="98818-809">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-810">CC004</span><span class="sxs-lookup"><span data-stu-id="98818-810">CC004</span></span></td>
<td><span data-ttu-id="98818-811">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="98818-811">Packaging</span></span></td>
<td><span data-ttu-id="98818-812">10001</span><span class="sxs-lookup"><span data-stu-id="98818-812">10001</span></span></td>
<td><span data-ttu-id="98818-813">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-813">Electricity</span></span></td>
<td><span data-ttu-id="98818-814">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-814">Variable cost</span></span></td>
<td><span data-ttu-id="98818-815">124.57</span><span class="sxs-lookup"><span data-stu-id="98818-815">124.57</span></span></td>
<td><span data-ttu-id="98818-816">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-817">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-817">CC002</span></span></td>
<td><span data-ttu-id="98818-818">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-818">Finance</span></span></td>
<td><span data-ttu-id="98818-819">10001</span><span class="sxs-lookup"><span data-stu-id="98818-819">10001</span></span></td>
<td><span data-ttu-id="98818-820">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-820">Electricity</span></span></td>
<td><span data-ttu-id="98818-821">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-821">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="98818-822">-675.00</span></span></td>
<td><span data-ttu-id="98818-823">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-824">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-824">CC003</span></span></td>
<td><span data-ttu-id="98818-825">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-825">Assembly</span></span></td>
<td><span data-ttu-id="98818-826">10001</span><span class="sxs-lookup"><span data-stu-id="98818-826">10001</span></span></td>
<td><span data-ttu-id="98818-827">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-827">Electricity</span></span></td>
<td><span data-ttu-id="98818-828">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-828">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-829">438.75</span><span class="sxs-lookup"><span data-stu-id="98818-829">438.75</span></span></td>
<td><span data-ttu-id="98818-830">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-831">CC004</span><span class="sxs-lookup"><span data-stu-id="98818-831">CC004</span></span></td>
<td><span data-ttu-id="98818-832">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="98818-832">Packaging</span></span></td>
<td><span data-ttu-id="98818-833">10001</span><span class="sxs-lookup"><span data-stu-id="98818-833">10001</span></span></td>
<td><span data-ttu-id="98818-834">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-834">Electricity</span></span></td>
<td><span data-ttu-id="98818-835">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-835">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-836">236.25</span><span class="sxs-lookup"><span data-stu-id="98818-836">236.25</span></span></td>
<td><span data-ttu-id="98818-837">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-838">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-838">CC002</span></span></td>
<td><span data-ttu-id="98818-839">Finanses</span><span class="sxs-lookup"><span data-stu-id="98818-839">Finance</span></span></td>
<td><span data-ttu-id="98818-840">10001</span><span class="sxs-lookup"><span data-stu-id="98818-840">10001</span></span></td>
<td><span data-ttu-id="98818-841">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-841">Electricity</span></span></td>
<td><span data-ttu-id="98818-842">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-842">Variable cost</span></span></td>
<td><span data-ttu-id="98818-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="98818-843">-8,150.29</span></span></td>
<td><span data-ttu-id="98818-844">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-845">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-845">CC003</span></span></td>
<td><span data-ttu-id="98818-846">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-846">Assembly</span></span></td>
<td><span data-ttu-id="98818-847">10001</span><span class="sxs-lookup"><span data-stu-id="98818-847">10001</span></span></td>
<td><span data-ttu-id="98818-848">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-848">Electricity</span></span></td>
<td><span data-ttu-id="98818-849">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-849">Variable cost</span></span></td>
<td><span data-ttu-id="98818-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="98818-850">5,297.69</span></span></td>
<td><span data-ttu-id="98818-851">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-852">CC004</span><span class="sxs-lookup"><span data-stu-id="98818-852">CC004</span></span></td>
<td><span data-ttu-id="98818-853">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="98818-853">Packaging</span></span></td>
<td><span data-ttu-id="98818-854">10001</span><span class="sxs-lookup"><span data-stu-id="98818-854">10001</span></span></td>
<td><span data-ttu-id="98818-855">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-855">Electricity</span></span></td>
<td><span data-ttu-id="98818-856">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-856">Variable cost</span></span></td>
<td><span data-ttu-id="98818-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="98818-857">2,852.60</span></span></td>
<td><span data-ttu-id="98818-858">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-859">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-859">CC003</span></span></td>
<td><span data-ttu-id="98818-860">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-860">Assembly</span></span></td>
<td><span data-ttu-id="98818-861">10001</span><span class="sxs-lookup"><span data-stu-id="98818-861">10001</span></span></td>
<td><span data-ttu-id="98818-862">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-862">Electricity</span></span></td>
<td><span data-ttu-id="98818-863">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-863">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="98818-864">-713.75</span></span></td>
<td><span data-ttu-id="98818-865">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="98818-866">Prod 1</span></span></td>
<td><span data-ttu-id="98818-867">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-867">Product 1</span></span></td>
<td><span data-ttu-id="98818-868">10001</span><span class="sxs-lookup"><span data-stu-id="98818-868">10001</span></span></td>
<td><span data-ttu-id="98818-869">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-869">Electricity</span></span></td>
<td><span data-ttu-id="98818-870">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-870">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-871">535.31</span><span class="sxs-lookup"><span data-stu-id="98818-871">535.31</span></span></td>
<td><span data-ttu-id="98818-872">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="98818-873">Prod 2</span></span></td>
<td><span data-ttu-id="98818-874">2. prece</span><span class="sxs-lookup"><span data-stu-id="98818-874">Product 2</span></span></td>
<td><span data-ttu-id="98818-875">10001</span><span class="sxs-lookup"><span data-stu-id="98818-875">10001</span></span></td>
<td><span data-ttu-id="98818-876">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-876">Electricity</span></span></td>
<td><span data-ttu-id="98818-877">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-877">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-878">178.44</span><span class="sxs-lookup"><span data-stu-id="98818-878">178.44</span></span></td>
<td><span data-ttu-id="98818-879">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-880">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-880">CC003</span></span></td>
<td><span data-ttu-id="98818-881">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-881">Assembly</span></span></td>
<td><span data-ttu-id="98818-882">10001</span><span class="sxs-lookup"><span data-stu-id="98818-882">10001</span></span></td>
<td><span data-ttu-id="98818-883">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-883">Electricity</span></span></td>
<td><span data-ttu-id="98818-884">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-884">Variable cost</span></span></td>
<td><span data-ttu-id="98818-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="98818-885">-5,982.83</span></span></td>
<td><span data-ttu-id="98818-886">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="98818-887">Prod 1</span></span></td>
<td><span data-ttu-id="98818-888">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-888">Product 1</span></span></td>
<td><span data-ttu-id="98818-889">10001</span><span class="sxs-lookup"><span data-stu-id="98818-889">10001</span></span></td>
<td><span data-ttu-id="98818-890">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-890">Electricity</span></span></td>
<td><span data-ttu-id="98818-891">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-891">Variable cost</span></span></td>
<td><span data-ttu-id="98818-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="98818-892">4,487.12</span></span></td>
<td><span data-ttu-id="98818-893">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="98818-894">Prod 2</span></span></td>
<td><span data-ttu-id="98818-895">2. prece</span><span class="sxs-lookup"><span data-stu-id="98818-895">Product 2</span></span></td>
<td><span data-ttu-id="98818-896">10001</span><span class="sxs-lookup"><span data-stu-id="98818-896">10001</span></span></td>
<td><span data-ttu-id="98818-897">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-897">Electricity</span></span></td>
<td><span data-ttu-id="98818-898">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-898">Variable cost</span></span></td>
<td><span data-ttu-id="98818-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="98818-899">1,495.71</span></span></td>
<td><span data-ttu-id="98818-900">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-901">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-901">CC003</span></span></td>
<td><span data-ttu-id="98818-902">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-902">Assembly</span></span></td>
<td><span data-ttu-id="98818-903">10001</span><span class="sxs-lookup"><span data-stu-id="98818-903">10001</span></span></td>
<td><span data-ttu-id="98818-904">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-904">Electricity</span></span></td>
<td><span data-ttu-id="98818-905">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-905">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="98818-906">-286.25</span></span></td>
<td><span data-ttu-id="98818-907">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="98818-908">Prod 1</span></span></td>
<td><span data-ttu-id="98818-909">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-909">Product 1</span></span></td>
<td><span data-ttu-id="98818-910">10001</span><span class="sxs-lookup"><span data-stu-id="98818-910">10001</span></span></td>
<td><span data-ttu-id="98818-911">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-911">Electricity</span></span></td>
<td><span data-ttu-id="98818-912">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-912">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-913">241.05</span><span class="sxs-lookup"><span data-stu-id="98818-913">241.05</span></span></td>
<td><span data-ttu-id="98818-914">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="98818-915">Prod 2</span></span></td>
<td><span data-ttu-id="98818-916">2. prece</span><span class="sxs-lookup"><span data-stu-id="98818-916">Product 2</span></span></td>
<td><span data-ttu-id="98818-917">10001</span><span class="sxs-lookup"><span data-stu-id="98818-917">10001</span></span></td>
<td><span data-ttu-id="98818-918">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-918">Electricity</span></span></td>
<td><span data-ttu-id="98818-919">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-919">Fixed cost</span></span></td>
<td><span data-ttu-id="98818-920">45.20</span><span class="sxs-lookup"><span data-stu-id="98818-920">45.20</span></span></td>
<td><span data-ttu-id="98818-921">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-922">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-922">CC003</span></span></td>
<td><span data-ttu-id="98818-923">Montāža</span><span class="sxs-lookup"><span data-stu-id="98818-923">Assembly</span></span></td>
<td><span data-ttu-id="98818-924">10001</span><span class="sxs-lookup"><span data-stu-id="98818-924">10001</span></span></td>
<td><span data-ttu-id="98818-925">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-925">Electricity</span></span></td>
<td><span data-ttu-id="98818-926">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-926">Variable cost</span></span></td>
<td><span data-ttu-id="98818-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="98818-927">-2,977.17</span></span></td>
<td><span data-ttu-id="98818-928">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="98818-929">Prod 1</span></span></td>
<td><span data-ttu-id="98818-930">1. prece</span><span class="sxs-lookup"><span data-stu-id="98818-930">Product 1</span></span></td>
<td><span data-ttu-id="98818-931">10001</span><span class="sxs-lookup"><span data-stu-id="98818-931">10001</span></span></td>
<td><span data-ttu-id="98818-932">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-932">Electricity</span></span></td>
<td><span data-ttu-id="98818-933">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-933">Variable cost</span></span></td>
<td><span data-ttu-id="98818-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="98818-934">2,507.09</span></span></td>
<td><span data-ttu-id="98818-935">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98818-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="98818-936">Prod 2</span></span></td>
<td><span data-ttu-id="98818-937">2. prece</span><span class="sxs-lookup"><span data-stu-id="98818-937">Product 2</span></span></td>
<td><span data-ttu-id="98818-938">10001</span><span class="sxs-lookup"><span data-stu-id="98818-938">10001</span></span></td>
<td><span data-ttu-id="98818-939">Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-939">Electricity</span></span></td>
<td><span data-ttu-id="98818-940">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-940">Variable cost</span></span></td>
<td><span data-ttu-id="98818-941">470.08</span><span class="sxs-lookup"><span data-stu-id="98818-941">470.08</span></span></td>
<td><span data-ttu-id="98818-942">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="98818-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="98818-943">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="98818-943">Conclusion</span></span>
<span data-ttu-id="98818-944">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="98818-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="98818-945">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="98818-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="98818-946">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="98818-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="98818-947">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="98818-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="98818-948">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="98818-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="98818-949">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="98818-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="98818-950">Summa</span><span class="sxs-lookup"><span data-stu-id="98818-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="98818-951">CC099</span><span class="sxs-lookup"><span data-stu-id="98818-951">CC099</span></span></th>
<th><span data-ttu-id="98818-952">CC001</span><span class="sxs-lookup"><span data-stu-id="98818-952">CC001</span></span></th>
<th><span data-ttu-id="98818-953">CC002</span><span class="sxs-lookup"><span data-stu-id="98818-953">CC002</span></span></th>
<th><span data-ttu-id="98818-954">CC003</span><span class="sxs-lookup"><span data-stu-id="98818-954">CC003</span></span></th>
<th><span data-ttu-id="98818-955">CC004</span><span class="sxs-lookup"><span data-stu-id="98818-955">CC004</span></span></th>
<th><span data-ttu-id="98818-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="98818-956">Proj 1</span></span></th>
<th><span data-ttu-id="98818-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="98818-957">Proj 2</span></span></th>
<th><span data-ttu-id="98818-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="98818-958">Prod 1</span></span></th>
<th><span data-ttu-id="98818-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="98818-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="98818-960">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="98818-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="98818-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="98818-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="98818-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="98818-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="98818-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="98818-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="98818-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="98818-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="98818-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="98818-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="98818-970">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="98818-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-971">0,00</span><span class="sxs-lookup"><span data-stu-id="98818-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="98818-972">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-973">0,00</span><span class="sxs-lookup"><span data-stu-id="98818-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-974">0,00</span><span class="sxs-lookup"><span data-stu-id="98818-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-975">0,00</span><span class="sxs-lookup"><span data-stu-id="98818-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-976">0,00</span><span class="sxs-lookup"><span data-stu-id="98818-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-977">0,00</span><span class="sxs-lookup"><span data-stu-id="98818-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="98818-978">776.36</span><span class="sxs-lookup"><span data-stu-id="98818-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-979">223.64</span><span class="sxs-lookup"><span data-stu-id="98818-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="98818-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="98818-981">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="98818-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-982">000</span><span class="sxs-lookup"><span data-stu-id="98818-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-983">0,00</span><span class="sxs-lookup"><span data-stu-id="98818-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-984">0,00</span><span class="sxs-lookup"><span data-stu-id="98818-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-985">0,00</span><span class="sxs-lookup"><span data-stu-id="98818-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-986">0,00</span><span class="sxs-lookup"><span data-stu-id="98818-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-987">30,00</span><span class="sxs-lookup"><span data-stu-id="98818-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-988">10,00</span><span class="sxs-lookup"><span data-stu-id="98818-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="98818-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="98818-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="98818-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="98818-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="98818-992">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="98818-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="98818-993">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="98818-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="98818-994">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="98818-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="98818-995">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="98818-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="98818-996">Sīkāku informāciju skatiet šeit: [Izmaksu apkopošanas politika](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="98818-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




