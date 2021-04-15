---
title: Sertifikāta veids
description: Šajā tēmā aprakstīta Sertifikāta veida entītija programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: fe5713b6b5f38ad7f6857b36c6b2f63a1dc0c320
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798397"
---
# <a name="certificate-type"></a><span data-ttu-id="d7651-103">Sertifikāta veids</span><span class="sxs-lookup"><span data-stu-id="d7651-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d7651-104">Šajā tēmā aprakstīta Sertifikāta veida entītija programmai Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="d7651-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="d7651-105">Fiziskais nosaukums: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="d7651-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="d7651-106">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d7651-106">Description</span></span>

<span data-ttu-id="d7651-107">Šī entītija definē profesionālo sertifikātu veidu sarakstu, kas iestatīti programmai Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d7651-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="d7651-108">Šī entītija nav specifiska juridiskajai personai (uzņēmumam).</span><span class="sxs-lookup"><span data-stu-id="d7651-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="d7651-109">JSON pārstāvība</span><span class="sxs-lookup"><span data-stu-id="d7651-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="d7651-110">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="d7651-110">Properties</span></span>

| <span data-ttu-id="d7651-111">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="d7651-111">Property</span></span><br><span data-ttu-id="d7651-112">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="d7651-112">**Physical name**</span></span><br><span data-ttu-id="d7651-113">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="d7651-113">**_Type_**</span></span> | <span data-ttu-id="d7651-114">Izmantot</span><span class="sxs-lookup"><span data-stu-id="d7651-114">Use</span></span> | <span data-ttu-id="d7651-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d7651-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d7651-116">**Sertifikāta veida elementa ID**</span><span class="sxs-lookup"><span data-stu-id="d7651-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="d7651-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="d7651-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="d7651-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="d7651-118">*GUID*</span></span> | <span data-ttu-id="d7651-119">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="d7651-119">Read-only</span></span><br><span data-ttu-id="d7651-120">Obligāts</span><span class="sxs-lookup"><span data-stu-id="d7651-120">Required</span></span> 
<span data-ttu-id="d7651-121">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="d7651-121">System-generated</span></span> | <span data-ttu-id="d7651-122">Unikāls sertifikāta veida primārais identifikators.</span><span class="sxs-lookup"><span data-stu-id="d7651-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="d7651-123">**Sertifikāta veids**</span><span class="sxs-lookup"><span data-stu-id="d7651-123">**Certificate Type**</span></span><br><span data-ttu-id="d7651-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="d7651-124">mshr_certificatetype</span></span><br><span data-ttu-id="d7651-125">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="d7651-125">*String*</span></span> | <span data-ttu-id="d7651-126">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="d7651-126">Read/write</span></span><br><span data-ttu-id="d7651-127">Obligāts</span><span class="sxs-lookup"><span data-stu-id="d7651-127">Required</span></span> | <span data-ttu-id="d7651-128">Unikāls sertifikāta veida lietotājam lasāms identifikators.</span><span class="sxs-lookup"><span data-stu-id="d7651-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="d7651-129">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="d7651-129">**Description**</span></span><br><span data-ttu-id="d7651-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="d7651-130">mshr_description</span></span><br><span data-ttu-id="d7651-131">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="d7651-131">*String*</span></span> | <span data-ttu-id="d7651-132">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="d7651-132">Read/write</span></span><br><span data-ttu-id="d7651-133">Obligāts</span><span class="sxs-lookup"><span data-stu-id="d7651-133">Required</span></span> | <span data-ttu-id="d7651-134">Sertifikāta veida apraksts.</span><span class="sxs-lookup"><span data-stu-id="d7651-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="d7651-135">**Nepieciešama atjaunošana**</span><span class="sxs-lookup"><span data-stu-id="d7651-135">**Require Renewal**</span></span><br><span data-ttu-id="d7651-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="d7651-136">mshr_requirerenewal</span></span><br><span data-ttu-id="d7651-137">*mshr_noyes opciju kopa*</span><span class="sxs-lookup"><span data-stu-id="d7651-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="d7651-138">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="d7651-138">Read/write</span></span><br><span data-ttu-id="d7651-139">Neobligāti</span><span class="sxs-lookup"><span data-stu-id="d7651-139">Optional</span></span> | <span data-ttu-id="d7651-140">Norāda, vai sertifikātam ir nepieciešama atjaunošana.</span><span class="sxs-lookup"><span data-stu-id="d7651-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d7651-141">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="d7651-141">See also</span></span>

[<span data-ttu-id="d7651-142">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="d7651-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="d7651-143">Piemērs Kandidāta vaicājumam par nolīgšanu</span><span class="sxs-lookup"><span data-stu-id="d7651-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]