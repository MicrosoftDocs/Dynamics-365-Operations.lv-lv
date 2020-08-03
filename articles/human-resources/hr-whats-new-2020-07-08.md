---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 08. jūlijs)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 7/08/2020
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
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8fe7bc33407bd5781d565f854c0f096766da5fc9
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555392"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="534a2-103">Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 8. jūlijs)</span><span class="sxs-lookup"><span data-stu-id="534a2-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

<span data-ttu-id="534a2-104">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="534a2-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="534a2-105">Izmaiņas attiecas uz būvējuma numuru 8.1.3382.</span><span class="sxs-lookup"><span data-stu-id="534a2-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="534a2-106">Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.</span><span class="sxs-lookup"><span data-stu-id="534a2-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="534a2-107">Datu bāzes reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="534a2-107">Database logging</span></span>

<span data-ttu-id="534a2-108">Datu bāzes reģistrācija ļauj noteikt, kuras tabulas un laukus ir pārraudzīt.</span><span class="sxs-lookup"><span data-stu-id="534a2-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="534a2-109">Tas arī ļauj noteikt notikumus, kam jāizraisa izmaiņu izsekošana.</span><span class="sxs-lookup"><span data-stu-id="534a2-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="534a2-110">Jūs izmantojat datu bāzes reģistrācijas iespējas, lai skatītu šīs izmaiņas laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="534a2-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="534a2-111">Papildinformāciju skatiet [Datu bāzes reģistrācijas konfigurēšana un pārvaldība](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="534a2-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="534a2-112">Konfigurēt Darbinieku patstāvīgi izmantojamais pakalpojums nosaukumu</span><span class="sxs-lookup"><span data-stu-id="534a2-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="534a2-113">Tagad **Personāla vadības parametri** var mainīt darbvietas nosaukumu **Darbinieku patstāvīgi izmantojamais pakalpojums** uz **Patstāvīgi izmantojamais pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="534a2-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="534a2-114">Papildinformāciju skatiet sadaļā [Darbinieku patstāvīgi izmantojamā pakalpojuma darbvietas nosaukuma maiņa](hr-employee-self-service-workspace-name.md).</span><span class="sxs-lookup"><span data-stu-id="534a2-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="534a2-115">Atvieglojumu pārvaldība atklātās reģistrācijas pieejai ārpus perioda</span><span class="sxs-lookup"><span data-stu-id="534a2-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="534a2-116">Šis laidiens izlabo kļūdu, kur darbinieki var piekļūt atklātās reģistrācijas atvieglojumiem ārpus reģistrācijas perioda vai bez dzīves notikuma.</span><span class="sxs-lookup"><span data-stu-id="534a2-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="534a2-117">Tā rezultātā, ja ir nepieciešama atklātās reģistrācijas demonstrācija Darbinieku patstāvīgi izmantojamajā pakalpojumā, jums ir jāpielāgo atklātās reģistrācijas datumi šodienai (vai agrāk), lai to padarītu pieejamu.</span><span class="sxs-lookup"><span data-stu-id="534a2-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="534a2-118">Varat mainīt šo iestatījumu, izmantojot **Atvieglojumu pārvaldība > Kārtulas un opciju periodi**.</span><span class="sxs-lookup"><span data-stu-id="534a2-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="534a2-119">Darbinieka e-pasta reģistrācijas apstiprinājums</span><span class="sxs-lookup"><span data-stu-id="534a2-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="534a2-120">Tagad varat nosūtīt e-pasta ziņojumus darbiniekiem pēc tam, kad tie pabeidz savu atvieglojumu atlasi.</span><span class="sxs-lookup"><span data-stu-id="534a2-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="534a2-121">Varat nosūtīt noklusējuma ziņojumu vai izmantot organizācija e-pasta veidni.</span><span class="sxs-lookup"><span data-stu-id="534a2-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="534a2-122">Šie iestatījumi atrodas **Personāla vadības parametri > Atvieglojumu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="534a2-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="534a2-123">Atceltais atvaļinājums joprojām tiek rādīts darbvietas Personas gaidāmajā brīvajā laika (441358)</span><span class="sxs-lookup"><span data-stu-id="534a2-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="534a2-124">Atceltais atvaļinājums vairs netiks rādīts kā gaidāmais brīvais laiks atvaļinājumu kartītēs darbvietā **Personas**.</span><span class="sxs-lookup"><span data-stu-id="534a2-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="534a2-125">Nevar izmantot nodaļas elementa rekvizītu elementā PositionV2 (456486)</span><span class="sxs-lookup"><span data-stu-id="534a2-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="534a2-126">Tagad varat pievienot nodaļu, neveidojot dublikāta relāciju.</span><span class="sxs-lookup"><span data-stu-id="534a2-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="534a2-127">PayrollWorkerEnrolledBenefitDetailEntity jāizmanto tikai aprēķinātā lauka pensiju plāniem (459779)</span><span class="sxs-lookup"><span data-stu-id="534a2-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="534a2-128">Eksportējot **PayrollWorkerEnrolledBenefitDetailEntity** elementu, eksportēšana nosaka, vai tam jāizmanto aprēķinātais lauks, pamatojoties uz likmes tabulu, vai jāizmanto lauks **ContributionAmountCur**, kas atrodas dublēšanas tabulā.</span><span class="sxs-lookup"><span data-stu-id="534a2-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="534a2-129">Datu elementa izmantotā loģika izmantos likmes tabulu situācijās, kurās parasti nav pieteikuma.</span><span class="sxs-lookup"><span data-stu-id="534a2-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="534a2-130">Šī loģika izraisa elementa eksportēšanu, lai atgrieztu nulles vērtību šai kolonnai, jo nav aprēķina likmes tabulas un prece neļauj klientam to norādīt.</span><span class="sxs-lookup"><span data-stu-id="534a2-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="534a2-131">Neskaidri tulkojumi čehu valodā Personāla pārvaldībā un Darbinieku patstāvīgi izmantojamajā pakalpojumā (400276)</span><span class="sxs-lookup"><span data-stu-id="534a2-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="534a2-132">Šajā laidienā ir izlaboti tulkojumi **Uzņēmuma direktorijs**, **Nākamais reģistrētais kurss**, **Darbs** un **Amats**.</span><span class="sxs-lookup"><span data-stu-id="534a2-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="534a2-133">Tabulā WorkCalendarEmployment nav iespējoti izveidotie un modificētie sistēmas lauki (460171)</span><span class="sxs-lookup"><span data-stu-id="534a2-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="534a2-134">Izveidotie un modificētie sistēmas lauki tagad ir iespējoti Human Resources tabulā **WorkCalendarEmployment**.</span><span class="sxs-lookup"><span data-stu-id="534a2-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="534a2-135">Nulles atsauces izņēmums Jauna darbinieka pieņemšanai darbā un informācijas pievienošanai (455475)</span><span class="sxs-lookup"><span data-stu-id="534a2-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="534a2-136">Šis laidiens izlabo kļūdu (nulles atsauce) racionalizētā darbinieka ierakstā, kad, pieņemot darbā darbinieku, izmantojat opciju **Pieņemt darbā un pievienot informāciju**.</span><span class="sxs-lookup"><span data-stu-id="534a2-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-common-data-service-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="534a2-137">Common Data Service darbinieka elementā veiktās izmaiņas netiek atspoguļotas Human Resources (455652)</span><span class="sxs-lookup"><span data-stu-id="534a2-137">Changes made in the Common Data Service Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="534a2-138">Izmaiņas, kas veiktas šādos laukos Common Data Service elementā **Darbinieks**, tagad tiks parādītas Human Resources:</span><span class="sxs-lookup"><span data-stu-id="534a2-138">Changes made to the following fields in the **Worker** entity in Common Data Service will now show up in Human Resources:</span></span>

- <span data-ttu-id="534a2-139">**Strādā no mājām**</span><span class="sxs-lookup"><span data-stu-id="534a2-139">**Works from home**</span></span>
- <span data-ttu-id="534a2-140">**Darba stāža datums**</span><span class="sxs-lookup"><span data-stu-id="534a2-140">**Seniority date**</span></span>
- <span data-ttu-id="534a2-141">**Gadadienas datums**</span><span class="sxs-lookup"><span data-stu-id="534a2-141">**Anniversary date**</span></span>
- <span data-ttu-id="534a2-142">**Sākotnējais darbā pieņemšanas datums**</span><span class="sxs-lookup"><span data-stu-id="534a2-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="534a2-143">Pamatojoties uz amatam piešķirto darbu, pareizais atlīdzības līmenis netiek noklusēts (394136)</span><span class="sxs-lookup"><span data-stu-id="534a2-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="534a2-144">Ar šīm izmaiņām pareizais atlīdzības līmenis tiek noklusēts pamatojoties uz **Spēkā stāšanās datuma** ierakstiem **Amata informācija** un **Sākuma datums**, **Atlīdzības plāna piešķirē**.</span><span class="sxs-lookup"><span data-stu-id="534a2-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="534a2-145">Priekšskatījumā</span><span class="sxs-lookup"><span data-stu-id="534a2-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="534a2-146">Obligātie lauki</span><span class="sxs-lookup"><span data-stu-id="534a2-146">Mandatory fields</span></span> 

<span data-ttu-id="534a2-147">Tagad ir iespējams padarīt laukus obligātus, izmantojot Personāla vadības personalizēšanas iespējas.</span><span class="sxs-lookup"><span data-stu-id="534a2-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="534a2-148">Šim līdzeklim nepieciešami **Saglabātie skati**.</span><span class="sxs-lookup"><span data-stu-id="534a2-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="534a2-149">Programma Human Resources programmā Teams</span><span class="sxs-lookup"><span data-stu-id="534a2-149">Human Resources application in Teams</span></span>

<span data-ttu-id="534a2-150">Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="534a2-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="534a2-151">Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="534a2-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="534a2-152">Papildinformāciju skatiet sadaļā [Personāla vadība programms sistēmā Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="534a2-152">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="534a2-153">Datu pārvaldības struktūras (DMF) elementi atvieglojumu pārvaldībai</span><span class="sxs-lookup"><span data-stu-id="534a2-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="534a2-154">Tiek izlaisti atvieglojumu pārvaldības elementi.</span><span class="sxs-lookup"><span data-stu-id="534a2-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="534a2-155">DMF elementi ļauj jums importēt un eksportēt datus, lai viegli konfigurētu atvieglojumu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="534a2-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="534a2-156">Lai pārvietotu datus, būs pieejama atvieglojumu pārvaldības veidne.</span><span class="sxs-lookup"><span data-stu-id="534a2-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="534a2-157">Veidne eksportē un importē datus secīgi, lai ievērotu datu atkarības.</span><span class="sxs-lookup"><span data-stu-id="534a2-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="534a2-158">Atvaļinājuma iegāde un pārdošana</span><span class="sxs-lookup"><span data-stu-id="534a2-158">Buy and sell leave</span></span> 

<span data-ttu-id="534a2-159">Dažas organizācijas sniedz atvieglojumus, kas ļauj darbiniekiem pirkt vai pārdot atvaļinājumu.</span><span class="sxs-lookup"><span data-stu-id="534a2-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="534a2-160">Šo procesu bieži pārvalda manuāli.</span><span class="sxs-lookup"><span data-stu-id="534a2-160">This process is often managed manually.</span></span> <span data-ttu-id="534a2-161">Šis līdzeklis automatizē personāla vadības departamenta politikas un pieprasījumu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="534a2-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="534a2-162">Tas vienkāršo atvaļinājumu pārvaldības procesu un palīdz likvidēt kļūdas.</span><span class="sxs-lookup"><span data-stu-id="534a2-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="534a2-163">Plašāku informāciju skatiet:</span><span class="sxs-lookup"><span data-stu-id="534a2-163">For more information, see:</span></span>

- [<span data-ttu-id="534a2-164">Atvaļinājuma iegādes un pārdošanas politiku pārvaldība</span><span class="sxs-lookup"><span data-stu-id="534a2-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="534a2-165">Atvaļinājuma iegāde un pārdošana</span><span class="sxs-lookup"><span data-stu-id="534a2-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="534a2-166">Atstāt uzkrājumu vienam uzņēmumam vai atsevišķam plānam</span><span class="sxs-lookup"><span data-stu-id="534a2-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="534a2-167">Debitori var apstrādāt uzkrājumus vienam uzņēmumam vai atsevišķam atvaļinājumu un prombūtnes plānam.</span><span class="sxs-lookup"><span data-stu-id="534a2-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="534a2-168">Šī iespēja nodrošina skaidrību uzkrāšanas procesā debitoriem ar dažādiem atvaļinājumu gadiem vai atvaļinājuma uzkrāšanas politikām.</span><span class="sxs-lookup"><span data-stu-id="534a2-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="534a2-169">Lai iegūtu papildu informāciju, skatiet [Uzkrāt atvaļinājumu pēc uzņēmuma vai atvaļinājuma plāna](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span><span class="sxs-lookup"><span data-stu-id="534a2-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="534a2-170">Pielikumu pievienošana brīvā laika pieprasījumiem</span><span class="sxs-lookup"><span data-stu-id="534a2-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="534a2-171">Iespēja pievienot pielikumus apstiprinātajiem atvaļinājumu pieprasījumiem ir kritiski nepieciešama pašreizējā COVID-19 vidē.</span><span class="sxs-lookup"><span data-stu-id="534a2-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="534a2-172">Tagad darbinieki var pievienot šos pielikumus.</span><span class="sxs-lookup"><span data-stu-id="534a2-172">Employees can now add these attachments.</span></span> <span data-ttu-id="534a2-173">Tām ir arī vairāk izpratnes par to, kā tiek atjaunināti atvaļinājumu pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="534a2-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="534a2-174">Lai iegūtu papildu informāciju, skatiet [Pielikumu pievienošana esošam pieprasījumam](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="534a2-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="534a2-175">Pievienot uzkrājumu atlikšanas iemesla kodu</span><span class="sxs-lookup"><span data-stu-id="534a2-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="534a2-176">Pamatojuma kodi ir pievienoti uzkrāšanas apturēšanai.</span><span class="sxs-lookup"><span data-stu-id="534a2-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="534a2-177">Pārnešanas kārtulas</span><span class="sxs-lookup"><span data-stu-id="534a2-177">Carry forward rules</span></span> 

<span data-ttu-id="534a2-178">Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas.</span><span class="sxs-lookup"><span data-stu-id="534a2-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="534a2-179">Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām.</span><span class="sxs-lookup"><span data-stu-id="534a2-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="534a2-180">Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="534a2-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="534a2-181">Aizturēt atvaļinājumu uzkrājumu norādīto atvaļinājumu veidiem</span><span class="sxs-lookup"><span data-stu-id="534a2-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="534a2-182">Jūs varat izveidot kārtulu, kas aptur atvaļinājumu uzkrājumus darbiniekiem ar atvaļinājumu pieprasījumiem, kas ievadīti neapmaksātam atvaļinājumam.</span><span class="sxs-lookup"><span data-stu-id="534a2-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="534a2-183">Neapmaksāts atvaļinājums var būt veids, bet tam nav obligāti jābūt.</span><span class="sxs-lookup"><span data-stu-id="534a2-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="534a2-184">Jūs varat aizturēt jebkuru atvaļinājumu, pamatojoties uz citu atvaļinājumu veidu.</span><span class="sxs-lookup"><span data-stu-id="534a2-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="534a2-185">DMF elements ir pieejams uzkrājumu atlikšanai</span><span class="sxs-lookup"><span data-stu-id="534a2-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="534a2-186">DMF elements tagad ir pieejams uzkrājumu atlikšanai.</span><span class="sxs-lookup"><span data-stu-id="534a2-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="534a2-187">Drīzumā</span><span class="sxs-lookup"><span data-stu-id="534a2-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="534a2-188">Kontrolsaraksta entītijas iekļautas Common Data Service</span><span class="sxs-lookup"><span data-stu-id="534a2-188">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="534a2-189">Kontrolsaraksta elementi Pievienošana, Noņemšana, Pārsūtīšana un Biznesa procesi drīz būs pieejami Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="534a2-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="534a2-190">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="534a2-190">See also</span></span>

[<span data-ttu-id="534a2-191">Jaunumi un izmaiņas programmā Human Resources</span><span class="sxs-lookup"><span data-stu-id="534a2-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="534a2-192">Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu</span><span class="sxs-lookup"><span data-stu-id="534a2-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="534a2-193">Procesa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="534a2-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="534a2-194">Līdzekļu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="534a2-194">Manage features</span></span>](hr-admin-manage-features.md)
