---
title: Sertifikāta veids
description: Šajā tēmā aprakstīta Sertifikāta veida entītija programmai Dynamics 365 Human Resources .
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b8e979f242eb689b730b7f8a8684b3e697adbee6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054696"
---
# <a name="certificate-type"></a><span data-ttu-id="bff17-103">Sertifikāta veids</span><span class="sxs-lookup"><span data-stu-id="bff17-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bff17-104">Šajā tēmā aprakstīta Sertifikāta veida entītija programmai Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="bff17-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="bff17-105">Fiziskais nosaukums: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="bff17-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="bff17-106">Apraksts</span><span class="sxs-lookup"><span data-stu-id="bff17-106">Description</span></span>

<span data-ttu-id="bff17-107">Šī entītija definē profesionālo sertifikātu veidu sarakstu, kas iestatīti programmai Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bff17-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="bff17-108">Šī entītija nav specifiska juridiskajai personai (uzņēmumam).</span><span class="sxs-lookup"><span data-stu-id="bff17-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="bff17-109">JSON pārstāvība</span><span class="sxs-lookup"><span data-stu-id="bff17-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="bff17-110">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="bff17-110">Properties</span></span>

| <span data-ttu-id="bff17-111">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="bff17-111">Property</span></span><br><span data-ttu-id="bff17-112">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="bff17-112">**Physical name**</span></span><br><span data-ttu-id="bff17-113">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="bff17-113">**_Type_**</span></span> | <span data-ttu-id="bff17-114">Izmantot</span><span class="sxs-lookup"><span data-stu-id="bff17-114">Use</span></span> | <span data-ttu-id="bff17-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="bff17-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="bff17-116">**Sertifikāta veida elementa ID**</span><span class="sxs-lookup"><span data-stu-id="bff17-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="bff17-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="bff17-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="bff17-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="bff17-118">*GUID*</span></span> | <span data-ttu-id="bff17-119">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="bff17-119">Read-only</span></span><br><span data-ttu-id="bff17-120">Obligāts</span><span class="sxs-lookup"><span data-stu-id="bff17-120">Required</span></span> 
<span data-ttu-id="bff17-121">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="bff17-121">System-generated</span></span> | <span data-ttu-id="bff17-122">Unikāls sertifikāta veida primārais identifikators.</span><span class="sxs-lookup"><span data-stu-id="bff17-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="bff17-123">**Sertifikāta veids**</span><span class="sxs-lookup"><span data-stu-id="bff17-123">**Certificate Type**</span></span><br><span data-ttu-id="bff17-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="bff17-124">mshr_certificatetype</span></span><br><span data-ttu-id="bff17-125">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="bff17-125">*String*</span></span> | <span data-ttu-id="bff17-126">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="bff17-126">Read/write</span></span><br><span data-ttu-id="bff17-127">Obligāts</span><span class="sxs-lookup"><span data-stu-id="bff17-127">Required</span></span> | <span data-ttu-id="bff17-128">Unikāls sertifikāta veida lietotājam lasāms identifikators.</span><span class="sxs-lookup"><span data-stu-id="bff17-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="bff17-129">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="bff17-129">**Description**</span></span><br><span data-ttu-id="bff17-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="bff17-130">mshr_description</span></span><br><span data-ttu-id="bff17-131">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="bff17-131">*String*</span></span> | <span data-ttu-id="bff17-132">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="bff17-132">Read/write</span></span><br><span data-ttu-id="bff17-133">Obligāts</span><span class="sxs-lookup"><span data-stu-id="bff17-133">Required</span></span> | <span data-ttu-id="bff17-134">Sertifikāta veida apraksts.</span><span class="sxs-lookup"><span data-stu-id="bff17-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="bff17-135">**Nepieciešama atjaunošana**</span><span class="sxs-lookup"><span data-stu-id="bff17-135">**Require Renewal**</span></span><br><span data-ttu-id="bff17-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="bff17-136">mshr_requirerenewal</span></span><br><span data-ttu-id="bff17-137">*mshr_noyes opciju kopa*</span><span class="sxs-lookup"><span data-stu-id="bff17-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="bff17-138">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="bff17-138">Read/write</span></span><br><span data-ttu-id="bff17-139">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="bff17-139">Optional</span></span> | <span data-ttu-id="bff17-140">Norāda, vai sertifikātam ir nepieciešama atjaunošana.</span><span class="sxs-lookup"><span data-stu-id="bff17-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="bff17-141">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="bff17-141">See also</span></span>

[<span data-ttu-id="bff17-142">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="bff17-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="bff17-143">Piemērs Kandidāta vaicājumam par nolīgšanu</span><span class="sxs-lookup"><span data-stu-id="bff17-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]