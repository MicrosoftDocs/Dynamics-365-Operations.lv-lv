---
title: Algas nodarbinātā adrese
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Algas nodarbinātā adreses elementam programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: 964f04261ea95ee6fa2880b0905a669855f6c58a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020709"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="a95da-103">Algas nodarbinātā adrese</span><span class="sxs-lookup"><span data-stu-id="a95da-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a95da-104">Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Algas nodarbinātā adreses elementam programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a95da-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="a95da-105">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="a95da-105">Properties</span></span>

| <span data-ttu-id="a95da-106">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="a95da-106">Property</span></span><br><span data-ttu-id="a95da-107">**Fiziskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="a95da-107">**Physical name**</span></span><br><span data-ttu-id="a95da-108">**_tips_**</span><span class="sxs-lookup"><span data-stu-id="a95da-108">**_Type_**</span></span> | <span data-ttu-id="a95da-109">Izmantot</span><span class="sxs-lookup"><span data-stu-id="a95da-109">Use</span></span> | <span data-ttu-id="a95da-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a95da-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a95da-111">**Pilsēta**</span><span class="sxs-lookup"><span data-stu-id="a95da-111">**City**</span></span><br><span data-ttu-id="a95da-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="a95da-112">mshr_city</span></span><br><span data-ttu-id="a95da-113">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a95da-113">*String*</span></span> | <span data-ttu-id="a95da-114">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a95da-114">Read-only</span></span><br><span data-ttu-id="a95da-115">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-115">Required</span></span> | <span data-ttu-id="a95da-116">Adresei definētā pilsēta.</span><span class="sxs-lookup"><span data-stu-id="a95da-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="a95da-117">**Darbinieku skaits**</span><span class="sxs-lookup"><span data-stu-id="a95da-117">**Personnel number**</span></span><br><span data-ttu-id="a95da-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="a95da-118">mshr_personnelnumber</span></span><br><span data-ttu-id="a95da-119">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a95da-119">*String*</span></span> | <span data-ttu-id="a95da-120">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a95da-120">Read-only</span></span><br><span data-ttu-id="a95da-121">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-121">Required</span></span> | <span data-ttu-id="a95da-122">Darbinieka unikālais personāla numurs.</span><span class="sxs-lookup"><span data-stu-id="a95da-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="a95da-123">**Valsts reģions**</span><span class="sxs-lookup"><span data-stu-id="a95da-123">**Country region**</span></span><br><span data-ttu-id="a95da-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="a95da-124">mshr_countryregionid</span></span><br><span data-ttu-id="a95da-125">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a95da-125">*String*</span></span> | <span data-ttu-id="a95da-126">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a95da-126">Read-only</span></span><br><span data-ttu-id="a95da-127">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-127">Required</span></span> | <span data-ttu-id="a95da-128">Adresei definētais valsts reģions</span><span class="sxs-lookup"><span data-stu-id="a95da-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="a95da-129">**Derīgs no**</span><span class="sxs-lookup"><span data-stu-id="a95da-129">**Valid from**</span></span><br><span data-ttu-id="a95da-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="a95da-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="a95da-131">*Datuma Laika Nobīde*</span><span class="sxs-lookup"><span data-stu-id="a95da-131">*Date Time Offset*</span></span> | <span data-ttu-id="a95da-132">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a95da-132">Read-only</span></span> <br><span data-ttu-id="a95da-133">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-133">Required</span></span> | <span data-ttu-id="a95da-134">Datums, no kura adrese ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="a95da-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="a95da-135">**Darba adrese**</span><span class="sxs-lookup"><span data-stu-id="a95da-135">**Worked in address**</span></span><br><span data-ttu-id="a95da-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="a95da-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="a95da-137">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a95da-137">Read-only</span></span><br><span data-ttu-id="a95da-138">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-138">Required</span></span> | <span data-ttu-id="a95da-139">Norāda, vai šī adrese ir darbinieka darba adrese.</span><span class="sxs-lookup"><span data-stu-id="a95da-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="a95da-140">**Pagasts**</span><span class="sxs-lookup"><span data-stu-id="a95da-140">**County**</span></span><br><span data-ttu-id="a95da-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="a95da-141">mshr_county</span></span><br><span data-ttu-id="a95da-142">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a95da-142">*String*</span></span> | <span data-ttu-id="a95da-143">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a95da-143">Read-only</span></span><br><span data-ttu-id="a95da-144">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-144">Required</span></span> | <span data-ttu-id="a95da-145">Adresei definētā valsts.</span><span class="sxs-lookup"><span data-stu-id="a95da-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="a95da-146">**Algas nodarbinātā adreses ID**</span><span class="sxs-lookup"><span data-stu-id="a95da-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="a95da-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="a95da-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="a95da-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="a95da-148">*GUID*</span></span> | <span data-ttu-id="a95da-149">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-149">Required</span></span><br><span data-ttu-id="a95da-150">Sistēmas ģenerēts</span><span class="sxs-lookup"><span data-stu-id="a95da-150">System generated</span></span> | <span data-ttu-id="a95da-151">Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu adresi.</span><span class="sxs-lookup"><span data-stu-id="a95da-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="a95da-152">**Primārais lauks**</span><span class="sxs-lookup"><span data-stu-id="a95da-152">**Primary field**</span></span><br><span data-ttu-id="a95da-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="a95da-153">mshr_primaryfield</span></span><br><span data-ttu-id="a95da-154">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a95da-154">*String*</span></span> | <span data-ttu-id="a95da-155">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a95da-155">Read-only</span></span><br><span data-ttu-id="a95da-156">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-156">Required</span></span> |  |
| <span data-ttu-id="a95da-157">**Iela**</span><span class="sxs-lookup"><span data-stu-id="a95da-157">**Street**</span></span><br><span data-ttu-id="a95da-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="a95da-158">mshr_street</span></span><br><span data-ttu-id="a95da-159">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a95da-159">*String*</span></span> | <span data-ttu-id="a95da-160">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a95da-160">Read-only</span></span><br><span data-ttu-id="a95da-161">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-161">Required</span></span> | <span data-ttu-id="a95da-162">Adresei definētā iela.</span><span class="sxs-lookup"><span data-stu-id="a95da-162">The street defined for the address.</span></span> |
| <span data-ttu-id="a95da-163">**Derīgs līdz**</span><span class="sxs-lookup"><span data-stu-id="a95da-163">**Valid to**</span></span><br><span data-ttu-id="a95da-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="a95da-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="a95da-165">*Datuma Laika Nobīde*</span><span class="sxs-lookup"><span data-stu-id="a95da-165">*Date Time Offset*</span></span> | <span data-ttu-id="a95da-166">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a95da-166">Read-only</span></span> <br><span data-ttu-id="a95da-167">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-167">Required</span></span> | <span data-ttu-id="a95da-168">Datums, līdz kuram adrese ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="a95da-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="a95da-169">**Atrašanās vietas ID**</span><span class="sxs-lookup"><span data-stu-id="a95da-169">**Location ID**</span></span><br><span data-ttu-id="a95da-170">mshr_locationidbr>*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a95da-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="a95da-171">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a95da-171">Read-only</span></span> <br><span data-ttu-id="a95da-172">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-172">Required</span></span> | <span data-ttu-id="a95da-173">Adreses ID.</span><span class="sxs-lookup"><span data-stu-id="a95da-173">The ID for the address.</span></span>  |
| <span data-ttu-id="a95da-174">**Pasta indekss**</span><span class="sxs-lookup"><span data-stu-id="a95da-174">**Postal code**</span></span><br><span data-ttu-id="a95da-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="a95da-175">mshr_zipcode</span></span><br><span data-ttu-id="a95da-176">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a95da-176">*String*</span></span> | <span data-ttu-id="a95da-177">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a95da-177">Read-only</span></span> <br><span data-ttu-id="a95da-178">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-178">Required</span></span> |<span data-ttu-id="a95da-179">Darbiniekam definētais identifikācijas numurs.</span><span class="sxs-lookup"><span data-stu-id="a95da-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="a95da-180">**Dzīves vieta**</span><span class="sxs-lookup"><span data-stu-id="a95da-180">**Lived in address**</span></span><br><span data-ttu-id="a95da-181">mshr_islivedinaddressbr>*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a95da-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="a95da-182">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a95da-182">Read-only</span></span><br><span data-ttu-id="a95da-183">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-183">Required</span></span> | <span data-ttu-id="a95da-184">Norāda, vai šī adrese ir darbinieka dzīves vieta.</span><span class="sxs-lookup"><span data-stu-id="a95da-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="a95da-185">**Novads**</span><span class="sxs-lookup"><span data-stu-id="a95da-185">**State**</span></span><br><span data-ttu-id="a95da-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="a95da-186">mshr_state</span></span><br><span data-ttu-id="a95da-187">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="a95da-187">*String*</span></span> | <span data-ttu-id="a95da-188">Tikai lasāms</span><span class="sxs-lookup"><span data-stu-id="a95da-188">Read-only</span></span><br><span data-ttu-id="a95da-189">Obligāts</span><span class="sxs-lookup"><span data-stu-id="a95da-189">Required</span></span> | <span data-ttu-id="a95da-190">Adresei definēts štats.</span><span class="sxs-lookup"><span data-stu-id="a95da-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="a95da-191">Piemēra vaicājums</span><span class="sxs-lookup"><span data-stu-id="a95da-191">Example query</span></span>

<span data-ttu-id="a95da-192">**Pieprasīt**</span><span class="sxs-lookup"><span data-stu-id="a95da-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="a95da-193">**Atbilde**</span><span class="sxs-lookup"><span data-stu-id="a95da-193">**Response**</span></span>

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
