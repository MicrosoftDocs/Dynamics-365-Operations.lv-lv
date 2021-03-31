---
title: Darbā pieņemšanas pieprasījuma atrašanās vieta
description: Šajā tēmā aprakstīta personāla atlases pieprasījuma atrašanās vietas elements, kas iestatīts programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: fa153b1cfcbb70294ed6da3618c83396df04f8db
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125237"
---
# <a name="recruiting-request-location"></a><span data-ttu-id="93dc4-103">Darbā pieņemšanas pieprasījuma atrašanās vieta</span><span class="sxs-lookup"><span data-stu-id="93dc4-103">Recruiting request location</span></span>

<span data-ttu-id="93dc4-104">Šajā tēmā aprakstīta personāla atlases pieprasījuma atrašanās vietas elements, kas iestatīts programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="93dc4-104">This topic describes the Recruiting request location entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="93dc4-105">Fiziskais nosaukums: mshr_hcmrecruitingrequestlocationentity</span><span class="sxs-lookup"><span data-stu-id="93dc4-105">Physical name: mshr_hcmrecruitingrequestlocationentity</span></span>

### <a name="description"></a><span data-ttu-id="93dc4-106">Apraksts</span><span class="sxs-lookup"><span data-stu-id="93dc4-106">Description</span></span>

<span data-ttu-id="93dc4-107">To vietu saraksts, kas definētas kā vietas, kur darbā pieņemtie darbinieki strādās pēc nolīgšanas.</span><span class="sxs-lookup"><span data-stu-id="93dc4-107">The list of locations defined as locations where recruited employees will work upon hiring.</span></span> <span data-ttu-id="93dc4-108">Šīs ir vietas, kas izveidotas juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="93dc4-108">These are locations created across legal entities.</span></span>

### <a name="json-representation"></a><span data-ttu-id="93dc4-109">JSON pārstāvība</span><span class="sxs-lookup"><span data-stu-id="93dc4-109">JSON representation</span></span>

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a><span data-ttu-id="93dc4-110">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="93dc4-110">Properties</span></span>

| <span data-ttu-id="93dc4-111">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="93dc4-111">Property</span></span><br><span data-ttu-id="93dc4-112">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="93dc4-112">**Physical name**</span></span><br><span data-ttu-id="93dc4-113">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="93dc4-113">**_Type_**</span></span> | <span data-ttu-id="93dc4-114">Izmantot</span><span class="sxs-lookup"><span data-stu-id="93dc4-114">Use</span></span> | <span data-ttu-id="93dc4-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="93dc4-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="93dc4-116">**Atrašanās vietas ID**</span><span class="sxs-lookup"><span data-stu-id="93dc4-116">**Location ID**</span></span><br><span data-ttu-id="93dc4-117">mshr_locationid</span><span class="sxs-lookup"><span data-stu-id="93dc4-117">mshr_locationid</span></span><br><span data-ttu-id="93dc4-118">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="93dc4-118">*String*</span></span> | <span data-ttu-id="93dc4-119">Rakstīt vienu reizi</span><span class="sxs-lookup"><span data-stu-id="93dc4-119">Write-once</span></span><br><span data-ttu-id="93dc4-120">Obligāts</span><span class="sxs-lookup"><span data-stu-id="93dc4-120">Required</span></span> | <span data-ttu-id="93dc4-121">Sistēmas ģenerēts lietotājam lasāms identifikators darbā pieņemšanas atrašanās vietai.</span><span class="sxs-lookup"><span data-stu-id="93dc4-121">The system-generated, user-readable identifier for the recruiting location.</span></span> |
| <span data-ttu-id="93dc4-122">**Darbā pieņemšanas pieprasījuma atrašanās vieta**</span><span class="sxs-lookup"><span data-stu-id="93dc4-122">**Recruiting Request Location**</span></span><br><span data-ttu-id="93dc4-123">mshr_recruitingrequestlocationid</span><span class="sxs-lookup"><span data-stu-id="93dc4-123">mshr_recruitingrequestlocationid</span></span><br><span data-ttu-id="93dc4-124">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="93dc4-124">*String*</span></span> | <span data-ttu-id="93dc4-125">Rakstīt vienu reizi</span><span class="sxs-lookup"><span data-stu-id="93dc4-125">Write-once</span></span><br><span data-ttu-id="93dc4-126">Obligāts</span><span class="sxs-lookup"><span data-stu-id="93dc4-126">Required</span></span> | <span data-ttu-id="93dc4-127">Lietotāja definēts unikāls darbā pieņemšanas atrašanās vietas identifikators.</span><span class="sxs-lookup"><span data-stu-id="93dc4-127">User-defined unique identifier for the recruiting location.</span></span> |
| <span data-ttu-id="93dc4-128">**Personāla atlases pieprasījuma atrašanās vietas elementa ID**</span><span class="sxs-lookup"><span data-stu-id="93dc4-128">**Recruiting Request Location Entity ID**</span></span><br><span data-ttu-id="93dc4-129">mshr_hcmrecruitingrequestlocationentityid</span><span class="sxs-lookup"><span data-stu-id="93dc4-129">mshr_hcmrecruitingrequestlocationentityid</span></span><br><span data-ttu-id="93dc4-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="93dc4-130">*GUID*</span></span> | <span data-ttu-id="93dc4-131">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="93dc4-131">Read-only</span></span><br><span data-ttu-id="93dc4-132">Obligāts</span><span class="sxs-lookup"><span data-stu-id="93dc4-132">Required</span></span> | <span data-ttu-id="93dc4-133">Sistēmas ģenerēts unikāls identifikators Personāla atlases pieprasījuma atrašanās vietas ierakstam.</span><span class="sxs-lookup"><span data-stu-id="93dc4-133">System-generated unique identifier for the recruiting request location record.</span></span> |
| <span data-ttu-id="93dc4-134">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="93dc4-134">**Description**</span></span><br><span data-ttu-id="93dc4-135">mshr_description</span><span class="sxs-lookup"><span data-stu-id="93dc4-135">mshr_description</span></span><br><span data-ttu-id="93dc4-136">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="93dc4-136">*String*</span></span> | <span data-ttu-id="93dc4-137">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="93dc4-137">Read/write</span></span><br><span data-ttu-id="93dc4-138">Obligāts</span><span class="sxs-lookup"><span data-stu-id="93dc4-138">Required</span></span> | <span data-ttu-id="93dc4-139">Vietas apraksts.</span><span class="sxs-lookup"><span data-stu-id="93dc4-139">Description of the location.</span></span> |
| <span data-ttu-id="93dc4-140">**Valsts/reģiona ID**</span><span class="sxs-lookup"><span data-stu-id="93dc4-140">**Country/Region ID**</span></span><br><span data-ttu-id="93dc4-141">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="93dc4-141">mshr_countryregionid</span></span><br><span data-ttu-id="93dc4-142">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="93dc4-142">*String*</span></span> | <span data-ttu-id="93dc4-143">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="93dc4-143">Read-only</span></span><br><span data-ttu-id="93dc4-144">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="93dc4-144">Optional</span></span> | <span data-ttu-id="93dc4-145">Norāda valsti vai reģionu, kur kandidātam ir pilsonība.</span><span class="sxs-lookup"><span data-stu-id="93dc4-145">Specifies the country or region where the candidate has citizenship.</span></span> |
| <span data-ttu-id="93dc4-146">**Valsts/reģiona ID vērtība**</span><span class="sxs-lookup"><span data-stu-id="93dc4-146">**Country/Region ID Value**</span></span><br><span data-ttu-id="93dc4-147">_mshr_fk_countriregion_id_value</span><span class="sxs-lookup"><span data-stu-id="93dc4-147">_mshr_fk_countriregion_id_value</span></span><br><span data-ttu-id="93dc4-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="93dc4-148">*GUID*</span></span> | <span data-ttu-id="93dc4-149">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="93dc4-149">Read-only</span></span><br><span data-ttu-id="93dc4-150">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="93dc4-150">Optional</span></span><br><span data-ttu-id="93dc4-151">Ārējā atslēga: mshr_logisticsaddresscountryregionentity mshr_logisticaddresscountryregionentityid</span><span class="sxs-lookup"><span data-stu-id="93dc4-151">Foreign key: mshr_logisticaddresscountryregionentityid of mshr_logisticsaddresscountryregionentity</span></span> | <span data-ttu-id="93dc4-152">Sistēmas ģenerēts unikālais adreses valsts/reģiona identifikators.</span><span class="sxs-lookup"><span data-stu-id="93dc4-152">System-generated unique identifier of the country/region of the address.</span></span> |
| <span data-ttu-id="93dc4-153">**Pasta indekss**</span><span class="sxs-lookup"><span data-stu-id="93dc4-153">**ZipCode**</span></span><br><span data-ttu-id="93dc4-154">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="93dc4-154">mshr_zipcode</span></span><br><span data-ttu-id="93dc4-155">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="93dc4-155">*String*</span></span> | <span data-ttu-id="93dc4-156">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="93dc4-156">Read-only</span></span><br><span data-ttu-id="93dc4-157">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="93dc4-157">Optional</span></span> | <span data-ttu-id="93dc4-158">Pasta indekss.</span><span class="sxs-lookup"><span data-stu-id="93dc4-158">Zip/postal code.</span></span> |
| <span data-ttu-id="93dc4-159">**Iela**</span><span class="sxs-lookup"><span data-stu-id="93dc4-159">**Street**</span></span><br><span data-ttu-id="93dc4-160">mshr_street</span><span class="sxs-lookup"><span data-stu-id="93dc4-160">mshr_street</span></span><br><span data-ttu-id="93dc4-161">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="93dc4-161">*String*</span></span> | <span data-ttu-id="93dc4-162">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="93dc4-162">Read-only</span></span><br><span data-ttu-id="93dc4-163">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="93dc4-163">Optional</span></span> | <span data-ttu-id="93dc4-164">Ielas adrese.</span><span class="sxs-lookup"><span data-stu-id="93dc4-164">Street address.</span></span> |
| <span data-ttu-id="93dc4-165">**Pilsēta**</span><span class="sxs-lookup"><span data-stu-id="93dc4-165">**City**</span></span><br><span data-ttu-id="93dc4-166">mshr_city</span><span class="sxs-lookup"><span data-stu-id="93dc4-166">mshr_city</span></span><br><span data-ttu-id="93dc4-167">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="93dc4-167">*String*</span></span> | <span data-ttu-id="93dc4-168">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="93dc4-168">Read-only</span></span><br><span data-ttu-id="93dc4-169">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="93dc4-169">Optional</span></span> | <span data-ttu-id="93dc4-170">Pilsēta.</span><span class="sxs-lookup"><span data-stu-id="93dc4-170">City.</span></span> |
| <span data-ttu-id="93dc4-171">**Novads**</span><span class="sxs-lookup"><span data-stu-id="93dc4-171">**State**</span></span><br><span data-ttu-id="93dc4-172">mshr_state</span><span class="sxs-lookup"><span data-stu-id="93dc4-172">mshr_state</span></span><br><span data-ttu-id="93dc4-173">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="93dc4-173">*String*</span></span> | <span data-ttu-id="93dc4-174">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="93dc4-174">Read-only</span></span><br><span data-ttu-id="93dc4-175">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="93dc4-175">Optional</span></span> | <span data-ttu-id="93dc4-176">Novads.</span><span class="sxs-lookup"><span data-stu-id="93dc4-176">State or province.</span></span> |
| <span data-ttu-id="93dc4-177">**Pagasts**</span><span class="sxs-lookup"><span data-stu-id="93dc4-177">**County**</span></span><br><span data-ttu-id="93dc4-178">mshr_county</span><span class="sxs-lookup"><span data-stu-id="93dc4-178">mshr_county</span></span><br><span data-ttu-id="93dc4-179">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="93dc4-179">*String*</span></span> | <span data-ttu-id="93dc4-180">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="93dc4-180">Read-only</span></span><br><span data-ttu-id="93dc4-181">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="93dc4-181">Optional</span></span> | <span data-ttu-id="93dc4-182">Pagasts.</span><span class="sxs-lookup"><span data-stu-id="93dc4-182">County.</span></span> |
| <span data-ttu-id="93dc4-183">**Tālrunis**</span><span class="sxs-lookup"><span data-stu-id="93dc4-183">**Telephone**</span></span><br><span data-ttu-id="93dc4-184">mshr_telephone</span><span class="sxs-lookup"><span data-stu-id="93dc4-184">mshr_telephone</span></span><br><span data-ttu-id="93dc4-185">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="93dc4-185">*String*</span></span> | <span data-ttu-id="93dc4-186">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="93dc4-186">Read/write</span></span><br><span data-ttu-id="93dc4-187">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="93dc4-187">Optional</span></span> | <span data-ttu-id="93dc4-188">Atrašanās vietas tālruņa numurs.</span><span class="sxs-lookup"><span data-stu-id="93dc4-188">Telephone number for the location.</span></span> |
| <span data-ttu-id="93dc4-189">**E-pasts**</span><span class="sxs-lookup"><span data-stu-id="93dc4-189">**Email**</span></span><br><span data-ttu-id="93dc4-190">mshr_email</span><span class="sxs-lookup"><span data-stu-id="93dc4-190">mshr_email</span></span><br><span data-ttu-id="93dc4-191">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="93dc4-191">*String*</span></span> | <span data-ttu-id="93dc4-192">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="93dc4-192">Read/write</span></span><br><span data-ttu-id="93dc4-193">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="93dc4-193">Optional</span></span> | <span data-ttu-id="93dc4-194">E-pasta adrese.</span><span class="sxs-lookup"><span data-stu-id="93dc4-194">Email address.</span></span> |
| <span data-ttu-id="93dc4-195">**InternetAddress**</span><span class="sxs-lookup"><span data-stu-id="93dc4-195">**InternetAddress**</span></span><br><span data-ttu-id="93dc4-196">mshr_internetaddress</span><span class="sxs-lookup"><span data-stu-id="93dc4-196">mshr_internetaddress</span></span><br><span data-ttu-id="93dc4-197">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="93dc4-197">*String*</span></span> | <span data-ttu-id="93dc4-198">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="93dc4-198">Read/write</span></span><br><span data-ttu-id="93dc4-199">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="93dc4-199">Optional</span></span> | <span data-ttu-id="93dc4-200">Atrašanās vietas vietnes vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="93dc4-200">URL for the location website.</span></span> |
| <span data-ttu-id="93dc4-201">**Datu apgabala ID**</span><span class="sxs-lookup"><span data-stu-id="93dc4-201">**Data Area ID**</span></span><br><span data-ttu-id="93dc4-202">mshr_dataareaid</span><span class="sxs-lookup"><span data-stu-id="93dc4-202">mshr_dataareaid</span></span><br><span data-ttu-id="93dc4-203">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="93dc4-203">*String*</span></span> | <span data-ttu-id="93dc4-204">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="93dc4-204">Read/write</span></span><br><span data-ttu-id="93dc4-205">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="93dc4-205">Optional</span></span> | <span data-ttu-id="93dc4-206">Norāda juridisko personu (uzņēmumu).</span><span class="sxs-lookup"><span data-stu-id="93dc4-206">Specifies the legal entity (company).</span></span> |
| <span data-ttu-id="93dc4-207">**Datu apgabala ID vērtība**</span><span class="sxs-lookup"><span data-stu-id="93dc4-207">**Data Area ID Value**</span></span><br><span data-ttu-id="93dc4-208">_mshr_dataareaid_id_value</span><span class="sxs-lookup"><span data-stu-id="93dc4-208">_mshr_dataareaid_id_value</span></span><br><span data-ttu-id="93dc4-209">*GUID*</span><span class="sxs-lookup"><span data-stu-id="93dc4-209">*GUID*</span></span> | <span data-ttu-id="93dc4-210">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="93dc4-210">Read-only</span></span><br><span data-ttu-id="93dc4-211">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="93dc4-211">Optional</span></span><br><span data-ttu-id="93dc4-212">Ārējā atslēga: cdm_companyid cdm_company elements</span><span class="sxs-lookup"><span data-stu-id="93dc4-212">Foreign key: cdm_companyid of cdm_company entity</span></span> | <span data-ttu-id="93dc4-213">Sistēmas ģenerēta GUID vērtība, kas identificē juridisko personu (uzņēmumu).</span><span class="sxs-lookup"><span data-stu-id="93dc4-213">System-generated GUID value identifying the legal entity (company).</span></span> |

## <a name="see-also"></a><span data-ttu-id="93dc4-214">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="93dc4-214">See also</span></span>

[<span data-ttu-id="93dc4-215">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="93dc4-215">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="93dc4-216">Piemērs personāla atlases pieprasījuma vaicājumam</span><span class="sxs-lookup"><span data-stu-id="93dc4-216">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
