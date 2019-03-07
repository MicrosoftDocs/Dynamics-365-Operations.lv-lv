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
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "335121"
---
# <a name="overhead-calculation"></a><span data-ttu-id="fe44d-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="fe44d-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe44d-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="fe44d-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="fe44d-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="fe44d-105">Term definition</span></span>
---------------

<span data-ttu-id="fe44d-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="fe44d-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="fe44d-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="fe44d-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="fe44d-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="fe44d-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="fe44d-109">Īre</span><span class="sxs-lookup"><span data-stu-id="fe44d-109">Rent</span></span>
-   <span data-ttu-id="fe44d-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-110">Electricity</span></span>
-   <span data-ttu-id="fe44d-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="fe44d-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="fe44d-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="fe44d-112">Overhead calculation overview</span></span>
<span data-ttu-id="fe44d-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="fe44d-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="fe44d-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="fe44d-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="fe44d-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="fe44d-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="fe44d-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="fe44d-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="fe44d-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="fe44d-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="fe44d-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="fe44d-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="fe44d-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="fe44d-119">Version type</span></span>
-   <span data-ttu-id="fe44d-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="fe44d-120">Date and time</span></span>
-   <span data-ttu-id="fe44d-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="fe44d-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="fe44d-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="fe44d-122">Fiscal year</span></span>
-   <span data-ttu-id="fe44d-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="fe44d-123">Fiscal period</span></span>

<span data-ttu-id="fe44d-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="fe44d-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="fe44d-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="fe44d-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="fe44d-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="fe44d-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="fe44d-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="fe44d-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="fe44d-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="fe44d-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="fe44d-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="fe44d-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="fe44d-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="fe44d-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="fe44d-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="fe44d-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="fe44d-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="fe44d-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="fe44d-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="fe44d-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="fe44d-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="fe44d-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="fe44d-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="fe44d-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="fe44d-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="fe44d-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="fe44d-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fe44d-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fe44d-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="fe44d-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fe44d-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="fe44d-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="fe44d-140">Main account</span></span></th>
<th><span data-ttu-id="fe44d-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="fe44d-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="fe44d-143">CC099</span><span class="sxs-lookup"><span data-stu-id="fe44d-143">CC099</span></span></td>
<td><span data-ttu-id="fe44d-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fe44d-144">Default cost center</span></span></td>
<td><span data-ttu-id="fe44d-145">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-145">10001</span></span></td>
<td><span data-ttu-id="fe44d-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-146">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="fe44d-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="fe44d-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="fe44d-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="fe44d-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="fe44d-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="fe44d-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="fe44d-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="fe44d-151">Define the cost behavior rule</span></span>

<span data-ttu-id="fe44d-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="fe44d-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="fe44d-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="fe44d-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="fe44d-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="fe44d-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="fe44d-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="fe44d-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="fe44d-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="fe44d-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="fe44d-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="fe44d-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="fe44d-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="fe44d-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fe44d-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fe44d-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fe44d-160">Journal</span></span></th>
<th><span data-ttu-id="fe44d-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="fe44d-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="fe44d-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="fe44d-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="fe44d-163">Versija</span><span class="sxs-lookup"><span data-stu-id="fe44d-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-164">00001</span><span class="sxs-lookup"><span data-stu-id="fe44d-164">00001</span></span></td>
<td><span data-ttu-id="fe44d-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="fe44d-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="fe44d-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="fe44d-166">Fiscal</span></span></td>
<td><span data-ttu-id="fe44d-167">2017</span><span class="sxs-lookup"><span data-stu-id="fe44d-167">2017</span></span></td>
<td><span data-ttu-id="fe44d-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-168">Period 1</span></span></td>
<td><span data-ttu-id="fe44d-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="fe44d-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="fe44d-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="fe44d-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fe44d-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fe44d-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="fe44d-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fe44d-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fe44d-173">Cost element</span></span></th>
<th><span data-ttu-id="fe44d-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fe44d-174">Cost behavior</span></span></th>
<th><span data-ttu-id="fe44d-175">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="fe44d-177">CC099</span><span class="sxs-lookup"><span data-stu-id="fe44d-177">CC099</span></span></td>
<td><span data-ttu-id="fe44d-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fe44d-178">Default cost center</span></span></td>
<td><span data-ttu-id="fe44d-179">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-179">10001</span></span></td>
<td><span data-ttu-id="fe44d-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-180">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="fe44d-181">Unclassified</span></span></td>
<td><span data-ttu-id="fe44d-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="fe44d-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="fe44d-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fe44d-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fe44d-185">Cost element</span></span></th>
<th><span data-ttu-id="fe44d-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fe44d-186">Cost behavior</span></span></th>
<th><span data-ttu-id="fe44d-187">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-187">Amount</span></span></th>
<th><span data-ttu-id="fe44d-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fe44d-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-189">CC099</span><span class="sxs-lookup"><span data-stu-id="fe44d-189">CC099</span></span></td>
<td><span data-ttu-id="fe44d-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fe44d-190">Default cost center</span></span></td>
<td><span data-ttu-id="fe44d-191">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-191">10001</span></span></td>
<td><span data-ttu-id="fe44d-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-192">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="fe44d-193">Unclassified</span></span></td>
<td><span data-ttu-id="fe44d-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-194">10,000.00</span></span></td>
<td><span data-ttu-id="fe44d-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-196">CC099</span><span class="sxs-lookup"><span data-stu-id="fe44d-196">CC099</span></span></td>
<td><span data-ttu-id="fe44d-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fe44d-197">Default cost center</span></span></td>
<td><span data-ttu-id="fe44d-198">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-198">10001</span></span></td>
<td><span data-ttu-id="fe44d-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-199">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="fe44d-200">Unclassified</span></span></td>
<td><span data-ttu-id="fe44d-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-201">-10,000.00</span></span></td>
<td><span data-ttu-id="fe44d-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-203">CC099</span><span class="sxs-lookup"><span data-stu-id="fe44d-203">CC099</span></span></td>
<td><span data-ttu-id="fe44d-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fe44d-204">Default cost center</span></span></td>
<td><span data-ttu-id="fe44d-205">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-205">10001</span></span></td>
<td><span data-ttu-id="fe44d-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-206">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-207">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-208">1,000.00</span></span></td>
<td><span data-ttu-id="fe44d-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-210">CC099</span><span class="sxs-lookup"><span data-stu-id="fe44d-210">CC099</span></span></td>
<td><span data-ttu-id="fe44d-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fe44d-211">Default cost center</span></span></td>
<td><span data-ttu-id="fe44d-212">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-212">10001</span></span></td>
<td><span data-ttu-id="fe44d-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-213">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-214">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="fe44d-215">9,000.00</span></span></td>
<td><span data-ttu-id="fe44d-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fe44d-217">Sīkāku informāciju skatiet šeit: [Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="fe44d-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="fe44d-218">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="fe44d-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="fe44d-219">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="fe44d-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="fe44d-220">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="fe44d-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="fe44d-221">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="fe44d-221">Define the cost distribution rule</span></span>

<span data-ttu-id="fe44d-222">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="fe44d-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="fe44d-223">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="fe44d-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="fe44d-224">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="fe44d-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="fe44d-225">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="fe44d-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="fe44d-226">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="fe44d-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="fe44d-227">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="fe44d-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-228">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-228">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="fe44d-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-230">CC001</span><span class="sxs-lookup"><span data-stu-id="fe44d-230">CC001</span></span></td>
<td><span data-ttu-id="fe44d-231">HR</span><span class="sxs-lookup"><span data-stu-id="fe44d-231">HR</span></span></td>
<td><span data-ttu-id="fe44d-232">1000</span><span class="sxs-lookup"><span data-stu-id="fe44d-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-233">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-233">CC002</span></span></td>
<td><span data-ttu-id="fe44d-234">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-234">Finance</span></span></td>
<td><span data-ttu-id="fe44d-235">6,000</span><span class="sxs-lookup"><span data-stu-id="fe44d-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-236">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-236">CC003</span></span></td>
<td><span data-ttu-id="fe44d-237">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-237">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-238">0</span><span class="sxs-lookup"><span data-stu-id="fe44d-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fe44d-239">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="fe44d-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-240">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-240">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-241">Lielums</span><span class="sxs-lookup"><span data-stu-id="fe44d-241">Magnitude</span></span></th>
<th><span data-ttu-id="fe44d-242">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fe44d-242">Allocation factor</span></span></th>
<th><span data-ttu-id="fe44d-243">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-244">CC001</span><span class="sxs-lookup"><span data-stu-id="fe44d-244">CC001</span></span></td>
<td><span data-ttu-id="fe44d-245">HR</span><span class="sxs-lookup"><span data-stu-id="fe44d-245">HR</span></span></td>
<td><span data-ttu-id="fe44d-246">1000</span><span class="sxs-lookup"><span data-stu-id="fe44d-246">1,000</span></span></td>
<td><span data-ttu-id="fe44d-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="fe44d-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="fe44d-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-249">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-249">CC002</span></span></td>
<td><span data-ttu-id="fe44d-250">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-250">Finance</span></span></td>
<td><span data-ttu-id="fe44d-251">6,000</span><span class="sxs-lookup"><span data-stu-id="fe44d-251">6,000</span></span></td>
<td><span data-ttu-id="fe44d-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="fe44d-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="fe44d-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-254">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-254">CC003</span></span></td>
<td><span data-ttu-id="fe44d-255">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-255">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-256">0</span><span class="sxs-lookup"><span data-stu-id="fe44d-256">0</span></span></td>
<td><span data-ttu-id="fe44d-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="fe44d-258">0,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fe44d-259">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="fe44d-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="fe44d-260">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="fe44d-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-261">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-261">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-262">Formula</span><span class="sxs-lookup"><span data-stu-id="fe44d-262">Formula</span></span></th>
<th><span data-ttu-id="fe44d-263">Lielums</span><span class="sxs-lookup"><span data-stu-id="fe44d-263">Magnitude</span></span></th>
<th><span data-ttu-id="fe44d-264">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fe44d-264">Allocation factor</span></span></th>
<th><span data-ttu-id="fe44d-265">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-266">CC001</span><span class="sxs-lookup"><span data-stu-id="fe44d-266">CC001</span></span></td>
<td><span data-ttu-id="fe44d-267">HR</span><span class="sxs-lookup"><span data-stu-id="fe44d-267">HR</span></span></td>
<td><span data-ttu-id="fe44d-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="fe44d-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="fe44d-269">1.</span><span class="sxs-lookup"><span data-stu-id="fe44d-269">1</span></span></td>
<td><span data-ttu-id="fe44d-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="fe44d-271">500,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-272">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-272">CC002</span></span></td>
<td><span data-ttu-id="fe44d-273">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-273">Finance</span></span></td>
<td><span data-ttu-id="fe44d-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="fe44d-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="fe44d-275">1.</span><span class="sxs-lookup"><span data-stu-id="fe44d-275">1</span></span></td>
<td><span data-ttu-id="fe44d-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="fe44d-277">500,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-278">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-278">CC003</span></span></td>
<td><span data-ttu-id="fe44d-279">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-279">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="fe44d-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="fe44d-281">0</span><span class="sxs-lookup"><span data-stu-id="fe44d-281">0</span></span></td>
<td><span data-ttu-id="fe44d-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="fe44d-283">0,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="fe44d-284">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fe44d-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fe44d-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fe44d-285">Journal</span></span></th>
<th><span data-ttu-id="fe44d-286">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="fe44d-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="fe44d-287">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="fe44d-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="fe44d-288">Versija</span><span class="sxs-lookup"><span data-stu-id="fe44d-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-289">00002</span><span class="sxs-lookup"><span data-stu-id="fe44d-289">00002</span></span></td>
<td><span data-ttu-id="fe44d-290">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="fe44d-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="fe44d-291">Finanšu</span><span class="sxs-lookup"><span data-stu-id="fe44d-291">Fiscal</span></span></td>
<td><span data-ttu-id="fe44d-292">2017</span><span class="sxs-lookup"><span data-stu-id="fe44d-292">2017</span></span></td>
<td><span data-ttu-id="fe44d-293">Periods 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-293">Period 1</span></span></td>
<td><span data-ttu-id="fe44d-294">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="fe44d-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="fe44d-295">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="fe44d-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fe44d-296">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fe44d-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="fe44d-297">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fe44d-298">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fe44d-298">Cost element</span></span></th>
<th><span data-ttu-id="fe44d-299">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fe44d-299">Cost behavior</span></span></th>
<th><span data-ttu-id="fe44d-300">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-301">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-302">CC099</span><span class="sxs-lookup"><span data-stu-id="fe44d-302">CC099</span></span></td>
<td><span data-ttu-id="fe44d-303">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fe44d-303">Default cost center</span></span></td>
<td><span data-ttu-id="fe44d-304">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-304">10001</span></span></td>
<td><span data-ttu-id="fe44d-305">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-305">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-306">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-306">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-308">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-309">CC099</span><span class="sxs-lookup"><span data-stu-id="fe44d-309">CC099</span></span></td>
<td><span data-ttu-id="fe44d-310">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fe44d-310">Default cost center</span></span></td>
<td><span data-ttu-id="fe44d-311">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-311">10001</span></span></td>
<td><span data-ttu-id="fe44d-312">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-312">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-313">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-313">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="fe44d-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="fe44d-315">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="fe44d-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-316">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fe44d-317">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fe44d-317">Cost element</span></span></th>
<th><span data-ttu-id="fe44d-318">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fe44d-318">Cost behavior</span></span></th>
<th><span data-ttu-id="fe44d-319">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-319">Amount</span></span></th>
<th><span data-ttu-id="fe44d-320">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fe44d-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-321">CC099</span><span class="sxs-lookup"><span data-stu-id="fe44d-321">CC099</span></span></td>
<td><span data-ttu-id="fe44d-322">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fe44d-322">Default cost center</span></span></td>
<td><span data-ttu-id="fe44d-323">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-323">10001</span></span></td>
<td><span data-ttu-id="fe44d-324">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-324">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-325">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-325">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-326">-1000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-326">-1,000.00</span></span></td>
<td><span data-ttu-id="fe44d-327">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-328">CC001</span><span class="sxs-lookup"><span data-stu-id="fe44d-328">CC001</span></span></td>
<td><span data-ttu-id="fe44d-329">HR</span><span class="sxs-lookup"><span data-stu-id="fe44d-329">HR</span></span></td>
<td><span data-ttu-id="fe44d-330">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-330">10001</span></span></td>
<td><span data-ttu-id="fe44d-331">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-331">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-332">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-332">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-333">500,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-333">500.00</span></span></td>
<td><span data-ttu-id="fe44d-334">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-335">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-335">CC002</span></span></td>
<td><span data-ttu-id="fe44d-336">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-336">Finance</span></span></td>
<td><span data-ttu-id="fe44d-337">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-337">10001</span></span></td>
<td><span data-ttu-id="fe44d-338">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-338">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-339">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-339">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-340">500,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-340">500.00</span></span></td>
<td><span data-ttu-id="fe44d-341">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-342">CC099</span><span class="sxs-lookup"><span data-stu-id="fe44d-342">CC099</span></span></td>
<td><span data-ttu-id="fe44d-343">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="fe44d-343">Default cost center</span></span></td>
<td><span data-ttu-id="fe44d-344">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-344">10001</span></span></td>
<td><span data-ttu-id="fe44d-345">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-345">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-346">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-346">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-347">-9,000.00</span></span></td>
<td><span data-ttu-id="fe44d-348">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-349">CC001</span><span class="sxs-lookup"><span data-stu-id="fe44d-349">CC001</span></span></td>
<td><span data-ttu-id="fe44d-350">HR</span><span class="sxs-lookup"><span data-stu-id="fe44d-350">HR</span></span></td>
<td><span data-ttu-id="fe44d-351">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-351">10001</span></span></td>
<td><span data-ttu-id="fe44d-352">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-352">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-353">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-353">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="fe44d-354">1,285.71</span></span></td>
<td><span data-ttu-id="fe44d-355">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-356">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-356">CC002</span></span></td>
<td><span data-ttu-id="fe44d-357">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-357">Finance</span></span></td>
<td><span data-ttu-id="fe44d-358">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-358">10001</span></span></td>
<td><span data-ttu-id="fe44d-359">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-359">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-360">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-360">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="fe44d-361">7,714.29</span></span></td>
<td><span data-ttu-id="fe44d-362">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fe44d-363">Sīkāku informāciju skatiet šeit: [Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="fe44d-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="fe44d-364">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="fe44d-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="fe44d-365">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="fe44d-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="fe44d-366">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="fe44d-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="fe44d-367">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="fe44d-367">Define the overhead rate</span></span>

<span data-ttu-id="fe44d-368">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="fe44d-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="fe44d-369">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="fe44d-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-370">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-370">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-371">Stundas</span><span class="sxs-lookup"><span data-stu-id="fe44d-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-372">Proj 1</span></span></td>
<td><span data-ttu-id="fe44d-373">1. projekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-373">Project 1</span></span></td>
<td><span data-ttu-id="fe44d-374">3.</span><span class="sxs-lookup"><span data-stu-id="fe44d-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-375">Proj 2</span></span></td>
<td><span data-ttu-id="fe44d-376">2. projekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-376">Project 2</span></span></td>
<td><span data-ttu-id="fe44d-377">1.</span><span class="sxs-lookup"><span data-stu-id="fe44d-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fe44d-378">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="fe44d-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-379">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-379">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-380">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fe44d-380">Cost element</span></span></th>
<th><span data-ttu-id="fe44d-381">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fe44d-381">Cost behavior</span></span></th>
<th><span data-ttu-id="fe44d-382">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="fe44d-382">Units</span></span></th>
<th><span data-ttu-id="fe44d-383">Likme</span><span class="sxs-lookup"><span data-stu-id="fe44d-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-384">CC001</span><span class="sxs-lookup"><span data-stu-id="fe44d-384">CC001</span></span></td>
<td><span data-ttu-id="fe44d-385">HR</span><span class="sxs-lookup"><span data-stu-id="fe44d-385">HR</span></span></td>
<td><span data-ttu-id="fe44d-386">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-386">10001</span></span></td>
<td><span data-ttu-id="fe44d-387">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-387">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-388">1</span><span class="sxs-lookup"><span data-stu-id="fe44d-388">1</span></span></td>
<td><span data-ttu-id="fe44d-389">10</span><span class="sxs-lookup"><span data-stu-id="fe44d-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fe44d-390">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="fe44d-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-391">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-391">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-392">Lielums</span><span class="sxs-lookup"><span data-stu-id="fe44d-392">Magnitude</span></span></th>
<th><span data-ttu-id="fe44d-393">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fe44d-393">Cost element</span></span></th>
<th><span data-ttu-id="fe44d-394">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fe44d-394">Allocation factor</span></span></th>
<th><span data-ttu-id="fe44d-395">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-396">Proj 1</span></span></td>
<td><span data-ttu-id="fe44d-397">1. projekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-397">Project 1</span></span></td>
<td><span data-ttu-id="fe44d-398">3.</span><span class="sxs-lookup"><span data-stu-id="fe44d-398">3</span></span></td>
<td><span data-ttu-id="fe44d-399">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-399">10001</span></span></td>
<td><span data-ttu-id="fe44d-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="fe44d-401">30,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-402">Proj 2</span></span></td>
<td><span data-ttu-id="fe44d-403">2. projekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-403">Project 2</span></span></td>
<td><span data-ttu-id="fe44d-404">1.</span><span class="sxs-lookup"><span data-stu-id="fe44d-404">1</span></span></td>
<td><span data-ttu-id="fe44d-405">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-405">10001</span></span></td>
<td><span data-ttu-id="fe44d-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="fe44d-407">10,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="fe44d-408">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fe44d-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fe44d-409">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fe44d-409">Journal</span></span></th>
<th><span data-ttu-id="fe44d-410">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="fe44d-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="fe44d-411">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="fe44d-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="fe44d-412">Versija</span><span class="sxs-lookup"><span data-stu-id="fe44d-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-413">00003</span><span class="sxs-lookup"><span data-stu-id="fe44d-413">00003</span></span></td>
<td><span data-ttu-id="fe44d-414">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="fe44d-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="fe44d-415">Finanšu</span><span class="sxs-lookup"><span data-stu-id="fe44d-415">Fiscal</span></span></td>
<td><span data-ttu-id="fe44d-416">2017</span><span class="sxs-lookup"><span data-stu-id="fe44d-416">2017</span></span></td>
<td><span data-ttu-id="fe44d-417">Periods 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-417">Period 1</span></span></td>
<td><span data-ttu-id="fe44d-418">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="fe44d-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="fe44d-419">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="fe44d-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fe44d-420">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fe44d-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="fe44d-421">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-421">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-422">Lielums</span><span class="sxs-lookup"><span data-stu-id="fe44d-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-423">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-424">Proj 1</span></span></td>
<td><span data-ttu-id="fe44d-425">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="fe44d-426">3,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-427">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-428">Proj 2</span></span></td>
<td><span data-ttu-id="fe44d-429">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="fe44d-430">1,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="fe44d-431">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="fe44d-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-432">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fe44d-433">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fe44d-433">Cost element</span></span></th>
<th><span data-ttu-id="fe44d-434">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fe44d-434">Cost behavior</span></span></th>
<th><span data-ttu-id="fe44d-435">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-435">Amount</span></span></th>
<th><span data-ttu-id="fe44d-436">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fe44d-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="fe44d-437">CC0001</span></span></td>
<td><span data-ttu-id="fe44d-438">HR</span><span class="sxs-lookup"><span data-stu-id="fe44d-438">HR</span></span></td>
<td><span data-ttu-id="fe44d-439">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-439">10001</span></span></td>
<td><span data-ttu-id="fe44d-440">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-440">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-441">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-441">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-442">-30.00</span></span></td>
<td><span data-ttu-id="fe44d-443">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-444">Proj 1</span></span></td>
<td><span data-ttu-id="fe44d-445">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="fe44d-446">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-446">10001</span></span></td>
<td><span data-ttu-id="fe44d-447">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-447">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-448">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-448">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-449">30,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-449">30.00</span></span></td>
<td><span data-ttu-id="fe44d-450">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-451">CC001</span><span class="sxs-lookup"><span data-stu-id="fe44d-451">CC001</span></span></td>
<td><span data-ttu-id="fe44d-452">HR</span><span class="sxs-lookup"><span data-stu-id="fe44d-452">HR</span></span></td>
<td><span data-ttu-id="fe44d-453">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-453">10001</span></span></td>
<td><span data-ttu-id="fe44d-454">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-454">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-455">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-455">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-456">-10.00</span></span></td>
<td><span data-ttu-id="fe44d-457">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-458">Proj 2</span></span></td>
<td><span data-ttu-id="fe44d-459">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="fe44d-460">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-460">10001</span></span></td>
<td><span data-ttu-id="fe44d-461">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-461">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-462">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-462">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-463">10,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-463">10.00</span></span></td>
<td><span data-ttu-id="fe44d-464">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fe44d-465">Sīkāku informāciju skatiet šeit: [Pieskaitāmo izmaksu aprēķina veikšana](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="fe44d-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="fe44d-466">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="fe44d-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="fe44d-467">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="fe44d-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="fe44d-468">Finance and Operations atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="fe44d-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="fe44d-469">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="fe44d-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="fe44d-470">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="fe44d-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="fe44d-471">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="fe44d-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="fe44d-472">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="fe44d-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="fe44d-473">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="fe44d-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="fe44d-474">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="fe44d-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="fe44d-475">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="fe44d-475">Define the cost allocation</span></span>

<span data-ttu-id="fe44d-476">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="fe44d-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="fe44d-477">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="fe44d-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="fe44d-478">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="fe44d-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-479">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-479">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-480">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="fe44d-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-481">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-481">CC002</span></span></td>
<td><span data-ttu-id="fe44d-482">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-482">Finance</span></span></td>
<td><span data-ttu-id="fe44d-483">35</span><span class="sxs-lookup"><span data-stu-id="fe44d-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-484">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-484">CC003</span></span></td>
<td><span data-ttu-id="fe44d-485">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-485">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-486">55</span><span class="sxs-lookup"><span data-stu-id="fe44d-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-487">CC004</span><span class="sxs-lookup"><span data-stu-id="fe44d-487">CC004</span></span></td>
<td><span data-ttu-id="fe44d-488">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fe44d-488">Packaging</span></span></td>
<td><span data-ttu-id="fe44d-489">10.</span><span class="sxs-lookup"><span data-stu-id="fe44d-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fe44d-490">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="fe44d-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="fe44d-491">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="fe44d-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-492">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-492">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-493">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="fe44d-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-494">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-494">CC003</span></span></td>
<td><span data-ttu-id="fe44d-495">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-495">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-496">65</span><span class="sxs-lookup"><span data-stu-id="fe44d-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-497">CC004</span><span class="sxs-lookup"><span data-stu-id="fe44d-497">CC004</span></span></td>
<td><span data-ttu-id="fe44d-498">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fe44d-498">Packaging</span></span></td>
<td><span data-ttu-id="fe44d-499">35</span><span class="sxs-lookup"><span data-stu-id="fe44d-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fe44d-500">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="fe44d-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="fe44d-501">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="fe44d-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-502">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-502">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-503">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="fe44d-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-504">Prod 1</span></span></td>
<td><span data-ttu-id="fe44d-505">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-505">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-506">60</span><span class="sxs-lookup"><span data-stu-id="fe44d-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-507">Prod 2</span></span></td>
<td><span data-ttu-id="fe44d-508">2. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-508">Product 2</span></span></td>
<td><span data-ttu-id="fe44d-509">20</span><span class="sxs-lookup"><span data-stu-id="fe44d-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fe44d-510">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="fe44d-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="fe44d-511">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="fe44d-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-512">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-512">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-513">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="fe44d-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-514">Prod 1</span></span></td>
<td><span data-ttu-id="fe44d-515">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-515">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-516">80</span><span class="sxs-lookup"><span data-stu-id="fe44d-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-517">Prod 2</span></span></td>
<td><span data-ttu-id="fe44d-518">2. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-518">Product 2</span></span></td>
<td><span data-ttu-id="fe44d-519">15.</span><span class="sxs-lookup"><span data-stu-id="fe44d-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="fe44d-520">Sistēmā Finance and Operations statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="fe44d-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="fe44d-521">Sīkāku informāciju skatiet šeit: [Statistikas mēru nodrošinātāja veidne](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="fe44d-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="fe44d-522">Nākamajā tabulā ir parādīts rezultāts, ja tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījuma pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="fe44d-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-523">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-523">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-524">Lielums</span><span class="sxs-lookup"><span data-stu-id="fe44d-524">Magnitude</span></span></th>
<th><span data-ttu-id="fe44d-525">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fe44d-525">Allocation factor</span></span></th>
<th><span data-ttu-id="fe44d-526">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-526">Amount</span></span></th>
<th><span data-ttu-id="fe44d-527">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fe44d-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-528">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-528">CC002</span></span></td>
<td><span data-ttu-id="fe44d-529">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-529">Finance</span></span></td>
<td><span data-ttu-id="fe44d-530">35</span><span class="sxs-lookup"><span data-stu-id="fe44d-530">35</span></span></td>
<td><span data-ttu-id="fe44d-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="fe44d-532">175.00</span><span class="sxs-lookup"><span data-stu-id="fe44d-532">175.00</span></span></td>
<td><span data-ttu-id="fe44d-533">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-534">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-534">CC003</span></span></td>
<td><span data-ttu-id="fe44d-535">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-535">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-536">55</span><span class="sxs-lookup"><span data-stu-id="fe44d-536">55</span></span></td>
<td><span data-ttu-id="fe44d-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="fe44d-538">275.00</span><span class="sxs-lookup"><span data-stu-id="fe44d-538">275.00</span></span></td>
<td><span data-ttu-id="fe44d-539">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-540">CC004</span><span class="sxs-lookup"><span data-stu-id="fe44d-540">CC004</span></span></td>
<td><span data-ttu-id="fe44d-541">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fe44d-541">Packaging</span></span></td>
<td><span data-ttu-id="fe44d-542">10.</span><span class="sxs-lookup"><span data-stu-id="fe44d-542">10</span></span></td>
<td><span data-ttu-id="fe44d-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="fe44d-544">50,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-544">50.00</span></span></td>
<td><span data-ttu-id="fe44d-545">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-546">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-546">CC002</span></span></td>
<td><span data-ttu-id="fe44d-547">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-547">Finance</span></span></td>
<td><span data-ttu-id="fe44d-548">35</span><span class="sxs-lookup"><span data-stu-id="fe44d-548">35</span></span></td>
<td><span data-ttu-id="fe44d-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="fe44d-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="fe44d-550">436.00</span><span class="sxs-lookup"><span data-stu-id="fe44d-550">436.00</span></span></td>
<td><span data-ttu-id="fe44d-551">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-552">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-552">CC003</span></span></td>
<td><span data-ttu-id="fe44d-553">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-553">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-554">55</span><span class="sxs-lookup"><span data-stu-id="fe44d-554">55</span></span></td>
<td><span data-ttu-id="fe44d-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="fe44d-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="fe44d-556">685.14</span><span class="sxs-lookup"><span data-stu-id="fe44d-556">685.14</span></span></td>
<td><span data-ttu-id="fe44d-557">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-558">CC004</span><span class="sxs-lookup"><span data-stu-id="fe44d-558">CC004</span></span></td>
<td><span data-ttu-id="fe44d-559">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fe44d-559">Packaging</span></span></td>
<td><span data-ttu-id="fe44d-560">10.</span><span class="sxs-lookup"><span data-stu-id="fe44d-560">10</span></span></td>
<td><span data-ttu-id="fe44d-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="fe44d-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="fe44d-562">124.57</span><span class="sxs-lookup"><span data-stu-id="fe44d-562">124.57</span></span></td>
<td><span data-ttu-id="fe44d-563">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fe44d-564">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="fe44d-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-565">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-565">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-566">Lielums</span><span class="sxs-lookup"><span data-stu-id="fe44d-566">Magnitude</span></span></th>
<th><span data-ttu-id="fe44d-567">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fe44d-567">Allocation factor</span></span></th>
<th><span data-ttu-id="fe44d-568">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-568">Amount</span></span></th>
<th><span data-ttu-id="fe44d-569">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fe44d-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-570">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-570">CC003</span></span></td>
<td><span data-ttu-id="fe44d-571">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-571">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-572">65</span><span class="sxs-lookup"><span data-stu-id="fe44d-572">65</span></span></td>
<td><span data-ttu-id="fe44d-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="fe44d-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="fe44d-574">438.75</span><span class="sxs-lookup"><span data-stu-id="fe44d-574">438.75</span></span></td>
<td><span data-ttu-id="fe44d-575">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-576">CC004</span><span class="sxs-lookup"><span data-stu-id="fe44d-576">CC004</span></span></td>
<td><span data-ttu-id="fe44d-577">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fe44d-577">Packaging</span></span></td>
<td><span data-ttu-id="fe44d-578">35</span><span class="sxs-lookup"><span data-stu-id="fe44d-578">35</span></span></td>
<td><span data-ttu-id="fe44d-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="fe44d-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="fe44d-580">236.25</span><span class="sxs-lookup"><span data-stu-id="fe44d-580">236.25</span></span></td>
<td><span data-ttu-id="fe44d-581">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-582">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-582">CC003</span></span></td>
<td><span data-ttu-id="fe44d-583">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-583">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-584">65</span><span class="sxs-lookup"><span data-stu-id="fe44d-584">65</span></span></td>
<td><span data-ttu-id="fe44d-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="fe44d-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="fe44d-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="fe44d-586">5,297.69</span></span></td>
<td><span data-ttu-id="fe44d-587">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-588">CC004</span><span class="sxs-lookup"><span data-stu-id="fe44d-588">CC004</span></span></td>
<td><span data-ttu-id="fe44d-589">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fe44d-589">Packaging</span></span></td>
<td><span data-ttu-id="fe44d-590">35</span><span class="sxs-lookup"><span data-stu-id="fe44d-590">35</span></span></td>
<td><span data-ttu-id="fe44d-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="fe44d-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="fe44d-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="fe44d-592">2,852.60</span></span></td>
<td><span data-ttu-id="fe44d-593">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fe44d-594">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="fe44d-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-595">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-595">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-596">Lielums</span><span class="sxs-lookup"><span data-stu-id="fe44d-596">Magnitude</span></span></th>
<th><span data-ttu-id="fe44d-597">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fe44d-597">Allocation factor</span></span></th>
<th><span data-ttu-id="fe44d-598">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-598">Amount</span></span></th>
<th><span data-ttu-id="fe44d-599">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fe44d-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-600">Prod 1</span></span></td>
<td><span data-ttu-id="fe44d-601">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-601">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-602">60</span><span class="sxs-lookup"><span data-stu-id="fe44d-602">60</span></span></td>
<td><span data-ttu-id="fe44d-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="fe44d-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="fe44d-604">535.31</span><span class="sxs-lookup"><span data-stu-id="fe44d-604">535.31</span></span></td>
<td><span data-ttu-id="fe44d-605">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-606">Prod 2</span></span></td>
<td><span data-ttu-id="fe44d-607">2. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-607">Product 2</span></span></td>
<td><span data-ttu-id="fe44d-608">20.</span><span class="sxs-lookup"><span data-stu-id="fe44d-608">20</span></span></td>
<td><span data-ttu-id="fe44d-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="fe44d-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="fe44d-610">178.44</span><span class="sxs-lookup"><span data-stu-id="fe44d-610">178.44</span></span></td>
<td><span data-ttu-id="fe44d-611">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-612">Prod 1</span></span></td>
<td><span data-ttu-id="fe44d-613">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-613">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-614">60</span><span class="sxs-lookup"><span data-stu-id="fe44d-614">60</span></span></td>
<td><span data-ttu-id="fe44d-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="fe44d-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="fe44d-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="fe44d-616">4,487.12</span></span></td>
<td><span data-ttu-id="fe44d-617">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-618">Prod 2</span></span></td>
<td><span data-ttu-id="fe44d-619">2. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-619">Product 2</span></span></td>
<td><span data-ttu-id="fe44d-620">20.</span><span class="sxs-lookup"><span data-stu-id="fe44d-620">20</span></span></td>
<td><span data-ttu-id="fe44d-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="fe44d-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="fe44d-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="fe44d-622">1,495.71</span></span></td>
<td><span data-ttu-id="fe44d-623">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fe44d-624">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="fe44d-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-625">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-625">Cost object</span></span></th>
<th><span data-ttu-id="fe44d-626">Lielums</span><span class="sxs-lookup"><span data-stu-id="fe44d-626">Magnitude</span></span></th>
<th><span data-ttu-id="fe44d-627">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="fe44d-627">Allocation factor</span></span></th>
<th><span data-ttu-id="fe44d-628">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-628">Amount</span></span></th>
<th><span data-ttu-id="fe44d-629">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fe44d-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-630">Prod 1</span></span></td>
<td><span data-ttu-id="fe44d-631">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-631">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-632">80</span><span class="sxs-lookup"><span data-stu-id="fe44d-632">80</span></span></td>
<td><span data-ttu-id="fe44d-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="fe44d-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="fe44d-634">241.05</span><span class="sxs-lookup"><span data-stu-id="fe44d-634">241.05</span></span></td>
<td><span data-ttu-id="fe44d-635">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-636">Prod 2</span></span></td>
<td><span data-ttu-id="fe44d-637">2. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-637">Product 2</span></span></td>
<td><span data-ttu-id="fe44d-638">15</span><span class="sxs-lookup"><span data-stu-id="fe44d-638">15</span></span></td>
<td><span data-ttu-id="fe44d-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="fe44d-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="fe44d-640">45.20</span><span class="sxs-lookup"><span data-stu-id="fe44d-640">45.20</span></span></td>
<td><span data-ttu-id="fe44d-641">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-642">Prod 1</span></span></td>
<td><span data-ttu-id="fe44d-643">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-643">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-644">80</span><span class="sxs-lookup"><span data-stu-id="fe44d-644">80</span></span></td>
<td><span data-ttu-id="fe44d-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="fe44d-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="fe44d-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="fe44d-646">2,507.09</span></span></td>
<td><span data-ttu-id="fe44d-647">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-648">Prod 2</span></span></td>
<td><span data-ttu-id="fe44d-649">2. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-649">Product 2</span></span></td>
<td><span data-ttu-id="fe44d-650">15</span><span class="sxs-lookup"><span data-stu-id="fe44d-650">15</span></span></td>
<td><span data-ttu-id="fe44d-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="fe44d-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="fe44d-652">470.08</span><span class="sxs-lookup"><span data-stu-id="fe44d-652">470.08</span></span></td>
<td><span data-ttu-id="fe44d-653">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="fe44d-654">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="fe44d-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fe44d-655">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="fe44d-655">Journal</span></span></th>
<th><span data-ttu-id="fe44d-656">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="fe44d-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="fe44d-657">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="fe44d-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="fe44d-658">Versija</span><span class="sxs-lookup"><span data-stu-id="fe44d-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-659">00004</span><span class="sxs-lookup"><span data-stu-id="fe44d-659">00004</span></span></td>
<td><span data-ttu-id="fe44d-660">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="fe44d-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="fe44d-661">Finanšu</span><span class="sxs-lookup"><span data-stu-id="fe44d-661">Fiscal</span></span></td>
<td><span data-ttu-id="fe44d-662">2017</span><span class="sxs-lookup"><span data-stu-id="fe44d-662">2017</span></span></td>
<td><span data-ttu-id="fe44d-663">Periods 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-663">Period 1</span></span></td>
<td><span data-ttu-id="fe44d-664">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="fe44d-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="fe44d-665">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="fe44d-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fe44d-666">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fe44d-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="fe44d-667">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fe44d-668">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fe44d-668">Cost element</span></span></th>
<th><span data-ttu-id="fe44d-669">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fe44d-669">Cost behavior</span></span></th>
<th><span data-ttu-id="fe44d-670">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-671">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-672">CC001</span><span class="sxs-lookup"><span data-stu-id="fe44d-672">CC001</span></span></td>
<td><span data-ttu-id="fe44d-673">HR</span><span class="sxs-lookup"><span data-stu-id="fe44d-673">HR</span></span></td>
<td><span data-ttu-id="fe44d-674">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-674">10001</span></span></td>
<td><span data-ttu-id="fe44d-675">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-675">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-676">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-676">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-677">500,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-678">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-679">CC001</span><span class="sxs-lookup"><span data-stu-id="fe44d-679">CC001</span></span></td>
<td><span data-ttu-id="fe44d-680">HR</span><span class="sxs-lookup"><span data-stu-id="fe44d-680">HR</span></span></td>
<td><span data-ttu-id="fe44d-681">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-681">10001</span></span></td>
<td><span data-ttu-id="fe44d-682">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-682">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-683">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-683">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="fe44d-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-685">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-686">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-686">CC002</span></span></td>
<td><span data-ttu-id="fe44d-687">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-687">Finance</span></span></td>
<td><span data-ttu-id="fe44d-688">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-688">10001</span></span></td>
<td><span data-ttu-id="fe44d-689">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-689">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-690">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-690">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-691">675.00</span><span class="sxs-lookup"><span data-stu-id="fe44d-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-692">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-693">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-693">CC002</span></span></td>
<td><span data-ttu-id="fe44d-694">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-694">Finance</span></span></td>
<td><span data-ttu-id="fe44d-695">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-695">10001</span></span></td>
<td><span data-ttu-id="fe44d-696">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-696">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-697">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-697">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="fe44d-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-699">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-700">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-700">CC003</span></span></td>
<td><span data-ttu-id="fe44d-701">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-701">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-702">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-702">10001</span></span></td>
<td><span data-ttu-id="fe44d-703">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-703">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-704">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-704">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-705">713.75</span><span class="sxs-lookup"><span data-stu-id="fe44d-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-706">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-707">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-707">CC003</span></span></td>
<td><span data-ttu-id="fe44d-708">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-708">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-709">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-709">10001</span></span></td>
<td><span data-ttu-id="fe44d-710">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-710">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-711">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-711">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="fe44d-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-713">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-714">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-714">CC003</span></span></td>
<td><span data-ttu-id="fe44d-715">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fe44d-715">Packaging</span></span></td>
<td><span data-ttu-id="fe44d-716">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-716">10001</span></span></td>
<td><span data-ttu-id="fe44d-717">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-717">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-718">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-718">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-719">286.25</span><span class="sxs-lookup"><span data-stu-id="fe44d-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-720">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-721">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-721">CC003</span></span></td>
<td><span data-ttu-id="fe44d-722">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fe44d-722">Packaging</span></span></td>
<td><span data-ttu-id="fe44d-723">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-723">10001</span></span></td>
<td><span data-ttu-id="fe44d-724">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-724">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-725">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-725">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="fe44d-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-727">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-728">Prod 1</span></span></td>
<td><span data-ttu-id="fe44d-729">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-729">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-730">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-730">10001</span></span></td>
<td><span data-ttu-id="fe44d-731">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-731">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-732">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-732">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-733">776.36</span><span class="sxs-lookup"><span data-stu-id="fe44d-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-734">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-735">Prod 1</span></span></td>
<td><span data-ttu-id="fe44d-736">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-736">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-737">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-737">10001</span></span></td>
<td><span data-ttu-id="fe44d-738">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-738">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-739">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-739">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="fe44d-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-741">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-742">Prod 2</span></span></td>
<td><span data-ttu-id="fe44d-743">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-743">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-744">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-744">10001</span></span></td>
<td><span data-ttu-id="fe44d-745">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-745">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-746">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-746">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-747">223.64</span><span class="sxs-lookup"><span data-stu-id="fe44d-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-748">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="fe44d-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-749">Prod 2</span></span></td>
<td><span data-ttu-id="fe44d-750">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-750">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-751">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-751">10001</span></span></td>
<td><span data-ttu-id="fe44d-752">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-752">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-753">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-753">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="fe44d-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="fe44d-755">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="fe44d-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="fe44d-756">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="fe44d-757">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fe44d-757">Cost element</span></span></th>
<th><span data-ttu-id="fe44d-758">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="fe44d-758">Cost behavior</span></span></th>
<th><span data-ttu-id="fe44d-759">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-759">Amount</span></span></th>
<th><span data-ttu-id="fe44d-760">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="fe44d-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fe44d-761">CC001</span><span class="sxs-lookup"><span data-stu-id="fe44d-761">CC001</span></span></td>
<td><span data-ttu-id="fe44d-762">HR</span><span class="sxs-lookup"><span data-stu-id="fe44d-762">HR</span></span></td>
<td><span data-ttu-id="fe44d-763">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-763">10001</span></span></td>
<td><span data-ttu-id="fe44d-764">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-764">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-765">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-765">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-766">-500.00</span></span></td>
<td><span data-ttu-id="fe44d-767">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-768">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-768">CC002</span></span></td>
<td><span data-ttu-id="fe44d-769">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-769">Finance</span></span></td>
<td><span data-ttu-id="fe44d-770">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-770">10001</span></span></td>
<td><span data-ttu-id="fe44d-771">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-771">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-772">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-772">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-773">175.00</span><span class="sxs-lookup"><span data-stu-id="fe44d-773">175.00</span></span></td>
<td><span data-ttu-id="fe44d-774">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-775">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-775">CC003</span></span></td>
<td><span data-ttu-id="fe44d-776">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-776">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-777">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-777">10001</span></span></td>
<td><span data-ttu-id="fe44d-778">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-778">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-779">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-779">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-780">275.00</span><span class="sxs-lookup"><span data-stu-id="fe44d-780">275.00</span></span></td>
<td><span data-ttu-id="fe44d-781">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-782">CC004</span><span class="sxs-lookup"><span data-stu-id="fe44d-782">CC004</span></span></td>
<td><span data-ttu-id="fe44d-783">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fe44d-783">Packaging</span></span></td>
<td><span data-ttu-id="fe44d-784">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-784">10001</span></span></td>
<td><span data-ttu-id="fe44d-785">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-785">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-786">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-786">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-787">50,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-787">50,00</span></span></td>
<td><span data-ttu-id="fe44d-788">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-789">CC001</span><span class="sxs-lookup"><span data-stu-id="fe44d-789">CC001</span></span></td>
<td><span data-ttu-id="fe44d-790">HR</span><span class="sxs-lookup"><span data-stu-id="fe44d-790">HR</span></span></td>
<td><span data-ttu-id="fe44d-791">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-791">10001</span></span></td>
<td><span data-ttu-id="fe44d-792">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-792">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-793">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-793">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="fe44d-794">-1,245.71</span></span></td>
<td><span data-ttu-id="fe44d-795">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-796">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-796">CC002</span></span></td>
<td><span data-ttu-id="fe44d-797">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-797">Finance</span></span></td>
<td><span data-ttu-id="fe44d-798">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-798">10001</span></span></td>
<td><span data-ttu-id="fe44d-799">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-799">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-800">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-800">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-801">436.00</span><span class="sxs-lookup"><span data-stu-id="fe44d-801">436.00</span></span></td>
<td><span data-ttu-id="fe44d-802">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-803">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-803">CC003</span></span></td>
<td><span data-ttu-id="fe44d-804">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-804">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-805">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-805">10001</span></span></td>
<td><span data-ttu-id="fe44d-806">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-806">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-807">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-807">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-808">685.14</span><span class="sxs-lookup"><span data-stu-id="fe44d-808">685.14</span></span></td>
<td><span data-ttu-id="fe44d-809">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-810">CC004</span><span class="sxs-lookup"><span data-stu-id="fe44d-810">CC004</span></span></td>
<td><span data-ttu-id="fe44d-811">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fe44d-811">Packaging</span></span></td>
<td><span data-ttu-id="fe44d-812">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-812">10001</span></span></td>
<td><span data-ttu-id="fe44d-813">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-813">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-814">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-814">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-815">124.57</span><span class="sxs-lookup"><span data-stu-id="fe44d-815">124.57</span></span></td>
<td><span data-ttu-id="fe44d-816">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-817">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-817">CC002</span></span></td>
<td><span data-ttu-id="fe44d-818">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-818">Finance</span></span></td>
<td><span data-ttu-id="fe44d-819">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-819">10001</span></span></td>
<td><span data-ttu-id="fe44d-820">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-820">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-821">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-821">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-822">-675.00</span></span></td>
<td><span data-ttu-id="fe44d-823">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-824">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-824">CC003</span></span></td>
<td><span data-ttu-id="fe44d-825">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-825">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-826">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-826">10001</span></span></td>
<td><span data-ttu-id="fe44d-827">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-827">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-828">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-828">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-829">438.75</span><span class="sxs-lookup"><span data-stu-id="fe44d-829">438.75</span></span></td>
<td><span data-ttu-id="fe44d-830">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-831">CC004</span><span class="sxs-lookup"><span data-stu-id="fe44d-831">CC004</span></span></td>
<td><span data-ttu-id="fe44d-832">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fe44d-832">Packaging</span></span></td>
<td><span data-ttu-id="fe44d-833">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-833">10001</span></span></td>
<td><span data-ttu-id="fe44d-834">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-834">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-835">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-835">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-836">236.25</span><span class="sxs-lookup"><span data-stu-id="fe44d-836">236.25</span></span></td>
<td><span data-ttu-id="fe44d-837">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-838">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-838">CC002</span></span></td>
<td><span data-ttu-id="fe44d-839">Finanses</span><span class="sxs-lookup"><span data-stu-id="fe44d-839">Finance</span></span></td>
<td><span data-ttu-id="fe44d-840">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-840">10001</span></span></td>
<td><span data-ttu-id="fe44d-841">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-841">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-842">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-842">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="fe44d-843">-8,150.29</span></span></td>
<td><span data-ttu-id="fe44d-844">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-845">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-845">CC003</span></span></td>
<td><span data-ttu-id="fe44d-846">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-846">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-847">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-847">10001</span></span></td>
<td><span data-ttu-id="fe44d-848">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-848">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-849">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-849">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="fe44d-850">5,297.69</span></span></td>
<td><span data-ttu-id="fe44d-851">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-852">CC004</span><span class="sxs-lookup"><span data-stu-id="fe44d-852">CC004</span></span></td>
<td><span data-ttu-id="fe44d-853">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="fe44d-853">Packaging</span></span></td>
<td><span data-ttu-id="fe44d-854">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-854">10001</span></span></td>
<td><span data-ttu-id="fe44d-855">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-855">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-856">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-856">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="fe44d-857">2,852.60</span></span></td>
<td><span data-ttu-id="fe44d-858">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-859">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-859">CC003</span></span></td>
<td><span data-ttu-id="fe44d-860">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-860">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-861">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-861">10001</span></span></td>
<td><span data-ttu-id="fe44d-862">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-862">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-863">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-863">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="fe44d-864">-713.75</span></span></td>
<td><span data-ttu-id="fe44d-865">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-866">Prod 1</span></span></td>
<td><span data-ttu-id="fe44d-867">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-867">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-868">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-868">10001</span></span></td>
<td><span data-ttu-id="fe44d-869">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-869">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-870">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-870">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-871">535.31</span><span class="sxs-lookup"><span data-stu-id="fe44d-871">535.31</span></span></td>
<td><span data-ttu-id="fe44d-872">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-873">Prod 2</span></span></td>
<td><span data-ttu-id="fe44d-874">2. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-874">Product 2</span></span></td>
<td><span data-ttu-id="fe44d-875">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-875">10001</span></span></td>
<td><span data-ttu-id="fe44d-876">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-876">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-877">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-877">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-878">178.44</span><span class="sxs-lookup"><span data-stu-id="fe44d-878">178.44</span></span></td>
<td><span data-ttu-id="fe44d-879">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-880">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-880">CC003</span></span></td>
<td><span data-ttu-id="fe44d-881">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-881">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-882">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-882">10001</span></span></td>
<td><span data-ttu-id="fe44d-883">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-883">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-884">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-884">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="fe44d-885">-5,982.83</span></span></td>
<td><span data-ttu-id="fe44d-886">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-887">Prod 1</span></span></td>
<td><span data-ttu-id="fe44d-888">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-888">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-889">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-889">10001</span></span></td>
<td><span data-ttu-id="fe44d-890">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-890">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-891">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-891">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="fe44d-892">4,487.12</span></span></td>
<td><span data-ttu-id="fe44d-893">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-894">Prod 2</span></span></td>
<td><span data-ttu-id="fe44d-895">2. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-895">Product 2</span></span></td>
<td><span data-ttu-id="fe44d-896">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-896">10001</span></span></td>
<td><span data-ttu-id="fe44d-897">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-897">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-898">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-898">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="fe44d-899">1,495.71</span></span></td>
<td><span data-ttu-id="fe44d-900">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-901">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-901">CC003</span></span></td>
<td><span data-ttu-id="fe44d-902">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-902">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-903">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-903">10001</span></span></td>
<td><span data-ttu-id="fe44d-904">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-904">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-905">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-905">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="fe44d-906">-286.25</span></span></td>
<td><span data-ttu-id="fe44d-907">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-908">Prod 1</span></span></td>
<td><span data-ttu-id="fe44d-909">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-909">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-910">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-910">10001</span></span></td>
<td><span data-ttu-id="fe44d-911">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-911">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-912">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-912">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-913">241.05</span><span class="sxs-lookup"><span data-stu-id="fe44d-913">241.05</span></span></td>
<td><span data-ttu-id="fe44d-914">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-915">Prod 2</span></span></td>
<td><span data-ttu-id="fe44d-916">2. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-916">Product 2</span></span></td>
<td><span data-ttu-id="fe44d-917">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-917">10001</span></span></td>
<td><span data-ttu-id="fe44d-918">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-918">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-919">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-919">Fixed cost</span></span></td>
<td><span data-ttu-id="fe44d-920">45.20</span><span class="sxs-lookup"><span data-stu-id="fe44d-920">45.20</span></span></td>
<td><span data-ttu-id="fe44d-921">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-922">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-922">CC003</span></span></td>
<td><span data-ttu-id="fe44d-923">Montāža</span><span class="sxs-lookup"><span data-stu-id="fe44d-923">Assembly</span></span></td>
<td><span data-ttu-id="fe44d-924">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-924">10001</span></span></td>
<td><span data-ttu-id="fe44d-925">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-925">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-926">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-926">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="fe44d-927">-2,977.17</span></span></td>
<td><span data-ttu-id="fe44d-928">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-929">Prod 1</span></span></td>
<td><span data-ttu-id="fe44d-930">1. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-930">Product 1</span></span></td>
<td><span data-ttu-id="fe44d-931">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-931">10001</span></span></td>
<td><span data-ttu-id="fe44d-932">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-932">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-933">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-933">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="fe44d-934">2,507.09</span></span></td>
<td><span data-ttu-id="fe44d-935">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fe44d-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-936">Prod 2</span></span></td>
<td><span data-ttu-id="fe44d-937">2. prece</span><span class="sxs-lookup"><span data-stu-id="fe44d-937">Product 2</span></span></td>
<td><span data-ttu-id="fe44d-938">10001</span><span class="sxs-lookup"><span data-stu-id="fe44d-938">10001</span></span></td>
<td><span data-ttu-id="fe44d-939">Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-939">Electricity</span></span></td>
<td><span data-ttu-id="fe44d-940">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-940">Variable cost</span></span></td>
<td><span data-ttu-id="fe44d-941">470.08</span><span class="sxs-lookup"><span data-stu-id="fe44d-941">470.08</span></span></td>
<td><span data-ttu-id="fe44d-942">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="fe44d-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="fe44d-943">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="fe44d-943">Conclusion</span></span>
<span data-ttu-id="fe44d-944">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="fe44d-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="fe44d-945">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="fe44d-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="fe44d-946">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="fe44d-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="fe44d-947">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="fe44d-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="fe44d-948">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="fe44d-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="fe44d-949">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="fe44d-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="fe44d-950">Summa</span><span class="sxs-lookup"><span data-stu-id="fe44d-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="fe44d-951">CC099</span><span class="sxs-lookup"><span data-stu-id="fe44d-951">CC099</span></span></th>
<th><span data-ttu-id="fe44d-952">CC001</span><span class="sxs-lookup"><span data-stu-id="fe44d-952">CC001</span></span></th>
<th><span data-ttu-id="fe44d-953">CC002</span><span class="sxs-lookup"><span data-stu-id="fe44d-953">CC002</span></span></th>
<th><span data-ttu-id="fe44d-954">CC003</span><span class="sxs-lookup"><span data-stu-id="fe44d-954">CC003</span></span></th>
<th><span data-ttu-id="fe44d-955">CC004</span><span class="sxs-lookup"><span data-stu-id="fe44d-955">CC004</span></span></th>
<th><span data-ttu-id="fe44d-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-956">Proj 1</span></span></th>
<th><span data-ttu-id="fe44d-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-957">Proj 2</span></span></th>
<th><span data-ttu-id="fe44d-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="fe44d-958">Prod 1</span></span></th>
<th><span data-ttu-id="fe44d-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="fe44d-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="fe44d-960">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="fe44d-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="fe44d-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="fe44d-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="fe44d-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="fe44d-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="fe44d-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="fe44d-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="fe44d-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="fe44d-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="fe44d-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="fe44d-970">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="fe44d-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-971">0,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="fe44d-972">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-973">0,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-974">0,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-975">0,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-976">0,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-977">0,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-978">776.36</span><span class="sxs-lookup"><span data-stu-id="fe44d-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-979">223.64</span><span class="sxs-lookup"><span data-stu-id="fe44d-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="fe44d-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="fe44d-981">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="fe44d-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-982">000</span><span class="sxs-lookup"><span data-stu-id="fe44d-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-983">0,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-984">0,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-985">0,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-986">0,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-987">30,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-988">10,00</span><span class="sxs-lookup"><span data-stu-id="fe44d-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="fe44d-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="fe44d-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="fe44d-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="fe44d-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="fe44d-992">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="fe44d-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="fe44d-993">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="fe44d-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="fe44d-994">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="fe44d-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="fe44d-995">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="fe44d-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="fe44d-996">Sīkāku informāciju skatiet šeit: [Izmaksu apkopošanas politika](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="fe44d-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



