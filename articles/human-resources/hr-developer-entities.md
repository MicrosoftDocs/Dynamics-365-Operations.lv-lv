---
title: Dataverse tabulas
description: Microsoft Dynamics 365 Human Resources izmanto Dataverse, lai iespējotu paplašināšanas un integrācijas scenārijus.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e316cda9b9c5361c0a2837e7ed6c050e76cc39b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793613"
---
# <a name="dataverse-tables"></a><span data-ttu-id="cccfd-103">Dataverse tabulas</span><span class="sxs-lookup"><span data-stu-id="cccfd-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cccfd-104">Microsoft Dynamics 365 Human Resources izmanto Dataverse, lai iespējotu paplašināšanas un integrācijas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="cccfd-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="cccfd-105">Human Resources elementi atbilst Dataverse tabulām.</span><span class="sxs-lookup"><span data-stu-id="cccfd-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="cccfd-106">Papildinformāciju par Dataverse (iepriekš Common Data Service) un terminoloģijas atjauninājumiem skatiet sadaļā [Kas ir Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="cccfd-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="cccfd-107">Šādas Dataverse tabulas ir pieejamas, pamatojoties uz Human Resources elementiem.</span><span class="sxs-lookup"><span data-stu-id="cccfd-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="cccfd-108">Atvieglojumu tabulas</span><span class="sxs-lookup"><span data-stu-id="cccfd-108">Benefit tables</span></span>

| <span data-ttu-id="cccfd-109">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="cccfd-109">Name</span></span> | <span data-ttu-id="cccfd-110">Tabula</span><span class="sxs-lookup"><span data-stu-id="cccfd-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cccfd-111">Atvieglojumu aprēķina biežums</span><span class="sxs-lookup"><span data-stu-id="cccfd-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="cccfd-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="cccfd-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="cccfd-113">Atvieglojumu aprēķina biežuma izmaksas periods</span><span class="sxs-lookup"><span data-stu-id="cccfd-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="cccfd-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="cccfd-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="cccfd-115">Atvieglojumu aprēķina likme</span><span class="sxs-lookup"><span data-stu-id="cccfd-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="cccfd-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="cccfd-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="cccfd-117">Atvieglojumu aprēķina likmes detalizēta informācija</span><span class="sxs-lookup"><span data-stu-id="cccfd-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="cccfd-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="cccfd-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="cccfd-119">Atvieglojumu opcija</span><span class="sxs-lookup"><span data-stu-id="cccfd-119">Benefit Option</span></span> | <span data-ttu-id="cccfd-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="cccfd-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="cccfd-121">Atvieglojumu plāns</span><span class="sxs-lookup"><span data-stu-id="cccfd-121">Benefit Plan</span></span> | <span data-ttu-id="cccfd-122">cdm_benefitplan (nav iespējots pielāgoto lauku atbalsts)</span><span class="sxs-lookup"><span data-stu-id="cccfd-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="cccfd-123">Atvieglojumu veids</span><span class="sxs-lookup"><span data-stu-id="cccfd-123">Benefit Type</span></span> | <span data-ttu-id="cccfd-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="cccfd-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="cccfd-125">Biznesa procesa uzdevumu tabulas</span><span class="sxs-lookup"><span data-stu-id="cccfd-125">Business process tasks tables</span></span>

| <span data-ttu-id="cccfd-126">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="cccfd-126">Name</span></span> | <span data-ttu-id="cccfd-127">Tabula</span><span class="sxs-lookup"><span data-stu-id="cccfd-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cccfd-128">Biznesa procesu kalendārs</span><span class="sxs-lookup"><span data-stu-id="cccfd-128">Business Process Calendar</span></span> | <span data-ttu-id="cccfd-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="cccfd-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="cccfd-130">Biznesa procesu grupu piešķire</span><span class="sxs-lookup"><span data-stu-id="cccfd-130">Business Process Group Assignment</span></span> | <span data-ttu-id="cccfd-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="cccfd-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="cccfd-132">Biznesa procesu bibliotēkas uzdevumu grupa</span><span class="sxs-lookup"><span data-stu-id="cccfd-132">Business Process Library Task Group</span></span> | <span data-ttu-id="cccfd-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="cccfd-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="cccfd-134">Biznesa procesu stadija</span><span class="sxs-lookup"><span data-stu-id="cccfd-134">Business Process Stage</span></span> | <span data-ttu-id="cccfd-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="cccfd-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="cccfd-136">Kontrolsaraksta veidnes galvene</span><span class="sxs-lookup"><span data-stu-id="cccfd-136">Checklist Template Header</span></span> | <span data-ttu-id="cccfd-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="cccfd-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="cccfd-138">Kontrolsaraksta veidnes uzdevums</span><span class="sxs-lookup"><span data-stu-id="cccfd-138">Checklist Template Task</span></span> | <span data-ttu-id="cccfd-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="cccfd-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="cccfd-140">Kompensāciju tabulas</span><span class="sxs-lookup"><span data-stu-id="cccfd-140">Compensation tables</span></span>

| <span data-ttu-id="cccfd-141">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="cccfd-141">Name</span></span> | <span data-ttu-id="cccfd-142">Tabula</span><span class="sxs-lookup"><span data-stu-id="cccfd-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cccfd-143">Atlīdzības fiksētais plāns</span><span class="sxs-lookup"><span data-stu-id="cccfd-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="cccfd-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="cccfd-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="cccfd-145">Atlīdzības režģis</span><span class="sxs-lookup"><span data-stu-id="cccfd-145">Compensation Grid</span></span> | <span data-ttu-id="cccfd-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="cccfd-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="cccfd-147">Atlīdzības līmenis</span><span class="sxs-lookup"><span data-stu-id="cccfd-147">Compensation Level</span></span> | <span data-ttu-id="cccfd-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="cccfd-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="cccfd-149">Atlīdzības izmaksas biežums</span><span class="sxs-lookup"><span data-stu-id="cccfd-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="cccfd-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="cccfd-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="cccfd-151">Atlīdzības raksturojuma punktu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cccfd-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="cccfd-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="cccfd-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="cccfd-153">Atlīdzības raksturojuma punktu iestatīšanas līnija</span><span class="sxs-lookup"><span data-stu-id="cccfd-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="cccfd-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="cccfd-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="cccfd-155">Atlīdzības reģions</span><span class="sxs-lookup"><span data-stu-id="cccfd-155">Compensation Region</span></span> | <span data-ttu-id="cccfd-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="cccfd-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="cccfd-157">Atlīdzības struktūra</span><span class="sxs-lookup"><span data-stu-id="cccfd-157">Compensation Structure</span></span> | <span data-ttu-id="cccfd-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="cccfd-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="cccfd-159">Atlīdzības mainīgais plāns</span><span class="sxs-lookup"><span data-stu-id="cccfd-159">Compensation Variable Plan</span></span> | <span data-ttu-id="cccfd-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="cccfd-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="cccfd-161">Atlīdzības mainīgā plāna līmenis</span><span class="sxs-lookup"><span data-stu-id="cccfd-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="cccfd-162">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="cccfd-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="cccfd-163">Atlīdzības mainīgā plāna tips</span><span class="sxs-lookup"><span data-stu-id="cccfd-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="cccfd-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="cccfd-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="cccfd-165">Fiksētas atlīdzības notikums</span><span class="sxs-lookup"><span data-stu-id="cccfd-165">Fixed Compensation Event</span></span> | <span data-ttu-id="cccfd-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="cccfd-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="cccfd-167">Izmaksu noteikums</span><span class="sxs-lookup"><span data-stu-id="cccfd-167">Vesting Rule</span></span> | <span data-ttu-id="cccfd-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="cccfd-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="cccfd-169">Nodarbinātā fiksētā atlīdzība</span><span class="sxs-lookup"><span data-stu-id="cccfd-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="cccfd-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="cccfd-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="cccfd-171">Organizācijas tabulas</span><span class="sxs-lookup"><span data-stu-id="cccfd-171">Organization tables</span></span>

| <span data-ttu-id="cccfd-172">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="cccfd-172">Name</span></span> | <span data-ttu-id="cccfd-173">Tabula</span><span class="sxs-lookup"><span data-stu-id="cccfd-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cccfd-174">Nodaļa</span><span class="sxs-lookup"><span data-stu-id="cccfd-174">Department</span></span> | <span data-ttu-id="cccfd-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="cccfd-175">cdm_department</span></span> |
| <span data-ttu-id="cccfd-176">Nodarbinātība</span><span class="sxs-lookup"><span data-stu-id="cccfd-176">Employment</span></span> | <span data-ttu-id="cccfd-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="cccfd-177">cdm_employment</span></span> |
| <span data-ttu-id="cccfd-178">Uzņēmums</span><span class="sxs-lookup"><span data-stu-id="cccfd-178">Company</span></span> | <span data-ttu-id="cccfd-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="cccfd-179">cdm_company</span></span> |
| <span data-ttu-id="cccfd-180">Darbs</span><span class="sxs-lookup"><span data-stu-id="cccfd-180">Job</span></span> | <span data-ttu-id="cccfd-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="cccfd-181">cdm_job</span></span> |
| <span data-ttu-id="cccfd-182">Darba funkcija</span><span class="sxs-lookup"><span data-stu-id="cccfd-182">Job Function</span></span> | <span data-ttu-id="cccfd-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="cccfd-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="cccfd-184">Amats</span><span class="sxs-lookup"><span data-stu-id="cccfd-184">Job Position</span></span> | <span data-ttu-id="cccfd-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="cccfd-185">cdm_jobposition</span></span> |
| <span data-ttu-id="cccfd-186">Amata veids</span><span class="sxs-lookup"><span data-stu-id="cccfd-186">Position Type</span></span> | <span data-ttu-id="cccfd-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="cccfd-187">cdm_positiontype</span></span> |
| <span data-ttu-id="cccfd-188">Amatā nodarbinātā piešķire</span><span class="sxs-lookup"><span data-stu-id="cccfd-188">Position Worker Assignment</span></span> | <span data-ttu-id="cccfd-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="cccfd-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="cccfd-190">Amata dimensija</span><span class="sxs-lookup"><span data-stu-id="cccfd-190">Job Position Dimension</span></span> | <span data-ttu-id="cccfd-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="cccfd-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="cccfd-192">Darba tips</span><span class="sxs-lookup"><span data-stu-id="cccfd-192">Job Type</span></span> | <span data-ttu-id="cccfd-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="cccfd-193">cdm_jobtype</span></span> |
| <span data-ttu-id="cccfd-194">Valoda</span><span class="sxs-lookup"><span data-stu-id="cccfd-194">Language</span></span> | <span data-ttu-id="cccfd-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="cccfd-195">cdm_language</span></span> |
| <span data-ttu-id="cccfd-196">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="cccfd-196">Title</span></span> | <span data-ttu-id="cccfd-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="cccfd-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="cccfd-198">Finanšu dimensijas **Amata veidam**, **Amata darbinieka piešķirei** un **Nodarbinātībai** pakalpojumam Dataverse nodrošina vienvirziena integrāciju.</span><span class="sxs-lookup"><span data-stu-id="cccfd-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="cccfd-199">Finanšu dimensiju atjauninājumi pašlaik nesinhronizējas no Dataverse uz personāla vadības resursiem.</span><span class="sxs-lookup"><span data-stu-id="cccfd-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="cccfd-200">Atvaļinājumu un prombūtnes tabulas</span><span class="sxs-lookup"><span data-stu-id="cccfd-200">Leave and absence tables</span></span>

| <span data-ttu-id="cccfd-201">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="cccfd-201">Name</span></span> | <span data-ttu-id="cccfd-202">Tabula</span><span class="sxs-lookup"><span data-stu-id="cccfd-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cccfd-203">Atvaļinājuma bankas transakcija</span><span class="sxs-lookup"><span data-stu-id="cccfd-203">Leave Bank Transaction</span></span> | <span data-ttu-id="cccfd-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="cccfd-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="cccfd-205">Atvaļinājuma reģistrācija</span><span class="sxs-lookup"><span data-stu-id="cccfd-205">Leave Enrollment</span></span> | <span data-ttu-id="cccfd-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="cccfd-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="cccfd-207">Atvaļinājumu plāns</span><span class="sxs-lookup"><span data-stu-id="cccfd-207">Leave Plan</span></span> | <span data-ttu-id="cccfd-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="cccfd-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="cccfd-209">Atvaļinājuma pieprasījums</span><span class="sxs-lookup"><span data-stu-id="cccfd-209">Leave Request</span></span> | <span data-ttu-id="cccfd-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="cccfd-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="cccfd-211">Atvaļinājuma pieprasījuma informācija</span><span class="sxs-lookup"><span data-stu-id="cccfd-211">Leave Request Detail</span></span> | <span data-ttu-id="cccfd-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="cccfd-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="cccfd-213">Atvaļinājuma tips</span><span class="sxs-lookup"><span data-stu-id="cccfd-213">Leave Type</span></span> | <span data-ttu-id="cccfd-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="cccfd-214">cdm_leavetype</span></span> |
| <span data-ttu-id="cccfd-215">Atvaļinājuma veida iemesla kods</span><span class="sxs-lookup"><span data-stu-id="cccfd-215">Leave Type Reason Code</span></span> | <span data-ttu-id="cccfd-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="cccfd-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="cccfd-217">Algu tabulas</span><span class="sxs-lookup"><span data-stu-id="cccfd-217">Payroll tables</span></span>

| <span data-ttu-id="cccfd-218">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="cccfd-218">Name</span></span> | <span data-ttu-id="cccfd-219">Tabula</span><span class="sxs-lookup"><span data-stu-id="cccfd-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cccfd-220">Apmaksas cikls</span><span class="sxs-lookup"><span data-stu-id="cccfd-220">Pay Cycle</span></span> | <span data-ttu-id="cccfd-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="cccfd-221">cdm_paycycle</span></span> |
| <span data-ttu-id="cccfd-222">Apmaksas periods</span><span class="sxs-lookup"><span data-stu-id="cccfd-222">Pay Period</span></span> | <span data-ttu-id="cccfd-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="cccfd-223">cdm_payperiod</span></span> |
| <span data-ttu-id="cccfd-224">Algas ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="cccfd-224">Payroll Earning Code</span></span> | <span data-ttu-id="cccfd-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="cccfd-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="cccfd-226">Bankas konta izdevumi</span><span class="sxs-lookup"><span data-stu-id="cccfd-226">Bank Account Disbursement</span></span> | <span data-ttu-id="cccfd-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="cccfd-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="cccfd-228">Nodokļu reģions</span><span class="sxs-lookup"><span data-stu-id="cccfd-228">Tax Region</span></span> | <span data-ttu-id="cccfd-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="cccfd-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="cccfd-230">Darbinieku tabulas</span><span class="sxs-lookup"><span data-stu-id="cccfd-230">Worker tables</span></span>

| <span data-ttu-id="cccfd-231">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="cccfd-231">Name</span></span> | <span data-ttu-id="cccfd-232">Tabula</span><span class="sxs-lookup"><span data-stu-id="cccfd-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cccfd-233">Darbinieks</span><span class="sxs-lookup"><span data-stu-id="cccfd-233">Worker</span></span> | <span data-ttu-id="cccfd-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="cccfd-234">cdm_worker</span></span> |
| <span data-ttu-id="cccfd-235">Nodarbinātā adrese</span><span class="sxs-lookup"><span data-stu-id="cccfd-235">Worker Address</span></span> | <span data-ttu-id="cccfd-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="cccfd-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="cccfd-237">Nodarbinātā personas dati</span><span class="sxs-lookup"><span data-stu-id="cccfd-237">Worker Personal Detail</span></span> | <span data-ttu-id="cccfd-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="cccfd-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="cccfd-239">Nodarbinātās personas identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="cccfd-239">Worker Person Identification Number</span></span> | <span data-ttu-id="cccfd-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="cccfd-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="cccfd-241">Nodarbinātās personas identifikācijas veids</span><span class="sxs-lookup"><span data-stu-id="cccfd-241">Worker Person Identification Type</span></span> | <span data-ttu-id="cccfd-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="cccfd-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="cccfd-243">Darba kalendārs</span><span class="sxs-lookup"><span data-stu-id="cccfd-243">Work Calendar</span></span> | <span data-ttu-id="cccfd-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="cccfd-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="cccfd-245">Darba kalendāra diena</span><span class="sxs-lookup"><span data-stu-id="cccfd-245">Work Calendar Day</span></span> | <span data-ttu-id="cccfd-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="cccfd-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="cccfd-247">Brīvdienas darba kalendārā</span><span class="sxs-lookup"><span data-stu-id="cccfd-247">Work Calendar Holiday</span></span> |<span data-ttu-id="cccfd-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="cccfd-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="cccfd-249">Brīvdienu rinda darba kalendārā</span><span class="sxs-lookup"><span data-stu-id="cccfd-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="cccfd-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="cccfd-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="cccfd-251">Darba kalendāra laika intervāls</span><span class="sxs-lookup"><span data-stu-id="cccfd-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="cccfd-252">cdm_workcalendartimeinterval (nav iespējots pielāgoto lauku atbalsts)</span><span class="sxs-lookup"><span data-stu-id="cccfd-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="cccfd-253">Nodarbinātā bankas konts</span><span class="sxs-lookup"><span data-stu-id="cccfd-253">Worker Bank Account</span></span> | <span data-ttu-id="cccfd-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="cccfd-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="cccfd-255">Darbinieka iestatījumu tabulas</span><span class="sxs-lookup"><span data-stu-id="cccfd-255">Worker setup tables</span></span>

| <span data-ttu-id="cccfd-256">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="cccfd-256">Name</span></span> | <span data-ttu-id="cccfd-257">Tabula</span><span class="sxs-lookup"><span data-stu-id="cccfd-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cccfd-258">Veterāna statuss</span><span class="sxs-lookup"><span data-stu-id="cccfd-258">Veteran Status</span></span> | <span data-ttu-id="cccfd-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="cccfd-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="cccfd-260">Etniskā izcelsme</span><span class="sxs-lookup"><span data-stu-id="cccfd-260">Ethnic Origin</span></span> | <span data-ttu-id="cccfd-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="cccfd-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="cccfd-262">Iemesla kods</span><span class="sxs-lookup"><span data-stu-id="cccfd-262">Reason Code</span></span> | <span data-ttu-id="cccfd-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="cccfd-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="cccfd-264">Personas identifikācijas izsniedzēja iestāde</span><span class="sxs-lookup"><span data-stu-id="cccfd-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="cccfd-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="cccfd-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="cccfd-266">Kompetenču tabulas</span><span class="sxs-lookup"><span data-stu-id="cccfd-266">Competency tables</span></span>

| <span data-ttu-id="cccfd-267">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="cccfd-267">Name</span></span> | <span data-ttu-id="cccfd-268">Tabula</span><span class="sxs-lookup"><span data-stu-id="cccfd-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cccfd-269">Prasmju tips</span><span class="sxs-lookup"><span data-stu-id="cccfd-269">Skill Type</span></span> | <span data-ttu-id="cccfd-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="cccfd-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="cccfd-271">Tabulas attiecību modeļi</span><span class="sxs-lookup"><span data-stu-id="cccfd-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="cccfd-272">Darbinieks</span><span class="sxs-lookup"><span data-stu-id="cccfd-272">Worker</span></span>

![Darbinieks](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="cccfd-274">Darbs un amats</span><span class="sxs-lookup"><span data-stu-id="cccfd-274">Job and Job Position</span></span>

![Darbs un amats](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="cccfd-276">Priekšrocības</span><span class="sxs-lookup"><span data-stu-id="cccfd-276">Benefits</span></span>

![Priekšrocības](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="cccfd-278">Kompensācija</span><span class="sxs-lookup"><span data-stu-id="cccfd-278">Compensation</span></span>

![Kompensācija](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="cccfd-280">Pamest</span><span class="sxs-lookup"><span data-stu-id="cccfd-280">Leave</span></span>

![Pamest](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="cccfd-282">Darba kalendārs</span><span class="sxs-lookup"><span data-stu-id="cccfd-282">Work Calendar</span></span>

![Darba kalendārs](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="cccfd-284">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="cccfd-284">See also</span></span>

[<span data-ttu-id="cccfd-285">Izvēlēties datu integrācijas tehnoloģiju</span><span class="sxs-lookup"><span data-stu-id="cccfd-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="cccfd-286">Pakalpojuma Dataverse integrācijas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="cccfd-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="cccfd-287">Pakalpojuma Dataverse virtuālo tabulu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="cccfd-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="cccfd-288">Human Resources virtuālās tabulas: Bieži uzdotie jautājumi</span><span class="sxs-lookup"><span data-stu-id="cccfd-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="cccfd-289">Kas ir Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="cccfd-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="cccfd-290">Terminoloģijas atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="cccfd-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]