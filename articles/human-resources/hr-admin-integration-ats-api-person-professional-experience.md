---
title: Personas profesionālā pieredze
description: Šajā tēmā aprakstīts Personas profesionālās pieredzes elements programmai Dynamics 365 Human Resources .
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51dd993e2d43174e96c062e142021cc0f6e3a288
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125285"
---
# <a name="person-professional-experience"></a><span data-ttu-id="e5522-103">Personas profesionālā pieredze</span><span class="sxs-lookup"><span data-stu-id="e5522-103">Person professional experience</span></span>

<span data-ttu-id="e5522-104">Šajā tēmā aprakstīts Personas profesionālās pieredzes elements programmai Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="e5522-104">This topic describes the Person professional experience entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="e5522-105">Fiziskais nosaukums: mshr_hcmpersonprofessionalexperienceentity</span><span class="sxs-lookup"><span data-stu-id="e5522-105">Physical name: mshr_hcmpersonprofessionalexperienceentity</span></span>

## <a name="description"></a><span data-ttu-id="e5522-106">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e5522-106">Description</span></span>

<span data-ttu-id="e5522-107">Šis elements apraksta kandidāta profesionālo pieredzi vai darba vēsturi.</span><span class="sxs-lookup"><span data-stu-id="e5522-107">This entity describes professional experience or work history of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e5522-108">JSON pārstāvība</span><span class="sxs-lookup"><span data-stu-id="e5522-108">JSON representation</span></span>

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="e5522-109">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="e5522-109">Properties</span></span>

| <span data-ttu-id="e5522-110">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="e5522-110">Property</span></span><br><span data-ttu-id="e5522-111">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="e5522-111">**Physical name**</span></span><br><span data-ttu-id="e5522-112">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="e5522-112">**_Type_**</span></span> | <span data-ttu-id="e5522-113">Izmantot</span><span class="sxs-lookup"><span data-stu-id="e5522-113">Use</span></span> | <span data-ttu-id="e5522-114">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e5522-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e5522-115">**Personas profesionālās pieredzes elementa ID**</span><span class="sxs-lookup"><span data-stu-id="e5522-115">**Person Professional Experience Entity ID**</span></span><br><span data-ttu-id="e5522-116">mshr_hcmpersonprofessionalexperienceentityid</span><span class="sxs-lookup"><span data-stu-id="e5522-116">mshr_hcmpersonprofessionalexperienceentityid</span></span><br><span data-ttu-id="e5522-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e5522-117">*GUID*</span></span> | <span data-ttu-id="e5522-118">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="e5522-118">Read-only</span></span><br><span data-ttu-id="e5522-119">Obligāts</span><span class="sxs-lookup"><span data-stu-id="e5522-119">Required</span></span> | <span data-ttu-id="e5522-120">Sistēmas ģenerēts unikāls identifikators elementa ierakstam.</span><span class="sxs-lookup"><span data-stu-id="e5522-120">System-generated unique identifier for the entity record.</span></span> |
| <span data-ttu-id="e5522-121">**Puses numurs**</span><span class="sxs-lookup"><span data-stu-id="e5522-121">**Party Number**</span></span><br><span data-ttu-id="e5522-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="e5522-122">mshr_partynumber</span></span><br><span data-ttu-id="e5522-123">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="e5522-123">*String*</span></span> | <span data-ttu-id="e5522-124">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="e5522-124">Read/write</span></span><br><span data-ttu-id="e5522-125">Obligāts</span><span class="sxs-lookup"><span data-stu-id="e5522-125">Required</span></span> | <span data-ttu-id="e5522-126">Unikāls kandidāta personas ieraksta identifikators.</span><span class="sxs-lookup"><span data-stu-id="e5522-126">Unique identifier of the person record for the candidate.</span></span> |
| <span data-ttu-id="e5522-127">**Personas ID vērtība**</span><span class="sxs-lookup"><span data-stu-id="e5522-127">**Person ID Value**</span></span><br><span data-ttu-id="e5522-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="e5522-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="e5522-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e5522-129">*GUID*</span></span> | <span data-ttu-id="e5522-130">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="e5522-130">Read-only</span></span><br><span data-ttu-id="e5522-131">Obligāts</span><span class="sxs-lookup"><span data-stu-id="e5522-131">Required</span></span><br><span data-ttu-id="e5522-132">Ārējā atslēga: mshr_dirpersonentity mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="e5522-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="e5522-133">Sistēmas ģenerēts unikāls personas elementa ieraksta identifikators.</span><span class="sxs-lookup"><span data-stu-id="e5522-133">System-generated unique identifier of the person entity record.</span></span> |
| <span data-ttu-id="e5522-134">**Darba devēja amats**</span><span class="sxs-lookup"><span data-stu-id="e5522-134">**Employer Position**</span></span><br><span data-ttu-id="e5522-135">mshr_employerposition</span><span class="sxs-lookup"><span data-stu-id="e5522-135">mshr_employerposition</span></span><br><span data-ttu-id="e5522-136">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="e5522-136">*String*</span></span> | <span data-ttu-id="e5522-137">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="e5522-137">Read/write</span></span><br><span data-ttu-id="e5522-138">Obligāts</span><span class="sxs-lookup"><span data-stu-id="e5522-138">Required</span></span> | <span data-ttu-id="e5522-139">Amata nosaukums, ko kandidāts ieņēma nodarbinātības laikā.</span><span class="sxs-lookup"><span data-stu-id="e5522-139">The position title held by the candidate while under employment.</span></span> |
| <span data-ttu-id="e5522-140">**Darbinieka vārds**</span><span class="sxs-lookup"><span data-stu-id="e5522-140">**Employer Name**</span></span><br><span data-ttu-id="e5522-141">mshr_employername</span><span class="sxs-lookup"><span data-stu-id="e5522-141">mshr_employername</span></span><br><span data-ttu-id="e5522-142">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="e5522-142">*String*</span></span> | <span data-ttu-id="e5522-143">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="e5522-143">Read/write</span></span><br><span data-ttu-id="e5522-144">Obligāts</span><span class="sxs-lookup"><span data-stu-id="e5522-144">Required</span></span> | <span data-ttu-id="e5522-145">Darba devēja vārds.</span><span class="sxs-lookup"><span data-stu-id="e5522-145">The name of the employer.</span></span> |
| <span data-ttu-id="e5522-146">**Darba devēja atrašanās vieta**</span><span class="sxs-lookup"><span data-stu-id="e5522-146">**Employer Location**</span></span><br><span data-ttu-id="e5522-147">mshr_employerlocation</span><span class="sxs-lookup"><span data-stu-id="e5522-147">mshr_employerlocation</span></span><br><span data-ttu-id="e5522-148">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="e5522-148">*String*</span></span> | <span data-ttu-id="e5522-149">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="e5522-149">Read/write</span></span><br><span data-ttu-id="e5522-150">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="e5522-150">Optional</span></span> | <span data-ttu-id="e5522-151">Darba devēja atrašanās vieta.</span><span class="sxs-lookup"><span data-stu-id="e5522-151">The employer’s location.</span></span> <span data-ttu-id="e5522-152">Maks. garums: 60.</span><span class="sxs-lookup"><span data-stu-id="e5522-152">Max length: 60.</span></span> <span data-ttu-id="e5522-153">Nav noteikts vai nepieciešams noteikts formāts.</span><span class="sxs-lookup"><span data-stu-id="e5522-153">No specific format defined or required.</span></span> |
| <span data-ttu-id="e5522-154">**Tālruņa numurs**</span><span class="sxs-lookup"><span data-stu-id="e5522-154">**Phone**</span></span><br><span data-ttu-id="e5522-155">mshr_phone</span><span class="sxs-lookup"><span data-stu-id="e5522-155">mshr_phone</span></span><br><span data-ttu-id="e5522-156">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="e5522-156">*String*</span></span> | <span data-ttu-id="e5522-157">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="e5522-157">Read/write</span></span><br><span data-ttu-id="e5522-158">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="e5522-158">Optional</span></span> | <span data-ttu-id="e5522-159">Darba devēja tālruņa numurs.</span><span class="sxs-lookup"><span data-stu-id="e5522-159">The employer’s phone number.</span></span> |
| <span data-ttu-id="e5522-160">**Vietrādis URL**</span><span class="sxs-lookup"><span data-stu-id="e5522-160">**URL**</span></span><br><span data-ttu-id="e5522-161">mshr_url</span><span class="sxs-lookup"><span data-stu-id="e5522-161">mshr_url</span></span><br><span data-ttu-id="e5522-162">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="e5522-162">*String*</span></span> | <span data-ttu-id="e5522-163">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="e5522-163">Read/write</span></span><br><span data-ttu-id="e5522-164">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="e5522-164">Optional</span></span> | <span data-ttu-id="e5522-165">Darba devēja tīmekļa vietnes vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="e5522-165">The URL of the employer’s website.</span></span> |
| <span data-ttu-id="e5522-166">**Sākuma datums**</span><span class="sxs-lookup"><span data-stu-id="e5522-166">**Start Date**</span></span><br><span data-ttu-id="e5522-167">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="e5522-167">mshr_startdate</span></span><br><span data-ttu-id="e5522-168">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="e5522-168">*Datetime*</span></span> | <span data-ttu-id="e5522-169">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="e5522-169">Read/write</span></span><br><span data-ttu-id="e5522-170">Obligāts</span><span class="sxs-lookup"><span data-stu-id="e5522-170">Required</span></span> | <span data-ttu-id="e5522-171">Kandidāta nodarbinātības sākuma datums.</span><span class="sxs-lookup"><span data-stu-id="e5522-171">The start date of the candidate’s employment.</span></span> |
| <span data-ttu-id="e5522-172">**Beigu datums**</span><span class="sxs-lookup"><span data-stu-id="e5522-172">**End Date**</span></span><br><span data-ttu-id="e5522-173">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="e5522-173">mshr_enddate</span></span><br><span data-ttu-id="e5522-174">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="e5522-174">*Datetime*</span></span> | <span data-ttu-id="e5522-175">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="e5522-175">Read/write</span></span><br><span data-ttu-id="e5522-176">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="e5522-176">Optional</span></span> | <span data-ttu-id="e5522-177">Kandidāta nodarbinātības beigu datums vai null, ja kandidāts joprojām šeit strādā.</span><span class="sxs-lookup"><span data-stu-id="e5522-177">The end date of the candidate’s employment, or null if the candidate is still employed here.</span></span> |
| <span data-ttu-id="e5522-178">**Atļaut sazināties ar darba devēju**</span><span class="sxs-lookup"><span data-stu-id="e5522-178">**Allow Contact Employer**</span></span><br><span data-ttu-id="e5522-179">mshr_allowcontactemployer</span><span class="sxs-lookup"><span data-stu-id="e5522-179">mshr_allowcontactemployer</span></span><br><span data-ttu-id="e5522-180">*mshr_hrmblankyesno opciju kopa*</span><span class="sxs-lookup"><span data-stu-id="e5522-180">*mshr_hrmblankyesno option set*</span></span> | <span data-ttu-id="e5522-181">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="e5522-181">Read/write</span></span><br><span data-ttu-id="e5522-182">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="e5522-182">Optional</span></span> | <span data-ttu-id="e5522-183">Norāda, vai kandidāts atļauj sazināties ar iepriekšējo darba devēju.</span><span class="sxs-lookup"><span data-stu-id="e5522-183">Signifies whether the candidate allows contacting the previous employer.</span></span> |
| <span data-ttu-id="e5522-184">**Piezīmes**</span><span class="sxs-lookup"><span data-stu-id="e5522-184">**Notes**</span></span><br><span data-ttu-id="e5522-185">mshr_note</span><span class="sxs-lookup"><span data-stu-id="e5522-185">mshr_note</span></span><br><span data-ttu-id="e5522-186">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="e5522-186">*String*</span></span> | <span data-ttu-id="e5522-187">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="e5522-187">Read/write</span></span><br><span data-ttu-id="e5522-188">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="e5522-188">Optional</span></span> | <span data-ttu-id="e5522-189">Piezīmes, ko izmantot darbā pieņēmējam vai personāla atlases darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="e5522-189">Notes for use by the recruiter or hiring manager.</span></span> |
| <span data-ttu-id="e5522-190">**Primārais lauks**</span><span class="sxs-lookup"><span data-stu-id="e5522-190">**Primary Field**</span></span><br><span data-ttu-id="e5522-191">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="e5522-191">mshr_primaryfield</span></span><br><span data-ttu-id="e5522-192">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="e5522-192">*String*</span></span> | <span data-ttu-id="e5522-193">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="e5522-193">Read-only</span></span><br><span data-ttu-id="e5522-194">Obligāts</span><span class="sxs-lookup"><span data-stu-id="e5522-194">Required</span></span> | <span data-ttu-id="e5522-195">Lauks, kas tiek izmantots kā elementa ieraksta primārais identifikators.</span><span class="sxs-lookup"><span data-stu-id="e5522-195">Field used as a primary identifier of the entity record.</span></span> <span data-ttu-id="e5522-196">Puses numura, sākuma datuma, darba devēja amata un darba devēja vārda kombinācija.</span><span class="sxs-lookup"><span data-stu-id="e5522-196">Combination of party number, start date, employer position, and employer name.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e5522-197">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="e5522-197">See also</span></span>

[<span data-ttu-id="e5522-198">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="e5522-198">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="e5522-199">Piemērs Kandidāta vaicājumam par nolīgšanu</span><span class="sxs-lookup"><span data-stu-id="e5522-199">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
