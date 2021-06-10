---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 23. jūlijs)
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 23. jūliju.
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e48b0694418710322957de811952e12da22b0509
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055393"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a><span data-ttu-id="c1cba-103">Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 23. jūlijs)</span><span class="sxs-lookup"><span data-stu-id="c1cba-103">What's new or changed in Dynamics 365 Human Resources (July 23, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c1cba-104">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c1cba-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c1cba-105">Izmaiņas attiecas uz būvējuma numuru 8.1.3416.</span><span class="sxs-lookup"><span data-stu-id="c1cba-105">Changes apply to build number 8.1.3416.</span></span> <span data-ttu-id="c1cba-106">Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.</span><span class="sxs-lookup"><span data-stu-id="c1cba-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a><span data-ttu-id="c1cba-107">Finanšu dimensiju dzēšana Pozīcijā nedarbojas, kā paredzēts (445476)</span><span class="sxs-lookup"><span data-stu-id="c1cba-107">Deleting Financial Dimensions on a Position doesn't work as expected (445476)</span></span>

<span data-ttu-id="c1cba-108">Noņemot dimensijas no pozīcijas, tās pašas pozīcijas tiek noņemtas no Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c1cba-108">Removing dimensions from a position now removes those same positions from Dataverse.</span></span>

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a><span data-ttu-id="c1cba-109">Pozīcijas, kas nav hierarhijā, rāda neaktīvās pozīcijas (397257)</span><span class="sxs-lookup"><span data-stu-id="c1cba-109">Positions not in hierarchy show inactive positions (397257)</span></span>

<span data-ttu-id="c1cba-110">Pozīcijas, kas ir neaktīvas (ir beidzies derīguma termiņš), vairs netiek rādītas pozīciju hierarhijā kā **Pozīcijas, kas nav hierarhijā**.</span><span class="sxs-lookup"><span data-stu-id="c1cba-110">Positions that are inactive (have an expired duration), no longer display in the position hierarchy as **Positions not in hierarchy**.</span></span> 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a><span data-ttu-id="c1cba-111">Pārbaude, kas rodas starp LeaveEnrollmentEntity un HcmWorkerEntity Datu pārvaldības struktūras (DMF) importēšanā, izraisa lēnu datu noslodzi (442324)</span><span class="sxs-lookup"><span data-stu-id="c1cba-111">Validation occurring between LeaveEnrollmentEntity and HcmWorkerEntity on Data Management Framework (DMF) import causes slow data loads (442324)</span></span>

<span data-ttu-id="c1cba-112">Šī izlaiduma izmaiņas palielina **LeaveEnrollmentEntity** veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="c1cba-112">Changes in this release increase the performance of **LeaveEnrollmentEntity**.</span></span>

## <a name="unable-to-personalize-in-organization-administration-447490"></a><span data-ttu-id="c1cba-113">Nevar personalizēt Organizācijas administrācijā (447490)</span><span class="sxs-lookup"><span data-stu-id="c1cba-113">Unable to personalize in Organization administration (447490)</span></span>

<span data-ttu-id="c1cba-114">Ar šīm izmaiņām jūs varat personalizēt saites **Organizācijas administrācijā**.</span><span class="sxs-lookup"><span data-stu-id="c1cba-114">With this change, you can now personalize the links in **Organization administration**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="c1cba-115">Priekšskatījumā</span><span class="sxs-lookup"><span data-stu-id="c1cba-115">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="c1cba-116">Obligātie lauki</span><span class="sxs-lookup"><span data-stu-id="c1cba-116">Mandatory fields</span></span> 

<span data-ttu-id="c1cba-117">Tagad ir iespējams padarīt laukus obligātus, izmantojot Personāla vadības personalizēšanas iespējas.</span><span class="sxs-lookup"><span data-stu-id="c1cba-117">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="c1cba-118">Šim līdzeklim nepieciešami **Saglabātie skati**.</span><span class="sxs-lookup"><span data-stu-id="c1cba-118">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="c1cba-119">Programma Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="c1cba-119">Human Resources application in Teams</span></span>

<span data-ttu-id="c1cba-120">Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c1cba-120">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="c1cba-121">Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="c1cba-121">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="c1cba-122">Papildinformāciju skatiet sadaļā [Personāla vadība programms sistēmā Teams](./hr-admin-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="c1cba-122">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="c1cba-123">Datu pārvaldības struktūras (DMF) elementi atvieglojumu pārvaldībai</span><span class="sxs-lookup"><span data-stu-id="c1cba-123">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="c1cba-124">Tiek izlaisti atvieglojumu pārvaldības elementi.</span><span class="sxs-lookup"><span data-stu-id="c1cba-124">Benefits management entities are releasing.</span></span> <span data-ttu-id="c1cba-125">DMF elementi ļauj jums importēt un eksportēt datus, lai viegli konfigurētu atvieglojumu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="c1cba-125">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="c1cba-126">Lai pārvietotu datus, būs pieejama atvieglojumu pārvaldības veidne.</span><span class="sxs-lookup"><span data-stu-id="c1cba-126">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="c1cba-127">Veidne eksportē un importē datus secīgi, lai ievērotu datu atkarības.</span><span class="sxs-lookup"><span data-stu-id="c1cba-127">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="c1cba-128">Atvaļinājuma iegāde un pārdošana</span><span class="sxs-lookup"><span data-stu-id="c1cba-128">Buy and sell leave</span></span> 

<span data-ttu-id="c1cba-129">Dažas organizācijas sniedz atvieglojumus, kas ļauj darbiniekiem pirkt vai pārdot atvaļinājumu.</span><span class="sxs-lookup"><span data-stu-id="c1cba-129">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="c1cba-130">Šo procesu bieži pārvalda manuāli.</span><span class="sxs-lookup"><span data-stu-id="c1cba-130">This process is often managed manually.</span></span> <span data-ttu-id="c1cba-131">Šis līdzeklis automatizē personāla vadības departamenta politikas un pieprasījumu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="c1cba-131">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="c1cba-132">Tas vienkāršo atvaļinājumu pārvaldības procesu un palīdz likvidēt kļūdas.</span><span class="sxs-lookup"><span data-stu-id="c1cba-132">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="c1cba-133">Plašāku informāciju skatiet:</span><span class="sxs-lookup"><span data-stu-id="c1cba-133">For more information, see:</span></span>

- [<span data-ttu-id="c1cba-134">Atvaļinājuma iegādes un pārdošanas politiku pārvaldība</span><span class="sxs-lookup"><span data-stu-id="c1cba-134">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="c1cba-135">Atvaļinājuma iegāde un pārdošana</span><span class="sxs-lookup"><span data-stu-id="c1cba-135">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="c1cba-136">Atstāt uzkrājumu vienam uzņēmumam vai atsevišķam plānam</span><span class="sxs-lookup"><span data-stu-id="c1cba-136">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="c1cba-137">Debitori var apstrādāt uzkrājumus vienam uzņēmumam vai atsevišķam atvaļinājumu un prombūtnes plānam.</span><span class="sxs-lookup"><span data-stu-id="c1cba-137">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="c1cba-138">Šī iespēja nodrošina skaidrību uzkrāšanas procesā debitoriem ar dažādiem atvaļinājumu gadiem vai atvaļinājumu uzkrāšanas politikām.</span><span class="sxs-lookup"><span data-stu-id="c1cba-138">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="c1cba-139">Lai iegūtu papildu informāciju, skatiet [Uzkrāt atvaļinājumu pēc uzņēmuma vai atvaļinājuma plāna](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="c1cba-139">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="c1cba-140">Pielikumu pievienošana brīvā laika pieprasījumiem</span><span class="sxs-lookup"><span data-stu-id="c1cba-140">Add attachments to time-off requests</span></span>

<span data-ttu-id="c1cba-141">Iespēja pievienot pielikumus apstiprinātajiem atvaļinājumu pieprasījumiem ir kritiski nepieciešama pašreizējā COVID-19 vidē.</span><span class="sxs-lookup"><span data-stu-id="c1cba-141">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="c1cba-142">Tagad darbinieki var pievienot šos pielikumus.</span><span class="sxs-lookup"><span data-stu-id="c1cba-142">Employees can now add these attachments.</span></span> <span data-ttu-id="c1cba-143">Tām ir arī vairāk izpratnes par to, kā tiek atjaunināti atvaļinājumu pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="c1cba-143">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="c1cba-144">Lai iegūtu papildu informāciju, skatiet [Pielikumu pievienošana esošam pieprasījumam](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="c1cba-144">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="c1cba-145">Pievienot uzkrājumu atlikšanas iemesla kodu</span><span class="sxs-lookup"><span data-stu-id="c1cba-145">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="c1cba-146">Pamatojuma kodi ir pievienoti uzkrāšanas apturēšanai.</span><span class="sxs-lookup"><span data-stu-id="c1cba-146">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="c1cba-147">Pārnešanas kārtulas</span><span class="sxs-lookup"><span data-stu-id="c1cba-147">Carry forward rules</span></span> 

<span data-ttu-id="c1cba-148">Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas.</span><span class="sxs-lookup"><span data-stu-id="c1cba-148">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="c1cba-149">Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām.</span><span class="sxs-lookup"><span data-stu-id="c1cba-149">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="c1cba-150">Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="c1cba-150">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="c1cba-151">Aizturēt atvaļinājumu uzkrājumu norādīto atvaļinājumu veidiem</span><span class="sxs-lookup"><span data-stu-id="c1cba-151">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="c1cba-152">Jūs varat izveidot kārtulu, kas aptur atvaļinājumu uzkrājumus darbiniekiem ar atvaļinājumu pieprasījumiem, kas ievadīti neapmaksātam atvaļinājumam.</span><span class="sxs-lookup"><span data-stu-id="c1cba-152">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="c1cba-153">Neapmaksāts atvaļinājums var būt veids, bet tam nav obligāti jābūt.</span><span class="sxs-lookup"><span data-stu-id="c1cba-153">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="c1cba-154">Jūs varat aizturēt jebkuru atvaļinājumu, pamatojoties uz citu atvaļinājumu veidu.</span><span class="sxs-lookup"><span data-stu-id="c1cba-154">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="c1cba-155">DMF elements ir pieejams uzkrājumu atlikšanai</span><span class="sxs-lookup"><span data-stu-id="c1cba-155">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="c1cba-156">DMF elements tagad ir pieejams uzkrājumu atlikšanai.</span><span class="sxs-lookup"><span data-stu-id="c1cba-156">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c1cba-157">Drīzumā</span><span class="sxs-lookup"><span data-stu-id="c1cba-157">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="c1cba-158">Kontrolsaraksta entītijas iekļautas Dataverse</span><span class="sxs-lookup"><span data-stu-id="c1cba-158">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="c1cba-159">Kontrolsaraksta elementi Pievienošana, Noņemšana, Pārsūtīšana un Biznesa procesi drīz būs pieejami Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c1cba-159">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="c1cba-160">Platformas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="c1cba-160">Platform changes</span></span>

<span data-ttu-id="c1cba-161">Platformas atjauninājums 10.0.12 (36)</span><span class="sxs-lookup"><span data-stu-id="c1cba-161">Platform update 10.0.12 (36)</span></span>

## <a name="see-also"></a><span data-ttu-id="c1cba-162">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="c1cba-162">See also</span></span>

[<span data-ttu-id="c1cba-163">Jaunumi un izmaiņas programmā Human Resources</span><span class="sxs-lookup"><span data-stu-id="c1cba-163">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="c1cba-164">Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu</span><span class="sxs-lookup"><span data-stu-id="c1cba-164">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="c1cba-165">Procesa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="c1cba-165">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="c1cba-166">Līdzekļu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="c1cba-166">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]