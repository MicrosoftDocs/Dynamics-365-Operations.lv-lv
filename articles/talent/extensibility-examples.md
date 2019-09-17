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
ms.openlocfilehash: 0b455a8194f58b41a349f004ceda8183c7ee3f7c
ms.sourcegitcommit: 9f94eff93d29bc27352569824e00bbccc2f961b8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/22/2019
ms.locfileid: "1781446"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="ffd20-103">Talent paplašināšana, izmantojot PowerApps un Microsoft Flow — paraugsituācijas</span><span class="sxs-lookup"><span data-stu-id="ffd20-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="ffd20-104">Šajā tēmā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 for Talent, kuros tiek izmantota programmatūra Microsoft PowerApps un Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="ffd20-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="ffd20-105">Varat importēt ar katru piemēru saistīto risinājumu pakotni savā PowerApps vidē.</span><span class="sxs-lookup"><span data-stu-id="ffd20-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="ffd20-106">Pēc tam varat izmantot pakotnes kā vadlīnijas vai kā sākumpunktu, lai īstenotu scenārijus, kas attiecas uz jūsu organizāciju.</span><span class="sxs-lookup"><span data-stu-id="ffd20-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ffd20-107">Ja vēlaties izmantot šajā tēmā aprakstītās veidnes un programmu nemainītā veidā, pārbaudiet tās un pārliecinieties, ka tās aptver visus scenārijus, kas raksturīgi jūsu ieviešanai.</span><span class="sxs-lookup"><span data-stu-id="ffd20-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="ffd20-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="ffd20-108">Prerequisites</span></span>

- <span data-ttu-id="ffd20-109">Lai importētu pakotnes, lietotājiem ir jābūt atļaujai **Vides veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="ffd20-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="ffd20-110">Lai eksportētu vai importētu programmas, lietotājiem jābūt PowerApps 2. plāna licencei vai PowerApps 2. plāna izmēģinājuma licencei.</span><span class="sxs-lookup"><span data-stu-id="ffd20-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="ffd20-111">Flow — Forms savienojums</span><span class="sxs-lookup"><span data-stu-id="ffd20-111">Flow – Form Connect</span></span>

<span data-ttu-id="ffd20-112">Veidni **Flow — Forms savienojums** var izmantot, lai nolasītu datus no pakalpojuma Microsoft Forms un saglabātu tos Common Data Service elementā.</span><span class="sxs-lookup"><span data-stu-id="ffd20-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="ffd20-113">Šo veidni var paplašināt, lai to varētu izmantot citiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="ffd20-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="ffd20-114">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="ffd20-114">Here are some examples:</span></span>

- <span data-ttu-id="ffd20-115">Kandidātu novērtējumu tveršana.</span><span class="sxs-lookup"><span data-stu-id="ffd20-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="ffd20-116">Rezultātu tveršana no kursu anketām.</span><span class="sxs-lookup"><span data-stu-id="ffd20-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="ffd20-117">Intervijām paredzētu jautājumu bibliotēkas veidošana personāla vadības administratoriem.</span><span class="sxs-lookup"><span data-stu-id="ffd20-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="ffd20-118">Kandidāta intervijas procesa novērtējuma tveršana</span><span class="sxs-lookup"><span data-stu-id="ffd20-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="ffd20-119">Programmā Microsoft Dynamics 365: Attract formas var parādīt kandidātu portālā, un kandidāti var aizpildīt datus.</span><span class="sxs-lookup"><span data-stu-id="ffd20-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="ffd20-120">Formas var arī iegult kā aktivitātes darba veidnē.</span><span class="sxs-lookup"><span data-stu-id="ffd20-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="ffd20-121">Kad kandidāts iesniedz formu, Microsoft Flow tver formas iesniegšanu, nolasa datus un saglabā tos Common Data Service elementā.</span><span class="sxs-lookup"><span data-stu-id="ffd20-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="ffd20-122">Lai lejupielādētu veidni **Flow — Forms savienojums** un pielāgoto elementu struktūru, atveriet [Flow — Forms savienojums](https://go.microsoft.com/fwlink/?linkid=2081988) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="ffd20-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="ffd20-123">Uz PowerApps nodoto parametru iniciēšana un izvilkšana</span><span class="sxs-lookup"><span data-stu-id="ffd20-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="ffd20-124">Veidni **Uz PowerApps nodoto parametru iniciēšana un izvilkšana** var izmantot kā sākumpunktu jebkuram PowerApps scenārijs, kas attiecas uz Attract.</span><span class="sxs-lookup"><span data-stu-id="ffd20-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="ffd20-125">Tajā ietilpst visi noklusējuma parametri, kurus nodod Attract, piemēram, **Darba pieteikums**, **Kandidāta ID** un **Darba ID**.</span><span class="sxs-lookup"><span data-stu-id="ffd20-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="ffd20-126">Šo veidni var izmantot, lai izgūtu kandidātu novērtējuma veidlapu, lai par pieņemšanu darbā atbildīgais vadītājs varētu redzēt kandidāta aizpildīto novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="ffd20-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="ffd20-127">Programmas, kas tiek izveidotas, izmantojot PowerApps, var iegult darba veidnē programmā Attract.</span><span class="sxs-lookup"><span data-stu-id="ffd20-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="ffd20-128">Lai lejupielādētu veidni **Uz PowerApps nodoto parametru iniciēšana un izvilkšana** un pielāgoto elementu struktūru, atveriet [Uz PowerApps nodoto parametru iniciēšana un izvilkšana](https://go.microsoft.com/fwlink/?linkid=2081991) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="ffd20-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="ffd20-129">Integrācija ar Office 365</span><span class="sxs-lookup"><span data-stu-id="ffd20-129">Integration with Office 365</span></span>

<span data-ttu-id="ffd20-130">Programmu **Integrācija ar Office 365** var izmantot, lai iegūtu grupas informāciju lietotājiem, kuri ir pierakstījušies, no programmas Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="ffd20-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="ffd20-131">Tā izmanto atsauces uz nodarbinātajiem programmā Talent, lai iegūtu ierašanās un aiziešanas informāciju un ierakstus par izņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="ffd20-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="ffd20-132">Ierašanās un aiziešanas informācija tiek glabāta pielāgotos Common Data Service elementos.</span><span class="sxs-lookup"><span data-stu-id="ffd20-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="ffd20-133">Tiek pieņemts, ka šī informācija tiek aizpildīta no trešo pušu sistēmām, izmantojot integrāciju.</span><span class="sxs-lookup"><span data-stu-id="ffd20-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="ffd20-134">Šo programmu var paplašināt, lai to varētu izmantot citiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="ffd20-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="ffd20-135">Piemēram, to var izmantot, lai rādītu darba grupas atvaļinājumu informāciju, kalendāra notikumus un ar darba grupu saistītus notikumus.</span><span class="sxs-lookup"><span data-stu-id="ffd20-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="ffd20-136">Lai lejupielādētu programmu **Integrācija ar Office 365** un pielāgoto elementu struktūru, atveriet [Integrācija ar Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="ffd20-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="ffd20-137">Sūtīt — e-pasta paziņojums</span><span class="sxs-lookup"><span data-stu-id="ffd20-137">Flow – Email Notification</span></span>

<span data-ttu-id="ffd20-138">Veidni **Flow — e-pasta paziņojums** var izmantot e-pasta paziņojumu scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="ffd20-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="ffd20-139">To var izmantot, lai aktivizētu paziņojuma e-pastus kandidātiem, kurus darbā pieņemšanas grupa noraida jebkurā personāla atlases procesa posmā.</span><span class="sxs-lookup"><span data-stu-id="ffd20-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="ffd20-140">Šo veidni var paplašināt, lai izsekotu kandidāta posma izmaiņām visā personāla atlases procesā un nosūtītu paziņojumus darbā pieņemšanas grupai un kandidātam.</span><span class="sxs-lookup"><span data-stu-id="ffd20-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="ffd20-141">Parasti elementiem, kas tiek glabāti Common Data Service, var iestatīt plūsmas, lai nosūtītu paziņojumus par notikumiem, kas notiek programmās Core HR, Attract vai Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="ffd20-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="ffd20-142">Lai lejupielādētu veidni **Flow — e-pasta paziņojums**, atveriet [Plūsma — e-pasta paziņojums](https://go.microsoft.com/fwlink/?linkid=2082103) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="ffd20-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="ffd20-143">Plūsmas — SQL savienojums un izpilde</span><span class="sxs-lookup"><span data-stu-id="ffd20-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="ffd20-144">Veidne **Flow — SQL savienojums un izpilde** izveido savienojumu ar Microsoft SQL Server un nodrošina SQL vaicājumu izpildi.</span><span class="sxs-lookup"><span data-stu-id="ffd20-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="ffd20-145">Lai gan šī veidne ir izveidota, lai lasītu un atjauninātu SQL tabulas, to var paplašināt, lai to varētu izmantot citiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="ffd20-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="ffd20-146">Piemēram, to var izmantot, lai aizpildītu sagatavošanas tabulu pakalpojumā Common Data Service ar ierakstiem no SQL Server un periodiski sinhronizētu sagatavošanas tabulu, izmantojot inkrementālu sadali no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ffd20-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="ffd20-147">Lai lejupielādētu veidni **Flow — SQL savienojums un izpilde**, atveriet [Flow — SQL savienojums un izpilde](https://go.microsoft.com/fwlink/?linkid=2081789) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="ffd20-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="ffd20-148">Flow — SharePoint integrācija</span><span class="sxs-lookup"><span data-stu-id="ffd20-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="ffd20-149">Veidni **Flow — SharePoint integrācija** var izmantot, lai nolasītu datus no Microsoft SharePoint saraksta, salīdzinātu sarakstu ar lauka vērtībām jebkuram Common Data Service elementam un nosūtītu salīdzinājuma rezultātus kā paziņojuma e-pastu.</span><span class="sxs-lookup"><span data-stu-id="ffd20-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="ffd20-150">Organizācijai var būt steidzami nepieciešams noteikts prasmju kopums.</span><span class="sxs-lookup"><span data-stu-id="ffd20-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="ffd20-151">Šīs prasmes var saglabāt SharePoint kā SharePoint sarakstu.</span><span class="sxs-lookup"><span data-stu-id="ffd20-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="ffd20-152">Kandidātam piesakoties tādam darbam, kuram ir izveidots saraksts ar nepieciešamo prasmju kopumu, ja pastāv būtiska atbilstība starp kandidāta prasmēm un SharePoint saglabātajām prasmēm, tiek nosūtīts paziņojuma e-pasts.</span><span class="sxs-lookup"><span data-stu-id="ffd20-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="ffd20-153">Šādā veidā amati, kas ir nepieciešami steidzami, tiek aizpildīti ātrāk, jo paziņojumi palīdz atlases darbiniekiem paplašināt kandidātu meklējumus un sadarboties darbā pieņemšanas jomā visā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="ffd20-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="ffd20-154">Šo veidni var paplašināt, lai to varētu izmantot jebkurā scenārijā, kas ietver SharePoint integrāciju.</span><span class="sxs-lookup"><span data-stu-id="ffd20-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="ffd20-155">Lai lejupielādētu veidni **Flow — SharePoint integrācija**, atveriet [Plūsma — SharePoint integrācija](https://go.microsoft.com/fwlink/?linkid=2082109) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="ffd20-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="ffd20-156">Atsauces programma</span><span class="sxs-lookup"><span data-stu-id="ffd20-156">Referral App</span></span>
<span data-ttu-id="ffd20-157">Varat izmantot atsauces programmu, lai pievienotu kandidātus kopīgai darbinieku kopai.</span><span class="sxs-lookup"><span data-stu-id="ffd20-157">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="ffd20-158">Iesniedzot kandidātu, ieteicējs var ievadīt **Vārdu**, **Uzvārdu**, **E-pastu** un **Linkedln vietrādi URL**.</span><span class="sxs-lookup"><span data-stu-id="ffd20-158">The referrer can enter **Firstname**, **Lastname**, **Email**, and **Linkedln URL** when submitting a candidate.</span></span> <span data-ttu-id="ffd20-159">Pēc tam kandidāts avota metadati tiek aizpildīti ar ieteicēja informāciju.</span><span class="sxs-lookup"><span data-stu-id="ffd20-159">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="ffd20-160">Šo programmu var iegult Darbinieku pašapkalpošanās (ESS) portālā atsauču iesniegšanai, vai arī to var izmantot kā hipersaiti uzņēmuma portālā un palaist kā savrupu programmu.</span><span class="sxs-lookup"><span data-stu-id="ffd20-160">You can embed this app in Employee self-service (ESS) for submitting referrals, or you can be use it as a hyperlink in the Corporate Portal and run as a stand-alone app.</span></span>

<span data-ttu-id="ffd20-161">Lai lejupielādētu **Atsauces programmu**, dodieties uz [Dynamics 365 for Talent paplašināmības risinājumu: Atsauces programma](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) Microsoft lejupielāžu centrā.</span><span class="sxs-lookup"><span data-stu-id="ffd20-161">To download **Referral App**, go to [Dynamics 365 for Talent extensibility solution: Referral App](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) on the Microsoft Download Center.</span></span> <span data-ttu-id="ffd20-162">Varat importēt šo programmu un pielāgot to, lai pievienotu papildu funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="ffd20-162">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ffd20-163">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ffd20-163">Additional resources</span></span>

[<span data-ttu-id="ffd20-164">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="ffd20-164">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="ffd20-165">Programmu migrēšana starp nomniekiem un vidēm</span><span class="sxs-lookup"><span data-stu-id="ffd20-165">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
