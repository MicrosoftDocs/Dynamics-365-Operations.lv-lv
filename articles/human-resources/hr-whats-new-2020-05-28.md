---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 28. maijs)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c386025843edef83d229a42d3f2314678fadae20
ms.sourcegitcommit: beddfba095c23b3265f0004f5124c4e9dc6404cc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411934"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="b03ed-103">Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 28. maijs)</span><span class="sxs-lookup"><span data-stu-id="b03ed-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

<span data-ttu-id="b03ed-104">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b03ed-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b03ed-105">Izmaiņas attiecas uz būvējuma numuru 8.1.3287.</span><span class="sxs-lookup"><span data-stu-id="b03ed-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="b03ed-106">Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.</span><span class="sxs-lookup"><span data-stu-id="b03ed-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="b03ed-107">LeaveRequest elements nedarbojas, ja iespējojat vairākus veidus atvaļinājumu plānam (447498)</span><span class="sxs-lookup"><span data-stu-id="b03ed-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="b03ed-108">Ar šo izmaiņu **LeaveEnrollmentV2Entity** tagad ir pieejams, lai labotu kļūdu, kas rodas, iespējojot vairākus atvaļinājumu veidus.</span><span class="sxs-lookup"><span data-stu-id="b03ed-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="b03ed-109">Partijas konfliktsituācijas samazināšanas līdzeklis (priekšskatījums) (446619)</span><span class="sxs-lookup"><span data-stu-id="b03ed-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="b03ed-110">Iespējojot šo līdzekli, var sagaidīt, ka, atlasot uzdevumus un apstrādājot darbus, pakešveida struktūras tabulu aizturēšana tiks samazināta.</span><span class="sxs-lookup"><span data-stu-id="b03ed-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="b03ed-111">UpdateConflict, saglabājot darbinieku, neļauj rediģēt ierakstu programmā Personas (427915)</span><span class="sxs-lookup"><span data-stu-id="b03ed-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="b03ed-112">Šīs izmaiņas labo kļūdu, pievienojot jaunu darbinieku, atjauninot adreses informāciju un mainot valodas preferenci.</span><span class="sxs-lookup"><span data-stu-id="b03ed-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="b03ed-113">Šajā unikālajā scenārijā tiek parādīta kļūda, kas norāda, ka ierakstu nevarēja atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="b03ed-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="b03ed-114">Nav iespējams pievienot pielikumu apstiprinātam atvaļinājuma pieprasījumam, lai to iesniegtu atkārtoti (425407)</span><span class="sxs-lookup"><span data-stu-id="b03ed-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="b03ed-115">Šī izmaiņa tagad ļauj pievienot pielikumus apstiprinātiem atvaļinājumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="b03ed-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="b03ed-116">Lietotājs var ievadīt kompensāciju darbiniekam citas juridiskās personas veidlapā (409529)</span><span class="sxs-lookup"><span data-stu-id="b03ed-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="b03ed-117">Šī izmaiņa atspējo kompensāciju opcijas, lai novērstu nejaušu kompensācijas ierakstu ievadīšanu nepareizai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="b03ed-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="b03ed-118">Kļūda, pārsūtot darbinieku un darbinieka amata piešķires datumu, rodas pirms amata ilguma (429402)</span><span class="sxs-lookup"><span data-stu-id="b03ed-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="b03ed-119">Pārsūtot darbinieku šajā scenārijā, ir atjaunināti kļūdu ziņojumi, lai labāk aprakstītu problēmas novēršanai nepieciešamās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="b03ed-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="b03ed-120">Pielikumu iespējas Darbinieku pašapkalpošanās atvieglojumu reģistrācijā</span><span class="sxs-lookup"><span data-stu-id="b03ed-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="b03ed-121">Tagad varat pievienot pielikumus atvieglojumu reģistrācijas procesa laikā katram plānam, kurā darbinieks ir reģistrējies.</span><span class="sxs-lookup"><span data-stu-id="b03ed-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="b03ed-122">Pēc tam varat skatīt pielikumus veidlapā **Darbinieka reģistrētais atvieglojums**.</span><span class="sxs-lookup"><span data-stu-id="b03ed-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="b03ed-123">Priekšskatījumā</span><span class="sxs-lookup"><span data-stu-id="b03ed-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="b03ed-124">Programma Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="b03ed-124">Human Resources application in Teams</span></span>

<span data-ttu-id="b03ed-125">Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b03ed-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="b03ed-126">Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="b03ed-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="b03ed-127">Papildinformāciju skatiet sadaļā [Personāla vadība programms sistēmā Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="b03ed-127">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="b03ed-128">Atvaļinājuma atlikšana</span><span class="sxs-lookup"><span data-stu-id="b03ed-128">Leave suspension</span></span>

<span data-ttu-id="b03ed-129">Jūs varat atlikt atvaļinājumu un prombūtni darbiniekam Personāla vadības programmā.</span><span class="sxs-lookup"><span data-stu-id="b03ed-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="b03ed-130">Aizturot atvaļinājumu, tiek apturēti atvaļinājumu uzkrājumi atsevišķiem atvaļinājumu veidiem.</span><span class="sxs-lookup"><span data-stu-id="b03ed-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="b03ed-131">Ja atlikšana notiek pēc uzkrājumu procesa, aizturētā atvaļinājuma rezultātā izveido proporcionālu pārrēķinu darbinieka atvaļinājuma bilancei.</span><span class="sxs-lookup"><span data-stu-id="b03ed-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="b03ed-132">Papildinformāciju skatiet [Aizturēt atvaļinājumu](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="b03ed-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="b03ed-133">Atjaunināt lietotāja pieredzi, lai norādītu, ka uzkrāšana ir apturēta (429550)</span><span class="sxs-lookup"><span data-stu-id="b03ed-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="b03ed-134">Lietotāja pieredze tagad norāda, ka uzkrājums ir atlikts plānam.</span><span class="sxs-lookup"><span data-stu-id="b03ed-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="b03ed-135">Drīzumā</span><span class="sxs-lookup"><span data-stu-id="b03ed-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="b03ed-136">Datu bāzes reģistrēšana (priekšskatījumā jūnijā)</span><span class="sxs-lookup"><span data-stu-id="b03ed-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="b03ed-137">Datu bāzes reģistrācijas līdzeklis ļauj noteikt, kura tabula un lauki ir jāpārrauga.</span><span class="sxs-lookup"><span data-stu-id="b03ed-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="b03ed-138">Tas arī ļauj noteikt notikumus, kam jāizraisa izmaiņu izsekošana.</span><span class="sxs-lookup"><span data-stu-id="b03ed-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="b03ed-139">Ir pieejamas ieprasījuma iespējas, lai laika gaitā skatītu šīs izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="b03ed-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="b03ed-140">Atvaļinājuma pirkšana un pārdošana (priekšskatījumā 1. jūnijā)</span><span class="sxs-lookup"><span data-stu-id="b03ed-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="b03ed-141">Dažas organizācijas sniedz atvieglojumus, kas ļauj darbiniekiem pirkt vai pārdot atvaļinājumu.</span><span class="sxs-lookup"><span data-stu-id="b03ed-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="b03ed-142">Šo procesu bieži pārvalda manuāli.</span><span class="sxs-lookup"><span data-stu-id="b03ed-142">This process is often managed manually.</span></span> <span data-ttu-id="b03ed-143">Šis līdzeklis nodrošina automatizētu veidu, kā pārvaldīt Cilvēkresursu departamenta politikas un pieprasījumus, un palīdz likvidēt kļūdas, racionalizējot atvaļinājumu pārvaldības procesu.</span><span class="sxs-lookup"><span data-stu-id="b03ed-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span>

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="b03ed-144">Datu pārvaldības struktūras (DMF) elementi atvieglojumu pārvaldībai</span><span class="sxs-lookup"><span data-stu-id="b03ed-144">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="b03ed-145">Tiek izlaisti atvieglojumu pārvaldības elementi.</span><span class="sxs-lookup"><span data-stu-id="b03ed-145">Benefits management entities are releasing.</span></span> <span data-ttu-id="b03ed-146">DMF elementi ļauj importēt un eksportēt datus, lai viegli konfigurētu atvieglojumu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="b03ed-146">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="b03ed-147">Lai pārvietotu datus, būs pieejama arī atvieglojumu pārvaldības veidne.</span><span class="sxs-lookup"><span data-stu-id="b03ed-147">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="b03ed-148">Veidne eksportē un importē datus secīgā veidā, lai ievērotu datu atkarības.</span><span class="sxs-lookup"><span data-stu-id="b03ed-148">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="b03ed-149">Pievienot uzkrājumu atlikšanas iemesla kodu (1. jūnijs)</span><span class="sxs-lookup"><span data-stu-id="b03ed-149">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="b03ed-150">Pamatojuma kodi ir pievienoti uzkrāšanas apturēšanai.</span><span class="sxs-lookup"><span data-stu-id="b03ed-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="b03ed-151">Pārnešanas kārtulas (1. jūnijs)</span><span class="sxs-lookup"><span data-stu-id="b03ed-151">Carry forward rules (June 1)</span></span>

<span data-ttu-id="b03ed-152">Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas.</span><span class="sxs-lookup"><span data-stu-id="b03ed-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="b03ed-153">Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām.</span><span class="sxs-lookup"><span data-stu-id="b03ed-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="b03ed-154">Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="b03ed-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="b03ed-155">Aizturēt atvaļinājumu uzkrājumu norādīto atvaļinājumu veidiem (1. jūnijs)</span><span class="sxs-lookup"><span data-stu-id="b03ed-155">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="b03ed-156">Šajā laidienā PV var izveidot kārtulu, kas aptur atvaļinājumu uzkrājumus darbiniekiem ar atvaļinājumu pieprasījumiem, kas ievadīti neapmaksātam atvaļinājumam.</span><span class="sxs-lookup"><span data-stu-id="b03ed-156">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="b03ed-157">Neapmaksāts atvaļinājums var būt veids, bet tam nav obligāti jābūt.</span><span class="sxs-lookup"><span data-stu-id="b03ed-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="b03ed-158">Jūs varat aizturēt jebkuru atvaļinājumu, pamatojoties uz citu atvaļinājumu veidu.</span><span class="sxs-lookup"><span data-stu-id="b03ed-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="b03ed-159">DMF elements ir pieejams uzkrājumu atlikšanai (1. jūnijs)</span><span class="sxs-lookup"><span data-stu-id="b03ed-159">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="b03ed-160">DMF elements tagad ir pieejams uzkrājumu atlikšanai.</span><span class="sxs-lookup"><span data-stu-id="b03ed-160">A DMF entity is now available for accrual suspensions.</span></span>