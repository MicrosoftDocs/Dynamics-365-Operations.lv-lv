---
title: Atlīdzības plāni
description: Atlīdzību un atvieglojumu vadītāji atlīdzību pārvaldību var izmantot, lai organizācijas darbiniekiem uzturētu un apstrādātu fiksētās un mainīgās atlīdzības sistēmas.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 12b7cdef75e9777b895d429e1e185f8654e67890
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/19/2019
ms.locfileid: "856949"
---
# <a name="compensation-plans"></a><span data-ttu-id="ee7ea-103">Atlīdzības plāni</span><span class="sxs-lookup"><span data-stu-id="ee7ea-103">Compensation plans</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ee7ea-104">Atlīdzību un atvieglojumu vadītāji atlīdzību pārvaldību var izmantot, lai organizācijas darbiniekiem uzturētu un apstrādātu fiksētās un mainīgās atlīdzības sistēmas.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="ee7ea-105">Ievads</span><span class="sxs-lookup"><span data-stu-id="ee7ea-105">Introduction</span></span>

<span data-ttu-id="ee7ea-106">Atlīdzību pārvaldība tiek izmantota, lai kontrolētu pamatalgas un prēmiju izsniegšanu.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="ee7ea-107">Darbinieka fiksētā pamatalga un nopelnu palielinājumi tiek kontrolēti, izmantojot fiksētas atlīdzības plānus.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="ee7ea-108">Veicināšanas maksājumu izsniegšana, piemēram, prēmiju maksājumi, apbalvojumi par sasniegumiem, uzņēmuma akciju iegādes iespējas un dotācijas, kā arī vienreizējas piemaksas, tiek kontrolētas ar mainīgās atlīdzības plāniem.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="ee7ea-109">Darbinieki var būt reģistrēti vienā vai vairākos abu veidu plānos.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="ee7ea-110">Lai būtu piemērots reģistrācijai kādā atlīdzības plānā, darbiniekam ir jāatbilst tālāk norādītajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="ee7ea-111">Darbiniekam ir nepieciešama aktīva amata piešķire.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="ee7ea-112">Darbiniekam ir nepieciešams atbilst kritērijiem, kas atlīdzības plānam ir definēti ar piemērotības nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="ee7ea-113">Atlīdzības iestatīšana</span><span class="sxs-lookup"><span data-stu-id="ee7ea-113">Compensation setup</span></span>
<span data-ttu-id="ee7ea-114">Nākamajā tabulā ir uzskaitīti atlīdzības procesa komponenti, kas var būt būtiski jūsu uzņēmuma atlīdzības plānu iestatīšanai.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ee7ea-115">Komponents</span><span class="sxs-lookup"><span data-stu-id="ee7ea-115">Component</span></span></th>
<th><span data-ttu-id="ee7ea-116">Papildinformācija...</span><span class="sxs-lookup"><span data-stu-id="ee7ea-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee7ea-117">Fiksētās atlīdzības darbības</span><span class="sxs-lookup"><span data-stu-id="ee7ea-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="ee7ea-118">Ar fiksētājām atlīdzības darbībām tiek sasniegti divi mērķi:</span><span class="sxs-lookup"><span data-stu-id="ee7ea-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="ee7ea-119">Darbības var norādīt, kāda informācija ir jāreģistrē, kad mainās darbinieka atlīdzība.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="ee7ea-120">Piemēram, varat pieprasīt, lai tiktu reģistrēts izmaiņu iemesls, piemēram, paaugstināšana vai pazemināšana amatā.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="ee7ea-121">Darbības var nodrošināt, ka fiksētās atlīdzības plānu apstrādāšanas laikā tiek lietots kāds aprēķins.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="ee7ea-122">Piemēram, izpildot tipa Kapitāls darbības, darbinieku alga tiek salīdzināta ar darbinieka līmeņa minimālo atsauces punktu un tiek nodrošināts, ka darbiniekam tiek samaksāta vismaz minimālā summa.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee&#39;s and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee7ea-123">Līmeņi</span><span class="sxs-lookup"><span data-stu-id="ee7ea-123">Levels</span></span></td>
<td><span data-ttu-id="ee7ea-124">Līmeņi ir saistīti ar darbiem un jebkuriem amatiem, kas ir saistīti ar darba atsauci.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="ee7ea-125">Varat izveidot atsevišķus līmeņus trīs atlīdzības plānu tipiem: Kategorija, Josla un Pakāpe.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee7ea-126">Diapazona lietojuma matrica</span><span class="sxs-lookup"><span data-stu-id="ee7ea-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="ee7ea-127">Diapazona lietojuma matrica jums palīdz pārcelt darbiniekus uz kontrolpunktu viņu darbiem.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="ee7ea-128">Varat izmantot diapazona lietojumu arī apmaksas likmes kapitāla kontrolei uzņēmumā, neņemot vērā atsevišķa darbinieka veiktspēju vai kopējo uzņēmuma veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee&#39;s performance or the overall performance of the company.</span></span> <span data-ttu-id="ee7ea-129">Piemēram, darbinieki, kas savā diapazonā ir zemāk apmaksāti, saņem lielāku procentuālo pieaugumu nekā darbinieki, kas savā diapazonā ir augstāk apmaksāti.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="ee7ea-130">Šādi varat sistemātiski nobīdīt kapitāla atšķirības.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="ee7ea-131">Diapazona lietojums tiek aprēķināts šādi: (Fiksēta apmaksas likme - Diapazona minimums) ÷ (Diapazona maksimums - Diapazona minimums).</span><span class="sxs-lookup"><span data-stu-id="ee7ea-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee7ea-132">Atsauces punkta iestatījumi</span><span class="sxs-lookup"><span data-stu-id="ee7ea-132">Reference point setups</span></span></td>
<td><span data-ttu-id="ee7ea-133">Atsauces punkta iestatījumi ietver atsauces punktu kopu, kuri veido matricas diapazonus.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="ee7ea-134">Katru diapazonu var saistīt ar kādu apmaksas likmi.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="ee7ea-135">Piemēram, kategoriju plāniem bieži vien ir atsauces punkti Minimums, Viduspunkts un Maksimums.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee7ea-136">Atlīdzības matrica</span><span class="sxs-lookup"><span data-stu-id="ee7ea-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="ee7ea-137">Atlīdzības matrica ir atsauces punktu un līmeņu kopa, ko izmantojat, lai veidotu atlīdzību struktūru.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee7ea-138">Atlīdzības struktūra</span><span class="sxs-lookup"><span data-stu-id="ee7ea-138">Compensation structure</span></span></td>
<td><span data-ttu-id="ee7ea-139">Atlīdzības struktūra ir atlīdzības matrica, kurā apmaksas likmes katram līmenim ir saistītas ar atsauces punktiem.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee7ea-140">Piemērotības nosacījumi</span><span class="sxs-lookup"><span data-stu-id="ee7ea-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="ee7ea-141">Piemērotības nosacījumi tiek izmantoti, lai identificētu darbiniekus konkrētos darbos, darbu funkcijās, darbu tipos, departamentos, arodbiedrībās vai atlīdzību reģionos, uz kuriem attiecas noteikti atlīdzību plāni.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="ee7ea-142">Lai darbiniekus reģistrētu plānā, jums ir jāizveido piemērotības nosacījumi gan mainīgās, gan fiksētās atlīdzības plāniem.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="ee7ea-143">Kad atlīdzības plānam ir norādīti piemērotības nosacījumi, varat definēt līmeņus, kas ir jālieto attiecībā uz šajā plāna ietvertajiem darbiem.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee7ea-144">Algas izmaksas biežums</span><span class="sxs-lookup"><span data-stu-id="ee7ea-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="ee7ea-145">Algas izmaksas biežums tiek lietots, lai definētu laika periodu, kādam ir norādīta atlīdzība.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="ee7ea-146">Algas izmaksas biežums jums palīdz saprast, piemēram, vai atlīdzības summa ir norādīta kā gada alga vai kā stundas apmaksas likme.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="ee7ea-147">Algas izmaksas biežums tiek arī lietots, lai iestatītu pārveidošanas koeficientus un atlīdzības summu no algas izmaksas biežuma reizi mēnesī, reizi nedēļā, divreiz nedēļā un reizi stundā varētu konvertēt uz gada algas izmaksas biežumu.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee7ea-148">Atlīdzības reģioni</span><span class="sxs-lookup"><span data-stu-id="ee7ea-148">Compensation regions</span></span></td>
<td><span data-ttu-id="ee7ea-149">Atlīdzības reģioni tiek lietoti, lai darbinieka atlīdzību norādītu, pamatojoties uz darbvietas atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee7ea-150">Kontrolpunkts</span><span class="sxs-lookup"><span data-stu-id="ee7ea-150">Control point</span></span></td>
<td><span data-ttu-id="ee7ea-151">Kontrolpunkts nosaka, ko jūs uzskatāt par ideālu apmaksas likmi visiem darbiniekiem kādā atlīdzības līmenī.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="ee7ea-152">Kategoriju plāna struktūrām kontrolpunkti parasti ir diapazona viduspunkts.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="ee7ea-153">Joslu struktūrās kontrolpunkti tiek izmantoti reti.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-153">Band structures rarely use control points.</span></span> <span data-ttu-id="ee7ea-154">Fiksētas atlīdzības plānam kontrolpunktu varat norādīt formā Fiksētas atlīdzības plāni.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee7ea-155">Darba funkcijas</span><span class="sxs-lookup"><span data-stu-id="ee7ea-155">Job functions</span></span></td>
<td><span data-ttu-id="ee7ea-156">Darba funkcijas tiek izmantotas, lai atlīdzību plānus klasificētu un filtrētu specifiskiem darbiem.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee7ea-157">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="ee7ea-157">Job types</span></span></td>
<td><span data-ttu-id="ee7ea-158">Darba tipi tiek izmantoti, lai atlīdzību plānus klasificētu un filtrētu specifiskiem darbiem.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee7ea-159">Mainīgas atlīdzības tipi</span><span class="sxs-lookup"><span data-stu-id="ee7ea-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="ee7ea-160">Mainīgas atlīdzības plānos tiek iestatīti mainīgas atlīdzības tipi, piemēram, akciju prēmijas vai skaidras naudas prēmijas.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee7ea-161">Atlīdzību režģi</span><span class="sxs-lookup"><span data-stu-id="ee7ea-161">Compensation grids</span></span></td>
<td><span data-ttu-id="ee7ea-162">Atlīdzību režģi ietver atlīdzību struktūru.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="ee7ea-163">Atlīdzību režģus var izmantot ar vienu vai vairākiem atlīdzības plāniem.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee7ea-164">Veiktspējas plāni</span><span class="sxs-lookup"><span data-stu-id="ee7ea-164">Performance plans</span></span></td>
<td><span data-ttu-id="ee7ea-165">Veiktspējas plāni tiek lietoti, lai veiktspēju saistītu ar sadalījumu matricu, tādējādi plānu varētu izmantot stratēģijai Samaksa par rezultātu.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee7ea-166">Veiktspējas vērtējumi</span><span class="sxs-lookup"><span data-stu-id="ee7ea-166">Performance ratings</span></span></td>
<td><span data-ttu-id="ee7ea-167">Veiktspējas vērtējumi tiek izmantoti veiktspējas plānos, lai noteiktu nopelnu piemaksas vai veiktspējas piemaksas apjomu.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="ee7ea-168">Apstrādes notikumi</span><span class="sxs-lookup"><span data-stu-id="ee7ea-168">Process events</span></span>
<span data-ttu-id="ee7ea-169">Procesa notikums aprēķina atlīdzības informāciju noteiktam periodam visiem darbiniekiem, kas ir reģistrēti vienā vai vairākos fiksētās vai mainīgās atlīdzības plānos.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="ee7ea-170">Procesa notikumu varat palaist atkārtoti, lai pārbaudītu vai atjauninātu aprēķinātos atlīdzības rezultātus.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="ee7ea-171">Atlīdzības notikumi</span><span class="sxs-lookup"><span data-stu-id="ee7ea-171">Compensation events</span></span>
-------------------

<span data-ttu-id="ee7ea-172">Katru reizi, kad tiek palaists procesa notikums, tiek izveidots atlīdzības notikums.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="ee7ea-173">Atlīdzības notikumi ietver atlīdzības procesa rezultātus katram darbiniekam, kas ir iekļauts attiecīgajā procesa notikumā.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="ee7ea-174">Kad šie aprēķini ir pareizi, varat ielādēt atlīdzības notikumu, lai atjauninātu atlīdzības ierakstus tiem darbiniekiem, kurus šis procesa notikums ietekmē.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="ee7ea-175">Ieteikumi</span><span class="sxs-lookup"><span data-stu-id="ee7ea-175">Recommendations</span></span>
<span data-ttu-id="ee7ea-176">Pēc procesa notikuma palaišanas varat ieteikt korekcijas darbinieka nopelnu palielinājumam vai piemaksas summai, pamatojoties uz procesa notikuma aprēķinātajām vadlīnijām.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="ee7ea-177">Lai darbiniekiem sniegtu ieteikumus, ieteikumi ir jāiespējo, kad iestatāt atlīdzību plānus vai kad iestatāt procesa notikumu.</span><span class="sxs-lookup"><span data-stu-id="ee7ea-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>



