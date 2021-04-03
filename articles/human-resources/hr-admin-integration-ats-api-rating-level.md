---
title: Novērtējuma līmenis
description: Šajā tēmā aprakstīta Novērtējuma līmenis entītija programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: 2dbdbea7087d8bca8563da10d1bf9a97df24e8b3
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464746"
---
# <a name="rating-level"></a><span data-ttu-id="6a040-103">Novērtējuma līmenis</span><span class="sxs-lookup"><span data-stu-id="6a040-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6a040-104">Šajā tēmā aprakstīta Novērtējuma līmenis entītija programmai Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="6a040-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="6a040-105">Fiziskais nosaukums: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="6a040-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="6a040-106">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6a040-106">Description</span></span>

<span data-ttu-id="6a040-107">Šis elements nodrošina pieejamos prasmju novērtējuma līmeņus.</span><span class="sxs-lookup"><span data-stu-id="6a040-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="6a040-108">Novērtējuma līmeņi attiecas uz visām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="6a040-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6a040-109">JSON pārstāvība</span><span class="sxs-lookup"><span data-stu-id="6a040-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="6a040-110">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="6a040-110">Properties</span></span>

| <span data-ttu-id="6a040-111">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="6a040-111">Property</span></span><br><span data-ttu-id="6a040-112">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="6a040-112">**Physical name**</span></span><br><span data-ttu-id="6a040-113">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="6a040-113">**_Type_**</span></span> | <span data-ttu-id="6a040-114">Izmantot</span><span class="sxs-lookup"><span data-stu-id="6a040-114">Use</span></span> | <span data-ttu-id="6a040-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6a040-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6a040-116">**Novērtējuma līmeņa elementa ID**</span><span class="sxs-lookup"><span data-stu-id="6a040-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="6a040-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="6a040-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="6a040-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6a040-118">*GUID*</span></span> | <span data-ttu-id="6a040-119">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="6a040-119">Read-only</span></span><br><span data-ttu-id="6a040-120">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6a040-120">Required</span></span><br><span data-ttu-id="6a040-121">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="6a040-121">System-generated</span></span> | <span data-ttu-id="6a040-122">Sistēmas ģenerēts līmeņa unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="6a040-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="6a040-123">**Novērtējuma līmeņa ID**</span><span class="sxs-lookup"><span data-stu-id="6a040-123">**Rating Level ID**</span></span><br><span data-ttu-id="6a040-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="6a040-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="6a040-125">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="6a040-125">*String*</span></span> | <span data-ttu-id="6a040-126">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="6a040-126">Read/write</span></span><br><span data-ttu-id="6a040-127">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6a040-127">Required</span></span> | <span data-ttu-id="6a040-128">Unikāls lietotājam lasāms līmeņa identifikators.</span><span class="sxs-lookup"><span data-stu-id="6a040-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="6a040-129">**Novērtēšanas modeļa ID**</span><span class="sxs-lookup"><span data-stu-id="6a040-129">**Rating Model ID**</span></span><br><span data-ttu-id="6a040-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="6a040-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="6a040-131">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="6a040-131">*String*</span></span> | <span data-ttu-id="6a040-132">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="6a040-132">Read/write</span></span><br><span data-ttu-id="6a040-133">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6a040-133">Required</span></span> | <span data-ttu-id="6a040-134">Novērtēšanas modelis, kuram pieder novērtēšanas līmenis.</span><span class="sxs-lookup"><span data-stu-id="6a040-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="6a040-135">**Novērtējuma modeļa elementa ID**</span><span class="sxs-lookup"><span data-stu-id="6a040-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="6a040-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="6a040-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="6a040-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6a040-137">*GUID*</span></span> | <span data-ttu-id="6a040-138">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="6a040-138">Read-only</span></span><br><span data-ttu-id="6a040-139">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6a040-139">Required</span></span><br><span data-ttu-id="6a040-140">Ārējā atslēga: mshr_hcmratingmodelentity mshr_hcmratingmodelentityid</span><span class="sxs-lookup"><span data-stu-id="6a040-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="6a040-141">Sistēmas ģenerēts identifikators novērtēšanas modelim, kuram pieder novērtēšanas līmenis.</span><span class="sxs-lookup"><span data-stu-id="6a040-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="6a040-142">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="6a040-142">**Description**</span></span><br><span data-ttu-id="6a040-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="6a040-143">mshr_description</span></span><br><span data-ttu-id="6a040-144">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="6a040-144">*String*</span></span> | <span data-ttu-id="6a040-145">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="6a040-145">Read/write</span></span><br><span data-ttu-id="6a040-146">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6a040-146">Required</span></span> | <span data-ttu-id="6a040-147">Novērtējuma līmeņa apraksts.</span><span class="sxs-lookup"><span data-stu-id="6a040-147">The description of the rating level.</span></span> |
| <span data-ttu-id="6a040-148">**Koeficients**</span><span class="sxs-lookup"><span data-stu-id="6a040-148">**Factor**</span></span><br><span data-ttu-id="6a040-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="6a040-149">mshr_factor</span></span><br><span data-ttu-id="6a040-150">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="6a040-150">*Integer*</span></span> | <span data-ttu-id="6a040-151">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="6a040-151">Read/write</span></span><br><span data-ttu-id="6a040-152">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6a040-152">Required</span></span> | <span data-ttu-id="6a040-153">Novērtējuma līmeņa koeficients.</span><span class="sxs-lookup"><span data-stu-id="6a040-153">The factor for the rating level.</span></span> <span data-ttu-id="6a040-154">Salīdzinot krājumus ar dažādu novērtējuma līmeņu skaitu, koeficients tiek izmantots rādītāju normalizēšanai.</span><span class="sxs-lookup"><span data-stu-id="6a040-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="6a040-155">Vērtībai jābūt veselam skaitlim no 0 līdz 9.</span><span class="sxs-lookup"><span data-stu-id="6a040-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="6a040-156">**Piezīme.**</span><span class="sxs-lookup"><span data-stu-id="6a040-156">**Note**</span></span><br><span data-ttu-id="6a040-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="6a040-157">mshr_note</span></span><br><span data-ttu-id="6a040-158">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="6a040-158">*String*</span></span> | <span data-ttu-id="6a040-159">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="6a040-159">Read/write</span></span><br><span data-ttu-id="6a040-160">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="6a040-160">Optional</span></span> | <span data-ttu-id="6a040-161">Jebkādas ar novērtējuma līmeni saistītas piezīmes.</span><span class="sxs-lookup"><span data-stu-id="6a040-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="6a040-162">**Primārais lauks**</span><span class="sxs-lookup"><span data-stu-id="6a040-162">**Primary Field**</span></span><br><span data-ttu-id="6a040-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="6a040-163">mshr_primaryfield</span></span><br><span data-ttu-id="6a040-164">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="6a040-164">*String*</span></span> | <span data-ttu-id="6a040-165">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="6a040-165">Read-only</span></span><br><span data-ttu-id="6a040-166">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6a040-166">Required</span></span> | <span data-ttu-id="6a040-167">Lauks, kas jāizmanto kā elementa ieraksta identifikators.</span><span class="sxs-lookup"><span data-stu-id="6a040-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="6a040-168">Novērtēšanas līmeņa ID un novērtēšanas modeļa ID kombinācija.</span><span class="sxs-lookup"><span data-stu-id="6a040-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="6a040-169">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="6a040-169">See also</span></span>

[<span data-ttu-id="6a040-170">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="6a040-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="6a040-171">Piemērs Kandidāta vaicājumam par nolīgšanu</span><span class="sxs-lookup"><span data-stu-id="6a040-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]