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
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125261"
---
# <a name="rating-level"></a><span data-ttu-id="7ec21-103">Novērtējuma līmenis</span><span class="sxs-lookup"><span data-stu-id="7ec21-103">Rating level</span></span>

<span data-ttu-id="7ec21-104">Šajā tēmā aprakstīta Novērtējuma līmenis entītija programmai Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="7ec21-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="7ec21-105">Fiziskais nosaukums: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="7ec21-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="7ec21-106">Apraksts</span><span class="sxs-lookup"><span data-stu-id="7ec21-106">Description</span></span>

<span data-ttu-id="7ec21-107">Šis elements nodrošina pieejamos prasmju novērtējuma līmeņus.</span><span class="sxs-lookup"><span data-stu-id="7ec21-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="7ec21-108">Novērtējuma līmeņi attiecas uz visām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="7ec21-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="7ec21-109">JSON pārstāvība</span><span class="sxs-lookup"><span data-stu-id="7ec21-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="7ec21-110">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="7ec21-110">Properties</span></span>

| <span data-ttu-id="7ec21-111">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="7ec21-111">Property</span></span><br><span data-ttu-id="7ec21-112">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="7ec21-112">**Physical name**</span></span><br><span data-ttu-id="7ec21-113">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="7ec21-113">**_Type_**</span></span> | <span data-ttu-id="7ec21-114">Izmantot</span><span class="sxs-lookup"><span data-stu-id="7ec21-114">Use</span></span> | <span data-ttu-id="7ec21-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="7ec21-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7ec21-116">**Novērtējuma līmeņa elementa ID**</span><span class="sxs-lookup"><span data-stu-id="7ec21-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="7ec21-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="7ec21-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="7ec21-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7ec21-118">*GUID*</span></span> | <span data-ttu-id="7ec21-119">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="7ec21-119">Read-only</span></span><br><span data-ttu-id="7ec21-120">Obligāts</span><span class="sxs-lookup"><span data-stu-id="7ec21-120">Required</span></span><br><span data-ttu-id="7ec21-121">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="7ec21-121">System-generated</span></span> | <span data-ttu-id="7ec21-122">Sistēmas ģenerēts līmeņa unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="7ec21-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="7ec21-123">**Novērtējuma līmeņa ID**</span><span class="sxs-lookup"><span data-stu-id="7ec21-123">**Rating Level ID**</span></span><br><span data-ttu-id="7ec21-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="7ec21-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="7ec21-125">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="7ec21-125">*String*</span></span> | <span data-ttu-id="7ec21-126">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="7ec21-126">Read/write</span></span><br><span data-ttu-id="7ec21-127">Obligāts</span><span class="sxs-lookup"><span data-stu-id="7ec21-127">Required</span></span> | <span data-ttu-id="7ec21-128">Unikāls lietotājam lasāms līmeņa identifikators.</span><span class="sxs-lookup"><span data-stu-id="7ec21-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="7ec21-129">**Novērtēšanas modeļa ID**</span><span class="sxs-lookup"><span data-stu-id="7ec21-129">**Rating Model ID**</span></span><br><span data-ttu-id="7ec21-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="7ec21-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="7ec21-131">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="7ec21-131">*String*</span></span> | <span data-ttu-id="7ec21-132">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="7ec21-132">Read/write</span></span><br><span data-ttu-id="7ec21-133">Obligāts</span><span class="sxs-lookup"><span data-stu-id="7ec21-133">Required</span></span> | <span data-ttu-id="7ec21-134">Novērtēšanas modelis, kuram pieder novērtēšanas līmenis.</span><span class="sxs-lookup"><span data-stu-id="7ec21-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="7ec21-135">**Novērtējuma modeļa elementa ID**</span><span class="sxs-lookup"><span data-stu-id="7ec21-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="7ec21-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="7ec21-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="7ec21-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7ec21-137">*GUID*</span></span> | <span data-ttu-id="7ec21-138">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="7ec21-138">Read-only</span></span><br><span data-ttu-id="7ec21-139">Obligāts</span><span class="sxs-lookup"><span data-stu-id="7ec21-139">Required</span></span><br><span data-ttu-id="7ec21-140">Ārējā atslēga: mshr_hcmratingmodelentity mshr_hcmratingmodelentityid</span><span class="sxs-lookup"><span data-stu-id="7ec21-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="7ec21-141">Sistēmas ģenerēts identifikators novērtēšanas modelim, kuram pieder novērtēšanas līmenis.</span><span class="sxs-lookup"><span data-stu-id="7ec21-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="7ec21-142">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="7ec21-142">**Description**</span></span><br><span data-ttu-id="7ec21-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="7ec21-143">mshr_description</span></span><br><span data-ttu-id="7ec21-144">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="7ec21-144">*String*</span></span> | <span data-ttu-id="7ec21-145">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="7ec21-145">Read/write</span></span><br><span data-ttu-id="7ec21-146">Obligāts</span><span class="sxs-lookup"><span data-stu-id="7ec21-146">Required</span></span> | <span data-ttu-id="7ec21-147">Novērtējuma līmeņa apraksts.</span><span class="sxs-lookup"><span data-stu-id="7ec21-147">The description of the rating level.</span></span> |
| <span data-ttu-id="7ec21-148">**Koeficients**</span><span class="sxs-lookup"><span data-stu-id="7ec21-148">**Factor**</span></span><br><span data-ttu-id="7ec21-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="7ec21-149">mshr_factor</span></span><br><span data-ttu-id="7ec21-150">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="7ec21-150">*Integer*</span></span> | <span data-ttu-id="7ec21-151">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="7ec21-151">Read/write</span></span><br><span data-ttu-id="7ec21-152">Obligāts</span><span class="sxs-lookup"><span data-stu-id="7ec21-152">Required</span></span> | <span data-ttu-id="7ec21-153">Novērtējuma līmeņa koeficients.</span><span class="sxs-lookup"><span data-stu-id="7ec21-153">The factor for the rating level.</span></span> <span data-ttu-id="7ec21-154">Salīdzinot krājumus ar dažādu novērtējuma līmeņu skaitu, koeficients tiek izmantots rādītāju normalizēšanai.</span><span class="sxs-lookup"><span data-stu-id="7ec21-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="7ec21-155">Vērtībai jābūt veselam skaitlim no 0 līdz 9.</span><span class="sxs-lookup"><span data-stu-id="7ec21-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="7ec21-156">**Piezīme.**</span><span class="sxs-lookup"><span data-stu-id="7ec21-156">**Note**</span></span><br><span data-ttu-id="7ec21-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="7ec21-157">mshr_note</span></span><br><span data-ttu-id="7ec21-158">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="7ec21-158">*String*</span></span> | <span data-ttu-id="7ec21-159">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="7ec21-159">Read/write</span></span><br><span data-ttu-id="7ec21-160">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="7ec21-160">Optional</span></span> | <span data-ttu-id="7ec21-161">Jebkādas ar novērtējuma līmeni saistītas piezīmes.</span><span class="sxs-lookup"><span data-stu-id="7ec21-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="7ec21-162">**Primārais lauks**</span><span class="sxs-lookup"><span data-stu-id="7ec21-162">**Primary Field**</span></span><br><span data-ttu-id="7ec21-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="7ec21-163">mshr_primaryfield</span></span><br><span data-ttu-id="7ec21-164">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="7ec21-164">*String*</span></span> | <span data-ttu-id="7ec21-165">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="7ec21-165">Read-only</span></span><br><span data-ttu-id="7ec21-166">Obligāts</span><span class="sxs-lookup"><span data-stu-id="7ec21-166">Required</span></span> | <span data-ttu-id="7ec21-167">Lauks, kas jāizmanto kā elementa ieraksta identifikators.</span><span class="sxs-lookup"><span data-stu-id="7ec21-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="7ec21-168">Novērtēšanas līmeņa ID un novērtēšanas modeļa ID kombinācija.</span><span class="sxs-lookup"><span data-stu-id="7ec21-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7ec21-169">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="7ec21-169">See also</span></span>

[<span data-ttu-id="7ec21-170">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="7ec21-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="7ec21-171">Piemērs Kandidāta vaicājumam par nolīgšanu</span><span class="sxs-lookup"><span data-stu-id="7ec21-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

