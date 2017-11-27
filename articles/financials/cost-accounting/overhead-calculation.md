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

# <a name="overhead-calculation"></a><span data-ttu-id="8d685-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="8d685-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8d685-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="8d685-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="8d685-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="8d685-105">Term definition</span></span>
---------------

<span data-ttu-id="8d685-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="8d685-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="8d685-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="8d685-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="8d685-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="8d685-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="8d685-109">Īre</span><span class="sxs-lookup"><span data-stu-id="8d685-109">Rent</span></span>
-   <span data-ttu-id="8d685-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-110">Electricity</span></span>
-   <span data-ttu-id="8d685-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="8d685-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="8d685-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="8d685-112">Overhead calculation overview</span></span>
<span data-ttu-id="8d685-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="8d685-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="8d685-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="8d685-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="8d685-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="8d685-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="8d685-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="8d685-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="8d685-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="8d685-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="8d685-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="8d685-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="8d685-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="8d685-119">Version type</span></span>
-   <span data-ttu-id="8d685-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="8d685-120">Date and time</span></span>
-   <span data-ttu-id="8d685-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="8d685-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="8d685-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="8d685-122">Fiscal year</span></span>
-   <span data-ttu-id="8d685-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="8d685-123">Fiscal period</span></span>

<span data-ttu-id="8d685-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="8d685-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="8d685-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="8d685-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="8d685-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="8d685-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="8d685-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="8d685-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="8d685-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="8d685-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="8d685-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="8d685-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="8d685-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="8d685-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="8d685-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="8d685-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="8d685-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="8d685-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="8d685-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="8d685-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="8d685-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="8d685-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="8d685-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="8d685-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="8d685-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="8d685-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="8d685-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d685-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="8d685-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8d685-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="8d685-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="8d685-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="8d685-140">Main account</span></span></th>
<th><span data-ttu-id="8d685-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="8d685-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="8d685-143">CC099</span><span class="sxs-lookup"><span data-stu-id="8d685-143">CC099</span></span></td>
<td><span data-ttu-id="8d685-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="8d685-144">Default cost center</span></span></td>
<td><span data-ttu-id="8d685-145">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-145">10001</span></span></td>
<td><span data-ttu-id="8d685-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-146">Electricity</span></span></td>
<td><span data-ttu-id="8d685-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="8d685-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="8d685-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="8d685-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="8d685-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="8d685-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="8d685-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="8d685-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="8d685-151">Define the cost behavior rule</span></span>

<span data-ttu-id="8d685-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="8d685-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="8d685-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="8d685-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="8d685-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="8d685-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="8d685-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="8d685-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="8d685-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="8d685-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="8d685-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="8d685-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="8d685-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="8d685-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="8d685-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d685-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="8d685-160">Journal</span></span></th>
<th><span data-ttu-id="8d685-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="8d685-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8d685-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="8d685-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8d685-163">Versija</span><span class="sxs-lookup"><span data-stu-id="8d685-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-164">00001</span><span class="sxs-lookup"><span data-stu-id="8d685-164">00001</span></span></td>
<td><span data-ttu-id="8d685-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="8d685-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="8d685-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="8d685-166">Fiscal</span></span></td>
<td><span data-ttu-id="8d685-167">2017</span><span class="sxs-lookup"><span data-stu-id="8d685-167">2017</span></span></td>
<td><span data-ttu-id="8d685-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="8d685-168">Period 1</span></span></td>
<td><span data-ttu-id="8d685-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="8d685-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8d685-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="8d685-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d685-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="8d685-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8d685-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d685-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="8d685-173">Cost element</span></span></th>
<th><span data-ttu-id="8d685-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="8d685-174">Cost behavior</span></span></th>
<th><span data-ttu-id="8d685-175">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="8d685-177">CC099</span><span class="sxs-lookup"><span data-stu-id="8d685-177">CC099</span></span></td>
<td><span data-ttu-id="8d685-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="8d685-178">Default cost center</span></span></td>
<td><span data-ttu-id="8d685-179">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-179">10001</span></span></td>
<td><span data-ttu-id="8d685-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-180">Electricity</span></span></td>
<td><span data-ttu-id="8d685-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="8d685-181">Unclassified</span></span></td>
<td><span data-ttu-id="8d685-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8d685-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="8d685-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d685-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="8d685-185">Cost element</span></span></th>
<th><span data-ttu-id="8d685-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="8d685-186">Cost behavior</span></span></th>
<th><span data-ttu-id="8d685-187">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-187">Amount</span></span></th>
<th><span data-ttu-id="8d685-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="8d685-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-189">CC099</span><span class="sxs-lookup"><span data-stu-id="8d685-189">CC099</span></span></td>
<td><span data-ttu-id="8d685-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="8d685-190">Default cost center</span></span></td>
<td><span data-ttu-id="8d685-191">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-191">10001</span></span></td>
<td><span data-ttu-id="8d685-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-192">Electricity</span></span></td>
<td><span data-ttu-id="8d685-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="8d685-193">Unclassified</span></span></td>
<td><span data-ttu-id="8d685-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-194">10,000.00</span></span></td>
<td><span data-ttu-id="8d685-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-196">CC099</span><span class="sxs-lookup"><span data-stu-id="8d685-196">CC099</span></span></td>
<td><span data-ttu-id="8d685-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="8d685-197">Default cost center</span></span></td>
<td><span data-ttu-id="8d685-198">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-198">10001</span></span></td>
<td><span data-ttu-id="8d685-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-199">Electricity</span></span></td>
<td><span data-ttu-id="8d685-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="8d685-200">Unclassified</span></span></td>
<td><span data-ttu-id="8d685-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-201">-10,000.00</span></span></td>
<td><span data-ttu-id="8d685-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-203">CC099</span><span class="sxs-lookup"><span data-stu-id="8d685-203">CC099</span></span></td>
<td><span data-ttu-id="8d685-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="8d685-204">Default cost center</span></span></td>
<td><span data-ttu-id="8d685-205">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-205">10001</span></span></td>
<td><span data-ttu-id="8d685-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-206">Electricity</span></span></td>
<td><span data-ttu-id="8d685-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-207">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-208">1,000.00</span></span></td>
<td><span data-ttu-id="8d685-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-210">CC099</span><span class="sxs-lookup"><span data-stu-id="8d685-210">CC099</span></span></td>
<td><span data-ttu-id="8d685-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="8d685-211">Default cost center</span></span></td>
<td><span data-ttu-id="8d685-212">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-212">10001</span></span></td>
<td><span data-ttu-id="8d685-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-213">Electricity</span></span></td>
<td><span data-ttu-id="8d685-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-214">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8d685-215">9,000.00</span></span></td>
<td><span data-ttu-id="8d685-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-217">Detalizētu informāciju par izmaksu uzvedību skatiet sadaļā Izmaksu uzvedības politika.</span><span class="sxs-lookup"><span data-stu-id="8d685-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="8d685-218">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)</span><span class="sxs-lookup"><span data-stu-id="8d685-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="8d685-219">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="8d685-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="8d685-220">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="8d685-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="8d685-221">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="8d685-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="8d685-222">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="8d685-222">Define the cost distribution rule</span></span>

<span data-ttu-id="8d685-223">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="8d685-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="8d685-224">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="8d685-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="8d685-225">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="8d685-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="8d685-226">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="8d685-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="8d685-227">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="8d685-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="8d685-228">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="8d685-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-229">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-229">Cost object</span></span></th>
<th><span data-ttu-id="8d685-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="8d685-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-231">CC001</span><span class="sxs-lookup"><span data-stu-id="8d685-231">CC001</span></span></td>
<td><span data-ttu-id="8d685-232">HR</span><span class="sxs-lookup"><span data-stu-id="8d685-232">HR</span></span></td>
<td><span data-ttu-id="8d685-233">1000</span><span class="sxs-lookup"><span data-stu-id="8d685-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-234">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-234">CC002</span></span></td>
<td><span data-ttu-id="8d685-235">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-235">Finance</span></span></td>
<td><span data-ttu-id="8d685-236">6,000</span><span class="sxs-lookup"><span data-stu-id="8d685-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-237">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-237">CC003</span></span></td>
<td><span data-ttu-id="8d685-238">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-238">Assembly</span></span></td>
<td><span data-ttu-id="8d685-239">0</span><span class="sxs-lookup"><span data-stu-id="8d685-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-240">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="8d685-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-241">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-241">Cost object</span></span></th>
<th><span data-ttu-id="8d685-242">Lielums</span><span class="sxs-lookup"><span data-stu-id="8d685-242">Magnitude</span></span></th>
<th><span data-ttu-id="8d685-243">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="8d685-243">Allocation factor</span></span></th>
<th><span data-ttu-id="8d685-244">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-245">CC001</span><span class="sxs-lookup"><span data-stu-id="8d685-245">CC001</span></span></td>
<td><span data-ttu-id="8d685-246">HR</span><span class="sxs-lookup"><span data-stu-id="8d685-246">HR</span></span></td>
<td><span data-ttu-id="8d685-247">1000</span><span class="sxs-lookup"><span data-stu-id="8d685-247">1,000</span></span></td>
<td><span data-ttu-id="8d685-248">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8d685-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8d685-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-250">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-250">CC002</span></span></td>
<td><span data-ttu-id="8d685-251">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-251">Finance</span></span></td>
<td><span data-ttu-id="8d685-252">6,000</span><span class="sxs-lookup"><span data-stu-id="8d685-252">6,000</span></span></td>
<td><span data-ttu-id="8d685-253">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8d685-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8d685-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-255">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-255">CC003</span></span></td>
<td><span data-ttu-id="8d685-256">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-256">Assembly</span></span></td>
<td><span data-ttu-id="8d685-257">0</span><span class="sxs-lookup"><span data-stu-id="8d685-257">0</span></span></td>
<td><span data-ttu-id="8d685-258">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8d685-259">0,00</span><span class="sxs-lookup"><span data-stu-id="8d685-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-260">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="8d685-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="8d685-261">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="8d685-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-262">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-262">Cost object</span></span></th>
<th><span data-ttu-id="8d685-263">Formula</span><span class="sxs-lookup"><span data-stu-id="8d685-263">Formula</span></span></th>
<th><span data-ttu-id="8d685-264">Lielums</span><span class="sxs-lookup"><span data-stu-id="8d685-264">Magnitude</span></span></th>
<th><span data-ttu-id="8d685-265">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="8d685-265">Allocation factor</span></span></th>
<th><span data-ttu-id="8d685-266">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-267">CC001</span><span class="sxs-lookup"><span data-stu-id="8d685-267">CC001</span></span></td>
<td><span data-ttu-id="8d685-268">HR</span><span class="sxs-lookup"><span data-stu-id="8d685-268">HR</span></span></td>
<td><span data-ttu-id="8d685-269">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8d685-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8d685-270">1.</span><span class="sxs-lookup"><span data-stu-id="8d685-270">1</span></span></td>
<td><span data-ttu-id="8d685-271">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8d685-272">500,00</span><span class="sxs-lookup"><span data-stu-id="8d685-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-273">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-273">CC002</span></span></td>
<td><span data-ttu-id="8d685-274">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-274">Finance</span></span></td>
<td><span data-ttu-id="8d685-275">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8d685-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8d685-276">1.</span><span class="sxs-lookup"><span data-stu-id="8d685-276">1</span></span></td>
<td><span data-ttu-id="8d685-277">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8d685-278">500,00</span><span class="sxs-lookup"><span data-stu-id="8d685-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-279">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-279">CC003</span></span></td>
<td><span data-ttu-id="8d685-280">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-280">Assembly</span></span></td>
<td><span data-ttu-id="8d685-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8d685-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8d685-282">0</span><span class="sxs-lookup"><span data-stu-id="8d685-282">0</span></span></td>
<td><span data-ttu-id="8d685-283">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8d685-284">0,00</span><span class="sxs-lookup"><span data-stu-id="8d685-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8d685-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="8d685-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d685-286">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="8d685-286">Journal</span></span></th>
<th><span data-ttu-id="8d685-287">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="8d685-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8d685-288">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="8d685-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8d685-289">Versija</span><span class="sxs-lookup"><span data-stu-id="8d685-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-290">00002</span><span class="sxs-lookup"><span data-stu-id="8d685-290">00002</span></span></td>
<td><span data-ttu-id="8d685-291">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="8d685-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="8d685-292">Finanšu</span><span class="sxs-lookup"><span data-stu-id="8d685-292">Fiscal</span></span></td>
<td><span data-ttu-id="8d685-293">2017</span><span class="sxs-lookup"><span data-stu-id="8d685-293">2017</span></span></td>
<td><span data-ttu-id="8d685-294">Periods 1</span><span class="sxs-lookup"><span data-stu-id="8d685-294">Period 1</span></span></td>
<td><span data-ttu-id="8d685-295">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="8d685-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8d685-296">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="8d685-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d685-297">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="8d685-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8d685-298">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d685-299">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="8d685-299">Cost element</span></span></th>
<th><span data-ttu-id="8d685-300">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="8d685-300">Cost behavior</span></span></th>
<th><span data-ttu-id="8d685-301">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-302">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-303">CC099</span><span class="sxs-lookup"><span data-stu-id="8d685-303">CC099</span></span></td>
<td><span data-ttu-id="8d685-304">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="8d685-304">Default cost center</span></span></td>
<td><span data-ttu-id="8d685-305">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-305">10001</span></span></td>
<td><span data-ttu-id="8d685-306">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-306">Electricity</span></span></td>
<td><span data-ttu-id="8d685-307">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-307">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-308">1000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-309">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-310">CC099</span><span class="sxs-lookup"><span data-stu-id="8d685-310">CC099</span></span></td>
<td><span data-ttu-id="8d685-311">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="8d685-311">Default cost center</span></span></td>
<td><span data-ttu-id="8d685-312">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-312">10001</span></span></td>
<td><span data-ttu-id="8d685-313">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-313">Electricity</span></span></td>
<td><span data-ttu-id="8d685-314">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-314">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8d685-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8d685-316">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="8d685-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-317">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d685-318">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="8d685-318">Cost element</span></span></th>
<th><span data-ttu-id="8d685-319">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="8d685-319">Cost behavior</span></span></th>
<th><span data-ttu-id="8d685-320">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-320">Amount</span></span></th>
<th><span data-ttu-id="8d685-321">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="8d685-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-322">CC099</span><span class="sxs-lookup"><span data-stu-id="8d685-322">CC099</span></span></td>
<td><span data-ttu-id="8d685-323">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="8d685-323">Default cost center</span></span></td>
<td><span data-ttu-id="8d685-324">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-324">10001</span></span></td>
<td><span data-ttu-id="8d685-325">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-325">Electricity</span></span></td>
<td><span data-ttu-id="8d685-326">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-326">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-327">-1000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-327">-1,000.00</span></span></td>
<td><span data-ttu-id="8d685-328">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-329">CC001</span><span class="sxs-lookup"><span data-stu-id="8d685-329">CC001</span></span></td>
<td><span data-ttu-id="8d685-330">HR</span><span class="sxs-lookup"><span data-stu-id="8d685-330">HR</span></span></td>
<td><span data-ttu-id="8d685-331">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-331">10001</span></span></td>
<td><span data-ttu-id="8d685-332">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-332">Electricity</span></span></td>
<td><span data-ttu-id="8d685-333">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-333">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-334">500,00</span><span class="sxs-lookup"><span data-stu-id="8d685-334">500.00</span></span></td>
<td><span data-ttu-id="8d685-335">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-336">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-336">CC002</span></span></td>
<td><span data-ttu-id="8d685-337">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-337">Finance</span></span></td>
<td><span data-ttu-id="8d685-338">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-338">10001</span></span></td>
<td><span data-ttu-id="8d685-339">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-339">Electricity</span></span></td>
<td><span data-ttu-id="8d685-340">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-340">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-341">500,00</span><span class="sxs-lookup"><span data-stu-id="8d685-341">500.00</span></span></td>
<td><span data-ttu-id="8d685-342">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-343">CC099</span><span class="sxs-lookup"><span data-stu-id="8d685-343">CC099</span></span></td>
<td><span data-ttu-id="8d685-344">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="8d685-344">Default cost center</span></span></td>
<td><span data-ttu-id="8d685-345">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-345">10001</span></span></td>
<td><span data-ttu-id="8d685-346">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-346">Electricity</span></span></td>
<td><span data-ttu-id="8d685-347">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-347">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-348">-9000,00</span><span class="sxs-lookup"><span data-stu-id="8d685-348">-9,000.00</span></span></td>
<td><span data-ttu-id="8d685-349">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-350">CC001</span><span class="sxs-lookup"><span data-stu-id="8d685-350">CC001</span></span></td>
<td><span data-ttu-id="8d685-351">HR</span><span class="sxs-lookup"><span data-stu-id="8d685-351">HR</span></span></td>
<td><span data-ttu-id="8d685-352">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-352">10001</span></span></td>
<td><span data-ttu-id="8d685-353">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-353">Electricity</span></span></td>
<td><span data-ttu-id="8d685-354">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-354">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8d685-355">1,285.71</span></span></td>
<td><span data-ttu-id="8d685-356">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-357">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-357">CC002</span></span></td>
<td><span data-ttu-id="8d685-358">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-358">Finance</span></span></td>
<td><span data-ttu-id="8d685-359">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-359">10001</span></span></td>
<td><span data-ttu-id="8d685-360">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-360">Electricity</span></span></td>
<td><span data-ttu-id="8d685-361">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-361">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8d685-362">7,714.29</span></span></td>
<td><span data-ttu-id="8d685-363">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-364">Detalizētu informāciju par izmaksu sadali un sadalījuma pamatiem skatiet sadaļā Izmaksu sadales politika un Sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="8d685-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="8d685-365">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)</span><span class="sxs-lookup"><span data-stu-id="8d685-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="8d685-366">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="8d685-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="8d685-367">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="8d685-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="8d685-368">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="8d685-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="8d685-369">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="8d685-369">Define the overhead rate</span></span>

<span data-ttu-id="8d685-370">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="8d685-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="8d685-371">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="8d685-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-372">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-372">Cost object</span></span></th>
<th><span data-ttu-id="8d685-373">Stundas</span><span class="sxs-lookup"><span data-stu-id="8d685-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8d685-374">Proj 1</span></span></td>
<td><span data-ttu-id="8d685-375">1. projekts</span><span class="sxs-lookup"><span data-stu-id="8d685-375">Project 1</span></span></td>
<td><span data-ttu-id="8d685-376">3.</span><span class="sxs-lookup"><span data-stu-id="8d685-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8d685-377">Proj 2</span></span></td>
<td><span data-ttu-id="8d685-378">2. projekts</span><span class="sxs-lookup"><span data-stu-id="8d685-378">Project 2</span></span></td>
<td><span data-ttu-id="8d685-379">1.</span><span class="sxs-lookup"><span data-stu-id="8d685-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-380">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="8d685-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-381">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-381">Cost object</span></span></th>
<th><span data-ttu-id="8d685-382">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="8d685-382">Cost element</span></span></th>
<th><span data-ttu-id="8d685-383">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="8d685-383">Cost behavior</span></span></th>
<th><span data-ttu-id="8d685-384">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="8d685-384">Units</span></span></th>
<th><span data-ttu-id="8d685-385">Likme</span><span class="sxs-lookup"><span data-stu-id="8d685-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-386">CC001</span><span class="sxs-lookup"><span data-stu-id="8d685-386">CC001</span></span></td>
<td><span data-ttu-id="8d685-387">HR</span><span class="sxs-lookup"><span data-stu-id="8d685-387">HR</span></span></td>
<td><span data-ttu-id="8d685-388">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-388">10001</span></span></td>
<td><span data-ttu-id="8d685-389">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-389">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-390">1</span><span class="sxs-lookup"><span data-stu-id="8d685-390">1</span></span></td>
<td><span data-ttu-id="8d685-391">10</span><span class="sxs-lookup"><span data-stu-id="8d685-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-392">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="8d685-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-393">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-393">Cost object</span></span></th>
<th><span data-ttu-id="8d685-394">Lielums</span><span class="sxs-lookup"><span data-stu-id="8d685-394">Magnitude</span></span></th>
<th><span data-ttu-id="8d685-395">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="8d685-395">Cost element</span></span></th>
<th><span data-ttu-id="8d685-396">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="8d685-396">Allocation factor</span></span></th>
<th><span data-ttu-id="8d685-397">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8d685-398">Proj 1</span></span></td>
<td><span data-ttu-id="8d685-399">1. projekts</span><span class="sxs-lookup"><span data-stu-id="8d685-399">Project 1</span></span></td>
<td><span data-ttu-id="8d685-400">3.</span><span class="sxs-lookup"><span data-stu-id="8d685-400">3</span></span></td>
<td><span data-ttu-id="8d685-401">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-401">10001</span></span></td>
<td><span data-ttu-id="8d685-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="8d685-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8d685-403">30,00</span><span class="sxs-lookup"><span data-stu-id="8d685-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8d685-404">Proj 2</span></span></td>
<td><span data-ttu-id="8d685-405">2. projekts</span><span class="sxs-lookup"><span data-stu-id="8d685-405">Project 2</span></span></td>
<td><span data-ttu-id="8d685-406">1.</span><span class="sxs-lookup"><span data-stu-id="8d685-406">1</span></span></td>
<td><span data-ttu-id="8d685-407">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-407">10001</span></span></td>
<td><span data-ttu-id="8d685-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="8d685-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8d685-409">10,00</span><span class="sxs-lookup"><span data-stu-id="8d685-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8d685-410">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="8d685-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d685-411">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="8d685-411">Journal</span></span></th>
<th><span data-ttu-id="8d685-412">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="8d685-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8d685-413">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="8d685-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8d685-414">Versija</span><span class="sxs-lookup"><span data-stu-id="8d685-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-415">00003</span><span class="sxs-lookup"><span data-stu-id="8d685-415">00003</span></span></td>
<td><span data-ttu-id="8d685-416">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="8d685-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="8d685-417">Finanšu</span><span class="sxs-lookup"><span data-stu-id="8d685-417">Fiscal</span></span></td>
<td><span data-ttu-id="8d685-418">2017</span><span class="sxs-lookup"><span data-stu-id="8d685-418">2017</span></span></td>
<td><span data-ttu-id="8d685-419">Periods 1</span><span class="sxs-lookup"><span data-stu-id="8d685-419">Period 1</span></span></td>
<td><span data-ttu-id="8d685-420">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="8d685-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="8d685-421">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="8d685-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d685-422">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="8d685-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8d685-423">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-423">Cost object</span></span></th>
<th><span data-ttu-id="8d685-424">Lielums</span><span class="sxs-lookup"><span data-stu-id="8d685-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-425">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8d685-426">Proj 1</span></span></td>
<td><span data-ttu-id="8d685-427">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="8d685-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8d685-428">3,00</span><span class="sxs-lookup"><span data-stu-id="8d685-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-429">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8d685-430">Proj 2</span></span></td>
<td><span data-ttu-id="8d685-431">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="8d685-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8d685-432">1,00</span><span class="sxs-lookup"><span data-stu-id="8d685-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8d685-433">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="8d685-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-434">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d685-435">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="8d685-435">Cost element</span></span></th>
<th><span data-ttu-id="8d685-436">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="8d685-436">Cost behavior</span></span></th>
<th><span data-ttu-id="8d685-437">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-437">Amount</span></span></th>
<th><span data-ttu-id="8d685-438">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="8d685-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="8d685-439">CC0001</span></span></td>
<td><span data-ttu-id="8d685-440">HR</span><span class="sxs-lookup"><span data-stu-id="8d685-440">HR</span></span></td>
<td><span data-ttu-id="8d685-441">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-441">10001</span></span></td>
<td><span data-ttu-id="8d685-442">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-442">Electricity</span></span></td>
<td><span data-ttu-id="8d685-443">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-443">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="8d685-444">-30.00</span></span></td>
<td><span data-ttu-id="8d685-445">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8d685-446">Proj 1</span></span></td>
<td><span data-ttu-id="8d685-447">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="8d685-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8d685-448">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-448">10001</span></span></td>
<td><span data-ttu-id="8d685-449">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-449">Electricity</span></span></td>
<td><span data-ttu-id="8d685-450">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-450">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-451">30,00</span><span class="sxs-lookup"><span data-stu-id="8d685-451">30.00</span></span></td>
<td><span data-ttu-id="8d685-452">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-453">CC001</span><span class="sxs-lookup"><span data-stu-id="8d685-453">CC001</span></span></td>
<td><span data-ttu-id="8d685-454">HR</span><span class="sxs-lookup"><span data-stu-id="8d685-454">HR</span></span></td>
<td><span data-ttu-id="8d685-455">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-455">10001</span></span></td>
<td><span data-ttu-id="8d685-456">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-456">Electricity</span></span></td>
<td><span data-ttu-id="8d685-457">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-457">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="8d685-458">-10.00</span></span></td>
<td><span data-ttu-id="8d685-459">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8d685-460">Proj 2</span></span></td>
<td><span data-ttu-id="8d685-461">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="8d685-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8d685-462">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-462">10001</span></span></td>
<td><span data-ttu-id="8d685-463">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-463">Electricity</span></span></td>
<td><span data-ttu-id="8d685-464">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-464">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-465">10,00</span><span class="sxs-lookup"><span data-stu-id="8d685-465">10.00</span></span></td>
<td><span data-ttu-id="8d685-466">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-467">Detalizētu informāciju par pieskaitāmo izmaksu likmes politiku skatiet sadaļā Pieskaitāmo izmaksu likmes politika un Sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="8d685-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="8d685-468">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)</span><span class="sxs-lookup"><span data-stu-id="8d685-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="8d685-469">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="8d685-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="8d685-470">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="8d685-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="8d685-471">Finance and Operations atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="8d685-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="8d685-472">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="8d685-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="8d685-473">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="8d685-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="8d685-474">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="8d685-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="8d685-475">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="8d685-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="8d685-476">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="8d685-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="8d685-477">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="8d685-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="8d685-478">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="8d685-478">Define the cost allocation</span></span>

<span data-ttu-id="8d685-479">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="8d685-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="8d685-480">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="8d685-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="8d685-481">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="8d685-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-482">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-482">Cost object</span></span></th>
<th><span data-ttu-id="8d685-483">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="8d685-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-484">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-484">CC002</span></span></td>
<td><span data-ttu-id="8d685-485">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-485">Finance</span></span></td>
<td><span data-ttu-id="8d685-486">35</span><span class="sxs-lookup"><span data-stu-id="8d685-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-487">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-487">CC003</span></span></td>
<td><span data-ttu-id="8d685-488">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-488">Assembly</span></span></td>
<td><span data-ttu-id="8d685-489">55</span><span class="sxs-lookup"><span data-stu-id="8d685-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-490">CC004</span><span class="sxs-lookup"><span data-stu-id="8d685-490">CC004</span></span></td>
<td><span data-ttu-id="8d685-491">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="8d685-491">Packaging</span></span></td>
<td><span data-ttu-id="8d685-492">10.</span><span class="sxs-lookup"><span data-stu-id="8d685-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-493">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="8d685-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="8d685-494">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="8d685-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-495">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-495">Cost object</span></span></th>
<th><span data-ttu-id="8d685-496">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="8d685-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-497">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-497">CC003</span></span></td>
<td><span data-ttu-id="8d685-498">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-498">Assembly</span></span></td>
<td><span data-ttu-id="8d685-499">65</span><span class="sxs-lookup"><span data-stu-id="8d685-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-500">CC004</span><span class="sxs-lookup"><span data-stu-id="8d685-500">CC004</span></span></td>
<td><span data-ttu-id="8d685-501">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="8d685-501">Packaging</span></span></td>
<td><span data-ttu-id="8d685-502">35</span><span class="sxs-lookup"><span data-stu-id="8d685-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-503">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="8d685-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="8d685-504">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="8d685-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-505">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-505">Cost object</span></span></th>
<th><span data-ttu-id="8d685-506">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="8d685-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8d685-507">Prod 1</span></span></td>
<td><span data-ttu-id="8d685-508">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-508">Product 1</span></span></td>
<td><span data-ttu-id="8d685-509">60</span><span class="sxs-lookup"><span data-stu-id="8d685-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8d685-510">Prod 2</span></span></td>
<td><span data-ttu-id="8d685-511">2. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-511">Product 2</span></span></td>
<td><span data-ttu-id="8d685-512">20</span><span class="sxs-lookup"><span data-stu-id="8d685-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-513">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="8d685-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="8d685-514">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="8d685-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-515">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-515">Cost object</span></span></th>
<th><span data-ttu-id="8d685-516">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="8d685-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8d685-517">Prod 1</span></span></td>
<td><span data-ttu-id="8d685-518">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-518">Product 1</span></span></td>
<td><span data-ttu-id="8d685-519">80</span><span class="sxs-lookup"><span data-stu-id="8d685-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8d685-520">Prod 2</span></span></td>
<td><span data-ttu-id="8d685-521">2. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-521">Product 2</span></span></td>
<td><span data-ttu-id="8d685-522">15.</span><span class="sxs-lookup"><span data-stu-id="8d685-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-523">**Piezīme.** Sistēmā Finance and Operations statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="8d685-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="8d685-524">Plašāku informāciju par statistisko mēru nodrošinātājiem skatiet sadaļā Statistisko mēru nodrošinātāja veidnes.</span><span class="sxs-lookup"><span data-stu-id="8d685-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="8d685-525">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.) Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="8d685-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-526">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-526">Cost object</span></span></th>
<th><span data-ttu-id="8d685-527">Lielums</span><span class="sxs-lookup"><span data-stu-id="8d685-527">Magnitude</span></span></th>
<th><span data-ttu-id="8d685-528">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="8d685-528">Allocation factor</span></span></th>
<th><span data-ttu-id="8d685-529">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-529">Amount</span></span></th>
<th><span data-ttu-id="8d685-530">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="8d685-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-531">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-531">CC002</span></span></td>
<td><span data-ttu-id="8d685-532">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-532">Finance</span></span></td>
<td><span data-ttu-id="8d685-533">35</span><span class="sxs-lookup"><span data-stu-id="8d685-533">35</span></span></td>
<td><span data-ttu-id="8d685-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8d685-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8d685-535">175.00</span><span class="sxs-lookup"><span data-stu-id="8d685-535">175.00</span></span></td>
<td><span data-ttu-id="8d685-536">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-537">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-537">CC003</span></span></td>
<td><span data-ttu-id="8d685-538">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-538">Assembly</span></span></td>
<td><span data-ttu-id="8d685-539">55</span><span class="sxs-lookup"><span data-stu-id="8d685-539">55</span></span></td>
<td><span data-ttu-id="8d685-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8d685-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8d685-541">275.00</span><span class="sxs-lookup"><span data-stu-id="8d685-541">275.00</span></span></td>
<td><span data-ttu-id="8d685-542">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-543">CC004</span><span class="sxs-lookup"><span data-stu-id="8d685-543">CC004</span></span></td>
<td><span data-ttu-id="8d685-544">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="8d685-544">Packaging</span></span></td>
<td><span data-ttu-id="8d685-545">10.</span><span class="sxs-lookup"><span data-stu-id="8d685-545">10</span></span></td>
<td><span data-ttu-id="8d685-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8d685-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8d685-547">50,00</span><span class="sxs-lookup"><span data-stu-id="8d685-547">50.00</span></span></td>
<td><span data-ttu-id="8d685-548">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-549">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-549">CC002</span></span></td>
<td><span data-ttu-id="8d685-550">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-550">Finance</span></span></td>
<td><span data-ttu-id="8d685-551">35</span><span class="sxs-lookup"><span data-stu-id="8d685-551">35</span></span></td>
<td><span data-ttu-id="8d685-552">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="8d685-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8d685-553">436.00</span><span class="sxs-lookup"><span data-stu-id="8d685-553">436.00</span></span></td>
<td><span data-ttu-id="8d685-554">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-555">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-555">CC003</span></span></td>
<td><span data-ttu-id="8d685-556">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-556">Assembly</span></span></td>
<td><span data-ttu-id="8d685-557">55</span><span class="sxs-lookup"><span data-stu-id="8d685-557">55</span></span></td>
<td><span data-ttu-id="8d685-558">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="8d685-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8d685-559">685.14</span><span class="sxs-lookup"><span data-stu-id="8d685-559">685.14</span></span></td>
<td><span data-ttu-id="8d685-560">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-561">CC004</span><span class="sxs-lookup"><span data-stu-id="8d685-561">CC004</span></span></td>
<td><span data-ttu-id="8d685-562">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="8d685-562">Packaging</span></span></td>
<td><span data-ttu-id="8d685-563">10.</span><span class="sxs-lookup"><span data-stu-id="8d685-563">10</span></span></td>
<td><span data-ttu-id="8d685-564">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="8d685-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8d685-565">124.57</span><span class="sxs-lookup"><span data-stu-id="8d685-565">124.57</span></span></td>
<td><span data-ttu-id="8d685-566">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-567">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="8d685-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-568">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-568">Cost object</span></span></th>
<th><span data-ttu-id="8d685-569">Lielums</span><span class="sxs-lookup"><span data-stu-id="8d685-569">Magnitude</span></span></th>
<th><span data-ttu-id="8d685-570">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="8d685-570">Allocation factor</span></span></th>
<th><span data-ttu-id="8d685-571">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-571">Amount</span></span></th>
<th><span data-ttu-id="8d685-572">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="8d685-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-573">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-573">CC003</span></span></td>
<td><span data-ttu-id="8d685-574">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-574">Assembly</span></span></td>
<td><span data-ttu-id="8d685-575">65</span><span class="sxs-lookup"><span data-stu-id="8d685-575">65</span></span></td>
<td><span data-ttu-id="8d685-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="8d685-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8d685-577">438.75</span><span class="sxs-lookup"><span data-stu-id="8d685-577">438.75</span></span></td>
<td><span data-ttu-id="8d685-578">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-579">CC004</span><span class="sxs-lookup"><span data-stu-id="8d685-579">CC004</span></span></td>
<td><span data-ttu-id="8d685-580">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="8d685-580">Packaging</span></span></td>
<td><span data-ttu-id="8d685-581">35</span><span class="sxs-lookup"><span data-stu-id="8d685-581">35</span></span></td>
<td><span data-ttu-id="8d685-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="8d685-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8d685-583">236.25</span><span class="sxs-lookup"><span data-stu-id="8d685-583">236.25</span></span></td>
<td><span data-ttu-id="8d685-584">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-585">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-585">CC003</span></span></td>
<td><span data-ttu-id="8d685-586">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-586">Assembly</span></span></td>
<td><span data-ttu-id="8d685-587">65</span><span class="sxs-lookup"><span data-stu-id="8d685-587">65</span></span></td>
<td><span data-ttu-id="8d685-588">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="8d685-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8d685-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8d685-589">5,297.69</span></span></td>
<td><span data-ttu-id="8d685-590">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-591">CC004</span><span class="sxs-lookup"><span data-stu-id="8d685-591">CC004</span></span></td>
<td><span data-ttu-id="8d685-592">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="8d685-592">Packaging</span></span></td>
<td><span data-ttu-id="8d685-593">35</span><span class="sxs-lookup"><span data-stu-id="8d685-593">35</span></span></td>
<td><span data-ttu-id="8d685-594">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="8d685-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8d685-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8d685-595">2,852.60</span></span></td>
<td><span data-ttu-id="8d685-596">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-597">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="8d685-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-598">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-598">Cost object</span></span></th>
<th><span data-ttu-id="8d685-599">Lielums</span><span class="sxs-lookup"><span data-stu-id="8d685-599">Magnitude</span></span></th>
<th><span data-ttu-id="8d685-600">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="8d685-600">Allocation factor</span></span></th>
<th><span data-ttu-id="8d685-601">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-601">Amount</span></span></th>
<th><span data-ttu-id="8d685-602">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="8d685-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8d685-603">Prod 1</span></span></td>
<td><span data-ttu-id="8d685-604">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-604">Product 1</span></span></td>
<td><span data-ttu-id="8d685-605">60</span><span class="sxs-lookup"><span data-stu-id="8d685-605">60</span></span></td>
<td><span data-ttu-id="8d685-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="8d685-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8d685-607">535.31</span><span class="sxs-lookup"><span data-stu-id="8d685-607">535.31</span></span></td>
<td><span data-ttu-id="8d685-608">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8d685-609">Prod 2</span></span></td>
<td><span data-ttu-id="8d685-610">2. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-610">Product 2</span></span></td>
<td><span data-ttu-id="8d685-611">20.</span><span class="sxs-lookup"><span data-stu-id="8d685-611">20</span></span></td>
<td><span data-ttu-id="8d685-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="8d685-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8d685-613">178.44</span><span class="sxs-lookup"><span data-stu-id="8d685-613">178.44</span></span></td>
<td><span data-ttu-id="8d685-614">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8d685-615">Prod 1</span></span></td>
<td><span data-ttu-id="8d685-616">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-616">Product 1</span></span></td>
<td><span data-ttu-id="8d685-617">60</span><span class="sxs-lookup"><span data-stu-id="8d685-617">60</span></span></td>
<td><span data-ttu-id="8d685-618">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="8d685-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8d685-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8d685-619">4,487.12</span></span></td>
<td><span data-ttu-id="8d685-620">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8d685-621">Prod 2</span></span></td>
<td><span data-ttu-id="8d685-622">2. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-622">Product 2</span></span></td>
<td><span data-ttu-id="8d685-623">20.</span><span class="sxs-lookup"><span data-stu-id="8d685-623">20</span></span></td>
<td><span data-ttu-id="8d685-624">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="8d685-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8d685-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8d685-625">1,495.71</span></span></td>
<td><span data-ttu-id="8d685-626">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8d685-627">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="8d685-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-628">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-628">Cost object</span></span></th>
<th><span data-ttu-id="8d685-629">Lielums</span><span class="sxs-lookup"><span data-stu-id="8d685-629">Magnitude</span></span></th>
<th><span data-ttu-id="8d685-630">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="8d685-630">Allocation factor</span></span></th>
<th><span data-ttu-id="8d685-631">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-631">Amount</span></span></th>
<th><span data-ttu-id="8d685-632">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="8d685-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8d685-633">Prod 1</span></span></td>
<td><span data-ttu-id="8d685-634">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-634">Product 1</span></span></td>
<td><span data-ttu-id="8d685-635">80</span><span class="sxs-lookup"><span data-stu-id="8d685-635">80</span></span></td>
<td><span data-ttu-id="8d685-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="8d685-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8d685-637">241.05</span><span class="sxs-lookup"><span data-stu-id="8d685-637">241.05</span></span></td>
<td><span data-ttu-id="8d685-638">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8d685-639">Prod 2</span></span></td>
<td><span data-ttu-id="8d685-640">2. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-640">Product 2</span></span></td>
<td><span data-ttu-id="8d685-641">15</span><span class="sxs-lookup"><span data-stu-id="8d685-641">15</span></span></td>
<td><span data-ttu-id="8d685-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="8d685-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8d685-643">45.20</span><span class="sxs-lookup"><span data-stu-id="8d685-643">45.20</span></span></td>
<td><span data-ttu-id="8d685-644">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8d685-645">Prod 1</span></span></td>
<td><span data-ttu-id="8d685-646">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-646">Product 1</span></span></td>
<td><span data-ttu-id="8d685-647">80</span><span class="sxs-lookup"><span data-stu-id="8d685-647">80</span></span></td>
<td><span data-ttu-id="8d685-648">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="8d685-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8d685-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8d685-649">2,507.09</span></span></td>
<td><span data-ttu-id="8d685-650">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8d685-651">Prod 2</span></span></td>
<td><span data-ttu-id="8d685-652">2. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-652">Product 2</span></span></td>
<td><span data-ttu-id="8d685-653">15</span><span class="sxs-lookup"><span data-stu-id="8d685-653">15</span></span></td>
<td><span data-ttu-id="8d685-654">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="8d685-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8d685-655">470.08</span><span class="sxs-lookup"><span data-stu-id="8d685-655">470.08</span></span></td>
<td><span data-ttu-id="8d685-656">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8d685-657">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="8d685-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d685-658">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="8d685-658">Journal</span></span></th>
<th><span data-ttu-id="8d685-659">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="8d685-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8d685-660">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="8d685-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8d685-661">Versija</span><span class="sxs-lookup"><span data-stu-id="8d685-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-662">00004</span><span class="sxs-lookup"><span data-stu-id="8d685-662">00004</span></span></td>
<td><span data-ttu-id="8d685-663">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="8d685-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="8d685-664">Finanšu</span><span class="sxs-lookup"><span data-stu-id="8d685-664">Fiscal</span></span></td>
<td><span data-ttu-id="8d685-665">2017</span><span class="sxs-lookup"><span data-stu-id="8d685-665">2017</span></span></td>
<td><span data-ttu-id="8d685-666">Periods 1</span><span class="sxs-lookup"><span data-stu-id="8d685-666">Period 1</span></span></td>
<td><span data-ttu-id="8d685-667">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="8d685-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="8d685-668">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="8d685-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d685-669">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="8d685-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8d685-670">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d685-671">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="8d685-671">Cost element</span></span></th>
<th><span data-ttu-id="8d685-672">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="8d685-672">Cost behavior</span></span></th>
<th><span data-ttu-id="8d685-673">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-674">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-675">CC001</span><span class="sxs-lookup"><span data-stu-id="8d685-675">CC001</span></span></td>
<td><span data-ttu-id="8d685-676">HR</span><span class="sxs-lookup"><span data-stu-id="8d685-676">HR</span></span></td>
<td><span data-ttu-id="8d685-677">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-677">10001</span></span></td>
<td><span data-ttu-id="8d685-678">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-678">Electricity</span></span></td>
<td><span data-ttu-id="8d685-679">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-679">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-680">500,00</span><span class="sxs-lookup"><span data-stu-id="8d685-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-681">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-682">CC001</span><span class="sxs-lookup"><span data-stu-id="8d685-682">CC001</span></span></td>
<td><span data-ttu-id="8d685-683">HR</span><span class="sxs-lookup"><span data-stu-id="8d685-683">HR</span></span></td>
<td><span data-ttu-id="8d685-684">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-684">10001</span></span></td>
<td><span data-ttu-id="8d685-685">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-685">Electricity</span></span></td>
<td><span data-ttu-id="8d685-686">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-686">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="8d685-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-688">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-689">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-689">CC002</span></span></td>
<td><span data-ttu-id="8d685-690">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-690">Finance</span></span></td>
<td><span data-ttu-id="8d685-691">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-691">10001</span></span></td>
<td><span data-ttu-id="8d685-692">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-692">Electricity</span></span></td>
<td><span data-ttu-id="8d685-693">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-693">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-694">675.00</span><span class="sxs-lookup"><span data-stu-id="8d685-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-695">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-696">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-696">CC002</span></span></td>
<td><span data-ttu-id="8d685-697">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-697">Finance</span></span></td>
<td><span data-ttu-id="8d685-698">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-698">10001</span></span></td>
<td><span data-ttu-id="8d685-699">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-699">Electricity</span></span></td>
<td><span data-ttu-id="8d685-700">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-700">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="8d685-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-702">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-703">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-703">CC003</span></span></td>
<td><span data-ttu-id="8d685-704">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-704">Assembly</span></span></td>
<td><span data-ttu-id="8d685-705">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-705">10001</span></span></td>
<td><span data-ttu-id="8d685-706">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-706">Electricity</span></span></td>
<td><span data-ttu-id="8d685-707">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-707">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-708">713.75</span><span class="sxs-lookup"><span data-stu-id="8d685-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-709">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-710">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-710">CC003</span></span></td>
<td><span data-ttu-id="8d685-711">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-711">Assembly</span></span></td>
<td><span data-ttu-id="8d685-712">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-712">10001</span></span></td>
<td><span data-ttu-id="8d685-713">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-713">Electricity</span></span></td>
<td><span data-ttu-id="8d685-714">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-714">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="8d685-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-716">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-717">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-717">CC003</span></span></td>
<td><span data-ttu-id="8d685-718">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="8d685-718">Packaging</span></span></td>
<td><span data-ttu-id="8d685-719">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-719">10001</span></span></td>
<td><span data-ttu-id="8d685-720">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-720">Electricity</span></span></td>
<td><span data-ttu-id="8d685-721">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-721">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-722">286.25</span><span class="sxs-lookup"><span data-stu-id="8d685-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-723">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-724">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-724">CC003</span></span></td>
<td><span data-ttu-id="8d685-725">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="8d685-725">Packaging</span></span></td>
<td><span data-ttu-id="8d685-726">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-726">10001</span></span></td>
<td><span data-ttu-id="8d685-727">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-727">Electricity</span></span></td>
<td><span data-ttu-id="8d685-728">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-728">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="8d685-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-730">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8d685-731">Prod 1</span></span></td>
<td><span data-ttu-id="8d685-732">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-732">Product 1</span></span></td>
<td><span data-ttu-id="8d685-733">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-733">10001</span></span></td>
<td><span data-ttu-id="8d685-734">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-734">Electricity</span></span></td>
<td><span data-ttu-id="8d685-735">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-735">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-736">776.36</span><span class="sxs-lookup"><span data-stu-id="8d685-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-737">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8d685-738">Prod 1</span></span></td>
<td><span data-ttu-id="8d685-739">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-739">Product 1</span></span></td>
<td><span data-ttu-id="8d685-740">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-740">10001</span></span></td>
<td><span data-ttu-id="8d685-741">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-741">Electricity</span></span></td>
<td><span data-ttu-id="8d685-742">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-742">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8d685-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-744">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8d685-745">Prod 2</span></span></td>
<td><span data-ttu-id="8d685-746">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-746">Product 1</span></span></td>
<td><span data-ttu-id="8d685-747">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-747">10001</span></span></td>
<td><span data-ttu-id="8d685-748">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-748">Electricity</span></span></td>
<td><span data-ttu-id="8d685-749">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-749">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-750">223.64</span><span class="sxs-lookup"><span data-stu-id="8d685-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-751">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="8d685-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8d685-752">Prod 2</span></span></td>
<td><span data-ttu-id="8d685-753">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-753">Product 1</span></span></td>
<td><span data-ttu-id="8d685-754">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-754">10001</span></span></td>
<td><span data-ttu-id="8d685-755">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-755">Electricity</span></span></td>
<td><span data-ttu-id="8d685-756">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-756">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8d685-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8d685-758">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="8d685-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8d685-759">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8d685-760">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="8d685-760">Cost element</span></span></th>
<th><span data-ttu-id="8d685-761">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="8d685-761">Cost behavior</span></span></th>
<th><span data-ttu-id="8d685-762">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-762">Amount</span></span></th>
<th><span data-ttu-id="8d685-763">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="8d685-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d685-764">CC001</span><span class="sxs-lookup"><span data-stu-id="8d685-764">CC001</span></span></td>
<td><span data-ttu-id="8d685-765">HR</span><span class="sxs-lookup"><span data-stu-id="8d685-765">HR</span></span></td>
<td><span data-ttu-id="8d685-766">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-766">10001</span></span></td>
<td><span data-ttu-id="8d685-767">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-767">Electricity</span></span></td>
<td><span data-ttu-id="8d685-768">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-768">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="8d685-769">-500.00</span></span></td>
<td><span data-ttu-id="8d685-770">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-771">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-771">CC002</span></span></td>
<td><span data-ttu-id="8d685-772">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-772">Finance</span></span></td>
<td><span data-ttu-id="8d685-773">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-773">10001</span></span></td>
<td><span data-ttu-id="8d685-774">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-774">Electricity</span></span></td>
<td><span data-ttu-id="8d685-775">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-775">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-776">175.00</span><span class="sxs-lookup"><span data-stu-id="8d685-776">175.00</span></span></td>
<td><span data-ttu-id="8d685-777">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-778">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-778">CC003</span></span></td>
<td><span data-ttu-id="8d685-779">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-779">Assembly</span></span></td>
<td><span data-ttu-id="8d685-780">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-780">10001</span></span></td>
<td><span data-ttu-id="8d685-781">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-781">Electricity</span></span></td>
<td><span data-ttu-id="8d685-782">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-782">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-783">275.00</span><span class="sxs-lookup"><span data-stu-id="8d685-783">275.00</span></span></td>
<td><span data-ttu-id="8d685-784">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-785">CC004</span><span class="sxs-lookup"><span data-stu-id="8d685-785">CC004</span></span></td>
<td><span data-ttu-id="8d685-786">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="8d685-786">Packaging</span></span></td>
<td><span data-ttu-id="8d685-787">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-787">10001</span></span></td>
<td><span data-ttu-id="8d685-788">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-788">Electricity</span></span></td>
<td><span data-ttu-id="8d685-789">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-789">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-790">50,00</span><span class="sxs-lookup"><span data-stu-id="8d685-790">50,00</span></span></td>
<td><span data-ttu-id="8d685-791">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-792">CC001</span><span class="sxs-lookup"><span data-stu-id="8d685-792">CC001</span></span></td>
<td><span data-ttu-id="8d685-793">HR</span><span class="sxs-lookup"><span data-stu-id="8d685-793">HR</span></span></td>
<td><span data-ttu-id="8d685-794">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-794">10001</span></span></td>
<td><span data-ttu-id="8d685-795">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-795">Electricity</span></span></td>
<td><span data-ttu-id="8d685-796">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-796">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-797">-1245,71</span><span class="sxs-lookup"><span data-stu-id="8d685-797">-1,245.71</span></span></td>
<td><span data-ttu-id="8d685-798">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-799">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-799">CC002</span></span></td>
<td><span data-ttu-id="8d685-800">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-800">Finance</span></span></td>
<td><span data-ttu-id="8d685-801">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-801">10001</span></span></td>
<td><span data-ttu-id="8d685-802">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-802">Electricity</span></span></td>
<td><span data-ttu-id="8d685-803">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-803">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-804">436.00</span><span class="sxs-lookup"><span data-stu-id="8d685-804">436.00</span></span></td>
<td><span data-ttu-id="8d685-805">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-806">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-806">CC003</span></span></td>
<td><span data-ttu-id="8d685-807">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-807">Assembly</span></span></td>
<td><span data-ttu-id="8d685-808">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-808">10001</span></span></td>
<td><span data-ttu-id="8d685-809">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-809">Electricity</span></span></td>
<td><span data-ttu-id="8d685-810">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-810">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-811">685.14</span><span class="sxs-lookup"><span data-stu-id="8d685-811">685.14</span></span></td>
<td><span data-ttu-id="8d685-812">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-813">CC004</span><span class="sxs-lookup"><span data-stu-id="8d685-813">CC004</span></span></td>
<td><span data-ttu-id="8d685-814">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="8d685-814">Packaging</span></span></td>
<td><span data-ttu-id="8d685-815">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-815">10001</span></span></td>
<td><span data-ttu-id="8d685-816">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-816">Electricity</span></span></td>
<td><span data-ttu-id="8d685-817">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-817">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-818">124.57</span><span class="sxs-lookup"><span data-stu-id="8d685-818">124.57</span></span></td>
<td><span data-ttu-id="8d685-819">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-820">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-820">CC002</span></span></td>
<td><span data-ttu-id="8d685-821">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-821">Finance</span></span></td>
<td><span data-ttu-id="8d685-822">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-822">10001</span></span></td>
<td><span data-ttu-id="8d685-823">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-823">Electricity</span></span></td>
<td><span data-ttu-id="8d685-824">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-824">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="8d685-825">-675.00</span></span></td>
<td><span data-ttu-id="8d685-826">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-827">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-827">CC003</span></span></td>
<td><span data-ttu-id="8d685-828">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-828">Assembly</span></span></td>
<td><span data-ttu-id="8d685-829">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-829">10001</span></span></td>
<td><span data-ttu-id="8d685-830">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-830">Electricity</span></span></td>
<td><span data-ttu-id="8d685-831">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-831">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-832">438.75</span><span class="sxs-lookup"><span data-stu-id="8d685-832">438.75</span></span></td>
<td><span data-ttu-id="8d685-833">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-834">CC004</span><span class="sxs-lookup"><span data-stu-id="8d685-834">CC004</span></span></td>
<td><span data-ttu-id="8d685-835">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="8d685-835">Packaging</span></span></td>
<td><span data-ttu-id="8d685-836">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-836">10001</span></span></td>
<td><span data-ttu-id="8d685-837">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-837">Electricity</span></span></td>
<td><span data-ttu-id="8d685-838">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-838">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-839">236.25</span><span class="sxs-lookup"><span data-stu-id="8d685-839">236.25</span></span></td>
<td><span data-ttu-id="8d685-840">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-841">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-841">CC002</span></span></td>
<td><span data-ttu-id="8d685-842">Finanses</span><span class="sxs-lookup"><span data-stu-id="8d685-842">Finance</span></span></td>
<td><span data-ttu-id="8d685-843">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-843">10001</span></span></td>
<td><span data-ttu-id="8d685-844">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-844">Electricity</span></span></td>
<td><span data-ttu-id="8d685-845">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-845">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-846">-8150,29</span><span class="sxs-lookup"><span data-stu-id="8d685-846">-8,150.29</span></span></td>
<td><span data-ttu-id="8d685-847">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-848">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-848">CC003</span></span></td>
<td><span data-ttu-id="8d685-849">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-849">Assembly</span></span></td>
<td><span data-ttu-id="8d685-850">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-850">10001</span></span></td>
<td><span data-ttu-id="8d685-851">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-851">Electricity</span></span></td>
<td><span data-ttu-id="8d685-852">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-852">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8d685-853">5,297.69</span></span></td>
<td><span data-ttu-id="8d685-854">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-855">CC004</span><span class="sxs-lookup"><span data-stu-id="8d685-855">CC004</span></span></td>
<td><span data-ttu-id="8d685-856">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="8d685-856">Packaging</span></span></td>
<td><span data-ttu-id="8d685-857">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-857">10001</span></span></td>
<td><span data-ttu-id="8d685-858">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-858">Electricity</span></span></td>
<td><span data-ttu-id="8d685-859">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-859">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8d685-860">2,852.60</span></span></td>
<td><span data-ttu-id="8d685-861">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-862">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-862">CC003</span></span></td>
<td><span data-ttu-id="8d685-863">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-863">Assembly</span></span></td>
<td><span data-ttu-id="8d685-864">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-864">10001</span></span></td>
<td><span data-ttu-id="8d685-865">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-865">Electricity</span></span></td>
<td><span data-ttu-id="8d685-866">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-866">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="8d685-867">-713.75</span></span></td>
<td><span data-ttu-id="8d685-868">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8d685-869">Prod 1</span></span></td>
<td><span data-ttu-id="8d685-870">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-870">Product 1</span></span></td>
<td><span data-ttu-id="8d685-871">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-871">10001</span></span></td>
<td><span data-ttu-id="8d685-872">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-872">Electricity</span></span></td>
<td><span data-ttu-id="8d685-873">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-873">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-874">535.31</span><span class="sxs-lookup"><span data-stu-id="8d685-874">535.31</span></span></td>
<td><span data-ttu-id="8d685-875">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8d685-876">Prod 2</span></span></td>
<td><span data-ttu-id="8d685-877">2. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-877">Product 2</span></span></td>
<td><span data-ttu-id="8d685-878">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-878">10001</span></span></td>
<td><span data-ttu-id="8d685-879">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-879">Electricity</span></span></td>
<td><span data-ttu-id="8d685-880">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-880">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-881">178.44</span><span class="sxs-lookup"><span data-stu-id="8d685-881">178.44</span></span></td>
<td><span data-ttu-id="8d685-882">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-883">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-883">CC003</span></span></td>
<td><span data-ttu-id="8d685-884">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-884">Assembly</span></span></td>
<td><span data-ttu-id="8d685-885">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-885">10001</span></span></td>
<td><span data-ttu-id="8d685-886">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-886">Electricity</span></span></td>
<td><span data-ttu-id="8d685-887">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-887">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-888">-5982,83</span><span class="sxs-lookup"><span data-stu-id="8d685-888">-5,982.83</span></span></td>
<td><span data-ttu-id="8d685-889">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8d685-890">Prod 1</span></span></td>
<td><span data-ttu-id="8d685-891">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-891">Product 1</span></span></td>
<td><span data-ttu-id="8d685-892">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-892">10001</span></span></td>
<td><span data-ttu-id="8d685-893">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-893">Electricity</span></span></td>
<td><span data-ttu-id="8d685-894">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-894">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8d685-895">4,487.12</span></span></td>
<td><span data-ttu-id="8d685-896">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8d685-897">Prod 2</span></span></td>
<td><span data-ttu-id="8d685-898">2. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-898">Product 2</span></span></td>
<td><span data-ttu-id="8d685-899">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-899">10001</span></span></td>
<td><span data-ttu-id="8d685-900">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-900">Electricity</span></span></td>
<td><span data-ttu-id="8d685-901">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-901">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8d685-902">1,495.71</span></span></td>
<td><span data-ttu-id="8d685-903">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-904">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-904">CC003</span></span></td>
<td><span data-ttu-id="8d685-905">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-905">Assembly</span></span></td>
<td><span data-ttu-id="8d685-906">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-906">10001</span></span></td>
<td><span data-ttu-id="8d685-907">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-907">Electricity</span></span></td>
<td><span data-ttu-id="8d685-908">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-908">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="8d685-909">-286.25</span></span></td>
<td><span data-ttu-id="8d685-910">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8d685-911">Prod 1</span></span></td>
<td><span data-ttu-id="8d685-912">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-912">Product 1</span></span></td>
<td><span data-ttu-id="8d685-913">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-913">10001</span></span></td>
<td><span data-ttu-id="8d685-914">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-914">Electricity</span></span></td>
<td><span data-ttu-id="8d685-915">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-915">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-916">241.05</span><span class="sxs-lookup"><span data-stu-id="8d685-916">241.05</span></span></td>
<td><span data-ttu-id="8d685-917">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8d685-918">Prod 2</span></span></td>
<td><span data-ttu-id="8d685-919">2. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-919">Product 2</span></span></td>
<td><span data-ttu-id="8d685-920">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-920">10001</span></span></td>
<td><span data-ttu-id="8d685-921">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-921">Electricity</span></span></td>
<td><span data-ttu-id="8d685-922">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-922">Fixed cost</span></span></td>
<td><span data-ttu-id="8d685-923">45.20</span><span class="sxs-lookup"><span data-stu-id="8d685-923">45.20</span></span></td>
<td><span data-ttu-id="8d685-924">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-925">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-925">CC003</span></span></td>
<td><span data-ttu-id="8d685-926">Montāža</span><span class="sxs-lookup"><span data-stu-id="8d685-926">Assembly</span></span></td>
<td><span data-ttu-id="8d685-927">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-927">10001</span></span></td>
<td><span data-ttu-id="8d685-928">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-928">Electricity</span></span></td>
<td><span data-ttu-id="8d685-929">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-929">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-930">-2977,17</span><span class="sxs-lookup"><span data-stu-id="8d685-930">-2,977.17</span></span></td>
<td><span data-ttu-id="8d685-931">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8d685-932">Prod 1</span></span></td>
<td><span data-ttu-id="8d685-933">1. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-933">Product 1</span></span></td>
<td><span data-ttu-id="8d685-934">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-934">10001</span></span></td>
<td><span data-ttu-id="8d685-935">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-935">Electricity</span></span></td>
<td><span data-ttu-id="8d685-936">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-936">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8d685-937">2,507.09</span></span></td>
<td><span data-ttu-id="8d685-938">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d685-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8d685-939">Prod 2</span></span></td>
<td><span data-ttu-id="8d685-940">2. prece</span><span class="sxs-lookup"><span data-stu-id="8d685-940">Product 2</span></span></td>
<td><span data-ttu-id="8d685-941">10001</span><span class="sxs-lookup"><span data-stu-id="8d685-941">10001</span></span></td>
<td><span data-ttu-id="8d685-942">Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-942">Electricity</span></span></td>
<td><span data-ttu-id="8d685-943">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-943">Variable cost</span></span></td>
<td><span data-ttu-id="8d685-944">470.08</span><span class="sxs-lookup"><span data-stu-id="8d685-944">470.08</span></span></td>
<td><span data-ttu-id="8d685-945">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="8d685-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="8d685-946">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="8d685-946">Conclusion</span></span>
<span data-ttu-id="8d685-947">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="8d685-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="8d685-948">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="8d685-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="8d685-949">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="8d685-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="8d685-950">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="8d685-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="8d685-951">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="8d685-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="8d685-952">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="8d685-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="8d685-953">Summa</span><span class="sxs-lookup"><span data-stu-id="8d685-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8d685-954">CC099</span><span class="sxs-lookup"><span data-stu-id="8d685-954">CC099</span></span></th>
<th><span data-ttu-id="8d685-955">CC001</span><span class="sxs-lookup"><span data-stu-id="8d685-955">CC001</span></span></th>
<th><span data-ttu-id="8d685-956">CC002</span><span class="sxs-lookup"><span data-stu-id="8d685-956">CC002</span></span></th>
<th><span data-ttu-id="8d685-957">CC003</span><span class="sxs-lookup"><span data-stu-id="8d685-957">CC003</span></span></th>
<th><span data-ttu-id="8d685-958">CC004</span><span class="sxs-lookup"><span data-stu-id="8d685-958">CC004</span></span></th>
<th><span data-ttu-id="8d685-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8d685-959">Proj 1</span></span></th>
<th><span data-ttu-id="8d685-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8d685-960">Proj 2</span></span></th>
<th><span data-ttu-id="8d685-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8d685-961">Prod 1</span></span></th>
<th><span data-ttu-id="8d685-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8d685-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="8d685-963">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="8d685-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8d685-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8d685-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8d685-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8d685-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8d685-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="8d685-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="8d685-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="8d685-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="8d685-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="8d685-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="8d685-973">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="8d685-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-974">0,00</span><span class="sxs-lookup"><span data-stu-id="8d685-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="8d685-975">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-976">0,00</span><span class="sxs-lookup"><span data-stu-id="8d685-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-977">0,00</span><span class="sxs-lookup"><span data-stu-id="8d685-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-978">0,00</span><span class="sxs-lookup"><span data-stu-id="8d685-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-979">0,00</span><span class="sxs-lookup"><span data-stu-id="8d685-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-980">0,00</span><span class="sxs-lookup"><span data-stu-id="8d685-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8d685-981">776.36</span><span class="sxs-lookup"><span data-stu-id="8d685-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-982">223.64</span><span class="sxs-lookup"><span data-stu-id="8d685-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="8d685-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="8d685-984">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="8d685-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-985">000</span><span class="sxs-lookup"><span data-stu-id="8d685-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-986">0,00</span><span class="sxs-lookup"><span data-stu-id="8d685-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-987">0,00</span><span class="sxs-lookup"><span data-stu-id="8d685-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-988">0,00</span><span class="sxs-lookup"><span data-stu-id="8d685-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-989">0,00</span><span class="sxs-lookup"><span data-stu-id="8d685-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-990">30,00</span><span class="sxs-lookup"><span data-stu-id="8d685-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-991">10,00</span><span class="sxs-lookup"><span data-stu-id="8d685-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8d685-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8d685-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8d685-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="8d685-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8d685-995">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="8d685-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="8d685-996">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="8d685-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="8d685-997">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="8d685-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="8d685-998">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="8d685-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="8d685-999">Papildinformāciju skatiet sadaļā Izmaksu apkopošanas politika.</span><span class="sxs-lookup"><span data-stu-id="8d685-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="8d685-1000">(Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)</span><span class="sxs-lookup"><span data-stu-id="8d685-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




