---
title: Common Data Service elementi
description: Microsoft Dynamics 365 Human Resources izmanto Common Data Service, lai iespējotu paplašināšanas un integrācijas scenārijus.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: c8e0288da16829c04a9b97c0a52caa8bd27cddf8
ms.sourcegitcommit: fde8045ea49d0cf26d5e7ac5a0da5c0d3d69d5bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/26/2020
ms.locfileid: "3166502"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="efba5-103">Common Data Service elementi</span><span class="sxs-lookup"><span data-stu-id="efba5-103">Common Data Service entities</span></span>

<span data-ttu-id="efba5-104">Microsoft Dynamics 365 Human Resources izmanto Common Data Service, lai iespējotu paplašināšanas un integrācijas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="efba5-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="efba5-105">Plašāku informāciju par Common Data Service skatiet [Kas ir Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="efba5-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="efba5-106">Common Data Service ir pieejami šādas cilvēkresursu entitījas.</span><span class="sxs-lookup"><span data-stu-id="efba5-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="efba5-107">Atvieglojumu elementi</span><span class="sxs-lookup"><span data-stu-id="efba5-107">Benefit entities</span></span>

| <span data-ttu-id="efba5-108">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="efba5-108">Name</span></span> | <span data-ttu-id="efba5-109">Elements</span><span class="sxs-lookup"><span data-stu-id="efba5-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="efba5-110">Atvieglojumu aprēķina biežums</span><span class="sxs-lookup"><span data-stu-id="efba5-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="efba5-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="efba5-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="efba5-112">Atvieglojumu aprēķina biežuma izmaksas periods</span><span class="sxs-lookup"><span data-stu-id="efba5-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="efba5-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="efba5-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="efba5-114">Atvieglojumu aprēķina likme</span><span class="sxs-lookup"><span data-stu-id="efba5-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="efba5-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="efba5-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="efba5-116">Atvieglojumu aprēķina likmes detalizēta informācija</span><span class="sxs-lookup"><span data-stu-id="efba5-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="efba5-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="efba5-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="efba5-118">Atvieglojumu opcija</span><span class="sxs-lookup"><span data-stu-id="efba5-118">Benefit Option</span></span> | <span data-ttu-id="efba5-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="efba5-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="efba5-120">Atvieglojumu plāns</span><span class="sxs-lookup"><span data-stu-id="efba5-120">Benefit Plan</span></span> | <span data-ttu-id="efba5-121">cdm_benefitplan (nav iespējots pielāgoto lauku atbalsts)</span><span class="sxs-lookup"><span data-stu-id="efba5-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="efba5-122">Atvieglojumu veids</span><span class="sxs-lookup"><span data-stu-id="efba5-122">Benefit Type</span></span> | <span data-ttu-id="efba5-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="efba5-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="efba5-124">Biznesa procesa uzdevumu entītijas</span><span class="sxs-lookup"><span data-stu-id="efba5-124">Business process tasks entities</span></span>

| <span data-ttu-id="efba5-125">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="efba5-125">Name</span></span> | <span data-ttu-id="efba5-126">Elements</span><span class="sxs-lookup"><span data-stu-id="efba5-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="efba5-127">Biznesa procesu kalendārs</span><span class="sxs-lookup"><span data-stu-id="efba5-127">Business Process Calendar</span></span> | <span data-ttu-id="efba5-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="efba5-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="efba5-129">Biznesa procesu grupu piešķire</span><span class="sxs-lookup"><span data-stu-id="efba5-129">Business Process Group Assignment</span></span> | <span data-ttu-id="efba5-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="efba5-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="efba5-131">Biznesa procesu bibliotēkas uzdevumu grupa</span><span class="sxs-lookup"><span data-stu-id="efba5-131">Business Process Library Task Group</span></span> | <span data-ttu-id="efba5-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="efba5-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="efba5-133">Biznesa procesu stadija</span><span class="sxs-lookup"><span data-stu-id="efba5-133">Business Process Stage</span></span> | <span data-ttu-id="efba5-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="efba5-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="efba5-135">Kontrolsaraksta veidnes galvene</span><span class="sxs-lookup"><span data-stu-id="efba5-135">Checklist Template Header</span></span> | <span data-ttu-id="efba5-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="efba5-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="efba5-137">Kontrolsaraksta veidnes uzdevums</span><span class="sxs-lookup"><span data-stu-id="efba5-137">Checklist Template Task</span></span> | <span data-ttu-id="efba5-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="efba5-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="efba5-139">Atlīdzības entitījas</span><span class="sxs-lookup"><span data-stu-id="efba5-139">Compensation entities</span></span>

| <span data-ttu-id="efba5-140">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="efba5-140">Name</span></span> | <span data-ttu-id="efba5-141">Elements</span><span class="sxs-lookup"><span data-stu-id="efba5-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="efba5-142">Atlīdzības fiksētais plāns</span><span class="sxs-lookup"><span data-stu-id="efba5-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="efba5-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="efba5-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="efba5-144">Atlīdzības režģis</span><span class="sxs-lookup"><span data-stu-id="efba5-144">Compensation Grid</span></span> | <span data-ttu-id="efba5-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="efba5-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="efba5-146">Atlīdzības līmenis</span><span class="sxs-lookup"><span data-stu-id="efba5-146">Compensation Level</span></span> | <span data-ttu-id="efba5-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="efba5-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="efba5-148">Atlīdzības izmaksas biežums</span><span class="sxs-lookup"><span data-stu-id="efba5-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="efba5-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="efba5-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="efba5-150">Atlīdzības raksturojuma punktu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="efba5-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="efba5-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="efba5-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="efba5-152">Atlīdzības raksturojuma punktu iestatīšanas līnija</span><span class="sxs-lookup"><span data-stu-id="efba5-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="efba5-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="efba5-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="efba5-154">Atlīdzības reģions</span><span class="sxs-lookup"><span data-stu-id="efba5-154">Compensation Region</span></span> | <span data-ttu-id="efba5-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="efba5-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="efba5-156">Atlīdzības struktūra</span><span class="sxs-lookup"><span data-stu-id="efba5-156">Compensation Structure</span></span> | <span data-ttu-id="efba5-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="efba5-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="efba5-158">Atlīdzības mainīgais plāns</span><span class="sxs-lookup"><span data-stu-id="efba5-158">Compensation Variable Plan</span></span> | <span data-ttu-id="efba5-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="efba5-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="efba5-160">Atlīdzības mainīgā plāna līmenis</span><span class="sxs-lookup"><span data-stu-id="efba5-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="efba5-161">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="efba5-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="efba5-162">Atlīdzības mainīgā plāna tips</span><span class="sxs-lookup"><span data-stu-id="efba5-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="efba5-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="efba5-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="efba5-164">Fiksētas atlīdzības notikums</span><span class="sxs-lookup"><span data-stu-id="efba5-164">Fixed Compensation Event</span></span> | <span data-ttu-id="efba5-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="efba5-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="efba5-166">Izmaksu noteikums</span><span class="sxs-lookup"><span data-stu-id="efba5-166">Vesting Rule</span></span> | <span data-ttu-id="efba5-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="efba5-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="efba5-168">Nodarbinātā fiksētā atlīdzība</span><span class="sxs-lookup"><span data-stu-id="efba5-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="efba5-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="efba5-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="efba5-170">Organizācijas entītijas</span><span class="sxs-lookup"><span data-stu-id="efba5-170">Organization entities</span></span>

| <span data-ttu-id="efba5-171">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="efba5-171">Name</span></span> | <span data-ttu-id="efba5-172">Elements</span><span class="sxs-lookup"><span data-stu-id="efba5-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="efba5-173">Nodaļa</span><span class="sxs-lookup"><span data-stu-id="efba5-173">Department</span></span> | <span data-ttu-id="efba5-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="efba5-174">cdm_department</span></span> |
| <span data-ttu-id="efba5-175">Nodarbinātība</span><span class="sxs-lookup"><span data-stu-id="efba5-175">Employment</span></span> | <span data-ttu-id="efba5-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="efba5-176">cdm_employment</span></span> |
| <span data-ttu-id="efba5-177">Uzņēmums</span><span class="sxs-lookup"><span data-stu-id="efba5-177">Company</span></span> | <span data-ttu-id="efba5-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="efba5-178">cdm_company</span></span> |
| <span data-ttu-id="efba5-179">Darbs</span><span class="sxs-lookup"><span data-stu-id="efba5-179">Job</span></span> | <span data-ttu-id="efba5-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="efba5-180">cdm_job</span></span> |
| <span data-ttu-id="efba5-181">Darba funkcija</span><span class="sxs-lookup"><span data-stu-id="efba5-181">Job Function</span></span> | <span data-ttu-id="efba5-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="efba5-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="efba5-183">Amats</span><span class="sxs-lookup"><span data-stu-id="efba5-183">Job Position</span></span> | <span data-ttu-id="efba5-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="efba5-184">cdm_jobposition</span></span> |
| <span data-ttu-id="efba5-185">Amata veids</span><span class="sxs-lookup"><span data-stu-id="efba5-185">Position Type</span></span> | <span data-ttu-id="efba5-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="efba5-186">cdm_positiontype</span></span> |
| <span data-ttu-id="efba5-187">Amatā nodarbinātā piešķire</span><span class="sxs-lookup"><span data-stu-id="efba5-187">Position Worker Assignment</span></span> | <span data-ttu-id="efba5-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="efba5-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="efba5-189">Amata dimensija</span><span class="sxs-lookup"><span data-stu-id="efba5-189">Job Position Dimension</span></span> | <span data-ttu-id="efba5-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="efba5-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="efba5-191">Darba tips</span><span class="sxs-lookup"><span data-stu-id="efba5-191">Job Type</span></span> | <span data-ttu-id="efba5-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="efba5-192">cdm_jobtype</span></span> |
| <span data-ttu-id="efba5-193">Valoda</span><span class="sxs-lookup"><span data-stu-id="efba5-193">Language</span></span> | <span data-ttu-id="efba5-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="efba5-194">cdm_language</span></span> |
| <span data-ttu-id="efba5-195">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="efba5-195">Title</span></span> | <span data-ttu-id="efba5-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="efba5-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="efba5-197">Finanšu dimensijas **Amata veidam**, **Amata darbinieka piešķirei**un **Nodarbinātībai** pakalpojumam Common Data Service nodrošina vienvirziena integrāciju.</span><span class="sxs-lookup"><span data-stu-id="efba5-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="efba5-198">Finanšu dimensiju atjauninājumi pašlaik nesinhronizējas no Common Data Service uz personāla vadības resursiem.</span><span class="sxs-lookup"><span data-stu-id="efba5-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="efba5-199">Atvaļinājumu un kavējumu elementi</span><span class="sxs-lookup"><span data-stu-id="efba5-199">Leave and absence entities</span></span>

| <span data-ttu-id="efba5-200">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="efba5-200">Name</span></span> | <span data-ttu-id="efba5-201">Elements</span><span class="sxs-lookup"><span data-stu-id="efba5-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="efba5-202">Atvaļinājuma bankas transakcija</span><span class="sxs-lookup"><span data-stu-id="efba5-202">Leave Bank Transaction</span></span> | <span data-ttu-id="efba5-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="efba5-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="efba5-204">Atvaļinājuma reģistrācija</span><span class="sxs-lookup"><span data-stu-id="efba5-204">Leave Enrollment</span></span> | <span data-ttu-id="efba5-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="efba5-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="efba5-206">Atvaļinājumu plāns</span><span class="sxs-lookup"><span data-stu-id="efba5-206">Leave Plan</span></span> | <span data-ttu-id="efba5-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="efba5-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="efba5-208">Atvaļinājuma pieprasījums</span><span class="sxs-lookup"><span data-stu-id="efba5-208">Leave Request</span></span> | <span data-ttu-id="efba5-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="efba5-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="efba5-210">Atvaļinājuma pieprasījuma informācija</span><span class="sxs-lookup"><span data-stu-id="efba5-210">Leave Request Detail</span></span> | <span data-ttu-id="efba5-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="efba5-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="efba5-212">Atvaļinājuma tips</span><span class="sxs-lookup"><span data-stu-id="efba5-212">Leave Type</span></span> | <span data-ttu-id="efba5-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="efba5-213">cdm_leavetype</span></span> |
| <span data-ttu-id="efba5-214">Atvaļinājuma veida iemesla kods</span><span class="sxs-lookup"><span data-stu-id="efba5-214">Leave Type Reason Code</span></span> | <span data-ttu-id="efba5-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="efba5-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="efba5-216">Algas elementi</span><span class="sxs-lookup"><span data-stu-id="efba5-216">Payroll entities</span></span>

| <span data-ttu-id="efba5-217">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="efba5-217">Name</span></span> | <span data-ttu-id="efba5-218">Elements</span><span class="sxs-lookup"><span data-stu-id="efba5-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="efba5-219">Apmaksas cikls</span><span class="sxs-lookup"><span data-stu-id="efba5-219">Pay Cycle</span></span> | <span data-ttu-id="efba5-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="efba5-220">cdm_paycycle</span></span> |
| <span data-ttu-id="efba5-221">Apmaksas periods</span><span class="sxs-lookup"><span data-stu-id="efba5-221">Pay Period</span></span> | <span data-ttu-id="efba5-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="efba5-222">cdm_payperiod</span></span> |
| <span data-ttu-id="efba5-223">Algas nopelnīšanas kods</span><span class="sxs-lookup"><span data-stu-id="efba5-223">Payroll Earning Code</span></span> | <span data-ttu-id="efba5-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="efba5-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="efba5-225">Bankas konta izdevumi</span><span class="sxs-lookup"><span data-stu-id="efba5-225">Bank Account Disbursement</span></span> | <span data-ttu-id="efba5-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="efba5-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="efba5-227">Nodokļu reģions</span><span class="sxs-lookup"><span data-stu-id="efba5-227">Tax Region</span></span> | <span data-ttu-id="efba5-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="efba5-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="efba5-229">Nodarbinātā elementi</span><span class="sxs-lookup"><span data-stu-id="efba5-229">Worker entities</span></span>

| <span data-ttu-id="efba5-230">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="efba5-230">Name</span></span> | <span data-ttu-id="efba5-231">Elements</span><span class="sxs-lookup"><span data-stu-id="efba5-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="efba5-232">Nodarbinātais</span><span class="sxs-lookup"><span data-stu-id="efba5-232">Worker</span></span> | <span data-ttu-id="efba5-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="efba5-233">cdm_worker</span></span> |
| <span data-ttu-id="efba5-234">Nodarbinātā adrese</span><span class="sxs-lookup"><span data-stu-id="efba5-234">Worker Address</span></span> | <span data-ttu-id="efba5-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="efba5-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="efba5-236">Nodarbinātā personas dati</span><span class="sxs-lookup"><span data-stu-id="efba5-236">Worker Personal Detail</span></span> | <span data-ttu-id="efba5-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="efba5-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="efba5-238">Nodarbinātās personas identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="efba5-238">Worker Person Identification Number</span></span> | <span data-ttu-id="efba5-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="efba5-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="efba5-240">Nodarbinātās personas identifikācijas veids</span><span class="sxs-lookup"><span data-stu-id="efba5-240">Worker Person Identification Type</span></span> | <span data-ttu-id="efba5-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="efba5-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="efba5-242">Darba kalendārs</span><span class="sxs-lookup"><span data-stu-id="efba5-242">Work Calendar</span></span> | <span data-ttu-id="efba5-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="efba5-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="efba5-244">Darba kalendāra diena</span><span class="sxs-lookup"><span data-stu-id="efba5-244">Work Calendar Day</span></span> | <span data-ttu-id="efba5-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="efba5-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="efba5-246">Brīvdienas darba kalendārā</span><span class="sxs-lookup"><span data-stu-id="efba5-246">Work Calendar Holiday</span></span> |<span data-ttu-id="efba5-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="efba5-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="efba5-248">Brīvdienu rinda darba kalendārā</span><span class="sxs-lookup"><span data-stu-id="efba5-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="efba5-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="efba5-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="efba5-250">Darba kalendāra laika intervāls</span><span class="sxs-lookup"><span data-stu-id="efba5-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="efba5-251">cdm_workcalendartimeinterval (nav iespējots pielāgoto lauku atbalsts)</span><span class="sxs-lookup"><span data-stu-id="efba5-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="efba5-252">Nodarbinātā bankas konts</span><span class="sxs-lookup"><span data-stu-id="efba5-252">Worker Bank Account</span></span> | <span data-ttu-id="efba5-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="efba5-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="efba5-254">Nodarbinātā iestatījumu entitījas</span><span class="sxs-lookup"><span data-stu-id="efba5-254">Worker setup entities</span></span>

| <span data-ttu-id="efba5-255">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="efba5-255">Name</span></span> | <span data-ttu-id="efba5-256">Elements</span><span class="sxs-lookup"><span data-stu-id="efba5-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="efba5-257">Veterāna statuss</span><span class="sxs-lookup"><span data-stu-id="efba5-257">Veteran Status</span></span> | <span data-ttu-id="efba5-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="efba5-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="efba5-259">Etniskā izcelsme</span><span class="sxs-lookup"><span data-stu-id="efba5-259">Ethnic Origin</span></span> | <span data-ttu-id="efba5-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="efba5-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="efba5-261">Iemesla kods</span><span class="sxs-lookup"><span data-stu-id="efba5-261">Reason Code</span></span> | <span data-ttu-id="efba5-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="efba5-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="efba5-263">Personas identifikācijas dokumenta izdevējiestāde</span><span class="sxs-lookup"><span data-stu-id="efba5-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="efba5-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="efba5-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="efba5-265">Kompetences entitījas</span><span class="sxs-lookup"><span data-stu-id="efba5-265">Competency entities</span></span>

| <span data-ttu-id="efba5-266">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="efba5-266">Name</span></span> | <span data-ttu-id="efba5-267">Elements</span><span class="sxs-lookup"><span data-stu-id="efba5-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="efba5-268">Prasmju veids</span><span class="sxs-lookup"><span data-stu-id="efba5-268">Skill Type</span></span> | <span data-ttu-id="efba5-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="efba5-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="efba5-270">Entitījas attiecību modeļi</span><span class="sxs-lookup"><span data-stu-id="efba5-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="efba5-271">Nodarbinātais</span><span class="sxs-lookup"><span data-stu-id="efba5-271">Worker</span></span>

![Nodarbinātais](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="efba5-273">Darbs un amats</span><span class="sxs-lookup"><span data-stu-id="efba5-273">Job and Job Position</span></span>

![Darbs un amats](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="efba5-275">Priekšrocības</span><span class="sxs-lookup"><span data-stu-id="efba5-275">Benefits</span></span>

![Priekšrocības](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="efba5-277">Kompensācija</span><span class="sxs-lookup"><span data-stu-id="efba5-277">Compensation</span></span>

![Kompensācija](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="efba5-279">Pamest</span><span class="sxs-lookup"><span data-stu-id="efba5-279">Leave</span></span>

![Pamest](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="efba5-281">Darba kalendārs</span><span class="sxs-lookup"><span data-stu-id="efba5-281">Work Calendar</span></span>

![Darba kalendārs](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="efba5-283">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="efba5-283">See also</span></span>

[<span data-ttu-id="efba5-284">Izvēlēties datu integrācijas tehnoloģiju</span><span class="sxs-lookup"><span data-stu-id="efba5-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="efba5-285">Common Data Service integrācijas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="efba5-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
