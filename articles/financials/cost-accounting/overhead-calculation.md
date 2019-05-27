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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544059"
---
# <a name="overhead-calculation"></a><span data-ttu-id="1e2ac-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="1e2ac-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e2ac-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="1e2ac-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="1e2ac-105">Term definition</span></span>
---------------

<span data-ttu-id="1e2ac-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="1e2ac-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="1e2ac-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="1e2ac-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="1e2ac-109">Īre</span><span class="sxs-lookup"><span data-stu-id="1e2ac-109">Rent</span></span>
-   <span data-ttu-id="1e2ac-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-110">Electricity</span></span>
-   <span data-ttu-id="1e2ac-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="1e2ac-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="1e2ac-112">Overhead calculation overview</span></span>
<span data-ttu-id="1e2ac-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="1e2ac-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="1e2ac-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="1e2ac-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="1e2ac-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="1e2ac-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="1e2ac-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="1e2ac-119">Version type</span></span>
-   <span data-ttu-id="1e2ac-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="1e2ac-120">Date and time</span></span>
-   <span data-ttu-id="1e2ac-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="1e2ac-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="1e2ac-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="1e2ac-122">Fiscal year</span></span>
-   <span data-ttu-id="1e2ac-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="1e2ac-123">Fiscal period</span></span>

<span data-ttu-id="1e2ac-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="1e2ac-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="1e2ac-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="1e2ac-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="1e2ac-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="1e2ac-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="1e2ac-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="1e2ac-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="1e2ac-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="1e2ac-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="1e2ac-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="1e2ac-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="1e2ac-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="1e2ac-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e2ac-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1e2ac-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="1e2ac-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="1e2ac-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-140">Main account</span></span></th>
<th><span data-ttu-id="1e2ac-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="1e2ac-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-143">CC099</span><span class="sxs-lookup"><span data-stu-id="1e2ac-143">CC099</span></span></td>
<td><span data-ttu-id="1e2ac-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="1e2ac-144">Default cost center</span></span></td>
<td><span data-ttu-id="1e2ac-145">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-145">10001</span></span></td>
<td><span data-ttu-id="1e2ac-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-146">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="1e2ac-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="1e2ac-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="1e2ac-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="1e2ac-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="1e2ac-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="1e2ac-151">Define the cost behavior rule</span></span>

<span data-ttu-id="1e2ac-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="1e2ac-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="1e2ac-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="1e2ac-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="1e2ac-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="1e2ac-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="1e2ac-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="1e2ac-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="1e2ac-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="1e2ac-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e2ac-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="1e2ac-160">Journal</span></span></th>
<th><span data-ttu-id="1e2ac-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="1e2ac-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1e2ac-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="1e2ac-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1e2ac-163">Versija</span><span class="sxs-lookup"><span data-stu-id="1e2ac-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-164">00001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-164">00001</span></span></td>
<td><span data-ttu-id="1e2ac-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="1e2ac-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="1e2ac-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="1e2ac-166">Fiscal</span></span></td>
<td><span data-ttu-id="1e2ac-167">2017</span><span class="sxs-lookup"><span data-stu-id="1e2ac-167">2017</span></span></td>
<td><span data-ttu-id="1e2ac-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-168">Period 1</span></span></td>
<td><span data-ttu-id="1e2ac-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="1e2ac-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="1e2ac-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e2ac-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1e2ac-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e2ac-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="1e2ac-173">Cost element</span></span></th>
<th><span data-ttu-id="1e2ac-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="1e2ac-174">Cost behavior</span></span></th>
<th><span data-ttu-id="1e2ac-175">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-177">CC099</span><span class="sxs-lookup"><span data-stu-id="1e2ac-177">CC099</span></span></td>
<td><span data-ttu-id="1e2ac-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="1e2ac-178">Default cost center</span></span></td>
<td><span data-ttu-id="1e2ac-179">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-179">10001</span></span></td>
<td><span data-ttu-id="1e2ac-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-180">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-181">Unclassified</span></span></td>
<td><span data-ttu-id="1e2ac-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1e2ac-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="1e2ac-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e2ac-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="1e2ac-185">Cost element</span></span></th>
<th><span data-ttu-id="1e2ac-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="1e2ac-186">Cost behavior</span></span></th>
<th><span data-ttu-id="1e2ac-187">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-187">Amount</span></span></th>
<th><span data-ttu-id="1e2ac-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-189">CC099</span><span class="sxs-lookup"><span data-stu-id="1e2ac-189">CC099</span></span></td>
<td><span data-ttu-id="1e2ac-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="1e2ac-190">Default cost center</span></span></td>
<td><span data-ttu-id="1e2ac-191">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-191">10001</span></span></td>
<td><span data-ttu-id="1e2ac-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-192">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-193">Unclassified</span></span></td>
<td><span data-ttu-id="1e2ac-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-194">10,000.00</span></span></td>
<td><span data-ttu-id="1e2ac-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-196">CC099</span><span class="sxs-lookup"><span data-stu-id="1e2ac-196">CC099</span></span></td>
<td><span data-ttu-id="1e2ac-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="1e2ac-197">Default cost center</span></span></td>
<td><span data-ttu-id="1e2ac-198">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-198">10001</span></span></td>
<td><span data-ttu-id="1e2ac-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-199">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-200">Unclassified</span></span></td>
<td><span data-ttu-id="1e2ac-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-201">-10,000.00</span></span></td>
<td><span data-ttu-id="1e2ac-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-203">CC099</span><span class="sxs-lookup"><span data-stu-id="1e2ac-203">CC099</span></span></td>
<td><span data-ttu-id="1e2ac-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="1e2ac-204">Default cost center</span></span></td>
<td><span data-ttu-id="1e2ac-205">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-205">10001</span></span></td>
<td><span data-ttu-id="1e2ac-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-206">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-207">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-208">1,000.00</span></span></td>
<td><span data-ttu-id="1e2ac-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-210">CC099</span><span class="sxs-lookup"><span data-stu-id="1e2ac-210">CC099</span></span></td>
<td><span data-ttu-id="1e2ac-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="1e2ac-211">Default cost center</span></span></td>
<td><span data-ttu-id="1e2ac-212">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-212">10001</span></span></td>
<td><span data-ttu-id="1e2ac-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-213">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-214">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-215">9,000.00</span></span></td>
<td><span data-ttu-id="1e2ac-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e2ac-217">Sīkāku informāciju skatiet šeit: [Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="1e2ac-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="1e2ac-218">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="1e2ac-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="1e2ac-219">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="1e2ac-220">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="1e2ac-221">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="1e2ac-221">Define the cost distribution rule</span></span>

<span data-ttu-id="1e2ac-222">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="1e2ac-223">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="1e2ac-224">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="1e2ac-225">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="1e2ac-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="1e2ac-226">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="1e2ac-227">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-228">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-228">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="1e2ac-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-230">CC001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-230">CC001</span></span></td>
<td><span data-ttu-id="1e2ac-231">HR</span><span class="sxs-lookup"><span data-stu-id="1e2ac-231">HR</span></span></td>
<td><span data-ttu-id="1e2ac-232">1000</span><span class="sxs-lookup"><span data-stu-id="1e2ac-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-233">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-233">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-234">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-234">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-235">6,000</span><span class="sxs-lookup"><span data-stu-id="1e2ac-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-236">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-236">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-237">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-237">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-238">0</span><span class="sxs-lookup"><span data-stu-id="1e2ac-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e2ac-239">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-240">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-240">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-241">Lielums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-241">Magnitude</span></span></th>
<th><span data-ttu-id="1e2ac-242">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="1e2ac-242">Allocation factor</span></span></th>
<th><span data-ttu-id="1e2ac-243">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-244">CC001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-244">CC001</span></span></td>
<td><span data-ttu-id="1e2ac-245">HR</span><span class="sxs-lookup"><span data-stu-id="1e2ac-245">HR</span></span></td>
<td><span data-ttu-id="1e2ac-246">1000</span><span class="sxs-lookup"><span data-stu-id="1e2ac-246">1,000</span></span></td>
<td><span data-ttu-id="1e2ac-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="1e2ac-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="1e2ac-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-249">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-249">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-250">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-250">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-251">6,000</span><span class="sxs-lookup"><span data-stu-id="1e2ac-251">6,000</span></span></td>
<td><span data-ttu-id="1e2ac-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="1e2ac-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="1e2ac-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-254">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-254">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-255">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-255">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-256">0</span><span class="sxs-lookup"><span data-stu-id="1e2ac-256">0</span></span></td>
<td><span data-ttu-id="1e2ac-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="1e2ac-258">0,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e2ac-259">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="1e2ac-260">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-261">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-261">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-262">Formula</span><span class="sxs-lookup"><span data-stu-id="1e2ac-262">Formula</span></span></th>
<th><span data-ttu-id="1e2ac-263">Lielums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-263">Magnitude</span></span></th>
<th><span data-ttu-id="1e2ac-264">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="1e2ac-264">Allocation factor</span></span></th>
<th><span data-ttu-id="1e2ac-265">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-266">CC001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-266">CC001</span></span></td>
<td><span data-ttu-id="1e2ac-267">HR</span><span class="sxs-lookup"><span data-stu-id="1e2ac-267">HR</span></span></td>
<td><span data-ttu-id="1e2ac-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="1e2ac-269">1.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-269">1</span></span></td>
<td><span data-ttu-id="1e2ac-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="1e2ac-271">500,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-272">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-272">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-273">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-273">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="1e2ac-275">1.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-275">1</span></span></td>
<td><span data-ttu-id="1e2ac-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="1e2ac-277">500,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-278">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-278">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-279">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-279">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="1e2ac-281">0</span><span class="sxs-lookup"><span data-stu-id="1e2ac-281">0</span></span></td>
<td><span data-ttu-id="1e2ac-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="1e2ac-283">0,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="1e2ac-284">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="1e2ac-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e2ac-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="1e2ac-285">Journal</span></span></th>
<th><span data-ttu-id="1e2ac-286">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="1e2ac-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1e2ac-287">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="1e2ac-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1e2ac-288">Versija</span><span class="sxs-lookup"><span data-stu-id="1e2ac-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-289">00002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-289">00002</span></span></td>
<td><span data-ttu-id="1e2ac-290">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="1e2ac-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="1e2ac-291">Finanšu</span><span class="sxs-lookup"><span data-stu-id="1e2ac-291">Fiscal</span></span></td>
<td><span data-ttu-id="1e2ac-292">2017</span><span class="sxs-lookup"><span data-stu-id="1e2ac-292">2017</span></span></td>
<td><span data-ttu-id="1e2ac-293">Periods 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-293">Period 1</span></span></td>
<td><span data-ttu-id="1e2ac-294">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="1e2ac-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="1e2ac-295">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e2ac-296">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1e2ac-297">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e2ac-298">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="1e2ac-298">Cost element</span></span></th>
<th><span data-ttu-id="1e2ac-299">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="1e2ac-299">Cost behavior</span></span></th>
<th><span data-ttu-id="1e2ac-300">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-301">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-302">CC099</span><span class="sxs-lookup"><span data-stu-id="1e2ac-302">CC099</span></span></td>
<td><span data-ttu-id="1e2ac-303">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="1e2ac-303">Default cost center</span></span></td>
<td><span data-ttu-id="1e2ac-304">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-304">10001</span></span></td>
<td><span data-ttu-id="1e2ac-305">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-305">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-306">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-306">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-308">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-309">CC099</span><span class="sxs-lookup"><span data-stu-id="1e2ac-309">CC099</span></span></td>
<td><span data-ttu-id="1e2ac-310">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="1e2ac-310">Default cost center</span></span></td>
<td><span data-ttu-id="1e2ac-311">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-311">10001</span></span></td>
<td><span data-ttu-id="1e2ac-312">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-312">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-313">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-313">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1e2ac-315">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="1e2ac-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-316">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e2ac-317">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="1e2ac-317">Cost element</span></span></th>
<th><span data-ttu-id="1e2ac-318">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="1e2ac-318">Cost behavior</span></span></th>
<th><span data-ttu-id="1e2ac-319">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-319">Amount</span></span></th>
<th><span data-ttu-id="1e2ac-320">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-321">CC099</span><span class="sxs-lookup"><span data-stu-id="1e2ac-321">CC099</span></span></td>
<td><span data-ttu-id="1e2ac-322">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="1e2ac-322">Default cost center</span></span></td>
<td><span data-ttu-id="1e2ac-323">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-323">10001</span></span></td>
<td><span data-ttu-id="1e2ac-324">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-324">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-325">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-325">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-326">-1000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-326">-1,000.00</span></span></td>
<td><span data-ttu-id="1e2ac-327">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-328">CC001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-328">CC001</span></span></td>
<td><span data-ttu-id="1e2ac-329">HR</span><span class="sxs-lookup"><span data-stu-id="1e2ac-329">HR</span></span></td>
<td><span data-ttu-id="1e2ac-330">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-330">10001</span></span></td>
<td><span data-ttu-id="1e2ac-331">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-331">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-332">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-332">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-333">500,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-333">500.00</span></span></td>
<td><span data-ttu-id="1e2ac-334">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-335">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-335">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-336">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-336">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-337">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-337">10001</span></span></td>
<td><span data-ttu-id="1e2ac-338">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-338">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-339">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-339">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-340">500,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-340">500.00</span></span></td>
<td><span data-ttu-id="1e2ac-341">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-342">CC099</span><span class="sxs-lookup"><span data-stu-id="1e2ac-342">CC099</span></span></td>
<td><span data-ttu-id="1e2ac-343">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="1e2ac-343">Default cost center</span></span></td>
<td><span data-ttu-id="1e2ac-344">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-344">10001</span></span></td>
<td><span data-ttu-id="1e2ac-345">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-345">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-346">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-346">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-347">-9,000.00</span></span></td>
<td><span data-ttu-id="1e2ac-348">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-349">CC001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-349">CC001</span></span></td>
<td><span data-ttu-id="1e2ac-350">HR</span><span class="sxs-lookup"><span data-stu-id="1e2ac-350">HR</span></span></td>
<td><span data-ttu-id="1e2ac-351">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-351">10001</span></span></td>
<td><span data-ttu-id="1e2ac-352">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-352">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-353">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-353">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="1e2ac-354">1,285.71</span></span></td>
<td><span data-ttu-id="1e2ac-355">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-356">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-356">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-357">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-357">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-358">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-358">10001</span></span></td>
<td><span data-ttu-id="1e2ac-359">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-359">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-360">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-360">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="1e2ac-361">7,714.29</span></span></td>
<td><span data-ttu-id="1e2ac-362">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e2ac-363">Sīkāku informāciju skatiet šeit: [Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="1e2ac-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="1e2ac-364">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="1e2ac-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="1e2ac-365">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="1e2ac-366">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="1e2ac-367">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="1e2ac-367">Define the overhead rate</span></span>

<span data-ttu-id="1e2ac-368">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="1e2ac-369">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-370">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-370">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-371">Stundas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-372">Proj 1</span></span></td>
<td><span data-ttu-id="1e2ac-373">1. projekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-373">Project 1</span></span></td>
<td><span data-ttu-id="1e2ac-374">3.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-375">Proj 2</span></span></td>
<td><span data-ttu-id="1e2ac-376">2. projekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-376">Project 2</span></span></td>
<td><span data-ttu-id="1e2ac-377">1.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e2ac-378">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-379">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-379">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-380">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="1e2ac-380">Cost element</span></span></th>
<th><span data-ttu-id="1e2ac-381">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="1e2ac-381">Cost behavior</span></span></th>
<th><span data-ttu-id="1e2ac-382">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="1e2ac-382">Units</span></span></th>
<th><span data-ttu-id="1e2ac-383">Likme</span><span class="sxs-lookup"><span data-stu-id="1e2ac-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-384">CC001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-384">CC001</span></span></td>
<td><span data-ttu-id="1e2ac-385">HR</span><span class="sxs-lookup"><span data-stu-id="1e2ac-385">HR</span></span></td>
<td><span data-ttu-id="1e2ac-386">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-386">10001</span></span></td>
<td><span data-ttu-id="1e2ac-387">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-387">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-388">1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-388">1</span></span></td>
<td><span data-ttu-id="1e2ac-389">10</span><span class="sxs-lookup"><span data-stu-id="1e2ac-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e2ac-390">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-391">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-391">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-392">Lielums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-392">Magnitude</span></span></th>
<th><span data-ttu-id="1e2ac-393">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="1e2ac-393">Cost element</span></span></th>
<th><span data-ttu-id="1e2ac-394">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="1e2ac-394">Allocation factor</span></span></th>
<th><span data-ttu-id="1e2ac-395">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-396">Proj 1</span></span></td>
<td><span data-ttu-id="1e2ac-397">1. projekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-397">Project 1</span></span></td>
<td><span data-ttu-id="1e2ac-398">3.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-398">3</span></span></td>
<td><span data-ttu-id="1e2ac-399">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-399">10001</span></span></td>
<td><span data-ttu-id="1e2ac-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="1e2ac-401">30,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-402">Proj 2</span></span></td>
<td><span data-ttu-id="1e2ac-403">2. projekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-403">Project 2</span></span></td>
<td><span data-ttu-id="1e2ac-404">1.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-404">1</span></span></td>
<td><span data-ttu-id="1e2ac-405">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-405">10001</span></span></td>
<td><span data-ttu-id="1e2ac-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="1e2ac-407">10,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="1e2ac-408">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="1e2ac-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e2ac-409">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="1e2ac-409">Journal</span></span></th>
<th><span data-ttu-id="1e2ac-410">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="1e2ac-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1e2ac-411">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="1e2ac-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1e2ac-412">Versija</span><span class="sxs-lookup"><span data-stu-id="1e2ac-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-413">00003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-413">00003</span></span></td>
<td><span data-ttu-id="1e2ac-414">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="1e2ac-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="1e2ac-415">Finanšu</span><span class="sxs-lookup"><span data-stu-id="1e2ac-415">Fiscal</span></span></td>
<td><span data-ttu-id="1e2ac-416">2017</span><span class="sxs-lookup"><span data-stu-id="1e2ac-416">2017</span></span></td>
<td><span data-ttu-id="1e2ac-417">Periods 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-417">Period 1</span></span></td>
<td><span data-ttu-id="1e2ac-418">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="1e2ac-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="1e2ac-419">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e2ac-420">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1e2ac-421">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-421">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-422">Lielums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-423">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-424">Proj 1</span></span></td>
<td><span data-ttu-id="1e2ac-425">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="1e2ac-426">3,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-427">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-428">Proj 2</span></span></td>
<td><span data-ttu-id="1e2ac-429">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="1e2ac-430">1,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1e2ac-431">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="1e2ac-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-432">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e2ac-433">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="1e2ac-433">Cost element</span></span></th>
<th><span data-ttu-id="1e2ac-434">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="1e2ac-434">Cost behavior</span></span></th>
<th><span data-ttu-id="1e2ac-435">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-435">Amount</span></span></th>
<th><span data-ttu-id="1e2ac-436">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-437">CC0001</span></span></td>
<td><span data-ttu-id="1e2ac-438">HR</span><span class="sxs-lookup"><span data-stu-id="1e2ac-438">HR</span></span></td>
<td><span data-ttu-id="1e2ac-439">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-439">10001</span></span></td>
<td><span data-ttu-id="1e2ac-440">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-440">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-441">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-441">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-442">-30.00</span></span></td>
<td><span data-ttu-id="1e2ac-443">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-444">Proj 1</span></span></td>
<td><span data-ttu-id="1e2ac-445">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="1e2ac-446">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-446">10001</span></span></td>
<td><span data-ttu-id="1e2ac-447">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-447">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-448">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-448">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-449">30,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-449">30.00</span></span></td>
<td><span data-ttu-id="1e2ac-450">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-451">CC001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-451">CC001</span></span></td>
<td><span data-ttu-id="1e2ac-452">HR</span><span class="sxs-lookup"><span data-stu-id="1e2ac-452">HR</span></span></td>
<td><span data-ttu-id="1e2ac-453">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-453">10001</span></span></td>
<td><span data-ttu-id="1e2ac-454">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-454">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-455">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-455">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-456">-10.00</span></span></td>
<td><span data-ttu-id="1e2ac-457">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-458">Proj 2</span></span></td>
<td><span data-ttu-id="1e2ac-459">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="1e2ac-460">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-460">10001</span></span></td>
<td><span data-ttu-id="1e2ac-461">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-461">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-462">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-462">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-463">10,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-463">10.00</span></span></td>
<td><span data-ttu-id="1e2ac-464">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e2ac-465">Sīkāku informāciju skatiet šeit: [Pieskaitāmo izmaksu aprēķina veikšana](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="1e2ac-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="1e2ac-466">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="1e2ac-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="1e2ac-467">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="1e2ac-468">Finance and Operations atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="1e2ac-469">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="1e2ac-470">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="1e2ac-471">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="1e2ac-472">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="1e2ac-473">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="1e2ac-474">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="1e2ac-475">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="1e2ac-475">Define the cost allocation</span></span>

<span data-ttu-id="1e2ac-476">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="1e2ac-477">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="1e2ac-478">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-479">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-479">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-480">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="1e2ac-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-481">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-481">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-482">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-482">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-483">35</span><span class="sxs-lookup"><span data-stu-id="1e2ac-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-484">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-484">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-485">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-485">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-486">55</span><span class="sxs-lookup"><span data-stu-id="1e2ac-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-487">CC004</span><span class="sxs-lookup"><span data-stu-id="1e2ac-487">CC004</span></span></td>
<td><span data-ttu-id="1e2ac-488">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="1e2ac-488">Packaging</span></span></td>
<td><span data-ttu-id="1e2ac-489">10.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e2ac-490">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="1e2ac-491">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-492">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-492">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-493">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="1e2ac-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-494">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-494">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-495">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-495">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-496">65</span><span class="sxs-lookup"><span data-stu-id="1e2ac-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-497">CC004</span><span class="sxs-lookup"><span data-stu-id="1e2ac-497">CC004</span></span></td>
<td><span data-ttu-id="1e2ac-498">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="1e2ac-498">Packaging</span></span></td>
<td><span data-ttu-id="1e2ac-499">35</span><span class="sxs-lookup"><span data-stu-id="1e2ac-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e2ac-500">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="1e2ac-501">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-502">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-502">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-503">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-504">Prod 1</span></span></td>
<td><span data-ttu-id="1e2ac-505">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-505">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-506">60</span><span class="sxs-lookup"><span data-stu-id="1e2ac-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-507">Prod 2</span></span></td>
<td><span data-ttu-id="1e2ac-508">2. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-508">Product 2</span></span></td>
<td><span data-ttu-id="1e2ac-509">20</span><span class="sxs-lookup"><span data-stu-id="1e2ac-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e2ac-510">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="1e2ac-511">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-512">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-512">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-513">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-514">Prod 1</span></span></td>
<td><span data-ttu-id="1e2ac-515">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-515">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-516">80</span><span class="sxs-lookup"><span data-stu-id="1e2ac-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-517">Prod 2</span></span></td>
<td><span data-ttu-id="1e2ac-518">2. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-518">Product 2</span></span></td>
<td><span data-ttu-id="1e2ac-519">15.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="1e2ac-520">Sistēmā Finance and Operations statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="1e2ac-521">Sīkāku informāciju skatiet šeit: [Statistikas mēru nodrošinātāja veidne](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="1e2ac-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="1e2ac-522">Nākamajā tabulā ir parādīts rezultāts, ja tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījuma pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-523">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-523">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-524">Lielums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-524">Magnitude</span></span></th>
<th><span data-ttu-id="1e2ac-525">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="1e2ac-525">Allocation factor</span></span></th>
<th><span data-ttu-id="1e2ac-526">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-526">Amount</span></span></th>
<th><span data-ttu-id="1e2ac-527">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="1e2ac-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-528">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-528">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-529">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-529">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-530">35</span><span class="sxs-lookup"><span data-stu-id="1e2ac-530">35</span></span></td>
<td><span data-ttu-id="1e2ac-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="1e2ac-532">175.00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-532">175.00</span></span></td>
<td><span data-ttu-id="1e2ac-533">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-534">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-534">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-535">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-535">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-536">55</span><span class="sxs-lookup"><span data-stu-id="1e2ac-536">55</span></span></td>
<td><span data-ttu-id="1e2ac-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="1e2ac-538">275.00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-538">275.00</span></span></td>
<td><span data-ttu-id="1e2ac-539">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-540">CC004</span><span class="sxs-lookup"><span data-stu-id="1e2ac-540">CC004</span></span></td>
<td><span data-ttu-id="1e2ac-541">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="1e2ac-541">Packaging</span></span></td>
<td><span data-ttu-id="1e2ac-542">10.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-542">10</span></span></td>
<td><span data-ttu-id="1e2ac-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="1e2ac-544">50,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-544">50.00</span></span></td>
<td><span data-ttu-id="1e2ac-545">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-546">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-546">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-547">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-547">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-548">35</span><span class="sxs-lookup"><span data-stu-id="1e2ac-548">35</span></span></td>
<td><span data-ttu-id="1e2ac-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="1e2ac-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="1e2ac-550">436.00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-550">436.00</span></span></td>
<td><span data-ttu-id="1e2ac-551">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-552">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-552">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-553">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-553">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-554">55</span><span class="sxs-lookup"><span data-stu-id="1e2ac-554">55</span></span></td>
<td><span data-ttu-id="1e2ac-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="1e2ac-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="1e2ac-556">685.14</span><span class="sxs-lookup"><span data-stu-id="1e2ac-556">685.14</span></span></td>
<td><span data-ttu-id="1e2ac-557">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-558">CC004</span><span class="sxs-lookup"><span data-stu-id="1e2ac-558">CC004</span></span></td>
<td><span data-ttu-id="1e2ac-559">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="1e2ac-559">Packaging</span></span></td>
<td><span data-ttu-id="1e2ac-560">10.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-560">10</span></span></td>
<td><span data-ttu-id="1e2ac-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="1e2ac-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="1e2ac-562">124.57</span><span class="sxs-lookup"><span data-stu-id="1e2ac-562">124.57</span></span></td>
<td><span data-ttu-id="1e2ac-563">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e2ac-564">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-565">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-565">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-566">Lielums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-566">Magnitude</span></span></th>
<th><span data-ttu-id="1e2ac-567">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="1e2ac-567">Allocation factor</span></span></th>
<th><span data-ttu-id="1e2ac-568">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-568">Amount</span></span></th>
<th><span data-ttu-id="1e2ac-569">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="1e2ac-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-570">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-570">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-571">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-571">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-572">65</span><span class="sxs-lookup"><span data-stu-id="1e2ac-572">65</span></span></td>
<td><span data-ttu-id="1e2ac-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="1e2ac-574">438.75</span><span class="sxs-lookup"><span data-stu-id="1e2ac-574">438.75</span></span></td>
<td><span data-ttu-id="1e2ac-575">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-576">CC004</span><span class="sxs-lookup"><span data-stu-id="1e2ac-576">CC004</span></span></td>
<td><span data-ttu-id="1e2ac-577">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="1e2ac-577">Packaging</span></span></td>
<td><span data-ttu-id="1e2ac-578">35</span><span class="sxs-lookup"><span data-stu-id="1e2ac-578">35</span></span></td>
<td><span data-ttu-id="1e2ac-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="1e2ac-580">236.25</span><span class="sxs-lookup"><span data-stu-id="1e2ac-580">236.25</span></span></td>
<td><span data-ttu-id="1e2ac-581">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-582">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-582">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-583">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-583">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-584">65</span><span class="sxs-lookup"><span data-stu-id="1e2ac-584">65</span></span></td>
<td><span data-ttu-id="1e2ac-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="1e2ac-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="1e2ac-586">5,297.69</span></span></td>
<td><span data-ttu-id="1e2ac-587">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-588">CC004</span><span class="sxs-lookup"><span data-stu-id="1e2ac-588">CC004</span></span></td>
<td><span data-ttu-id="1e2ac-589">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="1e2ac-589">Packaging</span></span></td>
<td><span data-ttu-id="1e2ac-590">35</span><span class="sxs-lookup"><span data-stu-id="1e2ac-590">35</span></span></td>
<td><span data-ttu-id="1e2ac-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="1e2ac-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="1e2ac-592">2,852.60</span></span></td>
<td><span data-ttu-id="1e2ac-593">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e2ac-594">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-595">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-595">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-596">Lielums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-596">Magnitude</span></span></th>
<th><span data-ttu-id="1e2ac-597">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="1e2ac-597">Allocation factor</span></span></th>
<th><span data-ttu-id="1e2ac-598">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-598">Amount</span></span></th>
<th><span data-ttu-id="1e2ac-599">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="1e2ac-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-600">Prod 1</span></span></td>
<td><span data-ttu-id="1e2ac-601">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-601">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-602">60</span><span class="sxs-lookup"><span data-stu-id="1e2ac-602">60</span></span></td>
<td><span data-ttu-id="1e2ac-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="1e2ac-604">535.31</span><span class="sxs-lookup"><span data-stu-id="1e2ac-604">535.31</span></span></td>
<td><span data-ttu-id="1e2ac-605">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-606">Prod 2</span></span></td>
<td><span data-ttu-id="1e2ac-607">2. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-607">Product 2</span></span></td>
<td><span data-ttu-id="1e2ac-608">20.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-608">20</span></span></td>
<td><span data-ttu-id="1e2ac-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="1e2ac-610">178.44</span><span class="sxs-lookup"><span data-stu-id="1e2ac-610">178.44</span></span></td>
<td><span data-ttu-id="1e2ac-611">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-612">Prod 1</span></span></td>
<td><span data-ttu-id="1e2ac-613">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-613">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-614">60</span><span class="sxs-lookup"><span data-stu-id="1e2ac-614">60</span></span></td>
<td><span data-ttu-id="1e2ac-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="1e2ac-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="1e2ac-616">4,487.12</span></span></td>
<td><span data-ttu-id="1e2ac-617">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-618">Prod 2</span></span></td>
<td><span data-ttu-id="1e2ac-619">2. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-619">Product 2</span></span></td>
<td><span data-ttu-id="1e2ac-620">20.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-620">20</span></span></td>
<td><span data-ttu-id="1e2ac-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="1e2ac-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="1e2ac-622">1,495.71</span></span></td>
<td><span data-ttu-id="1e2ac-623">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e2ac-624">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-625">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-625">Cost object</span></span></th>
<th><span data-ttu-id="1e2ac-626">Lielums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-626">Magnitude</span></span></th>
<th><span data-ttu-id="1e2ac-627">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="1e2ac-627">Allocation factor</span></span></th>
<th><span data-ttu-id="1e2ac-628">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-628">Amount</span></span></th>
<th><span data-ttu-id="1e2ac-629">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="1e2ac-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-630">Prod 1</span></span></td>
<td><span data-ttu-id="1e2ac-631">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-631">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-632">80</span><span class="sxs-lookup"><span data-stu-id="1e2ac-632">80</span></span></td>
<td><span data-ttu-id="1e2ac-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="1e2ac-634">241.05</span><span class="sxs-lookup"><span data-stu-id="1e2ac-634">241.05</span></span></td>
<td><span data-ttu-id="1e2ac-635">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-636">Prod 2</span></span></td>
<td><span data-ttu-id="1e2ac-637">2. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-637">Product 2</span></span></td>
<td><span data-ttu-id="1e2ac-638">15</span><span class="sxs-lookup"><span data-stu-id="1e2ac-638">15</span></span></td>
<td><span data-ttu-id="1e2ac-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="1e2ac-640">45.20</span><span class="sxs-lookup"><span data-stu-id="1e2ac-640">45.20</span></span></td>
<td><span data-ttu-id="1e2ac-641">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-642">Prod 1</span></span></td>
<td><span data-ttu-id="1e2ac-643">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-643">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-644">80</span><span class="sxs-lookup"><span data-stu-id="1e2ac-644">80</span></span></td>
<td><span data-ttu-id="1e2ac-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="1e2ac-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="1e2ac-646">2,507.09</span></span></td>
<td><span data-ttu-id="1e2ac-647">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-648">Prod 2</span></span></td>
<td><span data-ttu-id="1e2ac-649">2. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-649">Product 2</span></span></td>
<td><span data-ttu-id="1e2ac-650">15</span><span class="sxs-lookup"><span data-stu-id="1e2ac-650">15</span></span></td>
<td><span data-ttu-id="1e2ac-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="1e2ac-652">470.08</span><span class="sxs-lookup"><span data-stu-id="1e2ac-652">470.08</span></span></td>
<td><span data-ttu-id="1e2ac-653">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="1e2ac-654">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="1e2ac-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e2ac-655">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="1e2ac-655">Journal</span></span></th>
<th><span data-ttu-id="1e2ac-656">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="1e2ac-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1e2ac-657">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="1e2ac-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1e2ac-658">Versija</span><span class="sxs-lookup"><span data-stu-id="1e2ac-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-659">00004</span><span class="sxs-lookup"><span data-stu-id="1e2ac-659">00004</span></span></td>
<td><span data-ttu-id="1e2ac-660">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="1e2ac-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="1e2ac-661">Finanšu</span><span class="sxs-lookup"><span data-stu-id="1e2ac-661">Fiscal</span></span></td>
<td><span data-ttu-id="1e2ac-662">2017</span><span class="sxs-lookup"><span data-stu-id="1e2ac-662">2017</span></span></td>
<td><span data-ttu-id="1e2ac-663">Periods 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-663">Period 1</span></span></td>
<td><span data-ttu-id="1e2ac-664">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="1e2ac-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="1e2ac-665">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e2ac-666">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1e2ac-667">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e2ac-668">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="1e2ac-668">Cost element</span></span></th>
<th><span data-ttu-id="1e2ac-669">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="1e2ac-669">Cost behavior</span></span></th>
<th><span data-ttu-id="1e2ac-670">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-671">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-672">CC001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-672">CC001</span></span></td>
<td><span data-ttu-id="1e2ac-673">HR</span><span class="sxs-lookup"><span data-stu-id="1e2ac-673">HR</span></span></td>
<td><span data-ttu-id="1e2ac-674">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-674">10001</span></span></td>
<td><span data-ttu-id="1e2ac-675">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-675">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-676">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-676">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-677">500,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-678">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-679">CC001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-679">CC001</span></span></td>
<td><span data-ttu-id="1e2ac-680">HR</span><span class="sxs-lookup"><span data-stu-id="1e2ac-680">HR</span></span></td>
<td><span data-ttu-id="1e2ac-681">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-681">10001</span></span></td>
<td><span data-ttu-id="1e2ac-682">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-682">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-683">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-683">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="1e2ac-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-685">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-686">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-686">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-687">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-687">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-688">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-688">10001</span></span></td>
<td><span data-ttu-id="1e2ac-689">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-689">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-690">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-690">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-691">675.00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-692">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-693">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-693">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-694">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-694">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-695">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-695">10001</span></span></td>
<td><span data-ttu-id="1e2ac-696">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-696">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-697">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-697">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="1e2ac-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-699">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-700">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-700">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-701">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-701">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-702">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-702">10001</span></span></td>
<td><span data-ttu-id="1e2ac-703">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-703">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-704">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-704">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-705">713.75</span><span class="sxs-lookup"><span data-stu-id="1e2ac-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-706">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-707">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-707">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-708">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-708">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-709">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-709">10001</span></span></td>
<td><span data-ttu-id="1e2ac-710">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-710">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-711">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-711">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="1e2ac-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-713">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-714">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-714">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-715">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="1e2ac-715">Packaging</span></span></td>
<td><span data-ttu-id="1e2ac-716">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-716">10001</span></span></td>
<td><span data-ttu-id="1e2ac-717">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-717">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-718">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-718">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-719">286.25</span><span class="sxs-lookup"><span data-stu-id="1e2ac-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-720">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-721">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-721">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-722">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="1e2ac-722">Packaging</span></span></td>
<td><span data-ttu-id="1e2ac-723">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-723">10001</span></span></td>
<td><span data-ttu-id="1e2ac-724">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-724">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-725">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-725">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="1e2ac-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-727">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-728">Prod 1</span></span></td>
<td><span data-ttu-id="1e2ac-729">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-729">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-730">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-730">10001</span></span></td>
<td><span data-ttu-id="1e2ac-731">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-731">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-732">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-732">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-733">776.36</span><span class="sxs-lookup"><span data-stu-id="1e2ac-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-734">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-735">Prod 1</span></span></td>
<td><span data-ttu-id="1e2ac-736">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-736">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-737">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-737">10001</span></span></td>
<td><span data-ttu-id="1e2ac-738">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-738">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-739">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-739">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="1e2ac-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-741">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-742">Prod 2</span></span></td>
<td><span data-ttu-id="1e2ac-743">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-743">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-744">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-744">10001</span></span></td>
<td><span data-ttu-id="1e2ac-745">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-745">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-746">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-746">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-747">223.64</span><span class="sxs-lookup"><span data-stu-id="1e2ac-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-748">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e2ac-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-749">Prod 2</span></span></td>
<td><span data-ttu-id="1e2ac-750">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-750">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-751">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-751">10001</span></span></td>
<td><span data-ttu-id="1e2ac-752">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-752">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-753">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-753">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="1e2ac-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1e2ac-755">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="1e2ac-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e2ac-756">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e2ac-757">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="1e2ac-757">Cost element</span></span></th>
<th><span data-ttu-id="1e2ac-758">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="1e2ac-758">Cost behavior</span></span></th>
<th><span data-ttu-id="1e2ac-759">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-759">Amount</span></span></th>
<th><span data-ttu-id="1e2ac-760">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e2ac-761">CC001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-761">CC001</span></span></td>
<td><span data-ttu-id="1e2ac-762">HR</span><span class="sxs-lookup"><span data-stu-id="1e2ac-762">HR</span></span></td>
<td><span data-ttu-id="1e2ac-763">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-763">10001</span></span></td>
<td><span data-ttu-id="1e2ac-764">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-764">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-765">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-765">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-766">-500.00</span></span></td>
<td><span data-ttu-id="1e2ac-767">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-768">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-768">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-769">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-769">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-770">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-770">10001</span></span></td>
<td><span data-ttu-id="1e2ac-771">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-771">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-772">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-772">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-773">175.00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-773">175.00</span></span></td>
<td><span data-ttu-id="1e2ac-774">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-775">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-775">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-776">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-776">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-777">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-777">10001</span></span></td>
<td><span data-ttu-id="1e2ac-778">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-778">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-779">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-779">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-780">275.00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-780">275.00</span></span></td>
<td><span data-ttu-id="1e2ac-781">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-782">CC004</span><span class="sxs-lookup"><span data-stu-id="1e2ac-782">CC004</span></span></td>
<td><span data-ttu-id="1e2ac-783">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="1e2ac-783">Packaging</span></span></td>
<td><span data-ttu-id="1e2ac-784">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-784">10001</span></span></td>
<td><span data-ttu-id="1e2ac-785">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-785">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-786">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-786">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-787">50,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-787">50,00</span></span></td>
<td><span data-ttu-id="1e2ac-788">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-789">CC001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-789">CC001</span></span></td>
<td><span data-ttu-id="1e2ac-790">HR</span><span class="sxs-lookup"><span data-stu-id="1e2ac-790">HR</span></span></td>
<td><span data-ttu-id="1e2ac-791">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-791">10001</span></span></td>
<td><span data-ttu-id="1e2ac-792">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-792">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-793">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-793">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="1e2ac-794">-1,245.71</span></span></td>
<td><span data-ttu-id="1e2ac-795">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-796">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-796">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-797">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-797">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-798">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-798">10001</span></span></td>
<td><span data-ttu-id="1e2ac-799">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-799">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-800">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-800">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-801">436.00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-801">436.00</span></span></td>
<td><span data-ttu-id="1e2ac-802">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-803">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-803">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-804">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-804">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-805">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-805">10001</span></span></td>
<td><span data-ttu-id="1e2ac-806">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-806">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-807">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-807">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-808">685.14</span><span class="sxs-lookup"><span data-stu-id="1e2ac-808">685.14</span></span></td>
<td><span data-ttu-id="1e2ac-809">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-810">CC004</span><span class="sxs-lookup"><span data-stu-id="1e2ac-810">CC004</span></span></td>
<td><span data-ttu-id="1e2ac-811">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="1e2ac-811">Packaging</span></span></td>
<td><span data-ttu-id="1e2ac-812">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-812">10001</span></span></td>
<td><span data-ttu-id="1e2ac-813">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-813">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-814">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-814">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-815">124.57</span><span class="sxs-lookup"><span data-stu-id="1e2ac-815">124.57</span></span></td>
<td><span data-ttu-id="1e2ac-816">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-817">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-817">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-818">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-818">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-819">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-819">10001</span></span></td>
<td><span data-ttu-id="1e2ac-820">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-820">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-821">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-821">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-822">-675.00</span></span></td>
<td><span data-ttu-id="1e2ac-823">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-824">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-824">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-825">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-825">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-826">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-826">10001</span></span></td>
<td><span data-ttu-id="1e2ac-827">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-827">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-828">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-828">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-829">438.75</span><span class="sxs-lookup"><span data-stu-id="1e2ac-829">438.75</span></span></td>
<td><span data-ttu-id="1e2ac-830">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-831">CC004</span><span class="sxs-lookup"><span data-stu-id="1e2ac-831">CC004</span></span></td>
<td><span data-ttu-id="1e2ac-832">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="1e2ac-832">Packaging</span></span></td>
<td><span data-ttu-id="1e2ac-833">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-833">10001</span></span></td>
<td><span data-ttu-id="1e2ac-834">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-834">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-835">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-835">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-836">236.25</span><span class="sxs-lookup"><span data-stu-id="1e2ac-836">236.25</span></span></td>
<td><span data-ttu-id="1e2ac-837">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-838">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-838">CC002</span></span></td>
<td><span data-ttu-id="1e2ac-839">Finanses</span><span class="sxs-lookup"><span data-stu-id="1e2ac-839">Finance</span></span></td>
<td><span data-ttu-id="1e2ac-840">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-840">10001</span></span></td>
<td><span data-ttu-id="1e2ac-841">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-841">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-842">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-842">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="1e2ac-843">-8,150.29</span></span></td>
<td><span data-ttu-id="1e2ac-844">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-845">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-845">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-846">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-846">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-847">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-847">10001</span></span></td>
<td><span data-ttu-id="1e2ac-848">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-848">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-849">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-849">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="1e2ac-850">5,297.69</span></span></td>
<td><span data-ttu-id="1e2ac-851">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-852">CC004</span><span class="sxs-lookup"><span data-stu-id="1e2ac-852">CC004</span></span></td>
<td><span data-ttu-id="1e2ac-853">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="1e2ac-853">Packaging</span></span></td>
<td><span data-ttu-id="1e2ac-854">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-854">10001</span></span></td>
<td><span data-ttu-id="1e2ac-855">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-855">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-856">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-856">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="1e2ac-857">2,852.60</span></span></td>
<td><span data-ttu-id="1e2ac-858">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-859">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-859">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-860">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-860">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-861">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-861">10001</span></span></td>
<td><span data-ttu-id="1e2ac-862">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-862">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-863">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-863">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="1e2ac-864">-713.75</span></span></td>
<td><span data-ttu-id="1e2ac-865">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-866">Prod 1</span></span></td>
<td><span data-ttu-id="1e2ac-867">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-867">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-868">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-868">10001</span></span></td>
<td><span data-ttu-id="1e2ac-869">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-869">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-870">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-870">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-871">535.31</span><span class="sxs-lookup"><span data-stu-id="1e2ac-871">535.31</span></span></td>
<td><span data-ttu-id="1e2ac-872">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-873">Prod 2</span></span></td>
<td><span data-ttu-id="1e2ac-874">2. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-874">Product 2</span></span></td>
<td><span data-ttu-id="1e2ac-875">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-875">10001</span></span></td>
<td><span data-ttu-id="1e2ac-876">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-876">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-877">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-877">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-878">178.44</span><span class="sxs-lookup"><span data-stu-id="1e2ac-878">178.44</span></span></td>
<td><span data-ttu-id="1e2ac-879">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-880">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-880">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-881">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-881">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-882">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-882">10001</span></span></td>
<td><span data-ttu-id="1e2ac-883">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-883">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-884">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-884">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="1e2ac-885">-5,982.83</span></span></td>
<td><span data-ttu-id="1e2ac-886">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-887">Prod 1</span></span></td>
<td><span data-ttu-id="1e2ac-888">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-888">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-889">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-889">10001</span></span></td>
<td><span data-ttu-id="1e2ac-890">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-890">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-891">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-891">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="1e2ac-892">4,487.12</span></span></td>
<td><span data-ttu-id="1e2ac-893">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-894">Prod 2</span></span></td>
<td><span data-ttu-id="1e2ac-895">2. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-895">Product 2</span></span></td>
<td><span data-ttu-id="1e2ac-896">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-896">10001</span></span></td>
<td><span data-ttu-id="1e2ac-897">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-897">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-898">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-898">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="1e2ac-899">1,495.71</span></span></td>
<td><span data-ttu-id="1e2ac-900">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-901">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-901">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-902">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-902">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-903">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-903">10001</span></span></td>
<td><span data-ttu-id="1e2ac-904">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-904">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-905">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-905">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="1e2ac-906">-286.25</span></span></td>
<td><span data-ttu-id="1e2ac-907">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-908">Prod 1</span></span></td>
<td><span data-ttu-id="1e2ac-909">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-909">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-910">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-910">10001</span></span></td>
<td><span data-ttu-id="1e2ac-911">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-911">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-912">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-912">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-913">241.05</span><span class="sxs-lookup"><span data-stu-id="1e2ac-913">241.05</span></span></td>
<td><span data-ttu-id="1e2ac-914">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-915">Prod 2</span></span></td>
<td><span data-ttu-id="1e2ac-916">2. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-916">Product 2</span></span></td>
<td><span data-ttu-id="1e2ac-917">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-917">10001</span></span></td>
<td><span data-ttu-id="1e2ac-918">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-918">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-919">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-919">Fixed cost</span></span></td>
<td><span data-ttu-id="1e2ac-920">45.20</span><span class="sxs-lookup"><span data-stu-id="1e2ac-920">45.20</span></span></td>
<td><span data-ttu-id="1e2ac-921">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-922">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-922">CC003</span></span></td>
<td><span data-ttu-id="1e2ac-923">Montāža</span><span class="sxs-lookup"><span data-stu-id="1e2ac-923">Assembly</span></span></td>
<td><span data-ttu-id="1e2ac-924">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-924">10001</span></span></td>
<td><span data-ttu-id="1e2ac-925">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-925">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-926">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-926">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="1e2ac-927">-2,977.17</span></span></td>
<td><span data-ttu-id="1e2ac-928">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-929">Prod 1</span></span></td>
<td><span data-ttu-id="1e2ac-930">1. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-930">Product 1</span></span></td>
<td><span data-ttu-id="1e2ac-931">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-931">10001</span></span></td>
<td><span data-ttu-id="1e2ac-932">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-932">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-933">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-933">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="1e2ac-934">2,507.09</span></span></td>
<td><span data-ttu-id="1e2ac-935">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e2ac-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-936">Prod 2</span></span></td>
<td><span data-ttu-id="1e2ac-937">2. prece</span><span class="sxs-lookup"><span data-stu-id="1e2ac-937">Product 2</span></span></td>
<td><span data-ttu-id="1e2ac-938">10001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-938">10001</span></span></td>
<td><span data-ttu-id="1e2ac-939">Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-939">Electricity</span></span></td>
<td><span data-ttu-id="1e2ac-940">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-940">Variable cost</span></span></td>
<td><span data-ttu-id="1e2ac-941">470.08</span><span class="sxs-lookup"><span data-stu-id="1e2ac-941">470.08</span></span></td>
<td><span data-ttu-id="1e2ac-942">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="1e2ac-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="1e2ac-943">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="1e2ac-943">Conclusion</span></span>
<span data-ttu-id="1e2ac-944">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="1e2ac-945">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="1e2ac-946">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="1e2ac-947">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="1e2ac-948">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="1e2ac-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="1e2ac-949">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="1e2ac-950">Summa</span><span class="sxs-lookup"><span data-stu-id="1e2ac-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1e2ac-951">CC099</span><span class="sxs-lookup"><span data-stu-id="1e2ac-951">CC099</span></span></th>
<th><span data-ttu-id="1e2ac-952">CC001</span><span class="sxs-lookup"><span data-stu-id="1e2ac-952">CC001</span></span></th>
<th><span data-ttu-id="1e2ac-953">CC002</span><span class="sxs-lookup"><span data-stu-id="1e2ac-953">CC002</span></span></th>
<th><span data-ttu-id="1e2ac-954">CC003</span><span class="sxs-lookup"><span data-stu-id="1e2ac-954">CC003</span></span></th>
<th><span data-ttu-id="1e2ac-955">CC004</span><span class="sxs-lookup"><span data-stu-id="1e2ac-955">CC004</span></span></th>
<th><span data-ttu-id="1e2ac-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-956">Proj 1</span></span></th>
<th><span data-ttu-id="1e2ac-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-957">Proj 2</span></span></th>
<th><span data-ttu-id="1e2ac-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1e2ac-958">Prod 1</span></span></th>
<th><span data-ttu-id="1e2ac-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1e2ac-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="1e2ac-960">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="1e2ac-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="1e2ac-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="1e2ac-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="1e2ac-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="1e2ac-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="1e2ac-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="1e2ac-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="1e2ac-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="1e2ac-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="1e2ac-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="1e2ac-970">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="1e2ac-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-971">0,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="1e2ac-972">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-973">0,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-974">0,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-975">0,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-976">0,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-977">0,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-978">776.36</span><span class="sxs-lookup"><span data-stu-id="1e2ac-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-979">223.64</span><span class="sxs-lookup"><span data-stu-id="1e2ac-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="1e2ac-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="1e2ac-981">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="1e2ac-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-982">000</span><span class="sxs-lookup"><span data-stu-id="1e2ac-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-983">0,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-984">0,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-985">0,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-986">0,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-987">30,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-988">10,00</span><span class="sxs-lookup"><span data-stu-id="1e2ac-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="1e2ac-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="1e2ac-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e2ac-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="1e2ac-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="1e2ac-992">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="1e2ac-993">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="1e2ac-994">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="1e2ac-995">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="1e2ac-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="1e2ac-996">Sīkāku informāciju skatiet šeit: [Izmaksu apkopošanas politika](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="1e2ac-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



