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
ms.openlocfilehash: 6c045f82f3288dba193721dd80c90e68750af9a7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178858"
---
# <a name="overhead-calculation"></a><span data-ttu-id="7869a-103">Pieskaitāmo izmaksu aprēķins</span><span class="sxs-lookup"><span data-stu-id="7869a-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7869a-104">Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="7869a-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="7869a-105">Termina definīcija</span><span class="sxs-lookup"><span data-stu-id="7869a-105">Term definition</span></span>
---------------

<span data-ttu-id="7869a-106">Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="7869a-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="7869a-107">Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="7869a-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="7869a-108">Šeit norādītas dažas pieskaitāmās izmaksas:</span><span class="sxs-lookup"><span data-stu-id="7869a-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="7869a-109">Īre</span><span class="sxs-lookup"><span data-stu-id="7869a-109">Rent</span></span>
-   <span data-ttu-id="7869a-110">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-110">Electricity</span></span>
-   <span data-ttu-id="7869a-111">Administratīvās algas</span><span class="sxs-lookup"><span data-stu-id="7869a-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="7869a-112">Pieskaitāmo izmaksu aprēķina apskats</span><span class="sxs-lookup"><span data-stu-id="7869a-112">Overhead calculation overview</span></span>
<span data-ttu-id="7869a-113">Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā.</span><span class="sxs-lookup"><span data-stu-id="7869a-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="7869a-114">Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="7869a-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="7869a-115">Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās.</span><span class="sxs-lookup"><span data-stu-id="7869a-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="7869a-116">Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="7869a-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="7869a-117">Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="7869a-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="7869a-118">Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="7869a-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="7869a-119">Versijas tips</span><span class="sxs-lookup"><span data-stu-id="7869a-119">Version type</span></span>
-   <span data-ttu-id="7869a-120">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="7869a-120">Date and time</span></span>
-   <span data-ttu-id="7869a-121">Izmaksu uzskaites virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="7869a-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="7869a-122">Finanšu gads</span><span class="sxs-lookup"><span data-stu-id="7869a-122">Fiscal year</span></span>
-   <span data-ttu-id="7869a-123">Fiskālais periods</span><span class="sxs-lookup"><span data-stu-id="7869a-123">Fiscal period</span></span>

<span data-ttu-id="7869a-124">Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas.</span><span class="sxs-lookup"><span data-stu-id="7869a-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="7869a-125">Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="7869a-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="7869a-126">Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="7869a-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="7869a-127">Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="7869a-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="7869a-128">Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli.</span><span class="sxs-lookup"><span data-stu-id="7869a-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="7869a-129">Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade.</span><span class="sxs-lookup"><span data-stu-id="7869a-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="7869a-130">Tādēļ jums vienmēr ir pilnīga izsekojamība.</span><span class="sxs-lookup"><span data-stu-id="7869a-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="7869a-131">[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="7869a-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="7869a-132">Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="7869a-133">Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="7869a-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="7869a-134">Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati.</span><span class="sxs-lookup"><span data-stu-id="7869a-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="7869a-135">Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām.</span><span class="sxs-lookup"><span data-stu-id="7869a-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="7869a-136">Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam.</span><span class="sxs-lookup"><span data-stu-id="7869a-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="7869a-137">Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="7869a-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7869a-138">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7869a-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7869a-139">Izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7869a-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="7869a-140">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="7869a-140">Main account</span></span></th>
<th><span data-ttu-id="7869a-141">Summa uzskaites valūtā</span><span class="sxs-lookup"><span data-stu-id="7869a-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-142">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="7869a-143">CC099</span><span class="sxs-lookup"><span data-stu-id="7869a-143">CC099</span></span></td>
<td><span data-ttu-id="7869a-144">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7869a-144">Default cost center</span></span></td>
<td><span data-ttu-id="7869a-145">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-145">10001</span></span></td>
<td><span data-ttu-id="7869a-146">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-146">Electricity</span></span></td>
<td><span data-ttu-id="7869a-147">10 000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="7869a-148">1. solis. Apstrādāt izmaksu uzvedību aprēķinu</span><span class="sxs-lookup"><span data-stu-id="7869a-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="7869a-149">Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**.</span><span class="sxs-lookup"><span data-stu-id="7869a-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="7869a-150">Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="7869a-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="7869a-151">Definēt izmaksu uzvedības kārtulu</span><span class="sxs-lookup"><span data-stu-id="7869a-151">Define the cost behavior rule</span></span>

<span data-ttu-id="7869a-152">Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu.</span><span class="sxs-lookup"><span data-stu-id="7869a-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="7869a-153">Elektrības rēķini bieži atbilst šai definīcijai.</span><span class="sxs-lookup"><span data-stu-id="7869a-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="7869a-154">Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam.</span><span class="sxs-lookup"><span data-stu-id="7869a-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="7869a-155">Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="7869a-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="7869a-156">Fiksētā summa 1000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="7869a-157">0 &lt;= 1000,00 = Fiksēts</span><span class="sxs-lookup"><span data-stu-id="7869a-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="7869a-158">1000,01 &lt; N = Mainīgs</span><span class="sxs-lookup"><span data-stu-id="7869a-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="7869a-159">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7869a-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7869a-160">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7869a-160">Journal</span></span></th>
<th><span data-ttu-id="7869a-161">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="7869a-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7869a-162">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="7869a-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7869a-163">Versija</span><span class="sxs-lookup"><span data-stu-id="7869a-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-164">00001</span><span class="sxs-lookup"><span data-stu-id="7869a-164">00001</span></span></td>
<td><span data-ttu-id="7869a-165">Izmaksu izturēšanās aprēķināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="7869a-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="7869a-166">Finanšu</span><span class="sxs-lookup"><span data-stu-id="7869a-166">Fiscal</span></span></td>
<td><span data-ttu-id="7869a-167">2017</span><span class="sxs-lookup"><span data-stu-id="7869a-167">2017</span></span></td>
<td><span data-ttu-id="7869a-168">Periods 1</span><span class="sxs-lookup"><span data-stu-id="7869a-168">Period 1</span></span></td>
<td><span data-ttu-id="7869a-169">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="7869a-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7869a-170">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="7869a-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7869a-171">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7869a-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7869a-172">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7869a-173">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7869a-173">Cost element</span></span></th>
<th><span data-ttu-id="7869a-174">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7869a-174">Cost behavior</span></span></th>
<th><span data-ttu-id="7869a-175">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-176">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="7869a-177">CC099</span><span class="sxs-lookup"><span data-stu-id="7869a-177">CC099</span></span></td>
<td><span data-ttu-id="7869a-178">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7869a-178">Default cost center</span></span></td>
<td><span data-ttu-id="7869a-179">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-179">10001</span></span></td>
<td><span data-ttu-id="7869a-180">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-180">Electricity</span></span></td>
<td><span data-ttu-id="7869a-181">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="7869a-181">Unclassified</span></span></td>
<td><span data-ttu-id="7869a-182">10 000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7869a-183">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="7869a-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-184">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7869a-185">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7869a-185">Cost element</span></span></th>
<th><span data-ttu-id="7869a-186">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7869a-186">Cost behavior</span></span></th>
<th><span data-ttu-id="7869a-187">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-187">Amount</span></span></th>
<th><span data-ttu-id="7869a-188">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7869a-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-189">CC099</span><span class="sxs-lookup"><span data-stu-id="7869a-189">CC099</span></span></td>
<td><span data-ttu-id="7869a-190">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7869a-190">Default cost center</span></span></td>
<td><span data-ttu-id="7869a-191">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-191">10001</span></span></td>
<td><span data-ttu-id="7869a-192">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-192">Electricity</span></span></td>
<td><span data-ttu-id="7869a-193">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="7869a-193">Unclassified</span></span></td>
<td><span data-ttu-id="7869a-194">10 000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-194">10,000.00</span></span></td>
<td><span data-ttu-id="7869a-195">2017. gada 3. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-196">CC099</span><span class="sxs-lookup"><span data-stu-id="7869a-196">CC099</span></span></td>
<td><span data-ttu-id="7869a-197">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7869a-197">Default cost center</span></span></td>
<td><span data-ttu-id="7869a-198">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-198">10001</span></span></td>
<td><span data-ttu-id="7869a-199">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-199">Electricity</span></span></td>
<td><span data-ttu-id="7869a-200">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="7869a-200">Unclassified</span></span></td>
<td><span data-ttu-id="7869a-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-201">-10,000.00</span></span></td>
<td><span data-ttu-id="7869a-202">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-203">CC099</span><span class="sxs-lookup"><span data-stu-id="7869a-203">CC099</span></span></td>
<td><span data-ttu-id="7869a-204">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7869a-204">Default cost center</span></span></td>
<td><span data-ttu-id="7869a-205">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-205">10001</span></span></td>
<td><span data-ttu-id="7869a-206">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-206">Electricity</span></span></td>
<td><span data-ttu-id="7869a-207">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-207">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-208">1,000.00</span></span></td>
<td><span data-ttu-id="7869a-209">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-210">CC099</span><span class="sxs-lookup"><span data-stu-id="7869a-210">CC099</span></span></td>
<td><span data-ttu-id="7869a-211">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7869a-211">Default cost center</span></span></td>
<td><span data-ttu-id="7869a-212">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-212">10001</span></span></td>
<td><span data-ttu-id="7869a-213">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-213">Electricity</span></span></td>
<td><span data-ttu-id="7869a-214">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-214">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7869a-215">9,000.00</span></span></td>
<td><span data-ttu-id="7869a-216">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7869a-217">Sīkāku informāciju skatiet šeit: [Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="7869a-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="7869a-218">2. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="7869a-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="7869a-219">Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="7869a-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="7869a-220">Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.</span><span class="sxs-lookup"><span data-stu-id="7869a-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="7869a-221">Definēt izmaksu izplatīšanas kārtulu</span><span class="sxs-lookup"><span data-stu-id="7869a-221">Define the cost distribution rule</span></span>

<span data-ttu-id="7869a-222">Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa.</span><span class="sxs-lookup"><span data-stu-id="7869a-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="7869a-223">Izmaksu uzskaitē šī metode nav pietiekami detalizēta.</span><span class="sxs-lookup"><span data-stu-id="7869a-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="7869a-224">Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="7869a-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="7869a-225">Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh).</span><span class="sxs-lookup"><span data-stu-id="7869a-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="7869a-226">Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="7869a-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="7869a-227">Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.</span><span class="sxs-lookup"><span data-stu-id="7869a-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-228">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-228">Cost object</span></span></th>
<th><span data-ttu-id="7869a-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="7869a-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-230">CC001</span><span class="sxs-lookup"><span data-stu-id="7869a-230">CC001</span></span></td>
<td><span data-ttu-id="7869a-231">HR</span><span class="sxs-lookup"><span data-stu-id="7869a-231">HR</span></span></td>
<td><span data-ttu-id="7869a-232">1000</span><span class="sxs-lookup"><span data-stu-id="7869a-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-233">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-233">CC002</span></span></td>
<td><span data-ttu-id="7869a-234">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-234">Finance</span></span></td>
<td><span data-ttu-id="7869a-235">6,000</span><span class="sxs-lookup"><span data-stu-id="7869a-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-236">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-236">CC003</span></span></td>
<td><span data-ttu-id="7869a-237">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-237">Assembly</span></span></td>
<td><span data-ttu-id="7869a-238">0</span><span class="sxs-lookup"><span data-stu-id="7869a-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7869a-239">Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="7869a-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-240">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-240">Cost object</span></span></th>
<th><span data-ttu-id="7869a-241">Lielums</span><span class="sxs-lookup"><span data-stu-id="7869a-241">Magnitude</span></span></th>
<th><span data-ttu-id="7869a-242">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7869a-242">Allocation factor</span></span></th>
<th><span data-ttu-id="7869a-243">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-244">CC001</span><span class="sxs-lookup"><span data-stu-id="7869a-244">CC001</span></span></td>
<td><span data-ttu-id="7869a-245">HR</span><span class="sxs-lookup"><span data-stu-id="7869a-245">HR</span></span></td>
<td><span data-ttu-id="7869a-246">1000</span><span class="sxs-lookup"><span data-stu-id="7869a-246">1,000</span></span></td>
<td><span data-ttu-id="7869a-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7869a-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7869a-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-249">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-249">CC002</span></span></td>
<td><span data-ttu-id="7869a-250">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-250">Finance</span></span></td>
<td><span data-ttu-id="7869a-251">6,000</span><span class="sxs-lookup"><span data-stu-id="7869a-251">6,000</span></span></td>
<td><span data-ttu-id="7869a-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7869a-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7869a-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-254">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-254">CC003</span></span></td>
<td><span data-ttu-id="7869a-255">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-255">Assembly</span></span></td>
<td><span data-ttu-id="7869a-256">0</span><span class="sxs-lookup"><span data-stu-id="7869a-256">0</span></span></td>
<td><span data-ttu-id="7869a-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7869a-258">0,00</span><span class="sxs-lookup"><span data-stu-id="7869a-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7869a-259">Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību.</span><span class="sxs-lookup"><span data-stu-id="7869a-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="7869a-260">Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.</span><span class="sxs-lookup"><span data-stu-id="7869a-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-261">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-261">Cost object</span></span></th>
<th><span data-ttu-id="7869a-262">Formula</span><span class="sxs-lookup"><span data-stu-id="7869a-262">Formula</span></span></th>
<th><span data-ttu-id="7869a-263">Lielums</span><span class="sxs-lookup"><span data-stu-id="7869a-263">Magnitude</span></span></th>
<th><span data-ttu-id="7869a-264">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7869a-264">Allocation factor</span></span></th>
<th><span data-ttu-id="7869a-265">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-266">CC001</span><span class="sxs-lookup"><span data-stu-id="7869a-266">CC001</span></span></td>
<td><span data-ttu-id="7869a-267">HR</span><span class="sxs-lookup"><span data-stu-id="7869a-267">HR</span></span></td>
<td><span data-ttu-id="7869a-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7869a-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7869a-269">1.</span><span class="sxs-lookup"><span data-stu-id="7869a-269">1</span></span></td>
<td><span data-ttu-id="7869a-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7869a-271">500,00</span><span class="sxs-lookup"><span data-stu-id="7869a-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-272">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-272">CC002</span></span></td>
<td><span data-ttu-id="7869a-273">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-273">Finance</span></span></td>
<td><span data-ttu-id="7869a-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7869a-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7869a-275">1.</span><span class="sxs-lookup"><span data-stu-id="7869a-275">1</span></span></td>
<td><span data-ttu-id="7869a-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7869a-277">500,00</span><span class="sxs-lookup"><span data-stu-id="7869a-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-278">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-278">CC003</span></span></td>
<td><span data-ttu-id="7869a-279">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-279">Assembly</span></span></td>
<td><span data-ttu-id="7869a-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7869a-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7869a-281">0</span><span class="sxs-lookup"><span data-stu-id="7869a-281">0</span></span></td>
<td><span data-ttu-id="7869a-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7869a-283">0,00</span><span class="sxs-lookup"><span data-stu-id="7869a-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7869a-284">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7869a-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7869a-285">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7869a-285">Journal</span></span></th>
<th><span data-ttu-id="7869a-286">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="7869a-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7869a-287">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="7869a-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7869a-288">Versija</span><span class="sxs-lookup"><span data-stu-id="7869a-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-289">00002</span><span class="sxs-lookup"><span data-stu-id="7869a-289">00002</span></span></td>
<td><span data-ttu-id="7869a-290">Izmaksu sadales aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="7869a-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="7869a-291">Finanšu</span><span class="sxs-lookup"><span data-stu-id="7869a-291">Fiscal</span></span></td>
<td><span data-ttu-id="7869a-292">2017</span><span class="sxs-lookup"><span data-stu-id="7869a-292">2017</span></span></td>
<td><span data-ttu-id="7869a-293">Periods 1</span><span class="sxs-lookup"><span data-stu-id="7869a-293">Period 1</span></span></td>
<td><span data-ttu-id="7869a-294">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="7869a-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7869a-295">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="7869a-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7869a-296">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7869a-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7869a-297">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7869a-298">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7869a-298">Cost element</span></span></th>
<th><span data-ttu-id="7869a-299">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7869a-299">Cost behavior</span></span></th>
<th><span data-ttu-id="7869a-300">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-301">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-302">CC099</span><span class="sxs-lookup"><span data-stu-id="7869a-302">CC099</span></span></td>
<td><span data-ttu-id="7869a-303">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7869a-303">Default cost center</span></span></td>
<td><span data-ttu-id="7869a-304">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-304">10001</span></span></td>
<td><span data-ttu-id="7869a-305">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-305">Electricity</span></span></td>
<td><span data-ttu-id="7869a-306">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-306">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-308">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-309">CC099</span><span class="sxs-lookup"><span data-stu-id="7869a-309">CC099</span></span></td>
<td><span data-ttu-id="7869a-310">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7869a-310">Default cost center</span></span></td>
<td><span data-ttu-id="7869a-311">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-311">10001</span></span></td>
<td><span data-ttu-id="7869a-312">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-312">Electricity</span></span></td>
<td><span data-ttu-id="7869a-313">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-313">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7869a-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7869a-315">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="7869a-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-316">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7869a-317">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7869a-317">Cost element</span></span></th>
<th><span data-ttu-id="7869a-318">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7869a-318">Cost behavior</span></span></th>
<th><span data-ttu-id="7869a-319">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-319">Amount</span></span></th>
<th><span data-ttu-id="7869a-320">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7869a-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-321">CC099</span><span class="sxs-lookup"><span data-stu-id="7869a-321">CC099</span></span></td>
<td><span data-ttu-id="7869a-322">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7869a-322">Default cost center</span></span></td>
<td><span data-ttu-id="7869a-323">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-323">10001</span></span></td>
<td><span data-ttu-id="7869a-324">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-324">Electricity</span></span></td>
<td><span data-ttu-id="7869a-325">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-325">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-326">-1000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-326">-1,000.00</span></span></td>
<td><span data-ttu-id="7869a-327">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-328">CC001</span><span class="sxs-lookup"><span data-stu-id="7869a-328">CC001</span></span></td>
<td><span data-ttu-id="7869a-329">HR</span><span class="sxs-lookup"><span data-stu-id="7869a-329">HR</span></span></td>
<td><span data-ttu-id="7869a-330">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-330">10001</span></span></td>
<td><span data-ttu-id="7869a-331">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-331">Electricity</span></span></td>
<td><span data-ttu-id="7869a-332">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-332">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-333">500,00</span><span class="sxs-lookup"><span data-stu-id="7869a-333">500.00</span></span></td>
<td><span data-ttu-id="7869a-334">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-335">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-335">CC002</span></span></td>
<td><span data-ttu-id="7869a-336">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-336">Finance</span></span></td>
<td><span data-ttu-id="7869a-337">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-337">10001</span></span></td>
<td><span data-ttu-id="7869a-338">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-338">Electricity</span></span></td>
<td><span data-ttu-id="7869a-339">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-339">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-340">500,00</span><span class="sxs-lookup"><span data-stu-id="7869a-340">500.00</span></span></td>
<td><span data-ttu-id="7869a-341">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-342">CC099</span><span class="sxs-lookup"><span data-stu-id="7869a-342">CC099</span></span></td>
<td><span data-ttu-id="7869a-343">Noklusējuma izmaksu centrs</span><span class="sxs-lookup"><span data-stu-id="7869a-343">Default cost center</span></span></td>
<td><span data-ttu-id="7869a-344">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-344">10001</span></span></td>
<td><span data-ttu-id="7869a-345">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-345">Electricity</span></span></td>
<td><span data-ttu-id="7869a-346">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-346">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="7869a-347">-9,000.00</span></span></td>
<td><span data-ttu-id="7869a-348">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-349">CC001</span><span class="sxs-lookup"><span data-stu-id="7869a-349">CC001</span></span></td>
<td><span data-ttu-id="7869a-350">HR</span><span class="sxs-lookup"><span data-stu-id="7869a-350">HR</span></span></td>
<td><span data-ttu-id="7869a-351">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-351">10001</span></span></td>
<td><span data-ttu-id="7869a-352">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-352">Electricity</span></span></td>
<td><span data-ttu-id="7869a-353">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-353">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7869a-354">1,285.71</span></span></td>
<td><span data-ttu-id="7869a-355">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-356">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-356">CC002</span></span></td>
<td><span data-ttu-id="7869a-357">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-357">Finance</span></span></td>
<td><span data-ttu-id="7869a-358">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-358">10001</span></span></td>
<td><span data-ttu-id="7869a-359">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-359">Electricity</span></span></td>
<td><span data-ttu-id="7869a-360">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-360">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7869a-361">7,714.29</span></span></td>
<td><span data-ttu-id="7869a-362">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7869a-363">Sīkāku informāciju skatiet šeit: [Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="7869a-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="7869a-364">3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu</span><span class="sxs-lookup"><span data-stu-id="7869a-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="7869a-365">Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="7869a-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="7869a-366">Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="7869a-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="7869a-367">Definēt pieskaitāmo izmaksu likmi</span><span class="sxs-lookup"><span data-stu-id="7869a-367">Define the overhead rate</span></span>

<span data-ttu-id="7869a-368">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos.</span><span class="sxs-lookup"><span data-stu-id="7869a-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="7869a-369">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.</span><span class="sxs-lookup"><span data-stu-id="7869a-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-370">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-370">Cost object</span></span></th>
<th><span data-ttu-id="7869a-371">Stundas</span><span class="sxs-lookup"><span data-stu-id="7869a-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7869a-372">Proj 1</span></span></td>
<td><span data-ttu-id="7869a-373">1. projekts</span><span class="sxs-lookup"><span data-stu-id="7869a-373">Project 1</span></span></td>
<td><span data-ttu-id="7869a-374">3.</span><span class="sxs-lookup"><span data-stu-id="7869a-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7869a-375">Proj 2</span></span></td>
<td><span data-ttu-id="7869a-376">2. projekts</span><span class="sxs-lookup"><span data-stu-id="7869a-376">Project 2</span></span></td>
<td><span data-ttu-id="7869a-377">1.</span><span class="sxs-lookup"><span data-stu-id="7869a-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7869a-378">Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="7869a-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-379">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-379">Cost object</span></span></th>
<th><span data-ttu-id="7869a-380">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7869a-380">Cost element</span></span></th>
<th><span data-ttu-id="7869a-381">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7869a-381">Cost behavior</span></span></th>
<th><span data-ttu-id="7869a-382">Mērvienības</span><span class="sxs-lookup"><span data-stu-id="7869a-382">Units</span></span></th>
<th><span data-ttu-id="7869a-383">Likme</span><span class="sxs-lookup"><span data-stu-id="7869a-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-384">CC001</span><span class="sxs-lookup"><span data-stu-id="7869a-384">CC001</span></span></td>
<td><span data-ttu-id="7869a-385">HR</span><span class="sxs-lookup"><span data-stu-id="7869a-385">HR</span></span></td>
<td><span data-ttu-id="7869a-386">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-386">10001</span></span></td>
<td><span data-ttu-id="7869a-387">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-387">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-388">1</span><span class="sxs-lookup"><span data-stu-id="7869a-388">1</span></span></td>
<td><span data-ttu-id="7869a-389">10</span><span class="sxs-lookup"><span data-stu-id="7869a-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7869a-390">Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.</span><span class="sxs-lookup"><span data-stu-id="7869a-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-391">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-391">Cost object</span></span></th>
<th><span data-ttu-id="7869a-392">Lielums</span><span class="sxs-lookup"><span data-stu-id="7869a-392">Magnitude</span></span></th>
<th><span data-ttu-id="7869a-393">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7869a-393">Cost element</span></span></th>
<th><span data-ttu-id="7869a-394">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7869a-394">Allocation factor</span></span></th>
<th><span data-ttu-id="7869a-395">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7869a-396">Proj 1</span></span></td>
<td><span data-ttu-id="7869a-397">1. projekts</span><span class="sxs-lookup"><span data-stu-id="7869a-397">Project 1</span></span></td>
<td><span data-ttu-id="7869a-398">3.</span><span class="sxs-lookup"><span data-stu-id="7869a-398">3</span></span></td>
<td><span data-ttu-id="7869a-399">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-399">10001</span></span></td>
<td><span data-ttu-id="7869a-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7869a-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7869a-401">30,00</span><span class="sxs-lookup"><span data-stu-id="7869a-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7869a-402">Proj 2</span></span></td>
<td><span data-ttu-id="7869a-403">2. projekts</span><span class="sxs-lookup"><span data-stu-id="7869a-403">Project 2</span></span></td>
<td><span data-ttu-id="7869a-404">1.</span><span class="sxs-lookup"><span data-stu-id="7869a-404">1</span></span></td>
<td><span data-ttu-id="7869a-405">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-405">10001</span></span></td>
<td><span data-ttu-id="7869a-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7869a-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7869a-407">10,00</span><span class="sxs-lookup"><span data-stu-id="7869a-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7869a-408">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7869a-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7869a-409">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7869a-409">Journal</span></span></th>
<th><span data-ttu-id="7869a-410">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="7869a-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7869a-411">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="7869a-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7869a-412">Versija</span><span class="sxs-lookup"><span data-stu-id="7869a-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-413">00003</span><span class="sxs-lookup"><span data-stu-id="7869a-413">00003</span></span></td>
<td><span data-ttu-id="7869a-414">Pieskaitāmo izmaksu likmes aprēķina žurnāls</span><span class="sxs-lookup"><span data-stu-id="7869a-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="7869a-415">Finanšu</span><span class="sxs-lookup"><span data-stu-id="7869a-415">Fiscal</span></span></td>
<td><span data-ttu-id="7869a-416">2017</span><span class="sxs-lookup"><span data-stu-id="7869a-416">2017</span></span></td>
<td><span data-ttu-id="7869a-417">Periods 1</span><span class="sxs-lookup"><span data-stu-id="7869a-417">Period 1</span></span></td>
<td><span data-ttu-id="7869a-418">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="7869a-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="7869a-419">Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)</span><span class="sxs-lookup"><span data-stu-id="7869a-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7869a-420">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7869a-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7869a-421">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-421">Cost object</span></span></th>
<th><span data-ttu-id="7869a-422">Lielums</span><span class="sxs-lookup"><span data-stu-id="7869a-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-423">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7869a-424">Proj 1</span></span></td>
<td><span data-ttu-id="7869a-425">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="7869a-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7869a-426">3,00</span><span class="sxs-lookup"><span data-stu-id="7869a-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-427">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7869a-428">Proj 2</span></span></td>
<td><span data-ttu-id="7869a-429">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="7869a-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7869a-430">1,00</span><span class="sxs-lookup"><span data-stu-id="7869a-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7869a-431">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="7869a-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-432">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7869a-433">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7869a-433">Cost element</span></span></th>
<th><span data-ttu-id="7869a-434">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7869a-434">Cost behavior</span></span></th>
<th><span data-ttu-id="7869a-435">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-435">Amount</span></span></th>
<th><span data-ttu-id="7869a-436">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7869a-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="7869a-437">CC0001</span></span></td>
<td><span data-ttu-id="7869a-438">HR</span><span class="sxs-lookup"><span data-stu-id="7869a-438">HR</span></span></td>
<td><span data-ttu-id="7869a-439">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-439">10001</span></span></td>
<td><span data-ttu-id="7869a-440">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-440">Electricity</span></span></td>
<td><span data-ttu-id="7869a-441">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-441">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="7869a-442">-30.00</span></span></td>
<td><span data-ttu-id="7869a-443">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7869a-444">Proj 1</span></span></td>
<td><span data-ttu-id="7869a-445">Iekšējais 1. projekts</span><span class="sxs-lookup"><span data-stu-id="7869a-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7869a-446">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-446">10001</span></span></td>
<td><span data-ttu-id="7869a-447">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-447">Electricity</span></span></td>
<td><span data-ttu-id="7869a-448">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-448">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-449">30,00</span><span class="sxs-lookup"><span data-stu-id="7869a-449">30.00</span></span></td>
<td><span data-ttu-id="7869a-450">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-451">CC001</span><span class="sxs-lookup"><span data-stu-id="7869a-451">CC001</span></span></td>
<td><span data-ttu-id="7869a-452">HR</span><span class="sxs-lookup"><span data-stu-id="7869a-452">HR</span></span></td>
<td><span data-ttu-id="7869a-453">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-453">10001</span></span></td>
<td><span data-ttu-id="7869a-454">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-454">Electricity</span></span></td>
<td><span data-ttu-id="7869a-455">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-455">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="7869a-456">-10.00</span></span></td>
<td><span data-ttu-id="7869a-457">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7869a-458">Proj 2</span></span></td>
<td><span data-ttu-id="7869a-459">Iekšējais 2. projekts</span><span class="sxs-lookup"><span data-stu-id="7869a-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7869a-460">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-460">10001</span></span></td>
<td><span data-ttu-id="7869a-461">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-461">Electricity</span></span></td>
<td><span data-ttu-id="7869a-462">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-462">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-463">10,00</span><span class="sxs-lookup"><span data-stu-id="7869a-463">10.00</span></span></td>
<td><span data-ttu-id="7869a-464">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7869a-465">Sīkāku informāciju skatiet šeit: [Pieskaitāmo izmaksu aprēķina veikšana](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="7869a-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="7869a-466">4. solis. Apstrādāt izmaksu sadalījuma aprēķinu</span><span class="sxs-lookup"><span data-stu-id="7869a-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="7869a-467">Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu.</span><span class="sxs-lookup"><span data-stu-id="7869a-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="7869a-468">Finance atbalsta savstarpējā sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="7869a-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="7869a-469">Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās.</span><span class="sxs-lookup"><span data-stu-id="7869a-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="7869a-470">Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="7869a-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="7869a-471">Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata.</span><span class="sxs-lookup"><span data-stu-id="7869a-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="7869a-472">Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos.</span><span class="sxs-lookup"><span data-stu-id="7869a-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="7869a-473">Sadalījuma secību kontrolē izmaksu kontroles vienība.</span><span class="sxs-lookup"><span data-stu-id="7869a-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="7869a-474">[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="7869a-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="7869a-475">Definēt izmaksu sadalījumu</span><span class="sxs-lookup"><span data-stu-id="7869a-475">Define the cost allocation</span></span>

<span data-ttu-id="7869a-476">Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="7869a-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="7869a-477">Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="7869a-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="7869a-478">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="7869a-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-479">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-479">Cost object</span></span></th>
<th><span data-ttu-id="7869a-480">HR pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="7869a-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-481">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-481">CC002</span></span></td>
<td><span data-ttu-id="7869a-482">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-482">Finance</span></span></td>
<td><span data-ttu-id="7869a-483">35</span><span class="sxs-lookup"><span data-stu-id="7869a-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-484">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-484">CC003</span></span></td>
<td><span data-ttu-id="7869a-485">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-485">Assembly</span></span></td>
<td><span data-ttu-id="7869a-486">55</span><span class="sxs-lookup"><span data-stu-id="7869a-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-487">CC004</span><span class="sxs-lookup"><span data-stu-id="7869a-487">CC004</span></span></td>
<td><span data-ttu-id="7869a-488">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7869a-488">Packaging</span></span></td>
<td><span data-ttu-id="7869a-489">10.</span><span class="sxs-lookup"><span data-stu-id="7869a-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7869a-490">Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="7869a-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="7869a-491">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.</span><span class="sxs-lookup"><span data-stu-id="7869a-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-492">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-492">Cost object</span></span></th>
<th><span data-ttu-id="7869a-493">Finanšu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="7869a-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-494">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-494">CC003</span></span></td>
<td><span data-ttu-id="7869a-495">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-495">Assembly</span></span></td>
<td><span data-ttu-id="7869a-496">65</span><span class="sxs-lookup"><span data-stu-id="7869a-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-497">CC004</span><span class="sxs-lookup"><span data-stu-id="7869a-497">CC004</span></span></td>
<td><span data-ttu-id="7869a-498">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7869a-498">Packaging</span></span></td>
<td><span data-ttu-id="7869a-499">35</span><span class="sxs-lookup"><span data-stu-id="7869a-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7869a-500">Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="7869a-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="7869a-501">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="7869a-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-502">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-502">Cost object</span></span></th>
<th><span data-ttu-id="7869a-503">Montāžas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="7869a-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7869a-504">Prod 1</span></span></td>
<td><span data-ttu-id="7869a-505">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-505">Product 1</span></span></td>
<td><span data-ttu-id="7869a-506">60</span><span class="sxs-lookup"><span data-stu-id="7869a-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7869a-507">Prod 2</span></span></td>
<td><span data-ttu-id="7869a-508">2. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-508">Product 2</span></span></td>
<td><span data-ttu-id="7869a-509">20</span><span class="sxs-lookup"><span data-stu-id="7869a-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7869a-510">Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos.</span><span class="sxs-lookup"><span data-stu-id="7869a-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="7869a-511">Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="7869a-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-512">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-512">Cost object</span></span></th>
<th><span data-ttu-id="7869a-513">Iepakošanas pakalpojumi (stundas)</span><span class="sxs-lookup"><span data-stu-id="7869a-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7869a-514">Prod 1</span></span></td>
<td><span data-ttu-id="7869a-515">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-515">Product 1</span></span></td>
<td><span data-ttu-id="7869a-516">80</span><span class="sxs-lookup"><span data-stu-id="7869a-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7869a-517">Prod 2</span></span></td>
<td><span data-ttu-id="7869a-518">2. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-518">Product 2</span></span></td>
<td><span data-ttu-id="7869a-519">15</span><span class="sxs-lookup"><span data-stu-id="7869a-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7869a-520">Statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem.</span><span class="sxs-lookup"><span data-stu-id="7869a-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="7869a-521">Sīkāku informāciju skatiet šeit: [Statistikas mēru nodrošinātāja veidne](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="7869a-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="7869a-522">Nākamajā tabulā ir parādīts rezultāts, ja tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījuma pamats tiek lietoti HR pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="7869a-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-523">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-523">Cost object</span></span></th>
<th><span data-ttu-id="7869a-524">Lielums</span><span class="sxs-lookup"><span data-stu-id="7869a-524">Magnitude</span></span></th>
<th><span data-ttu-id="7869a-525">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7869a-525">Allocation factor</span></span></th>
<th><span data-ttu-id="7869a-526">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-526">Amount</span></span></th>
<th><span data-ttu-id="7869a-527">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7869a-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-528">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-528">CC002</span></span></td>
<td><span data-ttu-id="7869a-529">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-529">Finance</span></span></td>
<td><span data-ttu-id="7869a-530">35</span><span class="sxs-lookup"><span data-stu-id="7869a-530">35</span></span></td>
<td><span data-ttu-id="7869a-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7869a-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7869a-532">175.00</span><span class="sxs-lookup"><span data-stu-id="7869a-532">175.00</span></span></td>
<td><span data-ttu-id="7869a-533">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-534">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-534">CC003</span></span></td>
<td><span data-ttu-id="7869a-535">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-535">Assembly</span></span></td>
<td><span data-ttu-id="7869a-536">55</span><span class="sxs-lookup"><span data-stu-id="7869a-536">55</span></span></td>
<td><span data-ttu-id="7869a-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7869a-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7869a-538">275.00</span><span class="sxs-lookup"><span data-stu-id="7869a-538">275.00</span></span></td>
<td><span data-ttu-id="7869a-539">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-540">CC004</span><span class="sxs-lookup"><span data-stu-id="7869a-540">CC004</span></span></td>
<td><span data-ttu-id="7869a-541">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7869a-541">Packaging</span></span></td>
<td><span data-ttu-id="7869a-542">10.</span><span class="sxs-lookup"><span data-stu-id="7869a-542">10</span></span></td>
<td><span data-ttu-id="7869a-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7869a-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7869a-544">50,00</span><span class="sxs-lookup"><span data-stu-id="7869a-544">50.00</span></span></td>
<td><span data-ttu-id="7869a-545">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-546">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-546">CC002</span></span></td>
<td><span data-ttu-id="7869a-547">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-547">Finance</span></span></td>
<td><span data-ttu-id="7869a-548">35</span><span class="sxs-lookup"><span data-stu-id="7869a-548">35</span></span></td>
<td><span data-ttu-id="7869a-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="7869a-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7869a-550">436.00</span><span class="sxs-lookup"><span data-stu-id="7869a-550">436.00</span></span></td>
<td><span data-ttu-id="7869a-551">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-552">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-552">CC003</span></span></td>
<td><span data-ttu-id="7869a-553">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-553">Assembly</span></span></td>
<td><span data-ttu-id="7869a-554">55</span><span class="sxs-lookup"><span data-stu-id="7869a-554">55</span></span></td>
<td><span data-ttu-id="7869a-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="7869a-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7869a-556">685.14</span><span class="sxs-lookup"><span data-stu-id="7869a-556">685.14</span></span></td>
<td><span data-ttu-id="7869a-557">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-558">CC004</span><span class="sxs-lookup"><span data-stu-id="7869a-558">CC004</span></span></td>
<td><span data-ttu-id="7869a-559">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7869a-559">Packaging</span></span></td>
<td><span data-ttu-id="7869a-560">10.</span><span class="sxs-lookup"><span data-stu-id="7869a-560">10</span></span></td>
<td><span data-ttu-id="7869a-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="7869a-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7869a-562">124.57</span><span class="sxs-lookup"><span data-stu-id="7869a-562">124.57</span></span></td>
<td><span data-ttu-id="7869a-563">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7869a-564">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="7869a-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-565">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-565">Cost object</span></span></th>
<th><span data-ttu-id="7869a-566">Lielums</span><span class="sxs-lookup"><span data-stu-id="7869a-566">Magnitude</span></span></th>
<th><span data-ttu-id="7869a-567">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7869a-567">Allocation factor</span></span></th>
<th><span data-ttu-id="7869a-568">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-568">Amount</span></span></th>
<th><span data-ttu-id="7869a-569">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7869a-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-570">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-570">CC003</span></span></td>
<td><span data-ttu-id="7869a-571">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-571">Assembly</span></span></td>
<td><span data-ttu-id="7869a-572">65</span><span class="sxs-lookup"><span data-stu-id="7869a-572">65</span></span></td>
<td><span data-ttu-id="7869a-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7869a-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7869a-574">438.75</span><span class="sxs-lookup"><span data-stu-id="7869a-574">438.75</span></span></td>
<td><span data-ttu-id="7869a-575">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-576">CC004</span><span class="sxs-lookup"><span data-stu-id="7869a-576">CC004</span></span></td>
<td><span data-ttu-id="7869a-577">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7869a-577">Packaging</span></span></td>
<td><span data-ttu-id="7869a-578">35</span><span class="sxs-lookup"><span data-stu-id="7869a-578">35</span></span></td>
<td><span data-ttu-id="7869a-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7869a-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7869a-580">236.25</span><span class="sxs-lookup"><span data-stu-id="7869a-580">236.25</span></span></td>
<td><span data-ttu-id="7869a-581">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-582">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-582">CC003</span></span></td>
<td><span data-ttu-id="7869a-583">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-583">Assembly</span></span></td>
<td><span data-ttu-id="7869a-584">65</span><span class="sxs-lookup"><span data-stu-id="7869a-584">65</span></span></td>
<td><span data-ttu-id="7869a-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7869a-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7869a-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7869a-586">5,297.69</span></span></td>
<td><span data-ttu-id="7869a-587">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-588">CC004</span><span class="sxs-lookup"><span data-stu-id="7869a-588">CC004</span></span></td>
<td><span data-ttu-id="7869a-589">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7869a-589">Packaging</span></span></td>
<td><span data-ttu-id="7869a-590">35</span><span class="sxs-lookup"><span data-stu-id="7869a-590">35</span></span></td>
<td><span data-ttu-id="7869a-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7869a-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7869a-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7869a-592">2,852.60</span></span></td>
<td><span data-ttu-id="7869a-593">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7869a-594">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="7869a-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-595">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-595">Cost object</span></span></th>
<th><span data-ttu-id="7869a-596">Lielums</span><span class="sxs-lookup"><span data-stu-id="7869a-596">Magnitude</span></span></th>
<th><span data-ttu-id="7869a-597">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7869a-597">Allocation factor</span></span></th>
<th><span data-ttu-id="7869a-598">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-598">Amount</span></span></th>
<th><span data-ttu-id="7869a-599">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7869a-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7869a-600">Prod 1</span></span></td>
<td><span data-ttu-id="7869a-601">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-601">Product 1</span></span></td>
<td><span data-ttu-id="7869a-602">60</span><span class="sxs-lookup"><span data-stu-id="7869a-602">60</span></span></td>
<td><span data-ttu-id="7869a-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7869a-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7869a-604">535.31</span><span class="sxs-lookup"><span data-stu-id="7869a-604">535.31</span></span></td>
<td><span data-ttu-id="7869a-605">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7869a-606">Prod 2</span></span></td>
<td><span data-ttu-id="7869a-607">2. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-607">Product 2</span></span></td>
<td><span data-ttu-id="7869a-608">20.</span><span class="sxs-lookup"><span data-stu-id="7869a-608">20</span></span></td>
<td><span data-ttu-id="7869a-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7869a-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7869a-610">178.44</span><span class="sxs-lookup"><span data-stu-id="7869a-610">178.44</span></span></td>
<td><span data-ttu-id="7869a-611">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7869a-612">Prod 1</span></span></td>
<td><span data-ttu-id="7869a-613">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-613">Product 1</span></span></td>
<td><span data-ttu-id="7869a-614">60</span><span class="sxs-lookup"><span data-stu-id="7869a-614">60</span></span></td>
<td><span data-ttu-id="7869a-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7869a-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7869a-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7869a-616">4,487.12</span></span></td>
<td><span data-ttu-id="7869a-617">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7869a-618">Prod 2</span></span></td>
<td><span data-ttu-id="7869a-619">2. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-619">Product 2</span></span></td>
<td><span data-ttu-id="7869a-620">20.</span><span class="sxs-lookup"><span data-stu-id="7869a-620">20</span></span></td>
<td><span data-ttu-id="7869a-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7869a-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7869a-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7869a-622">1,495.71</span></span></td>
<td><span data-ttu-id="7869a-623">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7869a-624">Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="7869a-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-625">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-625">Cost object</span></span></th>
<th><span data-ttu-id="7869a-626">Lielums</span><span class="sxs-lookup"><span data-stu-id="7869a-626">Magnitude</span></span></th>
<th><span data-ttu-id="7869a-627">Sadalījuma koeficients</span><span class="sxs-lookup"><span data-stu-id="7869a-627">Allocation factor</span></span></th>
<th><span data-ttu-id="7869a-628">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-628">Amount</span></span></th>
<th><span data-ttu-id="7869a-629">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7869a-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7869a-630">Prod 1</span></span></td>
<td><span data-ttu-id="7869a-631">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-631">Product 1</span></span></td>
<td><span data-ttu-id="7869a-632">80</span><span class="sxs-lookup"><span data-stu-id="7869a-632">80</span></span></td>
<td><span data-ttu-id="7869a-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7869a-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7869a-634">241.05</span><span class="sxs-lookup"><span data-stu-id="7869a-634">241.05</span></span></td>
<td><span data-ttu-id="7869a-635">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7869a-636">Prod 2</span></span></td>
<td><span data-ttu-id="7869a-637">2. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-637">Product 2</span></span></td>
<td><span data-ttu-id="7869a-638">15</span><span class="sxs-lookup"><span data-stu-id="7869a-638">15</span></span></td>
<td><span data-ttu-id="7869a-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7869a-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7869a-640">45.20</span><span class="sxs-lookup"><span data-stu-id="7869a-640">45.20</span></span></td>
<td><span data-ttu-id="7869a-641">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7869a-642">Prod 1</span></span></td>
<td><span data-ttu-id="7869a-643">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-643">Product 1</span></span></td>
<td><span data-ttu-id="7869a-644">80</span><span class="sxs-lookup"><span data-stu-id="7869a-644">80</span></span></td>
<td><span data-ttu-id="7869a-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7869a-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7869a-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7869a-646">2,507.09</span></span></td>
<td><span data-ttu-id="7869a-647">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7869a-648">Prod 2</span></span></td>
<td><span data-ttu-id="7869a-649">2. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-649">Product 2</span></span></td>
<td><span data-ttu-id="7869a-650">15</span><span class="sxs-lookup"><span data-stu-id="7869a-650">15</span></span></td>
<td><span data-ttu-id="7869a-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7869a-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7869a-652">470.08</span><span class="sxs-lookup"><span data-stu-id="7869a-652">470.08</span></span></td>
<td><span data-ttu-id="7869a-653">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7869a-654">Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)</span><span class="sxs-lookup"><span data-stu-id="7869a-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7869a-655">Žurnāls</span><span class="sxs-lookup"><span data-stu-id="7869a-655">Journal</span></span></th>
<th><span data-ttu-id="7869a-656">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="7869a-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7869a-657">Kalendārais finanšu periods</span><span class="sxs-lookup"><span data-stu-id="7869a-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7869a-658">Versija</span><span class="sxs-lookup"><span data-stu-id="7869a-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-659">00004</span><span class="sxs-lookup"><span data-stu-id="7869a-659">00004</span></span></td>
<td><span data-ttu-id="7869a-660">Izmaksu sadalījuma žurnāls</span><span class="sxs-lookup"><span data-stu-id="7869a-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="7869a-661">Finanšu</span><span class="sxs-lookup"><span data-stu-id="7869a-661">Fiscal</span></span></td>
<td><span data-ttu-id="7869a-662">2017</span><span class="sxs-lookup"><span data-stu-id="7869a-662">2017</span></span></td>
<td><span data-ttu-id="7869a-663">Periods 1</span><span class="sxs-lookup"><span data-stu-id="7869a-663">Period 1</span></span></td>
<td><span data-ttu-id="7869a-664">Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</span><span class="sxs-lookup"><span data-stu-id="7869a-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="7869a-665">Žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="7869a-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7869a-666">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7869a-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7869a-667">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7869a-668">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7869a-668">Cost element</span></span></th>
<th><span data-ttu-id="7869a-669">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7869a-669">Cost behavior</span></span></th>
<th><span data-ttu-id="7869a-670">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-671">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-672">CC001</span><span class="sxs-lookup"><span data-stu-id="7869a-672">CC001</span></span></td>
<td><span data-ttu-id="7869a-673">HR</span><span class="sxs-lookup"><span data-stu-id="7869a-673">HR</span></span></td>
<td><span data-ttu-id="7869a-674">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-674">10001</span></span></td>
<td><span data-ttu-id="7869a-675">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-675">Electricity</span></span></td>
<td><span data-ttu-id="7869a-676">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-676">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-677">500,00</span><span class="sxs-lookup"><span data-stu-id="7869a-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-678">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-679">CC001</span><span class="sxs-lookup"><span data-stu-id="7869a-679">CC001</span></span></td>
<td><span data-ttu-id="7869a-680">HR</span><span class="sxs-lookup"><span data-stu-id="7869a-680">HR</span></span></td>
<td><span data-ttu-id="7869a-681">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-681">10001</span></span></td>
<td><span data-ttu-id="7869a-682">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-682">Electricity</span></span></td>
<td><span data-ttu-id="7869a-683">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-683">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="7869a-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-685">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-686">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-686">CC002</span></span></td>
<td><span data-ttu-id="7869a-687">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-687">Finance</span></span></td>
<td><span data-ttu-id="7869a-688">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-688">10001</span></span></td>
<td><span data-ttu-id="7869a-689">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-689">Electricity</span></span></td>
<td><span data-ttu-id="7869a-690">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-690">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-691">675.00</span><span class="sxs-lookup"><span data-stu-id="7869a-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-692">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-693">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-693">CC002</span></span></td>
<td><span data-ttu-id="7869a-694">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-694">Finance</span></span></td>
<td><span data-ttu-id="7869a-695">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-695">10001</span></span></td>
<td><span data-ttu-id="7869a-696">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-696">Electricity</span></span></td>
<td><span data-ttu-id="7869a-697">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-697">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="7869a-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-699">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-700">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-700">CC003</span></span></td>
<td><span data-ttu-id="7869a-701">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-701">Assembly</span></span></td>
<td><span data-ttu-id="7869a-702">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-702">10001</span></span></td>
<td><span data-ttu-id="7869a-703">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-703">Electricity</span></span></td>
<td><span data-ttu-id="7869a-704">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-704">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-705">713.75</span><span class="sxs-lookup"><span data-stu-id="7869a-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-706">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-707">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-707">CC003</span></span></td>
<td><span data-ttu-id="7869a-708">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-708">Assembly</span></span></td>
<td><span data-ttu-id="7869a-709">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-709">10001</span></span></td>
<td><span data-ttu-id="7869a-710">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-710">Electricity</span></span></td>
<td><span data-ttu-id="7869a-711">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-711">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="7869a-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-713">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-714">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-714">CC003</span></span></td>
<td><span data-ttu-id="7869a-715">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7869a-715">Packaging</span></span></td>
<td><span data-ttu-id="7869a-716">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-716">10001</span></span></td>
<td><span data-ttu-id="7869a-717">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-717">Electricity</span></span></td>
<td><span data-ttu-id="7869a-718">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-718">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-719">286.25</span><span class="sxs-lookup"><span data-stu-id="7869a-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-720">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-721">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-721">CC003</span></span></td>
<td><span data-ttu-id="7869a-722">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7869a-722">Packaging</span></span></td>
<td><span data-ttu-id="7869a-723">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-723">10001</span></span></td>
<td><span data-ttu-id="7869a-724">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-724">Electricity</span></span></td>
<td><span data-ttu-id="7869a-725">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-725">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="7869a-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-727">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7869a-728">Prod 1</span></span></td>
<td><span data-ttu-id="7869a-729">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-729">Product 1</span></span></td>
<td><span data-ttu-id="7869a-730">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-730">10001</span></span></td>
<td><span data-ttu-id="7869a-731">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-731">Electricity</span></span></td>
<td><span data-ttu-id="7869a-732">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-732">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-733">776.36</span><span class="sxs-lookup"><span data-stu-id="7869a-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-734">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7869a-735">Prod 1</span></span></td>
<td><span data-ttu-id="7869a-736">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-736">Product 1</span></span></td>
<td><span data-ttu-id="7869a-737">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-737">10001</span></span></td>
<td><span data-ttu-id="7869a-738">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-738">Electricity</span></span></td>
<td><span data-ttu-id="7869a-739">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-739">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7869a-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-741">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7869a-742">Prod 2</span></span></td>
<td><span data-ttu-id="7869a-743">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-743">Product 1</span></span></td>
<td><span data-ttu-id="7869a-744">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-744">10001</span></span></td>
<td><span data-ttu-id="7869a-745">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-745">Electricity</span></span></td>
<td><span data-ttu-id="7869a-746">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-746">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-747">223.64</span><span class="sxs-lookup"><span data-stu-id="7869a-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-748">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="7869a-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7869a-749">Prod 2</span></span></td>
<td><span data-ttu-id="7869a-750">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-750">Product 1</span></span></td>
<td><span data-ttu-id="7869a-751">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-751">10001</span></span></td>
<td><span data-ttu-id="7869a-752">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-752">Electricity</span></span></td>
<td><span data-ttu-id="7869a-753">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-753">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7869a-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7869a-755">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="7869a-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7869a-756">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7869a-757">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7869a-757">Cost element</span></span></th>
<th><span data-ttu-id="7869a-758">Izmaksu izturēšanās</span><span class="sxs-lookup"><span data-stu-id="7869a-758">Cost behavior</span></span></th>
<th><span data-ttu-id="7869a-759">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-759">Amount</span></span></th>
<th><span data-ttu-id="7869a-760">Uzskaites datums</span><span class="sxs-lookup"><span data-stu-id="7869a-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7869a-761">CC001</span><span class="sxs-lookup"><span data-stu-id="7869a-761">CC001</span></span></td>
<td><span data-ttu-id="7869a-762">HR</span><span class="sxs-lookup"><span data-stu-id="7869a-762">HR</span></span></td>
<td><span data-ttu-id="7869a-763">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-763">10001</span></span></td>
<td><span data-ttu-id="7869a-764">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-764">Electricity</span></span></td>
<td><span data-ttu-id="7869a-765">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-765">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="7869a-766">-500.00</span></span></td>
<td><span data-ttu-id="7869a-767">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-768">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-768">CC002</span></span></td>
<td><span data-ttu-id="7869a-769">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-769">Finance</span></span></td>
<td><span data-ttu-id="7869a-770">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-770">10001</span></span></td>
<td><span data-ttu-id="7869a-771">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-771">Electricity</span></span></td>
<td><span data-ttu-id="7869a-772">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-772">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-773">175.00</span><span class="sxs-lookup"><span data-stu-id="7869a-773">175.00</span></span></td>
<td><span data-ttu-id="7869a-774">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-775">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-775">CC003</span></span></td>
<td><span data-ttu-id="7869a-776">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-776">Assembly</span></span></td>
<td><span data-ttu-id="7869a-777">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-777">10001</span></span></td>
<td><span data-ttu-id="7869a-778">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-778">Electricity</span></span></td>
<td><span data-ttu-id="7869a-779">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-779">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-780">275.00</span><span class="sxs-lookup"><span data-stu-id="7869a-780">275.00</span></span></td>
<td><span data-ttu-id="7869a-781">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-782">CC004</span><span class="sxs-lookup"><span data-stu-id="7869a-782">CC004</span></span></td>
<td><span data-ttu-id="7869a-783">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7869a-783">Packaging</span></span></td>
<td><span data-ttu-id="7869a-784">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-784">10001</span></span></td>
<td><span data-ttu-id="7869a-785">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-785">Electricity</span></span></td>
<td><span data-ttu-id="7869a-786">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-786">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-787">50,00</span><span class="sxs-lookup"><span data-stu-id="7869a-787">50,00</span></span></td>
<td><span data-ttu-id="7869a-788">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-789">CC001</span><span class="sxs-lookup"><span data-stu-id="7869a-789">CC001</span></span></td>
<td><span data-ttu-id="7869a-790">HR</span><span class="sxs-lookup"><span data-stu-id="7869a-790">HR</span></span></td>
<td><span data-ttu-id="7869a-791">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-791">10001</span></span></td>
<td><span data-ttu-id="7869a-792">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-792">Electricity</span></span></td>
<td><span data-ttu-id="7869a-793">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-793">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="7869a-794">-1,245.71</span></span></td>
<td><span data-ttu-id="7869a-795">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-796">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-796">CC002</span></span></td>
<td><span data-ttu-id="7869a-797">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-797">Finance</span></span></td>
<td><span data-ttu-id="7869a-798">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-798">10001</span></span></td>
<td><span data-ttu-id="7869a-799">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-799">Electricity</span></span></td>
<td><span data-ttu-id="7869a-800">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-800">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-801">436.00</span><span class="sxs-lookup"><span data-stu-id="7869a-801">436.00</span></span></td>
<td><span data-ttu-id="7869a-802">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-803">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-803">CC003</span></span></td>
<td><span data-ttu-id="7869a-804">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-804">Assembly</span></span></td>
<td><span data-ttu-id="7869a-805">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-805">10001</span></span></td>
<td><span data-ttu-id="7869a-806">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-806">Electricity</span></span></td>
<td><span data-ttu-id="7869a-807">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-807">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-808">685.14</span><span class="sxs-lookup"><span data-stu-id="7869a-808">685.14</span></span></td>
<td><span data-ttu-id="7869a-809">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-810">CC004</span><span class="sxs-lookup"><span data-stu-id="7869a-810">CC004</span></span></td>
<td><span data-ttu-id="7869a-811">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7869a-811">Packaging</span></span></td>
<td><span data-ttu-id="7869a-812">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-812">10001</span></span></td>
<td><span data-ttu-id="7869a-813">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-813">Electricity</span></span></td>
<td><span data-ttu-id="7869a-814">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-814">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-815">124.57</span><span class="sxs-lookup"><span data-stu-id="7869a-815">124.57</span></span></td>
<td><span data-ttu-id="7869a-816">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-817">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-817">CC002</span></span></td>
<td><span data-ttu-id="7869a-818">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-818">Finance</span></span></td>
<td><span data-ttu-id="7869a-819">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-819">10001</span></span></td>
<td><span data-ttu-id="7869a-820">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-820">Electricity</span></span></td>
<td><span data-ttu-id="7869a-821">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-821">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="7869a-822">-675.00</span></span></td>
<td><span data-ttu-id="7869a-823">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-824">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-824">CC003</span></span></td>
<td><span data-ttu-id="7869a-825">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-825">Assembly</span></span></td>
<td><span data-ttu-id="7869a-826">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-826">10001</span></span></td>
<td><span data-ttu-id="7869a-827">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-827">Electricity</span></span></td>
<td><span data-ttu-id="7869a-828">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-828">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-829">438.75</span><span class="sxs-lookup"><span data-stu-id="7869a-829">438.75</span></span></td>
<td><span data-ttu-id="7869a-830">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-831">CC004</span><span class="sxs-lookup"><span data-stu-id="7869a-831">CC004</span></span></td>
<td><span data-ttu-id="7869a-832">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7869a-832">Packaging</span></span></td>
<td><span data-ttu-id="7869a-833">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-833">10001</span></span></td>
<td><span data-ttu-id="7869a-834">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-834">Electricity</span></span></td>
<td><span data-ttu-id="7869a-835">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-835">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-836">236.25</span><span class="sxs-lookup"><span data-stu-id="7869a-836">236.25</span></span></td>
<td><span data-ttu-id="7869a-837">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-838">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-838">CC002</span></span></td>
<td><span data-ttu-id="7869a-839">Finanses</span><span class="sxs-lookup"><span data-stu-id="7869a-839">Finance</span></span></td>
<td><span data-ttu-id="7869a-840">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-840">10001</span></span></td>
<td><span data-ttu-id="7869a-841">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-841">Electricity</span></span></td>
<td><span data-ttu-id="7869a-842">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-842">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="7869a-843">-8,150.29</span></span></td>
<td><span data-ttu-id="7869a-844">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-845">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-845">CC003</span></span></td>
<td><span data-ttu-id="7869a-846">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-846">Assembly</span></span></td>
<td><span data-ttu-id="7869a-847">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-847">10001</span></span></td>
<td><span data-ttu-id="7869a-848">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-848">Electricity</span></span></td>
<td><span data-ttu-id="7869a-849">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-849">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7869a-850">5,297.69</span></span></td>
<td><span data-ttu-id="7869a-851">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-852">CC004</span><span class="sxs-lookup"><span data-stu-id="7869a-852">CC004</span></span></td>
<td><span data-ttu-id="7869a-853">Iepakošana</span><span class="sxs-lookup"><span data-stu-id="7869a-853">Packaging</span></span></td>
<td><span data-ttu-id="7869a-854">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-854">10001</span></span></td>
<td><span data-ttu-id="7869a-855">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-855">Electricity</span></span></td>
<td><span data-ttu-id="7869a-856">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-856">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7869a-857">2,852.60</span></span></td>
<td><span data-ttu-id="7869a-858">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-859">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-859">CC003</span></span></td>
<td><span data-ttu-id="7869a-860">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-860">Assembly</span></span></td>
<td><span data-ttu-id="7869a-861">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-861">10001</span></span></td>
<td><span data-ttu-id="7869a-862">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-862">Electricity</span></span></td>
<td><span data-ttu-id="7869a-863">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-863">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="7869a-864">-713.75</span></span></td>
<td><span data-ttu-id="7869a-865">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7869a-866">Prod 1</span></span></td>
<td><span data-ttu-id="7869a-867">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-867">Product 1</span></span></td>
<td><span data-ttu-id="7869a-868">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-868">10001</span></span></td>
<td><span data-ttu-id="7869a-869">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-869">Electricity</span></span></td>
<td><span data-ttu-id="7869a-870">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-870">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-871">535.31</span><span class="sxs-lookup"><span data-stu-id="7869a-871">535.31</span></span></td>
<td><span data-ttu-id="7869a-872">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7869a-873">Prod 2</span></span></td>
<td><span data-ttu-id="7869a-874">2. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-874">Product 2</span></span></td>
<td><span data-ttu-id="7869a-875">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-875">10001</span></span></td>
<td><span data-ttu-id="7869a-876">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-876">Electricity</span></span></td>
<td><span data-ttu-id="7869a-877">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-877">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-878">178.44</span><span class="sxs-lookup"><span data-stu-id="7869a-878">178.44</span></span></td>
<td><span data-ttu-id="7869a-879">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-880">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-880">CC003</span></span></td>
<td><span data-ttu-id="7869a-881">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-881">Assembly</span></span></td>
<td><span data-ttu-id="7869a-882">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-882">10001</span></span></td>
<td><span data-ttu-id="7869a-883">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-883">Electricity</span></span></td>
<td><span data-ttu-id="7869a-884">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-884">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="7869a-885">-5,982.83</span></span></td>
<td><span data-ttu-id="7869a-886">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7869a-887">Prod 1</span></span></td>
<td><span data-ttu-id="7869a-888">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-888">Product 1</span></span></td>
<td><span data-ttu-id="7869a-889">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-889">10001</span></span></td>
<td><span data-ttu-id="7869a-890">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-890">Electricity</span></span></td>
<td><span data-ttu-id="7869a-891">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-891">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7869a-892">4,487.12</span></span></td>
<td><span data-ttu-id="7869a-893">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7869a-894">Prod 2</span></span></td>
<td><span data-ttu-id="7869a-895">2. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-895">Product 2</span></span></td>
<td><span data-ttu-id="7869a-896">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-896">10001</span></span></td>
<td><span data-ttu-id="7869a-897">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-897">Electricity</span></span></td>
<td><span data-ttu-id="7869a-898">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-898">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7869a-899">1,495.71</span></span></td>
<td><span data-ttu-id="7869a-900">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-901">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-901">CC003</span></span></td>
<td><span data-ttu-id="7869a-902">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-902">Assembly</span></span></td>
<td><span data-ttu-id="7869a-903">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-903">10001</span></span></td>
<td><span data-ttu-id="7869a-904">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-904">Electricity</span></span></td>
<td><span data-ttu-id="7869a-905">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-905">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="7869a-906">-286.25</span></span></td>
<td><span data-ttu-id="7869a-907">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7869a-908">Prod 1</span></span></td>
<td><span data-ttu-id="7869a-909">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-909">Product 1</span></span></td>
<td><span data-ttu-id="7869a-910">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-910">10001</span></span></td>
<td><span data-ttu-id="7869a-911">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-911">Electricity</span></span></td>
<td><span data-ttu-id="7869a-912">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-912">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-913">241.05</span><span class="sxs-lookup"><span data-stu-id="7869a-913">241.05</span></span></td>
<td><span data-ttu-id="7869a-914">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7869a-915">Prod 2</span></span></td>
<td><span data-ttu-id="7869a-916">2. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-916">Product 2</span></span></td>
<td><span data-ttu-id="7869a-917">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-917">10001</span></span></td>
<td><span data-ttu-id="7869a-918">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-918">Electricity</span></span></td>
<td><span data-ttu-id="7869a-919">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-919">Fixed cost</span></span></td>
<td><span data-ttu-id="7869a-920">45.20</span><span class="sxs-lookup"><span data-stu-id="7869a-920">45.20</span></span></td>
<td><span data-ttu-id="7869a-921">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-922">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-922">CC003</span></span></td>
<td><span data-ttu-id="7869a-923">Montāža</span><span class="sxs-lookup"><span data-stu-id="7869a-923">Assembly</span></span></td>
<td><span data-ttu-id="7869a-924">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-924">10001</span></span></td>
<td><span data-ttu-id="7869a-925">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-925">Electricity</span></span></td>
<td><span data-ttu-id="7869a-926">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-926">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="7869a-927">-2,977.17</span></span></td>
<td><span data-ttu-id="7869a-928">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7869a-929">Prod 1</span></span></td>
<td><span data-ttu-id="7869a-930">1. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-930">Product 1</span></span></td>
<td><span data-ttu-id="7869a-931">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-931">10001</span></span></td>
<td><span data-ttu-id="7869a-932">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-932">Electricity</span></span></td>
<td><span data-ttu-id="7869a-933">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-933">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7869a-934">2,507.09</span></span></td>
<td><span data-ttu-id="7869a-935">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7869a-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7869a-936">Prod 2</span></span></td>
<td><span data-ttu-id="7869a-937">2. prece</span><span class="sxs-lookup"><span data-stu-id="7869a-937">Product 2</span></span></td>
<td><span data-ttu-id="7869a-938">10001</span><span class="sxs-lookup"><span data-stu-id="7869a-938">10001</span></span></td>
<td><span data-ttu-id="7869a-939">Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-939">Electricity</span></span></td>
<td><span data-ttu-id="7869a-940">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-940">Variable cost</span></span></td>
<td><span data-ttu-id="7869a-941">470.08</span><span class="sxs-lookup"><span data-stu-id="7869a-941">470.08</span></span></td>
<td><span data-ttu-id="7869a-942">2017. gada 31. janvāris</span><span class="sxs-lookup"><span data-stu-id="7869a-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="7869a-943">Nobeigums</span><span class="sxs-lookup"><span data-stu-id="7869a-943">Conclusion</span></span>
<span data-ttu-id="7869a-944">Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID.</span><span class="sxs-lookup"><span data-stu-id="7869a-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="7869a-945">Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="7869a-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="7869a-946">Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām.</span><span class="sxs-lookup"><span data-stu-id="7869a-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="7869a-947">Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="7869a-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="7869a-948">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7869a-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="7869a-949">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7869a-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="7869a-950">Summa</span><span class="sxs-lookup"><span data-stu-id="7869a-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7869a-951">CC099</span><span class="sxs-lookup"><span data-stu-id="7869a-951">CC099</span></span></th>
<th><span data-ttu-id="7869a-952">CC001</span><span class="sxs-lookup"><span data-stu-id="7869a-952">CC001</span></span></th>
<th><span data-ttu-id="7869a-953">CC002</span><span class="sxs-lookup"><span data-stu-id="7869a-953">CC002</span></span></th>
<th><span data-ttu-id="7869a-954">CC003</span><span class="sxs-lookup"><span data-stu-id="7869a-954">CC003</span></span></th>
<th><span data-ttu-id="7869a-955">CC004</span><span class="sxs-lookup"><span data-stu-id="7869a-955">CC004</span></span></th>
<th><span data-ttu-id="7869a-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7869a-956">Proj 1</span></span></th>
<th><span data-ttu-id="7869a-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7869a-957">Proj 2</span></span></th>
<th><span data-ttu-id="7869a-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7869a-958">Prod 1</span></span></th>
<th><span data-ttu-id="7869a-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7869a-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="7869a-960">10001 Elektrība</span><span class="sxs-lookup"><span data-stu-id="7869a-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="7869a-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="7869a-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="7869a-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="7869a-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7869a-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="7869a-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="7869a-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="7869a-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="7869a-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="7869a-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="7869a-970">Neklasificēts</span><span class="sxs-lookup"><span data-stu-id="7869a-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-971">0,00</span><span class="sxs-lookup"><span data-stu-id="7869a-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="7869a-972">Fiksētas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-973">0,00</span><span class="sxs-lookup"><span data-stu-id="7869a-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-974">0,00</span><span class="sxs-lookup"><span data-stu-id="7869a-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-975">0,00</span><span class="sxs-lookup"><span data-stu-id="7869a-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-976">0,00</span><span class="sxs-lookup"><span data-stu-id="7869a-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-977">0,00</span><span class="sxs-lookup"><span data-stu-id="7869a-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7869a-978">776.36</span><span class="sxs-lookup"><span data-stu-id="7869a-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-979">223.64</span><span class="sxs-lookup"><span data-stu-id="7869a-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="7869a-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="7869a-981">Mainīgas izmaksas</span><span class="sxs-lookup"><span data-stu-id="7869a-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-982">000</span><span class="sxs-lookup"><span data-stu-id="7869a-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-983">0,00</span><span class="sxs-lookup"><span data-stu-id="7869a-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-984">0,00</span><span class="sxs-lookup"><span data-stu-id="7869a-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-985">0,00</span><span class="sxs-lookup"><span data-stu-id="7869a-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-986">0,00</span><span class="sxs-lookup"><span data-stu-id="7869a-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-987">30,00</span><span class="sxs-lookup"><span data-stu-id="7869a-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-988">10,00</span><span class="sxs-lookup"><span data-stu-id="7869a-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7869a-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7869a-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7869a-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="7869a-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7869a-992">Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem.</span><span class="sxs-lookup"><span data-stu-id="7869a-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="7869a-993">Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā.</span><span class="sxs-lookup"><span data-stu-id="7869a-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="7869a-994">Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti.</span><span class="sxs-lookup"><span data-stu-id="7869a-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="7869a-995">Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu.</span><span class="sxs-lookup"><span data-stu-id="7869a-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="7869a-996">Sīkāku informāciju skatiet šeit: [Izmaksu apkopošanas politika](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="7869a-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



