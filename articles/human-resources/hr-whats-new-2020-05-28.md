---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 28. maijs)
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 28. maiju.
author: andreabichsel
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e15891a2cb75851d195e08b87bbfc9efb78e66e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803397"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="1aae6-103">Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 28. maijs)</span><span class="sxs-lookup"><span data-stu-id="1aae6-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1aae6-104">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1aae6-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="1aae6-105">Izmaiņas attiecas uz būvējuma numuru 8.1.3287.</span><span class="sxs-lookup"><span data-stu-id="1aae6-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="1aae6-106">Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.</span><span class="sxs-lookup"><span data-stu-id="1aae6-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="1aae6-107">LeaveRequest elements nedarbojas, ja iespējojat vairākus veidus atvaļinājumu plānam (447498)</span><span class="sxs-lookup"><span data-stu-id="1aae6-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="1aae6-108">Ar šo izmaiņu **LeaveEnrollmentV2Entity** tagad ir pieejams, lai labotu kļūdu, kas rodas, iespējojot vairākus atvaļinājumu veidus.</span><span class="sxs-lookup"><span data-stu-id="1aae6-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="1aae6-109">Partijas konfliktsituācijas samazināšanas līdzeklis (priekšskatījums) (446619)</span><span class="sxs-lookup"><span data-stu-id="1aae6-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="1aae6-110">Iespējojot šo līdzekli, var sagaidīt, ka, atlasot uzdevumus un apstrādājot darbus, pakešveida struktūras tabulu aizturēšana tiks samazināta.</span><span class="sxs-lookup"><span data-stu-id="1aae6-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="1aae6-111">UpdateConflict, saglabājot darbinieku, neļauj rediģēt ierakstu programmā Personas (427915)</span><span class="sxs-lookup"><span data-stu-id="1aae6-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="1aae6-112">Šīs izmaiņas labo kļūdu, pievienojot jaunu darbinieku, atjauninot adreses informāciju un mainot valodas preferenci.</span><span class="sxs-lookup"><span data-stu-id="1aae6-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="1aae6-113">Šajā unikālajā scenārijā tiek parādīta kļūda, kas norāda, ka ierakstu nevarēja atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="1aae6-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="1aae6-114">Nav iespējams pievienot pielikumu apstiprinātam atvaļinājuma pieprasījumam, lai to iesniegtu atkārtoti (425407)</span><span class="sxs-lookup"><span data-stu-id="1aae6-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="1aae6-115">Šī izmaiņa tagad ļauj pievienot pielikumus apstiprinātiem atvaļinājumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="1aae6-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="1aae6-116">Lietotājs var ievadīt kompensāciju darbiniekam citas juridiskās personas veidlapā (409529)</span><span class="sxs-lookup"><span data-stu-id="1aae6-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="1aae6-117">Šī izmaiņa atspējo kompensāciju opcijas, lai novērstu nejaušu kompensācijas ierakstu ievadīšanu nepareizai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="1aae6-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="1aae6-118">Kļūda, pārsūtot darbinieku un darbinieka amata piešķires datumu, rodas pirms amata ilguma (429402)</span><span class="sxs-lookup"><span data-stu-id="1aae6-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="1aae6-119">Pārsūtot darbinieku šajā scenārijā, ir atjaunināti kļūdu ziņojumi, lai labāk aprakstītu problēmas novēršanai nepieciešamās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="1aae6-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="1aae6-120">Pielikumu iespējas Darbinieku pašapkalpošanās atvieglojumu reģistrācijā</span><span class="sxs-lookup"><span data-stu-id="1aae6-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="1aae6-121">Tagad varat pievienot pielikumus atvieglojumu reģistrācijas procesa laikā katram plānam, kurā darbinieks ir reģistrējies.</span><span class="sxs-lookup"><span data-stu-id="1aae6-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="1aae6-122">Pēc tam varat skatīt pielikumus veidlapā **Darbinieka reģistrētais atvieglojums**.</span><span class="sxs-lookup"><span data-stu-id="1aae6-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="1aae6-123">Priekšskatījumā</span><span class="sxs-lookup"><span data-stu-id="1aae6-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="1aae6-124">Programma Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="1aae6-124">Human Resources application in Teams</span></span>

<span data-ttu-id="1aae6-125">Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="1aae6-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="1aae6-126">Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="1aae6-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="1aae6-127">Papildinformāciju skatiet sadaļā [Personāla vadība programms sistēmā Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="1aae6-127">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="1aae6-128">Atvaļinājuma atlikšana</span><span class="sxs-lookup"><span data-stu-id="1aae6-128">Leave suspension</span></span>

<span data-ttu-id="1aae6-129">Jūs varat atlikt atvaļinājumu un prombūtni darbiniekam Personāla vadības programmā.</span><span class="sxs-lookup"><span data-stu-id="1aae6-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="1aae6-130">Aizturot atvaļinājumu, tiek apturēti atvaļinājumu uzkrājumi atsevišķiem atvaļinājumu veidiem.</span><span class="sxs-lookup"><span data-stu-id="1aae6-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="1aae6-131">Ja atlikšana notiek pēc uzkrājumu procesa, aizturētā atvaļinājuma rezultātā izveido proporcionālu pārrēķinu darbinieka atvaļinājuma bilancei.</span><span class="sxs-lookup"><span data-stu-id="1aae6-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="1aae6-132">Papildinformāciju skatiet [Aizturēt atvaļinājumu](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="1aae6-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="1aae6-133">Atjaunināt lietotāja pieredzi, lai norādītu, ka uzkrāšana ir apturēta (429550)</span><span class="sxs-lookup"><span data-stu-id="1aae6-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="1aae6-134">Lietotāja pieredze tagad norāda, ka uzkrājums ir atlikts plānam.</span><span class="sxs-lookup"><span data-stu-id="1aae6-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="1aae6-135">Drīzumā</span><span class="sxs-lookup"><span data-stu-id="1aae6-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="1aae6-136">Datu bāzes reģistrēšana (priekšskatījumā jūnijā)</span><span class="sxs-lookup"><span data-stu-id="1aae6-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="1aae6-137">Datu bāzes reģistrācijas līdzeklis ļauj noteikt, kura tabula un lauki ir jāpārrauga.</span><span class="sxs-lookup"><span data-stu-id="1aae6-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="1aae6-138">Tas arī ļauj noteikt notikumus, kam jāizraisa izmaiņu izsekošana.</span><span class="sxs-lookup"><span data-stu-id="1aae6-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="1aae6-139">Ir pieejamas ieprasījuma iespējas, lai laika gaitā skatītu šīs izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="1aae6-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="1aae6-140">Atvaļinājuma pirkšana un pārdošana (priekšskatījumā 1. jūnijā)</span><span class="sxs-lookup"><span data-stu-id="1aae6-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="1aae6-141">Dažas organizācijas sniedz atvieglojumus, kas ļauj darbiniekiem pirkt vai pārdot atvaļinājumu.</span><span class="sxs-lookup"><span data-stu-id="1aae6-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="1aae6-142">Šo procesu bieži pārvalda manuāli.</span><span class="sxs-lookup"><span data-stu-id="1aae6-142">This process is often managed manually.</span></span> <span data-ttu-id="1aae6-143">Šis līdzeklis nodrošina automatizētu veidu, kā pārvaldīt Cilvēkresursu departamenta politikas un pieprasījumus, un palīdz likvidēt kļūdas, racionalizējot atvaļinājumu pārvaldības procesu.</span><span class="sxs-lookup"><span data-stu-id="1aae6-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span> <span data-ttu-id="1aae6-144">Plašāku informāciju skatiet:</span><span class="sxs-lookup"><span data-stu-id="1aae6-144">For more information, see:</span></span>

- [<span data-ttu-id="1aae6-145">Atvaļinājuma iegādes un pārdošanas politiku pārvaldība</span><span class="sxs-lookup"><span data-stu-id="1aae6-145">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="1aae6-146">Atvaļinājuma iegāde un pārdošana</span><span class="sxs-lookup"><span data-stu-id="1aae6-146">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="1aae6-147">Datu pārvaldības struktūras (DMF) elementi atvieglojumu pārvaldībai</span><span class="sxs-lookup"><span data-stu-id="1aae6-147">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="1aae6-148">Tiek izlaisti atvieglojumu pārvaldības elementi.</span><span class="sxs-lookup"><span data-stu-id="1aae6-148">Benefits management entities are releasing.</span></span> <span data-ttu-id="1aae6-149">DMF elementi ļauj importēt un eksportēt datus, lai viegli konfigurētu atvieglojumu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="1aae6-149">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="1aae6-150">Lai pārvietotu datus, būs pieejama arī atvieglojumu pārvaldības veidne.</span><span class="sxs-lookup"><span data-stu-id="1aae6-150">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="1aae6-151">Veidne eksportē un importē datus secīgā veidā, lai ievērotu datu atkarības.</span><span class="sxs-lookup"><span data-stu-id="1aae6-151">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="1aae6-152">Pievienot uzkrājumu atlikšanas iemesla kodu (1. jūnijs)</span><span class="sxs-lookup"><span data-stu-id="1aae6-152">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="1aae6-153">Pamatojuma kodi ir pievienoti uzkrāšanas apturēšanai.</span><span class="sxs-lookup"><span data-stu-id="1aae6-153">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="1aae6-154">Pārnešanas kārtulas (1. jūnijs)</span><span class="sxs-lookup"><span data-stu-id="1aae6-154">Carry forward rules (June 1)</span></span>

<span data-ttu-id="1aae6-155">Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas.</span><span class="sxs-lookup"><span data-stu-id="1aae6-155">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="1aae6-156">Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām.</span><span class="sxs-lookup"><span data-stu-id="1aae6-156">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="1aae6-157">Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="1aae6-157">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="1aae6-158">Aizturēt atvaļinājumu uzkrājumu norādīto atvaļinājumu veidiem (1. jūnijs)</span><span class="sxs-lookup"><span data-stu-id="1aae6-158">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="1aae6-159">Šajā laidienā PV var izveidot kārtulu, kas aptur atvaļinājumu uzkrājumus darbiniekiem ar atvaļinājumu pieprasījumiem, kas ievadīti neapmaksātam atvaļinājumam.</span><span class="sxs-lookup"><span data-stu-id="1aae6-159">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="1aae6-160">Neapmaksāts atvaļinājums var būt veids, bet tam nav obligāti jābūt.</span><span class="sxs-lookup"><span data-stu-id="1aae6-160">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="1aae6-161">Jūs varat aizturēt jebkuru atvaļinājumu, pamatojoties uz citu atvaļinājumu veidu.</span><span class="sxs-lookup"><span data-stu-id="1aae6-161">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="1aae6-162">DMF elements ir pieejams uzkrājumu atlikšanai (1. jūnijs)</span><span class="sxs-lookup"><span data-stu-id="1aae6-162">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="1aae6-163">DMF elements tagad ir pieejams uzkrājumu atlikšanai.</span><span class="sxs-lookup"><span data-stu-id="1aae6-163">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="1aae6-164">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="1aae6-164">See also</span></span>

[<span data-ttu-id="1aae6-165">Jaunumi un izmaiņas programmā Human Resources</span><span class="sxs-lookup"><span data-stu-id="1aae6-165">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="1aae6-166">Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu</span><span class="sxs-lookup"><span data-stu-id="1aae6-166">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="1aae6-167">Procesa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="1aae6-167">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="1aae6-168">Līdzekļu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="1aae6-168">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]