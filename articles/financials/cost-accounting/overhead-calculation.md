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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cef4a80aa12927fdbffea4bb6bcb108ad81494a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841493"
---
# <a name="overhead-calculation"></a><span data-ttu-id="088a5-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="088a5-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="088a5-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="088a5-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="088a5-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="088a5-105">Term definition</span></span>
---------------

<span data-ttu-id="088a5-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="088a5-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="088a5-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="088a5-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="088a5-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="088a5-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="088a5-109">Īre</span><span class="sxs-lookup"><span data-stu-id="088a5-109">Rent</span></span>
-   <span data-ttu-id="088a5-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-110">Electricity</span></span>
-   <span data-ttu-id="088a5-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="088a5-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="088a5-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="088a5-112">Overhead calculation overview</span></span>
<span data-ttu-id="088a5-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="088a5-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="088a5-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="088a5-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="088a5-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="088a5-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="088a5-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="088a5-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="088a5-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="088a5-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="088a5-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="088a5-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="088a5-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="088a5-119">Version type</span></span>
-   <span data-ttu-id="088a5-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="088a5-120">Date and time</span></span>
-   <span data-ttu-id="088a5-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="088a5-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="088a5-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="088a5-122">Fiscal year</span></span>
-   <span data-ttu-id="088a5-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="088a5-123">Fiscal period</span></span>

<span data-ttu-id="088a5-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="088a5-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="088a5-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="088a5-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="088a5-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="088a5-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="088a5-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="088a5-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="088a5-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="088a5-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="088a5-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="088a5-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="088a5-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="088a5-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="088a5-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="088a5-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="088a5-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="088a5-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="088a5-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="088a5-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="088a5-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="088a5-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="088a5-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="088a5-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="088a5-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="088a5-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="088a5-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="088a5-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="088a5-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="088a5-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="088a5-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="088a5-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="088a5-140">Main account</span></span></th>
<th><span data-ttu-id="088a5-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="088a5-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="088a5-143">CC099</span><span class="sxs-lookup"><span data-stu-id="088a5-143">CC099</span></span></td>
<td><span data-ttu-id="088a5-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="088a5-144">Default cost center</span></span></td>
<td><span data-ttu-id="088a5-145">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-145">10001</span></span></td>
<td><span data-ttu-id="088a5-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-146">Electricity</span></span></td>
<td><span data-ttu-id="088a5-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="088a5-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="088a5-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="088a5-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="088a5-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="088a5-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="088a5-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="088a5-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="088a5-151">Define the cost behavior rule</span></span>

<span data-ttu-id="088a5-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="088a5-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="088a5-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="088a5-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="088a5-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="088a5-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="088a5-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="088a5-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="088a5-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="088a5-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="088a5-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="088a5-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="088a5-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="088a5-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="088a5-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="088a5-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="088a5-160">Journal</span></span></th>
<th><span data-ttu-id="088a5-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="088a5-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="088a5-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="088a5-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="088a5-163">Versija</span><span class="sxs-lookup"><span data-stu-id="088a5-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-164">00001</span><span class="sxs-lookup"><span data-stu-id="088a5-164">00001</span></span></td>
<td><span data-ttu-id="088a5-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="088a5-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="088a5-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="088a5-166">Fiscal</span></span></td>
<td><span data-ttu-id="088a5-167">2017</span><span class="sxs-lookup"><span data-stu-id="088a5-167">2017</span></span></td>
<td><span data-ttu-id="088a5-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="088a5-168">Period 1</span></span></td>
<td><span data-ttu-id="088a5-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="088a5-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="088a5-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="088a5-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="088a5-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="088a5-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="088a5-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="088a5-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="088a5-173">Cost element</span></span></th>
<th><span data-ttu-id="088a5-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="088a5-174">Cost behavior</span></span></th>
<th><span data-ttu-id="088a5-175">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="088a5-177">CC099</span><span class="sxs-lookup"><span data-stu-id="088a5-177">CC099</span></span></td>
<td><span data-ttu-id="088a5-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="088a5-178">Default cost center</span></span></td>
<td><span data-ttu-id="088a5-179">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-179">10001</span></span></td>
<td><span data-ttu-id="088a5-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-180">Electricity</span></span></td>
<td><span data-ttu-id="088a5-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="088a5-181">Unclassified</span></span></td>
<td><span data-ttu-id="088a5-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="088a5-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="088a5-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="088a5-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="088a5-185">Cost element</span></span></th>
<th><span data-ttu-id="088a5-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="088a5-186">Cost behavior</span></span></th>
<th><span data-ttu-id="088a5-187">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-187">Amount</span></span></th>
<th><span data-ttu-id="088a5-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="088a5-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-189">CC099</span><span class="sxs-lookup"><span data-stu-id="088a5-189">CC099</span></span></td>
<td><span data-ttu-id="088a5-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="088a5-190">Default cost center</span></span></td>
<td><span data-ttu-id="088a5-191">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-191">10001</span></span></td>
<td><span data-ttu-id="088a5-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-192">Electricity</span></span></td>
<td><span data-ttu-id="088a5-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="088a5-193">Unclassified</span></span></td>
<td><span data-ttu-id="088a5-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-194">10,000.00</span></span></td>
<td><span data-ttu-id="088a5-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-196">CC099</span><span class="sxs-lookup"><span data-stu-id="088a5-196">CC099</span></span></td>
<td><span data-ttu-id="088a5-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="088a5-197">Default cost center</span></span></td>
<td><span data-ttu-id="088a5-198">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-198">10001</span></span></td>
<td><span data-ttu-id="088a5-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-199">Electricity</span></span></td>
<td><span data-ttu-id="088a5-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="088a5-200">Unclassified</span></span></td>
<td><span data-ttu-id="088a5-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-201">-10,000.00</span></span></td>
<td><span data-ttu-id="088a5-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-203">CC099</span><span class="sxs-lookup"><span data-stu-id="088a5-203">CC099</span></span></td>
<td><span data-ttu-id="088a5-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="088a5-204">Default cost center</span></span></td>
<td><span data-ttu-id="088a5-205">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-205">10001</span></span></td>
<td><span data-ttu-id="088a5-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-206">Electricity</span></span></td>
<td><span data-ttu-id="088a5-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-207">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-208">1,000.00</span></span></td>
<td><span data-ttu-id="088a5-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-210">CC099</span><span class="sxs-lookup"><span data-stu-id="088a5-210">CC099</span></span></td>
<td><span data-ttu-id="088a5-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="088a5-211">Default cost center</span></span></td>
<td><span data-ttu-id="088a5-212">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-212">10001</span></span></td>
<td><span data-ttu-id="088a5-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-213">Electricity</span></span></td>
<td><span data-ttu-id="088a5-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-214">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="088a5-215">9,000.00</span></span></td>
<td><span data-ttu-id="088a5-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="088a5-217">Sīkāku informāciju skatiet šeit: [Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="088a5-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="088a5-218">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="088a5-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="088a5-219">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="088a5-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="088a5-220">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="088a5-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="088a5-221">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="088a5-221">Define the cost distribution rule</span></span>

<span data-ttu-id="088a5-222">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="088a5-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="088a5-223">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="088a5-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="088a5-224">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="088a5-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="088a5-225">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="088a5-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="088a5-226">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="088a5-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="088a5-227">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="088a5-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-228">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-228">Cost object</span></span></th>
<th><span data-ttu-id="088a5-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="088a5-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-230">CC001</span><span class="sxs-lookup"><span data-stu-id="088a5-230">CC001</span></span></td>
<td><span data-ttu-id="088a5-231">HR</span><span class="sxs-lookup"><span data-stu-id="088a5-231">HR</span></span></td>
<td><span data-ttu-id="088a5-232">1000</span><span class="sxs-lookup"><span data-stu-id="088a5-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-233">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-233">CC002</span></span></td>
<td><span data-ttu-id="088a5-234">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-234">Finance</span></span></td>
<td><span data-ttu-id="088a5-235">6,000</span><span class="sxs-lookup"><span data-stu-id="088a5-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-236">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-236">CC003</span></span></td>
<td><span data-ttu-id="088a5-237">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-237">Assembly</span></span></td>
<td><span data-ttu-id="088a5-238">0</span><span class="sxs-lookup"><span data-stu-id="088a5-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="088a5-239">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="088a5-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-240">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-240">Cost object</span></span></th>
<th><span data-ttu-id="088a5-241">Lielums</span><span class="sxs-lookup"><span data-stu-id="088a5-241">Magnitude</span></span></th>
<th><span data-ttu-id="088a5-242">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="088a5-242">Allocation factor</span></span></th>
<th><span data-ttu-id="088a5-243">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-244">CC001</span><span class="sxs-lookup"><span data-stu-id="088a5-244">CC001</span></span></td>
<td><span data-ttu-id="088a5-245">HR</span><span class="sxs-lookup"><span data-stu-id="088a5-245">HR</span></span></td>
<td><span data-ttu-id="088a5-246">1000</span><span class="sxs-lookup"><span data-stu-id="088a5-246">1,000</span></span></td>
<td><span data-ttu-id="088a5-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="088a5-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="088a5-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-249">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-249">CC002</span></span></td>
<td><span data-ttu-id="088a5-250">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-250">Finance</span></span></td>
<td><span data-ttu-id="088a5-251">6,000</span><span class="sxs-lookup"><span data-stu-id="088a5-251">6,000</span></span></td>
<td><span data-ttu-id="088a5-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="088a5-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="088a5-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-254">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-254">CC003</span></span></td>
<td><span data-ttu-id="088a5-255">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-255">Assembly</span></span></td>
<td><span data-ttu-id="088a5-256">0</span><span class="sxs-lookup"><span data-stu-id="088a5-256">0</span></span></td>
<td><span data-ttu-id="088a5-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="088a5-258">0,00</span><span class="sxs-lookup"><span data-stu-id="088a5-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="088a5-259">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="088a5-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="088a5-260">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="088a5-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-261">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-261">Cost object</span></span></th>
<th><span data-ttu-id="088a5-262">Formula</span><span class="sxs-lookup"><span data-stu-id="088a5-262">Formula</span></span></th>
<th><span data-ttu-id="088a5-263">Lielums</span><span class="sxs-lookup"><span data-stu-id="088a5-263">Magnitude</span></span></th>
<th><span data-ttu-id="088a5-264">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="088a5-264">Allocation factor</span></span></th>
<th><span data-ttu-id="088a5-265">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-266">CC001</span><span class="sxs-lookup"><span data-stu-id="088a5-266">CC001</span></span></td>
<td><span data-ttu-id="088a5-267">HR</span><span class="sxs-lookup"><span data-stu-id="088a5-267">HR</span></span></td>
<td><span data-ttu-id="088a5-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="088a5-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="088a5-269">1.</span><span class="sxs-lookup"><span data-stu-id="088a5-269">1</span></span></td>
<td><span data-ttu-id="088a5-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="088a5-271">500,00</span><span class="sxs-lookup"><span data-stu-id="088a5-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-272">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-272">CC002</span></span></td>
<td><span data-ttu-id="088a5-273">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-273">Finance</span></span></td>
<td><span data-ttu-id="088a5-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="088a5-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="088a5-275">1.</span><span class="sxs-lookup"><span data-stu-id="088a5-275">1</span></span></td>
<td><span data-ttu-id="088a5-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="088a5-277">500,00</span><span class="sxs-lookup"><span data-stu-id="088a5-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-278">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-278">CC003</span></span></td>
<td><span data-ttu-id="088a5-279">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-279">Assembly</span></span></td>
<td><span data-ttu-id="088a5-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="088a5-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="088a5-281">0</span><span class="sxs-lookup"><span data-stu-id="088a5-281">0</span></span></td>
<td><span data-ttu-id="088a5-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="088a5-283">0,00</span><span class="sxs-lookup"><span data-stu-id="088a5-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="088a5-284">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="088a5-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="088a5-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="088a5-285">Journal</span></span></th>
<th><span data-ttu-id="088a5-286">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="088a5-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="088a5-287">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="088a5-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="088a5-288">Versija</span><span class="sxs-lookup"><span data-stu-id="088a5-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-289">00002</span><span class="sxs-lookup"><span data-stu-id="088a5-289">00002</span></span></td>
<td><span data-ttu-id="088a5-290">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="088a5-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="088a5-291">Finanšu</span><span class="sxs-lookup"><span data-stu-id="088a5-291">Fiscal</span></span></td>
<td><span data-ttu-id="088a5-292">2017</span><span class="sxs-lookup"><span data-stu-id="088a5-292">2017</span></span></td>
<td><span data-ttu-id="088a5-293">Periods 1</span><span class="sxs-lookup"><span data-stu-id="088a5-293">Period 1</span></span></td>
<td><span data-ttu-id="088a5-294">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="088a5-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="088a5-295">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="088a5-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="088a5-296">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="088a5-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="088a5-297">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="088a5-298">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="088a5-298">Cost element</span></span></th>
<th><span data-ttu-id="088a5-299">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="088a5-299">Cost behavior</span></span></th>
<th><span data-ttu-id="088a5-300">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-301">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-302">CC099</span><span class="sxs-lookup"><span data-stu-id="088a5-302">CC099</span></span></td>
<td><span data-ttu-id="088a5-303">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="088a5-303">Default cost center</span></span></td>
<td><span data-ttu-id="088a5-304">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-304">10001</span></span></td>
<td><span data-ttu-id="088a5-305">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-305">Electricity</span></span></td>
<td><span data-ttu-id="088a5-306">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-306">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-308">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-309">CC099</span><span class="sxs-lookup"><span data-stu-id="088a5-309">CC099</span></span></td>
<td><span data-ttu-id="088a5-310">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="088a5-310">Default cost center</span></span></td>
<td><span data-ttu-id="088a5-311">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-311">10001</span></span></td>
<td><span data-ttu-id="088a5-312">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-312">Electricity</span></span></td>
<td><span data-ttu-id="088a5-313">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-313">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="088a5-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="088a5-315">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="088a5-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-316">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="088a5-317">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="088a5-317">Cost element</span></span></th>
<th><span data-ttu-id="088a5-318">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="088a5-318">Cost behavior</span></span></th>
<th><span data-ttu-id="088a5-319">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-319">Amount</span></span></th>
<th><span data-ttu-id="088a5-320">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="088a5-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-321">CC099</span><span class="sxs-lookup"><span data-stu-id="088a5-321">CC099</span></span></td>
<td><span data-ttu-id="088a5-322">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="088a5-322">Default cost center</span></span></td>
<td><span data-ttu-id="088a5-323">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-323">10001</span></span></td>
<td><span data-ttu-id="088a5-324">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-324">Electricity</span></span></td>
<td><span data-ttu-id="088a5-325">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-325">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-326">-1000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-326">-1,000.00</span></span></td>
<td><span data-ttu-id="088a5-327">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-328">CC001</span><span class="sxs-lookup"><span data-stu-id="088a5-328">CC001</span></span></td>
<td><span data-ttu-id="088a5-329">HR</span><span class="sxs-lookup"><span data-stu-id="088a5-329">HR</span></span></td>
<td><span data-ttu-id="088a5-330">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-330">10001</span></span></td>
<td><span data-ttu-id="088a5-331">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-331">Electricity</span></span></td>
<td><span data-ttu-id="088a5-332">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-332">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-333">500,00</span><span class="sxs-lookup"><span data-stu-id="088a5-333">500.00</span></span></td>
<td><span data-ttu-id="088a5-334">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-335">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-335">CC002</span></span></td>
<td><span data-ttu-id="088a5-336">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-336">Finance</span></span></td>
<td><span data-ttu-id="088a5-337">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-337">10001</span></span></td>
<td><span data-ttu-id="088a5-338">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-338">Electricity</span></span></td>
<td><span data-ttu-id="088a5-339">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-339">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-340">500,00</span><span class="sxs-lookup"><span data-stu-id="088a5-340">500.00</span></span></td>
<td><span data-ttu-id="088a5-341">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-342">CC099</span><span class="sxs-lookup"><span data-stu-id="088a5-342">CC099</span></span></td>
<td><span data-ttu-id="088a5-343">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="088a5-343">Default cost center</span></span></td>
<td><span data-ttu-id="088a5-344">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-344">10001</span></span></td>
<td><span data-ttu-id="088a5-345">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-345">Electricity</span></span></td>
<td><span data-ttu-id="088a5-346">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-346">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="088a5-347">-9,000.00</span></span></td>
<td><span data-ttu-id="088a5-348">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-349">CC001</span><span class="sxs-lookup"><span data-stu-id="088a5-349">CC001</span></span></td>
<td><span data-ttu-id="088a5-350">HR</span><span class="sxs-lookup"><span data-stu-id="088a5-350">HR</span></span></td>
<td><span data-ttu-id="088a5-351">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-351">10001</span></span></td>
<td><span data-ttu-id="088a5-352">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-352">Electricity</span></span></td>
<td><span data-ttu-id="088a5-353">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-353">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="088a5-354">1,285.71</span></span></td>
<td><span data-ttu-id="088a5-355">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-356">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-356">CC002</span></span></td>
<td><span data-ttu-id="088a5-357">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-357">Finance</span></span></td>
<td><span data-ttu-id="088a5-358">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-358">10001</span></span></td>
<td><span data-ttu-id="088a5-359">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-359">Electricity</span></span></td>
<td><span data-ttu-id="088a5-360">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-360">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="088a5-361">7,714.29</span></span></td>
<td><span data-ttu-id="088a5-362">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="088a5-363">Sīkāku informāciju skatiet šeit: [Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="088a5-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="088a5-364">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="088a5-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="088a5-365">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="088a5-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="088a5-366">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="088a5-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="088a5-367">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="088a5-367">Define the overhead rate</span></span>

<span data-ttu-id="088a5-368">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="088a5-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="088a5-369">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="088a5-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-370">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-370">Cost object</span></span></th>
<th><span data-ttu-id="088a5-371">Stundas</span><span class="sxs-lookup"><span data-stu-id="088a5-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="088a5-372">Proj 1</span></span></td>
<td><span data-ttu-id="088a5-373">1. projekts</span><span class="sxs-lookup"><span data-stu-id="088a5-373">Project 1</span></span></td>
<td><span data-ttu-id="088a5-374">3.</span><span class="sxs-lookup"><span data-stu-id="088a5-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="088a5-375">Proj 2</span></span></td>
<td><span data-ttu-id="088a5-376">2. projekts</span><span class="sxs-lookup"><span data-stu-id="088a5-376">Project 2</span></span></td>
<td><span data-ttu-id="088a5-377">1.</span><span class="sxs-lookup"><span data-stu-id="088a5-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="088a5-378">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="088a5-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-379">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-379">Cost object</span></span></th>
<th><span data-ttu-id="088a5-380">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="088a5-380">Cost element</span></span></th>
<th><span data-ttu-id="088a5-381">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="088a5-381">Cost behavior</span></span></th>
<th><span data-ttu-id="088a5-382">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="088a5-382">Units</span></span></th>
<th><span data-ttu-id="088a5-383">Likme</span><span class="sxs-lookup"><span data-stu-id="088a5-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-384">CC001</span><span class="sxs-lookup"><span data-stu-id="088a5-384">CC001</span></span></td>
<td><span data-ttu-id="088a5-385">HR</span><span class="sxs-lookup"><span data-stu-id="088a5-385">HR</span></span></td>
<td><span data-ttu-id="088a5-386">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-386">10001</span></span></td>
<td><span data-ttu-id="088a5-387">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-387">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-388">1</span><span class="sxs-lookup"><span data-stu-id="088a5-388">1</span></span></td>
<td><span data-ttu-id="088a5-389">10</span><span class="sxs-lookup"><span data-stu-id="088a5-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="088a5-390">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="088a5-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-391">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-391">Cost object</span></span></th>
<th><span data-ttu-id="088a5-392">Lielums</span><span class="sxs-lookup"><span data-stu-id="088a5-392">Magnitude</span></span></th>
<th><span data-ttu-id="088a5-393">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="088a5-393">Cost element</span></span></th>
<th><span data-ttu-id="088a5-394">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="088a5-394">Allocation factor</span></span></th>
<th><span data-ttu-id="088a5-395">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="088a5-396">Proj 1</span></span></td>
<td><span data-ttu-id="088a5-397">1. projekts</span><span class="sxs-lookup"><span data-stu-id="088a5-397">Project 1</span></span></td>
<td><span data-ttu-id="088a5-398">3.</span><span class="sxs-lookup"><span data-stu-id="088a5-398">3</span></span></td>
<td><span data-ttu-id="088a5-399">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-399">10001</span></span></td>
<td><span data-ttu-id="088a5-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="088a5-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="088a5-401">30,00</span><span class="sxs-lookup"><span data-stu-id="088a5-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="088a5-402">Proj 2</span></span></td>
<td><span data-ttu-id="088a5-403">2. projekts</span><span class="sxs-lookup"><span data-stu-id="088a5-403">Project 2</span></span></td>
<td><span data-ttu-id="088a5-404">1.</span><span class="sxs-lookup"><span data-stu-id="088a5-404">1</span></span></td>
<td><span data-ttu-id="088a5-405">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-405">10001</span></span></td>
<td><span data-ttu-id="088a5-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="088a5-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="088a5-407">10,00</span><span class="sxs-lookup"><span data-stu-id="088a5-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="088a5-408">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="088a5-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="088a5-409">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="088a5-409">Journal</span></span></th>
<th><span data-ttu-id="088a5-410">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="088a5-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="088a5-411">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="088a5-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="088a5-412">Versija</span><span class="sxs-lookup"><span data-stu-id="088a5-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-413">00003</span><span class="sxs-lookup"><span data-stu-id="088a5-413">00003</span></span></td>
<td><span data-ttu-id="088a5-414">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="088a5-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="088a5-415">Finanšu</span><span class="sxs-lookup"><span data-stu-id="088a5-415">Fiscal</span></span></td>
<td><span data-ttu-id="088a5-416">2017</span><span class="sxs-lookup"><span data-stu-id="088a5-416">2017</span></span></td>
<td><span data-ttu-id="088a5-417">Periods 1</span><span class="sxs-lookup"><span data-stu-id="088a5-417">Period 1</span></span></td>
<td><span data-ttu-id="088a5-418">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="088a5-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="088a5-419">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="088a5-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="088a5-420">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="088a5-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="088a5-421">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-421">Cost object</span></span></th>
<th><span data-ttu-id="088a5-422">Lielums</span><span class="sxs-lookup"><span data-stu-id="088a5-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-423">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="088a5-424">Proj 1</span></span></td>
<td><span data-ttu-id="088a5-425">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="088a5-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="088a5-426">3,00</span><span class="sxs-lookup"><span data-stu-id="088a5-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-427">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="088a5-428">Proj 2</span></span></td>
<td><span data-ttu-id="088a5-429">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="088a5-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="088a5-430">1,00</span><span class="sxs-lookup"><span data-stu-id="088a5-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="088a5-431">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="088a5-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-432">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="088a5-433">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="088a5-433">Cost element</span></span></th>
<th><span data-ttu-id="088a5-434">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="088a5-434">Cost behavior</span></span></th>
<th><span data-ttu-id="088a5-435">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-435">Amount</span></span></th>
<th><span data-ttu-id="088a5-436">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="088a5-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="088a5-437">CC0001</span></span></td>
<td><span data-ttu-id="088a5-438">HR</span><span class="sxs-lookup"><span data-stu-id="088a5-438">HR</span></span></td>
<td><span data-ttu-id="088a5-439">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-439">10001</span></span></td>
<td><span data-ttu-id="088a5-440">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-440">Electricity</span></span></td>
<td><span data-ttu-id="088a5-441">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-441">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="088a5-442">-30.00</span></span></td>
<td><span data-ttu-id="088a5-443">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="088a5-444">Proj 1</span></span></td>
<td><span data-ttu-id="088a5-445">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="088a5-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="088a5-446">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-446">10001</span></span></td>
<td><span data-ttu-id="088a5-447">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-447">Electricity</span></span></td>
<td><span data-ttu-id="088a5-448">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-448">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-449">30,00</span><span class="sxs-lookup"><span data-stu-id="088a5-449">30.00</span></span></td>
<td><span data-ttu-id="088a5-450">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-451">CC001</span><span class="sxs-lookup"><span data-stu-id="088a5-451">CC001</span></span></td>
<td><span data-ttu-id="088a5-452">HR</span><span class="sxs-lookup"><span data-stu-id="088a5-452">HR</span></span></td>
<td><span data-ttu-id="088a5-453">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-453">10001</span></span></td>
<td><span data-ttu-id="088a5-454">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-454">Electricity</span></span></td>
<td><span data-ttu-id="088a5-455">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-455">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="088a5-456">-10.00</span></span></td>
<td><span data-ttu-id="088a5-457">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="088a5-458">Proj 2</span></span></td>
<td><span data-ttu-id="088a5-459">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="088a5-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="088a5-460">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-460">10001</span></span></td>
<td><span data-ttu-id="088a5-461">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-461">Electricity</span></span></td>
<td><span data-ttu-id="088a5-462">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-462">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-463">10,00</span><span class="sxs-lookup"><span data-stu-id="088a5-463">10.00</span></span></td>
<td><span data-ttu-id="088a5-464">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="088a5-465">Sīkāku informāciju skatiet šeit: [Pieskaitāmo izmaksu aprēķina veikšana](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="088a5-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="088a5-466">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="088a5-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="088a5-467">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="088a5-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="088a5-468">Finance and Operations atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="088a5-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="088a5-469">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="088a5-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="088a5-470">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="088a5-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="088a5-471">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="088a5-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="088a5-472">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="088a5-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="088a5-473">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="088a5-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="088a5-474">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="088a5-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="088a5-475">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="088a5-475">Define the cost allocation</span></span>

<span data-ttu-id="088a5-476">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="088a5-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="088a5-477">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="088a5-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="088a5-478">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="088a5-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-479">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-479">Cost object</span></span></th>
<th><span data-ttu-id="088a5-480">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="088a5-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-481">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-481">CC002</span></span></td>
<td><span data-ttu-id="088a5-482">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-482">Finance</span></span></td>
<td><span data-ttu-id="088a5-483">35</span><span class="sxs-lookup"><span data-stu-id="088a5-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-484">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-484">CC003</span></span></td>
<td><span data-ttu-id="088a5-485">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-485">Assembly</span></span></td>
<td><span data-ttu-id="088a5-486">55</span><span class="sxs-lookup"><span data-stu-id="088a5-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-487">CC004</span><span class="sxs-lookup"><span data-stu-id="088a5-487">CC004</span></span></td>
<td><span data-ttu-id="088a5-488">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="088a5-488">Packaging</span></span></td>
<td><span data-ttu-id="088a5-489">10.</span><span class="sxs-lookup"><span data-stu-id="088a5-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="088a5-490">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="088a5-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="088a5-491">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="088a5-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-492">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-492">Cost object</span></span></th>
<th><span data-ttu-id="088a5-493">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="088a5-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-494">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-494">CC003</span></span></td>
<td><span data-ttu-id="088a5-495">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-495">Assembly</span></span></td>
<td><span data-ttu-id="088a5-496">65</span><span class="sxs-lookup"><span data-stu-id="088a5-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-497">CC004</span><span class="sxs-lookup"><span data-stu-id="088a5-497">CC004</span></span></td>
<td><span data-ttu-id="088a5-498">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="088a5-498">Packaging</span></span></td>
<td><span data-ttu-id="088a5-499">35</span><span class="sxs-lookup"><span data-stu-id="088a5-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="088a5-500">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="088a5-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="088a5-501">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="088a5-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-502">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-502">Cost object</span></span></th>
<th><span data-ttu-id="088a5-503">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="088a5-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="088a5-504">Prod 1</span></span></td>
<td><span data-ttu-id="088a5-505">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-505">Product 1</span></span></td>
<td><span data-ttu-id="088a5-506">60</span><span class="sxs-lookup"><span data-stu-id="088a5-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="088a5-507">Prod 2</span></span></td>
<td><span data-ttu-id="088a5-508">2. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-508">Product 2</span></span></td>
<td><span data-ttu-id="088a5-509">20</span><span class="sxs-lookup"><span data-stu-id="088a5-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="088a5-510">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="088a5-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="088a5-511">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="088a5-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-512">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-512">Cost object</span></span></th>
<th><span data-ttu-id="088a5-513">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="088a5-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="088a5-514">Prod 1</span></span></td>
<td><span data-ttu-id="088a5-515">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-515">Product 1</span></span></td>
<td><span data-ttu-id="088a5-516">80</span><span class="sxs-lookup"><span data-stu-id="088a5-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="088a5-517">Prod 2</span></span></td>
<td><span data-ttu-id="088a5-518">2. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-518">Product 2</span></span></td>
<td><span data-ttu-id="088a5-519">15.</span><span class="sxs-lookup"><span data-stu-id="088a5-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="088a5-520">Sistēmā Finance and Operations statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="088a5-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="088a5-521">Sīkāku informāciju skatiet šeit: [Statistikas mēru nodrošinātāja veidne](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="088a5-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="088a5-522">Nākamajā tabulā ir parādīts rezultāts, ja tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījuma pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="088a5-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-523">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-523">Cost object</span></span></th>
<th><span data-ttu-id="088a5-524">Lielums</span><span class="sxs-lookup"><span data-stu-id="088a5-524">Magnitude</span></span></th>
<th><span data-ttu-id="088a5-525">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="088a5-525">Allocation factor</span></span></th>
<th><span data-ttu-id="088a5-526">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-526">Amount</span></span></th>
<th><span data-ttu-id="088a5-527">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="088a5-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-528">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-528">CC002</span></span></td>
<td><span data-ttu-id="088a5-529">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-529">Finance</span></span></td>
<td><span data-ttu-id="088a5-530">35</span><span class="sxs-lookup"><span data-stu-id="088a5-530">35</span></span></td>
<td><span data-ttu-id="088a5-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="088a5-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="088a5-532">175.00</span><span class="sxs-lookup"><span data-stu-id="088a5-532">175.00</span></span></td>
<td><span data-ttu-id="088a5-533">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-534">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-534">CC003</span></span></td>
<td><span data-ttu-id="088a5-535">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-535">Assembly</span></span></td>
<td><span data-ttu-id="088a5-536">55</span><span class="sxs-lookup"><span data-stu-id="088a5-536">55</span></span></td>
<td><span data-ttu-id="088a5-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="088a5-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="088a5-538">275.00</span><span class="sxs-lookup"><span data-stu-id="088a5-538">275.00</span></span></td>
<td><span data-ttu-id="088a5-539">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-540">CC004</span><span class="sxs-lookup"><span data-stu-id="088a5-540">CC004</span></span></td>
<td><span data-ttu-id="088a5-541">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="088a5-541">Packaging</span></span></td>
<td><span data-ttu-id="088a5-542">10.</span><span class="sxs-lookup"><span data-stu-id="088a5-542">10</span></span></td>
<td><span data-ttu-id="088a5-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="088a5-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="088a5-544">50,00</span><span class="sxs-lookup"><span data-stu-id="088a5-544">50.00</span></span></td>
<td><span data-ttu-id="088a5-545">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-546">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-546">CC002</span></span></td>
<td><span data-ttu-id="088a5-547">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-547">Finance</span></span></td>
<td><span data-ttu-id="088a5-548">35</span><span class="sxs-lookup"><span data-stu-id="088a5-548">35</span></span></td>
<td><span data-ttu-id="088a5-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="088a5-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="088a5-550">436.00</span><span class="sxs-lookup"><span data-stu-id="088a5-550">436.00</span></span></td>
<td><span data-ttu-id="088a5-551">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-552">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-552">CC003</span></span></td>
<td><span data-ttu-id="088a5-553">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-553">Assembly</span></span></td>
<td><span data-ttu-id="088a5-554">55</span><span class="sxs-lookup"><span data-stu-id="088a5-554">55</span></span></td>
<td><span data-ttu-id="088a5-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="088a5-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="088a5-556">685.14</span><span class="sxs-lookup"><span data-stu-id="088a5-556">685.14</span></span></td>
<td><span data-ttu-id="088a5-557">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-558">CC004</span><span class="sxs-lookup"><span data-stu-id="088a5-558">CC004</span></span></td>
<td><span data-ttu-id="088a5-559">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="088a5-559">Packaging</span></span></td>
<td><span data-ttu-id="088a5-560">10.</span><span class="sxs-lookup"><span data-stu-id="088a5-560">10</span></span></td>
<td><span data-ttu-id="088a5-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="088a5-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="088a5-562">124.57</span><span class="sxs-lookup"><span data-stu-id="088a5-562">124.57</span></span></td>
<td><span data-ttu-id="088a5-563">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="088a5-564">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="088a5-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-565">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-565">Cost object</span></span></th>
<th><span data-ttu-id="088a5-566">Lielums</span><span class="sxs-lookup"><span data-stu-id="088a5-566">Magnitude</span></span></th>
<th><span data-ttu-id="088a5-567">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="088a5-567">Allocation factor</span></span></th>
<th><span data-ttu-id="088a5-568">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-568">Amount</span></span></th>
<th><span data-ttu-id="088a5-569">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="088a5-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-570">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-570">CC003</span></span></td>
<td><span data-ttu-id="088a5-571">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-571">Assembly</span></span></td>
<td><span data-ttu-id="088a5-572">65</span><span class="sxs-lookup"><span data-stu-id="088a5-572">65</span></span></td>
<td><span data-ttu-id="088a5-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="088a5-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="088a5-574">438.75</span><span class="sxs-lookup"><span data-stu-id="088a5-574">438.75</span></span></td>
<td><span data-ttu-id="088a5-575">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-576">CC004</span><span class="sxs-lookup"><span data-stu-id="088a5-576">CC004</span></span></td>
<td><span data-ttu-id="088a5-577">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="088a5-577">Packaging</span></span></td>
<td><span data-ttu-id="088a5-578">35</span><span class="sxs-lookup"><span data-stu-id="088a5-578">35</span></span></td>
<td><span data-ttu-id="088a5-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="088a5-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="088a5-580">236.25</span><span class="sxs-lookup"><span data-stu-id="088a5-580">236.25</span></span></td>
<td><span data-ttu-id="088a5-581">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-582">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-582">CC003</span></span></td>
<td><span data-ttu-id="088a5-583">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-583">Assembly</span></span></td>
<td><span data-ttu-id="088a5-584">65</span><span class="sxs-lookup"><span data-stu-id="088a5-584">65</span></span></td>
<td><span data-ttu-id="088a5-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="088a5-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="088a5-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="088a5-586">5,297.69</span></span></td>
<td><span data-ttu-id="088a5-587">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-588">CC004</span><span class="sxs-lookup"><span data-stu-id="088a5-588">CC004</span></span></td>
<td><span data-ttu-id="088a5-589">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="088a5-589">Packaging</span></span></td>
<td><span data-ttu-id="088a5-590">35</span><span class="sxs-lookup"><span data-stu-id="088a5-590">35</span></span></td>
<td><span data-ttu-id="088a5-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="088a5-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="088a5-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="088a5-592">2,852.60</span></span></td>
<td><span data-ttu-id="088a5-593">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="088a5-594">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="088a5-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-595">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-595">Cost object</span></span></th>
<th><span data-ttu-id="088a5-596">Lielums</span><span class="sxs-lookup"><span data-stu-id="088a5-596">Magnitude</span></span></th>
<th><span data-ttu-id="088a5-597">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="088a5-597">Allocation factor</span></span></th>
<th><span data-ttu-id="088a5-598">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-598">Amount</span></span></th>
<th><span data-ttu-id="088a5-599">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="088a5-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="088a5-600">Prod 1</span></span></td>
<td><span data-ttu-id="088a5-601">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-601">Product 1</span></span></td>
<td><span data-ttu-id="088a5-602">60</span><span class="sxs-lookup"><span data-stu-id="088a5-602">60</span></span></td>
<td><span data-ttu-id="088a5-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="088a5-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="088a5-604">535.31</span><span class="sxs-lookup"><span data-stu-id="088a5-604">535.31</span></span></td>
<td><span data-ttu-id="088a5-605">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="088a5-606">Prod 2</span></span></td>
<td><span data-ttu-id="088a5-607">2. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-607">Product 2</span></span></td>
<td><span data-ttu-id="088a5-608">20.</span><span class="sxs-lookup"><span data-stu-id="088a5-608">20</span></span></td>
<td><span data-ttu-id="088a5-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="088a5-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="088a5-610">178.44</span><span class="sxs-lookup"><span data-stu-id="088a5-610">178.44</span></span></td>
<td><span data-ttu-id="088a5-611">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="088a5-612">Prod 1</span></span></td>
<td><span data-ttu-id="088a5-613">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-613">Product 1</span></span></td>
<td><span data-ttu-id="088a5-614">60</span><span class="sxs-lookup"><span data-stu-id="088a5-614">60</span></span></td>
<td><span data-ttu-id="088a5-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="088a5-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="088a5-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="088a5-616">4,487.12</span></span></td>
<td><span data-ttu-id="088a5-617">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="088a5-618">Prod 2</span></span></td>
<td><span data-ttu-id="088a5-619">2. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-619">Product 2</span></span></td>
<td><span data-ttu-id="088a5-620">20.</span><span class="sxs-lookup"><span data-stu-id="088a5-620">20</span></span></td>
<td><span data-ttu-id="088a5-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="088a5-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="088a5-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="088a5-622">1,495.71</span></span></td>
<td><span data-ttu-id="088a5-623">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="088a5-624">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="088a5-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-625">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-625">Cost object</span></span></th>
<th><span data-ttu-id="088a5-626">Lielums</span><span class="sxs-lookup"><span data-stu-id="088a5-626">Magnitude</span></span></th>
<th><span data-ttu-id="088a5-627">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="088a5-627">Allocation factor</span></span></th>
<th><span data-ttu-id="088a5-628">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-628">Amount</span></span></th>
<th><span data-ttu-id="088a5-629">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="088a5-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="088a5-630">Prod 1</span></span></td>
<td><span data-ttu-id="088a5-631">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-631">Product 1</span></span></td>
<td><span data-ttu-id="088a5-632">80</span><span class="sxs-lookup"><span data-stu-id="088a5-632">80</span></span></td>
<td><span data-ttu-id="088a5-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="088a5-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="088a5-634">241.05</span><span class="sxs-lookup"><span data-stu-id="088a5-634">241.05</span></span></td>
<td><span data-ttu-id="088a5-635">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="088a5-636">Prod 2</span></span></td>
<td><span data-ttu-id="088a5-637">2. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-637">Product 2</span></span></td>
<td><span data-ttu-id="088a5-638">15</span><span class="sxs-lookup"><span data-stu-id="088a5-638">15</span></span></td>
<td><span data-ttu-id="088a5-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="088a5-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="088a5-640">45.20</span><span class="sxs-lookup"><span data-stu-id="088a5-640">45.20</span></span></td>
<td><span data-ttu-id="088a5-641">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="088a5-642">Prod 1</span></span></td>
<td><span data-ttu-id="088a5-643">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-643">Product 1</span></span></td>
<td><span data-ttu-id="088a5-644">80</span><span class="sxs-lookup"><span data-stu-id="088a5-644">80</span></span></td>
<td><span data-ttu-id="088a5-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="088a5-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="088a5-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="088a5-646">2,507.09</span></span></td>
<td><span data-ttu-id="088a5-647">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="088a5-648">Prod 2</span></span></td>
<td><span data-ttu-id="088a5-649">2. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-649">Product 2</span></span></td>
<td><span data-ttu-id="088a5-650">15</span><span class="sxs-lookup"><span data-stu-id="088a5-650">15</span></span></td>
<td><span data-ttu-id="088a5-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="088a5-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="088a5-652">470.08</span><span class="sxs-lookup"><span data-stu-id="088a5-652">470.08</span></span></td>
<td><span data-ttu-id="088a5-653">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="088a5-654">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="088a5-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="088a5-655">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="088a5-655">Journal</span></span></th>
<th><span data-ttu-id="088a5-656">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="088a5-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="088a5-657">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="088a5-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="088a5-658">Versija</span><span class="sxs-lookup"><span data-stu-id="088a5-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-659">00004</span><span class="sxs-lookup"><span data-stu-id="088a5-659">00004</span></span></td>
<td><span data-ttu-id="088a5-660">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="088a5-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="088a5-661">Finanšu</span><span class="sxs-lookup"><span data-stu-id="088a5-661">Fiscal</span></span></td>
<td><span data-ttu-id="088a5-662">2017</span><span class="sxs-lookup"><span data-stu-id="088a5-662">2017</span></span></td>
<td><span data-ttu-id="088a5-663">Periods 1</span><span class="sxs-lookup"><span data-stu-id="088a5-663">Period 1</span></span></td>
<td><span data-ttu-id="088a5-664">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="088a5-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="088a5-665">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="088a5-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="088a5-666">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="088a5-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="088a5-667">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="088a5-668">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="088a5-668">Cost element</span></span></th>
<th><span data-ttu-id="088a5-669">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="088a5-669">Cost behavior</span></span></th>
<th><span data-ttu-id="088a5-670">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-671">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-672">CC001</span><span class="sxs-lookup"><span data-stu-id="088a5-672">CC001</span></span></td>
<td><span data-ttu-id="088a5-673">HR</span><span class="sxs-lookup"><span data-stu-id="088a5-673">HR</span></span></td>
<td><span data-ttu-id="088a5-674">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-674">10001</span></span></td>
<td><span data-ttu-id="088a5-675">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-675">Electricity</span></span></td>
<td><span data-ttu-id="088a5-676">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-676">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-677">500,00</span><span class="sxs-lookup"><span data-stu-id="088a5-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-678">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-679">CC001</span><span class="sxs-lookup"><span data-stu-id="088a5-679">CC001</span></span></td>
<td><span data-ttu-id="088a5-680">HR</span><span class="sxs-lookup"><span data-stu-id="088a5-680">HR</span></span></td>
<td><span data-ttu-id="088a5-681">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-681">10001</span></span></td>
<td><span data-ttu-id="088a5-682">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-682">Electricity</span></span></td>
<td><span data-ttu-id="088a5-683">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-683">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="088a5-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-685">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-686">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-686">CC002</span></span></td>
<td><span data-ttu-id="088a5-687">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-687">Finance</span></span></td>
<td><span data-ttu-id="088a5-688">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-688">10001</span></span></td>
<td><span data-ttu-id="088a5-689">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-689">Electricity</span></span></td>
<td><span data-ttu-id="088a5-690">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-690">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-691">675.00</span><span class="sxs-lookup"><span data-stu-id="088a5-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-692">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-693">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-693">CC002</span></span></td>
<td><span data-ttu-id="088a5-694">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-694">Finance</span></span></td>
<td><span data-ttu-id="088a5-695">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-695">10001</span></span></td>
<td><span data-ttu-id="088a5-696">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-696">Electricity</span></span></td>
<td><span data-ttu-id="088a5-697">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-697">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="088a5-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-699">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-700">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-700">CC003</span></span></td>
<td><span data-ttu-id="088a5-701">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-701">Assembly</span></span></td>
<td><span data-ttu-id="088a5-702">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-702">10001</span></span></td>
<td><span data-ttu-id="088a5-703">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-703">Electricity</span></span></td>
<td><span data-ttu-id="088a5-704">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-704">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-705">713.75</span><span class="sxs-lookup"><span data-stu-id="088a5-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-706">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-707">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-707">CC003</span></span></td>
<td><span data-ttu-id="088a5-708">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-708">Assembly</span></span></td>
<td><span data-ttu-id="088a5-709">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-709">10001</span></span></td>
<td><span data-ttu-id="088a5-710">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-710">Electricity</span></span></td>
<td><span data-ttu-id="088a5-711">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-711">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="088a5-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-713">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-714">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-714">CC003</span></span></td>
<td><span data-ttu-id="088a5-715">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="088a5-715">Packaging</span></span></td>
<td><span data-ttu-id="088a5-716">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-716">10001</span></span></td>
<td><span data-ttu-id="088a5-717">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-717">Electricity</span></span></td>
<td><span data-ttu-id="088a5-718">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-718">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-719">286.25</span><span class="sxs-lookup"><span data-stu-id="088a5-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-720">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-721">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-721">CC003</span></span></td>
<td><span data-ttu-id="088a5-722">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="088a5-722">Packaging</span></span></td>
<td><span data-ttu-id="088a5-723">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-723">10001</span></span></td>
<td><span data-ttu-id="088a5-724">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-724">Electricity</span></span></td>
<td><span data-ttu-id="088a5-725">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-725">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="088a5-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-727">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="088a5-728">Prod 1</span></span></td>
<td><span data-ttu-id="088a5-729">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-729">Product 1</span></span></td>
<td><span data-ttu-id="088a5-730">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-730">10001</span></span></td>
<td><span data-ttu-id="088a5-731">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-731">Electricity</span></span></td>
<td><span data-ttu-id="088a5-732">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-732">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-733">776.36</span><span class="sxs-lookup"><span data-stu-id="088a5-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-734">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="088a5-735">Prod 1</span></span></td>
<td><span data-ttu-id="088a5-736">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-736">Product 1</span></span></td>
<td><span data-ttu-id="088a5-737">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-737">10001</span></span></td>
<td><span data-ttu-id="088a5-738">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-738">Electricity</span></span></td>
<td><span data-ttu-id="088a5-739">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-739">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="088a5-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-741">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="088a5-742">Prod 2</span></span></td>
<td><span data-ttu-id="088a5-743">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-743">Product 1</span></span></td>
<td><span data-ttu-id="088a5-744">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-744">10001</span></span></td>
<td><span data-ttu-id="088a5-745">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-745">Electricity</span></span></td>
<td><span data-ttu-id="088a5-746">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-746">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-747">223.64</span><span class="sxs-lookup"><span data-stu-id="088a5-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-748">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="088a5-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="088a5-749">Prod 2</span></span></td>
<td><span data-ttu-id="088a5-750">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-750">Product 1</span></span></td>
<td><span data-ttu-id="088a5-751">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-751">10001</span></span></td>
<td><span data-ttu-id="088a5-752">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-752">Electricity</span></span></td>
<td><span data-ttu-id="088a5-753">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-753">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="088a5-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="088a5-755">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="088a5-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="088a5-756">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="088a5-757">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="088a5-757">Cost element</span></span></th>
<th><span data-ttu-id="088a5-758">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="088a5-758">Cost behavior</span></span></th>
<th><span data-ttu-id="088a5-759">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-759">Amount</span></span></th>
<th><span data-ttu-id="088a5-760">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="088a5-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="088a5-761">CC001</span><span class="sxs-lookup"><span data-stu-id="088a5-761">CC001</span></span></td>
<td><span data-ttu-id="088a5-762">HR</span><span class="sxs-lookup"><span data-stu-id="088a5-762">HR</span></span></td>
<td><span data-ttu-id="088a5-763">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-763">10001</span></span></td>
<td><span data-ttu-id="088a5-764">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-764">Electricity</span></span></td>
<td><span data-ttu-id="088a5-765">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-765">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="088a5-766">-500.00</span></span></td>
<td><span data-ttu-id="088a5-767">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-768">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-768">CC002</span></span></td>
<td><span data-ttu-id="088a5-769">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-769">Finance</span></span></td>
<td><span data-ttu-id="088a5-770">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-770">10001</span></span></td>
<td><span data-ttu-id="088a5-771">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-771">Electricity</span></span></td>
<td><span data-ttu-id="088a5-772">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-772">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-773">175.00</span><span class="sxs-lookup"><span data-stu-id="088a5-773">175.00</span></span></td>
<td><span data-ttu-id="088a5-774">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-775">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-775">CC003</span></span></td>
<td><span data-ttu-id="088a5-776">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-776">Assembly</span></span></td>
<td><span data-ttu-id="088a5-777">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-777">10001</span></span></td>
<td><span data-ttu-id="088a5-778">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-778">Electricity</span></span></td>
<td><span data-ttu-id="088a5-779">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-779">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-780">275.00</span><span class="sxs-lookup"><span data-stu-id="088a5-780">275.00</span></span></td>
<td><span data-ttu-id="088a5-781">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-782">CC004</span><span class="sxs-lookup"><span data-stu-id="088a5-782">CC004</span></span></td>
<td><span data-ttu-id="088a5-783">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="088a5-783">Packaging</span></span></td>
<td><span data-ttu-id="088a5-784">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-784">10001</span></span></td>
<td><span data-ttu-id="088a5-785">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-785">Electricity</span></span></td>
<td><span data-ttu-id="088a5-786">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-786">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-787">50,00</span><span class="sxs-lookup"><span data-stu-id="088a5-787">50,00</span></span></td>
<td><span data-ttu-id="088a5-788">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-789">CC001</span><span class="sxs-lookup"><span data-stu-id="088a5-789">CC001</span></span></td>
<td><span data-ttu-id="088a5-790">HR</span><span class="sxs-lookup"><span data-stu-id="088a5-790">HR</span></span></td>
<td><span data-ttu-id="088a5-791">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-791">10001</span></span></td>
<td><span data-ttu-id="088a5-792">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-792">Electricity</span></span></td>
<td><span data-ttu-id="088a5-793">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-793">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="088a5-794">-1,245.71</span></span></td>
<td><span data-ttu-id="088a5-795">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-796">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-796">CC002</span></span></td>
<td><span data-ttu-id="088a5-797">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-797">Finance</span></span></td>
<td><span data-ttu-id="088a5-798">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-798">10001</span></span></td>
<td><span data-ttu-id="088a5-799">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-799">Electricity</span></span></td>
<td><span data-ttu-id="088a5-800">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-800">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-801">436.00</span><span class="sxs-lookup"><span data-stu-id="088a5-801">436.00</span></span></td>
<td><span data-ttu-id="088a5-802">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-803">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-803">CC003</span></span></td>
<td><span data-ttu-id="088a5-804">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-804">Assembly</span></span></td>
<td><span data-ttu-id="088a5-805">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-805">10001</span></span></td>
<td><span data-ttu-id="088a5-806">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-806">Electricity</span></span></td>
<td><span data-ttu-id="088a5-807">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-807">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-808">685.14</span><span class="sxs-lookup"><span data-stu-id="088a5-808">685.14</span></span></td>
<td><span data-ttu-id="088a5-809">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-810">CC004</span><span class="sxs-lookup"><span data-stu-id="088a5-810">CC004</span></span></td>
<td><span data-ttu-id="088a5-811">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="088a5-811">Packaging</span></span></td>
<td><span data-ttu-id="088a5-812">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-812">10001</span></span></td>
<td><span data-ttu-id="088a5-813">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-813">Electricity</span></span></td>
<td><span data-ttu-id="088a5-814">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-814">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-815">124.57</span><span class="sxs-lookup"><span data-stu-id="088a5-815">124.57</span></span></td>
<td><span data-ttu-id="088a5-816">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-817">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-817">CC002</span></span></td>
<td><span data-ttu-id="088a5-818">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-818">Finance</span></span></td>
<td><span data-ttu-id="088a5-819">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-819">10001</span></span></td>
<td><span data-ttu-id="088a5-820">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-820">Electricity</span></span></td>
<td><span data-ttu-id="088a5-821">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-821">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="088a5-822">-675.00</span></span></td>
<td><span data-ttu-id="088a5-823">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-824">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-824">CC003</span></span></td>
<td><span data-ttu-id="088a5-825">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-825">Assembly</span></span></td>
<td><span data-ttu-id="088a5-826">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-826">10001</span></span></td>
<td><span data-ttu-id="088a5-827">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-827">Electricity</span></span></td>
<td><span data-ttu-id="088a5-828">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-828">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-829">438.75</span><span class="sxs-lookup"><span data-stu-id="088a5-829">438.75</span></span></td>
<td><span data-ttu-id="088a5-830">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-831">CC004</span><span class="sxs-lookup"><span data-stu-id="088a5-831">CC004</span></span></td>
<td><span data-ttu-id="088a5-832">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="088a5-832">Packaging</span></span></td>
<td><span data-ttu-id="088a5-833">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-833">10001</span></span></td>
<td><span data-ttu-id="088a5-834">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-834">Electricity</span></span></td>
<td><span data-ttu-id="088a5-835">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-835">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-836">236.25</span><span class="sxs-lookup"><span data-stu-id="088a5-836">236.25</span></span></td>
<td><span data-ttu-id="088a5-837">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-838">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-838">CC002</span></span></td>
<td><span data-ttu-id="088a5-839">Finanses</span><span class="sxs-lookup"><span data-stu-id="088a5-839">Finance</span></span></td>
<td><span data-ttu-id="088a5-840">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-840">10001</span></span></td>
<td><span data-ttu-id="088a5-841">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-841">Electricity</span></span></td>
<td><span data-ttu-id="088a5-842">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-842">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="088a5-843">-8,150.29</span></span></td>
<td><span data-ttu-id="088a5-844">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-845">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-845">CC003</span></span></td>
<td><span data-ttu-id="088a5-846">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-846">Assembly</span></span></td>
<td><span data-ttu-id="088a5-847">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-847">10001</span></span></td>
<td><span data-ttu-id="088a5-848">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-848">Electricity</span></span></td>
<td><span data-ttu-id="088a5-849">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-849">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="088a5-850">5,297.69</span></span></td>
<td><span data-ttu-id="088a5-851">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-852">CC004</span><span class="sxs-lookup"><span data-stu-id="088a5-852">CC004</span></span></td>
<td><span data-ttu-id="088a5-853">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="088a5-853">Packaging</span></span></td>
<td><span data-ttu-id="088a5-854">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-854">10001</span></span></td>
<td><span data-ttu-id="088a5-855">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-855">Electricity</span></span></td>
<td><span data-ttu-id="088a5-856">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-856">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="088a5-857">2,852.60</span></span></td>
<td><span data-ttu-id="088a5-858">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-859">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-859">CC003</span></span></td>
<td><span data-ttu-id="088a5-860">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-860">Assembly</span></span></td>
<td><span data-ttu-id="088a5-861">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-861">10001</span></span></td>
<td><span data-ttu-id="088a5-862">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-862">Electricity</span></span></td>
<td><span data-ttu-id="088a5-863">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-863">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="088a5-864">-713.75</span></span></td>
<td><span data-ttu-id="088a5-865">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="088a5-866">Prod 1</span></span></td>
<td><span data-ttu-id="088a5-867">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-867">Product 1</span></span></td>
<td><span data-ttu-id="088a5-868">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-868">10001</span></span></td>
<td><span data-ttu-id="088a5-869">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-869">Electricity</span></span></td>
<td><span data-ttu-id="088a5-870">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-870">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-871">535.31</span><span class="sxs-lookup"><span data-stu-id="088a5-871">535.31</span></span></td>
<td><span data-ttu-id="088a5-872">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="088a5-873">Prod 2</span></span></td>
<td><span data-ttu-id="088a5-874">2. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-874">Product 2</span></span></td>
<td><span data-ttu-id="088a5-875">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-875">10001</span></span></td>
<td><span data-ttu-id="088a5-876">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-876">Electricity</span></span></td>
<td><span data-ttu-id="088a5-877">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-877">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-878">178.44</span><span class="sxs-lookup"><span data-stu-id="088a5-878">178.44</span></span></td>
<td><span data-ttu-id="088a5-879">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-880">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-880">CC003</span></span></td>
<td><span data-ttu-id="088a5-881">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-881">Assembly</span></span></td>
<td><span data-ttu-id="088a5-882">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-882">10001</span></span></td>
<td><span data-ttu-id="088a5-883">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-883">Electricity</span></span></td>
<td><span data-ttu-id="088a5-884">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-884">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="088a5-885">-5,982.83</span></span></td>
<td><span data-ttu-id="088a5-886">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="088a5-887">Prod 1</span></span></td>
<td><span data-ttu-id="088a5-888">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-888">Product 1</span></span></td>
<td><span data-ttu-id="088a5-889">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-889">10001</span></span></td>
<td><span data-ttu-id="088a5-890">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-890">Electricity</span></span></td>
<td><span data-ttu-id="088a5-891">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-891">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="088a5-892">4,487.12</span></span></td>
<td><span data-ttu-id="088a5-893">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="088a5-894">Prod 2</span></span></td>
<td><span data-ttu-id="088a5-895">2. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-895">Product 2</span></span></td>
<td><span data-ttu-id="088a5-896">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-896">10001</span></span></td>
<td><span data-ttu-id="088a5-897">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-897">Electricity</span></span></td>
<td><span data-ttu-id="088a5-898">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-898">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="088a5-899">1,495.71</span></span></td>
<td><span data-ttu-id="088a5-900">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-901">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-901">CC003</span></span></td>
<td><span data-ttu-id="088a5-902">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-902">Assembly</span></span></td>
<td><span data-ttu-id="088a5-903">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-903">10001</span></span></td>
<td><span data-ttu-id="088a5-904">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-904">Electricity</span></span></td>
<td><span data-ttu-id="088a5-905">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-905">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="088a5-906">-286.25</span></span></td>
<td><span data-ttu-id="088a5-907">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="088a5-908">Prod 1</span></span></td>
<td><span data-ttu-id="088a5-909">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-909">Product 1</span></span></td>
<td><span data-ttu-id="088a5-910">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-910">10001</span></span></td>
<td><span data-ttu-id="088a5-911">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-911">Electricity</span></span></td>
<td><span data-ttu-id="088a5-912">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-912">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-913">241.05</span><span class="sxs-lookup"><span data-stu-id="088a5-913">241.05</span></span></td>
<td><span data-ttu-id="088a5-914">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="088a5-915">Prod 2</span></span></td>
<td><span data-ttu-id="088a5-916">2. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-916">Product 2</span></span></td>
<td><span data-ttu-id="088a5-917">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-917">10001</span></span></td>
<td><span data-ttu-id="088a5-918">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-918">Electricity</span></span></td>
<td><span data-ttu-id="088a5-919">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-919">Fixed cost</span></span></td>
<td><span data-ttu-id="088a5-920">45.20</span><span class="sxs-lookup"><span data-stu-id="088a5-920">45.20</span></span></td>
<td><span data-ttu-id="088a5-921">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-922">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-922">CC003</span></span></td>
<td><span data-ttu-id="088a5-923">Montāža</span><span class="sxs-lookup"><span data-stu-id="088a5-923">Assembly</span></span></td>
<td><span data-ttu-id="088a5-924">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-924">10001</span></span></td>
<td><span data-ttu-id="088a5-925">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-925">Electricity</span></span></td>
<td><span data-ttu-id="088a5-926">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-926">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="088a5-927">-2,977.17</span></span></td>
<td><span data-ttu-id="088a5-928">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="088a5-929">Prod 1</span></span></td>
<td><span data-ttu-id="088a5-930">1. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-930">Product 1</span></span></td>
<td><span data-ttu-id="088a5-931">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-931">10001</span></span></td>
<td><span data-ttu-id="088a5-932">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-932">Electricity</span></span></td>
<td><span data-ttu-id="088a5-933">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-933">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="088a5-934">2,507.09</span></span></td>
<td><span data-ttu-id="088a5-935">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="088a5-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="088a5-936">Prod 2</span></span></td>
<td><span data-ttu-id="088a5-937">2. prece</span><span class="sxs-lookup"><span data-stu-id="088a5-937">Product 2</span></span></td>
<td><span data-ttu-id="088a5-938">10001</span><span class="sxs-lookup"><span data-stu-id="088a5-938">10001</span></span></td>
<td><span data-ttu-id="088a5-939">Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-939">Electricity</span></span></td>
<td><span data-ttu-id="088a5-940">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-940">Variable cost</span></span></td>
<td><span data-ttu-id="088a5-941">470.08</span><span class="sxs-lookup"><span data-stu-id="088a5-941">470.08</span></span></td>
<td><span data-ttu-id="088a5-942">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="088a5-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="088a5-943">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="088a5-943">Conclusion</span></span>
<span data-ttu-id="088a5-944">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="088a5-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="088a5-945">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="088a5-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="088a5-946">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="088a5-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="088a5-947">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="088a5-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="088a5-948">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="088a5-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="088a5-949">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="088a5-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="088a5-950">Summa</span><span class="sxs-lookup"><span data-stu-id="088a5-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="088a5-951">CC099</span><span class="sxs-lookup"><span data-stu-id="088a5-951">CC099</span></span></th>
<th><span data-ttu-id="088a5-952">CC001</span><span class="sxs-lookup"><span data-stu-id="088a5-952">CC001</span></span></th>
<th><span data-ttu-id="088a5-953">CC002</span><span class="sxs-lookup"><span data-stu-id="088a5-953">CC002</span></span></th>
<th><span data-ttu-id="088a5-954">CC003</span><span class="sxs-lookup"><span data-stu-id="088a5-954">CC003</span></span></th>
<th><span data-ttu-id="088a5-955">CC004</span><span class="sxs-lookup"><span data-stu-id="088a5-955">CC004</span></span></th>
<th><span data-ttu-id="088a5-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="088a5-956">Proj 1</span></span></th>
<th><span data-ttu-id="088a5-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="088a5-957">Proj 2</span></span></th>
<th><span data-ttu-id="088a5-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="088a5-958">Prod 1</span></span></th>
<th><span data-ttu-id="088a5-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="088a5-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="088a5-960">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="088a5-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="088a5-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="088a5-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="088a5-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="088a5-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="088a5-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="088a5-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="088a5-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="088a5-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="088a5-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="088a5-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="088a5-970">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="088a5-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-971">0,00</span><span class="sxs-lookup"><span data-stu-id="088a5-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="088a5-972">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-973">0,00</span><span class="sxs-lookup"><span data-stu-id="088a5-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-974">0,00</span><span class="sxs-lookup"><span data-stu-id="088a5-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-975">0,00</span><span class="sxs-lookup"><span data-stu-id="088a5-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-976">0,00</span><span class="sxs-lookup"><span data-stu-id="088a5-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-977">0,00</span><span class="sxs-lookup"><span data-stu-id="088a5-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="088a5-978">776.36</span><span class="sxs-lookup"><span data-stu-id="088a5-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-979">223.64</span><span class="sxs-lookup"><span data-stu-id="088a5-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="088a5-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="088a5-981">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="088a5-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-982">000</span><span class="sxs-lookup"><span data-stu-id="088a5-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-983">0,00</span><span class="sxs-lookup"><span data-stu-id="088a5-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-984">0,00</span><span class="sxs-lookup"><span data-stu-id="088a5-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-985">0,00</span><span class="sxs-lookup"><span data-stu-id="088a5-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-986">0,00</span><span class="sxs-lookup"><span data-stu-id="088a5-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-987">30,00</span><span class="sxs-lookup"><span data-stu-id="088a5-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-988">10,00</span><span class="sxs-lookup"><span data-stu-id="088a5-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="088a5-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="088a5-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="088a5-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="088a5-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="088a5-992">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="088a5-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="088a5-993">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="088a5-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="088a5-994">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="088a5-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="088a5-995">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="088a5-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="088a5-996">Sīkāku informāciju skatiet šeit: [Izmaksu apkopošanas politika](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="088a5-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



