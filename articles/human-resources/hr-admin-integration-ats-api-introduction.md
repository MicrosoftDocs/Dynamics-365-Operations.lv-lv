---
title: Kandidāta izsekošanas sistēmas integrācijas API ievads
description: Šajā tēmā aprakstīts Dynamics 365 Human Resources kandidāta izsekošanas sistēmas (ATS) integrācijas API.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f70e377d6844b5c4f9201f0a561ad9cfcab2eda1
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890129"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="bcdcf-103">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="bcdcf-103">Applicant Tracking System integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bcdcf-104">Šajā tēmā aprakstīts Dynamics 365 Human Resources kandidāta izsekošanas sistēmas (ATS) integrācijas API.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="bcdcf-105">API nolūks ir nodrošināt racionalizētu integrāciju starp Dynamics 365 Human Resources un partnera ATS.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![AtS integrācijas plūsma](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="bcdcf-107">Integrētā pieredze Human Resources sākas, kad darbā pieņemšanas vadītājs izveido personāla atlases pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="bcdcf-108">Kad pieprasījums ir aktivizēts, ATS izvelk detalizētu informāciju pieprasījumam izveidot personāla atlases projektu.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="bcdcf-109">Pēc tam tas seko darbā pieņemšanas konveijeram, lai atlasītu un pieņemtu kandidātu šiem amatiem.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="bcdcf-110">Visbeidzot ATS pabeidz aprites integrāciju uz serveri, nosūtot atlasītā kandidāta ierakstu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="bcdcf-111">Pēc tam kandidāta ierakstam var veikt vairākas uzņēmuma apstiprināšanas un darbplūsmām, lai izveidotu darbinieka ierakstu.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="bcdcf-112">Lai iespējotu integrāciju, Human Resources ir pievienojusi šādus komponentus:</span><span class="sxs-lookup"><span data-stu-id="bcdcf-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="bcdcf-113">Personāla atlases pieprasījuma izveides funkcionalitāte.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="bcdcf-114">Izvērsts kandidāta profils un saistītās darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="bcdcf-115">Integrācijas API, kas atver jauno funkcionalitāti programmu integrēšanai.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="bcdcf-116">Papildinformāciju par personāla atlases pieprasījumu un kandidātu funkcionalitātes iestatīšanu un lietošanu skatiet sadaļā [Darba kandidātu pieņemšana darbā](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="bcdcf-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="bcdcf-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="bcdcf-117">Microsoft Dataverse</span></span>

<span data-ttu-id="bcdcf-118">Šis API ir veidots Microsoft Dataverse (iepriekš Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="bcdcf-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="bcdcf-119">Visa RESTful mijiedarbība ar šo API tiek veikta, izmantojot Microsoft Dataverse Web API, kas izmanto OData.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="bcdcf-120">Šis API ir Dataverse Web API apakškopa.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="bcdcf-121">Dataverse Web API nosaka tādus raksturlielumus kā autentifikācija, SLA, pakete, vienlaicīguma kontrole un kļūdu apstrāde.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="bcdcf-122">Vispārīgāku informāciju par Microsoft Dataverse Web API skatiet šeit:</span><span class="sxs-lookup"><span data-stu-id="bcdcf-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="bcdcf-123">Kas ir Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="bcdcf-123">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="bcdcf-124">Izmantot Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="bcdcf-124">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="bcdcf-125">Microsoft Dataverse izstrādātāja rokasgrāmata</span><span class="sxs-lookup"><span data-stu-id="bcdcf-125">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="bcdcf-126">Iepriekš minētajā dokumentācijā ir ietvertas detalizētas un izstrādātāja norādes par Dataverse Web API izmantošanu, piemēram, [autentifikācijas pārvaldību](/powerapps/developer/data-platform/webapi/authenticate-web-api), [darbību veikšanu](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [Postman izmantošanu ar API](/powerapps/developer/data-platform/webapi/use-postman-web-api) un [izmaiņu izsekošanas vai delta marķieru izmantošanu](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) ar API.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="bcdcf-127">Opciju kopas</span><span class="sxs-lookup"><span data-stu-id="bcdcf-127">Option sets</span></span>

<span data-ttu-id="bcdcf-128">Šajā dokumentā aprakstītais ATS integrācijas API datu modelis ietver opciju kopas, kas nodrošina ar elementa rekvizītiem saistītas uzskaitījuma vērtības.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="bcdcf-129">Papildinformāciju par darbu ar opciju kopām Dataverse Web API skatiet sadaļā [Opciju kopu izveide un atjaunināšana, izmantojot Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets).</span><span class="sxs-lookup"><span data-stu-id="bcdcf-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="bcdcf-130">Opciju kopas tiek definētas katrai Dataverse videi.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="bcdcf-131">Virtuālie tabulas Human Resources programmā Dataverse</span><span class="sxs-lookup"><span data-stu-id="bcdcf-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="bcdcf-132">Galapunkti ATS integrācijai API izmanto Microsoft Dataverse virtuālās tabulas platformas iespējas.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="bcdcf-133">Pēc noklusējuma virtuālās tabulas un to saistītie API galapunkti nav izvietoti Human Resources vidēs, iespējojot organizācijas, lai noteiktu, kuri OData galapunkti būs redzami vidē.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="bcdcf-134">Lai izmantotu API, videi ir jāizveido Human Resources elementu virtuālās tabulas.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="bcdcf-135">Informāciju par API virtuālo tabulu ģenerēšanu skatiet [Konfigurēt Dataverse virtuālās tabulas](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="bcdcf-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="bcdcf-136">Datu modelis</span><span class="sxs-lookup"><span data-stu-id="bcdcf-136">Data model</span></span>

<span data-ttu-id="bcdcf-137">Datu modelis ir centrēts ap diviem galvenajiem elementiem:</span><span class="sxs-lookup"><span data-stu-id="bcdcf-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="bcdcf-138">**RecruitingRequest** pārstāv pieprasījumu ATS pieņemt darbā vienu vai vairākus atvērtus amatus. Vaicājuma piemēru skatiet sadaļā [Vaicājuma piemērs personāla atlases pieprasījumam](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="bcdcf-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="bcdcf-139">**CandidateToHire** parāda informāciju par kandidātu, kurš pieņēmis amata piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="bcdcf-140">**Persona** parāda personu, kas ir kandidāts.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="bcdcf-141">Personai uzņēmumā var būt vairākas lomas, piemēram, kandidāts, darbinieks, nodarbinātais vai darbuzņēmējs.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="bcdcf-142">Vaicājuma piemēru skatiet sadaļā [Vaicājuma piemērs kandidāta pieņemšanai darbā](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="bcdcf-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="bcdcf-143">Sekojošā diagramma attēlo attiecības API.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="bcdcf-144">Vairākiem veidiem ir ārējās atslēgas citām, iepriekš esošām Human Resources entītijām, kas šeit nav attēlotas.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="bcdcf-145">Šajā dokumentā ir sniegta informācija par elementiem, kas ir specifiski darbā pieņemšanas integrācijas scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="bcdcf-146">Tomēr Web API ir daudzi citi elementi Dataverse Web API programmai Dynamics 365 Human Resources, kas var būt atbilstīgi jūsu integrācijai.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="bcdcf-147">Piemēram, jums var būt nepieciešama detalizēta informācija par darbiniekiem, darbiem, amatiem vai citiem šeit nedefinētiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="bcdcf-148">Daudziem no šiem elementiem ir atsauces ārējās atslēgas attiecībās vai navigācijas rekvizītos.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![ATS integrācijas API datu modelis](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="bcdcf-150">Darbā pieņemšanas pieprasījums un saistītie elementi un opciju kopas</span><span class="sxs-lookup"><span data-stu-id="bcdcf-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="bcdcf-151">Piemēra vaicājums:</span><span class="sxs-lookup"><span data-stu-id="bcdcf-151">Example query:</span></span> 

- [<span data-ttu-id="bcdcf-152">Piemērs personāla atlases pieprasījuma vaicājumam</span><span class="sxs-lookup"><span data-stu-id="bcdcf-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="bcdcf-153">Elementi:</span><span class="sxs-lookup"><span data-stu-id="bcdcf-153">Entities:</span></span>

- [<span data-ttu-id="bcdcf-154">Pieņemšanas darbā pieprasījums</span><span class="sxs-lookup"><span data-stu-id="bcdcf-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="bcdcf-155">Darbā pieņemšanas pieprasījuma amats</span><span class="sxs-lookup"><span data-stu-id="bcdcf-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="bcdcf-156">Personāla atlases pieprasījuma prasmes</span><span class="sxs-lookup"><span data-stu-id="bcdcf-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="bcdcf-157">Personāla atlases pieprasījuma izglītība</span><span class="sxs-lookup"><span data-stu-id="bcdcf-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="bcdcf-158">Darbā pieņemšanas pieprasījuma atrašanās vieta</span><span class="sxs-lookup"><span data-stu-id="bcdcf-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="bcdcf-159">Opciju kopas:</span><span class="sxs-lookup"><span data-stu-id="bcdcf-159">Option sets:</span></span>

- [<span data-ttu-id="bcdcf-160">Darba nodokļu atvieglojumu statuss</span><span class="sxs-lookup"><span data-stu-id="bcdcf-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="bcdcf-161">Personāla atlases pieprasījuma pozīcijas statuss</span><span class="sxs-lookup"><span data-stu-id="bcdcf-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="bcdcf-162">Personāla atlases pieprasījuma statuss</span><span class="sxs-lookup"><span data-stu-id="bcdcf-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="bcdcf-163">Normatīvā darba kategorija</span><span class="sxs-lookup"><span data-stu-id="bcdcf-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="bcdcf-164">Kandidāts, kuru pieņemt darbā un saistīties elementi un opciju kopas</span><span class="sxs-lookup"><span data-stu-id="bcdcf-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="bcdcf-165">Piemēra vaicājums:</span><span class="sxs-lookup"><span data-stu-id="bcdcf-165">Example query:</span></span>

- [<span data-ttu-id="bcdcf-166">Piemērs Kandidāta vaicājumam par nolīgšanu</span><span class="sxs-lookup"><span data-stu-id="bcdcf-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="bcdcf-167">Elementi:</span><span class="sxs-lookup"><span data-stu-id="bcdcf-167">Entities:</span></span>

- [<span data-ttu-id="bcdcf-168">Kandidāts pieņemšanai darbā</span><span class="sxs-lookup"><span data-stu-id="bcdcf-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="bcdcf-169">Persona</span><span class="sxs-lookup"><span data-stu-id="bcdcf-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="bcdcf-170">Personas izglītība</span><span class="sxs-lookup"><span data-stu-id="bcdcf-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="bcdcf-171">Personas profesionālā pieredze</span><span class="sxs-lookup"><span data-stu-id="bcdcf-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="bcdcf-172">Personas adrese</span><span class="sxs-lookup"><span data-stu-id="bcdcf-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="bcdcf-173">Puses kontaktpersona</span><span class="sxs-lookup"><span data-stu-id="bcdcf-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="bcdcf-174">Personas prasme</span><span class="sxs-lookup"><span data-stu-id="bcdcf-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="bcdcf-175">Novērtējuma līmenis</span><span class="sxs-lookup"><span data-stu-id="bcdcf-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="bcdcf-176">Personas sertifikāts</span><span class="sxs-lookup"><span data-stu-id="bcdcf-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="bcdcf-177">Sertifikāta veids</span><span class="sxs-lookup"><span data-stu-id="bcdcf-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="bcdcf-178">Personas izvērtēšana</span><span class="sxs-lookup"><span data-stu-id="bcdcf-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="bcdcf-179">Izvērtēšanas tipi</span><span class="sxs-lookup"><span data-stu-id="bcdcf-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="bcdcf-180">Personas identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="bcdcf-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="bcdcf-181">Opciju kopas:</span><span class="sxs-lookup"><span data-stu-id="bcdcf-181">Option sets:</span></span>

- [<span data-ttu-id="bcdcf-182">Kandidātu integrācijas rezultāts</span><span class="sxs-lookup"><span data-stu-id="bcdcf-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="bcdcf-183">Tukšs Jā Nē</span><span class="sxs-lookup"><span data-stu-id="bcdcf-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="bcdcf-184">Izpildes statuss</span><span class="sxs-lookup"><span data-stu-id="bcdcf-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="bcdcf-185">Kontaktpersonas tips</span><span class="sxs-lookup"><span data-stu-id="bcdcf-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="bcdcf-186">Izglītības kredīta bāze</span><span class="sxs-lookup"><span data-stu-id="bcdcf-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="bcdcf-187">Dzimums</span><span class="sxs-lookup"><span data-stu-id="bcdcf-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="bcdcf-188">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="bcdcf-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="bcdcf-189">Gada mēneši</span><span class="sxs-lookup"><span data-stu-id="bcdcf-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="bcdcf-190">Nē Jā</span><span class="sxs-lookup"><span data-stu-id="bcdcf-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="bcdcf-191">Perioda vienība</span><span class="sxs-lookup"><span data-stu-id="bcdcf-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="bcdcf-192">Izvērtēšanas biežums</span><span class="sxs-lookup"><span data-stu-id="bcdcf-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="bcdcf-193">Izvērtēšanas biežums ǵenerāts no</span><span class="sxs-lookup"><span data-stu-id="bcdcf-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="bcdcf-194">Prasmju līmeņa veids</span><span class="sxs-lookup"><span data-stu-id="bcdcf-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="bcdcf-195">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="bcdcf-195">See also</span></span>

[<span data-ttu-id="bcdcf-196">Kandidātu pieņemšana darbā</span><span class="sxs-lookup"><span data-stu-id="bcdcf-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="bcdcf-197">Kas ir Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="bcdcf-197">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="bcdcf-198">Izmantot Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="bcdcf-198">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="bcdcf-199">Opciju kopu izveide un atjaunināšana, izmantojot Web API</span><span class="sxs-lookup"><span data-stu-id="bcdcf-199">Create and update option sets using the Web API</span></span>](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]