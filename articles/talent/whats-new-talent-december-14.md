---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2018. gada 14. decembris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c2d209cac52665053b664a93bfb6c35e171b0948
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518535"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a><span data-ttu-id="33849-103">Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2018. gada 14. decembris)</span><span class="sxs-lookup"><span data-stu-id="33849-103">What's new or changed in Dynamics 365 for Talent Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33849-104">**8.1.2085 būvējums**</span><span class="sxs-lookup"><span data-stu-id="33849-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="33849-105">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.</span><span class="sxs-lookup"><span data-stu-id="33849-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="33849-106">Izmaiņas</span><span class="sxs-lookup"><span data-stu-id="33849-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="33849-107">ASV — ACA (Pieejamās aprūpes akts) atbalsts 2018. taksācijas gada formām 1095-B un 1095-C</span><span class="sxs-lookup"><span data-stu-id="33849-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="33849-108">Katru gadu attiecīgajiem lielajiem darba devējiem (ALE) jāsniedz katram pilnas slodzes darbiniekam forma 1095-C.</span><span class="sxs-lookup"><span data-stu-id="33849-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="33849-109">Turklāt, ja darba devējs nodrošina paša apdrošinātu segumu, tam ir jāsniedz forma 1095-C (ja tas ir ALE) un 1095-B (ja tas ir mazais darba devējs) visiem pilna laika vai nepilna laika darbiniekiem, uz kuriem attiecas kāds no tā piedāvātajiem veselības aizsardzības plāniem.</span><span class="sxs-lookup"><span data-stu-id="33849-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="33849-110">Šis līdzeklis nodrošina drukājamas formas 1095-C un 1095-B.</span><span class="sxs-lookup"><span data-stu-id="33849-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="33849-111">Importēšanas laikā tiek ignorēts lauks SubmittedByPersonId sadaļā HcmPerfJournalEntity</span><span class="sxs-lookup"><span data-stu-id="33849-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="33849-112">Importējot/eksportējot veiktspējas žurnāla ierakstus, lauks **Iesniedza** tiek ignorēts.</span><span class="sxs-lookup"><span data-stu-id="33849-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="33849-113">Ar šīm izmaiņām vērtība **importēts/eksportēts** atspoguļos tabulas vērtību eksportēšanas laikā; importējot sistēma tiks atjaunināta ar vērtību, kas norādīta importa failā.</span><span class="sxs-lookup"><span data-stu-id="33849-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="33849-114">Darbvietas "Atvaļinājumi un kavējumi" cilnē Analīze tiek parādīta kļūda "OpenConnectionError" ar sistēmu nesaistītām administratora lomām</span><span class="sxs-lookup"><span data-stu-id="33849-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="33849-115">Ar šo atjauninājumu netiks rādītas kļūdas, atverot cilni **Analīze** darbvietā **Atvaļinājumi un kavējumi**.</span><span class="sxs-lookup"><span data-stu-id="33849-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="33849-116">Darbinieku pašapkalpošanās, amatu hierarhijas detalizētas rādīšanas rezultātā no elementa neizdodas iegūt pamatzaru</span><span class="sxs-lookup"><span data-stu-id="33849-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="33849-117">Ir veiktas izmaiņas, lai labotu kļūdu "Pamatzara iegūšana neizdevās", kad amatu hierarhija ir personalizēta, lai parādītos esošā darbvietā, un hierarhijā tiek atlasīts amats.</span><span class="sxs-lookup"><span data-stu-id="33849-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="33849-118">Lai skatītu cilni Alga lapā Amats, ir jābūt sistēmas administratoram.</span><span class="sxs-lookup"><span data-stu-id="33849-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="33849-119">Ir veiktas izmaiņas, lai ietvertu pareizos drošības elementus esošajā privilēģijā: "Uzturēt algas nodarbinātā un amata informāciju".</span><span class="sxs-lookup"><span data-stu-id="33849-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="33849-120">Ar šīm izmaiņām pēc noklusējuma algu administratoram būs piekļuve lapas Amats laukiem Alga.</span><span class="sxs-lookup"><span data-stu-id="33849-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="33849-121">Kļūda, iesniedzot veiktspējas pārskatu vadītājam un ja sadaļā Iesniegšanas instrukcijas ir izmantots vietturis %Reviews.PerfPeriod%</span><span class="sxs-lookup"><span data-stu-id="33849-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="33849-122">Ir veiktas izmaiņas, kas izlabo kļūdu "Nulles atsauces" kļūdu, izmantojot vietturi %Reviews.PerfPeriod% sadaļā Iesniegšanas instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="33849-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="33849-123">Darbaspēka Power BI pārskats rāda kļūdu, ja nodarbinātā darba stāža datums ir liekā diena garajā gadā</span><span class="sxs-lookup"><span data-stu-id="33849-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="33849-124">Ar šīm izmaiņām pakalpojumā Power BI tagad tiek atbalstītas liekās dienas.</span><span class="sxs-lookup"><span data-stu-id="33849-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="33849-125">Integrācija starp Core HR un Attract</span><span class="sxs-lookup"><span data-stu-id="33849-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="33849-126">Ir veiktas izmaiņas, lai atjauninātu integrāciju starp Core HR un Attract saistībā darbā pieņemamajiem kandidātiem.</span><span class="sxs-lookup"><span data-stu-id="33849-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="33849-127">Lai darbā pieņemamie kandidāti būtu redzami darbvietā **Personāla vadība**, tiek izmantotas tālāk aprakstītās Common Data Service entītijas.</span><span class="sxs-lookup"><span data-stu-id="33849-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following Common Data Service entities are used:</span></span>

<span data-ttu-id="33849-128">Darba pieteikums</span><span class="sxs-lookup"><span data-stu-id="33849-128">Job Application</span></span>
- <span data-ttu-id="33849-129">Statusa iemeslam jābūt iestatītam kā Piedāvājums pieņemts</span><span class="sxs-lookup"><span data-stu-id="33849-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="33849-130">Nodrošina vienumus Kandidāts un Darba piedāvājums</span><span class="sxs-lookup"><span data-stu-id="33849-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="33849-131">Kandidāts</span><span class="sxs-lookup"><span data-stu-id="33849-131">Candidate</span></span>
-   <span data-ttu-id="33849-132">Nodrošina vienumu Informācija par kandidātu</span><span class="sxs-lookup"><span data-stu-id="33849-132">Provides Candidate information</span></span>

<span data-ttu-id="33849-133">Darba piedāvājums</span><span class="sxs-lookup"><span data-stu-id="33849-133">Job Opening</span></span>
-   <span data-ttu-id="33849-134">Nodrošina vienumus Darba piedāvājuma ID un Darba piedāvājuma dalībnieki</span><span class="sxs-lookup"><span data-stu-id="33849-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="33849-135">Darba piedāvājuma dalībnieki</span><span class="sxs-lookup"><span data-stu-id="33849-135">Job Opening Participants</span></span>
-   <span data-ttu-id="33849-136">Nodrošina vienumu Par pieņemšanu darbā atbildīgais vadītājs</span><span class="sxs-lookup"><span data-stu-id="33849-136">Provides Hiring Manager</span></span>

<span data-ttu-id="33849-137">Kad kandidāts ir pievienots personāla vadībai, to tagad var arī noraidīt, izmantojot jaunu opciju, kas pieejama kandidāta kartītē.</span><span class="sxs-lookup"><span data-stu-id="33849-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="33849-138">Drīzumā</span><span class="sxs-lookup"><span data-stu-id="33849-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="33849-139">Atvaļinājumi un kavējumi: turpmāko atvaļinājumu un prognozēto atvaļinājumu atlikumi</span><span class="sxs-lookup"><span data-stu-id="33849-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="33849-140">Līdz ar izmaiņām, kas veiktas, lai ļautu darbiniekiem prognozēt prombūtni un iesniegt turpmākās prombūtnes pieprasījumus, neietekmējot pašreizējos prombūtnes atlikumus, ir mainīts arī prombūtnes atlikumu attēlošanas veids.</span><span class="sxs-lookup"><span data-stu-id="33849-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="33849-141">Pašlaik parādītais pieejamais atlikums ir pieprasījumiem pieejamais atvaļinājuma laika daudzums, ieskaitot uzkrāto atvaļinājumu līdz attiecīgajai dienai un visus apstiprinātos atvaļinājuma pieprasījumus līdz laika beigām.</span><span class="sxs-lookup"><span data-stu-id="33849-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="33849-142">Izlaižot prognozēšanas iespēju, parādītais atlikums mainās uz pašreizējo prombūtnes laika atlikumu, ieskaitot uzkrāto atvaļinājumu līdz attiecīgajai dienai un pieprasījumiem līdz attiecīgajai dienai.</span><span class="sxs-lookup"><span data-stu-id="33849-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="33849-143">Darbinieki un vadītāji redzēs šos atjauninātos atlikumus darbinieku un vadītāju pašapkalpošanās sadaļā kartītē **Prombūtne** un logā **Prombūtnes atlikumi**.</span><span class="sxs-lookup"><span data-stu-id="33849-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="33849-144">Personāldaļas vadītāji redzēs šos atjauninātos atlikumus darbvietā **Cilvēki** un logā **Piešķirtie atvaļinājumu plāni**, kas attiecas uz darbinieku.</span><span class="sxs-lookup"><span data-stu-id="33849-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="33849-145">Zināma problēma</span><span class="sxs-lookup"><span data-stu-id="33849-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a><span data-ttu-id="33849-146">Kartēšanas kļūdas integrēšanā ar programmu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="33849-146">Mapping errors in the integration with Finance and Operations</span></span>

<span data-ttu-id="33849-147">Pašreizējā veidnē Talent integrēšanai ar Dynamics 365 for Finance and Operations ir identificētas šādas problēmas.</span><span class="sxs-lookup"><span data-stu-id="33849-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="33849-148">Drīzumā tiks publicēta jauna veidne, un tā tiks lietota visiem jaunajiem izveidotajiem integrācijas projektiem.</span><span class="sxs-lookup"><span data-stu-id="33849-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="33849-149">Esošajiem integrācijas projektiem var atjaunināt uzdevuma kartējumus.</span><span class="sxs-lookup"><span data-stu-id="33849-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="33849-150">Informāciju par atjauninātajiem kartējumiem skatiet tālāk esošajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="33849-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="33849-151">Uzdevums No sadaļas Amati uz sadaļu Amatu pamatdarba piešķire neintegrē datus.</span><span class="sxs-lookup"><span data-stu-id="33849-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="33849-152">Šī problēma pašreiz tiek pētīta.</span><span class="sxs-lookup"><span data-stu-id="33849-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="33849-153">Pašreizējā kartējumā nav kļūdas apiešanas risinājuma.</span><span class="sxs-lookup"><span data-stu-id="33849-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="33849-154">Uzdevumam No sadaļas Nodaļas uz sadaļu Pārvaldības struktūrvienības ir jāatjaunina šādi kartējumi.</span><span class="sxs-lookup"><span data-stu-id="33849-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="33849-155">Esošais avota lauks</span><span class="sxs-lookup"><span data-stu-id="33849-155">Existing source field</span></span>          | <span data-ttu-id="33849-156">Jaunais avota lauks</span><span class="sxs-lookup"><span data-stu-id="33849-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="33849-157">cdm_description (Apraksts)</span><span class="sxs-lookup"><span data-stu-id="33849-157">cdm_description (Description)</span></span>  | <span data-ttu-id="33849-158">cdm_name (Nosaukums)</span><span class="sxs-lookup"><span data-stu-id="33849-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="33849-159">Ir jāpievieno arī papildu kartējums.</span><span class="sxs-lookup"><span data-stu-id="33849-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="33849-160">Atlasiet pēdējo lauku **Nav**, lai pievienotu šādu kartējumu.</span><span class="sxs-lookup"><span data-stu-id="33849-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="33849-161">Avota lauks</span><span class="sxs-lookup"><span data-stu-id="33849-161">Source field</span></span>                   | <span data-ttu-id="33849-162">Mērķa lauks</span><span class="sxs-lookup"><span data-stu-id="33849-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="33849-163">cdm_description (Apraksts)</span><span class="sxs-lookup"><span data-stu-id="33849-163">cdm_description (Description)</span></span>  | <span data-ttu-id="33849-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="33849-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="33849-165">Atjauninātajiem kartējumiem jāizskatās, kā norādīts tālāk redzamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="33849-165">The updated mappings should look like the following image.</span></span>

![Uzdevums No sadaļas Nodaļas uz sadaļu Pārvaldības struktūrvienības](./media/DepartmentMapping.png)


<span data-ttu-id="33849-167">Uzdevumam No sadaļas Darbi uz sadaļu Darba papildinformācija ir jāatjaunina šādi kartējumi.</span><span class="sxs-lookup"><span data-stu-id="33849-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="33849-168">Esošais avota lauks</span><span class="sxs-lookup"><span data-stu-id="33849-168">Existing source field</span></span>          | <span data-ttu-id="33849-169">Jaunais avota lauks</span><span class="sxs-lookup"><span data-stu-id="33849-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="33849-170">cdm_name (Nosaukums)</span><span class="sxs-lookup"><span data-stu-id="33849-170">cdm_name (Name)</span></span>                | <span data-ttu-id="33849-171">cdm_description (Apraksts)</span><span class="sxs-lookup"><span data-stu-id="33849-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="33849-172">cdm_name (Apraksts)</span><span class="sxs-lookup"><span data-stu-id="33849-172">cdm_name (Description)</span></span>         | <span data-ttu-id="33849-173">cdm_jobdescription (Pienākumu apraksts)</span><span class="sxs-lookup"><span data-stu-id="33849-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="33849-174">Atjauninātajiem kartējumiem jāizskatās, kā norādīts tālāk redzamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="33849-174">The updated mappings should look like the image below.</span></span>

![Uzdevums No sadaļas Darbi uz sadaļu Darba papildinformācija](./media/JobMapping.png)

<span data-ttu-id="33849-176">Uzdevumam No sadaļas Nodarbinātie uz sadaļu Darbs ir jāatjaunina šādi kartējumi.</span><span class="sxs-lookup"><span data-stu-id="33849-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="33849-177">Esošais avota lauks</span><span class="sxs-lookup"><span data-stu-id="33849-177">Existing source field</span></span>                 | <span data-ttu-id="33849-178">Jaunais avota lauks</span><span class="sxs-lookup"><span data-stu-id="33849-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="33849-179">cdm_emailaddress1 (1. e-pasta adrese)</span><span class="sxs-lookup"><span data-stu-id="33849-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="33849-180">cdm_primaryemailaddress (Primārā e-pasta adrese</span><span class="sxs-lookup"><span data-stu-id="33849-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="33849-181">cdm_telephone1 (1. tālrunis)</span><span class="sxs-lookup"><span data-stu-id="33849-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="33849-182">cdm_primarytelephone (Primārais tālrunis)</span><span class="sxs-lookup"><span data-stu-id="33849-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="33849-183">Ir jāatjaunina arī lauka Dzimums pārveidošana.</span><span class="sxs-lookup"><span data-stu-id="33849-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="33849-184">Atlasiet **fn** (funkcijas) kartes veidu vienumam Dzimums un atjauniniet šādus vērtību kartējumus.</span><span class="sxs-lookup"><span data-stu-id="33849-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="33849-185">Common Data Service vērtība</span><span class="sxs-lookup"><span data-stu-id="33849-185">Common Data Service value</span></span>                   | <span data-ttu-id="33849-186">Finance and Operations vērtība</span><span class="sxs-lookup"><span data-stu-id="33849-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="33849-187">75440000</span><span class="sxs-lookup"><span data-stu-id="33849-187">75440000</span></span>                    | <span data-ttu-id="33849-188">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="33849-188">Male</span></span>                                             |
| <span data-ttu-id="33849-189">75440001</span><span class="sxs-lookup"><span data-stu-id="33849-189">75440001</span></span>                    | <span data-ttu-id="33849-190">Sieviete</span><span class="sxs-lookup"><span data-stu-id="33849-190">Female</span></span>                                           |
| <span data-ttu-id="33849-191">75440002</span><span class="sxs-lookup"><span data-stu-id="33849-191">75440002</span></span>                    | <span data-ttu-id="33849-192">Nav</span><span class="sxs-lookup"><span data-stu-id="33849-192">None</span></span>                                             | 
| <span data-ttu-id="33849-193">75440003</span><span class="sxs-lookup"><span data-stu-id="33849-193">75440003</span></span>                    | <span data-ttu-id="33849-194">Nenoteikts</span><span class="sxs-lookup"><span data-stu-id="33849-194">NonSpecific</span></span>                                      |

<span data-ttu-id="33849-195">Atjauninātajiem kartējumiem jāizskatās, kā norādīts tālāk redzamajos attēlos.</span><span class="sxs-lookup"><span data-stu-id="33849-195">The updated mappings should look like the following images.</span></span>

![Uzdevums No sadaļas Nodarbinātie uz sadaļu Darbs](./media/WorkerMapping.png)

![Lauka Dzimums pārveidošana](./media/WorkerTransform.png)
