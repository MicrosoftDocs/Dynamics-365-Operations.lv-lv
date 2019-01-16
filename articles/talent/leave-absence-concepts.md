---
title: "Atvaļinājumu un kavējumu jēdzieni"
description: "Šajā tēmā ir aprakstīti atvaļinājumu un kavējumu jēdzieni un brīvā laika bilanču noteikšanas principi."
author: jcart
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: a388e0efe6c19a3aabe04e7fff039ce11ae023c4
ms.openlocfilehash: 563593d6c93b0488c681f5b43004f5c0d22cc004
ms.contentlocale: lv-lv
ms.lasthandoff: 01/07/2019

---

# <a name="leave-and-absence-concepts"></a><span data-ttu-id="bfa1d-103">Atvaļinājumu un kavējumu jēdzieni</span><span class="sxs-lookup"><span data-stu-id="bfa1d-103">Leave and absence concepts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bfa1d-104">Jēdzieni un noteikumi, kas ir aprakstīti šajā tēmā, var palīdzēt noteikt, kā darbiniekam tiek piešķirts brīvais laiks un kā tiek aprēķinātas šī darbinieka laika bilances.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="bfa1d-105">Papildinformāciju par atvaļinājumu un kavējumu pārvaldību skatiet tēmā [Atvaļinājumu un kavējumu pārvaldība](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span><span class="sxs-lookup"><span data-stu-id="bfa1d-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="bfa1d-106">Detalizēta informācija par atvaļinājuma plānu</span><span class="sxs-lookup"><span data-stu-id="bfa1d-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="bfa1d-107">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-107">Start date</span></span>

<span data-ttu-id="bfa1d-108">Sākuma datums ir datums, kurā sākas uzkrājumu apstrāde.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="bfa1d-109">Sākuma datums ir arī gadadienas datums, ko izmanto, lai aprēķinātu pārnestās summas.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="bfa1d-110">Uzkrājumi</span><span class="sxs-lookup"><span data-stu-id="bfa1d-110">Accruals</span></span>

<span data-ttu-id="bfa1d-111">Uzkrājumi nosaka, kad un cik bieži darbiniekam tiek piešķirts brīvais laiks.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="bfa1d-112">Uzkrājumu piešķiršanas politika un proporcionalitātes politika tiek definēta sadaļā **Uzkrājumi**, kad iestatāt atvaļinājuma un kavējuma plānu.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="bfa1d-113">Uzkrāšanas biežums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-113">Accrual frequency</span></span>

<span data-ttu-id="bfa1d-114">Uzkrāšanas biežums nosaka, cik bieži atvaļinājums tiek uzkrāts vai piešķirts.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="bfa1d-115">Ir pieejamas tālāk minētās opcijas.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-115">The following options are available:</span></span>

- <span data-ttu-id="bfa1d-116">Ikdienas</span><span class="sxs-lookup"><span data-stu-id="bfa1d-116">Daily</span></span>
- <span data-ttu-id="bfa1d-117">Iknedēļas</span><span class="sxs-lookup"><span data-stu-id="bfa1d-117">Weekly</span></span>
- <span data-ttu-id="bfa1d-118">Katru otro nedēļu</span><span class="sxs-lookup"><span data-stu-id="bfa1d-118">Biweekly</span></span>
- <span data-ttu-id="bfa1d-119">Pusmēneša</span><span class="sxs-lookup"><span data-stu-id="bfa1d-119">Semimonthly</span></span>
- <span data-ttu-id="bfa1d-120">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="bfa1d-120">Monthly</span></span>
- <span data-ttu-id="bfa1d-121">Ceturkšņa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-121">Quarterly</span></span>
- <span data-ttu-id="bfa1d-122">Divreiz gadā</span><span class="sxs-lookup"><span data-stu-id="bfa1d-122">Semiannually</span></span>
- <span data-ttu-id="bfa1d-123">Reizi gadā</span><span class="sxs-lookup"><span data-stu-id="bfa1d-123">Annually</span></span>
- <span data-ttu-id="bfa1d-124">Neviens</span><span class="sxs-lookup"><span data-stu-id="bfa1d-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="bfa1d-125">Uzkrāšanas perioda kritērijs</span><span class="sxs-lookup"><span data-stu-id="bfa1d-125">Accrual period basis</span></span>

<span data-ttu-id="bfa1d-126">Uzkrāšanas perioda kritērijs nosaka datumu, kas tiek izmantots, lai aprēķinātu uzkrāšanas periodu.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="bfa1d-127">Ir pieejamas tālāk minētās opcijas.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-127">The following options are available:</span></span>

- <span data-ttu-id="bfa1d-128">**Plāna sākuma datums**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-128">**Plan start date**</span></span>
- <span data-ttu-id="bfa1d-129">**Darbiniekam noteikts datums** — ja ir atlasīta šī opcija, vērtība nosaka sākotnējā datuma vērtības avotu, kas tiek izmantots, lai aprēķinātu uzkrāšanas periodus.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="bfa1d-130">Ir pieejamas tālāk minētās opcijas.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-130">The following options are available:</span></span>

    - <span data-ttu-id="bfa1d-131">Pielāgot</span><span class="sxs-lookup"><span data-stu-id="bfa1d-131">Custom</span></span>
    - <span data-ttu-id="bfa1d-132">Gadadienas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-132">Anniversary date</span></span>
    - <span data-ttu-id="bfa1d-133">Sākotnējais darbā pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-133">Original hire date</span></span>
    - <span data-ttu-id="bfa1d-134">Darba stāža datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-134">Seniority date</span></span>
    - <span data-ttu-id="bfa1d-135">Nodarbinātā koriģētais pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="bfa1d-136">Nodarbinātā pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="bfa1d-137">Uzkrājuma piešķiršanas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-137">Accrual award date</span></span>

<span data-ttu-id="bfa1d-138">Uzkrājuma piešķiršanas datums nosaka, kad darbiniekam tiek piešķirts brīvais laiks.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="bfa1d-139">Ir pieejamas tālāk minētās opcijas.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-139">The following options are available:</span></span>

- <span data-ttu-id="bfa1d-140">**Uzkrāšanas perioda beigu datums** — darbiniekam brīvais laiks tiks piešķirts piešķiršanas perioda pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="bfa1d-141">Lai uzkrātu pareizu summu, uzkrāšanas procesā ir jāiekļauj viss periods.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="bfa1d-142">Piemēram, uzkrāšanas periods ir no 2018. gada 1. janvāra līdz 2018. gada 31. janvārim.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="bfa1d-143">Šajā gadījumā, lai janvāris tiktu iekļauts periodā, uzkrāšanas beigu datumam ir jābūt 2018. gada 1. februārī.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="bfa1d-144">**Uzkrāšanas perioda sākuma datums** — darbiniekam brīvais laiks tiks piešķirts piešķiršanas perioda pirmajā dienā.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="bfa1d-145">Uzkrājuma politika reģistrācijas gadījumā</span><span class="sxs-lookup"><span data-stu-id="bfa1d-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="bfa1d-146">Uzkrājuma politika reģistrācijas gadījumā nosaka, kā tiek aprēķināts uzkrājums, kad darbinieks ir reģistrēts uzkrāšanas perioda vidū.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="bfa1d-147">Ir pieejamas tālāk minētās opcijas.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-147">The following options are available:</span></span>

- <span data-ttu-id="bfa1d-148">**Proporcionāli sadalīts** — lai noteiktu starpību dienās, tiek izmantots datumu diapazons starp reģistrācijas datumu un sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="bfa1d-149">Šī starpība tiek piemērota, kad uzkrājumi tiek apstrādāti.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="bfa1d-150">**Pilns uzkrājums** — pirmās uzkrājumu apstrādes laikā tiek piešķirta pilna uzkrājuma summa atbilstoši pakāpei.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="bfa1d-151">**Nav uzkrājuma** — līdz nākamajam uzkrāšanas periodam netiek piešķirts uzkrājums.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="bfa1d-152">Uzkrājuma politika reģistrācijas pārtraukšanas gadījumā</span><span class="sxs-lookup"><span data-stu-id="bfa1d-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="bfa1d-153">Uzkrājuma politika reģistrācijas pārtraukšanas gadījumā nosaka, kā tiek aprēķināts uzkrājums, kad darbinieka reģistrācija tiek pārtraukta uzkrāšanas perioda vidū.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="bfa1d-154">Ir pieejamas tālāk minētās opcijas.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-154">The following options are available:</span></span>

- <span data-ttu-id="bfa1d-155">**Proporcionāli sadalīts** — lai noteiktu starpību dienās, tiek izmantots datumu diapazons starp reģistrācijas datumu un sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="bfa1d-156">Šī starpība tiek piemērota, kad uzkrājumi tiek apstrādāti.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="bfa1d-157">**Pilns uzkrājums** — pirmās uzkrājumu apstrādes laikā tiek piešķirta pilna uzkrājuma summa atbilstoši pakāpei.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="bfa1d-158">**Nav uzkrājuma** — līdz nākamajam uzkrāšanas periodam netiek piešķirts uzkrājums.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="bfa1d-159">Uzkrāšanas grafiks</span><span class="sxs-lookup"><span data-stu-id="bfa1d-159">Accrual schedule</span></span>

<span data-ttu-id="bfa1d-160">Uzkrāšanas grafiks nosaka, kā darbinieks uzkrās brīvo laiku un kādas summas šis darbinieks varēs uzkrāt un pārnest.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="bfa1d-161">Pakāpes var izveidot tā, lai brīvais laiks tiktu piešķirts, pamatojoties uz dažādiem līmeņiem.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="bfa1d-162">Nodarbinātības mēnešu skaits</span><span class="sxs-lookup"><span data-stu-id="bfa1d-162">Months of service</span></span>

<span data-ttu-id="bfa1d-163">**Nodarbinātības mēnešu skaits** vērtība nosaka minimālo mēnešu skaitu, kas darbiniekiem jānostrādā, lai viņiem pienāktos uzkrājumi.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="bfa1d-164">Ja minimālais skaits nav nepieciešams, iestatiet vērtību **0**.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="bfa1d-165">Nostrādātās stundas</span><span class="sxs-lookup"><span data-stu-id="bfa1d-165">Hours worked</span></span>

<span data-ttu-id="bfa1d-166">**Nostrādātās stundas** vērtība nosaka minimālo stundu skaitu, kas darbiniekiem jānostrādā uzkrāšanas periodā, lai viņiem pienāktos uzkrājumi.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="bfa1d-167">Ja minimālais skaits nav nepieciešams, iestatiet vērtību **0**.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="bfa1d-168">Uzkrājuma summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-168">Accrual amount</span></span>

<span data-ttu-id="bfa1d-169">Uzkrājumu summa ir stundu vai dienu skaits, ko darbinieki periodā uzkrāj.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="bfa1d-170">Periodu nosaka uzkrāšanas biežums.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="bfa1d-171">Minimālā bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-171">Minimum balance</span></span>

<span data-ttu-id="bfa1d-172">Negatīvu vērtību var izmantot minimālajai bilancei, ja darbinieki var pieprasīt vairāk atvaļinājumu, nekā viņiem ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="bfa1d-173">Maksimālā pārnesamā summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-173">Maximum carry-forward</span></span>

<span data-ttu-id="bfa1d-174">Uzkrāšanas procesā atvaļinājumu bilances, kas pārsniedz maksimālo pārnešanas bilanci, tiks pielāgotas sākuma datuma gadadienā.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="bfa1d-175">Garantētā summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-175">Grant amount</span></span>

<span data-ttu-id="bfa1d-176">Garantētā summa ir sākotnējais stundu vai dienu skaits, kas darbiniekiem tiek piešķirts, kad viņi pirmo reizi reģistrējas atvaļinājuma plānā.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="bfa1d-177">Summa netiek uzkrāta katram uzkrāšanas periodam.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="bfa1d-178">Registrācijas un bilances</span><span class="sxs-lookup"><span data-stu-id="bfa1d-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="bfa1d-179">Reģistrācijas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-179">Enrollment date</span></span>

<span data-ttu-id="bfa1d-180">Reģistrācijas datums nosaka, kad darbinieks var sākt uzkrāt brīvo laiku.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="bfa1d-181">Piemēram, ja darbiniece tiek reģistrēta atvaļinājuma plānā 2018. gada 15. jūnijā, viņa nevar uzkrāt brīvo laiku pirms 2018. gada 15. jūnija.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="bfa1d-182">Pašreizējā bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-182">Current balance</span></span>

<span data-ttu-id="bfa1d-183">Pašreizējā bilance ir atvaļinājuma apjoms, kas ir pieejams brīvā laika pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="bfa1d-184">Šis apjoms iekļauj uzkrājumus, apstiprinātos pieprasījumus un korekcijas līdz pašreizējam datumam.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="bfa1d-185">Pašreizējās bilances piemēri</span><span class="sxs-lookup"><span data-stu-id="bfa1d-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="bfa1d-186">Gada plāns</span><span class="sxs-lookup"><span data-stu-id="bfa1d-186">Annual plan</span></span>

<span data-ttu-id="bfa1d-187">**Plāna iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-187">**Plan setup**</span></span>

| <span data-ttu-id="bfa1d-188">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-188">Plan start date</span></span> | <span data-ttu-id="bfa1d-189">Reģistrācijas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-189">Enrollment date</span></span> | <span data-ttu-id="bfa1d-190">Uzkrāšanas biežums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-190">Accrual frequency</span></span> | <span data-ttu-id="bfa1d-191">Uzkrāšanas perioda kritērijs</span><span class="sxs-lookup"><span data-stu-id="bfa1d-191">Accrual period basis</span></span> | <span data-ttu-id="bfa1d-192">Uzkrājuma piešķiršanas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="bfa1d-193">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-193">1/1/2018</span></span>        | <span data-ttu-id="bfa1d-194">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-194">1/1/2018</span></span>        | <span data-ttu-id="bfa1d-195">Ikgadējs</span><span class="sxs-lookup"><span data-stu-id="bfa1d-195">Annual</span></span>            | <span data-ttu-id="bfa1d-196">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-196">Plan start date</span></span>      | <span data-ttu-id="bfa1d-197">Uzkrāšanas perioda beigu datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-197">End of accrual period</span></span> |

<span data-ttu-id="bfa1d-198">Uzkrājumi tiek apstrādāti 2019. gada 1. janvārī (1/1/2019), lai tiktu iekļauts viss periods.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="bfa1d-199">**Rezultāti**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-199">**Results**</span></span>

| <span data-ttu-id="bfa1d-200">Uzkrājuma summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-200">Accrual amount</span></span> | <span data-ttu-id="bfa1d-201">Minimālā bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-201">Minimum balance</span></span> | <span data-ttu-id="bfa1d-202">Maksimālā pārnesamā summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-202">Maximum carry-forward</span></span> | <span data-ttu-id="bfa1d-203">Pieprasījumu summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-203">Request amount</span></span> | <span data-ttu-id="bfa1d-204">Pašreizējā bilance (uz 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="bfa1d-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="bfa1d-205">200</span><span class="sxs-lookup"><span data-stu-id="bfa1d-205">200</span></span>            | <span data-ttu-id="bfa1d-206">0</span><span class="sxs-lookup"><span data-stu-id="bfa1d-206">0</span></span>               | <span data-ttu-id="bfa1d-207">120</span><span class="sxs-lookup"><span data-stu-id="bfa1d-207">120</span></span>                   | <span data-ttu-id="bfa1d-208">40</span><span class="sxs-lookup"><span data-stu-id="bfa1d-208">40</span></span>             | <span data-ttu-id="bfa1d-209">160</span><span class="sxs-lookup"><span data-stu-id="bfa1d-209">160</span></span>                              |

<span data-ttu-id="bfa1d-210">Pašreizējā bilance (160) = uzkrājumu summa (200) – pieprasījumu summa (40)</span><span class="sxs-lookup"><span data-stu-id="bfa1d-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="bfa1d-211">Pusmēneša plāns</span><span class="sxs-lookup"><span data-stu-id="bfa1d-211">Semimonthly plan</span></span>

<span data-ttu-id="bfa1d-212">**Plāna iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-212">**Plan setup**</span></span>

| <span data-ttu-id="bfa1d-213">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-213">Plan start date</span></span> | <span data-ttu-id="bfa1d-214">Reģistrācijas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-214">Enrollment date</span></span> | <span data-ttu-id="bfa1d-215">Uzkrāšanas biežums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-215">Accrual frequency</span></span> | <span data-ttu-id="bfa1d-216">Uzkrāšanas perioda kritērijs</span><span class="sxs-lookup"><span data-stu-id="bfa1d-216">Accrual period basis</span></span> | <span data-ttu-id="bfa1d-217">Uzkrājuma piešķiršanas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="bfa1d-218">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-218">1/1/2018</span></span>        | <span data-ttu-id="bfa1d-219">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-219">2/1/2018</span></span>        | <span data-ttu-id="bfa1d-220">Pusmēneša</span><span class="sxs-lookup"><span data-stu-id="bfa1d-220">Semimonthly</span></span>       | <span data-ttu-id="bfa1d-221">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-221">Plan start date</span></span>      | <span data-ttu-id="bfa1d-222">Uzkrāšanas perioda beigu datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-222">End of accrual period</span></span> |

<span data-ttu-id="bfa1d-223">Uzkrājumi tiek apstrādāti 2018. gada 1. maijā (5/1/2018), lai tiktu iekļauts viss periods.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="bfa1d-224">**Rezultāti**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-224">**Results**</span></span>

| <span data-ttu-id="bfa1d-225">Uzkrājuma summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-225">Accrual amount</span></span> | <span data-ttu-id="bfa1d-226">Minimālā bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-226">Minimum balance</span></span> | <span data-ttu-id="bfa1d-227">Maksimālā pārnesamā summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-227">Maximum carry-forward</span></span> | <span data-ttu-id="bfa1d-228">Pieprasījumu summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-228">Request amount</span></span> | <span data-ttu-id="bfa1d-229">Pašreizējā bilance (uz 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="bfa1d-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="bfa1d-230">5.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-230">5</span></span>              | <span data-ttu-id="bfa1d-231">0</span><span class="sxs-lookup"><span data-stu-id="bfa1d-231">0</span></span>               | <span data-ttu-id="bfa1d-232">120</span><span class="sxs-lookup"><span data-stu-id="bfa1d-232">120</span></span>                   | <span data-ttu-id="bfa1d-233">8</span><span class="sxs-lookup"><span data-stu-id="bfa1d-233">8</span></span>              | <span data-ttu-id="bfa1d-234">22</span><span class="sxs-lookup"><span data-stu-id="bfa1d-234">22</span></span>                               |

<span data-ttu-id="bfa1d-235">Pašreizējā bilance (22) = uzkrājumu summa (5 x 6) – pieprasījumu summa (8)</span><span class="sxs-lookup"><span data-stu-id="bfa1d-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="bfa1d-236">Mēneša plāns</span><span class="sxs-lookup"><span data-stu-id="bfa1d-236">Monthly plan</span></span>

<span data-ttu-id="bfa1d-237">**Plāna iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-237">**Plan setup**</span></span>

| <span data-ttu-id="bfa1d-238">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-238">Plan start date</span></span> | <span data-ttu-id="bfa1d-239">Reģistrācijas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-239">Enrollment date</span></span> | <span data-ttu-id="bfa1d-240">Uzkrāšanas biežums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-240">Accrual frequency</span></span> | <span data-ttu-id="bfa1d-241">Uzkrāšanas perioda kritērijs</span><span class="sxs-lookup"><span data-stu-id="bfa1d-241">Accrual period basis</span></span> | <span data-ttu-id="bfa1d-242">Uzkrājuma piešķiršanas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="bfa1d-243">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-243">1/1/2018</span></span>        | <span data-ttu-id="bfa1d-244">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-244">2/1/2018</span></span>        | <span data-ttu-id="bfa1d-245">Pusmēneša</span><span class="sxs-lookup"><span data-stu-id="bfa1d-245">Semimonthly</span></span>       | <span data-ttu-id="bfa1d-246">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-246">Plan start date</span></span>      | <span data-ttu-id="bfa1d-247">Uzkrāšanas perioda beigu datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-247">End of accrual period</span></span> |

<span data-ttu-id="bfa1d-248">Uzkrājumi tiek apstrādāti 2018. gada 1. maijā (5/1/2018), lai tiktu iekļauts viss periods.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="bfa1d-249">**Rezultāti**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-249">**Results**</span></span>

| <span data-ttu-id="bfa1d-250">Uzkrājuma summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-250">Accrual amount</span></span> | <span data-ttu-id="bfa1d-251">Minimālā bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-251">Minimum balance</span></span> | <span data-ttu-id="bfa1d-252">Maksimālā pārnesamā summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-252">Maximum carry-forward</span></span> | <span data-ttu-id="bfa1d-253">Pieprasījumu summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-253">Request amount</span></span> | <span data-ttu-id="bfa1d-254">Pašreizējā bilance (uz 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="bfa1d-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="bfa1d-255">5.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-255">5</span></span>              | <span data-ttu-id="bfa1d-256">0</span><span class="sxs-lookup"><span data-stu-id="bfa1d-256">0</span></span>               | <span data-ttu-id="bfa1d-257">120</span><span class="sxs-lookup"><span data-stu-id="bfa1d-257">120</span></span>                   | <span data-ttu-id="bfa1d-258">8</span><span class="sxs-lookup"><span data-stu-id="bfa1d-258">8</span></span>              | <span data-ttu-id="bfa1d-259">7.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-259">7</span></span>                                |

<span data-ttu-id="bfa1d-260">Pašreizējā bilance (7) = uzkrājumu summa (5 x 3) – pieprasījumu summa (8)</span><span class="sxs-lookup"><span data-stu-id="bfa1d-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="bfa1d-261">Prognozētā bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-261">Forecasted balance</span></span>

<span data-ttu-id="bfa1d-262">*Prognozētā bilance* ir atvaļinājuma laiks, kas ir pieejams tālākā datumā.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="bfa1d-263">Uzkrājumu un pārnešanas korekcijas tiek prognozētas līdz attiecīgajam datumam.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="bfa1d-264">Tiek izmantota šāda formula:</span><span class="sxs-lookup"><span data-stu-id="bfa1d-264">The following formula is used:</span></span>

<span data-ttu-id="bfa1d-265">Pirmdienai prognozētā bilance = pašreizējā bilance – pieprasījumi + uzkrājumi – pārnešanas korekcija</span><span class="sxs-lookup"><span data-stu-id="bfa1d-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="bfa1d-266">Prognozētās bilances piemēri</span><span class="sxs-lookup"><span data-stu-id="bfa1d-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="bfa1d-267">Gada plāns</span><span class="sxs-lookup"><span data-stu-id="bfa1d-267">Annual plan</span></span>

<span data-ttu-id="bfa1d-268">**Plāna iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-268">**Plan setup**</span></span>

| <span data-ttu-id="bfa1d-269">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-269">Plan start date</span></span> | <span data-ttu-id="bfa1d-270">Reģistrācijas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-270">Enrollment date</span></span> | <span data-ttu-id="bfa1d-271">Uzkrāšanas biežums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-271">Accrual frequency</span></span> | <span data-ttu-id="bfa1d-272">Uzkrāšanas perioda kritērijs</span><span class="sxs-lookup"><span data-stu-id="bfa1d-272">Accrual period basis</span></span> | <span data-ttu-id="bfa1d-273">Uzkrājuma piešķiršanas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="bfa1d-274">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-274">1/1/2018</span></span>        | <span data-ttu-id="bfa1d-275">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-275">1/1/2018</span></span>        | <span data-ttu-id="bfa1d-276">Ikgadējs</span><span class="sxs-lookup"><span data-stu-id="bfa1d-276">Annual</span></span>            | <span data-ttu-id="bfa1d-277">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-277">Plan start date</span></span>      | <span data-ttu-id="bfa1d-278">Uzkrāšanas perioda beigu datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-278">End of accrual period</span></span> |

<span data-ttu-id="bfa1d-279">Uzkrājumi tiek apstrādāti 2019. gada 15. februārī (2/15/2019), lai tiktu iekļauts viss periods.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="bfa1d-280">**Rezultāti**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-280">**Results**</span></span>

| <span data-ttu-id="bfa1d-281">Uzkrājuma summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-281">Accrual amount</span></span> | <span data-ttu-id="bfa1d-282">Minimālā bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-282">Minimum balance</span></span> | <span data-ttu-id="bfa1d-283">Maksimālā pārnesamā summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-283">Maximum carry-forward</span></span> | <span data-ttu-id="bfa1d-284">Pašreizējā bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-284">Current balance</span></span> | <span data-ttu-id="bfa1d-285">Prognozētā bilance (uz 2/15/2019)</span><span class="sxs-lookup"><span data-stu-id="bfa1d-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="bfa1d-286">20.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-286">20</span></span>             | <span data-ttu-id="bfa1d-287">0</span><span class="sxs-lookup"><span data-stu-id="bfa1d-287">0</span></span>               | <span data-ttu-id="bfa1d-288">20.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-288">20</span></span>                    | <span data-ttu-id="bfa1d-289">40</span><span class="sxs-lookup"><span data-stu-id="bfa1d-289">40</span></span>              | <span data-ttu-id="bfa1d-290">40</span><span class="sxs-lookup"><span data-stu-id="bfa1d-290">40</span></span>                                   |

<span data-ttu-id="bfa1d-291">Prognozētā bilance (40) = uzkrājumu summa (20) + pašreizējā bilance (40) – pārnešanas korekcija (20)</span><span class="sxs-lookup"><span data-stu-id="bfa1d-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="bfa1d-292">Pusmēneša plāns</span><span class="sxs-lookup"><span data-stu-id="bfa1d-292">Semimonthly plan</span></span>

<span data-ttu-id="bfa1d-293">**Plāna iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-293">**Plan setup**</span></span>

| <span data-ttu-id="bfa1d-294">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-294">Plan start date</span></span> | <span data-ttu-id="bfa1d-295">Reģistrācijas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-295">Enrollment date</span></span> | <span data-ttu-id="bfa1d-296">Uzkrāšanas biežums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-296">Accrual frequency</span></span> | <span data-ttu-id="bfa1d-297">Uzkrāšanas perioda kritērijs</span><span class="sxs-lookup"><span data-stu-id="bfa1d-297">Accrual period basis</span></span> | <span data-ttu-id="bfa1d-298">Uzkrājuma piešķiršanas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="bfa1d-299">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-299">1/1/2018</span></span>        | <span data-ttu-id="bfa1d-300">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-300">2/1/2018</span></span>        | <span data-ttu-id="bfa1d-301">Pusmēneša</span><span class="sxs-lookup"><span data-stu-id="bfa1d-301">Semimonthly</span></span>       | <span data-ttu-id="bfa1d-302">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-302">Plan start date</span></span>      | <span data-ttu-id="bfa1d-303">Uzkrāšanas perioda beigu datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-303">End of accrual period</span></span> |

<span data-ttu-id="bfa1d-304">Uzkrājumi tiek apstrādāti 2019. gada 15. februārī (2/15/2019), lai tiktu iekļauts viss periods.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="bfa1d-305">**Rezultāti**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-305">**Results**</span></span>

| <span data-ttu-id="bfa1d-306">Uzkrājuma summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-306">Accrual amount</span></span> | <span data-ttu-id="bfa1d-307">Minimālā bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-307">Minimum balance</span></span> | <span data-ttu-id="bfa1d-308">Maksimālā pārnesamā summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-308">Maximum carry-forward</span></span> | <span data-ttu-id="bfa1d-309">Pašreizējā bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-309">Current balance</span></span> | <span data-ttu-id="bfa1d-310">Prognozētā bilance (uz 2/15/2019)</span><span class="sxs-lookup"><span data-stu-id="bfa1d-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="bfa1d-311">5.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-311">5</span></span>              | <span data-ttu-id="bfa1d-312">0</span><span class="sxs-lookup"><span data-stu-id="bfa1d-312">0</span></span>               | <span data-ttu-id="bfa1d-313">20.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-313">20</span></span>                    | <span data-ttu-id="bfa1d-314">40</span><span class="sxs-lookup"><span data-stu-id="bfa1d-314">40</span></span>              | <span data-ttu-id="bfa1d-315">35</span><span class="sxs-lookup"><span data-stu-id="bfa1d-315">35</span></span>                                   |

<span data-ttu-id="bfa1d-316">Prognozētā bilance (35) = uzkrājumu summa (5 x 3) + pašreizējā bilance (40) – pārnešanas korekcija (20)</span><span class="sxs-lookup"><span data-stu-id="bfa1d-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="bfa1d-317">Mēneša plāns</span><span class="sxs-lookup"><span data-stu-id="bfa1d-317">Monthly plan</span></span>

<span data-ttu-id="bfa1d-318">**Plāna iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-318">**Plan setup**</span></span>

| <span data-ttu-id="bfa1d-319">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-319">Plan start date</span></span> | <span data-ttu-id="bfa1d-320">Reģistrācijas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-320">Enrollment date</span></span> | <span data-ttu-id="bfa1d-321">Uzkrāšanas biežums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-321">Accrual frequency</span></span> | <span data-ttu-id="bfa1d-322">Uzkrāšanas perioda kritērijs</span><span class="sxs-lookup"><span data-stu-id="bfa1d-322">Accrual period basis</span></span> | <span data-ttu-id="bfa1d-323">Uzkrājuma piešķiršanas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="bfa1d-324">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-324">1/1/2018</span></span>        | <span data-ttu-id="bfa1d-325">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-325">2/1/2018</span></span>        | <span data-ttu-id="bfa1d-326">Pusmēneša</span><span class="sxs-lookup"><span data-stu-id="bfa1d-326">Semimonthly</span></span>       | <span data-ttu-id="bfa1d-327">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-327">Plan start date</span></span>      | <span data-ttu-id="bfa1d-328">Uzkrāšanas perioda beigu datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-328">End of accrual period</span></span> |

<span data-ttu-id="bfa1d-329">Uzkrājumi tiek apstrādāti 2019. gada 15. februārī (2/15/2019), lai tiktu iekļauts viss periods.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="bfa1d-330">**Rezultāti**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-330">**Results**</span></span>

| <span data-ttu-id="bfa1d-331">Uzkrājuma summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-331">Accrual amount</span></span> | <span data-ttu-id="bfa1d-332">Minimālā bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-332">Minimum balance</span></span> | <span data-ttu-id="bfa1d-333">Maksimālā pārnesamā summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-333">Maximum carry-forward</span></span> | <span data-ttu-id="bfa1d-334">Pašreizējā bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-334">Current balance</span></span> | <span data-ttu-id="bfa1d-335">Prognozētā bilance (uz 2/15/2019)</span><span class="sxs-lookup"><span data-stu-id="bfa1d-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="bfa1d-336">10.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-336">10</span></span>             | <span data-ttu-id="bfa1d-337">0</span><span class="sxs-lookup"><span data-stu-id="bfa1d-337">0</span></span>               | <span data-ttu-id="bfa1d-338">20.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-338">20</span></span>                    | <span data-ttu-id="bfa1d-339">40</span><span class="sxs-lookup"><span data-stu-id="bfa1d-339">40</span></span>              | <span data-ttu-id="bfa1d-340">30</span><span class="sxs-lookup"><span data-stu-id="bfa1d-340">30</span></span>                                   |

<span data-ttu-id="bfa1d-341">Prognozētā bilance (30) = uzkrājumu summa (10 x 1) + pašreizējā bilance (40) – pārnešanas korekcija (20)</span><span class="sxs-lookup"><span data-stu-id="bfa1d-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="bfa1d-342">Proporcionālā sadalījuma bilances piemēri</span><span class="sxs-lookup"><span data-stu-id="bfa1d-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="bfa1d-343">Proporcionāli sadalītais mēneša plāns</span><span class="sxs-lookup"><span data-stu-id="bfa1d-343">Prorated monthly plan</span></span>

<span data-ttu-id="bfa1d-344">**Plāna iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-344">**Plan setup**</span></span>

| <span data-ttu-id="bfa1d-345">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-345">Plan start date</span></span> | <span data-ttu-id="bfa1d-346">Uzkrāšanas biežums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-346">Accrual frequency</span></span> | <span data-ttu-id="bfa1d-347">Uzkrāšanas perioda kritērijs</span><span class="sxs-lookup"><span data-stu-id="bfa1d-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="bfa1d-348">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-348">1/1/2018</span></span>        | <span data-ttu-id="bfa1d-349">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="bfa1d-349">Monthly</span></span>           | <span data-ttu-id="bfa1d-350">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-350">Plan start date</span></span>      |

<span data-ttu-id="bfa1d-351">**Rezultāti**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-351">**Results**</span></span>

| <span data-ttu-id="bfa1d-352">Darbinieks</span><span class="sxs-lookup"><span data-stu-id="bfa1d-352">Employee</span></span>            | <span data-ttu-id="bfa1d-353">Nodarbinātības mēnešu skaits</span><span class="sxs-lookup"><span data-stu-id="bfa1d-353">Months of service</span></span> | <span data-ttu-id="bfa1d-354">Reģistrācijas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-354">Enrollment date</span></span> | <span data-ttu-id="bfa1d-355">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-355">Start date</span></span> | <span data-ttu-id="bfa1d-356">Uzkrājuma summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-356">Accrual amount</span></span> | <span data-ttu-id="bfa1d-357">Apstrādātais uzkrājums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-357">Process accrual</span></span> | <span data-ttu-id="bfa1d-358">Bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="bfa1d-359">Žanete Nikolsone</span><span class="sxs-lookup"><span data-stu-id="bfa1d-359">Jeannette Nicholson</span></span> | <span data-ttu-id="bfa1d-360">0,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-360">0.00</span></span>              | <span data-ttu-id="bfa1d-361">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-361">6/1/2018</span></span>        | <span data-ttu-id="bfa1d-362">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-362">6/1/2018</span></span>   | <span data-ttu-id="bfa1d-363">1,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-363">1.00</span></span>           | <span data-ttu-id="bfa1d-364">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-364">9/1/2018</span></span>        | <span data-ttu-id="bfa1d-365">3,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-365">3.00</span></span>    |
| <span data-ttu-id="bfa1d-366">Džejs Normans</span><span class="sxs-lookup"><span data-stu-id="bfa1d-366">Jay Norman</span></span>          | <span data-ttu-id="bfa1d-367">0,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-367">0.00</span></span>              | <span data-ttu-id="bfa1d-368">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-368">6/15/2018</span></span>       | <span data-ttu-id="bfa1d-369">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-369">6/15/2018</span></span>  | <span data-ttu-id="bfa1d-370">1,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-370">1.00</span></span>           | <span data-ttu-id="bfa1d-371">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-371">9/1/2018</span></span>        | <span data-ttu-id="bfa1d-372">2,53</span><span class="sxs-lookup"><span data-stu-id="bfa1d-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="bfa1d-373">Pilna uzkrājuma mēneša plāns</span><span class="sxs-lookup"><span data-stu-id="bfa1d-373">Full accrual monthly plan</span></span>

<span data-ttu-id="bfa1d-374">**Plāna iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-374">**Plan setup**</span></span>

| <span data-ttu-id="bfa1d-375">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-375">Plan start date</span></span> | <span data-ttu-id="bfa1d-376">Uzkrāšanas biežums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-376">Accrual frequency</span></span> | <span data-ttu-id="bfa1d-377">Uzkrāšanas perioda kritērijs</span><span class="sxs-lookup"><span data-stu-id="bfa1d-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="bfa1d-378">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-378">1/1/2018</span></span>        | <span data-ttu-id="bfa1d-379">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="bfa1d-379">Monthly</span></span>           | <span data-ttu-id="bfa1d-380">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-380">Plan start date</span></span>      |

<span data-ttu-id="bfa1d-381">**Rezultāti**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-381">**Results**</span></span>

| <span data-ttu-id="bfa1d-382">Darbinieks</span><span class="sxs-lookup"><span data-stu-id="bfa1d-382">Employee</span></span>            | <span data-ttu-id="bfa1d-383">Nodarbinātības mēnešu skaits</span><span class="sxs-lookup"><span data-stu-id="bfa1d-383">Months of service</span></span> | <span data-ttu-id="bfa1d-384">Reģistrācijas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-384">Enrollment date</span></span> | <span data-ttu-id="bfa1d-385">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-385">Start date</span></span> | <span data-ttu-id="bfa1d-386">Uzkrājuma summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-386">Accrual amount</span></span> | <span data-ttu-id="bfa1d-387">Apstrādātais uzkrājums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-387">Process accrual</span></span> | <span data-ttu-id="bfa1d-388">Bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="bfa1d-389">Žanete Nikolsone</span><span class="sxs-lookup"><span data-stu-id="bfa1d-389">Jeannette Nicholson</span></span> | <span data-ttu-id="bfa1d-390">0,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-390">0.00</span></span>              | <span data-ttu-id="bfa1d-391">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-391">6/1/2018</span></span>        | <span data-ttu-id="bfa1d-392">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-392">6/1/2018</span></span>   | <span data-ttu-id="bfa1d-393">1,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-393">1.00</span></span>           | <span data-ttu-id="bfa1d-394">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-394">9/1/2018</span></span>        | <span data-ttu-id="bfa1d-395">3,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-395">3.00</span></span>    |
| <span data-ttu-id="bfa1d-396">Džejs Normans</span><span class="sxs-lookup"><span data-stu-id="bfa1d-396">Jay Norman</span></span>          | <span data-ttu-id="bfa1d-397">0,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-397">0.00</span></span>              | <span data-ttu-id="bfa1d-398">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-398">6/15/2018</span></span>       | <span data-ttu-id="bfa1d-399">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-399">6/15/2018</span></span>  | <span data-ttu-id="bfa1d-400">1,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-400">1.00</span></span>           | <span data-ttu-id="bfa1d-401">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-401">9/1/2018</span></span>        | <span data-ttu-id="bfa1d-402">3,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="bfa1d-403">Mēneša bez uzkrājuma plāns</span><span class="sxs-lookup"><span data-stu-id="bfa1d-403">No accrual monthly plan</span></span>

<span data-ttu-id="bfa1d-404">**Plāna iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-404">**Plan setup**</span></span>

| <span data-ttu-id="bfa1d-405">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-405">Plan start date</span></span> | <span data-ttu-id="bfa1d-406">Uzkrāšanas biežums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-406">Accrual frequency</span></span> | <span data-ttu-id="bfa1d-407">Uzkrāšanas perioda kritērijs</span><span class="sxs-lookup"><span data-stu-id="bfa1d-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="bfa1d-408">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-408">1/1/2018</span></span>        | <span data-ttu-id="bfa1d-409">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="bfa1d-409">Monthly</span></span>           | <span data-ttu-id="bfa1d-410">Plāna sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-410">Plan start date</span></span>      |

<span data-ttu-id="bfa1d-411">**Rezultāti**</span><span class="sxs-lookup"><span data-stu-id="bfa1d-411">**Results**</span></span>

| <span data-ttu-id="bfa1d-412">Darbinieks</span><span class="sxs-lookup"><span data-stu-id="bfa1d-412">Employee</span></span>            | <span data-ttu-id="bfa1d-413">Nodarbinātības mēnešu skaits</span><span class="sxs-lookup"><span data-stu-id="bfa1d-413">Months of service</span></span> | <span data-ttu-id="bfa1d-414">Reģistrācijas datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-414">Enrollment date</span></span> | <span data-ttu-id="bfa1d-415">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-415">Start date</span></span> | <span data-ttu-id="bfa1d-416">Uzkrājuma summa</span><span class="sxs-lookup"><span data-stu-id="bfa1d-416">Accrual amount</span></span> | <span data-ttu-id="bfa1d-417">Apstrādātais uzkrājums</span><span class="sxs-lookup"><span data-stu-id="bfa1d-417">Process accrual</span></span> | <span data-ttu-id="bfa1d-418">Bilance</span><span class="sxs-lookup"><span data-stu-id="bfa1d-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="bfa1d-419">Žanete Nikolsone</span><span class="sxs-lookup"><span data-stu-id="bfa1d-419">Jeannette Nicholson</span></span> | <span data-ttu-id="bfa1d-420">0,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-420">0.00</span></span>              | <span data-ttu-id="bfa1d-421">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-421">6/1/2018</span></span>        | <span data-ttu-id="bfa1d-422">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-422">6/1/2018</span></span>   | <span data-ttu-id="bfa1d-423">1,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-423">1.00</span></span>           | <span data-ttu-id="bfa1d-424">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-424">9/1/2018</span></span>        | <span data-ttu-id="bfa1d-425">3,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-425">3.00</span></span>    |
| <span data-ttu-id="bfa1d-426">Džejs Normans</span><span class="sxs-lookup"><span data-stu-id="bfa1d-426">Jay Norman</span></span>          | <span data-ttu-id="bfa1d-427">0,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-427">0.00</span></span>              | <span data-ttu-id="bfa1d-428">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-428">6/15/2018</span></span>       | <span data-ttu-id="bfa1d-429">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-429">6/15/2018</span></span>  | <span data-ttu-id="bfa1d-430">1,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-430">1.00</span></span>           | <span data-ttu-id="bfa1d-431">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="bfa1d-431">9/1/2018</span></span>        | <span data-ttu-id="bfa1d-432">2,00</span><span class="sxs-lookup"><span data-stu-id="bfa1d-432">2.00</span></span>    |

