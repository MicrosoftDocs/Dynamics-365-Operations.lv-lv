---
title: Sertifikāta veids
description: Šajā tēmā aprakstīta Sertifikāta veida entītija programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125717"
---
# <a name="certificate-type"></a><span data-ttu-id="2736d-103">Sertifikāta veids</span><span class="sxs-lookup"><span data-stu-id="2736d-103">Certificate type</span></span>

<span data-ttu-id="2736d-104">Šajā tēmā aprakstīta Sertifikāta veida entītija programmai Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="2736d-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="2736d-105">Fiziskais nosaukums: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="2736d-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="2736d-106">Apraksts</span><span class="sxs-lookup"><span data-stu-id="2736d-106">Description</span></span>

<span data-ttu-id="2736d-107">Šī entītija definē profesionālo sertifikātu veidu sarakstu, kas iestatīti programmai Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2736d-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="2736d-108">Šī entītija nav specifiska juridiskajai personai (uzņēmumam).</span><span class="sxs-lookup"><span data-stu-id="2736d-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="2736d-109">JSON pārstāvība</span><span class="sxs-lookup"><span data-stu-id="2736d-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="2736d-110">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="2736d-110">Properties</span></span>

| <span data-ttu-id="2736d-111">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="2736d-111">Property</span></span><br><span data-ttu-id="2736d-112">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="2736d-112">**Physical name**</span></span><br><span data-ttu-id="2736d-113">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="2736d-113">**_Type_**</span></span> | <span data-ttu-id="2736d-114">Izmantot</span><span class="sxs-lookup"><span data-stu-id="2736d-114">Use</span></span> | <span data-ttu-id="2736d-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="2736d-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2736d-116">**Sertifikāta veida elementa ID**</span><span class="sxs-lookup"><span data-stu-id="2736d-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="2736d-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="2736d-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="2736d-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="2736d-118">*GUID*</span></span> | <span data-ttu-id="2736d-119">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="2736d-119">Read-only</span></span><br><span data-ttu-id="2736d-120">Obligāts</span><span class="sxs-lookup"><span data-stu-id="2736d-120">Required</span></span> 
<span data-ttu-id="2736d-121">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="2736d-121">System-generated</span></span> | <span data-ttu-id="2736d-122">Unikāls sertifikāta veida primārais identifikators.</span><span class="sxs-lookup"><span data-stu-id="2736d-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="2736d-123">**Sertifikāta veids**</span><span class="sxs-lookup"><span data-stu-id="2736d-123">**Certificate Type**</span></span><br><span data-ttu-id="2736d-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="2736d-124">mshr_certificatetype</span></span><br><span data-ttu-id="2736d-125">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="2736d-125">*String*</span></span> | <span data-ttu-id="2736d-126">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="2736d-126">Read/write</span></span><br><span data-ttu-id="2736d-127">Obligāts</span><span class="sxs-lookup"><span data-stu-id="2736d-127">Required</span></span> | <span data-ttu-id="2736d-128">Unikāls sertifikāta veida lietotājam lasāms identifikators.</span><span class="sxs-lookup"><span data-stu-id="2736d-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="2736d-129">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="2736d-129">**Description**</span></span><br><span data-ttu-id="2736d-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="2736d-130">mshr_description</span></span><br><span data-ttu-id="2736d-131">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="2736d-131">*String*</span></span> | <span data-ttu-id="2736d-132">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="2736d-132">Read/write</span></span><br><span data-ttu-id="2736d-133">Obligāts</span><span class="sxs-lookup"><span data-stu-id="2736d-133">Required</span></span> | <span data-ttu-id="2736d-134">Sertifikāta veida apraksts.</span><span class="sxs-lookup"><span data-stu-id="2736d-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="2736d-135">**Nepieciešama atjaunošana**</span><span class="sxs-lookup"><span data-stu-id="2736d-135">**Require Renewal**</span></span><br><span data-ttu-id="2736d-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="2736d-136">mshr_requirerenewal</span></span><br><span data-ttu-id="2736d-137">*mshr_noyes opciju kopa*</span><span class="sxs-lookup"><span data-stu-id="2736d-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="2736d-138">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="2736d-138">Read/write</span></span><br><span data-ttu-id="2736d-139">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="2736d-139">Optional</span></span> | <span data-ttu-id="2736d-140">Norāda, vai sertifikātam ir nepieciešama atjaunošana.</span><span class="sxs-lookup"><span data-stu-id="2736d-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="2736d-141">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="2736d-141">See also</span></span>

[<span data-ttu-id="2736d-142">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="2736d-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="2736d-143">Piemērs Kandidāta vaicājumam par nolīgšanu</span><span class="sxs-lookup"><span data-stu-id="2736d-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

