---
title: Paplašināt Talent ar Power Apps un Power Automate
description: Šajā tēmā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 Talent, kuros tiek izmantota programmatūra Microsoft Power Apps un Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
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
ms.openlocfilehash: 6c8a583a93c2ceb70d8c3b0e0047e2bf2047b56d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898321"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="4c908-103">Paplašināt Talent ar Power Apps un Power Automate</span><span class="sxs-lookup"><span data-stu-id="4c908-103">Extend Talent with Power Apps and Power Automate</span></span>

<span data-ttu-id="4c908-104">Šajā tēmā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 Talent, kuros tiek izmantota programmatūra Microsoft Power Apps un Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="4c908-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="4c908-105">Varat importēt ar katru piemēru saistīto risinājumu pakotni savā Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="4c908-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="4c908-106">Pēc tam varat izmantot pakotnes kā vadlīnijas vai kā sākumpunktu, lai īstenotu scenārijus, kas attiecas uz jūsu organizāciju.</span><span class="sxs-lookup"><span data-stu-id="4c908-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c908-107">Ja vēlaties izmantot šajā tēmā aprakstītās veidnes un programmu nemainītā veidā, pārbaudiet tās un pārliecinieties, ka tās aptver visus scenārijus, kas raksturīgi jūsu ieviešanai.</span><span class="sxs-lookup"><span data-stu-id="4c908-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="4c908-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="4c908-108">Prerequisites</span></span>

- <span data-ttu-id="4c908-109">Lai importētu pakotnes, lietotājiem ir jābūt atļaujai **Vides veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="4c908-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="4c908-110">Lai eksportētu vai importētu programmas, lietotājiem jābūt Power Apps 2. plāna licencei vai Power Apps 2. plāna izmēģinājuma licencei.</span><span class="sxs-lookup"><span data-stu-id="4c908-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="4c908-111">Power Automate — Formas savienojums</span><span class="sxs-lookup"><span data-stu-id="4c908-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="4c908-112">Veidni **Power Automate – Formas savienojums** var izmantot, lai nolasītu datus no pakalpojuma Microsoft Forms un saglabātu tos Common Data Service elementā.</span><span class="sxs-lookup"><span data-stu-id="4c908-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="4c908-113">Šo veidni var paplašināt, lai to varētu izmantot citiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="4c908-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="4c908-114">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="4c908-114">Here are some examples:</span></span>

- <span data-ttu-id="4c908-115">Kandidātu novērtējumu tveršana.</span><span class="sxs-lookup"><span data-stu-id="4c908-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="4c908-116">Rezultātu tveršana no kursu anketām.</span><span class="sxs-lookup"><span data-stu-id="4c908-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="4c908-117">Intervijām paredzētu jautājumu bibliotēkas veidošana personāla vadības administratoriem.</span><span class="sxs-lookup"><span data-stu-id="4c908-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="4c908-118">Kandidāta intervijas procesa novērtējuma tveršana</span><span class="sxs-lookup"><span data-stu-id="4c908-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="4c908-119">Programmā Microsoft Dynamics 365: Attract formas var parādīt kandidātu portālā, un kandidāti var aizpildīt datus.</span><span class="sxs-lookup"><span data-stu-id="4c908-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="4c908-120">Formas var arī iegult kā aktivitātes darba veidnē.</span><span class="sxs-lookup"><span data-stu-id="4c908-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="4c908-121">Kad kandidāts iesniedz formu, Microsoft Power Automate tver formas iesniegšanu, nolasa datus un saglabā tos Common Data Service elementā.</span><span class="sxs-lookup"><span data-stu-id="4c908-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="4c908-122">Lai lejupielādētu veidni  **Power Automate – formas savienojums** un pielāgoto elementu struktūru, ejiet uz  [Power Automate – Formas savienojums](https://go.microsoft.com/fwlink/?linkid=2081988) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="4c908-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a><span data-ttu-id="4c908-123">Uz PowerApps nodoto parametru iniciēšana un izvilkšana Power Apps</span><span class="sxs-lookup"><span data-stu-id="4c908-123">Initiate and Extract Parameters Passed to Power Apps</span></span>

<span data-ttu-id="4c908-124">Veidni **Uz Power Apps nodoto parametru iniciēšana un izvilkšana** var izmantot kā sākumpunktu jebkuram Power Apps scenārijam, kas attiecas uz Attract.</span><span class="sxs-lookup"><span data-stu-id="4c908-124">The **Initiate and Extract Parameters Passed to Power Apps** template can be used as a starting point for any Power Apps scenario that is specific to Attract.</span></span> <span data-ttu-id="4c908-125">Tajā ietilpst visi noklusējuma parametri, kurus nodod Attract, piemēram, **Darba pieteikums**, **Kandidāta ID** un **Darba ID**.</span><span class="sxs-lookup"><span data-stu-id="4c908-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="4c908-126">Šo veidni var izmantot, lai izgūtu kandidātu novērtējuma veidlapu, lai par pieņemšanu darbā atbildīgais vadītājs varētu redzēt kandidāta aizpildīto novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="4c908-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="4c908-127">Programmas, kas tiek izveidotas, izmantojot Power Apps, var iegult darba veidnē programmā Attract.</span><span class="sxs-lookup"><span data-stu-id="4c908-127">Apps that are created by using Power Apps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="4c908-128">Lai lejupielādētu veidni **Uz Power Apps nodoto parametru iniciēšana un izvilkšana** un pielāgoto elementu struktūru, ejiet uz [Uz Power Apps nodoto parametru iniciēšana un izvilkšana](https://go.microsoft.com/fwlink/?linkid=2081991) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="4c908-128">To download the **Initiate and Extract Parameters Passed to Power Apps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="4c908-129">Integrācija ar Office 365</span><span class="sxs-lookup"><span data-stu-id="4c908-129">Integration with Office 365</span></span>

<span data-ttu-id="4c908-130">Programmu **Integrācija ar Office 365** var izmantot, lai iegūtu grupas informāciju lietotājiem, kuri ir pierakstījušies, no programmas Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="4c908-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="4c908-131">Tā izmanto atsauces uz nodarbinātajiem programmā Talent, lai iegūtu ierašanās un aiziešanas informāciju un ierakstus par izņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="4c908-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="4c908-132">Ierašanās un aiziešanas informācija tiek glabāta pielāgotos Common Data Service elementos.</span><span class="sxs-lookup"><span data-stu-id="4c908-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="4c908-133">Tiek pieņemts, ka šī informācija tiek aizpildīta no trešo pušu sistēmām, izmantojot integrāciju.</span><span class="sxs-lookup"><span data-stu-id="4c908-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="4c908-134">Šo programmu var paplašināt, lai to varētu izmantot citiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="4c908-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="4c908-135">Piemēram, to var izmantot, lai rādītu darba grupas atvaļinājumu informāciju, kalendāra notikumus un ar darba grupu saistītus notikumus.</span><span class="sxs-lookup"><span data-stu-id="4c908-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="4c908-136">Lai lejupielādētu programmu **Integrācija ar Office 365** un pielāgoto elementu struktūru, atveriet [Integrācija ar Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="4c908-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--email-notification"></a><span data-ttu-id="4c908-137">Power Automate - e-pasta paziņojums</span><span class="sxs-lookup"><span data-stu-id="4c908-137">Power Automate – Email Notification</span></span>

<span data-ttu-id="4c908-138">Veidni **Power Automate – e-pasta paziņojums** var izmantot e-pasta paziņojumu scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="4c908-138">The **Power Automate – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="4c908-139">To var izmantot, lai aktivizētu paziņojuma e-pastus kandidātiem, kurus darbā pieņemšanas grupa noraida jebkurā personāla atlases procesa posmā.</span><span class="sxs-lookup"><span data-stu-id="4c908-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="4c908-140">Šo veidni var paplašināt, lai izsekotu kandidāta posma izmaiņām visā personāla atlases procesā un nosūtītu paziņojumus darbā pieņemšanas grupai un kandidātam.</span><span class="sxs-lookup"><span data-stu-id="4c908-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="4c908-141">Parasti elementiem, kas tiek glabāti Common Data Service, var iestatīt plūsmas, lai nosūtītu paziņojumus par notikumiem, kas notiek programmās Core HR, Attract vai Onboard.</span><span class="sxs-lookup"><span data-stu-id="4c908-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Onboard.</span></span>

<span data-ttu-id="4c908-142">Lai lejupielādētu veidni **Power Automate – e-pasta paziņojums**, ejiet uz [Power Automate – e-pasta paziņojums](https://go.microsoft.com/fwlink/?linkid=2082103) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="4c908-142">To download the **Power Automate – Email Notification** template, go to [Power Automate – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="4c908-143">Power Automate — SQL savienojums un izpilde</span><span class="sxs-lookup"><span data-stu-id="4c908-143">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="4c908-144">Veidne **Power Automate – SQL savienojums un izpilde** izveido savienojumu ar Microsoft SQL Server un nodrošina SQL vaicājumu izpildi.</span><span class="sxs-lookup"><span data-stu-id="4c908-144">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="4c908-145">Lai gan šī veidne ir izveidota, lai lasītu un atjauninātu SQL tabulas, to var paplašināt, lai to varētu izmantot citiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="4c908-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="4c908-146">Piemēram, to var izmantot, lai aizpildītu sagatavošanas tabulu pakalpojumā Common Data Service ar ierakstiem no SQL Server un periodiski sinhronizētu sagatavošanas tabulu, izmantojot inkrementālu sadali no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4c908-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="4c908-147">Lai lejupielādētu veidni **Power Automate – SQL savienojums un izpilde**, ejiet uz [Power Automate – SQL savienojums un izpilde](https://go.microsoft.com/fwlink/?linkid=2081789) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="4c908-147">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="4c908-148">Power Automate – SharePoint Integrācija</span><span class="sxs-lookup"><span data-stu-id="4c908-148">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="4c908-149">Veidni **Power Automate – SharePoint Integrācija** var izmantot, lai nolasītu datus no Microsoft SharePoint saraksta, salīdzinātu sarakstu ar lauka vērtībām jebkuram  Common Data Service elementam un nosūtītu salīdzinājuma rezultātus kā paziņojuma e-pastu.</span><span class="sxs-lookup"><span data-stu-id="4c908-149">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="4c908-150">Organizācijai var būt steidzami nepieciešams noteikts prasmju kopums.</span><span class="sxs-lookup"><span data-stu-id="4c908-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="4c908-151">Šīs prasmes var saglabāt SharePoint kā SharePoint sarakstu.</span><span class="sxs-lookup"><span data-stu-id="4c908-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="4c908-152">Kandidātam piesakoties tādam darbam, kuram ir izveidots saraksts ar nepieciešamo prasmju kopumu, ja pastāv būtiska atbilstība starp kandidāta prasmēm un SharePoint saglabātajām prasmēm, tiek nosūtīts paziņojuma e-pasts.</span><span class="sxs-lookup"><span data-stu-id="4c908-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="4c908-153">Šādā veidā amati, kas ir nepieciešami steidzami, tiek aizpildīti ātrāk, jo paziņojumi palīdz atlases darbiniekiem paplašināt kandidātu meklējumus un sadarboties darbā pieņemšanas jomā visā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="4c908-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="4c908-154">Šo veidni var paplašināt, lai to varētu izmantot jebkurā scenārijā, kas ietver SharePoint integrāciju.</span><span class="sxs-lookup"><span data-stu-id="4c908-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="4c908-155">Lai lejupielādētu veidni **Power Automate – SharePoint Integrācija**, ejiet uz  [Power Automate – SharePoint Integrācija](https://go.microsoft.com/fwlink/?linkid=2082109) Microsoft lejupielādes centrā.</span><span class="sxs-lookup"><span data-stu-id="4c908-155">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="4c908-156">Atsauces programma</span><span class="sxs-lookup"><span data-stu-id="4c908-156">Referral App</span></span>
<span data-ttu-id="4c908-157">Varat izmantot atsauces programmu, lai pievienotu kandidātus kopīgai darbinieku kopai.</span><span class="sxs-lookup"><span data-stu-id="4c908-157">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="4c908-158">Iesniedzot kandidātu, ieteicējs var ievadīt **Vārdu**, **Uzvārdu**, **E-pastu** un **Linkedln vietrādi URL**.</span><span class="sxs-lookup"><span data-stu-id="4c908-158">The referrer can enter **Firstname**, **Lastname**, **Email**, and **Linkedln URL** when submitting a candidate.</span></span> <span data-ttu-id="4c908-159">Pēc tam kandidāts avota metadati tiek aizpildīti ar ieteicēja informāciju.</span><span class="sxs-lookup"><span data-stu-id="4c908-159">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="4c908-160">Šo programmu var iegult Darbinieku pašapkalpošanās (ESS) portālā atsauču iesniegšanai, vai arī to var izmantot kā hipersaiti uzņēmuma portālā un palaist kā savrupu programmu.</span><span class="sxs-lookup"><span data-stu-id="4c908-160">You can embed this app in Employee self-service (ESS) for submitting referrals, or you can be use it as a hyperlink in the Corporate Portal and run as a stand-alone app.</span></span>

<span data-ttu-id="4c908-161">Lai lejupielādētu **Atsauces programmu**, dodieties uz [Dynamics 365 Talent paplašināmības risinājumu: Atsauces programma](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) Microsoft lejupielāžu centrā.</span><span class="sxs-lookup"><span data-stu-id="4c908-161">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) on the Microsoft Download Center.</span></span> <span data-ttu-id="4c908-162">Varat importēt šo programmu un pielāgot to, lai pievienotu papildu funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="4c908-162">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c908-163">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4c908-163">Additional resources</span></span>

[<span data-ttu-id="4c908-164">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="4c908-164">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="4c908-165">Programmu migrēšana starp nomniekiem un vidēm</span><span class="sxs-lookup"><span data-stu-id="4c908-165">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
