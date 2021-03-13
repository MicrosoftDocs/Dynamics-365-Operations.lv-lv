---
title: Dataverse tabulas
description: Microsoft Dynamics 365 Human Resources izmanto Dataverse, lai iespējotu paplašināšanas un integrācijas scenārijus.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: 2f075a8e96af55b1363d2d51db377c5b25c38775
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113446"
---
# <a name="dataverse-tables"></a><span data-ttu-id="d2ebb-103">Dataverse tabulas</span><span class="sxs-lookup"><span data-stu-id="d2ebb-103">Dataverse tables</span></span>

<span data-ttu-id="d2ebb-104">Microsoft Dynamics 365 Human Resources izmanto Dataverse, lai iespējotu paplašināšanas un integrācijas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="d2ebb-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="d2ebb-105">Human Resources elementi atbilst Dataverse tabulām.</span><span class="sxs-lookup"><span data-stu-id="d2ebb-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="d2ebb-106">Papildinformāciju par Dataverse (iepriekš Common Data Service) un terminoloģijas atjauninājumiem skatiet sadaļā [Kas ir Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="d2ebb-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="d2ebb-107">Šādas Dataverse tabulas ir pieejamas, pamatojoties uz Human Resources elementiem.</span><span class="sxs-lookup"><span data-stu-id="d2ebb-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="d2ebb-108">Atvieglojumu tabulas</span><span class="sxs-lookup"><span data-stu-id="d2ebb-108">Benefit tables</span></span>

| <span data-ttu-id="d2ebb-109">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="d2ebb-109">Name</span></span> | <span data-ttu-id="d2ebb-110">Tabula</span><span class="sxs-lookup"><span data-stu-id="d2ebb-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d2ebb-111">Atvieglojumu aprēķina biežums</span><span class="sxs-lookup"><span data-stu-id="d2ebb-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="d2ebb-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="d2ebb-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="d2ebb-113">Atvieglojumu aprēķina biežuma izmaksas periods</span><span class="sxs-lookup"><span data-stu-id="d2ebb-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="d2ebb-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="d2ebb-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="d2ebb-115">Atvieglojumu aprēķina likme</span><span class="sxs-lookup"><span data-stu-id="d2ebb-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="d2ebb-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="d2ebb-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="d2ebb-117">Atvieglojumu aprēķina likmes detalizēta informācija</span><span class="sxs-lookup"><span data-stu-id="d2ebb-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="d2ebb-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="d2ebb-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="d2ebb-119">Atvieglojumu opcija</span><span class="sxs-lookup"><span data-stu-id="d2ebb-119">Benefit Option</span></span> | <span data-ttu-id="d2ebb-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="d2ebb-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="d2ebb-121">Atvieglojumu plāns</span><span class="sxs-lookup"><span data-stu-id="d2ebb-121">Benefit Plan</span></span> | <span data-ttu-id="d2ebb-122">cdm_benefitplan (nav iespējots pielāgoto lauku atbalsts)</span><span class="sxs-lookup"><span data-stu-id="d2ebb-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="d2ebb-123">Atvieglojumu veids</span><span class="sxs-lookup"><span data-stu-id="d2ebb-123">Benefit Type</span></span> | <span data-ttu-id="d2ebb-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="d2ebb-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="d2ebb-125">Biznesa procesa uzdevumu tabulas</span><span class="sxs-lookup"><span data-stu-id="d2ebb-125">Business process tasks tables</span></span>

| <span data-ttu-id="d2ebb-126">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="d2ebb-126">Name</span></span> | <span data-ttu-id="d2ebb-127">Tabula</span><span class="sxs-lookup"><span data-stu-id="d2ebb-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d2ebb-128">Biznesa procesu kalendārs</span><span class="sxs-lookup"><span data-stu-id="d2ebb-128">Business Process Calendar</span></span> | <span data-ttu-id="d2ebb-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="d2ebb-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="d2ebb-130">Biznesa procesu grupu piešķire</span><span class="sxs-lookup"><span data-stu-id="d2ebb-130">Business Process Group Assignment</span></span> | <span data-ttu-id="d2ebb-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="d2ebb-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="d2ebb-132">Biznesa procesu bibliotēkas uzdevumu grupa</span><span class="sxs-lookup"><span data-stu-id="d2ebb-132">Business Process Library Task Group</span></span> | <span data-ttu-id="d2ebb-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="d2ebb-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="d2ebb-134">Biznesa procesu stadija</span><span class="sxs-lookup"><span data-stu-id="d2ebb-134">Business Process Stage</span></span> | <span data-ttu-id="d2ebb-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="d2ebb-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="d2ebb-136">Kontrolsaraksta veidnes galvene</span><span class="sxs-lookup"><span data-stu-id="d2ebb-136">Checklist Template Header</span></span> | <span data-ttu-id="d2ebb-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="d2ebb-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="d2ebb-138">Kontrolsaraksta veidnes uzdevums</span><span class="sxs-lookup"><span data-stu-id="d2ebb-138">Checklist Template Task</span></span> | <span data-ttu-id="d2ebb-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="d2ebb-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="d2ebb-140">Kompensāciju tabulas</span><span class="sxs-lookup"><span data-stu-id="d2ebb-140">Compensation tables</span></span>

| <span data-ttu-id="d2ebb-141">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="d2ebb-141">Name</span></span> | <span data-ttu-id="d2ebb-142">Tabula</span><span class="sxs-lookup"><span data-stu-id="d2ebb-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d2ebb-143">Atlīdzības fiksētais plāns</span><span class="sxs-lookup"><span data-stu-id="d2ebb-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="d2ebb-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="d2ebb-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="d2ebb-145">Atlīdzības režģis</span><span class="sxs-lookup"><span data-stu-id="d2ebb-145">Compensation Grid</span></span> | <span data-ttu-id="d2ebb-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="d2ebb-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="d2ebb-147">Atlīdzības līmenis</span><span class="sxs-lookup"><span data-stu-id="d2ebb-147">Compensation Level</span></span> | <span data-ttu-id="d2ebb-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="d2ebb-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="d2ebb-149">Atlīdzības izmaksas biežums</span><span class="sxs-lookup"><span data-stu-id="d2ebb-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="d2ebb-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="d2ebb-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="d2ebb-151">Atlīdzības raksturojuma punktu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d2ebb-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="d2ebb-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="d2ebb-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="d2ebb-153">Atlīdzības raksturojuma punktu iestatīšanas līnija</span><span class="sxs-lookup"><span data-stu-id="d2ebb-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="d2ebb-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="d2ebb-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="d2ebb-155">Atlīdzības reģions</span><span class="sxs-lookup"><span data-stu-id="d2ebb-155">Compensation Region</span></span> | <span data-ttu-id="d2ebb-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="d2ebb-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="d2ebb-157">Atlīdzības struktūra</span><span class="sxs-lookup"><span data-stu-id="d2ebb-157">Compensation Structure</span></span> | <span data-ttu-id="d2ebb-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="d2ebb-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="d2ebb-159">Atlīdzības mainīgais plāns</span><span class="sxs-lookup"><span data-stu-id="d2ebb-159">Compensation Variable Plan</span></span> | <span data-ttu-id="d2ebb-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="d2ebb-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="d2ebb-161">Atlīdzības mainīgā plāna līmenis</span><span class="sxs-lookup"><span data-stu-id="d2ebb-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="d2ebb-162">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="d2ebb-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="d2ebb-163">Atlīdzības mainīgā plāna tips</span><span class="sxs-lookup"><span data-stu-id="d2ebb-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="d2ebb-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="d2ebb-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="d2ebb-165">Fiksētas atlīdzības notikums</span><span class="sxs-lookup"><span data-stu-id="d2ebb-165">Fixed Compensation Event</span></span> | <span data-ttu-id="d2ebb-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="d2ebb-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="d2ebb-167">Izmaksu noteikums</span><span class="sxs-lookup"><span data-stu-id="d2ebb-167">Vesting Rule</span></span> | <span data-ttu-id="d2ebb-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="d2ebb-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="d2ebb-169">Nodarbinātā fiksētā atlīdzība</span><span class="sxs-lookup"><span data-stu-id="d2ebb-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="d2ebb-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="d2ebb-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="d2ebb-171">Organizācijas tabulas</span><span class="sxs-lookup"><span data-stu-id="d2ebb-171">Organization tables</span></span>

| <span data-ttu-id="d2ebb-172">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="d2ebb-172">Name</span></span> | <span data-ttu-id="d2ebb-173">Tabula</span><span class="sxs-lookup"><span data-stu-id="d2ebb-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d2ebb-174">Nodaļa</span><span class="sxs-lookup"><span data-stu-id="d2ebb-174">Department</span></span> | <span data-ttu-id="d2ebb-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="d2ebb-175">cdm_department</span></span> |
| <span data-ttu-id="d2ebb-176">Nodarbinātība</span><span class="sxs-lookup"><span data-stu-id="d2ebb-176">Employment</span></span> | <span data-ttu-id="d2ebb-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="d2ebb-177">cdm_employment</span></span> |
| <span data-ttu-id="d2ebb-178">Uzņēmums</span><span class="sxs-lookup"><span data-stu-id="d2ebb-178">Company</span></span> | <span data-ttu-id="d2ebb-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="d2ebb-179">cdm_company</span></span> |
| <span data-ttu-id="d2ebb-180">Darbs</span><span class="sxs-lookup"><span data-stu-id="d2ebb-180">Job</span></span> | <span data-ttu-id="d2ebb-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="d2ebb-181">cdm_job</span></span> |
| <span data-ttu-id="d2ebb-182">Darba funkcija</span><span class="sxs-lookup"><span data-stu-id="d2ebb-182">Job Function</span></span> | <span data-ttu-id="d2ebb-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="d2ebb-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="d2ebb-184">Amats</span><span class="sxs-lookup"><span data-stu-id="d2ebb-184">Job Position</span></span> | <span data-ttu-id="d2ebb-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="d2ebb-185">cdm_jobposition</span></span> |
| <span data-ttu-id="d2ebb-186">Amata veids</span><span class="sxs-lookup"><span data-stu-id="d2ebb-186">Position Type</span></span> | <span data-ttu-id="d2ebb-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="d2ebb-187">cdm_positiontype</span></span> |
| <span data-ttu-id="d2ebb-188">Amatā nodarbinātā piešķire</span><span class="sxs-lookup"><span data-stu-id="d2ebb-188">Position Worker Assignment</span></span> | <span data-ttu-id="d2ebb-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="d2ebb-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="d2ebb-190">Amata dimensija</span><span class="sxs-lookup"><span data-stu-id="d2ebb-190">Job Position Dimension</span></span> | <span data-ttu-id="d2ebb-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="d2ebb-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="d2ebb-192">Darba tips</span><span class="sxs-lookup"><span data-stu-id="d2ebb-192">Job Type</span></span> | <span data-ttu-id="d2ebb-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="d2ebb-193">cdm_jobtype</span></span> |
| <span data-ttu-id="d2ebb-194">Valoda</span><span class="sxs-lookup"><span data-stu-id="d2ebb-194">Language</span></span> | <span data-ttu-id="d2ebb-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="d2ebb-195">cdm_language</span></span> |
| <span data-ttu-id="d2ebb-196">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="d2ebb-196">Title</span></span> | <span data-ttu-id="d2ebb-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="d2ebb-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="d2ebb-198">Finanšu dimensijas **Amata veidam**, **Amata darbinieka piešķirei** un **Nodarbinātībai** pakalpojumam Dataverse nodrošina vienvirziena integrāciju.</span><span class="sxs-lookup"><span data-stu-id="d2ebb-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="d2ebb-199">Finanšu dimensiju atjauninājumi pašlaik nesinhronizējas no Dataverse uz personāla vadības resursiem.</span><span class="sxs-lookup"><span data-stu-id="d2ebb-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="d2ebb-200">Atvaļinājumu un prombūtnes tabulas</span><span class="sxs-lookup"><span data-stu-id="d2ebb-200">Leave and absence tables</span></span>

| <span data-ttu-id="d2ebb-201">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="d2ebb-201">Name</span></span> | <span data-ttu-id="d2ebb-202">Tabula</span><span class="sxs-lookup"><span data-stu-id="d2ebb-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d2ebb-203">Atvaļinājuma bankas transakcija</span><span class="sxs-lookup"><span data-stu-id="d2ebb-203">Leave Bank Transaction</span></span> | <span data-ttu-id="d2ebb-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="d2ebb-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="d2ebb-205">Atvaļinājuma reģistrācija</span><span class="sxs-lookup"><span data-stu-id="d2ebb-205">Leave Enrollment</span></span> | <span data-ttu-id="d2ebb-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="d2ebb-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="d2ebb-207">Atvaļinājumu plāns</span><span class="sxs-lookup"><span data-stu-id="d2ebb-207">Leave Plan</span></span> | <span data-ttu-id="d2ebb-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="d2ebb-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="d2ebb-209">Atvaļinājuma pieprasījums</span><span class="sxs-lookup"><span data-stu-id="d2ebb-209">Leave Request</span></span> | <span data-ttu-id="d2ebb-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="d2ebb-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="d2ebb-211">Atvaļinājuma pieprasījuma informācija</span><span class="sxs-lookup"><span data-stu-id="d2ebb-211">Leave Request Detail</span></span> | <span data-ttu-id="d2ebb-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="d2ebb-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="d2ebb-213">Atvaļinājuma tips</span><span class="sxs-lookup"><span data-stu-id="d2ebb-213">Leave Type</span></span> | <span data-ttu-id="d2ebb-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="d2ebb-214">cdm_leavetype</span></span> |
| <span data-ttu-id="d2ebb-215">Atvaļinājuma veida iemesla kods</span><span class="sxs-lookup"><span data-stu-id="d2ebb-215">Leave Type Reason Code</span></span> | <span data-ttu-id="d2ebb-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="d2ebb-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="d2ebb-217">Algu tabulas</span><span class="sxs-lookup"><span data-stu-id="d2ebb-217">Payroll tables</span></span>

| <span data-ttu-id="d2ebb-218">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="d2ebb-218">Name</span></span> | <span data-ttu-id="d2ebb-219">Tabula</span><span class="sxs-lookup"><span data-stu-id="d2ebb-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d2ebb-220">Apmaksas cikls</span><span class="sxs-lookup"><span data-stu-id="d2ebb-220">Pay Cycle</span></span> | <span data-ttu-id="d2ebb-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="d2ebb-221">cdm_paycycle</span></span> |
| <span data-ttu-id="d2ebb-222">Apmaksas periods</span><span class="sxs-lookup"><span data-stu-id="d2ebb-222">Pay Period</span></span> | <span data-ttu-id="d2ebb-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="d2ebb-223">cdm_payperiod</span></span> |
| <span data-ttu-id="d2ebb-224">Algas ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="d2ebb-224">Payroll Earning Code</span></span> | <span data-ttu-id="d2ebb-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="d2ebb-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="d2ebb-226">Bankas konta izdevumi</span><span class="sxs-lookup"><span data-stu-id="d2ebb-226">Bank Account Disbursement</span></span> | <span data-ttu-id="d2ebb-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="d2ebb-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="d2ebb-228">Nodokļu reģions</span><span class="sxs-lookup"><span data-stu-id="d2ebb-228">Tax Region</span></span> | <span data-ttu-id="d2ebb-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="d2ebb-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="d2ebb-230">Darbinieku tabulas</span><span class="sxs-lookup"><span data-stu-id="d2ebb-230">Worker tables</span></span>

| <span data-ttu-id="d2ebb-231">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="d2ebb-231">Name</span></span> | <span data-ttu-id="d2ebb-232">Tabula</span><span class="sxs-lookup"><span data-stu-id="d2ebb-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d2ebb-233">Darbinieks</span><span class="sxs-lookup"><span data-stu-id="d2ebb-233">Worker</span></span> | <span data-ttu-id="d2ebb-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="d2ebb-234">cdm_worker</span></span> |
| <span data-ttu-id="d2ebb-235">Nodarbinātā adrese</span><span class="sxs-lookup"><span data-stu-id="d2ebb-235">Worker Address</span></span> | <span data-ttu-id="d2ebb-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="d2ebb-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="d2ebb-237">Nodarbinātā personas dati</span><span class="sxs-lookup"><span data-stu-id="d2ebb-237">Worker Personal Detail</span></span> | <span data-ttu-id="d2ebb-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="d2ebb-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="d2ebb-239">Nodarbinātās personas identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="d2ebb-239">Worker Person Identification Number</span></span> | <span data-ttu-id="d2ebb-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="d2ebb-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="d2ebb-241">Nodarbinātās personas identifikācijas veids</span><span class="sxs-lookup"><span data-stu-id="d2ebb-241">Worker Person Identification Type</span></span> | <span data-ttu-id="d2ebb-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="d2ebb-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="d2ebb-243">Darba kalendārs</span><span class="sxs-lookup"><span data-stu-id="d2ebb-243">Work Calendar</span></span> | <span data-ttu-id="d2ebb-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="d2ebb-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="d2ebb-245">Darba kalendāra diena</span><span class="sxs-lookup"><span data-stu-id="d2ebb-245">Work Calendar Day</span></span> | <span data-ttu-id="d2ebb-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="d2ebb-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="d2ebb-247">Brīvdienas darba kalendārā</span><span class="sxs-lookup"><span data-stu-id="d2ebb-247">Work Calendar Holiday</span></span> |<span data-ttu-id="d2ebb-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="d2ebb-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="d2ebb-249">Brīvdienu rinda darba kalendārā</span><span class="sxs-lookup"><span data-stu-id="d2ebb-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="d2ebb-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="d2ebb-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="d2ebb-251">Darba kalendāra laika intervāls</span><span class="sxs-lookup"><span data-stu-id="d2ebb-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="d2ebb-252">cdm_workcalendartimeinterval (nav iespējots pielāgoto lauku atbalsts)</span><span class="sxs-lookup"><span data-stu-id="d2ebb-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="d2ebb-253">Nodarbinātā bankas konts</span><span class="sxs-lookup"><span data-stu-id="d2ebb-253">Worker Bank Account</span></span> | <span data-ttu-id="d2ebb-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="d2ebb-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="d2ebb-255">Darbinieka iestatījumu tabulas</span><span class="sxs-lookup"><span data-stu-id="d2ebb-255">Worker setup tables</span></span>

| <span data-ttu-id="d2ebb-256">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="d2ebb-256">Name</span></span> | <span data-ttu-id="d2ebb-257">Tabula</span><span class="sxs-lookup"><span data-stu-id="d2ebb-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d2ebb-258">Veterāna statuss</span><span class="sxs-lookup"><span data-stu-id="d2ebb-258">Veteran Status</span></span> | <span data-ttu-id="d2ebb-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="d2ebb-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="d2ebb-260">Etniskā izcelsme</span><span class="sxs-lookup"><span data-stu-id="d2ebb-260">Ethnic Origin</span></span> | <span data-ttu-id="d2ebb-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="d2ebb-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="d2ebb-262">Iemesla kods</span><span class="sxs-lookup"><span data-stu-id="d2ebb-262">Reason Code</span></span> | <span data-ttu-id="d2ebb-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="d2ebb-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="d2ebb-264">Personas identifikācijas izsniedzēja iestāde</span><span class="sxs-lookup"><span data-stu-id="d2ebb-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="d2ebb-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="d2ebb-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="d2ebb-266">Kompetenču tabulas</span><span class="sxs-lookup"><span data-stu-id="d2ebb-266">Competency tables</span></span>

| <span data-ttu-id="d2ebb-267">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="d2ebb-267">Name</span></span> | <span data-ttu-id="d2ebb-268">Tabula</span><span class="sxs-lookup"><span data-stu-id="d2ebb-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d2ebb-269">Prasmju tips</span><span class="sxs-lookup"><span data-stu-id="d2ebb-269">Skill Type</span></span> | <span data-ttu-id="d2ebb-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="d2ebb-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="d2ebb-271">Tabulas attiecību modeļi</span><span class="sxs-lookup"><span data-stu-id="d2ebb-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="d2ebb-272">Darbinieks</span><span class="sxs-lookup"><span data-stu-id="d2ebb-272">Worker</span></span>

![Darbinieks](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="d2ebb-274">Darbs un amats</span><span class="sxs-lookup"><span data-stu-id="d2ebb-274">Job and Job Position</span></span>

![Darbs un amats](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="d2ebb-276">Priekšrocības</span><span class="sxs-lookup"><span data-stu-id="d2ebb-276">Benefits</span></span>

![Priekšrocības](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="d2ebb-278">Kompensācija</span><span class="sxs-lookup"><span data-stu-id="d2ebb-278">Compensation</span></span>

![Kompensācija](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="d2ebb-280">Pamest</span><span class="sxs-lookup"><span data-stu-id="d2ebb-280">Leave</span></span>

![Pamest](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="d2ebb-282">Darba kalendārs</span><span class="sxs-lookup"><span data-stu-id="d2ebb-282">Work Calendar</span></span>

![Darba kalendārs](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="d2ebb-284">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="d2ebb-284">See also</span></span>

[<span data-ttu-id="d2ebb-285">Izvēlēties datu integrācijas tehnoloģiju</span><span class="sxs-lookup"><span data-stu-id="d2ebb-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="d2ebb-286">Dataverse integrācijas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="d2ebb-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="d2ebb-287">Dataverse virtuālo tabulu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="d2ebb-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="d2ebb-288">Human Resources virtuālās tabulas: Bieži uzdotie jautājumi</span><span class="sxs-lookup"><span data-stu-id="d2ebb-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="d2ebb-289">Kas ir Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="d2ebb-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="d2ebb-290">Terminoloģijas atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="d2ebb-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
