---
title: Kavējuma reģistrēšana sadaļā Laiks un apmeklētība
description: Šajā tēmā ir paskaidros, kā reģistrēt kavējumu sadaļā Laiks un apmeklētība.
author: johanhoffmann
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ef244d5abf762bcaab426cf1cefb232383a8109
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549294"
---
# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="e9fb9-103">Kavējuma reģistrēšana sadaļā Laiks un apmeklētība</span><span class="sxs-lookup"><span data-stu-id="e9fb9-103">Absence registration in Time and attendance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9fb9-104">Šajā tēmā ir aprakstīti kavējuma jēdzieni un ir paskaidrots, kā reģistrēt kavējumu sadaļā Laiks un apmeklētība.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="e9fb9-105">Kavējums, pamatojoties uz parasto darba laiku</span><span class="sxs-lookup"><span data-stu-id="e9fb9-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="e9fb9-106">Par nodarbinātā kavējumu tiek uzskatīts viss laiks, ko nodarbinātais nestrādā savā parastajā darba laikā.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="e9fb9-107">Parastais darba laiks ir definēts nodarbinātā standarta laika profilā.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="e9fb9-108">Piemēram, nodarbinātais strādā atbilstoši dienas profilam ar ierašanās laiku plkst. 7:00 un aiziešanas laiku plkst. 15:00.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="e9fb9-109">Ja nodarbinātais ierodas plkst. 9:00, tiek uzskatīts, ka viņš šajā dienā ir kavējis darbu no plkst. 7:00 līdz plkst. 9:00.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="e9fb9-110">Šādā gadījumā noradinātajam tiek prasīts ievadīt kavējuma iemeslu.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="e9fb9-111">Viņi var norādīt iemeslu, atlasot kavējuma kodu.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="e9fb9-112">Kavējumu kodi</span><span class="sxs-lookup"><span data-stu-id="e9fb9-112">Absence codes</span></span>

<span data-ttu-id="e9fb9-113">Kavējumu kodi atbilst dažādajiem kavējumu veidiem.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="e9fb9-114">Kavējumu kodus definē uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="e9fb9-115">Kavējumu kodiem var lietot dažādas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="e9fb9-116">Piemēram, kavējuma kodu var konfigurēt tā, lai samazinātu vai palielinātu algu.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="e9fb9-117">Piemēram, uzņēmums definē kavējuma kodu **Vēlu**, ko nodarbinātie izmanto, ja ir ieradušies vēlu bez pamatota iemesla.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="e9fb9-118">Uzņēmums definē arī kavējuma kodu **Iekšējais mācību kurss**, ko nodarbinātie izmanto, lai reģistrētu laiku, ko viņi ir patērējuši iekšējo mācību kursu apmeklējumam.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="e9fb9-119">Šos kavējumu kodus var iestatīt tā, lai kods **Vēlu** izraisītu nodarbinātā algas samazināšanu, bet kods **Iekšējais mācību kurss** neizraisītu nodarbinātā algas samazināšanu.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="e9fb9-120">Varat iestatīt automātiskus kavējumu kodus.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="e9fb9-121">Šos kavējumu kodus var izmantot, lai aprēķinātu nodarbinātā darba laiku, kad nav reģistrēti kavējumi.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="e9fb9-122">No nodarbinātā laika profila ir atkarīgs tas, vai tiek lietots standarta laika vai brīvā režīma kavējuma kods.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="e9fb9-123">Standarta laika un brīvā režīma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e9fb9-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="e9fb9-124">Konfigurējiet standarta laika un brīvā režīma parametrus, izmantojot opcijas **Automātiski ievietot kavējumu** un **Automātiski ievieto brīvo režīmu-** lapā **Laika un apmeklētības parametri**.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="e9fb9-125">Kavējumu grupas</span><span class="sxs-lookup"><span data-stu-id="e9fb9-125">Absence groups</span></span>

<span data-ttu-id="e9fb9-126">Kavējumi kodi tiek grupēti kavējumu grupās.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="e9fb9-127">Izmantojot kavējumu grupas, varat grupēt kavējumu kodus, kam ir kopīgas īpašības.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="e9fb9-128">Piemēram, kavējuma kodus, kas ir saistīti ar atļautiem kavējumiem vai kavējumiem ārsta apmeklējuma, zvērinātā pienākumu vai bērna saslimšanas dēļ.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="e9fb9-129">Plānotā prombūtne</span><span class="sxs-lookup"><span data-stu-id="e9fb9-129">Planned absence</span></span>

<span data-ttu-id="e9fb9-130">Ja zināt, ka nodarbinātais kavēs darbu noteiktu laika periodu, piemēram, gaidāma atvaļinājuma dēļ, varat izmantot plānotu kavējumu.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="e9fb9-131">Plānotu kavējumu var iestatīt, konfigurējot kavējuma kodu tā, lai tiktu ņemts vērā plānotais kavējums.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="e9fb9-132">Ja esat iestatījis plānotu kavējumu, kavējuma periodā netiek prasīts ievadīt kavējuma kodu, kad tiek aprēķinātas lietotāja laika reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="e9fb9-133">Varat definēt viena nodarbinātā plānotu kavējumu vai pakešuzdevumu, lai atjaunotu plānotos kavējumu vairākiem nodarbinātajiem vienlaikus.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="e9fb9-134">Plānota kavējuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e9fb9-134">Set up planned absence</span></span>

1. <span data-ttu-id="e9fb9-135">Atlasiet **Personāla vadība** &gt; **Nodarbinātie** &gt; **Darbinieki** un atlasiet darbinieku.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="e9fb9-136">Atlasiet **Laiks** &gt; **Laika piešķires** &gt; **Kavējuma laika reģistrācija** un iestatiet plānoto kavējumu.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="e9fb9-137">Pārtraukts plānotais kavējums</span><span class="sxs-lookup"><span data-stu-id="e9fb9-137">Interrupted planned absence</span></span>

<span data-ttu-id="e9fb9-138">Ja, iestatot plānotu kavējumu, izmantojat opciju **Pārtraukt**, plānotais kavējums tiek pārtraukts gadījumā, ja nodarbinātais pierakstās plānotā kavējuma perioda laikā.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="e9fb9-139">Plānotais kavējums tiek apzīmēts kā **Pārtraukts** un neietekmē turpmākos aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="e9fb9-140">Pārtraucama plānota kavējuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e9fb9-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="e9fb9-141">Atveriet lapu **Kavējuma laika reģistrācija**, kā tas ir norādīts plānota kavējuma iestatīšanas procedūras aprakstā.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="e9fb9-142">Atlasiet **Pārtraukt**.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-142">Select **Interrupt**.</span></span>

<span data-ttu-id="e9fb9-143">Opcija **Pārtraukt** tiek lietota, ja ražotnes terminālī vai ražotnes ierīcē tiek reģistrēts laiks.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="e9fb9-144">Šī opcija netiek lietota, ja reģistrācija tiek veikta aprēķina un apstiprinājuma lapās vai lapā **Elektroniskā darba laika uzskaites karte**.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="e9fb9-145">Piemēri kavējumu lietošanai brīvā režīma profilā</span><span class="sxs-lookup"><span data-stu-id="e9fb9-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="e9fb9-146">Tālāk ir sniegti trīs piemēri tam, kā kavējumi tiek aprēķināti profilā, kam ir iestatīti brīvā grafika periodi.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="e9fb9-147">Piemēros ir izmantots tālāk norādītais profils.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-147">The examples use the following profile.</span></span>

| <span data-ttu-id="e9fb9-148">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="e9fb9-148">Clock-in</span></span> | <span data-ttu-id="e9fb9-149">Standarta laiks</span><span class="sxs-lookup"><span data-stu-id="e9fb9-149">Standard time</span></span>    | <span data-ttu-id="e9fb9-150">Pārtraukums</span><span class="sxs-lookup"><span data-stu-id="e9fb9-150">Break</span></span>             | <span data-ttu-id="e9fb9-151">Standarta laiks</span><span class="sxs-lookup"><span data-stu-id="e9fb9-151">Standard time</span></span> | <span data-ttu-id="e9fb9-152">Brīvais režīms-</span><span class="sxs-lookup"><span data-stu-id="e9fb9-152">Flex-</span></span>        | <span data-ttu-id="e9fb9-153">Aiziešana</span><span class="sxs-lookup"><span data-stu-id="e9fb9-153">Clock-out</span></span> | <span data-ttu-id="e9fb9-154">Brīvais režīms +</span><span class="sxs-lookup"><span data-stu-id="e9fb9-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="e9fb9-155">8:00</span><span class="sxs-lookup"><span data-stu-id="e9fb9-155">8 AM</span></span>     | <span data-ttu-id="e9fb9-156">No 9:00 līdz 11:30</span><span class="sxs-lookup"><span data-stu-id="e9fb9-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="e9fb9-157">No 11:30 līdz 12:00</span><span class="sxs-lookup"><span data-stu-id="e9fb9-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="e9fb9-158">No 12:00 līdz 15:00</span><span class="sxs-lookup"><span data-stu-id="e9fb9-158">12 PM to 3 PM</span></span> | <span data-ttu-id="e9fb9-159">No 15:00 līdz 16:00</span><span class="sxs-lookup"><span data-stu-id="e9fb9-159">3 PM to 4 PM</span></span> | <span data-ttu-id="e9fb9-160">16:00</span><span class="sxs-lookup"><span data-stu-id="e9fb9-160">4 PM</span></span>      | <span data-ttu-id="e9fb9-161">No 16:00 līdz 18:00</span><span class="sxs-lookup"><span data-stu-id="e9fb9-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="e9fb9-162">1. piemērs: izrakstīšanās brīvā režīma- periodā</span><span class="sxs-lookup"><span data-stu-id="e9fb9-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="e9fb9-163">Nodarbinātais ierodas darbā plkst. 8:00 un aiziet plkst. 15:30.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="e9fb9-164">Šāda gadījumā netiek aprēķināts kavējums un no nodarbinātā brīvā režīma bilances tiek noņemta pusstunda, jo nodarbinātais ir aizgājis brīvā režīma- periodā.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="e9fb9-165">2. piemērs: izrakstīšanās standarta laika periodā</span><span class="sxs-lookup"><span data-stu-id="e9fb9-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="e9fb9-166">Nodarbinātais ierodas darbā plkst. 8:00 un aiziet plkst. 14:30.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="e9fb9-167">Šādā gadījumā tiek aprēķināts kavējums no plkst. 14:30 līdz plkst. 16:00 un tiek reģistrēts 1,5 stundas ilgs kavējuma periods, jo nodarbinātais ir aizgājis standarta laika periodā.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="e9fb9-168">Šim periodam ir jānorāda kavējuma kods.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="e9fb9-169">3. piemērs: izrakstīšanās brīvā režīma+ periodā</span><span class="sxs-lookup"><span data-stu-id="e9fb9-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="e9fb9-170">Nodarbinātais ierodas darbā plkst. 8:00 un aiziet plkst. 16:30.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="e9fb9-171">Šāda gadījumā netiek aprēķināts kavējums un nodarbinātā brīvā režīma bilancei tiek pievienota pusstunda, jo nodarbinātais ir aizgājis brīvā režīma+ periodā.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="e9fb9-172">Darbs ar kavējumiem aprēķināšanas un apstiprināšanas procesa laikā</span><span class="sxs-lookup"><span data-stu-id="e9fb9-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="e9fb9-173">Darbinieku laika reģistrācijas ir jāaprēķina un jāapstiprina, pirms tās var pārsūtīt uz algu sistēmu kā apmaksas elementus.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="e9fb9-174">Apstiprinātājs var mainīt nodarbinātā laika reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="e9fb9-175">Apstiprinātājs var pat mainīt jebkuru nodarbinātā reģistrēto kavējumu.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="e9fb9-176">Ja apstiprinātājs manuāli ievada laika periodu ar kavējuma kodu, šī perioda kavējuma kods netiek aizstāts ar noklusējuma apmeklējuma kodu, kas ir norādīts sadaļā Laika un apmeklētības parametri.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="e9fb9-177">Piemēram, nodarbinātā ierodas darbā plkst. 10:00 un atlasa kavējuma kodu, kas norāda, ka viņa ir ieradusies vēlu.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="e9fb9-178">Vēlāk darbiniece informē vadītāju, ka laikā no plkst. 8:00 līdz plkst. 10:00 viņa apmeklēja ārstu.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="e9fb9-179">Ārsta apmeklējums nedrīkst izraisīt nodarbinātās algas samazināšanu.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="e9fb9-180">Tāpēc šajā gadījumā vadītājs var pielāgot divas kavējuma stundas no plkst. 8:00 līdz plkst. 10:00, šīm divām stundām manuāli ievadot kavējuma kodu, kas norāda saslimšanu.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="e9fb9-181">Kavējuma aprēķināšana un apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="e9fb9-181">Calculate and approve absence</span></span>

- <span data-ttu-id="e9fb9-182">Atlasiet **Apmeklētības laiks** &gt; **Pārskatīt un apstiprināt** &gt; **Apstiprināt vai aprēķināt**.</span><span class="sxs-lookup"><span data-stu-id="e9fb9-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>
