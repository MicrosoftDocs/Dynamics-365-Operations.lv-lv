---
title: Darbaspēka organizēšana, izmantojot nodaļas, darbus un amatus
description: Nodaļas, amati un pozīcijas ir organizācijas elementi, kas tiek uzturēti personāla vadības procesā. Šajā tēmā ir sniegta konceptuāla informācija par šiem elementiem.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent, Retail
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 968167f735cfa05ef17348ce1d55a184e355fbad
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/19/2019
ms.locfileid: "857342"
---
# <a name="organize-your-workforce-by-using-departments-jobs-and-positions"></a><span data-ttu-id="938d0-104">Darbaspēka organizēšana, izmantojot nodaļas, darbus un amatus</span><span class="sxs-lookup"><span data-stu-id="938d0-104">Organize your workforce by using departments, jobs, and positions</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="938d0-105">Nodaļas, amati un pozīcijas ir organizācijas elementi, kas tiek uzturēti personāla vadības procesā.</span><span class="sxs-lookup"><span data-stu-id="938d0-105">Departments, jobs, and positions are organizational elements that are maintained within Human resources.</span></span> <span data-ttu-id="938d0-106">Šajā tēmā ir sniegta konceptuāla informācija par šiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="938d0-106">This topic describes conceptual information about these elements.</span></span> 

<span data-ttu-id="938d0-107">Tālāk sniegtais piemērs tiek izmantots, lai paskaidrotu šajā tēmā aprakstītās koncepcijas.</span><span class="sxs-lookup"><span data-stu-id="938d0-107">The following example is used to illustrate the concepts described in this topic.</span></span>

|<span data-ttu-id="938d0-108">**Nodaļa**</span><span class="sxs-lookup"><span data-stu-id="938d0-108">**Department**</span></span>|<span data-ttu-id="938d0-109">**Amats**</span><span class="sxs-lookup"><span data-stu-id="938d0-109">**Position**</span></span>|<span data-ttu-id="938d0-110">**Darbs**</span><span class="sxs-lookup"><span data-stu-id="938d0-110">**Job**</span></span>|
|---|---|---|
|<span data-ttu-id="938d0-111">**Pārdošana**</span><span class="sxs-lookup"><span data-stu-id="938d0-111">**Sales**</span></span>|<span data-ttu-id="938d0-112">Pārdošanas daļas vadītājs (austrumu reģions)</span><span class="sxs-lookup"><span data-stu-id="938d0-112">Sales manager (East)</span></span>|<span data-ttu-id="938d0-113">Pārdošanas daļas vadītājs</span><span class="sxs-lookup"><span data-stu-id="938d0-113">Sales manager</span></span>|
|<span data-ttu-id="938d0-114">**Pārdošana**</span><span class="sxs-lookup"><span data-stu-id="938d0-114">**Sales**</span></span>|<span data-ttu-id="938d0-115">Pārdošanas daļas vadītājs (rietumu reģions)</span><span class="sxs-lookup"><span data-stu-id="938d0-115">Sales manager (West)</span></span>|<span data-ttu-id="938d0-116">Pārdošanas daļas vadītājs</span><span class="sxs-lookup"><span data-stu-id="938d0-116">Sales manager</span></span>|
|<span data-ttu-id="938d0-117">**Pārdošana**</span><span class="sxs-lookup"><span data-stu-id="938d0-117">**Sales**</span></span>|<span data-ttu-id="938d0-118">Pārdošanas daļas vadītājs (centrālais reģions)</span><span class="sxs-lookup"><span data-stu-id="938d0-118">Sales manager (Central)</span></span>|<span data-ttu-id="938d0-119">Pārdošanas daļas vadītājs</span><span class="sxs-lookup"><span data-stu-id="938d0-119">Sales manager</span></span>|
|<span data-ttu-id="938d0-120">**Uzskaite**</span><span class="sxs-lookup"><span data-stu-id="938d0-120">**Accounting**</span></span>|<span data-ttu-id="938d0-121">Uzskaites supervizors</span><span class="sxs-lookup"><span data-stu-id="938d0-121">Accounting supervisor</span></span>|<span data-ttu-id="938d0-122">Uzskaites vadītājs</span><span class="sxs-lookup"><span data-stu-id="938d0-122">Accounting manager</span></span>|
|<span data-ttu-id="938d0-123">**Uzskaite**</span><span class="sxs-lookup"><span data-stu-id="938d0-123">**Accounting**</span></span>|<span data-ttu-id="938d0-124">Uzskaite A</span><span class="sxs-lookup"><span data-stu-id="938d0-124">Accounting-A</span></span>|<span data-ttu-id="938d0-125">Grāmatvedis</span><span class="sxs-lookup"><span data-stu-id="938d0-125">Accountant</span></span>|
|<span data-ttu-id="938d0-126">**Personāla vadība**</span><span class="sxs-lookup"><span data-stu-id="938d0-126">**Human resources**</span></span>|<span data-ttu-id="938d0-127">PV vadītājs (austrumu reģions)</span><span class="sxs-lookup"><span data-stu-id="938d0-127">HR manager (East)</span></span>|<span data-ttu-id="938d0-128">PV vadītājs</span><span class="sxs-lookup"><span data-stu-id="938d0-128">HR manager</span></span>|
|<span data-ttu-id="938d0-129">**Personāla vadība**</span><span class="sxs-lookup"><span data-stu-id="938d0-129">**Human resources**</span></span>|<span data-ttu-id="938d0-130">PV vadītājs (rietumu reģions)</span><span class="sxs-lookup"><span data-stu-id="938d0-130">HR manager (West)</span></span>|<span data-ttu-id="938d0-131">PV vadītājs</span><span class="sxs-lookup"><span data-stu-id="938d0-131">HR manager</span></span>|
|<span data-ttu-id="938d0-132">**Personāla vadība**</span><span class="sxs-lookup"><span data-stu-id="938d0-132">**Human resources**</span></span>|<span data-ttu-id="938d0-133">PV vadītājs (centrālais reģions)</span><span class="sxs-lookup"><span data-stu-id="938d0-133">HR manager (Central)</span></span>|<span data-ttu-id="938d0-134">PV vadītājs</span><span class="sxs-lookup"><span data-stu-id="938d0-134">HR manager</span></span>|


 <a name="departments"></a><span data-ttu-id="938d0-135">Nodaļas</span><span class="sxs-lookup"><span data-stu-id="938d0-135">Departments</span></span>
------------

<span data-ttu-id="938d0-136">Nodaļa ir pārvaldības struktūrvienība, kas atbilst organizācijas kategorijai vai funkcionālajai jomai, kas ir atbildīga par noteiktu organizācijas darbības jomu, piemēram, pārdošanu vai uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="938d0-136">A department is an operating unit that represents a category or functional area of an organization that is responsible for a specific area of the organization, such as sales or accounting.</span></span> <span data-ttu-id="938d0-137">Nodaļa tiek izmantota, lai ziņotu par funkcionālajām jomām, un tā var būt atbildīga par peļņu un zaudējumiem.</span><span class="sxs-lookup"><span data-stu-id="938d0-137">A department is used to report on functional areas and may have profit and loss responsibility.</span></span> <span data-ttu-id="938d0-138">Turklāt nodaļa var ietvert izmaksu centru grupu.</span><span class="sxs-lookup"><span data-stu-id="938d0-138">Also, a department might include a group of cost centers.</span></span> <span data-ttu-id="938d0-139">Organizācijā var būt tādas nodaļas kā, piemēram, pārdošanas, uzskaites un personāla vadības nodaļa.</span><span class="sxs-lookup"><span data-stu-id="938d0-139">Sales, accounting, and human resources are some examples of departments in an organization.</span></span>

## <a name="jobs-and-positions"></a><span data-ttu-id="938d0-140"> Darbi un amati</span><span class="sxs-lookup"><span data-stu-id="938d0-140">Jobs and positions</span></span>
<span data-ttu-id="938d0-141">Darbs ir uzdevumu un atbildības jomu kopums, kas ir jāizpilda personai, kura veic darbu.</span><span class="sxs-lookup"><span data-stu-id="938d0-141">A job is a collection of tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="938d0-142">Pozīcija ir atsevišķa darba instance.</span><span class="sxs-lookup"><span data-stu-id="938d0-142">A position is an individual instance of a job.</span></span> <span data-ttu-id="938d0-143">Darba veikšanai nepieciešamās atbildības jomas, darba uzdevumi, darba funkcijas, iemaņas, izglītības informācija un sertifikāti ir nepieciešami arī amatiem, kas ir saistīti ar šo darbu.</span><span class="sxs-lookup"><span data-stu-id="938d0-143">Areas of responsibility, job tasks, job functions, skills, education information, and certificates that are required for a job are also required for positions that are associated with a job.</span></span>
### <a name="job-tasks"></a><span data-ttu-id="938d0-144">Darba uzdevumi</span><span class="sxs-lookup"><span data-stu-id="938d0-144">Job tasks</span></span>

<span data-ttu-id="938d0-145">Varat izveidot darba uzdevumus, kas atbilst pamata uzdevumiem, kuri ir jāveic darbiniekam, kas ieņem šī darba amatu.</span><span class="sxs-lookup"><span data-stu-id="938d0-145">You can create job tasks that describe the basic tasks that a worker in a position for that job must complete.</span></span> <span data-ttu-id="938d0-146">Vienu darba uzdevumu var pievienot vairākiem darbiem, un šī darba amati pārmanto šos darba uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="938d0-146">The same job task can be added to multiple jobs, and positions for those jobs will inherit those job tasks.</span></span> <span data-ttu-id="938d0-147">Tālāk esošajā tabulā ir norādīti darba uzdevumu piemēri.</span><span class="sxs-lookup"><span data-stu-id="938d0-147">Examples of job tasks are listed in the following table.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="938d0-148">Darbs</span><span class="sxs-lookup"><span data-stu-id="938d0-148">Job</span></span></th>
<th><span data-ttu-id="938d0-149">Darba uzdevums</span><span class="sxs-lookup"><span data-stu-id="938d0-149">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="938d0-150">Pārdošanas daļas vadītājs</span><span class="sxs-lookup"><span data-stu-id="938d0-150">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="938d0-151"><span class="input">Izpildes novērtēšana</span> — novērtēt katra pārdevēja darba izpildi.</span><span class="sxs-lookup"><span data-stu-id="938d0-151"><span class="input">Perf-review</span> – Review each salesperson’s job performance.</span></span></li>
<li><span data-ttu-id="938d0-152"><span class="input">Kavējumu izskatīšana</span> — apstiprināt vai noraidīt katra pārdevēja kavējumu pieprasījumus vai reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="938d0-152"><span class="input">Abs-review</span> – Approve or reject each salesperson’s absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938d0-153">Grāmatvedis</span><span class="sxs-lookup"><span data-stu-id="938d0-153">Accountant</span></span></td>
<td><span data-ttu-id="938d0-154"><span class="input">Finanšu pārskata sniegšana</span> — sniegt iknedēļas finanšu pārskatus finanšu direktoram.</span><span class="sxs-lookup"><span data-stu-id="938d0-154"><span class="input">FIN-Report</span> – Present weekly financial reports to chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

### <a name="job-functions"></a><span data-ttu-id="938d0-155">Darba funkcijas</span><span class="sxs-lookup"><span data-stu-id="938d0-155">Job functions</span></span>

<span data-ttu-id="938d0-156">Darba funkcijas līdzinās darba uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="938d0-156">Job functions are like job tasks.</span></span> <span data-ttu-id="938d0-157">Darba funkcija atbilst vienam vai vairākiem uzdevumiem, pienākumiem vai atbildības jomām, kas ir piešķirti darbam.</span><span class="sxs-lookup"><span data-stu-id="938d0-157">A job function describes one or more tasks, duties or responsibilities that are assigned to a job.</span></span> <span data-ttu-id="938d0-158">Darba funkcijas var piešķirt darbiem un izmantot, lai iestatītu un ieviestu atlīdzības plānu piemērotības noteikumus.</span><span class="sxs-lookup"><span data-stu-id="938d0-158">Job functions can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="938d0-159">Nākamajā tabulā ir norādīti darba funkciju piemēri.</span><span class="sxs-lookup"><span data-stu-id="938d0-159">Examples of job functions are listed in the following table.</span></span>

| <span data-ttu-id="938d0-160">Darbs</span><span class="sxs-lookup"><span data-stu-id="938d0-160">Job</span></span>           | <span data-ttu-id="938d0-161">Darba funkcija</span><span class="sxs-lookup"><span data-stu-id="938d0-161">Job function</span></span>                                                |
|---------------|-------------------------------------------------------------|
| <span data-ttu-id="938d0-162">Pārdošanas daļas vadītājs</span><span class="sxs-lookup"><span data-stu-id="938d0-162">Sales manager</span></span> | <span data-ttu-id="938d0-163">Cilvēku vadība — jums pakļauto cilvēku vadība.</span><span class="sxs-lookup"><span data-stu-id="938d0-163">Mng-people – Manage people who report to you.</span></span>               |
| <span data-ttu-id="938d0-164">Grāmatvedis</span><span class="sxs-lookup"><span data-stu-id="938d0-164">Accountant</span></span>    | <span data-ttu-id="938d0-165">Finanšu datu novērtēšana — uzturēt finanšu datus par kontu kopu.</span><span class="sxs-lookup"><span data-stu-id="938d0-165">FIN-Review – Maintain financial data for a set of accounts.</span></span> |

### <a name="job-types"></a><span data-ttu-id="938d0-166">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="938d0-166">Job types</span></span>

<span data-ttu-id="938d0-167">Izmantojiet darbu tipus, lai klasificētu līdzīgos darbus kategorijās.</span><span class="sxs-lookup"><span data-stu-id="938d0-167">Use job types to classify similar jobs into categories.</span></span> <span data-ttu-id="938d0-168">Darbu tipus, tāpat kā darba funkcijas, var piešķirt darbiem un izmantot, lai iestatītu un ieviestu atlīdzības plānu piemērotības noteikumus.</span><span class="sxs-lookup"><span data-stu-id="938d0-168">Job types, just like job functions, can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="938d0-169">Tālāk esošajā sarakstā ir norādīti daži darbu tipu piemēri.</span><span class="sxs-lookup"><span data-stu-id="938d0-169">Some examples of job types are included in the following list:</span></span>
-   <span data-ttu-id="938d0-170">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="938d0-170">Full-time</span></span>
-   <span data-ttu-id="938d0-171">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="938d0-171">Part-time</span></span>
-   <span data-ttu-id="938d0-172">Alga</span><span class="sxs-lookup"><span data-stu-id="938d0-172">Salary</span></span>
-   <span data-ttu-id="938d0-173">Stundu apmaksa</span><span class="sxs-lookup"><span data-stu-id="938d0-173">Hourly pay</span></span>

### <a name="areas-of-responsibility"></a><span data-ttu-id="938d0-174">Atbildības jomas</span><span class="sxs-lookup"><span data-stu-id="938d0-174">Areas of responsibility</span></span>

<span data-ttu-id="938d0-175">Izmantojiet atbildības jomas, lai norādītu darba lomas, procesus un preces, par ko ir atbildīgs darbinieks, kurš ieņem šī darba amatu.</span><span class="sxs-lookup"><span data-stu-id="938d0-175">Use areas of responsibility to indicate the work roles, processes, and products that a worker in a position for that job would be responsible for.</span></span> <span data-ttu-id="938d0-176">Darbam “Grāmatvedis” var būt tādas atbildības jomas kā, piemēram, “Finanšu pārskatu izveide par preci A”.</span><span class="sxs-lookup"><span data-stu-id="938d0-176">An example of an area of responsibility for a job titled “Accountant” might be “Financial reporting for Product A”.</span></span>

<a name="positions"></a><span data-ttu-id="938d0-177">Amati</span><span class="sxs-lookup"><span data-stu-id="938d0-177">Positions</span></span>
----------

<span data-ttu-id="938d0-178">Amats ir nozīmīgs organizācijas hierarhijas zemāko līmeņu elements.</span><span class="sxs-lookup"><span data-stu-id="938d0-178">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="938d0-179">Pozīcija ir atsevišķa darba instance.</span><span class="sxs-lookup"><span data-stu-id="938d0-179">A position is an individual instance of a job.</span></span> <span data-ttu-id="938d0-180">Piemēram, amats “Pārdošanas daļas vadītājs (austrumu reģions)” ir tikai viens no amatiem, kas ir saistīti ar darbu “Pārdošanas daļas vadītājs”.</span><span class="sxs-lookup"><span data-stu-id="938d0-180">For example, the position, “Sales manager (East),” is just one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="938d0-181">Amati ir ietverti nodaļā un tiek piešķirti darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="938d0-181">Positions exist in a department and are assigned to workers.</span></span>
### <a name="position-creation-and-maintenance"></a><span data-ttu-id="938d0-182">Amata izveide un uzturēšana</span><span class="sxs-lookup"><span data-stu-id="938d0-182">Position creation and maintenance</span></span>

-   <span data-ttu-id="938d0-183">Varat skatīt ar amatu saistīto sistēmas izmaiņu vēsturi viegli pieejamā saraksta lapā.</span><span class="sxs-lookup"><span data-stu-id="938d0-183">You can view a history of position-related system changes in an easy-to-access list page.</span></span>
-   <span data-ttu-id="938d0-184">Varat izveidot iemeslu kodus, ko lietotāji var atlasīt, kad viņi izveido vai modificē amatus.</span><span class="sxs-lookup"><span data-stu-id="938d0-184">You can create reason codes that your users can select when they create or modify positions.</span></span>
-   <span data-ttu-id="938d0-185">Varat izveidot personāla darbību tipus un piešķirt numuru sēriju personāla darbībām.</span><span class="sxs-lookup"><span data-stu-id="938d0-185">You can create personnel action types and assign a number sequence to personnel actions.</span></span>
-   <span data-ttu-id="938d0-186">Varat iestatīt darbplūsmas, lai amatu pievienošanai un izmaiņām būtu nepieciešams apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="938d0-186">You can set up workflow so that position additions and changes can require approval.</span></span>

### <a name="position-duration"></a><span data-ttu-id="938d0-187">Amata ieņemšanas ilgums</span><span class="sxs-lookup"><span data-stu-id="938d0-187">Position duration</span></span>

<span data-ttu-id="938d0-188">Katrs amats ir spēkā noteiktu laika periodu.</span><span class="sxs-lookup"><span data-stu-id="938d0-188">Every position has a length of time that the position is effective.</span></span> <span data-ttu-id="938d0-189">Šis laika periods tiek saukts par ilgumu.</span><span class="sxs-lookup"><span data-stu-id="938d0-189">This length of time is referred to as duration.</span></span> <span data-ttu-id="938d0-190">Piemēram, vasaras amatu ieņemšanas ilgums var būt no 2015. gada 1. maija līdz 2015. gada 31. augustam.</span><span class="sxs-lookup"><span data-stu-id="938d0-190">For example, summer positions might have duration of May 1, 2015 until August 31, 2015.</span></span>

### <a name="worker-assignments"></a><span data-ttu-id="938d0-191">Nodarbināto piešķires</span><span class="sxs-lookup"><span data-stu-id="938d0-191">Worker assignments</span></span>

<span data-ttu-id="938d0-192">Piešķirot darbinieku amatam, šis amats tiek aizņemts.</span><span class="sxs-lookup"><span data-stu-id="938d0-192">When you assign a worker to a position, you fill that position.</span></span> <span data-ttu-id="938d0-193">Varat piešķirt darbiniekus vairākiem amatiem, taču vienam amatam vienlaikus var piešķirt tikai vienu darbinieku.</span><span class="sxs-lookup"><span data-stu-id="938d0-193">You can assign workers to multiple positions, but only one worker can be assigned to a position at the same time.</span></span>

### <a name="reporting-relationships"></a><span data-ttu-id="938d0-194">Pārskata sakarības</span><span class="sxs-lookup"><span data-stu-id="938d0-194">Reporting relationships</span></span>

<span data-ttu-id="938d0-195">Amati ir nozīmīgi organizācijas hierarhijas zemāko līmeņu elementi.</span><span class="sxs-lookup"><span data-stu-id="938d0-195">Positions are important elements of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="938d0-196">Veidlapā Amats varat norādīt amatu, kuram ir pakļauts šis amats.</span><span class="sxs-lookup"><span data-stu-id="938d0-196">In the Position form, you can specify the position that a position reports to.</span></span> <span data-ttu-id="938d0-197">Kad piešķirat darbinieku amatam, kas ir pakļauts citam amatam, tiek izveidotas pakļautības attiecības starp darbiniekiem, kas ir piešķirti šiem diviem amatiem.</span><span class="sxs-lookup"><span data-stu-id="938d0-197">When you assign a worker to a position that reports to another position, you create a reporting relationship between the workers who are assigned to the two positions.</span></span> <span data-ttu-id="938d0-198">Piemēram, amats “Grāmatvedis A” ir pakļauts amatam “Uzskaites supervizors”.</span><span class="sxs-lookup"><span data-stu-id="938d0-198">For example, position “Accountant-A” reports to position “Accounting Supervisor”.</span></span> <span data-ttu-id="938d0-199">Kims Akers ir piešķirts amatam “Uzskaites supervizors”, un Sandžejs Patels ir piešķirts amatam “Grāmatvedis A”.</span><span class="sxs-lookup"><span data-stu-id="938d0-199">Kim Akers is assigned to position “Accounting Supervisor” and Sanjay Patel is assigned to position “Accountant-A”.</span></span> <span data-ttu-id="938d0-200">Tas nozīmē, ka Sandžejs Patels ir pakļauts Kimam Akeram.</span><span class="sxs-lookup"><span data-stu-id="938d0-200">This means that Sanjay Patel reports to Kim Akers.</span></span> 

<span data-ttu-id="938d0-201">Ja jūsu organizācija izmanto matricas hierarhiju vai citu pielāgotu hierarhiju, varat iestatīt amatu hierarhijas tipus un pēc tam pievienot katra iestatītā hierarhijas tipa matiem pakļautības attiecības.</span><span class="sxs-lookup"><span data-stu-id="938d0-201">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span> <span data-ttu-id="938d0-202">Piemēram, Lorija Penora ir uzņēmuma Adventure Works ģenerāldirektore un ir piešķirta amatam “Ģenerāldirektors”.</span><span class="sxs-lookup"><span data-stu-id="938d0-202">For example, Lori Penor is a general manager at Adventure Works and is assigned to the “General Manager” position.</span></span> <span data-ttu-id="938d0-203">Lorija vada logrīku notīrīšanai paredzēta produkta izstrādi.</span><span class="sxs-lookup"><span data-stu-id="938d0-203">Lori manages the development of a product that is used to clean widgets.</span></span> <span data-ttu-id="938d0-204">Lorijai ir nepieciešams grāmatvedis, kas var viņai palīdzēt apstrādāt produkta izstrādes finanšu datus.</span><span class="sxs-lookup"><span data-stu-id="938d0-204">Lori requires an accountant to help her with the finances for developing the product.</span></span> <span data-ttu-id="938d0-205">Tāpēc viņa ir pieņēmusi Sandžeju Patelu kā grāmatvedi.</span><span class="sxs-lookup"><span data-stu-id="938d0-205">Therefore, she has recruited Sanjay Patel to be her accountant.</span></span> <span data-ttu-id="938d0-206">Sandžejs ir tieši pakļauts Kimam Akeram, taču strādā arī kopā ar Loriju Penori, apstrādājot logrīku notīrīšanas produkta izstrādes finanšu datus.</span><span class="sxs-lookup"><span data-stu-id="938d0-206">Sanjay reports directly to Kim Akers, but also works with Lori Penor on his work related to the finances for developing the widget cleaner.</span></span> 

<span data-ttu-id="938d0-207">Iepriekšējā piemērā aprakstītajā situācijā ir jāveic tālāk norādītie uzdevumi, lai iestatītu darba attiecības starp Sandžeju Patelu un Loriju Penori.</span><span class="sxs-lookup"><span data-stu-id="938d0-207">For the previous example, you would complete the following tasks to set up the working relationship between Sanjay Patel and Lori Penor:</span></span>
1.  <span data-ttu-id="938d0-208">Izveidojiet pielāgotu amatu hierarhijas tipu “Logrīks”, lai izveidotu hierarhiju, kurā ir ietverti amati, kas ir saistīti ar logrīku notīrīšanas produkta izstrādi.</span><span class="sxs-lookup"><span data-stu-id="938d0-208">Create a custom position hierarchy type called “Widget” to create a hierarchy that includes positions responsible for working on the widget cleaner product.</span></span>
2.  <span data-ttu-id="938d0-209">Norādiet, ka amats “Grāmatvedis A” ir pakļauts amatam “Ģenerāldirektors” hierarhijā “Logrīks”.</span><span class="sxs-lookup"><span data-stu-id="938d0-209">Assign the General Manager position to be the position that the Accountant-A position reports to in the Widget hierarchy.</span></span>

<span data-ttu-id="938d0-210">Izmantojiet amatu hierarhiju, lai skatītu amatu pakļautības struktūru.</span><span class="sxs-lookup"><span data-stu-id="938d0-210">Use the position hierarchy to view the reporting structure of positions.</span></span> <span data-ttu-id="938d0-211">Ja jums ir vairākas amatu hierarhijas, varat skatīt katra hierarhijas tipa hierarhiju amatu hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="938d0-211">If you have multiple position hierarchies, you can view the hierarchy for each hierarchy type in the position hierarchy.</span></span> <span data-ttu-id="938d0-212">Varat arī meklēt amatu pēc amata ID vai tā darbinieka vārda, kurš ir piešķirts šim amatam.</span><span class="sxs-lookup"><span data-stu-id="938d0-212">Also, you can search for a position by position ID or by the name of the worker who is assigned to the position.</span></span> <span data-ttu-id="938d0-213">Amatu hierarhija ir organizācijas hierarhija.</span><span class="sxs-lookup"><span data-stu-id="938d0-213">The position hierarchy is an organizational hierarchy.</span></span>

## <a name="date-effective-records"></a><span data-ttu-id="938d0-214">Efektīvo ierakstu datums</span><span class="sxs-lookup"><span data-stu-id="938d0-214">Date effective records</span></span>
<span data-ttu-id="938d0-215">Dažiem ierakstiem varat norādīt turpmākās ierakstu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="938d0-215">For some records, you can specify future changes to the record.</span></span> <span data-ttu-id="938d0-216">Tālāk norādītā informācija ir atkarīga no datuma.</span><span class="sxs-lookup"><span data-stu-id="938d0-216">The following information is date effective.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="938d0-217">Ieraksti</span><span class="sxs-lookup"><span data-stu-id="938d0-217">Records</span></span></th>
<th><span data-ttu-id="938d0-218">No datuma atkarīgā informācija</span><span class="sxs-lookup"><span data-stu-id="938d0-218">Date effective information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="938d0-219">Darbi</span><span class="sxs-lookup"><span data-stu-id="938d0-219">Jobs</span></span></td>
<td><ul>
<li><span data-ttu-id="938d0-220">Noteikta detalizētā informācija par darbu</span><span class="sxs-lookup"><span data-stu-id="938d0-220">Some detailed job information</span></span></li>
<li><span data-ttu-id="938d0-221">Darba klasifikācijas informācija</span><span class="sxs-lookup"><span data-stu-id="938d0-221">Job classification information</span></span></li>
<li><span data-ttu-id="938d0-222">Atlīdzības informācija</span><span class="sxs-lookup"><span data-stu-id="938d0-222">Compensation information</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938d0-223">Pozīcijas</span><span class="sxs-lookup"><span data-stu-id="938d0-223">Positions</span></span></td>
<td><ul>
<li><span data-ttu-id="938d0-224">Noteikta detalizētā informācija par amatu</span><span class="sxs-lookup"><span data-stu-id="938d0-224">Some detailed position information</span></span></li>
<li><span data-ttu-id="938d0-225">Darbinieku piešķires</span><span class="sxs-lookup"><span data-stu-id="938d0-225">Worker assignments</span></span></li>
<li><span data-ttu-id="938d0-226">Amatu ieņemšanas ilgumi</span><span class="sxs-lookup"><span data-stu-id="938d0-226">Position durations</span></span></li>
<li><span data-ttu-id="938d0-227">Pozīciju hierarhijas</span><span class="sxs-lookup"><span data-stu-id="938d0-227">Position hierarchies</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="938d0-228">Varat modificēt iepriekš esošajā tabulā ietverto informāciju par amatu vai darbu un norādīt datumu, kas amata vai darba izmaiņām ir jāstājas spēkā.</span><span class="sxs-lookup"><span data-stu-id="938d0-228">You can modify the information mentioned in the previous table for a position or a job and specify a date when the modifications to the position or job should take effect.</span></span> <span data-ttu-id="938d0-229">Piemēram, amatu var piešķirt tikai vienam darbiniekam, taču Sandžejs Patels, kurš ir piešķirts amatam “Grāmatvedis A”, aizies no darba pēc divām nedēļām.</span><span class="sxs-lookup"><span data-stu-id="938d0-229">For example, a position can only be assigned to one worker, but Sanjay Patel, who is assigned to the position Accountant-A, will be leaving in two weeks.</span></span> <span data-ttu-id="938d0-230">Pēc tam Sandžeja Patelu aizstās Džo Hīlijs.</span><span class="sxs-lookup"><span data-stu-id="938d0-230">Joe Healy will replace Sanjay Patel when he leaves.</span></span> <span data-ttu-id="938d0-231">Lai gan Sandžejs joprojām ir piešķirts savam amatam, varat piešķirt šim amatam arī Džo Hīliju tā, lai šī piešķire stātos spēkā tikai pēc Sandžeja pēdējās darba dienas.</span><span class="sxs-lookup"><span data-stu-id="938d0-231">Even though Sanjay is still assigned to his position, you can assign Joe Healy to the same position so that the assignment is effective only after Sanjay’s last day.</span></span>





