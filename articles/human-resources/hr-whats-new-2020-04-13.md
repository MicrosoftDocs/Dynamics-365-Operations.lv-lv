---
title: Jaunumi vai izmaiņas risinājumā Dynamics 365 Human Resources (2020. gada 13. aprīlis)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 13. aprīli.
author: andreabichsel
ms.date: 04/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2a43b55c075102056ed7c752b72a85f2c9012d46
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051045"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="7d45b-103">Jaunumi vai izmaiņas risinājumā Dynamics 365 Human Resources (2020. gada 13. aprīlis)</span><span class="sxs-lookup"><span data-stu-id="7d45b-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7d45b-104">Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7d45b-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7d45b-105">Izmaiņas attiecas uz būvējuma numuru 8.1.3136.</span><span class="sxs-lookup"><span data-stu-id="7d45b-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="7d45b-106">Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.</span><span class="sxs-lookup"><span data-stu-id="7d45b-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="7d45b-107">Jauns ražošanas laidiena ritms</span><span class="sxs-lookup"><span data-stu-id="7d45b-107">New production release cadence</span></span>

<span data-ttu-id="7d45b-108">Ar šīs nedēļas laidienu Personāla vadības laidienu ritms mainās no iknedēļas atjauninājumiem uz atjauninājumiem reizi divās nedēļās.</span><span class="sxs-lookup"><span data-stu-id="7d45b-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="7d45b-109">Lai nodrošinātu saskaņotību ar drošām izvietošanas praksēm, kā arī uzturētu augstus stabilitātes un uzticamības standartus pakalpojumā, pakalpojumu atjauninājumu izvietošanas process visiem reģioniem tagad ir divu nedēļu izvēršana.</span><span class="sxs-lookup"><span data-stu-id="7d45b-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="7d45b-110">Ir paredzēta papildu pārbaudes un uzraudzība, lai nodrošinātu veiksmīgu izvietošanu katrā procesa posmā.</span><span class="sxs-lookup"><span data-stu-id="7d45b-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="7d45b-111">Lai iegūtu papildu informāciju par laidiena ritmu skatiet rakstu [Atjaunināšanas process](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="7d45b-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="7d45b-112">Noapaļošanas precizitātes lauks nav rediģējams pēc Noapaļošanas veida norādīšanas (435616)</span><span class="sxs-lookup"><span data-stu-id="7d45b-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="7d45b-113">Ar šī izmaiņām lauks **Noapaļošanas precizitāte** tagad ir pieejams pēc lauka **Noapaļošanas veids** atjaunināšanas.</span><span class="sxs-lookup"><span data-stu-id="7d45b-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="7d45b-114">Nevar rediģēt atvaļinājuma reģistrācijas beigu datumu, kad atvaļinājumu plānam nav uzkrāšanas periodu (413628)</span><span class="sxs-lookup"><span data-stu-id="7d45b-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="7d45b-115">Tagad varat rediģēt reģistrācijas beigu datumu, neuzrādot kļūdu "Jānorāda lauka uzkrāšanas datums."</span><span class="sxs-lookup"><span data-stu-id="7d45b-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a><span data-ttu-id="7d45b-116">Nodarbinātības elements nav sinhronizēts ar Dataverse (430834)</span><span class="sxs-lookup"><span data-stu-id="7d45b-116">Employment entity doesn't sync to Dataverse (430834)</span></span>

<span data-ttu-id="7d45b-117">Šīs izmaiņas labo problēmu, kad nodarbinātības dati netika sinhronizēti ar Dataverse pēc finanšu dimensiju pievienošanas.</span><span class="sxs-lookup"><span data-stu-id="7d45b-117">This change corrects an issue where the employment data wasn't syncing to Dataverse after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="7d45b-118">Noņemt vairāku vecāku izmantošanu Darba kalendāra laika intervāla elementam (431775)</span><span class="sxs-lookup"><span data-stu-id="7d45b-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="7d45b-119">Šīs izmaiņas noņem vairāku vecāku izmantošanu **Darba kalendāra laika intervāla** elementam.</span><span class="sxs-lookup"><span data-stu-id="7d45b-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="7d45b-120">Filtrs ar CAST funkciju nedarbojas uz OData zvana Pozīcijas darbinieka piešķires elementā (431699)</span><span class="sxs-lookup"><span data-stu-id="7d45b-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="7d45b-121">Šis atjauninājums ietver izmaiņas, lai atļautu filtru ar CAST funkciju, kas ir OData **Pozīcijas darbinieka piešķires** elementam.</span><span class="sxs-lookup"><span data-stu-id="7d45b-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="7d45b-122">Priekšskatījumā</span><span class="sxs-lookup"><span data-stu-id="7d45b-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="7d45b-123">Atvaļinājuma atlikšana</span><span class="sxs-lookup"><span data-stu-id="7d45b-123">Leave suspension</span></span>

<span data-ttu-id="7d45b-124">Jūs varat atlikt atvaļinājumu un prombūtni darbiniekam Personāla vadības programmā.</span><span class="sxs-lookup"><span data-stu-id="7d45b-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="7d45b-125">Aizturot atvaļinājumu, tiek apturēti atvaļinājumu uzkrājumi atsevišķiem atvaļinājumu veidiem.</span><span class="sxs-lookup"><span data-stu-id="7d45b-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="7d45b-126">Ja atlikšana notiek pēc uzkrājumu procesa, aizturētā atvaļinājuma rezultātā izveido proporcionālu pārrēķinu darbinieka atvaļinājuma bilancei.</span><span class="sxs-lookup"><span data-stu-id="7d45b-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="7d45b-127">Papildinformāciju skatiet [Aizturēt atvaļinājumu](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="7d45b-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="7d45b-128">Pārnešanas kārtulas</span><span class="sxs-lookup"><span data-stu-id="7d45b-128">Carry forward rules</span></span>

<span data-ttu-id="7d45b-129">Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas.</span><span class="sxs-lookup"><span data-stu-id="7d45b-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="7d45b-130">Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām.</span><span class="sxs-lookup"><span data-stu-id="7d45b-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="7d45b-131">Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="7d45b-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="7d45b-132">Zināmās problēmas</span><span class="sxs-lookup"><span data-stu-id="7d45b-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="7d45b-133">Nodarbinātības informācijas elements</span><span class="sxs-lookup"><span data-stu-id="7d45b-133">Employment Details entity</span></span>

<span data-ttu-id="7d45b-134">**Nodarbinātības informācijas** elements ir atjaunināts ar šādiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="7d45b-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="7d45b-135">**PayFrequency**</span><span class="sxs-lookup"><span data-stu-id="7d45b-135">**PayFrequency**</span></span>
- <span data-ttu-id="7d45b-136">**Nodarbinātības kategorijas ID**</span><span class="sxs-lookup"><span data-stu-id="7d45b-136">**Employment Category ID**</span></span>
- <span data-ttu-id="7d45b-137">**Nodarbinātības veids**</span><span class="sxs-lookup"><span data-stu-id="7d45b-137">**Employment Type**</span></span>
- <span data-ttu-id="7d45b-138">**EmploymentType ID**</span><span class="sxs-lookup"><span data-stu-id="7d45b-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="7d45b-139">**Pabalstu nodarbinātības statuss**</span><span class="sxs-lookup"><span data-stu-id="7d45b-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="7d45b-140">Šo lauku iestatīšanas dati paļaujas uz atvieglojumu pārvaldību, kas ir iespējota **Līdzekļu pārvaldības** darbvietā.</span><span class="sxs-lookup"><span data-stu-id="7d45b-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="7d45b-141">Neaizpildiet vai neatjauniniet šos laukus **Nodarbinātības informācijas** elementā, jo importēšanas laikā radīsies kļūdas.</span><span class="sxs-lookup"><span data-stu-id="7d45b-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="7d45b-142">SharePoint priekšskatījums dažās vidēs nedarbojas</span><span class="sxs-lookup"><span data-stu-id="7d45b-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="7d45b-143">Ja dokumenta priekšskatījums dokumentiem, kas saglabāti SharePoint programmā, nedarbojas, veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="7d45b-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="7d45b-144">Pārbaudiet, vai administratora lietotāja kontam ir e-pasts, kas saistīts ar lietotāja ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7d45b-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="7d45b-145">Šo informāciju varat aplūkot lapā **Lietotājs**.</span><span class="sxs-lookup"><span data-stu-id="7d45b-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="7d45b-146">Ja e-pasta ziņojums nav iestatīts, e-pasta ziņojums un nodrošinātājs ir jāpievieno, izmantojot OData Excel pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="7d45b-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="7d45b-147">Pēc noklusējuma e-pasta adrese nav atrodama Excel noformējumā.</span><span class="sxs-lookup"><span data-stu-id="7d45b-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="7d45b-148">Jums vajadzēs rediģēt Excel noformējumu, pievienot visus laukus, piemērot un atsvaidzināt.</span><span class="sxs-lookup"><span data-stu-id="7d45b-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="7d45b-149">Kad šīs darbības ir izpildītas, varat atjaunināt administratora kontu.</span><span class="sxs-lookup"><span data-stu-id="7d45b-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="7d45b-150">Pēc tam, kad administratora kontam ir saistītais e-pasta konts, piesakieties pakalpojumā Human Resources ar administratora akreditācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="7d45b-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="7d45b-151">Lai sāktu dokumenta priekšskatījumu, piekļūstiet SharePoint pielikumam.</span><span class="sxs-lookup"><span data-stu-id="7d45b-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="7d45b-152">Piesakieties ar citu lietotāja kontu, kam ir piekļuve pielikumiem, un apstipriniet, ka priekšskatījums darbojas kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="7d45b-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d45b-153">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="7d45b-153">See also</span></span>

[<span data-ttu-id="7d45b-154">Jaunumi un izmaiņas programmā Human Resources</span><span class="sxs-lookup"><span data-stu-id="7d45b-154">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="7d45b-155">Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu</span><span class="sxs-lookup"><span data-stu-id="7d45b-155">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="7d45b-156">Procesa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="7d45b-156">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="7d45b-157">Līdzekļu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="7d45b-157">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]