---
title: Izvērtēšanas tipi
description: Šajā tēmā aprakstīta Izvērtēšanas tipi entītija programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: 361f8c866abb9d34eb3e2be7ea42626e98e34779
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805134"
---
# <a name="screening-types"></a><span data-ttu-id="09565-103">Izvērtēšanas tipi</span><span class="sxs-lookup"><span data-stu-id="09565-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="09565-104">Šajā tēmā aprakstīta Izvērtēšanas tipi entītija programmai Dynamics 365 Human Resources .</span><span class="sxs-lookup"><span data-stu-id="09565-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="09565-105">Fiziskais nosaukums: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="09565-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="09565-106">Apraksts</span><span class="sxs-lookup"><span data-stu-id="09565-106">Description</span></span>

<span data-ttu-id="09565-107">Šis elements apraksta izvērtēšanas tipus, ko uzņēmums iestatījis pirms darbā pieņemšanas un notiekošajiem darbinieku izvērtēšanas procesiem.</span><span class="sxs-lookup"><span data-stu-id="09565-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="09565-108">JSON pārstāvība</span><span class="sxs-lookup"><span data-stu-id="09565-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="09565-109">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="09565-109">Properties</span></span>

| <span data-ttu-id="09565-110">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="09565-110">Property</span></span><br><span data-ttu-id="09565-111">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="09565-111">**Physical name**</span></span><br><span data-ttu-id="09565-112">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="09565-112">**_Type_**</span></span> | <span data-ttu-id="09565-113">Izmantot</span><span class="sxs-lookup"><span data-stu-id="09565-113">Use</span></span> | <span data-ttu-id="09565-114">Apraksts</span><span class="sxs-lookup"><span data-stu-id="09565-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="09565-115">**Izvērtēšanas veida elementa ID**</span><span class="sxs-lookup"><span data-stu-id="09565-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="09565-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="09565-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="09565-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="09565-117">*GUID*</span></span> | <span data-ttu-id="09565-118">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="09565-118">Read-only</span></span><br><span data-ttu-id="09565-119">Obligāts</span><span class="sxs-lookup"><span data-stu-id="09565-119">Required</span></span><br><span data-ttu-id="09565-120">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="09565-120">System-generated</span></span> | <span data-ttu-id="09565-121">Unikāls izvērtēšanas veida ieraksta primārais identifikators.</span><span class="sxs-lookup"><span data-stu-id="09565-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="09565-122">**Izvērtēšanas veida ID**</span><span class="sxs-lookup"><span data-stu-id="09565-122">**Screening Type ID**</span></span><br><span data-ttu-id="09565-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="09565-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="09565-124">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="09565-124">*String*</span></span> | <span data-ttu-id="09565-125">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="09565-125">Read/write</span></span><br><span data-ttu-id="09565-126">Obligāts</span><span class="sxs-lookup"><span data-stu-id="09565-126">Required</span></span> | <span data-ttu-id="09565-127">Lietotāja definēts unikāls izvērtēšanas veida primārais identifikators.</span><span class="sxs-lookup"><span data-stu-id="09565-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="09565-128">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="09565-128">**Description**</span></span><br><span data-ttu-id="09565-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="09565-129">mshr_description</span></span><br><span data-ttu-id="09565-130">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="09565-130">*String*</span></span> | <span data-ttu-id="09565-131">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="09565-131">Read/write</span></span><br><span data-ttu-id="09565-132">Obligāts</span><span class="sxs-lookup"><span data-stu-id="09565-132">Required</span></span> | <span data-ttu-id="09565-133">Izvērtēšanas veida apraksts.</span><span class="sxs-lookup"><span data-stu-id="09565-133">The description of the screening type.</span></span> |
| <span data-ttu-id="09565-134">**Biežuma vienība**</span><span class="sxs-lookup"><span data-stu-id="09565-134">**Frequency Unit**</span></span><br><span data-ttu-id="09565-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="09565-135">mshr_frequencyunit</span></span><br><span data-ttu-id="09565-136">*mshr_hcmfrequencyunit opciju kopa*</span><span class="sxs-lookup"><span data-stu-id="09565-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="09565-137">Lasīt/rakstīt</span><span class="sxs-lookup"><span data-stu-id="09565-137">Read/write</span></span><br><span data-ttu-id="09565-138">Obligāts</span><span class="sxs-lookup"><span data-stu-id="09565-138">Required</span></span> | <span data-ttu-id="09565-139">Apraksta, cik bieži izvērtēšana jāveic nozīmētai personai.</span><span class="sxs-lookup"><span data-stu-id="09565-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="09565-140">**Ģenerēt no**</span><span class="sxs-lookup"><span data-stu-id="09565-140">**Generate From**</span></span><br><span data-ttu-id="09565-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="09565-141">mshr_generatefrom</span></span><br><span data-ttu-id="09565-142">*mshr_hcmfrequencygeneratefrom opciju kopa*</span><span class="sxs-lookup"><span data-stu-id="09565-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="09565-143">Lasīt-rakstīt</span><span class="sxs-lookup"><span data-stu-id="09565-143">Read-write</span></span><br><span data-ttu-id="09565-144">Obligāts</span><span class="sxs-lookup"><span data-stu-id="09565-144">Required</span></span> | <span data-ttu-id="09565-145">Ja Biežuma vērtība ir jebkura vērtība, kas nav "Tikai vienu reizi", vērtība GenerateFrom nosaka datumu, no kura aprēķināt nākamo izvērtēšanas notikumu.</span><span class="sxs-lookup"><span data-stu-id="09565-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="09565-146">**Biežuma intervāls**</span><span class="sxs-lookup"><span data-stu-id="09565-146">**Frequency Interval**</span></span><br><span data-ttu-id="09565-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="09565-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="09565-148">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="09565-148">*Integer*</span></span> | <span data-ttu-id="09565-149">Lasīt-rakstīt</span><span class="sxs-lookup"><span data-stu-id="09565-149">Read-write</span></span><br><span data-ttu-id="09565-150">Obligāts</span><span class="sxs-lookup"><span data-stu-id="09565-150">Required</span></span> | <span data-ttu-id="09565-151">Ja biežuma vērtība ir jebkura vērtība, kas nav "Tikai vienu reizi", jums ir jādefinē laika vienību intervāls starp katru izvērtēšanas notikumu.</span><span class="sxs-lookup"><span data-stu-id="09565-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="09565-152">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="09565-152">See also</span></span>

[<span data-ttu-id="09565-153">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="09565-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="09565-154">Piemērs Kandidāta vaicājumam par nolīgšanu</span><span class="sxs-lookup"><span data-stu-id="09565-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]