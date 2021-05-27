---
title: Algas detalizēta informācija Pozīcijām
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Algas informācijai elementam Pozīcijas programmā Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019326"
---
# <a name="payroll-position"></a><span data-ttu-id="6feef-103">Algas pozīcija</span><span class="sxs-lookup"><span data-stu-id="6feef-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6feef-104">Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Algas informācijai elementam Pozīcijas programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6feef-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="6feef-105">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="6feef-105">Properties</span></span>

| <span data-ttu-id="6feef-106">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="6feef-106">Property</span></span><br><span data-ttu-id="6feef-107">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="6feef-107">**Physical name**</span></span><br><span data-ttu-id="6feef-108">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="6feef-108">**_Type_**</span></span> | <span data-ttu-id="6feef-109">Izmantot</span><span class="sxs-lookup"><span data-stu-id="6feef-109">Use</span></span> | <span data-ttu-id="6feef-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6feef-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6feef-111">**Ikgadējas regulāras stundas**</span><span class="sxs-lookup"><span data-stu-id="6feef-111">**Annual regular hours**</span></span><br><span data-ttu-id="6feef-112">Ikgadējās regulārās stundas</span><span class="sxs-lookup"><span data-stu-id="6feef-112">annualregularhours</span></span><br><span data-ttu-id="6feef-113">*Decimāldaļskaitlis*</span><span class="sxs-lookup"><span data-stu-id="6feef-113">*Decimal*</span></span> | <span data-ttu-id="6feef-114">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="6feef-114">Read-only</span></span><br><span data-ttu-id="6feef-115">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6feef-115">Required</span></span> | <span data-ttu-id="6feef-116">Ikgadējās regulārās stundas, kas definētas šajā pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="6feef-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="6feef-117">**Algas pozīcijas detalizētas informācijas elementa ID**</span><span class="sxs-lookup"><span data-stu-id="6feef-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="6feef-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="6feef-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="6feef-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="6feef-119">*Guid*</span></span> | <span data-ttu-id="6feef-120">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6feef-120">Required</span></span><br><span data-ttu-id="6feef-121">Sistēmas ģenerēts.</span><span class="sxs-lookup"><span data-stu-id="6feef-121">System generated.</span></span> | <span data-ttu-id="6feef-122">Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu pozīciju.</span><span class="sxs-lookup"><span data-stu-id="6feef-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="6feef-123">**Primārais lauks**</span><span class="sxs-lookup"><span data-stu-id="6feef-123">**Primary field**</span></span><br><span data-ttu-id="6feef-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="6feef-124">mshr_primaryfield</span></span><br><span data-ttu-id="6feef-125">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="6feef-125">*String*</span></span> | <span data-ttu-id="6feef-126">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6feef-126">Required</span></span><br><span data-ttu-id="6feef-127">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="6feef-127">System generated</span></span> |  |
| <span data-ttu-id="6feef-128">**Pozīcijas darba ID vērtība**</span><span class="sxs-lookup"><span data-stu-id="6feef-128">**Position job ID value**</span></span><br><span data-ttu-id="6feef-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="6feef-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="6feef-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6feef-130">*GUID*</span></span> | <span data-ttu-id="6feef-131">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="6feef-131">Read-only</span></span><br><span data-ttu-id="6feef-132">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6feef-132">Required</span></span><br><span data-ttu-id="6feef-133">Ārējā atslēga:mshr_PayrollPositionJobEntity no mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="6feef-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="6feef-134">Darba ID, kas saistīts ar amatu.</span><span class="sxs-lookup"><span data-stu-id="6feef-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="6feef-135">**Fiksētās atlīdzības plāna ID vērtība**</span><span class="sxs-lookup"><span data-stu-id="6feef-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="6feef-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="6feef-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="6feef-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6feef-137">*GUID*</span></span> | <span data-ttu-id="6feef-138">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="6feef-138">Read-only</span></span><br><span data-ttu-id="6feef-139">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6feef-139">Required</span></span><br><span data-ttu-id="6feef-140">Ārējā atslēga: mshr_FixedCompPlan_id no mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="6feef-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="6feef-141">Fiksētās atlīdzības plāna ID, kas saistīts ar amatu.</span><span class="sxs-lookup"><span data-stu-id="6feef-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="6feef-142">**Apmaksas cikla ID**</span><span class="sxs-lookup"><span data-stu-id="6feef-142">**Pay cycle ID**</span></span><br><span data-ttu-id="6feef-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="6feef-143">mshr_primaryfield</span></span><br><span data-ttu-id="6feef-144">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="6feef-144">*String*</span></span> | <span data-ttu-id="6feef-145">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="6feef-145">Read-only</span></span><br><span data-ttu-id="6feef-146">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6feef-146">Required</span></span> | <span data-ttu-id="6feef-147">Pozīcijai definētais algas cikls.</span><span class="sxs-lookup"><span data-stu-id="6feef-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="6feef-148">**Apmaksātāja juridiskā persona**</span><span class="sxs-lookup"><span data-stu-id="6feef-148">**Paid by legal entity**</span></span><br><span data-ttu-id="6feef-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="6feef-149">paidbylegalentity</span></span><br><span data-ttu-id="6feef-150">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="6feef-150">*String*</span></span> | <span data-ttu-id="6feef-151">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="6feef-151">Read-only</span></span><br><span data-ttu-id="6feef-152">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6feef-152">Required</span></span> | <span data-ttu-id="6feef-153">Par maksājuma izsniegšanu atbildīgā pozīcijā definētā juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="6feef-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="6feef-154">**Amata ID**</span><span class="sxs-lookup"><span data-stu-id="6feef-154">**Position ID**</span></span><br><span data-ttu-id="6feef-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="6feef-155">mshr_positionid</span></span><br><span data-ttu-id="6feef-156">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="6feef-156">*String*</span></span> | <span data-ttu-id="6feef-157">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="6feef-157">Read-only</span></span><br><span data-ttu-id="6feef-158">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6feef-158">Required</span></span> | <span data-ttu-id="6feef-159">Pozīcijas ID.</span><span class="sxs-lookup"><span data-stu-id="6feef-159">The ID of the position.</span></span> |
| <span data-ttu-id="6feef-160">**Derīgs līdz**</span><span class="sxs-lookup"><span data-stu-id="6feef-160">**Valid to**</span></span><br><span data-ttu-id="6feef-161">derīgs līdz</span><span class="sxs-lookup"><span data-stu-id="6feef-161">validto</span></span><br><span data-ttu-id="6feef-162">*Datuma Laika Nobīde*</span><span class="sxs-lookup"><span data-stu-id="6feef-162">*Date Time Offset*</span></span> | <span data-ttu-id="6feef-163">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="6feef-163">Read-only</span></span><br><span data-ttu-id="6feef-164">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6feef-164">Required</span></span> |<span data-ttu-id="6feef-165">Datums, no kura ir derīga pozīcijas informācija.</span><span class="sxs-lookup"><span data-stu-id="6feef-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="6feef-166">**Derīgs no**</span><span class="sxs-lookup"><span data-stu-id="6feef-166">**Valid from**</span></span><br><span data-ttu-id="6feef-167">derīgs no</span><span class="sxs-lookup"><span data-stu-id="6feef-167">validfrom</span></span><br><span data-ttu-id="6feef-168">*Datuma Laika Nobīde*</span><span class="sxs-lookup"><span data-stu-id="6feef-168">*Date Time Offset*</span></span> | <span data-ttu-id="6feef-169">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="6feef-169">Read-only</span></span><br><span data-ttu-id="6feef-170">Obligāts</span><span class="sxs-lookup"><span data-stu-id="6feef-170">Required</span></span> |<span data-ttu-id="6feef-171">Datums, līdz kuram ir derīga pozīcijas informācija.</span><span class="sxs-lookup"><span data-stu-id="6feef-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="6feef-172">**Vaicājums**</span><span class="sxs-lookup"><span data-stu-id="6feef-172">**Query**</span></span>

<span data-ttu-id="6feef-173">**Pieprasīt**</span><span class="sxs-lookup"><span data-stu-id="6feef-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="6feef-174">**Atbilde**</span><span class="sxs-lookup"><span data-stu-id="6feef-174">**Response**</span></span>

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
