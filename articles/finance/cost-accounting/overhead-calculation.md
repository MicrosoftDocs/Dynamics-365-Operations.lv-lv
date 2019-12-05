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
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770808"
---
# <a name="overhead-calculation"></a><span data-ttu-id="7d6c0-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="7d6c0-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d6c0-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="7d6c0-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="7d6c0-105">Term definition</span></span>
---------------

<span data-ttu-id="7d6c0-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="7d6c0-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="7d6c0-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="7d6c0-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="7d6c0-109">Īre</span><span class="sxs-lookup"><span data-stu-id="7d6c0-109">Rent</span></span>
-   <span data-ttu-id="7d6c0-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-110">Electricity</span></span>
-   <span data-ttu-id="7d6c0-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="7d6c0-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="7d6c0-112">Overhead calculation overview</span></span>
<span data-ttu-id="7d6c0-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="7d6c0-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="7d6c0-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="7d6c0-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="7d6c0-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="7d6c0-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="7d6c0-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="7d6c0-119">Version type</span></span>
-   <span data-ttu-id="7d6c0-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="7d6c0-120">Date and time</span></span>
-   <span data-ttu-id="7d6c0-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="7d6c0-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="7d6c0-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="7d6c0-122">Fiscal year</span></span>
-   <span data-ttu-id="7d6c0-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="7d6c0-123">Fiscal period</span></span>

<span data-ttu-id="7d6c0-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="7d6c0-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="7d6c0-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="7d6c0-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="7d6c0-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="7d6c0-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="7d6c0-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="7d6c0-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="7d6c0-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="7d6c0-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="7d6c0-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="7d6c0-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="7d6c0-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="7d6c0-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7d6c0-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7d6c0-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7d6c0-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="7d6c0-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-140">Main account</span></span></th>
<th><span data-ttu-id="7d6c0-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="7d6c0-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-143">CC099</span><span class="sxs-lookup"><span data-stu-id="7d6c0-143">CC099</span></span></td>
<td><span data-ttu-id="7d6c0-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7d6c0-144">Default cost center</span></span></td>
<td><span data-ttu-id="7d6c0-145">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-145">10001</span></span></td>
<td><span data-ttu-id="7d6c0-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-146">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="7d6c0-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="7d6c0-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="7d6c0-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="7d6c0-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="7d6c0-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="7d6c0-151">Define the cost behavior rule</span></span>

<span data-ttu-id="7d6c0-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="7d6c0-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="7d6c0-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="7d6c0-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="7d6c0-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="7d6c0-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="7d6c0-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="7d6c0-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="7d6c0-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7d6c0-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7d6c0-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7d6c0-160">Journal</span></span></th>
<th><span data-ttu-id="7d6c0-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="7d6c0-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7d6c0-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="7d6c0-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7d6c0-163">Versija</span><span class="sxs-lookup"><span data-stu-id="7d6c0-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-164">00001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-164">00001</span></span></td>
<td><span data-ttu-id="7d6c0-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="7d6c0-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="7d6c0-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="7d6c0-166">Fiscal</span></span></td>
<td><span data-ttu-id="7d6c0-167">2017</span><span class="sxs-lookup"><span data-stu-id="7d6c0-167">2017</span></span></td>
<td><span data-ttu-id="7d6c0-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-168">Period 1</span></span></td>
<td><span data-ttu-id="7d6c0-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="7d6c0-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7d6c0-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7d6c0-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7d6c0-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7d6c0-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7d6c0-173">Cost element</span></span></th>
<th><span data-ttu-id="7d6c0-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7d6c0-174">Cost behavior</span></span></th>
<th><span data-ttu-id="7d6c0-175">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-177">CC099</span><span class="sxs-lookup"><span data-stu-id="7d6c0-177">CC099</span></span></td>
<td><span data-ttu-id="7d6c0-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7d6c0-178">Default cost center</span></span></td>
<td><span data-ttu-id="7d6c0-179">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-179">10001</span></span></td>
<td><span data-ttu-id="7d6c0-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-180">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-181">Unclassified</span></span></td>
<td><span data-ttu-id="7d6c0-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7d6c0-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="7d6c0-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7d6c0-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7d6c0-185">Cost element</span></span></th>
<th><span data-ttu-id="7d6c0-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7d6c0-186">Cost behavior</span></span></th>
<th><span data-ttu-id="7d6c0-187">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-187">Amount</span></span></th>
<th><span data-ttu-id="7d6c0-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-189">CC099</span><span class="sxs-lookup"><span data-stu-id="7d6c0-189">CC099</span></span></td>
<td><span data-ttu-id="7d6c0-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7d6c0-190">Default cost center</span></span></td>
<td><span data-ttu-id="7d6c0-191">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-191">10001</span></span></td>
<td><span data-ttu-id="7d6c0-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-192">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-193">Unclassified</span></span></td>
<td><span data-ttu-id="7d6c0-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-194">10,000.00</span></span></td>
<td><span data-ttu-id="7d6c0-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-196">CC099</span><span class="sxs-lookup"><span data-stu-id="7d6c0-196">CC099</span></span></td>
<td><span data-ttu-id="7d6c0-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7d6c0-197">Default cost center</span></span></td>
<td><span data-ttu-id="7d6c0-198">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-198">10001</span></span></td>
<td><span data-ttu-id="7d6c0-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-199">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-200">Unclassified</span></span></td>
<td><span data-ttu-id="7d6c0-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-201">-10,000.00</span></span></td>
<td><span data-ttu-id="7d6c0-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-203">CC099</span><span class="sxs-lookup"><span data-stu-id="7d6c0-203">CC099</span></span></td>
<td><span data-ttu-id="7d6c0-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7d6c0-204">Default cost center</span></span></td>
<td><span data-ttu-id="7d6c0-205">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-205">10001</span></span></td>
<td><span data-ttu-id="7d6c0-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-206">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-207">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-208">1,000.00</span></span></td>
<td><span data-ttu-id="7d6c0-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-210">CC099</span><span class="sxs-lookup"><span data-stu-id="7d6c0-210">CC099</span></span></td>
<td><span data-ttu-id="7d6c0-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7d6c0-211">Default cost center</span></span></td>
<td><span data-ttu-id="7d6c0-212">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-212">10001</span></span></td>
<td><span data-ttu-id="7d6c0-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-213">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-214">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-215">9,000.00</span></span></td>
<td><span data-ttu-id="7d6c0-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7d6c0-217">Sīkāku informāciju skatiet šeit: [Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="7d6c0-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="7d6c0-218">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="7d6c0-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="7d6c0-219">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="7d6c0-220">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="7d6c0-221">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="7d6c0-221">Define the cost distribution rule</span></span>

<span data-ttu-id="7d6c0-222">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="7d6c0-223">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="7d6c0-224">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="7d6c0-225">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="7d6c0-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="7d6c0-226">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="7d6c0-227">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-228">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-228">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="7d6c0-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-230">CC001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-230">CC001</span></span></td>
<td><span data-ttu-id="7d6c0-231">HR</span><span class="sxs-lookup"><span data-stu-id="7d6c0-231">HR</span></span></td>
<td><span data-ttu-id="7d6c0-232">1000</span><span class="sxs-lookup"><span data-stu-id="7d6c0-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-233">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-233">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-234">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-234">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-235">6,000</span><span class="sxs-lookup"><span data-stu-id="7d6c0-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-236">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-236">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-237">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-237">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-238">0</span><span class="sxs-lookup"><span data-stu-id="7d6c0-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7d6c0-239">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-240">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-240">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-241">Lielums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-241">Magnitude</span></span></th>
<th><span data-ttu-id="7d6c0-242">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7d6c0-242">Allocation factor</span></span></th>
<th><span data-ttu-id="7d6c0-243">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-244">CC001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-244">CC001</span></span></td>
<td><span data-ttu-id="7d6c0-245">HR</span><span class="sxs-lookup"><span data-stu-id="7d6c0-245">HR</span></span></td>
<td><span data-ttu-id="7d6c0-246">1000</span><span class="sxs-lookup"><span data-stu-id="7d6c0-246">1,000</span></span></td>
<td><span data-ttu-id="7d6c0-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7d6c0-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7d6c0-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-249">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-249">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-250">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-250">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-251">6,000</span><span class="sxs-lookup"><span data-stu-id="7d6c0-251">6,000</span></span></td>
<td><span data-ttu-id="7d6c0-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7d6c0-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7d6c0-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-254">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-254">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-255">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-255">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-256">0</span><span class="sxs-lookup"><span data-stu-id="7d6c0-256">0</span></span></td>
<td><span data-ttu-id="7d6c0-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7d6c0-258">0,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7d6c0-259">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="7d6c0-260">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-261">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-261">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-262">Formula</span><span class="sxs-lookup"><span data-stu-id="7d6c0-262">Formula</span></span></th>
<th><span data-ttu-id="7d6c0-263">Lielums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-263">Magnitude</span></span></th>
<th><span data-ttu-id="7d6c0-264">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7d6c0-264">Allocation factor</span></span></th>
<th><span data-ttu-id="7d6c0-265">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-266">CC001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-266">CC001</span></span></td>
<td><span data-ttu-id="7d6c0-267">HR</span><span class="sxs-lookup"><span data-stu-id="7d6c0-267">HR</span></span></td>
<td><span data-ttu-id="7d6c0-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7d6c0-269">1.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-269">1</span></span></td>
<td><span data-ttu-id="7d6c0-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7d6c0-271">500,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-272">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-272">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-273">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-273">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7d6c0-275">1.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-275">1</span></span></td>
<td><span data-ttu-id="7d6c0-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7d6c0-277">500,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-278">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-278">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-279">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-279">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7d6c0-281">0</span><span class="sxs-lookup"><span data-stu-id="7d6c0-281">0</span></span></td>
<td><span data-ttu-id="7d6c0-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7d6c0-283">0,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7d6c0-284">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7d6c0-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7d6c0-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7d6c0-285">Journal</span></span></th>
<th><span data-ttu-id="7d6c0-286">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="7d6c0-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7d6c0-287">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="7d6c0-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7d6c0-288">Versija</span><span class="sxs-lookup"><span data-stu-id="7d6c0-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-289">00002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-289">00002</span></span></td>
<td><span data-ttu-id="7d6c0-290">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="7d6c0-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="7d6c0-291">Finanšu</span><span class="sxs-lookup"><span data-stu-id="7d6c0-291">Fiscal</span></span></td>
<td><span data-ttu-id="7d6c0-292">2017</span><span class="sxs-lookup"><span data-stu-id="7d6c0-292">2017</span></span></td>
<td><span data-ttu-id="7d6c0-293">Periods 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-293">Period 1</span></span></td>
<td><span data-ttu-id="7d6c0-294">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="7d6c0-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7d6c0-295">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7d6c0-296">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7d6c0-297">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7d6c0-298">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7d6c0-298">Cost element</span></span></th>
<th><span data-ttu-id="7d6c0-299">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7d6c0-299">Cost behavior</span></span></th>
<th><span data-ttu-id="7d6c0-300">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-301">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-302">CC099</span><span class="sxs-lookup"><span data-stu-id="7d6c0-302">CC099</span></span></td>
<td><span data-ttu-id="7d6c0-303">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7d6c0-303">Default cost center</span></span></td>
<td><span data-ttu-id="7d6c0-304">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-304">10001</span></span></td>
<td><span data-ttu-id="7d6c0-305">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-305">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-306">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-306">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-308">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-309">CC099</span><span class="sxs-lookup"><span data-stu-id="7d6c0-309">CC099</span></span></td>
<td><span data-ttu-id="7d6c0-310">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7d6c0-310">Default cost center</span></span></td>
<td><span data-ttu-id="7d6c0-311">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-311">10001</span></span></td>
<td><span data-ttu-id="7d6c0-312">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-312">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-313">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-313">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7d6c0-315">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="7d6c0-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-316">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7d6c0-317">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7d6c0-317">Cost element</span></span></th>
<th><span data-ttu-id="7d6c0-318">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7d6c0-318">Cost behavior</span></span></th>
<th><span data-ttu-id="7d6c0-319">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-319">Amount</span></span></th>
<th><span data-ttu-id="7d6c0-320">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-321">CC099</span><span class="sxs-lookup"><span data-stu-id="7d6c0-321">CC099</span></span></td>
<td><span data-ttu-id="7d6c0-322">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7d6c0-322">Default cost center</span></span></td>
<td><span data-ttu-id="7d6c0-323">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-323">10001</span></span></td>
<td><span data-ttu-id="7d6c0-324">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-324">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-325">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-325">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-326">-1000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-326">-1,000.00</span></span></td>
<td><span data-ttu-id="7d6c0-327">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-328">CC001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-328">CC001</span></span></td>
<td><span data-ttu-id="7d6c0-329">HR</span><span class="sxs-lookup"><span data-stu-id="7d6c0-329">HR</span></span></td>
<td><span data-ttu-id="7d6c0-330">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-330">10001</span></span></td>
<td><span data-ttu-id="7d6c0-331">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-331">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-332">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-332">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-333">500,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-333">500.00</span></span></td>
<td><span data-ttu-id="7d6c0-334">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-335">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-335">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-336">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-336">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-337">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-337">10001</span></span></td>
<td><span data-ttu-id="7d6c0-338">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-338">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-339">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-339">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-340">500,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-340">500.00</span></span></td>
<td><span data-ttu-id="7d6c0-341">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-342">CC099</span><span class="sxs-lookup"><span data-stu-id="7d6c0-342">CC099</span></span></td>
<td><span data-ttu-id="7d6c0-343">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7d6c0-343">Default cost center</span></span></td>
<td><span data-ttu-id="7d6c0-344">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-344">10001</span></span></td>
<td><span data-ttu-id="7d6c0-345">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-345">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-346">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-346">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-347">-9,000.00</span></span></td>
<td><span data-ttu-id="7d6c0-348">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-349">CC001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-349">CC001</span></span></td>
<td><span data-ttu-id="7d6c0-350">HR</span><span class="sxs-lookup"><span data-stu-id="7d6c0-350">HR</span></span></td>
<td><span data-ttu-id="7d6c0-351">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-351">10001</span></span></td>
<td><span data-ttu-id="7d6c0-352">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-352">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-353">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-353">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7d6c0-354">1,285.71</span></span></td>
<td><span data-ttu-id="7d6c0-355">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-356">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-356">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-357">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-357">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-358">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-358">10001</span></span></td>
<td><span data-ttu-id="7d6c0-359">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-359">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-360">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-360">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7d6c0-361">7,714.29</span></span></td>
<td><span data-ttu-id="7d6c0-362">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7d6c0-363">Sīkāku informāciju skatiet šeit: [Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="7d6c0-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="7d6c0-364">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="7d6c0-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="7d6c0-365">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="7d6c0-366">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="7d6c0-367">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="7d6c0-367">Define the overhead rate</span></span>

<span data-ttu-id="7d6c0-368">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="7d6c0-369">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-370">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-370">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-371">Stundas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-372">Proj 1</span></span></td>
<td><span data-ttu-id="7d6c0-373">1. projekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-373">Project 1</span></span></td>
<td><span data-ttu-id="7d6c0-374">3.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-375">Proj 2</span></span></td>
<td><span data-ttu-id="7d6c0-376">2. projekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-376">Project 2</span></span></td>
<td><span data-ttu-id="7d6c0-377">1.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7d6c0-378">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-379">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-379">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-380">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7d6c0-380">Cost element</span></span></th>
<th><span data-ttu-id="7d6c0-381">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7d6c0-381">Cost behavior</span></span></th>
<th><span data-ttu-id="7d6c0-382">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="7d6c0-382">Units</span></span></th>
<th><span data-ttu-id="7d6c0-383">Likme</span><span class="sxs-lookup"><span data-stu-id="7d6c0-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-384">CC001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-384">CC001</span></span></td>
<td><span data-ttu-id="7d6c0-385">HR</span><span class="sxs-lookup"><span data-stu-id="7d6c0-385">HR</span></span></td>
<td><span data-ttu-id="7d6c0-386">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-386">10001</span></span></td>
<td><span data-ttu-id="7d6c0-387">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-387">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-388">1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-388">1</span></span></td>
<td><span data-ttu-id="7d6c0-389">10</span><span class="sxs-lookup"><span data-stu-id="7d6c0-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7d6c0-390">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-391">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-391">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-392">Lielums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-392">Magnitude</span></span></th>
<th><span data-ttu-id="7d6c0-393">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7d6c0-393">Cost element</span></span></th>
<th><span data-ttu-id="7d6c0-394">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7d6c0-394">Allocation factor</span></span></th>
<th><span data-ttu-id="7d6c0-395">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-396">Proj 1</span></span></td>
<td><span data-ttu-id="7d6c0-397">1. projekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-397">Project 1</span></span></td>
<td><span data-ttu-id="7d6c0-398">3.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-398">3</span></span></td>
<td><span data-ttu-id="7d6c0-399">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-399">10001</span></span></td>
<td><span data-ttu-id="7d6c0-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7d6c0-401">30,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-402">Proj 2</span></span></td>
<td><span data-ttu-id="7d6c0-403">2. projekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-403">Project 2</span></span></td>
<td><span data-ttu-id="7d6c0-404">1.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-404">1</span></span></td>
<td><span data-ttu-id="7d6c0-405">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-405">10001</span></span></td>
<td><span data-ttu-id="7d6c0-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7d6c0-407">10,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7d6c0-408">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7d6c0-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7d6c0-409">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7d6c0-409">Journal</span></span></th>
<th><span data-ttu-id="7d6c0-410">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="7d6c0-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7d6c0-411">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="7d6c0-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7d6c0-412">Versija</span><span class="sxs-lookup"><span data-stu-id="7d6c0-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-413">00003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-413">00003</span></span></td>
<td><span data-ttu-id="7d6c0-414">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="7d6c0-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="7d6c0-415">Finanšu</span><span class="sxs-lookup"><span data-stu-id="7d6c0-415">Fiscal</span></span></td>
<td><span data-ttu-id="7d6c0-416">2017</span><span class="sxs-lookup"><span data-stu-id="7d6c0-416">2017</span></span></td>
<td><span data-ttu-id="7d6c0-417">Periods 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-417">Period 1</span></span></td>
<td><span data-ttu-id="7d6c0-418">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="7d6c0-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="7d6c0-419">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7d6c0-420">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7d6c0-421">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-421">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-422">Lielums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-423">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-424">Proj 1</span></span></td>
<td><span data-ttu-id="7d6c0-425">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7d6c0-426">3,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-427">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-428">Proj 2</span></span></td>
<td><span data-ttu-id="7d6c0-429">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7d6c0-430">1,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7d6c0-431">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="7d6c0-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-432">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7d6c0-433">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7d6c0-433">Cost element</span></span></th>
<th><span data-ttu-id="7d6c0-434">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7d6c0-434">Cost behavior</span></span></th>
<th><span data-ttu-id="7d6c0-435">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-435">Amount</span></span></th>
<th><span data-ttu-id="7d6c0-436">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-437">CC0001</span></span></td>
<td><span data-ttu-id="7d6c0-438">HR</span><span class="sxs-lookup"><span data-stu-id="7d6c0-438">HR</span></span></td>
<td><span data-ttu-id="7d6c0-439">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-439">10001</span></span></td>
<td><span data-ttu-id="7d6c0-440">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-440">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-441">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-441">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-442">-30.00</span></span></td>
<td><span data-ttu-id="7d6c0-443">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-444">Proj 1</span></span></td>
<td><span data-ttu-id="7d6c0-445">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7d6c0-446">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-446">10001</span></span></td>
<td><span data-ttu-id="7d6c0-447">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-447">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-448">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-448">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-449">30,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-449">30.00</span></span></td>
<td><span data-ttu-id="7d6c0-450">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-451">CC001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-451">CC001</span></span></td>
<td><span data-ttu-id="7d6c0-452">HR</span><span class="sxs-lookup"><span data-stu-id="7d6c0-452">HR</span></span></td>
<td><span data-ttu-id="7d6c0-453">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-453">10001</span></span></td>
<td><span data-ttu-id="7d6c0-454">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-454">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-455">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-455">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-456">-10.00</span></span></td>
<td><span data-ttu-id="7d6c0-457">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-458">Proj 2</span></span></td>
<td><span data-ttu-id="7d6c0-459">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7d6c0-460">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-460">10001</span></span></td>
<td><span data-ttu-id="7d6c0-461">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-461">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-462">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-462">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-463">10,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-463">10.00</span></span></td>
<td><span data-ttu-id="7d6c0-464">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7d6c0-465">Sīkāku informāciju skatiet šeit: [Pieskaitāmo izmaksu aprēķina veikšana](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="7d6c0-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="7d6c0-466">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="7d6c0-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="7d6c0-467">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="7d6c0-468">Finance atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="7d6c0-469">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="7d6c0-470">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="7d6c0-471">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="7d6c0-472">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="7d6c0-473">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="7d6c0-474">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="7d6c0-475">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="7d6c0-475">Define the cost allocation</span></span>

<span data-ttu-id="7d6c0-476">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="7d6c0-477">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="7d6c0-478">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-479">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-479">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-480">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="7d6c0-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-481">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-481">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-482">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-482">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-483">35</span><span class="sxs-lookup"><span data-stu-id="7d6c0-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-484">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-484">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-485">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-485">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-486">55</span><span class="sxs-lookup"><span data-stu-id="7d6c0-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-487">CC004</span><span class="sxs-lookup"><span data-stu-id="7d6c0-487">CC004</span></span></td>
<td><span data-ttu-id="7d6c0-488">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7d6c0-488">Packaging</span></span></td>
<td><span data-ttu-id="7d6c0-489">10.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7d6c0-490">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="7d6c0-491">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-492">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-492">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-493">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="7d6c0-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-494">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-494">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-495">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-495">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-496">65</span><span class="sxs-lookup"><span data-stu-id="7d6c0-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-497">CC004</span><span class="sxs-lookup"><span data-stu-id="7d6c0-497">CC004</span></span></td>
<td><span data-ttu-id="7d6c0-498">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7d6c0-498">Packaging</span></span></td>
<td><span data-ttu-id="7d6c0-499">35</span><span class="sxs-lookup"><span data-stu-id="7d6c0-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7d6c0-500">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="7d6c0-501">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-502">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-502">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-503">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-504">Prod 1</span></span></td>
<td><span data-ttu-id="7d6c0-505">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-505">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-506">60</span><span class="sxs-lookup"><span data-stu-id="7d6c0-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-507">Prod 2</span></span></td>
<td><span data-ttu-id="7d6c0-508">2. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-508">Product 2</span></span></td>
<td><span data-ttu-id="7d6c0-509">20</span><span class="sxs-lookup"><span data-stu-id="7d6c0-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7d6c0-510">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="7d6c0-511">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-512">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-512">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-513">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-514">Prod 1</span></span></td>
<td><span data-ttu-id="7d6c0-515">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-515">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-516">80</span><span class="sxs-lookup"><span data-stu-id="7d6c0-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-517">Prod 2</span></span></td>
<td><span data-ttu-id="7d6c0-518">2. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-518">Product 2</span></span></td>
<td><span data-ttu-id="7d6c0-519">15</span><span class="sxs-lookup"><span data-stu-id="7d6c0-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7d6c0-520">Statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="7d6c0-521">Sīkāku informāciju skatiet šeit: [Statistikas mēru nodrošinātāja veidne](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="7d6c0-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="7d6c0-522">Nākamajā tabulā ir parādīts rezultāts, ja tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījuma pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-523">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-523">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-524">Lielums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-524">Magnitude</span></span></th>
<th><span data-ttu-id="7d6c0-525">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7d6c0-525">Allocation factor</span></span></th>
<th><span data-ttu-id="7d6c0-526">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-526">Amount</span></span></th>
<th><span data-ttu-id="7d6c0-527">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7d6c0-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-528">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-528">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-529">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-529">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-530">35</span><span class="sxs-lookup"><span data-stu-id="7d6c0-530">35</span></span></td>
<td><span data-ttu-id="7d6c0-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7d6c0-532">175.00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-532">175.00</span></span></td>
<td><span data-ttu-id="7d6c0-533">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-534">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-534">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-535">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-535">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-536">55</span><span class="sxs-lookup"><span data-stu-id="7d6c0-536">55</span></span></td>
<td><span data-ttu-id="7d6c0-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7d6c0-538">275.00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-538">275.00</span></span></td>
<td><span data-ttu-id="7d6c0-539">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-540">CC004</span><span class="sxs-lookup"><span data-stu-id="7d6c0-540">CC004</span></span></td>
<td><span data-ttu-id="7d6c0-541">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7d6c0-541">Packaging</span></span></td>
<td><span data-ttu-id="7d6c0-542">10.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-542">10</span></span></td>
<td><span data-ttu-id="7d6c0-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7d6c0-544">50,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-544">50.00</span></span></td>
<td><span data-ttu-id="7d6c0-545">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-546">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-546">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-547">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-547">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-548">35</span><span class="sxs-lookup"><span data-stu-id="7d6c0-548">35</span></span></td>
<td><span data-ttu-id="7d6c0-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="7d6c0-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7d6c0-550">436.00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-550">436.00</span></span></td>
<td><span data-ttu-id="7d6c0-551">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-552">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-552">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-553">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-553">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-554">55</span><span class="sxs-lookup"><span data-stu-id="7d6c0-554">55</span></span></td>
<td><span data-ttu-id="7d6c0-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="7d6c0-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7d6c0-556">685.14</span><span class="sxs-lookup"><span data-stu-id="7d6c0-556">685.14</span></span></td>
<td><span data-ttu-id="7d6c0-557">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-558">CC004</span><span class="sxs-lookup"><span data-stu-id="7d6c0-558">CC004</span></span></td>
<td><span data-ttu-id="7d6c0-559">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7d6c0-559">Packaging</span></span></td>
<td><span data-ttu-id="7d6c0-560">10.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-560">10</span></span></td>
<td><span data-ttu-id="7d6c0-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="7d6c0-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7d6c0-562">124.57</span><span class="sxs-lookup"><span data-stu-id="7d6c0-562">124.57</span></span></td>
<td><span data-ttu-id="7d6c0-563">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7d6c0-564">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-565">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-565">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-566">Lielums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-566">Magnitude</span></span></th>
<th><span data-ttu-id="7d6c0-567">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7d6c0-567">Allocation factor</span></span></th>
<th><span data-ttu-id="7d6c0-568">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-568">Amount</span></span></th>
<th><span data-ttu-id="7d6c0-569">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7d6c0-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-570">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-570">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-571">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-571">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-572">65</span><span class="sxs-lookup"><span data-stu-id="7d6c0-572">65</span></span></td>
<td><span data-ttu-id="7d6c0-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7d6c0-574">438.75</span><span class="sxs-lookup"><span data-stu-id="7d6c0-574">438.75</span></span></td>
<td><span data-ttu-id="7d6c0-575">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-576">CC004</span><span class="sxs-lookup"><span data-stu-id="7d6c0-576">CC004</span></span></td>
<td><span data-ttu-id="7d6c0-577">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7d6c0-577">Packaging</span></span></td>
<td><span data-ttu-id="7d6c0-578">35</span><span class="sxs-lookup"><span data-stu-id="7d6c0-578">35</span></span></td>
<td><span data-ttu-id="7d6c0-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7d6c0-580">236.25</span><span class="sxs-lookup"><span data-stu-id="7d6c0-580">236.25</span></span></td>
<td><span data-ttu-id="7d6c0-581">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-582">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-582">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-583">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-583">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-584">65</span><span class="sxs-lookup"><span data-stu-id="7d6c0-584">65</span></span></td>
<td><span data-ttu-id="7d6c0-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7d6c0-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7d6c0-586">5,297.69</span></span></td>
<td><span data-ttu-id="7d6c0-587">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-588">CC004</span><span class="sxs-lookup"><span data-stu-id="7d6c0-588">CC004</span></span></td>
<td><span data-ttu-id="7d6c0-589">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7d6c0-589">Packaging</span></span></td>
<td><span data-ttu-id="7d6c0-590">35</span><span class="sxs-lookup"><span data-stu-id="7d6c0-590">35</span></span></td>
<td><span data-ttu-id="7d6c0-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7d6c0-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7d6c0-592">2,852.60</span></span></td>
<td><span data-ttu-id="7d6c0-593">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7d6c0-594">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-595">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-595">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-596">Lielums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-596">Magnitude</span></span></th>
<th><span data-ttu-id="7d6c0-597">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7d6c0-597">Allocation factor</span></span></th>
<th><span data-ttu-id="7d6c0-598">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-598">Amount</span></span></th>
<th><span data-ttu-id="7d6c0-599">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7d6c0-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-600">Prod 1</span></span></td>
<td><span data-ttu-id="7d6c0-601">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-601">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-602">60</span><span class="sxs-lookup"><span data-stu-id="7d6c0-602">60</span></span></td>
<td><span data-ttu-id="7d6c0-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7d6c0-604">535.31</span><span class="sxs-lookup"><span data-stu-id="7d6c0-604">535.31</span></span></td>
<td><span data-ttu-id="7d6c0-605">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-606">Prod 2</span></span></td>
<td><span data-ttu-id="7d6c0-607">2. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-607">Product 2</span></span></td>
<td><span data-ttu-id="7d6c0-608">20.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-608">20</span></span></td>
<td><span data-ttu-id="7d6c0-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7d6c0-610">178.44</span><span class="sxs-lookup"><span data-stu-id="7d6c0-610">178.44</span></span></td>
<td><span data-ttu-id="7d6c0-611">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-612">Prod 1</span></span></td>
<td><span data-ttu-id="7d6c0-613">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-613">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-614">60</span><span class="sxs-lookup"><span data-stu-id="7d6c0-614">60</span></span></td>
<td><span data-ttu-id="7d6c0-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7d6c0-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7d6c0-616">4,487.12</span></span></td>
<td><span data-ttu-id="7d6c0-617">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-618">Prod 2</span></span></td>
<td><span data-ttu-id="7d6c0-619">2. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-619">Product 2</span></span></td>
<td><span data-ttu-id="7d6c0-620">20.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-620">20</span></span></td>
<td><span data-ttu-id="7d6c0-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7d6c0-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7d6c0-622">1,495.71</span></span></td>
<td><span data-ttu-id="7d6c0-623">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7d6c0-624">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-625">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-625">Cost object</span></span></th>
<th><span data-ttu-id="7d6c0-626">Lielums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-626">Magnitude</span></span></th>
<th><span data-ttu-id="7d6c0-627">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7d6c0-627">Allocation factor</span></span></th>
<th><span data-ttu-id="7d6c0-628">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-628">Amount</span></span></th>
<th><span data-ttu-id="7d6c0-629">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7d6c0-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-630">Prod 1</span></span></td>
<td><span data-ttu-id="7d6c0-631">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-631">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-632">80</span><span class="sxs-lookup"><span data-stu-id="7d6c0-632">80</span></span></td>
<td><span data-ttu-id="7d6c0-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7d6c0-634">241.05</span><span class="sxs-lookup"><span data-stu-id="7d6c0-634">241.05</span></span></td>
<td><span data-ttu-id="7d6c0-635">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-636">Prod 2</span></span></td>
<td><span data-ttu-id="7d6c0-637">2. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-637">Product 2</span></span></td>
<td><span data-ttu-id="7d6c0-638">15</span><span class="sxs-lookup"><span data-stu-id="7d6c0-638">15</span></span></td>
<td><span data-ttu-id="7d6c0-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7d6c0-640">45.20</span><span class="sxs-lookup"><span data-stu-id="7d6c0-640">45.20</span></span></td>
<td><span data-ttu-id="7d6c0-641">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-642">Prod 1</span></span></td>
<td><span data-ttu-id="7d6c0-643">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-643">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-644">80</span><span class="sxs-lookup"><span data-stu-id="7d6c0-644">80</span></span></td>
<td><span data-ttu-id="7d6c0-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7d6c0-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7d6c0-646">2,507.09</span></span></td>
<td><span data-ttu-id="7d6c0-647">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-648">Prod 2</span></span></td>
<td><span data-ttu-id="7d6c0-649">2. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-649">Product 2</span></span></td>
<td><span data-ttu-id="7d6c0-650">15</span><span class="sxs-lookup"><span data-stu-id="7d6c0-650">15</span></span></td>
<td><span data-ttu-id="7d6c0-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7d6c0-652">470.08</span><span class="sxs-lookup"><span data-stu-id="7d6c0-652">470.08</span></span></td>
<td><span data-ttu-id="7d6c0-653">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7d6c0-654">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="7d6c0-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7d6c0-655">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7d6c0-655">Journal</span></span></th>
<th><span data-ttu-id="7d6c0-656">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="7d6c0-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7d6c0-657">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="7d6c0-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7d6c0-658">Versija</span><span class="sxs-lookup"><span data-stu-id="7d6c0-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-659">00004</span><span class="sxs-lookup"><span data-stu-id="7d6c0-659">00004</span></span></td>
<td><span data-ttu-id="7d6c0-660">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="7d6c0-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="7d6c0-661">Finanšu</span><span class="sxs-lookup"><span data-stu-id="7d6c0-661">Fiscal</span></span></td>
<td><span data-ttu-id="7d6c0-662">2017</span><span class="sxs-lookup"><span data-stu-id="7d6c0-662">2017</span></span></td>
<td><span data-ttu-id="7d6c0-663">Periods 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-663">Period 1</span></span></td>
<td><span data-ttu-id="7d6c0-664">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="7d6c0-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="7d6c0-665">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7d6c0-666">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7d6c0-667">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7d6c0-668">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7d6c0-668">Cost element</span></span></th>
<th><span data-ttu-id="7d6c0-669">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7d6c0-669">Cost behavior</span></span></th>
<th><span data-ttu-id="7d6c0-670">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-671">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-672">CC001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-672">CC001</span></span></td>
<td><span data-ttu-id="7d6c0-673">HR</span><span class="sxs-lookup"><span data-stu-id="7d6c0-673">HR</span></span></td>
<td><span data-ttu-id="7d6c0-674">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-674">10001</span></span></td>
<td><span data-ttu-id="7d6c0-675">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-675">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-676">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-676">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-677">500,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-678">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-679">CC001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-679">CC001</span></span></td>
<td><span data-ttu-id="7d6c0-680">HR</span><span class="sxs-lookup"><span data-stu-id="7d6c0-680">HR</span></span></td>
<td><span data-ttu-id="7d6c0-681">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-681">10001</span></span></td>
<td><span data-ttu-id="7d6c0-682">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-682">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-683">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-683">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="7d6c0-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-685">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-686">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-686">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-687">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-687">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-688">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-688">10001</span></span></td>
<td><span data-ttu-id="7d6c0-689">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-689">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-690">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-690">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-691">675.00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-692">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-693">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-693">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-694">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-694">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-695">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-695">10001</span></span></td>
<td><span data-ttu-id="7d6c0-696">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-696">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-697">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-697">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="7d6c0-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-699">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-700">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-700">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-701">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-701">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-702">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-702">10001</span></span></td>
<td><span data-ttu-id="7d6c0-703">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-703">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-704">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-704">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-705">713.75</span><span class="sxs-lookup"><span data-stu-id="7d6c0-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-706">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-707">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-707">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-708">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-708">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-709">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-709">10001</span></span></td>
<td><span data-ttu-id="7d6c0-710">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-710">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-711">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-711">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="7d6c0-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-713">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-714">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-714">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-715">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7d6c0-715">Packaging</span></span></td>
<td><span data-ttu-id="7d6c0-716">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-716">10001</span></span></td>
<td><span data-ttu-id="7d6c0-717">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-717">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-718">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-718">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-719">286.25</span><span class="sxs-lookup"><span data-stu-id="7d6c0-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-720">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-721">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-721">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-722">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7d6c0-722">Packaging</span></span></td>
<td><span data-ttu-id="7d6c0-723">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-723">10001</span></span></td>
<td><span data-ttu-id="7d6c0-724">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-724">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-725">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-725">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="7d6c0-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-727">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-728">Prod 1</span></span></td>
<td><span data-ttu-id="7d6c0-729">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-729">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-730">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-730">10001</span></span></td>
<td><span data-ttu-id="7d6c0-731">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-731">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-732">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-732">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-733">776.36</span><span class="sxs-lookup"><span data-stu-id="7d6c0-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-734">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-735">Prod 1</span></span></td>
<td><span data-ttu-id="7d6c0-736">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-736">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-737">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-737">10001</span></span></td>
<td><span data-ttu-id="7d6c0-738">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-738">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-739">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-739">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7d6c0-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-741">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-742">Prod 2</span></span></td>
<td><span data-ttu-id="7d6c0-743">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-743">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-744">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-744">10001</span></span></td>
<td><span data-ttu-id="7d6c0-745">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-745">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-746">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-746">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-747">223.64</span><span class="sxs-lookup"><span data-stu-id="7d6c0-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-748">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="7d6c0-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-749">Prod 2</span></span></td>
<td><span data-ttu-id="7d6c0-750">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-750">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-751">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-751">10001</span></span></td>
<td><span data-ttu-id="7d6c0-752">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-752">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-753">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-753">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7d6c0-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7d6c0-755">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="7d6c0-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7d6c0-756">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7d6c0-757">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7d6c0-757">Cost element</span></span></th>
<th><span data-ttu-id="7d6c0-758">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7d6c0-758">Cost behavior</span></span></th>
<th><span data-ttu-id="7d6c0-759">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-759">Amount</span></span></th>
<th><span data-ttu-id="7d6c0-760">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d6c0-761">CC001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-761">CC001</span></span></td>
<td><span data-ttu-id="7d6c0-762">HR</span><span class="sxs-lookup"><span data-stu-id="7d6c0-762">HR</span></span></td>
<td><span data-ttu-id="7d6c0-763">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-763">10001</span></span></td>
<td><span data-ttu-id="7d6c0-764">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-764">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-765">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-765">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-766">-500.00</span></span></td>
<td><span data-ttu-id="7d6c0-767">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-768">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-768">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-769">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-769">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-770">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-770">10001</span></span></td>
<td><span data-ttu-id="7d6c0-771">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-771">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-772">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-772">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-773">175.00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-773">175.00</span></span></td>
<td><span data-ttu-id="7d6c0-774">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-775">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-775">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-776">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-776">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-777">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-777">10001</span></span></td>
<td><span data-ttu-id="7d6c0-778">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-778">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-779">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-779">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-780">275.00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-780">275.00</span></span></td>
<td><span data-ttu-id="7d6c0-781">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-782">CC004</span><span class="sxs-lookup"><span data-stu-id="7d6c0-782">CC004</span></span></td>
<td><span data-ttu-id="7d6c0-783">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7d6c0-783">Packaging</span></span></td>
<td><span data-ttu-id="7d6c0-784">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-784">10001</span></span></td>
<td><span data-ttu-id="7d6c0-785">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-785">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-786">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-786">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-787">50,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-787">50,00</span></span></td>
<td><span data-ttu-id="7d6c0-788">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-789">CC001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-789">CC001</span></span></td>
<td><span data-ttu-id="7d6c0-790">HR</span><span class="sxs-lookup"><span data-stu-id="7d6c0-790">HR</span></span></td>
<td><span data-ttu-id="7d6c0-791">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-791">10001</span></span></td>
<td><span data-ttu-id="7d6c0-792">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-792">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-793">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-793">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="7d6c0-794">-1,245.71</span></span></td>
<td><span data-ttu-id="7d6c0-795">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-796">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-796">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-797">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-797">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-798">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-798">10001</span></span></td>
<td><span data-ttu-id="7d6c0-799">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-799">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-800">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-800">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-801">436.00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-801">436.00</span></span></td>
<td><span data-ttu-id="7d6c0-802">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-803">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-803">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-804">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-804">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-805">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-805">10001</span></span></td>
<td><span data-ttu-id="7d6c0-806">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-806">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-807">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-807">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-808">685.14</span><span class="sxs-lookup"><span data-stu-id="7d6c0-808">685.14</span></span></td>
<td><span data-ttu-id="7d6c0-809">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-810">CC004</span><span class="sxs-lookup"><span data-stu-id="7d6c0-810">CC004</span></span></td>
<td><span data-ttu-id="7d6c0-811">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7d6c0-811">Packaging</span></span></td>
<td><span data-ttu-id="7d6c0-812">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-812">10001</span></span></td>
<td><span data-ttu-id="7d6c0-813">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-813">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-814">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-814">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-815">124.57</span><span class="sxs-lookup"><span data-stu-id="7d6c0-815">124.57</span></span></td>
<td><span data-ttu-id="7d6c0-816">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-817">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-817">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-818">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-818">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-819">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-819">10001</span></span></td>
<td><span data-ttu-id="7d6c0-820">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-820">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-821">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-821">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-822">-675.00</span></span></td>
<td><span data-ttu-id="7d6c0-823">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-824">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-824">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-825">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-825">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-826">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-826">10001</span></span></td>
<td><span data-ttu-id="7d6c0-827">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-827">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-828">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-828">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-829">438.75</span><span class="sxs-lookup"><span data-stu-id="7d6c0-829">438.75</span></span></td>
<td><span data-ttu-id="7d6c0-830">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-831">CC004</span><span class="sxs-lookup"><span data-stu-id="7d6c0-831">CC004</span></span></td>
<td><span data-ttu-id="7d6c0-832">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7d6c0-832">Packaging</span></span></td>
<td><span data-ttu-id="7d6c0-833">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-833">10001</span></span></td>
<td><span data-ttu-id="7d6c0-834">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-834">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-835">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-835">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-836">236.25</span><span class="sxs-lookup"><span data-stu-id="7d6c0-836">236.25</span></span></td>
<td><span data-ttu-id="7d6c0-837">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-838">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-838">CC002</span></span></td>
<td><span data-ttu-id="7d6c0-839">Finanses</span><span class="sxs-lookup"><span data-stu-id="7d6c0-839">Finance</span></span></td>
<td><span data-ttu-id="7d6c0-840">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-840">10001</span></span></td>
<td><span data-ttu-id="7d6c0-841">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-841">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-842">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-842">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="7d6c0-843">-8,150.29</span></span></td>
<td><span data-ttu-id="7d6c0-844">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-845">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-845">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-846">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-846">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-847">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-847">10001</span></span></td>
<td><span data-ttu-id="7d6c0-848">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-848">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-849">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-849">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7d6c0-850">5,297.69</span></span></td>
<td><span data-ttu-id="7d6c0-851">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-852">CC004</span><span class="sxs-lookup"><span data-stu-id="7d6c0-852">CC004</span></span></td>
<td><span data-ttu-id="7d6c0-853">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7d6c0-853">Packaging</span></span></td>
<td><span data-ttu-id="7d6c0-854">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-854">10001</span></span></td>
<td><span data-ttu-id="7d6c0-855">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-855">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-856">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-856">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7d6c0-857">2,852.60</span></span></td>
<td><span data-ttu-id="7d6c0-858">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-859">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-859">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-860">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-860">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-861">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-861">10001</span></span></td>
<td><span data-ttu-id="7d6c0-862">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-862">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-863">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-863">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="7d6c0-864">-713.75</span></span></td>
<td><span data-ttu-id="7d6c0-865">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-866">Prod 1</span></span></td>
<td><span data-ttu-id="7d6c0-867">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-867">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-868">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-868">10001</span></span></td>
<td><span data-ttu-id="7d6c0-869">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-869">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-870">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-870">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-871">535.31</span><span class="sxs-lookup"><span data-stu-id="7d6c0-871">535.31</span></span></td>
<td><span data-ttu-id="7d6c0-872">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-873">Prod 2</span></span></td>
<td><span data-ttu-id="7d6c0-874">2. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-874">Product 2</span></span></td>
<td><span data-ttu-id="7d6c0-875">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-875">10001</span></span></td>
<td><span data-ttu-id="7d6c0-876">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-876">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-877">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-877">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-878">178.44</span><span class="sxs-lookup"><span data-stu-id="7d6c0-878">178.44</span></span></td>
<td><span data-ttu-id="7d6c0-879">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-880">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-880">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-881">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-881">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-882">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-882">10001</span></span></td>
<td><span data-ttu-id="7d6c0-883">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-883">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-884">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-884">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="7d6c0-885">-5,982.83</span></span></td>
<td><span data-ttu-id="7d6c0-886">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-887">Prod 1</span></span></td>
<td><span data-ttu-id="7d6c0-888">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-888">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-889">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-889">10001</span></span></td>
<td><span data-ttu-id="7d6c0-890">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-890">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-891">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-891">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7d6c0-892">4,487.12</span></span></td>
<td><span data-ttu-id="7d6c0-893">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-894">Prod 2</span></span></td>
<td><span data-ttu-id="7d6c0-895">2. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-895">Product 2</span></span></td>
<td><span data-ttu-id="7d6c0-896">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-896">10001</span></span></td>
<td><span data-ttu-id="7d6c0-897">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-897">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-898">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-898">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7d6c0-899">1,495.71</span></span></td>
<td><span data-ttu-id="7d6c0-900">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-901">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-901">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-902">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-902">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-903">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-903">10001</span></span></td>
<td><span data-ttu-id="7d6c0-904">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-904">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-905">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-905">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="7d6c0-906">-286.25</span></span></td>
<td><span data-ttu-id="7d6c0-907">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-908">Prod 1</span></span></td>
<td><span data-ttu-id="7d6c0-909">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-909">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-910">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-910">10001</span></span></td>
<td><span data-ttu-id="7d6c0-911">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-911">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-912">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-912">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-913">241.05</span><span class="sxs-lookup"><span data-stu-id="7d6c0-913">241.05</span></span></td>
<td><span data-ttu-id="7d6c0-914">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-915">Prod 2</span></span></td>
<td><span data-ttu-id="7d6c0-916">2. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-916">Product 2</span></span></td>
<td><span data-ttu-id="7d6c0-917">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-917">10001</span></span></td>
<td><span data-ttu-id="7d6c0-918">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-918">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-919">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-919">Fixed cost</span></span></td>
<td><span data-ttu-id="7d6c0-920">45.20</span><span class="sxs-lookup"><span data-stu-id="7d6c0-920">45.20</span></span></td>
<td><span data-ttu-id="7d6c0-921">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-922">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-922">CC003</span></span></td>
<td><span data-ttu-id="7d6c0-923">Montāža</span><span class="sxs-lookup"><span data-stu-id="7d6c0-923">Assembly</span></span></td>
<td><span data-ttu-id="7d6c0-924">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-924">10001</span></span></td>
<td><span data-ttu-id="7d6c0-925">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-925">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-926">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-926">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="7d6c0-927">-2,977.17</span></span></td>
<td><span data-ttu-id="7d6c0-928">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-929">Prod 1</span></span></td>
<td><span data-ttu-id="7d6c0-930">1. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-930">Product 1</span></span></td>
<td><span data-ttu-id="7d6c0-931">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-931">10001</span></span></td>
<td><span data-ttu-id="7d6c0-932">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-932">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-933">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-933">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7d6c0-934">2,507.09</span></span></td>
<td><span data-ttu-id="7d6c0-935">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7d6c0-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-936">Prod 2</span></span></td>
<td><span data-ttu-id="7d6c0-937">2. prece</span><span class="sxs-lookup"><span data-stu-id="7d6c0-937">Product 2</span></span></td>
<td><span data-ttu-id="7d6c0-938">10001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-938">10001</span></span></td>
<td><span data-ttu-id="7d6c0-939">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-939">Electricity</span></span></td>
<td><span data-ttu-id="7d6c0-940">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-940">Variable cost</span></span></td>
<td><span data-ttu-id="7d6c0-941">470.08</span><span class="sxs-lookup"><span data-stu-id="7d6c0-941">470.08</span></span></td>
<td><span data-ttu-id="7d6c0-942">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7d6c0-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="7d6c0-943">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="7d6c0-943">Conclusion</span></span>
<span data-ttu-id="7d6c0-944">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="7d6c0-945">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="7d6c0-946">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="7d6c0-947">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="7d6c0-948">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7d6c0-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="7d6c0-949">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="7d6c0-950">Summa</span><span class="sxs-lookup"><span data-stu-id="7d6c0-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7d6c0-951">CC099</span><span class="sxs-lookup"><span data-stu-id="7d6c0-951">CC099</span></span></th>
<th><span data-ttu-id="7d6c0-952">CC001</span><span class="sxs-lookup"><span data-stu-id="7d6c0-952">CC001</span></span></th>
<th><span data-ttu-id="7d6c0-953">CC002</span><span class="sxs-lookup"><span data-stu-id="7d6c0-953">CC002</span></span></th>
<th><span data-ttu-id="7d6c0-954">CC003</span><span class="sxs-lookup"><span data-stu-id="7d6c0-954">CC003</span></span></th>
<th><span data-ttu-id="7d6c0-955">CC004</span><span class="sxs-lookup"><span data-stu-id="7d6c0-955">CC004</span></span></th>
<th><span data-ttu-id="7d6c0-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-956">Proj 1</span></span></th>
<th><span data-ttu-id="7d6c0-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-957">Proj 2</span></span></th>
<th><span data-ttu-id="7d6c0-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7d6c0-958">Prod 1</span></span></th>
<th><span data-ttu-id="7d6c0-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7d6c0-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="7d6c0-960">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="7d6c0-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="7d6c0-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="7d6c0-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="7d6c0-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="7d6c0-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="7d6c0-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="7d6c0-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="7d6c0-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="7d6c0-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="7d6c0-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="7d6c0-970">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="7d6c0-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-971">0,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="7d6c0-972">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-973">0,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-974">0,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-975">0,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-976">0,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-977">0,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-978">776.36</span><span class="sxs-lookup"><span data-stu-id="7d6c0-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-979">223.64</span><span class="sxs-lookup"><span data-stu-id="7d6c0-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="7d6c0-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="7d6c0-981">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7d6c0-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-982">000</span><span class="sxs-lookup"><span data-stu-id="7d6c0-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-983">0,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-984">0,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-985">0,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-986">0,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-987">30,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-988">10,00</span><span class="sxs-lookup"><span data-stu-id="7d6c0-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7d6c0-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7d6c0-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7d6c0-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="7d6c0-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7d6c0-992">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="7d6c0-993">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="7d6c0-994">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="7d6c0-995">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="7d6c0-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="7d6c0-996">Plašāku informāciju skatiet [Izmaksu apkopojuma politika un pieskaitāmo izmaksu aprēķins](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="7d6c0-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



