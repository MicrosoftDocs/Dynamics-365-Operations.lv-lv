---
title: Izvērtēšanas tipi
description: Šajā tēmā aprakstīta Izvērtēšanas tipi entītija programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126174"
---
# <a name="screening-types"></a><span data-ttu-id="cc929-103">Izvērtēšanas tipi</span><span class="sxs-lookup"><span data-stu-id="cc929-103">Screening types</span></span>

<span data-ttu-id="cc929-104">Šajā tēmā aprakstīta Izvērtēšanas tipi entītija programmai Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="cc929-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="cc929-105">Fiziskais nosaukums: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="cc929-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="cc929-106">Apraksts</span><span class="sxs-lookup"><span data-stu-id="cc929-106">Description</span></span>

<span data-ttu-id="cc929-107">Šis elements apraksta izvērtēšanas tipus, ko uzņēmums iestatījis pirms darbā pieņemšanas un notiekošajiem darbinieku izvērtēšanas procesiem.</span><span class="sxs-lookup"><span data-stu-id="cc929-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="cc929-108">JSON pārstāvība</span><span class="sxs-lookup"><span data-stu-id="cc929-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="cc929-109">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="cc929-109">Properties</span></span>

| <span data-ttu-id="cc929-110">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="cc929-110">Property</span></span><br><span data-ttu-id="cc929-111">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="cc929-111">**Physical name**</span></span><br><span data-ttu-id="cc929-112">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="cc929-112">**_Type_**</span></span> | <span data-ttu-id="cc929-113">Izmantot</span><span class="sxs-lookup"><span data-stu-id="cc929-113">Use</span></span> | <span data-ttu-id="cc929-114">Apraksts</span><span class="sxs-lookup"><span data-stu-id="cc929-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cc929-115">**Izvērtēšanas veida elementa ID**</span><span class="sxs-lookup"><span data-stu-id="cc929-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="cc929-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="cc929-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="cc929-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="cc929-117">*GUID*</span></span> | <span data-ttu-id="cc929-118">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="cc929-118">Read-only</span></span><br><span data-ttu-id="cc929-119">Obligāts</span><span class="sxs-lookup"><span data-stu-id="cc929-119">Required</span></span><br><span data-ttu-id="cc929-120">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="cc929-120">System-generated</span></span> | <span data-ttu-id="cc929-121">Unikāls izvērtēšanas veida ieraksta primārais identifikators.</span><span class="sxs-lookup"><span data-stu-id="cc929-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="cc929-122">**Izvērtēšanas veida ID**</span><span class="sxs-lookup"><span data-stu-id="cc929-122">**Screening Type ID**</span></span><br><span data-ttu-id="cc929-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="cc929-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="cc929-124">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="cc929-124">*String*</span></span> | <span data-ttu-id="cc929-125">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="cc929-125">Read/write</span></span><br><span data-ttu-id="cc929-126">Obligāts</span><span class="sxs-lookup"><span data-stu-id="cc929-126">Required</span></span> | <span data-ttu-id="cc929-127">Lietotāja definēts unikāls izvērtēšanas veida primārais identifikators.</span><span class="sxs-lookup"><span data-stu-id="cc929-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="cc929-128">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="cc929-128">**Description**</span></span><br><span data-ttu-id="cc929-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="cc929-129">mshr_description</span></span><br><span data-ttu-id="cc929-130">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="cc929-130">*String*</span></span> | <span data-ttu-id="cc929-131">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="cc929-131">Read/write</span></span><br><span data-ttu-id="cc929-132">Obligāts</span><span class="sxs-lookup"><span data-stu-id="cc929-132">Required</span></span> | <span data-ttu-id="cc929-133">Izvērtēšanas veida apraksts.</span><span class="sxs-lookup"><span data-stu-id="cc929-133">The description of the screening type.</span></span> |
| <span data-ttu-id="cc929-134">**Biežuma vienība**</span><span class="sxs-lookup"><span data-stu-id="cc929-134">**Frequency Unit**</span></span><br><span data-ttu-id="cc929-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="cc929-135">mshr_frequencyunit</span></span><br><span data-ttu-id="cc929-136">*mshr_hcmfrequencyunit opciju kopa*</span><span class="sxs-lookup"><span data-stu-id="cc929-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="cc929-137">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="cc929-137">Read/write</span></span><br><span data-ttu-id="cc929-138">Obligāts</span><span class="sxs-lookup"><span data-stu-id="cc929-138">Required</span></span> | <span data-ttu-id="cc929-139">Apraksta, cik bieži izvērtēšana jāveic nozīmētai personai.</span><span class="sxs-lookup"><span data-stu-id="cc929-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="cc929-140">**Ģenerēt no**</span><span class="sxs-lookup"><span data-stu-id="cc929-140">**Generate From**</span></span><br><span data-ttu-id="cc929-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="cc929-141">mshr_generatefrom</span></span><br><span data-ttu-id="cc929-142">*mshr_hcmfrequencygeneratefrom opciju kopa*</span><span class="sxs-lookup"><span data-stu-id="cc929-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="cc929-143">Lasīt-rakstīt</span><span class="sxs-lookup"><span data-stu-id="cc929-143">Read-write</span></span><br><span data-ttu-id="cc929-144">Obligāts</span><span class="sxs-lookup"><span data-stu-id="cc929-144">Required</span></span> | <span data-ttu-id="cc929-145">Ja Biežuma vērtība ir jebkura vērtība, kas nav "Tikai vienu reizi", vērtība GenerateFrom nosaka datumu, no kura aprēķināt nākamo izvērtēšanas notikumu.</span><span class="sxs-lookup"><span data-stu-id="cc929-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="cc929-146">**Biežuma intervāls**</span><span class="sxs-lookup"><span data-stu-id="cc929-146">**Frequency Interval**</span></span><br><span data-ttu-id="cc929-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="cc929-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="cc929-148">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="cc929-148">*Integer*</span></span> | <span data-ttu-id="cc929-149">Lasīt-rakstīt</span><span class="sxs-lookup"><span data-stu-id="cc929-149">Read-write</span></span><br><span data-ttu-id="cc929-150">Obligāts</span><span class="sxs-lookup"><span data-stu-id="cc929-150">Required</span></span> | <span data-ttu-id="cc929-151">Ja biežuma vērtība ir jebkura vērtība, kas nav "Tikai vienu reizi", jums ir jādefinē laika vienību intervāls starp katru izvērtēšanas notikumu.</span><span class="sxs-lookup"><span data-stu-id="cc929-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="cc929-152">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="cc929-152">See also</span></span>

[<span data-ttu-id="cc929-153">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="cc929-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="cc929-154">Piemērs Kandidāta vaicājumam par nolīgšanu</span><span class="sxs-lookup"><span data-stu-id="cc929-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
