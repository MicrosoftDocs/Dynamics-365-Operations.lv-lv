---
title: Jaunumi un izmaiņas programmatūrā Dynamics 365 Human Resources (2020. gada 25. jūnijs)
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 23. jūniju.
author: andreabichsel
ms.date: 06/25/2020
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
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 228883dd4af3f4f51c53524813c1852d392c1d29
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053951"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a><span data-ttu-id="016bc-103">Jaunumi un izmaiņas programmatūrā Dynamics 365 Human Resources (2020. gada 23. jūnijs)</span><span class="sxs-lookup"><span data-stu-id="016bc-103">What's new or changed in Dynamics 365 Human Resources (June 23, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="016bc-104">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="016bc-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="016bc-105">Izmaiņas attiecas uz būvējuma numuru 8.1.3347.</span><span class="sxs-lookup"><span data-stu-id="016bc-105">Changes apply to build number 8.1.3347.</span></span> <span data-ttu-id="016bc-106">Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.</span><span class="sxs-lookup"><span data-stu-id="016bc-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a><span data-ttu-id="016bc-107">Beidzoties reģistrācijai, darbinieka atvaļinājuma veids, bilance un summa tiek dzēsti Atvaļinājuma reģistrācijas formā (444867)</span><span class="sxs-lookup"><span data-stu-id="016bc-107">When an enrollment is expired for a terminated employee, the leave type, balance, and amount are all cleared in the Leave enrollment form (444867)</span></span>

<span data-ttu-id="016bc-108">Tagad, veicot šo atlasi, **Atvaļinājuma veids**, **Bilance** un **Summa** vērtības tiek uzturētas, nevis dzēstas.</span><span class="sxs-lookup"><span data-stu-id="016bc-108">Values in the **Leave type**, **Balance**, and **Amount** are now maintained instead of cleared upon making this selection.</span></span>

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a><span data-ttu-id="016bc-109">Prognozētā bilance nav pareiza, ja ir iespējots jauns līdzeklis (Atvaļinājuma uzkrājums vienam uzņēmumam vai vienam plānam) (456553)</span><span class="sxs-lookup"><span data-stu-id="016bc-109">Incorrect forecasted balance when new feature (Leave accrual for a single company or a single plan) is enabled (456553)</span></span>

<span data-ttu-id="016bc-110">Pareizā prognozētā bilance tagad tiek parādīta, kad ir iespējots viena uzņēmuma vai viena plāna atvaļinājuma uzkrājums.</span><span class="sxs-lookup"><span data-stu-id="016bc-110">The correct forecasted balance now displays when the leave accrual for a single company or single plan has been enabled.</span></span>

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a><span data-ttu-id="016bc-111">EntītIjas ar relācijām, kuru rezultātā tiek dublēti navigācijas rekvizīti (456486)</span><span class="sxs-lookup"><span data-stu-id="016bc-111">Entities with relations that result in duplicate navigation properties (456486)</span></span>

<span data-ttu-id="016bc-112">Šis laidiens novērš problēmu ar vairāku entītiju navigācijas rekvizītiem (relācija).</span><span class="sxs-lookup"><span data-stu-id="016bc-112">This release corrects an issue with the navigation properties (relation) of multiple entities.</span></span> <span data-ttu-id="016bc-113">Tiek noteiktas dublikātu relācijas.</span><span class="sxs-lookup"><span data-stu-id="016bc-113">Duplicate relations are detected.</span></span> <span data-ttu-id="016bc-114">Šie scenāriji ir izlaboti.</span><span class="sxs-lookup"><span data-stu-id="016bc-114">These scenarios have all been corrected.</span></span>
 
## <a name="cross-company-comments-on-performance-review-455536"></a><span data-ttu-id="016bc-115">Starpuzņēmuma komentāri par Veiktspējas pārskatu (455536)</span><span class="sxs-lookup"><span data-stu-id="016bc-115">Cross-company comments on Performance review (455536)</span></span>

<span data-ttu-id="016bc-116">Starpuzņēmumu komentāri tagad ir redzami veiktspējas pārskatos ar šo labojumu.</span><span class="sxs-lookup"><span data-stu-id="016bc-116">Cross-company comments are now visible on performance reviews with this fix.</span></span> <span data-ttu-id="016bc-117">Šī izmaiņa labo pārskatītāja komentāru skatu, kas tika ievadīti dažādos uzņēmumos vienam veiktspējas pārskatam.</span><span class="sxs-lookup"><span data-stu-id="016bc-117">This change corrects the view of reviewer comments that were entered in different companies for the same performance review.</span></span>
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a><span data-ttu-id="016bc-118">Nekonsekvence, parādot atlīdzības pārvaldības datus (432562)</span><span class="sxs-lookup"><span data-stu-id="016bc-118">Inconsistency in showing compensation management data (432562)</span></span>

<span data-ttu-id="016bc-119">Saskaņots atlīdzības datu skats tagad tiek uzturēts Vadītāja pašapkalpošanās pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="016bc-119">A consistent view of compensation data is now maintained in Manager self service.</span></span> <span data-ttu-id="016bc-120">Atkarībā no tā, kā pārvietojaties uz darbinieka **Atlīdzības informāciju**, atlīdzības dati tagad pastāvīgi tiek parādīti vadītājiem.</span><span class="sxs-lookup"><span data-stu-id="016bc-120">Depending on how you navigate to a worker's **Compensation details**, compensation data now consistently displays to managers.</span></span>
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a><span data-ttu-id="016bc-121">Fiksētās atlīdzības plāna spēkā stāšanās datums pēc noklusējuma ir šodienas datums (411994)</span><span class="sxs-lookup"><span data-stu-id="016bc-121">Fixed compensation plan's effective date defaults to today's date (411994)</span></span>

<span data-ttu-id="016bc-122">Atlīdzības sākuma datums tagad ir balstīts uz darbiniekam piešķirtā amata sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="016bc-122">The compensation start date is now based on the start date of the position being assigned to the employee.</span></span>

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a><span data-ttu-id="016bc-123">Atvaļinājuma un kavējuma forma iespējot pusi dienas definīciju tiek atspējota, atverot formu (452607)</span><span class="sxs-lookup"><span data-stu-id="016bc-123">Leave and absence form Enable half day definition is disabled when form opens (452607)</span></span>

<span data-ttu-id="016bc-124">Ar šīm izmaiņām **Iespējot pusi dienas definīciju** tiks aktivizēta, līdz jaunam atvaļinājuma darījumam.</span><span class="sxs-lookup"><span data-stu-id="016bc-124">With this change, the **Enable half day definition** will be enabled until new leave transactions exist.</span></span> 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a><span data-ttu-id="016bc-125">Nevar publicēt programmā HcmDiscussionEntity, izmantojot Excel; TotalRatingScore lauka kļūda (453899)</span><span class="sxs-lookup"><span data-stu-id="016bc-125">Unable to publish to HcmDiscussionEntity via Excel; TotalRatingScore field error (453899)</span></span>

<span data-ttu-id="016bc-126">Tagad varat atjaunināt lauku **TotalRatingScore**, izmantojot **HCMDiscussionEntity** Excel darbgrāmatas veidotājā.</span><span class="sxs-lookup"><span data-stu-id="016bc-126">You can now update the **TotalRatingScore** field using **HCMDiscussionEntity** in the Excel workbook designer.</span></span>

## <a name="in-preview"></a><span data-ttu-id="016bc-127">Priekšskatījumā</span><span class="sxs-lookup"><span data-stu-id="016bc-127">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="016bc-128">Datu bāzes reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="016bc-128">Database logging</span></span>

<span data-ttu-id="016bc-129">Datu bāzes reģistrācija ļauj noteikt, kuras tabulas un laukus ir pārraudzīt.</span><span class="sxs-lookup"><span data-stu-id="016bc-129">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="016bc-130">Tas arī ļauj noteikt notikumus, kam jāizraisa izmaiņu izsekošana.</span><span class="sxs-lookup"><span data-stu-id="016bc-130">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="016bc-131">Jūs izmantojat datu bāzes reģistrācijas iespējas, lai skatītu šīs izmaiņas laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="016bc-131">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="016bc-132">Papildinformāciju skatiet [Datu bāzes reģistrācijas konfigurēšana un pārvaldība](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="016bc-132">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="016bc-133">Obligātie lauki</span><span class="sxs-lookup"><span data-stu-id="016bc-133">Mandatory fields</span></span> 

<span data-ttu-id="016bc-134">Tagad ir iespējams padarīt laukus obligātus, izmantojot Personāla vadības personalizēšanas iespējas.</span><span class="sxs-lookup"><span data-stu-id="016bc-134">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="016bc-135">Šim līdzeklim nepieciešami **Saglabātie skati**.</span><span class="sxs-lookup"><span data-stu-id="016bc-135">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="016bc-136">Programma Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="016bc-136">Human Resources application in Teams</span></span>

<span data-ttu-id="016bc-137">Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="016bc-137">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="016bc-138">Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="016bc-138">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="016bc-139">Papildinformāciju skatiet sadaļā [Personāla vadība programms sistēmā Teams](./hr-admin-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="016bc-139">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="016bc-140">Datu pārvaldības struktūras (DMF) elementi atvieglojumu pārvaldībai</span><span class="sxs-lookup"><span data-stu-id="016bc-140">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="016bc-141">Tiek izlaisti atvieglojumu pārvaldības elementi.</span><span class="sxs-lookup"><span data-stu-id="016bc-141">Benefits management entities are releasing.</span></span> <span data-ttu-id="016bc-142">DMF elementi ļauj jums importēt un eksportēt datus, lai viegli konfigurētu atvieglojumu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="016bc-142">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="016bc-143">Lai pārvietotu datus, būs pieejama atvieglojumu pārvaldības veidne.</span><span class="sxs-lookup"><span data-stu-id="016bc-143">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="016bc-144">Veidne eksportē un importē datus secīgi, lai ievērotu datu atkarības.</span><span class="sxs-lookup"><span data-stu-id="016bc-144">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="016bc-145">Atvaļinājuma iegāde un pārdošana</span><span class="sxs-lookup"><span data-stu-id="016bc-145">Buy and sell leave</span></span> 

<span data-ttu-id="016bc-146">Dažas organizācijas sniedz atvieglojumus, kas ļauj darbiniekiem pirkt vai pārdot atvaļinājumu.</span><span class="sxs-lookup"><span data-stu-id="016bc-146">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="016bc-147">Šo procesu bieži pārvalda manuāli.</span><span class="sxs-lookup"><span data-stu-id="016bc-147">This process is often managed manually.</span></span> <span data-ttu-id="016bc-148">Šis līdzeklis automatizē personāla vadības departamenta politikas un pieprasījumu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="016bc-148">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="016bc-149">Tas vienkāršo atvaļinājumu pārvaldības procesu un palīdz likvidēt kļūdas.</span><span class="sxs-lookup"><span data-stu-id="016bc-149">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="016bc-150">Plašāku informāciju skatiet:</span><span class="sxs-lookup"><span data-stu-id="016bc-150">For more information, see:</span></span>

- [<span data-ttu-id="016bc-151">Atvaļinājuma iegādes un pārdošanas politiku pārvaldība</span><span class="sxs-lookup"><span data-stu-id="016bc-151">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="016bc-152">Atvaļinājuma iegāde un pārdošana</span><span class="sxs-lookup"><span data-stu-id="016bc-152">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="016bc-153">Atstāt uzkrājumu vienam uzņēmumam vai atsevišķam plānam</span><span class="sxs-lookup"><span data-stu-id="016bc-153">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="016bc-154">Debitori var apstrādāt uzkrājumus vienam uzņēmumam vai atsevišķam atvaļinājumu un prombūtnes plānam.</span><span class="sxs-lookup"><span data-stu-id="016bc-154">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="016bc-155">Šī spēja nodrošina skaidrību uzkrāšanas procesā debitoriem ar dažādiem atvaļinājumu gadiem vai atvaļinājuma uzkrāšanas politikām.</span><span class="sxs-lookup"><span data-stu-id="016bc-155">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="016bc-156">Lai iegūtu papildu informāciju, skatiet [Uzkrāt atvaļinājumu pēc uzņēmuma vai atvaļinājuma plāna](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="016bc-156">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="016bc-157">Pievienojiet pielikumus brīvā laika pieprasījumiem</span><span class="sxs-lookup"><span data-stu-id="016bc-157">Add attachments to time off requests</span></span>

<span data-ttu-id="016bc-158">Iespēja pievienot pielikumus apstiprinātajiem atvaļinājumu pieprasījumiem ir kritiski nepieciešama pašreizējā COVID-19 vidē.</span><span class="sxs-lookup"><span data-stu-id="016bc-158">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="016bc-159">Tagad darbinieki var pievienot šos pielikumus.</span><span class="sxs-lookup"><span data-stu-id="016bc-159">Employees can now add these attachments.</span></span> <span data-ttu-id="016bc-160">Tām ir arī vairāk izpratnes par to, kā tiek atjaunināti atvaļinājumu pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="016bc-160">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="016bc-161">Lai iegūtu papildu informāciju, skatiet [Pielikumu pievienošana esošam pieprasījumam](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="016bc-161">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="016bc-162">Pievienot uzkrājumu atlikšanas iemesla kodu</span><span class="sxs-lookup"><span data-stu-id="016bc-162">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="016bc-163">Pamatojuma kodi ir pievienoti uzkrāšanas apturēšanai.</span><span class="sxs-lookup"><span data-stu-id="016bc-163">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="016bc-164">Pārnešanas kārtulas</span><span class="sxs-lookup"><span data-stu-id="016bc-164">Carry forward rules</span></span> 

<span data-ttu-id="016bc-165">Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas.</span><span class="sxs-lookup"><span data-stu-id="016bc-165">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="016bc-166">Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām.</span><span class="sxs-lookup"><span data-stu-id="016bc-166">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="016bc-167">Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="016bc-167">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="016bc-168">Aizturēt atvaļinājumu uzkrājumu norādīto atvaļinājumu veidiem</span><span class="sxs-lookup"><span data-stu-id="016bc-168">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="016bc-169">Jūs varat izveidot kārtulu, kas aptur atvaļinājumu uzkrājumus darbiniekiem ar atvaļinājumu pieprasījumiem, kas ievadīti neapmaksātam atvaļinājumam.</span><span class="sxs-lookup"><span data-stu-id="016bc-169">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="016bc-170">Neapmaksāts atvaļinājums var būt veids, bet tam nav obligāti jābūt.</span><span class="sxs-lookup"><span data-stu-id="016bc-170">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="016bc-171">Jūs varat aizturēt jebkuru atvaļinājumu, pamatojoties uz citu atvaļinājumu veidu.</span><span class="sxs-lookup"><span data-stu-id="016bc-171">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="016bc-172">DMF elements ir pieejams uzkrājumu atlikšanai</span><span class="sxs-lookup"><span data-stu-id="016bc-172">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="016bc-173">DMF elements tagad ir pieejams uzkrājumu atlikšanai.</span><span class="sxs-lookup"><span data-stu-id="016bc-173">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="016bc-174">Drīzumā</span><span class="sxs-lookup"><span data-stu-id="016bc-174">Coming soon</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="016bc-175">Konfigurēt Darbinieku pašapkalpošanās nosaukumu</span><span class="sxs-lookup"><span data-stu-id="016bc-175">Configure the name of Employee self-service</span></span>

<span data-ttu-id="016bc-176">**Personāla vadības parametros** būs pieejama jauna opcija, lai atjauninātu Darbinieku pašapkalpošanās darbvietas nosaukumu uz Pašapkalpošanās.</span><span class="sxs-lookup"><span data-stu-id="016bc-176">A new option will be available in **Human Resources parameters** to update the name of the Employee self service workspace to Self service.</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="016bc-177">Kontrolsaraksta entītijas iekļautas Dataverse</span><span class="sxs-lookup"><span data-stu-id="016bc-177">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="016bc-178">Kontrolsaraksta entītijas Pievienošana, Noņemšana, Pārsūtīšana un Biznesa procesi drīz būs pieejamas Dataverse.</span><span class="sxs-lookup"><span data-stu-id="016bc-178">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon within Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="016bc-179">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="016bc-179">See also</span></span>

[<span data-ttu-id="016bc-180">Jaunumi un izmaiņas programmā Human Resources</span><span class="sxs-lookup"><span data-stu-id="016bc-180">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="016bc-181">Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu</span><span class="sxs-lookup"><span data-stu-id="016bc-181">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="016bc-182">Procesa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="016bc-182">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="016bc-183">Līdzekļu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="016bc-183">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]