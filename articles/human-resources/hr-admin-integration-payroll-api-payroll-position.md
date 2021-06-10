---
title: Algas detalizēta informācija Pozīcijām
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Algas informācijai elementam Pozīcijas programmā Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056784"
---
# <a name="payroll-position"></a><span data-ttu-id="a9edd-103">Algas pozīcija</span><span class="sxs-lookup"><span data-stu-id="a9edd-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a9edd-104">Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Algas informācijai elementam Pozīcijas programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a9edd-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="a9edd-105">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="a9edd-105">Properties</span></span>

| <span data-ttu-id="a9edd-106">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="a9edd-106">Property</span></span><br><span data-ttu-id="a9edd-107">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="a9edd-107">**Physical name**</span></span><br><span data-ttu-id="a9edd-108">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="a9edd-108">**_Type_**</span></span> | <span data-ttu-id="a9edd-109">Izmantot</span><span class="sxs-lookup"><span data-stu-id="a9edd-109">Use</span></span> | <span data-ttu-id="a9edd-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a9edd-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a9edd-111">**Ikgadējas regulāras stundas**</span><span class="sxs-lookup"><span data-stu-id="a9edd-111">**Annual regular hours**</span></span><br><span data-ttu-id="a9edd-112">Ikgadējās regulārās stundas</span><span class="sxs-lookup"><span data-stu-id="a9edd-112">annualregularhours</span></span><br><span data-ttu-id="a9edd-113">*Decimāldaļskaitlis*</span><span class="sxs-lookup"><span data-stu-id="a9edd-113">*Decimal*</span></span> | <span data-ttu-id="a9edd-114">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a9edd-114">Read-only</span></span><br><span data-ttu-id="a9edd-115">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a9edd-115">Required</span></span> | <span data-ttu-id="a9edd-116">Ikgadējās regulārās stundas, kas definētas šajā pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="a9edd-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="a9edd-117">**Algas pozīcijas detalizētas informācijas elementa ID**</span><span class="sxs-lookup"><span data-stu-id="a9edd-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="a9edd-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="a9edd-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="a9edd-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="a9edd-119">*Guid*</span></span> | <span data-ttu-id="a9edd-120">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a9edd-120">Required</span></span><br><span data-ttu-id="a9edd-121">Sistēmas ģenerēts.</span><span class="sxs-lookup"><span data-stu-id="a9edd-121">System generated.</span></span> | <span data-ttu-id="a9edd-122">Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu pozīciju.</span><span class="sxs-lookup"><span data-stu-id="a9edd-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="a9edd-123">**Primārais lauks**</span><span class="sxs-lookup"><span data-stu-id="a9edd-123">**Primary field**</span></span><br><span data-ttu-id="a9edd-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="a9edd-124">mshr_primaryfield</span></span><br><span data-ttu-id="a9edd-125">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a9edd-125">*String*</span></span> | <span data-ttu-id="a9edd-126">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a9edd-126">Required</span></span><br><span data-ttu-id="a9edd-127">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="a9edd-127">System generated</span></span> |  |
| <span data-ttu-id="a9edd-128">**Pozīcijas darba ID vērtība**</span><span class="sxs-lookup"><span data-stu-id="a9edd-128">**Position job ID value**</span></span><br><span data-ttu-id="a9edd-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="a9edd-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="a9edd-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="a9edd-130">*GUID*</span></span> | <span data-ttu-id="a9edd-131">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a9edd-131">Read-only</span></span><br><span data-ttu-id="a9edd-132">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a9edd-132">Required</span></span><br><span data-ttu-id="a9edd-133">Ārējā atslēga:mshr_PayrollPositionJobEntity no mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="a9edd-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="a9edd-134">Darba ID, kas saistīts ar amatu.</span><span class="sxs-lookup"><span data-stu-id="a9edd-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="a9edd-135">**Fiksētās atlīdzības plāna ID vērtība**</span><span class="sxs-lookup"><span data-stu-id="a9edd-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="a9edd-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="a9edd-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="a9edd-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="a9edd-137">*GUID*</span></span> | <span data-ttu-id="a9edd-138">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a9edd-138">Read-only</span></span><br><span data-ttu-id="a9edd-139">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a9edd-139">Required</span></span><br><span data-ttu-id="a9edd-140">Ārējā atslēga: mshr_FixedCompPlan_id no mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="a9edd-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="a9edd-141">Fiksētās atlīdzības plāna ID, kas saistīts ar amatu.</span><span class="sxs-lookup"><span data-stu-id="a9edd-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="a9edd-142">**Apmaksas cikla ID**</span><span class="sxs-lookup"><span data-stu-id="a9edd-142">**Pay cycle ID**</span></span><br><span data-ttu-id="a9edd-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="a9edd-143">mshr_primaryfield</span></span><br><span data-ttu-id="a9edd-144">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a9edd-144">*String*</span></span> | <span data-ttu-id="a9edd-145">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a9edd-145">Read-only</span></span><br><span data-ttu-id="a9edd-146">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a9edd-146">Required</span></span> | <span data-ttu-id="a9edd-147">Pozīcijai definētais algas cikls.</span><span class="sxs-lookup"><span data-stu-id="a9edd-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="a9edd-148">**Apmaksātāja juridiskā persona**</span><span class="sxs-lookup"><span data-stu-id="a9edd-148">**Paid by legal entity**</span></span><br><span data-ttu-id="a9edd-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="a9edd-149">paidbylegalentity</span></span><br><span data-ttu-id="a9edd-150">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a9edd-150">*String*</span></span> | <span data-ttu-id="a9edd-151">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a9edd-151">Read-only</span></span><br><span data-ttu-id="a9edd-152">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a9edd-152">Required</span></span> | <span data-ttu-id="a9edd-153">Par maksājuma izsniegšanu atbildīgā pozīcijā definētā juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="a9edd-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="a9edd-154">**Amata ID**</span><span class="sxs-lookup"><span data-stu-id="a9edd-154">**Position ID**</span></span><br><span data-ttu-id="a9edd-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="a9edd-155">mshr_positionid</span></span><br><span data-ttu-id="a9edd-156">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a9edd-156">*String*</span></span> | <span data-ttu-id="a9edd-157">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a9edd-157">Read-only</span></span><br><span data-ttu-id="a9edd-158">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a9edd-158">Required</span></span> | <span data-ttu-id="a9edd-159">Pozīcijas ID.</span><span class="sxs-lookup"><span data-stu-id="a9edd-159">The ID of the position.</span></span> |
| <span data-ttu-id="a9edd-160">**Derīgs līdz**</span><span class="sxs-lookup"><span data-stu-id="a9edd-160">**Valid to**</span></span><br><span data-ttu-id="a9edd-161">derīgs līdz</span><span class="sxs-lookup"><span data-stu-id="a9edd-161">validto</span></span><br><span data-ttu-id="a9edd-162">*Datuma Laika Nobīde*</span><span class="sxs-lookup"><span data-stu-id="a9edd-162">*Date Time Offset*</span></span> | <span data-ttu-id="a9edd-163">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a9edd-163">Read-only</span></span><br><span data-ttu-id="a9edd-164">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a9edd-164">Required</span></span> |<span data-ttu-id="a9edd-165">Datums, no kura ir derīga pozīcijas informācija.</span><span class="sxs-lookup"><span data-stu-id="a9edd-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="a9edd-166">**Derīgs no**</span><span class="sxs-lookup"><span data-stu-id="a9edd-166">**Valid from**</span></span><br><span data-ttu-id="a9edd-167">derīgs no</span><span class="sxs-lookup"><span data-stu-id="a9edd-167">validfrom</span></span><br><span data-ttu-id="a9edd-168">*Datuma Laika Nobīde*</span><span class="sxs-lookup"><span data-stu-id="a9edd-168">*Date Time Offset*</span></span> | <span data-ttu-id="a9edd-169">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a9edd-169">Read-only</span></span><br><span data-ttu-id="a9edd-170">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a9edd-170">Required</span></span> |<span data-ttu-id="a9edd-171">Datums, līdz kuram ir derīga pozīcijas informācija.</span><span class="sxs-lookup"><span data-stu-id="a9edd-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="a9edd-172">**Vaicājums**</span><span class="sxs-lookup"><span data-stu-id="a9edd-172">**Query**</span></span>

<span data-ttu-id="a9edd-173">**Pieprasīt**</span><span class="sxs-lookup"><span data-stu-id="a9edd-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="a9edd-174">**Atbilde**</span><span class="sxs-lookup"><span data-stu-id="a9edd-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
