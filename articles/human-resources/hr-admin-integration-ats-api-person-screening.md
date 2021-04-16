---
title: Personas izvērtēšana
description: Šajā tēmā aprakstīts Personas izvērtēšanas elements Dynamics 365 Human Resources .
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bc32eb948f4a4966a927b0907b8d499486e43dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798037"
---
# <a name="person-screening"></a><span data-ttu-id="389ab-103">Personas izvērtēšana</span><span class="sxs-lookup"><span data-stu-id="389ab-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="389ab-104">Šajā tēmā aprakstīts Personas izvērtēšanas elements Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="389ab-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="389ab-105">Fiziskais nosaukums: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="389ab-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="389ab-106">Apraksts</span><span class="sxs-lookup"><span data-stu-id="389ab-106">Description</span></span>

<span data-ttu-id="389ab-107">Šis elements apraksta kandidāta izvērtēšanu, kas kandidātam ir veikta vai jāveic, lai tiktu pieņemts darbā.</span><span class="sxs-lookup"><span data-stu-id="389ab-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="389ab-108">JSON pārstāvība</span><span class="sxs-lookup"><span data-stu-id="389ab-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="389ab-109">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="389ab-109">Properties</span></span>

| <span data-ttu-id="389ab-110">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="389ab-110">Property</span></span><br><span data-ttu-id="389ab-111">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="389ab-111">**Physical name**</span></span><br><span data-ttu-id="389ab-112">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="389ab-112">**_Type_**</span></span> | <span data-ttu-id="389ab-113">Izmantot</span><span class="sxs-lookup"><span data-stu-id="389ab-113">Use</span></span> | <span data-ttu-id="389ab-114">Apraksts</span><span class="sxs-lookup"><span data-stu-id="389ab-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="389ab-115">**Personas izvērtēšanas elementa ID**</span><span class="sxs-lookup"><span data-stu-id="389ab-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="389ab-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="389ab-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="389ab-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="389ab-117">*GUID*</span></span> | <span data-ttu-id="389ab-118">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="389ab-118">Read-only</span></span><br><span data-ttu-id="389ab-119">Obligāts</span><span class="sxs-lookup"><span data-stu-id="389ab-119">Required</span></span><br><span data-ttu-id="389ab-120">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="389ab-120">System-generated</span></span> | <span data-ttu-id="389ab-121">Unikāls personas izvērtēšanas ieraksta primārais identifikators.</span><span class="sxs-lookup"><span data-stu-id="389ab-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="389ab-122">**Puses numurs**</span><span class="sxs-lookup"><span data-stu-id="389ab-122">**Party Number**</span></span><br><span data-ttu-id="389ab-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="389ab-123">mshr_partynumber</span></span><br><span data-ttu-id="389ab-124">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="389ab-124">*String*</span></span> | <span data-ttu-id="389ab-125">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="389ab-125">Read/write</span></span><br><span data-ttu-id="389ab-126">Obligāts</span><span class="sxs-lookup"><span data-stu-id="389ab-126">Required</span></span> | <span data-ttu-id="389ab-127">Ar kandidātu saistītais puses (personas) numurs.</span><span class="sxs-lookup"><span data-stu-id="389ab-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="389ab-128">**Personas ID vērtība**</span><span class="sxs-lookup"><span data-stu-id="389ab-128">**Person ID Value**</span></span><br><span data-ttu-id="389ab-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="389ab-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="389ab-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="389ab-130">*GUID*</span></span> | <span data-ttu-id="389ab-131">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="389ab-131">Read-only</span></span><br><span data-ttu-id="389ab-132">Obligāts</span><span class="sxs-lookup"><span data-stu-id="389ab-132">Required</span></span><br><span data-ttu-id="389ab-133">Ārējā atslēga: mshr_dirpersonentity mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="389ab-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="389ab-134">Sistēmas ģenerēts puses (personas) elementa ieraksta identifikators.</span><span class="sxs-lookup"><span data-stu-id="389ab-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="389ab-135">**Izvērtēšanas veida ID**</span><span class="sxs-lookup"><span data-stu-id="389ab-135">**Screening Type ID**</span></span><br><span data-ttu-id="389ab-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="389ab-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="389ab-137">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="389ab-137">*String*</span></span> | <span data-ttu-id="389ab-138">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="389ab-138">Read/write</span></span><br><span data-ttu-id="389ab-139">Obligāts</span><span class="sxs-lookup"><span data-stu-id="389ab-139">Required</span></span><br><span data-ttu-id="389ab-140">Ārējā atslēga: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="389ab-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="389ab-141">Personāla vadībā definētā izvērtēšanas veida identifikators.</span><span class="sxs-lookup"><span data-stu-id="389ab-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="389ab-142">**Izvērtēšanas veida ID vērtība**</span><span class="sxs-lookup"><span data-stu-id="389ab-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="389ab-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="389ab-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="389ab-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="389ab-144">*GUID*</span></span> | <span data-ttu-id="389ab-145">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="389ab-145">Read-only</span></span><br><span data-ttu-id="389ab-146">Obligāts</span><span class="sxs-lookup"><span data-stu-id="389ab-146">Required</span></span><br><span data-ttu-id="389ab-147">Ārējā atslēga: mshr_hcmscreeningtypeentity mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="389ab-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="389ab-148">Sistēmas ģenerēts izvērtēšanas veida ieraksta identifikators saistītajā elementā.</span><span class="sxs-lookup"><span data-stu-id="389ab-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="389ab-149">**Nepieciešams līdz šādam datumam:**</span><span class="sxs-lookup"><span data-stu-id="389ab-149">**Required By**</span></span><br><span data-ttu-id="389ab-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="389ab-150">mshr_requiredby</span></span><br><span data-ttu-id="389ab-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="389ab-151">*Datetime*</span></span> | <span data-ttu-id="389ab-152">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="389ab-152">Read/write</span></span><br><span data-ttu-id="389ab-153">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="389ab-153">Optional</span></span> | <span data-ttu-id="389ab-154">Datums, līdz kuram nepieciešams veikt izvērtēšanu.</span><span class="sxs-lookup"><span data-stu-id="389ab-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="389ab-155">**Statuss**</span><span class="sxs-lookup"><span data-stu-id="389ab-155">**Status**</span></span><br><span data-ttu-id="389ab-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="389ab-156">mshr_status</span></span><br><span data-ttu-id="389ab-157">*mshr_hcmcompletionstatus opciju kopa*</span><span class="sxs-lookup"><span data-stu-id="389ab-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="389ab-158">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="389ab-158">Read/write</span></span><br><span data-ttu-id="389ab-159">Obligāts</span><span class="sxs-lookup"><span data-stu-id="389ab-159">Required</span></span> | <span data-ttu-id="389ab-160">Sniedz kandidāta statusu izvērtēšanai.</span><span class="sxs-lookup"><span data-stu-id="389ab-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="389ab-161">**Pabeigšanas datums**</span><span class="sxs-lookup"><span data-stu-id="389ab-161">**Completed Date**</span></span><br><span data-ttu-id="389ab-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="389ab-162">mshr_completeddate</span></span><br><span data-ttu-id="389ab-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="389ab-163">*Datetime*</span></span> | <span data-ttu-id="389ab-164">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="389ab-164">Read/write</span></span><br><span data-ttu-id="389ab-165">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="389ab-165">Optional</span></span> | <span data-ttu-id="389ab-166">Datums, kad izvērtēšana tika pabeigta.</span><span class="sxs-lookup"><span data-stu-id="389ab-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="389ab-167">**Piezīmes**</span><span class="sxs-lookup"><span data-stu-id="389ab-167">**Notes**</span></span><br><span data-ttu-id="389ab-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="389ab-168">mshr_note</span></span><br><span data-ttu-id="389ab-169">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="389ab-169">*String*</span></span> | <span data-ttu-id="389ab-170">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="389ab-170">Read/write</span></span><br><span data-ttu-id="389ab-171">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="389ab-171">Optional</span></span> | <span data-ttu-id="389ab-172">Piezīmes, ko izmantot personāla atlases darbiniekiem un darbā pieņēmējiem.</span><span class="sxs-lookup"><span data-stu-id="389ab-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="389ab-173">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="389ab-173">See also</span></span>

[<span data-ttu-id="389ab-174">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="389ab-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="389ab-175">Piemērs Kandidāta vaicājumam par nolīgšanu</span><span class="sxs-lookup"><span data-stu-id="389ab-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]