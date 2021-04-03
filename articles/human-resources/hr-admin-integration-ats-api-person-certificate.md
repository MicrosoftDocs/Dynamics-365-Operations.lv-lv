---
title: Personas sertifikāts
description: Šajā tēmā aprakstīts Personas sertifikāta elements programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: 4587337d8fd52828309826f3301b6f053b267819
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466524"
---
# <a name="person-certificate"></a><span data-ttu-id="3fa00-103">Personas sertifikāts</span><span class="sxs-lookup"><span data-stu-id="3fa00-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3fa00-104">Šajā tēmā aprakstīts Personas sertifikāta elements programmai Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="3fa00-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="3fa00-105">Fiziskais nosaukums: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="3fa00-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="3fa00-106">Apraksts</span><span class="sxs-lookup"><span data-stu-id="3fa00-106">Description</span></span>

<span data-ttu-id="3fa00-107">Šis elements apraksta kandidāta profesionālos sertifikātus.</span><span class="sxs-lookup"><span data-stu-id="3fa00-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3fa00-108">JSON pārstāvība</span><span class="sxs-lookup"><span data-stu-id="3fa00-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="3fa00-109">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="3fa00-109">Properties</span></span>

| <span data-ttu-id="3fa00-110">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="3fa00-110">Property</span></span><br><span data-ttu-id="3fa00-111">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="3fa00-111">**Physical name**</span></span><br><span data-ttu-id="3fa00-112">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="3fa00-112">**_Type_**</span></span> | <span data-ttu-id="3fa00-113">Izmantot</span><span class="sxs-lookup"><span data-stu-id="3fa00-113">Use</span></span> | <span data-ttu-id="3fa00-114">Apraksts</span><span class="sxs-lookup"><span data-stu-id="3fa00-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3fa00-115">**Personas sertifikāta elementa ID**</span><span class="sxs-lookup"><span data-stu-id="3fa00-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="3fa00-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="3fa00-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="3fa00-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3fa00-117">*GUID*</span></span> | <span data-ttu-id="3fa00-118">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="3fa00-118">Read-only</span></span><br><span data-ttu-id="3fa00-119">Obligāts</span><span class="sxs-lookup"><span data-stu-id="3fa00-119">Required</span></span> | <span data-ttu-id="3fa00-120">Sistēmas ģenerēts unikāls identifikators personas sertifikāta elementa ierakstam.</span><span class="sxs-lookup"><span data-stu-id="3fa00-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="3fa00-121">**Puses numurs**</span><span class="sxs-lookup"><span data-stu-id="3fa00-121">**Party Number**</span></span><br><span data-ttu-id="3fa00-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="3fa00-122">mshr_partynumber</span></span><br><span data-ttu-id="3fa00-123">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="3fa00-123">*String*</span></span> | <span data-ttu-id="3fa00-124">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="3fa00-124">Read/write</span></span><br><span data-ttu-id="3fa00-125">Obligāts</span><span class="sxs-lookup"><span data-stu-id="3fa00-125">Required</span></span> | <span data-ttu-id="3fa00-126">Kandidāta puses (personas) ID.</span><span class="sxs-lookup"><span data-stu-id="3fa00-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="3fa00-127">**Personas ID vērtība**</span><span class="sxs-lookup"><span data-stu-id="3fa00-127">**Person ID Value**</span></span><br><span data-ttu-id="3fa00-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="3fa00-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="3fa00-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3fa00-129">*GUID*</span></span> | <span data-ttu-id="3fa00-130">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="3fa00-130">Read-only</span></span><br><span data-ttu-id="3fa00-131">Obligāts</span><span class="sxs-lookup"><span data-stu-id="3fa00-131">Required</span></span><br><span data-ttu-id="3fa00-132">Ārējā atslēga: mshr_dirpersonentity mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="3fa00-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="3fa00-133">Sistēmas ģenerēts puses (personas) elementa ieraksta identifikators.</span><span class="sxs-lookup"><span data-stu-id="3fa00-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="3fa00-134">**Sertifikāta veida ID**</span><span class="sxs-lookup"><span data-stu-id="3fa00-134">**Certificate Type ID**</span></span><br><span data-ttu-id="3fa00-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="3fa00-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="3fa00-136">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="3fa00-136">*String*</span></span> | <span data-ttu-id="3fa00-137">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="3fa00-137">Read/write</span></span><br><span data-ttu-id="3fa00-138">Obligāts</span><span class="sxs-lookup"><span data-stu-id="3fa00-138">Required</span></span> |  <span data-ttu-id="3fa00-139">Personāla vadībā definētā sertifikāta veida identifikators.</span><span class="sxs-lookup"><span data-stu-id="3fa00-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="3fa00-140">**Sertifikāta veida ID vērtība**</span><span class="sxs-lookup"><span data-stu-id="3fa00-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="3fa00-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="3fa00-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="3fa00-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3fa00-142">*GUID*</span></span> | <span data-ttu-id="3fa00-143">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="3fa00-143">Read-only</span></span><br><span data-ttu-id="3fa00-144">Obligāts</span><span class="sxs-lookup"><span data-stu-id="3fa00-144">Required</span></span><br><span data-ttu-id="3fa00-145">Ārējā atslēga: mshr_hcmcertificatetypeentity mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="3fa00-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="3fa00-146">Sistēmas ģenerēts saistītā elementa sertifikāta veida unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="3fa00-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="3fa00-147">**Sākuma datums**</span><span class="sxs-lookup"><span data-stu-id="3fa00-147">**Start Date**</span></span><br><span data-ttu-id="3fa00-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="3fa00-148">mshr_startdate</span></span><br><span data-ttu-id="3fa00-149">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="3fa00-149">*Datetime*</span></span> | <span data-ttu-id="3fa00-150">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="3fa00-150">Read/write</span></span><br><span data-ttu-id="3fa00-151">Obligāts</span><span class="sxs-lookup"><span data-stu-id="3fa00-151">Required</span></span> | <span data-ttu-id="3fa00-152">Datums, kurā sertifikāts tika izsniegts.</span><span class="sxs-lookup"><span data-stu-id="3fa00-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="3fa00-153">**Beigu datums**</span><span class="sxs-lookup"><span data-stu-id="3fa00-153">**End Date**</span></span><br><span data-ttu-id="3fa00-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="3fa00-154">mshr_enddate</span></span><br><span data-ttu-id="3fa00-155">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="3fa00-155">*Datetime*</span></span> | <span data-ttu-id="3fa00-156">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="3fa00-156">Read/write</span></span><br><span data-ttu-id="3fa00-157">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="3fa00-157">Optional</span></span> | <span data-ttu-id="3fa00-158">Datums, kurā sertifikāta derīgums beigsies.</span><span class="sxs-lookup"><span data-stu-id="3fa00-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="3fa00-159">**Piezīmes**</span><span class="sxs-lookup"><span data-stu-id="3fa00-159">**Notes**</span></span><br><span data-ttu-id="3fa00-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="3fa00-160">mshr_notes</span></span><br><span data-ttu-id="3fa00-161">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="3fa00-161">*String*</span></span> | <span data-ttu-id="3fa00-162">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="3fa00-162">Read/write</span></span><br><span data-ttu-id="3fa00-163">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="3fa00-163">Optional</span></span> | <span data-ttu-id="3fa00-164">Piezīmes, ko izmantot personāla atlases darbiniekiem un darbā pieņēmējiem.</span><span class="sxs-lookup"><span data-stu-id="3fa00-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="3fa00-165">**Primārais lauks**</span><span class="sxs-lookup"><span data-stu-id="3fa00-165">**Primary Field**</span></span><br><span data-ttu-id="3fa00-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="3fa00-166">mshr_primaryfield</span></span><br><span data-ttu-id="3fa00-167">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="3fa00-167">*String*</span></span> | <span data-ttu-id="3fa00-168">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="3fa00-168">Read-only</span></span><br><span data-ttu-id="3fa00-169">Obligāts</span><span class="sxs-lookup"><span data-stu-id="3fa00-169">Required</span></span> |  <span data-ttu-id="3fa00-170">Lauks, kas jāizmanto kā elementa ieraksta identifikators.</span><span class="sxs-lookup"><span data-stu-id="3fa00-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="3fa00-171">Puses numura, sertifikāta veida ID un sākuma datuma kombinācija.</span><span class="sxs-lookup"><span data-stu-id="3fa00-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3fa00-172">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="3fa00-172">See also</span></span>

[<span data-ttu-id="3fa00-173">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="3fa00-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="3fa00-174">Piemērs Kandidāta vaicājumam par nolīgšanu</span><span class="sxs-lookup"><span data-stu-id="3fa00-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]