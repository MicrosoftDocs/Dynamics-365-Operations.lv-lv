---
title: Algas nodarbinātā adrese
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Algas nodarbinātā adreses elementam programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882030"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="516fc-103">Algas nodarbinātā adrese</span><span class="sxs-lookup"><span data-stu-id="516fc-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="516fc-104">Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Algas nodarbinātā adreses elementam programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="516fc-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="516fc-105">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="516fc-105">Properties</span></span>

| <span data-ttu-id="516fc-106">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="516fc-106">Property</span></span><br><span data-ttu-id="516fc-107">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="516fc-107">**Physical name**</span></span><br><span data-ttu-id="516fc-108">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="516fc-108">**_Type_**</span></span> | <span data-ttu-id="516fc-109">Izmantot</span><span class="sxs-lookup"><span data-stu-id="516fc-109">Use</span></span> | <span data-ttu-id="516fc-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="516fc-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="516fc-111">**Pilsēta**</span><span class="sxs-lookup"><span data-stu-id="516fc-111">**City**</span></span><br><span data-ttu-id="516fc-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="516fc-112">mshr_city</span></span><br><span data-ttu-id="516fc-113">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="516fc-113">*String*</span></span> | <span data-ttu-id="516fc-114">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="516fc-114">Read-only</span></span><br><span data-ttu-id="516fc-115">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-115">Required</span></span> | <span data-ttu-id="516fc-116">Adresei definētā pilsēta.</span><span class="sxs-lookup"><span data-stu-id="516fc-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="516fc-117">**Darbinieku skaits**</span><span class="sxs-lookup"><span data-stu-id="516fc-117">**Personnel number**</span></span><br><span data-ttu-id="516fc-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="516fc-118">mshr_personnelnumber</span></span><br><span data-ttu-id="516fc-119">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="516fc-119">*String*</span></span> | <span data-ttu-id="516fc-120">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="516fc-120">Read-only</span></span><br><span data-ttu-id="516fc-121">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-121">Required</span></span> | <span data-ttu-id="516fc-122">Darbinieka unikālais personāla numurs.</span><span class="sxs-lookup"><span data-stu-id="516fc-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="516fc-123">**Valsts reģions**</span><span class="sxs-lookup"><span data-stu-id="516fc-123">**Country region**</span></span><br><span data-ttu-id="516fc-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="516fc-124">mshr_countryregionid</span></span><br><span data-ttu-id="516fc-125">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="516fc-125">*String*</span></span> | <span data-ttu-id="516fc-126">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="516fc-126">Read-only</span></span><br><span data-ttu-id="516fc-127">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-127">Required</span></span> | <span data-ttu-id="516fc-128">Adresei definētais valsts reģions</span><span class="sxs-lookup"><span data-stu-id="516fc-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="516fc-129">**Derīgs no**</span><span class="sxs-lookup"><span data-stu-id="516fc-129">**Valid from**</span></span><br><span data-ttu-id="516fc-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="516fc-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="516fc-131">*Datuma Laika Nobīde*</span><span class="sxs-lookup"><span data-stu-id="516fc-131">*Date Time Offset*</span></span> | <span data-ttu-id="516fc-132">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="516fc-132">Read-only</span></span> <br><span data-ttu-id="516fc-133">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-133">Required</span></span> | <span data-ttu-id="516fc-134">Datums, no kura adrese ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="516fc-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="516fc-135">**Darba adrese**</span><span class="sxs-lookup"><span data-stu-id="516fc-135">**Worked in address**</span></span><br><span data-ttu-id="516fc-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="516fc-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="516fc-137">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="516fc-137">Read-only</span></span><br><span data-ttu-id="516fc-138">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-138">Required</span></span> | <span data-ttu-id="516fc-139">Norāda, vai šī adrese ir darbinieka darba adrese.</span><span class="sxs-lookup"><span data-stu-id="516fc-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="516fc-140">**Pagasts**</span><span class="sxs-lookup"><span data-stu-id="516fc-140">**County**</span></span><br><span data-ttu-id="516fc-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="516fc-141">mshr_county</span></span><br><span data-ttu-id="516fc-142">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="516fc-142">*String*</span></span> | <span data-ttu-id="516fc-143">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="516fc-143">Read-only</span></span><br><span data-ttu-id="516fc-144">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-144">Required</span></span> | <span data-ttu-id="516fc-145">Adresei definētā valsts.</span><span class="sxs-lookup"><span data-stu-id="516fc-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="516fc-146">**Algas nodarbinātā adreses ID**</span><span class="sxs-lookup"><span data-stu-id="516fc-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="516fc-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="516fc-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="516fc-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="516fc-148">*GUID*</span></span> | <span data-ttu-id="516fc-149">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-149">Required</span></span><br><span data-ttu-id="516fc-150">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="516fc-150">System generated</span></span> | <span data-ttu-id="516fc-151">Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu adresi.</span><span class="sxs-lookup"><span data-stu-id="516fc-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="516fc-152">**Primārais lauks**</span><span class="sxs-lookup"><span data-stu-id="516fc-152">**Primary field**</span></span><br><span data-ttu-id="516fc-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="516fc-153">mshr_primaryfield</span></span><br><span data-ttu-id="516fc-154">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="516fc-154">*String*</span></span> | <span data-ttu-id="516fc-155">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="516fc-155">Read-only</span></span><br><span data-ttu-id="516fc-156">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-156">Required</span></span> |  |
| <span data-ttu-id="516fc-157">**Iela**</span><span class="sxs-lookup"><span data-stu-id="516fc-157">**Street**</span></span><br><span data-ttu-id="516fc-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="516fc-158">mshr_street</span></span><br><span data-ttu-id="516fc-159">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="516fc-159">*String*</span></span> | <span data-ttu-id="516fc-160">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="516fc-160">Read-only</span></span><br><span data-ttu-id="516fc-161">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-161">Required</span></span> | <span data-ttu-id="516fc-162">Adresei definētā iela.</span><span class="sxs-lookup"><span data-stu-id="516fc-162">The street defined for the address.</span></span> |
| <span data-ttu-id="516fc-163">**Derīgs līdz**</span><span class="sxs-lookup"><span data-stu-id="516fc-163">**Valid to**</span></span><br><span data-ttu-id="516fc-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="516fc-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="516fc-165">*Datuma Laika Nobīde*</span><span class="sxs-lookup"><span data-stu-id="516fc-165">*Date Time Offset*</span></span> | <span data-ttu-id="516fc-166">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="516fc-166">Read-only</span></span> <br><span data-ttu-id="516fc-167">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-167">Required</span></span> | <span data-ttu-id="516fc-168">Datums, līdz kuram adrese ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="516fc-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="516fc-169">**Atrašanās vietas ID**</span><span class="sxs-lookup"><span data-stu-id="516fc-169">**Location ID**</span></span><br><span data-ttu-id="516fc-170">mshr_locationidbr>*Virkne*</span><span class="sxs-lookup"><span data-stu-id="516fc-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="516fc-171">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="516fc-171">Read-only</span></span> <br><span data-ttu-id="516fc-172">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-172">Required</span></span> | <span data-ttu-id="516fc-173">Adreses ID.</span><span class="sxs-lookup"><span data-stu-id="516fc-173">The ID for the address.</span></span>  |
| <span data-ttu-id="516fc-174">**Pasta indekss**</span><span class="sxs-lookup"><span data-stu-id="516fc-174">**Postal code**</span></span><br><span data-ttu-id="516fc-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="516fc-175">mshr_zipcode</span></span><br><span data-ttu-id="516fc-176">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="516fc-176">*String*</span></span> | <span data-ttu-id="516fc-177">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="516fc-177">Read-only</span></span> <br><span data-ttu-id="516fc-178">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-178">Required</span></span> |<span data-ttu-id="516fc-179">Darbiniekam definētais identifikācijas numurs.</span><span class="sxs-lookup"><span data-stu-id="516fc-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="516fc-180">**Dzīves vieta**</span><span class="sxs-lookup"><span data-stu-id="516fc-180">**Lived in address**</span></span><br><span data-ttu-id="516fc-181">mshr_islivedinaddressbr>*Virkne*</span><span class="sxs-lookup"><span data-stu-id="516fc-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="516fc-182">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="516fc-182">Read-only</span></span><br><span data-ttu-id="516fc-183">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-183">Required</span></span> | <span data-ttu-id="516fc-184">Norāda, vai šī adrese ir darbinieka dzīves vieta.</span><span class="sxs-lookup"><span data-stu-id="516fc-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="516fc-185">**Novads**</span><span class="sxs-lookup"><span data-stu-id="516fc-185">**State**</span></span><br><span data-ttu-id="516fc-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="516fc-186">mshr_state</span></span><br><span data-ttu-id="516fc-187">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="516fc-187">*String*</span></span> | <span data-ttu-id="516fc-188">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="516fc-188">Read-only</span></span><br><span data-ttu-id="516fc-189">Obligāts</span><span class="sxs-lookup"><span data-stu-id="516fc-189">Required</span></span> | <span data-ttu-id="516fc-190">Adresei definēts štats.</span><span class="sxs-lookup"><span data-stu-id="516fc-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="516fc-191">Piemēra vaicājums</span><span class="sxs-lookup"><span data-stu-id="516fc-191">Example query</span></span>

<span data-ttu-id="516fc-192">**Pieprasīt**</span><span class="sxs-lookup"><span data-stu-id="516fc-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="516fc-193">**Atbilde**</span><span class="sxs-lookup"><span data-stu-id="516fc-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
