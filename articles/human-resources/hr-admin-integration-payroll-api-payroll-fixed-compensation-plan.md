---
title: Algu aprēķina fiksētās atlīdzības plāns
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Payroll fiksētā atlīdzības plāna elementam programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021300"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="95200-103">Algu aprēķina fiksētās atlīdzības plāns</span><span class="sxs-lookup"><span data-stu-id="95200-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="95200-104">Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Payroll fiksētā atlīdzības plāna elementam programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="95200-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="95200-105">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="95200-105">Properties</span></span>

| <span data-ttu-id="95200-106">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="95200-106">Property</span></span><br><span data-ttu-id="95200-107">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="95200-107">**Physical name**</span></span><br><span data-ttu-id="95200-108">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="95200-108">**_Type_**</span></span> | <span data-ttu-id="95200-109">Izmantot</span><span class="sxs-lookup"><span data-stu-id="95200-109">Use</span></span> | <span data-ttu-id="95200-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="95200-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="95200-111">**Darbinieka ID**</span><span class="sxs-lookup"><span data-stu-id="95200-111">**Employee ID**</span></span><br><span data-ttu-id="95200-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="95200-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="95200-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="95200-113">*GUID*</span></span> | <span data-ttu-id="95200-114">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="95200-114">Read-only</span></span><br><span data-ttu-id="95200-115">Obligāts</span><span class="sxs-lookup"><span data-stu-id="95200-115">Required</span></span><br><span data-ttu-id="95200-116">Ārējā atslēga:mshr_Employee_id no mshr_payrollemployeeentity elementa</span><span class="sxs-lookup"><span data-stu-id="95200-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="95200-117">Darbinieka ID</span><span class="sxs-lookup"><span data-stu-id="95200-117">Employee ID</span></span> |
| <span data-ttu-id="95200-118">**Maksājuma kurss**</span><span class="sxs-lookup"><span data-stu-id="95200-118">**Pay rate**</span></span><br><span data-ttu-id="95200-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="95200-119">mshr_payrate</span></span><br><span data-ttu-id="95200-120">*Decimāldaļskaitlis*</span><span class="sxs-lookup"><span data-stu-id="95200-120">*Decimal*</span></span> | <span data-ttu-id="95200-121">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="95200-121">Read-only</span></span><br><span data-ttu-id="95200-122">Obligāts</span><span class="sxs-lookup"><span data-stu-id="95200-122">Required</span></span> | <span data-ttu-id="95200-123">Fiksētās atlīdzības plānā definētais algas kurss.</span><span class="sxs-lookup"><span data-stu-id="95200-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="95200-124">**Plāna ID**</span><span class="sxs-lookup"><span data-stu-id="95200-124">**Plan ID**</span></span><br><span data-ttu-id="95200-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="95200-125">mshr_planid</span></span><br><span data-ttu-id="95200-126">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="95200-126">*String*</span></span> | <span data-ttu-id="95200-127">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="95200-127">Read-only</span></span><br><span data-ttu-id="95200-128">Obligāts</span><span class="sxs-lookup"><span data-stu-id="95200-128">Required</span></span> |<span data-ttu-id="95200-129">Norāda atlīdzības plānu.</span><span class="sxs-lookup"><span data-stu-id="95200-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="95200-130">**Derīgs no**</span><span class="sxs-lookup"><span data-stu-id="95200-130">**Valid from**</span></span><br><span data-ttu-id="95200-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="95200-131">mshr_validfrom</span></span><br><span data-ttu-id="95200-132">*Datuma Laika Nobīde*</span><span class="sxs-lookup"><span data-stu-id="95200-132">*Date Time Offset*</span></span> |  <span data-ttu-id="95200-133">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="95200-133">Read-only</span></span><br><span data-ttu-id="95200-134">Obligāts</span><span class="sxs-lookup"><span data-stu-id="95200-134">Required</span></span> |<span data-ttu-id="95200-135">Datums, no kura ir fiksētā atlīdzība par darbinieku.</span><span class="sxs-lookup"><span data-stu-id="95200-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="95200-136">**Elements Algu aprēķina fiksētās atlīdzības plāns**</span><span class="sxs-lookup"><span data-stu-id="95200-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="95200-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="95200-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="95200-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="95200-138">*GUID*</span></span> | <span data-ttu-id="95200-139">Obligāts</span><span class="sxs-lookup"><span data-stu-id="95200-139">Required</span></span><br><span data-ttu-id="95200-140">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="95200-140">Sytem generated</span></span> | <span data-ttu-id="95200-141">Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu atlīdzības plānu.</span><span class="sxs-lookup"><span data-stu-id="95200-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="95200-142">**Algas izmaksas biežums**</span><span class="sxs-lookup"><span data-stu-id="95200-142">**Pay frequency**</span></span><br><span data-ttu-id="95200-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="95200-143">mshr_payfrequency</span></span><br><span data-ttu-id="95200-144">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="95200-144">*String*</span></span> | <span data-ttu-id="95200-145">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="95200-145">Read-only</span></span><br><span data-ttu-id="95200-146">Obligāts</span><span class="sxs-lookup"><span data-stu-id="95200-146">Required</span></span> |<span data-ttu-id="95200-147">Darbinieka apmaksas biežums.</span><span class="sxs-lookup"><span data-stu-id="95200-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="95200-148">**Derīgs līdz**</span><span class="sxs-lookup"><span data-stu-id="95200-148">**Valid to**</span></span><br><span data-ttu-id="95200-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="95200-149">mshr_validto</span></span><br><span data-ttu-id="95200-150">*Datuma Laika Nobīde*</span><span class="sxs-lookup"><span data-stu-id="95200-150">*Date Time Offset*</span></span> | <span data-ttu-id="95200-151">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="95200-151">Read-only</span></span> <br><span data-ttu-id="95200-152">Obligāts</span><span class="sxs-lookup"><span data-stu-id="95200-152">Required</span></span> | <span data-ttu-id="95200-153">Datums, līdz kuram ir fiksētā atlīdzība par darbinieku.</span><span class="sxs-lookup"><span data-stu-id="95200-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="95200-154">**Amata ID**</span><span class="sxs-lookup"><span data-stu-id="95200-154">**Position ID**</span></span><br><span data-ttu-id="95200-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="95200-155">mshr_positionid</span></span><br><span data-ttu-id="95200-156">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="95200-156">*String*</span></span> | <span data-ttu-id="95200-157">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="95200-157">Read-only</span></span> <br><span data-ttu-id="95200-158">Obligāts</span><span class="sxs-lookup"><span data-stu-id="95200-158">Required</span></span> | <span data-ttu-id="95200-159">Amata ID, kas saistīts ar darbinieka un fiksētās atlīdzības plāna reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="95200-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="95200-160">**Valūta**</span><span class="sxs-lookup"><span data-stu-id="95200-160">**Currency**</span></span><br><span data-ttu-id="95200-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="95200-161">mshr_currency</span></span><br><span data-ttu-id="95200-162">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="95200-162">*String*</span></span> | <span data-ttu-id="95200-163">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="95200-163">Read-only</span></span> <br><span data-ttu-id="95200-164">Obligāts</span><span class="sxs-lookup"><span data-stu-id="95200-164">Required</span></span> |<span data-ttu-id="95200-165">Fiksētās atlīdzības plānam definētā valūta</span><span class="sxs-lookup"><span data-stu-id="95200-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="95200-166">**Darbinieku skaits**</span><span class="sxs-lookup"><span data-stu-id="95200-166">**Personnel number**</span></span><br><span data-ttu-id="95200-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="95200-167">mshr_personnelnumber</span></span><br><span data-ttu-id="95200-168">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="95200-168">*String*</span></span> | <span data-ttu-id="95200-169">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="95200-169">Read-only</span></span><br><span data-ttu-id="95200-170">Obligāts</span><span class="sxs-lookup"><span data-stu-id="95200-170">Required</span></span> |<span data-ttu-id="95200-171">Darbinieka unikālais personāla numurs.</span><span class="sxs-lookup"><span data-stu-id="95200-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="95200-172">**Vaicājums**</span><span class="sxs-lookup"><span data-stu-id="95200-172">**Query**</span></span>

<span data-ttu-id="95200-173">**Pieprasīt**</span><span class="sxs-lookup"><span data-stu-id="95200-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="95200-174">**Atbilde**</span><span class="sxs-lookup"><span data-stu-id="95200-174">**Response**</span></span>

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
