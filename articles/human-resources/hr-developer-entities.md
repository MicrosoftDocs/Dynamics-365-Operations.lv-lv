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
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087350"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="772ef-103">Common Data Service elementi</span><span class="sxs-lookup"><span data-stu-id="772ef-103">Common Data Service entities</span></span>

<span data-ttu-id="772ef-104">Microsoft Dynamics 365 Human Resources izmanto Common Data Service, lai iespējotu paplašināšanas un integrācijas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="772ef-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="772ef-105">Plašāku informāciju par Common Data Service skatiet [Kas ir Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="772ef-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="772ef-106">Common Data Service ir pieejami šādas cilvēkresursu entitījas.</span><span class="sxs-lookup"><span data-stu-id="772ef-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="772ef-107">Atvieglojumu elementi</span><span class="sxs-lookup"><span data-stu-id="772ef-107">Benefit entities</span></span>

| <span data-ttu-id="772ef-108">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="772ef-108">Name</span></span> | <span data-ttu-id="772ef-109">Elements</span><span class="sxs-lookup"><span data-stu-id="772ef-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="772ef-110">Atvieglojumu aprēķina biežums</span><span class="sxs-lookup"><span data-stu-id="772ef-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="772ef-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="772ef-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="772ef-112">Atvieglojumu aprēķina biežuma izmaksas periods</span><span class="sxs-lookup"><span data-stu-id="772ef-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="772ef-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="772ef-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="772ef-114">Atvieglojumu aprēķina likme</span><span class="sxs-lookup"><span data-stu-id="772ef-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="772ef-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="772ef-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="772ef-116">Atvieglojumu aprēķina likmes detalizēta informācija</span><span class="sxs-lookup"><span data-stu-id="772ef-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="772ef-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="772ef-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="772ef-118">Atvieglojumu opcija</span><span class="sxs-lookup"><span data-stu-id="772ef-118">Benefit Option</span></span> | <span data-ttu-id="772ef-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="772ef-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="772ef-120">Atvieglojumu plāns</span><span class="sxs-lookup"><span data-stu-id="772ef-120">Benefit Plan</span></span> | <span data-ttu-id="772ef-121">cdm_benefitplan (nav iespējots pielāgoto lauku atbalsts)</span><span class="sxs-lookup"><span data-stu-id="772ef-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="772ef-122">Atvieglojumu veids</span><span class="sxs-lookup"><span data-stu-id="772ef-122">Benefit Type</span></span> | <span data-ttu-id="772ef-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="772ef-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="772ef-124">Biznesa procesa uzdevumu entītijas</span><span class="sxs-lookup"><span data-stu-id="772ef-124">Business process tasks entities</span></span>

| <span data-ttu-id="772ef-125">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="772ef-125">Name</span></span> | <span data-ttu-id="772ef-126">Elements</span><span class="sxs-lookup"><span data-stu-id="772ef-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="772ef-127">Biznesa procesu kalendārs</span><span class="sxs-lookup"><span data-stu-id="772ef-127">Business Process Calendar</span></span> | <span data-ttu-id="772ef-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="772ef-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="772ef-129">Biznesa procesu grupu piešķire</span><span class="sxs-lookup"><span data-stu-id="772ef-129">Business Process Group Assignment</span></span> | <span data-ttu-id="772ef-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="772ef-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="772ef-131">Biznesa procesu bibliotēkas uzdevumu grupa</span><span class="sxs-lookup"><span data-stu-id="772ef-131">Business Process Library Task Group</span></span> | <span data-ttu-id="772ef-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="772ef-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="772ef-133">Biznesa procesu stadija</span><span class="sxs-lookup"><span data-stu-id="772ef-133">Business Process Stage</span></span> | <span data-ttu-id="772ef-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="772ef-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="772ef-135">Kontrolsaraksta veidnes galvene</span><span class="sxs-lookup"><span data-stu-id="772ef-135">Checklist Template Header</span></span> | <span data-ttu-id="772ef-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="772ef-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="772ef-137">Kontrolsaraksta veidnes uzdevums</span><span class="sxs-lookup"><span data-stu-id="772ef-137">Checklist Template Task</span></span> | <span data-ttu-id="772ef-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="772ef-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="772ef-139">Atlīdzības entitījas</span><span class="sxs-lookup"><span data-stu-id="772ef-139">Compensation entities</span></span>

| <span data-ttu-id="772ef-140">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="772ef-140">Name</span></span> | <span data-ttu-id="772ef-141">Elements</span><span class="sxs-lookup"><span data-stu-id="772ef-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="772ef-142">Atlīdzības fiksētais plāns</span><span class="sxs-lookup"><span data-stu-id="772ef-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="772ef-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="772ef-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="772ef-144">Atlīdzības režģis</span><span class="sxs-lookup"><span data-stu-id="772ef-144">Compensation Grid</span></span> | <span data-ttu-id="772ef-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="772ef-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="772ef-146">Atlīdzības līmenis</span><span class="sxs-lookup"><span data-stu-id="772ef-146">Compensation Level</span></span> | <span data-ttu-id="772ef-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="772ef-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="772ef-148">Atlīdzības izmaksas biežums</span><span class="sxs-lookup"><span data-stu-id="772ef-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="772ef-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="772ef-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="772ef-150">Atlīdzības raksturojuma punktu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="772ef-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="772ef-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="772ef-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="772ef-152">Atlīdzības raksturojuma punktu iestatīšanas līnija</span><span class="sxs-lookup"><span data-stu-id="772ef-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="772ef-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="772ef-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="772ef-154">Atlīdzības reģions</span><span class="sxs-lookup"><span data-stu-id="772ef-154">Compensation Region</span></span> | <span data-ttu-id="772ef-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="772ef-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="772ef-156">Atlīdzības struktūra</span><span class="sxs-lookup"><span data-stu-id="772ef-156">Compensation Structure</span></span> | <span data-ttu-id="772ef-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="772ef-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="772ef-158">Atlīdzības mainīgais plāns</span><span class="sxs-lookup"><span data-stu-id="772ef-158">Compensation Variable Plan</span></span> | <span data-ttu-id="772ef-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="772ef-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="772ef-160">Atlīdzības mainīgā plāna līmenis</span><span class="sxs-lookup"><span data-stu-id="772ef-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="772ef-161">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="772ef-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="772ef-162">Atlīdzības mainīgā plāna tips</span><span class="sxs-lookup"><span data-stu-id="772ef-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="772ef-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="772ef-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="772ef-164">Fiksētas atlīdzības notikums</span><span class="sxs-lookup"><span data-stu-id="772ef-164">Fixed Compensation Event</span></span> | <span data-ttu-id="772ef-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="772ef-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="772ef-166">Izmaksu noteikums</span><span class="sxs-lookup"><span data-stu-id="772ef-166">Vesting Rule</span></span> | <span data-ttu-id="772ef-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="772ef-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="772ef-168">Nodarbinātā fiksētā atlīdzība</span><span class="sxs-lookup"><span data-stu-id="772ef-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="772ef-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="772ef-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="772ef-170">Organizācijas entītijas</span><span class="sxs-lookup"><span data-stu-id="772ef-170">Organization entities</span></span>

| <span data-ttu-id="772ef-171">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="772ef-171">Name</span></span> | <span data-ttu-id="772ef-172">Elements</span><span class="sxs-lookup"><span data-stu-id="772ef-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="772ef-173">Nodaļa</span><span class="sxs-lookup"><span data-stu-id="772ef-173">Department</span></span> | <span data-ttu-id="772ef-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="772ef-174">cdm_department</span></span> |
| <span data-ttu-id="772ef-175">Nodarbinātība</span><span class="sxs-lookup"><span data-stu-id="772ef-175">Employment</span></span> | <span data-ttu-id="772ef-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="772ef-176">cdm_employment</span></span> |
| <span data-ttu-id="772ef-177">Uzņēmums</span><span class="sxs-lookup"><span data-stu-id="772ef-177">Company</span></span> | <span data-ttu-id="772ef-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="772ef-178">cdm_company</span></span> |
| <span data-ttu-id="772ef-179">Darbs</span><span class="sxs-lookup"><span data-stu-id="772ef-179">Job</span></span> | <span data-ttu-id="772ef-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="772ef-180">cdm_job</span></span> |
| <span data-ttu-id="772ef-181">Darba funkcija</span><span class="sxs-lookup"><span data-stu-id="772ef-181">Job Function</span></span> | <span data-ttu-id="772ef-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="772ef-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="772ef-183">Amats</span><span class="sxs-lookup"><span data-stu-id="772ef-183">Job Position</span></span> | <span data-ttu-id="772ef-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="772ef-184">cdm_jobposition</span></span> |
| <span data-ttu-id="772ef-185">Amata veids</span><span class="sxs-lookup"><span data-stu-id="772ef-185">Position Type</span></span> | <span data-ttu-id="772ef-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="772ef-186">cdm_positiontype</span></span> |
| <span data-ttu-id="772ef-187">Amatā nodarbinātā piešķire</span><span class="sxs-lookup"><span data-stu-id="772ef-187">Position Worker Assignment</span></span> | <span data-ttu-id="772ef-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="772ef-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="772ef-189">Darba tips</span><span class="sxs-lookup"><span data-stu-id="772ef-189">Job Type</span></span> | <span data-ttu-id="772ef-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="772ef-190">cdm_jobtype</span></span> |
| <span data-ttu-id="772ef-191">Valoda</span><span class="sxs-lookup"><span data-stu-id="772ef-191">Language</span></span> | <span data-ttu-id="772ef-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="772ef-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="772ef-193">Atvaļinājumu un kavējumu elementi</span><span class="sxs-lookup"><span data-stu-id="772ef-193">Leave and absence entities</span></span>

| <span data-ttu-id="772ef-194">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="772ef-194">Name</span></span> | <span data-ttu-id="772ef-195">Elements</span><span class="sxs-lookup"><span data-stu-id="772ef-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="772ef-196">Transakcija Atstāt tukšu</span><span class="sxs-lookup"><span data-stu-id="772ef-196">Leave Bank Transaction</span></span> | <span data-ttu-id="772ef-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="772ef-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="772ef-198">Atvaļinājuma reģistrācija</span><span class="sxs-lookup"><span data-stu-id="772ef-198">Leave Enrollment</span></span> | <span data-ttu-id="772ef-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="772ef-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="772ef-200">Atvaļinājumu plāns</span><span class="sxs-lookup"><span data-stu-id="772ef-200">Leave Plan</span></span> | <span data-ttu-id="772ef-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="772ef-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="772ef-202">Atvaļinājuma pieprasījums</span><span class="sxs-lookup"><span data-stu-id="772ef-202">Leave Request</span></span> | <span data-ttu-id="772ef-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="772ef-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="772ef-204">Atvaļinājuma pieprasījuma informācija</span><span class="sxs-lookup"><span data-stu-id="772ef-204">Leave Request Detail</span></span> | <span data-ttu-id="772ef-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="772ef-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="772ef-206">Atvaļinājuma tips</span><span class="sxs-lookup"><span data-stu-id="772ef-206">Leave Type</span></span> | <span data-ttu-id="772ef-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="772ef-207">cdm_leavetype</span></span> |
| <span data-ttu-id="772ef-208">Atvaļinājuma veida iemesla kods</span><span class="sxs-lookup"><span data-stu-id="772ef-208">Leave Type Reason Code</span></span> | <span data-ttu-id="772ef-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="772ef-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="772ef-210">Algas elementi</span><span class="sxs-lookup"><span data-stu-id="772ef-210">Payroll entities</span></span>

| <span data-ttu-id="772ef-211">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="772ef-211">Name</span></span> | <span data-ttu-id="772ef-212">Elements</span><span class="sxs-lookup"><span data-stu-id="772ef-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="772ef-213">Apmaksas cikls</span><span class="sxs-lookup"><span data-stu-id="772ef-213">Pay Cycle</span></span> | <span data-ttu-id="772ef-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="772ef-214">cdm_paycycle</span></span> |
| <span data-ttu-id="772ef-215">Apmaksas periods</span><span class="sxs-lookup"><span data-stu-id="772ef-215">Pay Period</span></span> | <span data-ttu-id="772ef-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="772ef-216">cdm_payperiod</span></span> |
| <span data-ttu-id="772ef-217">Algas nopelnīšanas kods</span><span class="sxs-lookup"><span data-stu-id="772ef-217">Payroll Earning Code</span></span> | <span data-ttu-id="772ef-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="772ef-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="772ef-219">Bankas konta izdevumi</span><span class="sxs-lookup"><span data-stu-id="772ef-219">Bank Account Disbursement</span></span> | <span data-ttu-id="772ef-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="772ef-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="772ef-221">Nodokļu reģions</span><span class="sxs-lookup"><span data-stu-id="772ef-221">Tax Region</span></span> | <span data-ttu-id="772ef-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="772ef-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="772ef-223">Nodarbinātā elementi</span><span class="sxs-lookup"><span data-stu-id="772ef-223">Worker entities</span></span>

| <span data-ttu-id="772ef-224">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="772ef-224">Name</span></span> | <span data-ttu-id="772ef-225">Elements</span><span class="sxs-lookup"><span data-stu-id="772ef-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="772ef-226">Nodarbinātais</span><span class="sxs-lookup"><span data-stu-id="772ef-226">Worker</span></span> | <span data-ttu-id="772ef-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="772ef-227">cdm_worker</span></span> |
| <span data-ttu-id="772ef-228">Nodarbinātā adrese</span><span class="sxs-lookup"><span data-stu-id="772ef-228">Worker Address</span></span> | <span data-ttu-id="772ef-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="772ef-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="772ef-230">Nodarbinātā personas dati</span><span class="sxs-lookup"><span data-stu-id="772ef-230">Worker Personal Detail</span></span> | <span data-ttu-id="772ef-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="772ef-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="772ef-232">Nodarbinātās personas identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="772ef-232">Worker Person Identification Number</span></span> | <span data-ttu-id="772ef-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="772ef-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="772ef-234">Nodarbinātās personas identifikācijas veids</span><span class="sxs-lookup"><span data-stu-id="772ef-234">Worker Person Identification Type</span></span> | <span data-ttu-id="772ef-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="772ef-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="772ef-236">Darba kalendārs</span><span class="sxs-lookup"><span data-stu-id="772ef-236">Work Calendar</span></span> | <span data-ttu-id="772ef-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="772ef-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="772ef-238">Darba kalendāra diena</span><span class="sxs-lookup"><span data-stu-id="772ef-238">Work Calendar Day</span></span> | <span data-ttu-id="772ef-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="772ef-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="772ef-240">Brīvdienas darba kalendārā</span><span class="sxs-lookup"><span data-stu-id="772ef-240">Work Calendar Holiday</span></span> |<span data-ttu-id="772ef-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="772ef-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="772ef-242">Brīvdienu rinda darba kalendārā</span><span class="sxs-lookup"><span data-stu-id="772ef-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="772ef-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="772ef-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="772ef-244">Darba kalendāra laika intervāls</span><span class="sxs-lookup"><span data-stu-id="772ef-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="772ef-245">cdm_workcalendartimeinterval (nav iespējots pielāgoto lauku atbalsts)</span><span class="sxs-lookup"><span data-stu-id="772ef-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="772ef-246">Nodarbinātā bankas konts</span><span class="sxs-lookup"><span data-stu-id="772ef-246">Worker Bank Account</span></span> | <span data-ttu-id="772ef-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="772ef-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="772ef-248">Nodarbinātā iestatījumu entitījas</span><span class="sxs-lookup"><span data-stu-id="772ef-248">Worker setup entities</span></span>

| <span data-ttu-id="772ef-249">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="772ef-249">Name</span></span> | <span data-ttu-id="772ef-250">Elements</span><span class="sxs-lookup"><span data-stu-id="772ef-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="772ef-251">Veterāna statuss</span><span class="sxs-lookup"><span data-stu-id="772ef-251">Veteran Status</span></span> | <span data-ttu-id="772ef-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="772ef-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="772ef-253">Etniskā izcelsme</span><span class="sxs-lookup"><span data-stu-id="772ef-253">Ethnic Origin</span></span> | <span data-ttu-id="772ef-254">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="772ef-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="772ef-255">Iemesla kods</span><span class="sxs-lookup"><span data-stu-id="772ef-255">Reason Code</span></span> | <span data-ttu-id="772ef-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="772ef-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="772ef-257">Personas identifikācijas dokumenta izdevējiestāde</span><span class="sxs-lookup"><span data-stu-id="772ef-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="772ef-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="772ef-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="772ef-259">Kompetences entitījas</span><span class="sxs-lookup"><span data-stu-id="772ef-259">Competency entities</span></span>

| <span data-ttu-id="772ef-260">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="772ef-260">Name</span></span> | <span data-ttu-id="772ef-261">Elements</span><span class="sxs-lookup"><span data-stu-id="772ef-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="772ef-262">Prasmju veids</span><span class="sxs-lookup"><span data-stu-id="772ef-262">Skill Type</span></span> | <span data-ttu-id="772ef-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="772ef-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="772ef-264">Entitījas attiecību modeļi</span><span class="sxs-lookup"><span data-stu-id="772ef-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="772ef-265">Nodarbinātais</span><span class="sxs-lookup"><span data-stu-id="772ef-265">Worker</span></span>

![Nodarbinātais](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="772ef-267">Darbs un amats</span><span class="sxs-lookup"><span data-stu-id="772ef-267">Job and Job Position</span></span>

![Darbs un amats](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="772ef-269">Priekšrocības</span><span class="sxs-lookup"><span data-stu-id="772ef-269">Benefits</span></span>

![Priekšrocības](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="772ef-271">Kompensācija</span><span class="sxs-lookup"><span data-stu-id="772ef-271">Compensation</span></span>

![Kompensācija](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="772ef-273">Pamest</span><span class="sxs-lookup"><span data-stu-id="772ef-273">Leave</span></span>

![Pamest](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="772ef-275">Darba kalendārs</span><span class="sxs-lookup"><span data-stu-id="772ef-275">Work Calendar</span></span>

![Darba kalendārs](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="772ef-277">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="772ef-277">See also</span></span>

[<span data-ttu-id="772ef-278">Izvēlēties datu integrācijas tehnoloģiju</span><span class="sxs-lookup"><span data-stu-id="772ef-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="772ef-279">Common Data Service integrācijas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="772ef-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)