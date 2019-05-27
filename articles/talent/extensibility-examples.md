---
title: Talent paplašināšana, izmantojot PowerApps un Microsoft Flow — paraugsituācijas
description: Šajā tēmā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 for Talent, kuros tiek izmantota programmatūra Microsoft PowerApps un Microsoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c113b0f4ab2c8e44d00fcfca3f0a6ca828a854ae
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518536"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="5da48-103">Talent paplašināšana, izmantojot PowerApps un Microsoft Flow — paraugsituācijas</span><span class="sxs-lookup"><span data-stu-id="5da48-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="5da48-104">Šajā tēmā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 for Talent, kuros tiek izmantota programmatūra Microsoft PowerApps un Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="5da48-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="5da48-105">Varat importēt ar katru piemēru saistīto risinājumu pakotni savā PowerApps vidē.</span><span class="sxs-lookup"><span data-stu-id="5da48-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="5da48-106">Pēc tam varat izmantot pakotnes kā vadlīnijas vai kā sākumpunktu, lai īstenotu scenārijus, kas attiecas uz jūsu organizāciju.</span><span class="sxs-lookup"><span data-stu-id="5da48-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5da48-107">Ja vēlaties izmantot šajā tēmā aprakstītās veidnes un programmu nemainītā veidā, pārbaudiet tās un pārliecinieties, ka tās aptver visus scenārijus, kas raksturīgi jūsu ieviešanai.</span><span class="sxs-lookup"><span data-stu-id="5da48-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="5da48-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="5da48-108">Prerequisites</span></span>

- <span data-ttu-id="5da48-109">Lai importētu pakotnes, lietotājiem ir jābūt atļaujai **Vides veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="5da48-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="5da48-110">Lai eksportētu vai importētu programmas, lietotājiem jābūt PowerApps 2. plāna licencei vai PowerApps 2. plāna izmēģinājuma licencei.</span><span class="sxs-lookup"><span data-stu-id="5da48-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="5da48-111">Flow — Forms savienojums</span><span class="sxs-lookup"><span data-stu-id="5da48-111">Flow – Form Connect</span></span>

<span data-ttu-id="5da48-112">Veidni **Flow — Forms savienojums** var izmantot, lai nolasītu datus no pakalpojuma Microsoft Forms un saglabātu tos Common Data Service elementā.</span><span class="sxs-lookup"><span data-stu-id="5da48-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="5da48-113">Šo veidni var paplašināt, lai to varētu izmantot citiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="5da48-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="5da48-114">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="5da48-114">Here are some examples:</span></span>

- <span data-ttu-id="5da48-115">Kandidātu novērtējumu tveršana.</span><span class="sxs-lookup"><span data-stu-id="5da48-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="5da48-116">Rezultātu tveršana no kursu anketām.</span><span class="sxs-lookup"><span data-stu-id="5da48-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="5da48-117">Intervijām paredzētu jautājumu bibliotēkas veidošana personāla vadības administratoriem.</span><span class="sxs-lookup"><span data-stu-id="5da48-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="5da48-118">Kandidāta intervijas procesa novērtējuma tveršana</span><span class="sxs-lookup"><span data-stu-id="5da48-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="5da48-119">Programmā Microsoft Dynamics 365: Attract formas var parādīt kandidātu portālā, un kandidāti var aizpildīt datus.</span><span class="sxs-lookup"><span data-stu-id="5da48-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="5da48-120">Formas var arī iegult kā aktivitātes darba veidnē.</span><span class="sxs-lookup"><span data-stu-id="5da48-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="5da48-121">Kad kandidāts iesniedz formu, Microsoft Flow tver formas iesniegšanu, nolasa datus un saglabā tos Common Data Service elementā.</span><span class="sxs-lookup"><span data-stu-id="5da48-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="5da48-122">Lai lejupielādētu veidni **Flow — Forms savienojums** un pielāgoto elementu struktūru, atveriet [Flow — Forms savienojums](https://go.microsoft.com/fwlink/?linkid=2081988) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="5da48-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="5da48-123">Uz PowerApps nodoto parametru iniciēšana un izvilkšana</span><span class="sxs-lookup"><span data-stu-id="5da48-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="5da48-124">Veidni **Uz PowerApps nodoto parametru iniciēšana un izvilkšana** var izmantot kā sākumpunktu jebkuram PowerApps scenārijs, kas attiecas uz Attract.</span><span class="sxs-lookup"><span data-stu-id="5da48-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="5da48-125">Tajā ietilpst visi noklusējuma parametri, kurus nodod Attract, piemēram, **Darba pieteikums**, **Kandidāta ID** un **Darba ID**.</span><span class="sxs-lookup"><span data-stu-id="5da48-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="5da48-126">Šo veidni var izmantot, lai izgūtu kandidātu novērtējuma veidlapu, lai par pieņemšanu darbā atbildīgais vadītājs varētu redzēt kandidāta aizpildīto novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="5da48-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="5da48-127">Programmas, kas tiek izveidotas, izmantojot PowerApps, var iegult darba veidnē programmā Attract.</span><span class="sxs-lookup"><span data-stu-id="5da48-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="5da48-128">Lai lejupielādētu veidni **Uz PowerApps nodoto parametru iniciēšana un izvilkšana** un pielāgoto elementu struktūru, atveriet [Uz PowerApps nodoto parametru iniciēšana un izvilkšana](https://go.microsoft.com/fwlink/?linkid=2081991) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="5da48-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="5da48-129">Integrācija ar Office 365</span><span class="sxs-lookup"><span data-stu-id="5da48-129">Integration with Office 365</span></span>

<span data-ttu-id="5da48-130">Programmu **Integrācija ar Office 365** var izmantot, lai iegūtu grupas informāciju lietotājiem, kuri ir pierakstījušies, no programmas Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="5da48-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="5da48-131">Tā izmanto atsauces uz nodarbinātajiem programmā Talent, lai iegūtu ierašanās un aiziešanas informāciju un ierakstus par izņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="5da48-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="5da48-132">Ierašanās un aiziešanas informācija tiek glabāta pielāgotos Common Data Service elementos.</span><span class="sxs-lookup"><span data-stu-id="5da48-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="5da48-133">Tiek pieņemts, ka šī informācija tiek aizpildīta no trešo pušu sistēmām, izmantojot integrāciju.</span><span class="sxs-lookup"><span data-stu-id="5da48-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="5da48-134">Šo programmu var paplašināt, lai to varētu izmantot citiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="5da48-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="5da48-135">Piemēram, to var izmantot, lai rādītu darba grupas atvaļinājumu informāciju, kalendāra notikumus un ar darba grupu saistītus notikumus.</span><span class="sxs-lookup"><span data-stu-id="5da48-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="5da48-136">Lai lejupielādētu programmu **Integrācija ar Office 365** un pielāgoto elementu struktūru, atveriet [Integrācija ar Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="5da48-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="5da48-137">Sūtīt — e-pasta paziņojums</span><span class="sxs-lookup"><span data-stu-id="5da48-137">Flow – Email Notification</span></span>

<span data-ttu-id="5da48-138">Veidni **Flow — e-pasta paziņojums** var izmantot e-pasta paziņojumu scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="5da48-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="5da48-139">To var izmantot, lai aktivizētu paziņojuma e-pastus kandidātiem, kurus darbā pieņemšanas grupa noraida jebkurā personāla atlases procesa posmā.</span><span class="sxs-lookup"><span data-stu-id="5da48-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="5da48-140">Šo veidni var paplašināt, lai izsekotu kandidāta posma izmaiņām visā personāla atlases procesā un nosūtītu paziņojumus darbā pieņemšanas grupai un kandidātam.</span><span class="sxs-lookup"><span data-stu-id="5da48-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="5da48-141">Parasti elementiem, kas tiek glabāti Common Data Service, var iestatīt plūsmas, lai nosūtītu paziņojumus par notikumiem, kas notiek programmās Core HR, Attract vai Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="5da48-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="5da48-142">Lai lejupielādētu veidni **Flow — e-pasta paziņojums**, atveriet [Plūsma — e-pasta paziņojums](https://go.microsoft.com/fwlink/?linkid=2082103) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="5da48-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="5da48-143">Plūsmas — SQL savienojums un izpilde</span><span class="sxs-lookup"><span data-stu-id="5da48-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="5da48-144">Veidne **Flow — SQL savienojums un izpilde** izveido savienojumu ar Microsoft SQL Server un nodrošina SQL vaicājumu izpildi.</span><span class="sxs-lookup"><span data-stu-id="5da48-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="5da48-145">Lai gan šī veidne ir izveidota, lai lasītu un atjauninātu SQL tabulas, to var paplašināt, lai to varētu izmantot citiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="5da48-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="5da48-146">Piemēram, to var izmantot, lai aizpildītu sagatavošanas tabulu pakalpojumā Common Data Service ar ierakstiem no SQL Server un periodiski sinhronizētu sagatavošanas tabulu, izmantojot inkrementālu sadali no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5da48-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="5da48-147">Lai lejupielādētu veidni **Flow — SQL savienojums un izpilde**, atveriet [Flow — SQL savienojums un izpilde](https://go.microsoft.com/fwlink/?linkid=2081789) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="5da48-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="5da48-148">Flow — SharePoint integrācija</span><span class="sxs-lookup"><span data-stu-id="5da48-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="5da48-149">Veidni **Flow — SharePoint integrācija** var izmantot, lai nolasītu datus no Microsoft SharePoint saraksta, salīdzinātu sarakstu ar lauka vērtībām jebkuram Common Data Service elementam un nosūtītu salīdzinājuma rezultātus kā paziņojuma e-pastu.</span><span class="sxs-lookup"><span data-stu-id="5da48-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="5da48-150">Organizācijai var būt steidzami nepieciešams noteikts prasmju kopums.</span><span class="sxs-lookup"><span data-stu-id="5da48-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="5da48-151">Šīs prasmes var saglabāt SharePoint kā SharePoint sarakstu.</span><span class="sxs-lookup"><span data-stu-id="5da48-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="5da48-152">Kandidātam piesakoties tādam darbam, kuram ir izveidots saraksts ar nepieciešamo prasmju kopumu, ja pastāv būtiska atbilstība starp kandidāta prasmēm un SharePoint saglabātajām prasmēm, tiek nosūtīts paziņojuma e-pasts.</span><span class="sxs-lookup"><span data-stu-id="5da48-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="5da48-153">Šādā veidā amati, kas ir nepieciešami steidzami, tiek aizpildīti ātrāk, jo paziņojumi palīdz atlases darbiniekiem paplašināt kandidātu meklējumus un sadarboties darbā pieņemšanas jomā visā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="5da48-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="5da48-154">Šo veidni var paplašināt, lai to varētu izmantot jebkurā scenārijā, kas ietver SharePoint integrāciju.</span><span class="sxs-lookup"><span data-stu-id="5da48-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="5da48-155">Lai lejupielādētu veidni **Flow — SharePoint integrācija**, atveriet [Plūsma — SharePoint integrācija](https://go.microsoft.com/fwlink/?linkid=2082109) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="5da48-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="admin-console-to-manage-talent-pools"></a><span data-ttu-id="5da48-156">Administratora konsole kandidātu kopu pārvaldīšanai</span><span class="sxs-lookup"><span data-stu-id="5da48-156">Admin console to manage talent pools</span></span>

<span data-ttu-id="5da48-157">Iespējojot integrāciju ar LinkedIn, pakalpojums Attract automātiski izveido LinkedIn kandidātu kopu.</span><span class="sxs-lookup"><span data-stu-id="5da48-157">When you enable integration with LinkedIn, Attract automatically createas a LinkedIn talent pool.</span></span> <span data-ttu-id="5da48-158">Kad personāla atlases darbinieks veic saziņu InMail formātā ar kandidātu, izmantojot LinkedIn, pakalpojums Attract izveido kandidāta profilu un kandidāts kļūst par LinkedIn kandidātu kopas dalībnieku.</span><span class="sxs-lookup"><span data-stu-id="5da48-158">When a recruiter exchanges InMail with a recruit through LinkedIn, Attract creates a profile for the recruit, and the recruit becomes a member of the LinkedIn talent pool.</span></span> <span data-ttu-id="5da48-159">Šī PowerApps programma ir noderīga, lai reorganizētu kandidātus kandidātu kopās, pamatojoties uz prasmēm.</span><span class="sxs-lookup"><span data-stu-id="5da48-159">This PowerApps app is useful for reorganizing candidates in talent pools based on skill.</span></span>

<span data-ttu-id="5da48-160">Palaidiet šo PowerApps programmu kā administratora konsoli, lai izpildītu tālāk minētos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="5da48-160">Run this PowerApps app as an admin console to perform the following tasks:</span></span>

- <span data-ttu-id="5da48-161">Kandidātu iekļaušana kandidātu kopas sarakstā</span><span class="sxs-lookup"><span data-stu-id="5da48-161">List candidates in a talent pool</span></span>
- <span data-ttu-id="5da48-162">Kandidātu pievienošana un noņemšana no kandidātu kopas</span><span class="sxs-lookup"><span data-stu-id="5da48-162">Add and remove candidates from a talent pool</span></span>
- <span data-ttu-id="5da48-163">Kandidātu pārvietošana no vienas kandidātu kopas uz citu</span><span class="sxs-lookup"><span data-stu-id="5da48-163">Move candidates from one talent pool to another</span></span>
- <span data-ttu-id="5da48-164">Pirms pārvietošanas veikta noteikšana, kuri kandidāti jau ir iekļauti kandidātu kopā</span><span class="sxs-lookup"><span data-stu-id="5da48-164">Determine whether candidates are already part of a talent pool before moving them</span></span>
- <span data-ttu-id="5da48-165">Kandidātu prasmju pārbaude pirms to pārvietošanas uz citām kandidātu kopām</span><span class="sxs-lookup"><span data-stu-id="5da48-165">Check the skills of candidates before moving them to other talent pools</span></span>

<span data-ttu-id="5da48-166">Šajā PowerApps programmā tiek lietotas “daudzi pret daudziem” tipa attiecības, tāpēc to var izmantot kā veidni citiem scenārijiem, kur nepieciešams iegūt ierakstus ar “daudzi pret daudziem” tipa attiecībām.</span><span class="sxs-lookup"><span data-stu-id="5da48-166">This PowerApps app uses many-to-many relationships, so you can use it as a template for other scenarios where you need to extract records that have many-to-many relationships.</span></span>

<span data-ttu-id="5da48-167">Lai lejupielādētu veidni **Administratora konsole kandidātu kopu pārvaldīšanai**, dodieties uz sadaļu [Administratora konsole kandidātu kopu pārvaldīšanai](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="5da48-167">To download the **Admin console to manage talent pools** template,  go to [Admin console to manage talent pools](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5da48-168">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5da48-168">Additional resources</span></span>

[<span data-ttu-id="5da48-169">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="5da48-169">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="5da48-170">Programmu migrēšana starp nomniekiem un vidēm</span><span class="sxs-lookup"><span data-stu-id="5da48-170">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
