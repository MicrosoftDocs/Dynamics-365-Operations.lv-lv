---
title: Jaunumi un izmaiņas programmatūrā Dynamics 365 Human Resources (2020. gada 11. jūnijs)
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 11. jūniju.
author: andreabichsel
ms.date: 06/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8265c0b6218f69b95f2729140aa303edeaa31443
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891941"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="77c54-103">Jaunumi un izmaiņas programmatūrā Dynamics 365 Human Resources (2020. gada 11. jūnijs)</span><span class="sxs-lookup"><span data-stu-id="77c54-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="77c54-104">Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="77c54-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="77c54-105">Izmaiņas attiecas uz būvējuma numuru 8.1.3316.</span><span class="sxs-lookup"><span data-stu-id="77c54-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="77c54-106">Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.</span><span class="sxs-lookup"><span data-stu-id="77c54-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="77c54-107">Vienkāršota darbinieka veidlapa dažreiz izraisa atvašu veidlapas slēgšanas (X) pogas darba pārtraukšanu (442369)</span><span class="sxs-lookup"><span data-stu-id="77c54-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="77c54-108">Kad ir iespējota jaunā **Darbinieka** veidlapa, poga Aizvērt (**X**) reizēm nedarbojās pakārtotās veidlapās.</span><span class="sxs-lookup"><span data-stu-id="77c54-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="77c54-109">Šī problēma bija intermitējoša.</span><span class="sxs-lookup"><span data-stu-id="77c54-109">This problem was intermittent.</span></span> <span data-ttu-id="77c54-110">Šo veidlapu var aizvērt pēc aiziešanas un atgriešanās pie tās.</span><span class="sxs-lookup"><span data-stu-id="77c54-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="77c54-111">Piemēram, varat atlasīt izvēlnes elementu kreisajā pusē un pārvietoties uz **Darbinieku** veidlapu, un pēc tam aizvērt to.</span><span class="sxs-lookup"><span data-stu-id="77c54-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="77c54-112">Šīs nedēļas laidiens salabo šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="77c54-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="77c54-113">Darbinieka personīgās kontaktpersonas entītija neeksportē personīgos kontaktus ar pamata attiecību tipu</span><span class="sxs-lookup"><span data-stu-id="77c54-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="77c54-114">Ar šo laidienu **Darbinieka personīgās kontaktpersonas** entītija eksportē visus attiecību tipus.</span><span class="sxs-lookup"><span data-stu-id="77c54-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="77c54-115">HcmPositionWorkerAssignmentV2Entity ir jābūt daļai no Ceridian algu integrācijas pakotnes pēc noklusējuma (448506)</span><span class="sxs-lookup"><span data-stu-id="77c54-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="77c54-116">Ar šīm izmaiņām **HcmPositionWorkerAssignmentV2Entity** ir iekļauts Ceridian algu integrācijas pakotnē.</span><span class="sxs-lookup"><span data-stu-id="77c54-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="77c54-117">Priekšskatījumā</span><span class="sxs-lookup"><span data-stu-id="77c54-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="77c54-118">Datu bāzes reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="77c54-118">Database logging</span></span>

<span data-ttu-id="77c54-119">Datu bāzes reģistrācijas līdzeklis ļauj noteikt, kura tabulas un lauki ir jāpārrauga.</span><span class="sxs-lookup"><span data-stu-id="77c54-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="77c54-120">Tas arī ļauj noteikt notikumus, kam jāizraisa izmaiņu izsekošana.</span><span class="sxs-lookup"><span data-stu-id="77c54-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="77c54-121">Jūs izmantojat datu bāzes reģistrācijas iespējas, lai skatītu šīs izmaiņas laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="77c54-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="77c54-122">Papildinformāciju skatiet [Datu bāzes reģistrācijas konfigurēšana un pārvaldība](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="77c54-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="77c54-123">Programma Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="77c54-123">Human Resources application in Teams</span></span>

<span data-ttu-id="77c54-124">Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="77c54-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="77c54-125">Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="77c54-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="77c54-126">Papildinformāciju skatiet sadaļā [Personāla vadība programms sistēmā Teams](./hr-admin-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="77c54-126">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="77c54-127">Datu pārvaldības struktūras (DMF) elementi atvieglojumu pārvaldībai</span><span class="sxs-lookup"><span data-stu-id="77c54-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="77c54-128">Tiek izlaisti atvieglojumu pārvaldības elementi.</span><span class="sxs-lookup"><span data-stu-id="77c54-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="77c54-129">DMF elementi ļauj jums importēt un eksportēt datus, lai viegli konfigurētu atvieglojumu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="77c54-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="77c54-130">Lai pārvietotu datus, būs pieejama atvieglojumu pārvaldības veidne.</span><span class="sxs-lookup"><span data-stu-id="77c54-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="77c54-131">Veidne eksportē un importē datus secīgi, lai ievērotu datu atkarības.</span><span class="sxs-lookup"><span data-stu-id="77c54-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="77c54-132">Atvaļinājuma iegāde un pārdošana</span><span class="sxs-lookup"><span data-stu-id="77c54-132">Buy and sell leave</span></span> 

<span data-ttu-id="77c54-133">Dažas organizācijas sniedz atvieglojumus, kas ļauj darbiniekiem pirkt vai pārdot atvaļinājumu.</span><span class="sxs-lookup"><span data-stu-id="77c54-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="77c54-134">Šo procesu bieži pārvalda manuāli.</span><span class="sxs-lookup"><span data-stu-id="77c54-134">This process is often managed manually.</span></span> <span data-ttu-id="77c54-135">Šis līdzeklis automatizē personāla vadības departamenta politikas un pieprasījumu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="77c54-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="77c54-136">Tas vienkāršo atvaļinājumu pārvaldības procesu un palīdz likvidēt kļūdas.</span><span class="sxs-lookup"><span data-stu-id="77c54-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="77c54-137">Plašāku informāciju skatiet:</span><span class="sxs-lookup"><span data-stu-id="77c54-137">For more information, see:</span></span>

- [<span data-ttu-id="77c54-138">Atvaļinājuma iegādes un pārdošanas politiku pārvaldība</span><span class="sxs-lookup"><span data-stu-id="77c54-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="77c54-139">Atvaļinājuma iegāde un pārdošana</span><span class="sxs-lookup"><span data-stu-id="77c54-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="77c54-140">Atstāt uzkrājumu vienam uzņēmumam vai atsevišķam plānam</span><span class="sxs-lookup"><span data-stu-id="77c54-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="77c54-141">Debitori var apstrādāt uzkrājumus vienam uzņēmumam vai atsevišķam atvaļinājumu un prombūtnes plānam.</span><span class="sxs-lookup"><span data-stu-id="77c54-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="77c54-142">Šī spēja nodrošina skaidrību uzkrāšanas procesā debitoriem ar dažādiem atvaļinājumu gadiem vai atvaļinājuma uzkrāšanas politikām.</span><span class="sxs-lookup"><span data-stu-id="77c54-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="77c54-143">Lai iegūtu papildu informāciju, skatiet [Uzkrāt atvaļinājumu pēc uzņēmuma vai atvaļinājuma plāna](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="77c54-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="77c54-144">Pievienojiet pielikumus brīvā laika pieprasījumiem</span><span class="sxs-lookup"><span data-stu-id="77c54-144">Add attachments to time off requests</span></span>

<span data-ttu-id="77c54-145">Iespēja pievienot pielikumus apstiprinātajiem atvaļinājumu pieprasījumiem ir kritiski nepieciešama pašreizējā COVID-19 vidē.</span><span class="sxs-lookup"><span data-stu-id="77c54-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="77c54-146">Tagad darbinieki var pievienot šos pielikumus.</span><span class="sxs-lookup"><span data-stu-id="77c54-146">Employees can now add these attachments.</span></span> <span data-ttu-id="77c54-147">Tām ir arī vairāk izpratnes par to, kā tiek atjaunināti atvaļinājumu pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="77c54-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="77c54-148">Lai iegūtu papildu informāciju, skatiet [Pielikumu pievienošana esošam pieprasījumam](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="77c54-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="77c54-149">Pievienot uzkrājumu atlikšanas iemesla kodu</span><span class="sxs-lookup"><span data-stu-id="77c54-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="77c54-150">Pamatojuma kodi ir pievienoti uzkrāšanas apturēšanai.</span><span class="sxs-lookup"><span data-stu-id="77c54-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="77c54-151">Pārnešanas kārtulas</span><span class="sxs-lookup"><span data-stu-id="77c54-151">Carry forward rules</span></span> 

<span data-ttu-id="77c54-152">Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas.</span><span class="sxs-lookup"><span data-stu-id="77c54-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="77c54-153">Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām.</span><span class="sxs-lookup"><span data-stu-id="77c54-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="77c54-154">Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="77c54-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="77c54-155">Aizturēt atvaļinājumu uzkrājumu norādīto atvaļinājumu veidiem</span><span class="sxs-lookup"><span data-stu-id="77c54-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="77c54-156">Jūs varat izveidot kārtulu, kas aptur atvaļinājumu uzkrājumus darbiniekiem ar atvaļinājumu pieprasījumiem, kas ievadīti neapmaksātam atvaļinājumam.</span><span class="sxs-lookup"><span data-stu-id="77c54-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="77c54-157">Neapmaksāts atvaļinājums var būt veids, bet tam nav obligāti jābūt.</span><span class="sxs-lookup"><span data-stu-id="77c54-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="77c54-158">Jūs varat aizturēt jebkuru atvaļinājumu, pamatojoties uz citu atvaļinājumu veidu.</span><span class="sxs-lookup"><span data-stu-id="77c54-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="77c54-159">DMF elements ir pieejams uzkrājumu atlikšanai</span><span class="sxs-lookup"><span data-stu-id="77c54-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="77c54-160">DMF elements tagad ir pieejams uzkrājumu atlikšanai.</span><span class="sxs-lookup"><span data-stu-id="77c54-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="77c54-161">Drīzumā</span><span class="sxs-lookup"><span data-stu-id="77c54-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="77c54-162">Jaunas platformas iespējas</span><span class="sxs-lookup"><span data-stu-id="77c54-162">New platform capabilities</span></span> 

<span data-ttu-id="77c54-163">Jūs varēsit padarīt laukus obligātus, izmantojot personalizāciju.</span><span class="sxs-lookup"><span data-stu-id="77c54-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="77c54-164">Šim līdzeklim būs nepieciešams iespējot **Saglabātos skatus**.</span><span class="sxs-lookup"><span data-stu-id="77c54-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="77c54-165">Konfigurēt Darbinieku pašapkalpošanās nosaukumu</span><span class="sxs-lookup"><span data-stu-id="77c54-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="77c54-166">Personāla vadības parametros būs pieejama jauna opcija, lai atjauninātu Darbinieku pašapkalpošanās darbvietas nosaukumu uz Pašapkalpošanās.</span><span class="sxs-lookup"><span data-stu-id="77c54-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="77c54-167">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="77c54-167">See also</span></span>

[<span data-ttu-id="77c54-168">Jaunumi un izmaiņas programmā Human Resources</span><span class="sxs-lookup"><span data-stu-id="77c54-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="77c54-169">Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu</span><span class="sxs-lookup"><span data-stu-id="77c54-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="77c54-170">Procesa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="77c54-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="77c54-171">Līdzekļu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="77c54-171">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]