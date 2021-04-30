---
title: Algu aprēķina fiksētās atlīdzības plāns
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Payroll fiksētā atlīdzības plāna elementam programmā Dynamics 365 Human Resources.
author: jcart
manager: tfehr
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
ms.openlocfilehash: 78a274cc491041d3d917a50bfb433f667cd8c255
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882033"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="1a2e5-103">Algu aprēķina fiksētās atlīdzības plāns</span><span class="sxs-lookup"><span data-stu-id="1a2e5-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1a2e5-104">Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Payroll fiksētā atlīdzības plāna elementam programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1a2e5-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="1a2e5-105">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="1a2e5-105">Properties</span></span>

| <span data-ttu-id="1a2e5-106">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="1a2e5-106">Property</span></span><br><span data-ttu-id="1a2e5-107">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-107">**Physical name**</span></span><br><span data-ttu-id="1a2e5-108">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-108">**_Type_**</span></span> | <span data-ttu-id="1a2e5-109">Izmantot</span><span class="sxs-lookup"><span data-stu-id="1a2e5-109">Use</span></span> | <span data-ttu-id="1a2e5-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1a2e5-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1a2e5-111">**Darbinieka ID**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-111">**Employee ID**</span></span><br><span data-ttu-id="1a2e5-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="1a2e5-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="1a2e5-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="1a2e5-113">*GUID*</span></span> | <span data-ttu-id="1a2e5-114">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="1a2e5-114">Read-only</span></span><br><span data-ttu-id="1a2e5-115">Obligāts</span><span class="sxs-lookup"><span data-stu-id="1a2e5-115">Required</span></span><br><span data-ttu-id="1a2e5-116">Ārējā atslēga:mshr_Employee_id no mshr_payrollemployeeentity elementa</span><span class="sxs-lookup"><span data-stu-id="1a2e5-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="1a2e5-117">Darbinieka ID</span><span class="sxs-lookup"><span data-stu-id="1a2e5-117">Employee ID</span></span> |
| <span data-ttu-id="1a2e5-118">**Maksājuma kurss**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-118">**Pay rate**</span></span><br><span data-ttu-id="1a2e5-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="1a2e5-119">mshr_payrate</span></span><br><span data-ttu-id="1a2e5-120">*Decimāldaļskaitlis*</span><span class="sxs-lookup"><span data-stu-id="1a2e5-120">*Decimal*</span></span> | <span data-ttu-id="1a2e5-121">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="1a2e5-121">Read-only</span></span><br><span data-ttu-id="1a2e5-122">Obligāts</span><span class="sxs-lookup"><span data-stu-id="1a2e5-122">Required</span></span> | <span data-ttu-id="1a2e5-123">Fiksētās atlīdzības plānā definētais algas kurss.</span><span class="sxs-lookup"><span data-stu-id="1a2e5-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="1a2e5-124">**Plāna ID**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-124">**Plan ID**</span></span><br><span data-ttu-id="1a2e5-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="1a2e5-125">mshr_planid</span></span><br><span data-ttu-id="1a2e5-126">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="1a2e5-126">*String*</span></span> | <span data-ttu-id="1a2e5-127">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="1a2e5-127">Read-only</span></span><br><span data-ttu-id="1a2e5-128">Obligāts</span><span class="sxs-lookup"><span data-stu-id="1a2e5-128">Required</span></span> |<span data-ttu-id="1a2e5-129">Norāda atlīdzības plānu.</span><span class="sxs-lookup"><span data-stu-id="1a2e5-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="1a2e5-130">**Derīgs no**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-130">**Valid from**</span></span><br><span data-ttu-id="1a2e5-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="1a2e5-131">mshr_validfrom</span></span><br><span data-ttu-id="1a2e5-132">*Datuma Laika Nobīde*</span><span class="sxs-lookup"><span data-stu-id="1a2e5-132">*Date Time Offset*</span></span> |  <span data-ttu-id="1a2e5-133">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="1a2e5-133">Read-only</span></span><br><span data-ttu-id="1a2e5-134">Obligāts</span><span class="sxs-lookup"><span data-stu-id="1a2e5-134">Required</span></span> |<span data-ttu-id="1a2e5-135">Datums, no kura ir fiksētā atlīdzība par darbinieku.</span><span class="sxs-lookup"><span data-stu-id="1a2e5-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="1a2e5-136">**Elements Algu aprēķina fiksētās atlīdzības plāns**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="1a2e5-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="1a2e5-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="1a2e5-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="1a2e5-138">*GUID*</span></span> | <span data-ttu-id="1a2e5-139">Obligāts</span><span class="sxs-lookup"><span data-stu-id="1a2e5-139">Required</span></span><br><span data-ttu-id="1a2e5-140">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="1a2e5-140">Sytem generated</span></span> | <span data-ttu-id="1a2e5-141">Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu atlīdzības plānu.</span><span class="sxs-lookup"><span data-stu-id="1a2e5-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="1a2e5-142">**Algas izmaksas biežums**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-142">**Pay frequency**</span></span><br><span data-ttu-id="1a2e5-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="1a2e5-143">mshr_payfrequency</span></span><br><span data-ttu-id="1a2e5-144">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="1a2e5-144">*String*</span></span> | <span data-ttu-id="1a2e5-145">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="1a2e5-145">Read-only</span></span><br><span data-ttu-id="1a2e5-146">Obligāts</span><span class="sxs-lookup"><span data-stu-id="1a2e5-146">Required</span></span> |<span data-ttu-id="1a2e5-147">Darbinieka apmaksas biežums.</span><span class="sxs-lookup"><span data-stu-id="1a2e5-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="1a2e5-148">**Derīgs līdz**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-148">**Valid to**</span></span><br><span data-ttu-id="1a2e5-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="1a2e5-149">mshr_validto</span></span><br><span data-ttu-id="1a2e5-150">*Datuma Laika Nobīde*</span><span class="sxs-lookup"><span data-stu-id="1a2e5-150">*Date Time Offset*</span></span> | <span data-ttu-id="1a2e5-151">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="1a2e5-151">Read-only</span></span> <br><span data-ttu-id="1a2e5-152">Obligāts</span><span class="sxs-lookup"><span data-stu-id="1a2e5-152">Required</span></span> | <span data-ttu-id="1a2e5-153">Datums, līdz kuram ir fiksētā atlīdzība par darbinieku.</span><span class="sxs-lookup"><span data-stu-id="1a2e5-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="1a2e5-154">**Amata ID**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-154">**Position ID**</span></span><br><span data-ttu-id="1a2e5-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="1a2e5-155">mshr_positionid</span></span><br><span data-ttu-id="1a2e5-156">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="1a2e5-156">*String*</span></span> | <span data-ttu-id="1a2e5-157">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="1a2e5-157">Read-only</span></span> <br><span data-ttu-id="1a2e5-158">Obligāts</span><span class="sxs-lookup"><span data-stu-id="1a2e5-158">Required</span></span> | <span data-ttu-id="1a2e5-159">Amata ID, kas saistīts ar darbinieka un fiksētās atlīdzības plāna reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="1a2e5-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="1a2e5-160">**Valūta**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-160">**Currency**</span></span><br><span data-ttu-id="1a2e5-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="1a2e5-161">mshr_currency</span></span><br><span data-ttu-id="1a2e5-162">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="1a2e5-162">*String*</span></span> | <span data-ttu-id="1a2e5-163">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="1a2e5-163">Read-only</span></span> <br><span data-ttu-id="1a2e5-164">Obligāts</span><span class="sxs-lookup"><span data-stu-id="1a2e5-164">Required</span></span> |<span data-ttu-id="1a2e5-165">Fiksētās atlīdzības plānam definētā valūta</span><span class="sxs-lookup"><span data-stu-id="1a2e5-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="1a2e5-166">**Darbinieku skaits**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-166">**Personnel number**</span></span><br><span data-ttu-id="1a2e5-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="1a2e5-167">mshr_personnelnumber</span></span><br><span data-ttu-id="1a2e5-168">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="1a2e5-168">*String*</span></span> | <span data-ttu-id="1a2e5-169">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="1a2e5-169">Read-only</span></span><br><span data-ttu-id="1a2e5-170">Obligāts</span><span class="sxs-lookup"><span data-stu-id="1a2e5-170">Required</span></span> |<span data-ttu-id="1a2e5-171">Darbinieka unikālais personāla numurs.</span><span class="sxs-lookup"><span data-stu-id="1a2e5-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="1a2e5-172">**Vaicājums**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-172">**Query**</span></span>

<span data-ttu-id="1a2e5-173">**Pieprasīt**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="1a2e5-174">**Atbilde**</span><span class="sxs-lookup"><span data-stu-id="1a2e5-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
