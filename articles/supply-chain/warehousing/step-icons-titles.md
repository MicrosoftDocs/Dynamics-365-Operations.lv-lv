---
title: Darbību ikonu un nosaukumu piešķiršana Warehouse Management mobilajai programmai
description: Šajā tēmā ir aprakstīts, kā piešķirt darbību ikonas un virsrakstus jaunām vai pielāgotām uzdevumu plūsmām Warehouse Management mobilajai lietojumprogrammai.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049368"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="9f544-103">Darbību ikonu un nosaukumu piešķiršana Warehouse Management mobilajai programmai</span><span class="sxs-lookup"><span data-stu-id="9f544-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f544-104">Šajā tēmā ir aprakstīts, kā piešķirt darbību ikonas un virsrakstus jaunām vai pielāgotām uzdevumu plūsmām Warehouse Management mobilajai lietojumprogrammai.</span><span class="sxs-lookup"><span data-stu-id="9f544-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="9f544-105">Nākamajās ilustrācijās ir parādīts, kā darbību ikonas un virsraksti tiek parādīti Warehouse Management mobilajā lietojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="9f544-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="9f544-106">![Darbību ikonas un virsraksta piemērs Warehouse Management mobilajā lietojumprogrammā](media/step-icon-example.png "Darbību ikonas un virsraksta piemērs Warehouse Management mobilajā lietojumprogrammā")</span><span class="sxs-lookup"><span data-stu-id="9f544-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="9f544-107">Šī līdzekļa ieslēgšana sistēmā</span><span class="sxs-lookup"><span data-stu-id="9f544-107">Turn on this feature in your system</span></span>

<span data-ttu-id="9f544-108">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="9f544-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="9f544-109">Administratori var izmantot [Funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="9f544-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="9f544-110">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="9f544-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9f544-111">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="9f544-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="9f544-112">**Līdzekļa nosaukums:** *Lietotāja iestatījumi, ikonas un darbību nosaukumi jaunajai noliktavas programmai*</span><span class="sxs-lookup"><span data-stu-id="9f544-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="9f544-113">Standarta darbību ID, klases un ikonas</span><span class="sxs-lookup"><span data-stu-id="9f544-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="9f544-114">Katra darbība uzdevumu plūsmā tiek identificēta ar darbības ID, un katram darbības ID ir atbilstoša darbības klase.</span><span class="sxs-lookup"><span data-stu-id="9f544-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="9f544-115">Darbības ikona un virsraksts ir norādīti katrā darbības klasē.</span><span class="sxs-lookup"><span data-stu-id="9f544-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="9f544-116">Darbību ID un darbības klases</span><span class="sxs-lookup"><span data-stu-id="9f544-116">Step IDs and step classes</span></span>

<span data-ttu-id="9f544-117">Šajā tabulā ir uzskaitīti visi darbības ID, kas pašlaik ir pieejami, un tai atbilstoša darbības klase.</span><span class="sxs-lookup"><span data-stu-id="9f544-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="9f544-118">Primārā ievades lauka kontroles nosaukums tiek izmantots kā darbības ID.</span><span class="sxs-lookup"><span data-stu-id="9f544-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="9f544-119">Piemēru, kurā parādīts, kā tiek lietoti šie darbības ID un klases, skatiet `WHSMobileAppStepInfoBuilder.stepId()` metodes ieviešanas sadaļā [Piemērs: Darbību ikonu un nosaukumu piešķiršana pielāgotajai plūsmai](#example) tālāk šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="9f544-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="9f544-120">Darbības ID</span><span class="sxs-lookup"><span data-stu-id="9f544-120">Step ID</span></span> | <span data-ttu-id="9f544-121">Darbības klase</span><span class="sxs-lookup"><span data-stu-id="9f544-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="9f544-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="9f544-122">BatchDisposition</span></span> | <span data-ttu-id="9f544-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="9f544-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="9f544-124">Pārvadātājs</span><span class="sxs-lookup"><span data-stu-id="9f544-124">Carrier</span></span> | <span data-ttu-id="9f544-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="9f544-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="9f544-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="9f544-126">CatchWeight</span></span> | <span data-ttu-id="9f544-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="9f544-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="9f544-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="9f544-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="9f544-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="9f544-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="9f544-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="9f544-130">CatchWeightTag</span></span> | <span data-ttu-id="9f544-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="9f544-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="9f544-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="9f544-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="9f544-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="9f544-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="9f544-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="9f544-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="9f544-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="9f544-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="9f544-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="9f544-136">CheckDigit</span></span> | <span data-ttu-id="9f544-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="9f544-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="9f544-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="9f544-138">ClusterId</span></span> | <span data-ttu-id="9f544-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="9f544-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="9f544-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="9f544-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="9f544-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="9f544-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="9f544-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="9f544-142">ClusterPosition</span></span> | <span data-ttu-id="9f544-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="9f544-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="9f544-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="9f544-144">ConfigId</span></span> | <span data-ttu-id="9f544-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="9f544-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="9f544-146">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="9f544-146">Confirmation</span></span> | <span data-ttu-id="9f544-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="9f544-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="9f544-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="9f544-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="9f544-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="9f544-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="9f544-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="9f544-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="9f544-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="9f544-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="9f544-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="9f544-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="9f544-154">ContainerType</span></span> | <span data-ttu-id="9f544-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="9f544-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="9f544-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="9f544-156">CountingReasonCode</span></span> | <span data-ttu-id="9f544-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="9f544-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="9f544-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="9f544-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="9f544-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="9f544-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="9f544-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="9f544-160">CycleCountQty1</span></span> | <span data-ttu-id="9f544-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="9f544-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="9f544-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="9f544-162">CycleCountQty2</span></span> | <span data-ttu-id="9f544-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="9f544-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="9f544-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="9f544-164">CycleCountQty3</span></span> | <span data-ttu-id="9f544-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="9f544-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="9f544-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="9f544-166">CycleCountQty4</span></span> | <span data-ttu-id="9f544-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="9f544-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="9f544-168">Atgriešanas metode</span><span class="sxs-lookup"><span data-stu-id="9f544-168">Disposition</span></span> | <span data-ttu-id="9f544-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="9f544-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="9f544-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="9f544-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="9f544-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="9f544-172">DriverCheckInId</span></span> | <span data-ttu-id="9f544-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="9f544-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="9f544-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="9f544-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="9f544-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="9f544-176">DriverCheckOutId</span></span> | <span data-ttu-id="9f544-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="9f544-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="9f544-178">ExpDate</span><span class="sxs-lookup"><span data-stu-id="9f544-178">ExpDate</span></span> | <span data-ttu-id="9f544-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="9f544-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="9f544-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="9f544-180">FromBatchDisposition</span></span> | <span data-ttu-id="9f544-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="9f544-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="9f544-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="9f544-182">FromInventoryStatus</span></span> | <span data-ttu-id="9f544-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="9f544-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="9f544-184">FullQty</span><span class="sxs-lookup"><span data-stu-id="9f544-184">FullQty</span></span> | <span data-ttu-id="9f544-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="9f544-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="9f544-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="9f544-186">InboundPut</span></span> | <span data-ttu-id="9f544-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="9f544-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="9f544-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="9f544-188">InventBatchId</span></span> | <span data-ttu-id="9f544-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="9f544-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="9f544-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="9f544-190">InventColorId</span></span> | <span data-ttu-id="9f544-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="9f544-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="9f544-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="9f544-192">InventLocation</span></span> | <span data-ttu-id="9f544-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="9f544-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="9f544-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="9f544-194">InventLocationId</span></span> | <span data-ttu-id="9f544-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="9f544-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="9f544-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="9f544-196">InventSerialId</span></span> | <span data-ttu-id="9f544-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="9f544-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="9f544-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="9f544-198">InventSizeId</span></span> | <span data-ttu-id="9f544-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="9f544-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="9f544-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="9f544-200">InventStatusId</span></span> | <span data-ttu-id="9f544-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="9f544-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="9f544-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="9f544-202">InventStyleId</span></span> | <span data-ttu-id="9f544-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="9f544-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="9f544-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="9f544-204">InventVersionId</span></span> | <span data-ttu-id="9f544-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="9f544-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="9f544-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="9f544-206">ItemId</span></span> | <span data-ttu-id="9f544-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="9f544-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="9f544-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="9f544-208">ITMContainerID</span></span> | <span data-ttu-id="9f544-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="9f544-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="9f544-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="9f544-210">ITMShipmentID</span></span> | <span data-ttu-id="9f544-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="9f544-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="9f544-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="9f544-212">KanbanCardId</span></span> | <span data-ttu-id="9f544-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="9f544-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="9f544-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="9f544-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="9f544-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="9f544-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="9f544-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="9f544-216">KanbanOrCardId</span></span> | <span data-ttu-id="9f544-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="9f544-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="9f544-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="9f544-218">LicensePlateId</span></span> | <span data-ttu-id="9f544-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="9f544-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="9f544-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="9f544-220">LoadId</span></span> | <span data-ttu-id="9f544-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="9f544-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="9f544-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="9f544-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="9f544-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="9f544-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="9f544-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="9f544-224">LocOrLP</span></span> | <span data-ttu-id="9f544-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="9f544-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="9f544-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="9f544-226">LocOrLP_From</span></span> | <span data-ttu-id="9f544-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="9f544-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="9f544-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="9f544-228">LocOrLP_To</span></span> | <span data-ttu-id="9f544-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="9f544-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="9f544-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="9f544-230">LocOrLPCheck</span></span> | <span data-ttu-id="9f544-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="9f544-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="9f544-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="9f544-232">LocVerification</span></span> | <span data-ttu-id="9f544-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="9f544-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="9f544-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="9f544-234">LPAdjustIn</span></span> | <span data-ttu-id="9f544-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="9f544-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="9f544-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="9f544-236">LPBreakChildLP</span></span> | <span data-ttu-id="9f544-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="9f544-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="9f544-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="9f544-238">LPBreakParentLP</span></span> | <span data-ttu-id="9f544-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="9f544-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="9f544-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="9f544-240">LPBuildChildLP</span></span> | <span data-ttu-id="9f544-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="9f544-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="9f544-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="9f544-242">LPBuildParentLP</span></span> | <span data-ttu-id="9f544-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="9f544-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="9f544-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="9f544-244">LPVerification</span></span> | <span data-ttu-id="9f544-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="9f544-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="9f544-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="9f544-246">MergeContainerId</span></span> | <span data-ttu-id="9f544-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="9f544-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="9f544-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="9f544-248">MixedLPLineNum</span></span> | <span data-ttu-id="9f544-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="9f544-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="9f544-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="9f544-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="9f544-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="9f544-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="9f544-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="9f544-252">MovementConfirmCancel</span></span> | <span data-ttu-id="9f544-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="9f544-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="9f544-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="9f544-254">NewCaptureWeight</span></span> | <span data-ttu-id="9f544-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="9f544-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="9f544-256">NewQty</span><span class="sxs-lookup"><span data-stu-id="9f544-256">NewQty</span></span> | <span data-ttu-id="9f544-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="9f544-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="9f544-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="9f544-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="9f544-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="9f544-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="9f544-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="9f544-260">OutboundPut</span></span> | <span data-ttu-id="9f544-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="9f544-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="9f544-262">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="9f544-262">OutboundWeight</span></span> | <span data-ttu-id="9f544-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="9f544-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="9f544-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="9f544-264">OverridePutNewLocation</span></span> | <span data-ttu-id="9f544-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="9f544-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="9f544-266">PieceByPieceConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="9f544-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="9f544-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="9f544-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="9f544-268">POLineNum</span></span> | <span data-ttu-id="9f544-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="9f544-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="9f544-270">PONum</span><span class="sxs-lookup"><span data-stu-id="9f544-270">PONum</span></span> | <span data-ttu-id="9f544-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="9f544-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="9f544-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="9f544-272">PositionFull</span></span> | <span data-ttu-id="9f544-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="9f544-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="9f544-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="9f544-274">PositionFullQty</span></span> | <span data-ttu-id="9f544-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="9f544-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="9f544-276">Saturs</span><span class="sxs-lookup"><span data-stu-id="9f544-276">Potency</span></span> | <span data-ttu-id="9f544-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="9f544-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="9f544-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="9f544-278">PrinterName</span></span> | <span data-ttu-id="9f544-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="9f544-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="9f544-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="9f544-280">ProdId</span></span> | <span data-ttu-id="9f544-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="9f544-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="9f544-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="9f544-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="9f544-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-284">ProductConfirmation</span></span> | <span data-ttu-id="9f544-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="9f544-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="9f544-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="9f544-288">Izvietot</span><span class="sxs-lookup"><span data-stu-id="9f544-288">Put</span></span> | <span data-ttu-id="9f544-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="9f544-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="9f544-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="9f544-290">PutawayClusterId</span></span> | <span data-ttu-id="9f544-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="9f544-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="9f544-292">Daudz.</span><span class="sxs-lookup"><span data-stu-id="9f544-292">Qty</span></span> | <span data-ttu-id="9f544-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="9f544-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="9f544-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="9f544-294">QtyAdjust</span></span> | <span data-ttu-id="9f544-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="9f544-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="9f544-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="9f544-296">QtyShort</span></span> | <span data-ttu-id="9f544-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="9f544-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="9f544-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="9f544-298">QtyToConsume</span></span> | <span data-ttu-id="9f544-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="9f544-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="9f544-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="9f544-300">QtyToPick</span></span> | <span data-ttu-id="9f544-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="9f544-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="9f544-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="9f544-302">QtyToPut</span></span> | <span data-ttu-id="9f544-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="9f544-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="9f544-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="9f544-304">QtyToScrap</span></span> | <span data-ttu-id="9f544-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="9f544-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="9f544-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="9f544-306">QtyVerification</span></span> | <span data-ttu-id="9f544-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="9f544-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="9f544-308">QtyWithScanningLimit</span><span class="sxs-lookup"><span data-stu-id="9f544-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="9f544-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="9f544-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="9f544-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="9f544-310">ReasonString</span></span> | <span data-ttu-id="9f544-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="9f544-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="9f544-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="9f544-312">RecvLocationId</span></span> | <span data-ttu-id="9f544-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="9f544-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="9f544-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="9f544-314">RemoveContainerId</span></span> | <span data-ttu-id="9f544-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="9f544-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="9f544-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="9f544-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="9f544-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="9f544-318">RMANum</span></span> | <span data-ttu-id="9f544-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="9f544-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="9f544-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="9f544-320">ShortPickReason</span></span> | <span data-ttu-id="9f544-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="9f544-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="9f544-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="9f544-322">SortConOrLP</span></span> | <span data-ttu-id="9f544-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="9f544-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="9f544-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="9f544-324">SortLicensePlateId</span></span> | <span data-ttu-id="9f544-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="9f544-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="9f544-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="9f544-326">SortPositionId</span></span> | <span data-ttu-id="9f544-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="9f544-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="9f544-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="9f544-328">SortVerification</span></span> | <span data-ttu-id="9f544-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="9f544-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="9f544-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="9f544-330">StartLocationId</span></span> | <span data-ttu-id="9f544-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="9f544-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="9f544-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="9f544-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="9f544-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="9f544-334">TargetLicensePlateId</span></span> | <span data-ttu-id="9f544-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="9f544-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="9f544-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="9f544-336">TOLineNum</span></span> | <span data-ttu-id="9f544-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="9f544-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="9f544-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="9f544-338">ToLocation</span></span> | <span data-ttu-id="9f544-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="9f544-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="9f544-340">TONum</span><span class="sxs-lookup"><span data-stu-id="9f544-340">TONum</span></span> | <span data-ttu-id="9f544-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="9f544-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="9f544-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="9f544-342">ToWarehouse</span></span> | <span data-ttu-id="9f544-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="9f544-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="9f544-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="9f544-344">TransportLoadId</span></span> | <span data-ttu-id="9f544-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="9f544-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="9f544-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="9f544-346">WaveLabelId</span></span> | <span data-ttu-id="9f544-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="9f544-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="9f544-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="9f544-348">WaveLblQty</span></span> | <span data-ttu-id="9f544-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="9f544-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="9f544-350">Lielums</span><span class="sxs-lookup"><span data-stu-id="9f544-350">Weight</span></span> | <span data-ttu-id="9f544-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="9f544-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="9f544-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="9f544-352">WeightToConsume</span></span> | <span data-ttu-id="9f544-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="9f544-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="9f544-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="9f544-354">WHSAdjustmentType</span></span> | <span data-ttu-id="9f544-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="9f544-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="9f544-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="9f544-356">WHSReceivingException</span></span> | <span data-ttu-id="9f544-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="9f544-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="9f544-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="9f544-358">WHSWorkException</span></span> | <span data-ttu-id="9f544-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="9f544-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="9f544-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="9f544-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="9f544-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="9f544-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="9f544-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="9f544-362">WMSLocationId</span></span> | <span data-ttu-id="9f544-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="9f544-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="9f544-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="9f544-364">WorkId</span></span> | <span data-ttu-id="9f544-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="9f544-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="9f544-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="9f544-366">WorkIdToCancel</span></span> | <span data-ttu-id="9f544-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="9f544-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="9f544-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="9f544-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="9f544-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="9f544-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="9f544-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="9f544-370">WorkPoolId</span></span> | <span data-ttu-id="9f544-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="9f544-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="9f544-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="9f544-372">ZoneId</span></span> | <span data-ttu-id="9f544-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="9f544-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="9f544-374">Pieejamās darbību ikonas</span><span class="sxs-lookup"><span data-stu-id="9f544-374">Available step icons</span></span>

<span data-ttu-id="9f544-375">Sistēmā ir ietverta standarta darbību ikonu kolekcija, ko varat izmantot arī pielāgotajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="9f544-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="9f544-376">Šobrīd nevar augšupielādēt pielāgotās darbību ikonas.</span><span class="sxs-lookup"><span data-stu-id="9f544-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="9f544-377">Tāpēc vienmēr jāatlasa viena no standarta darbību ikonām.</span><span class="sxs-lookup"><span data-stu-id="9f544-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="9f544-378">Šajā tabulā parādīta katra standarta darbības ikona, kas pašreiz ir pieejama, un tās nosaukums.</span><span class="sxs-lookup"><span data-stu-id="9f544-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Par darbības ikonu"><br><span data-ttu-id="9f544-380">Par programmu</span><span class="sxs-lookup"><span data-stu-id="9f544-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Pievienot numura zīmi vai krājuma darbības ikonu"><br><span data-ttu-id="9f544-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="9f544-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Partijas atgriešanas darbības ikona"><br><span data-ttu-id="9f544-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="9f544-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Pārvadātāja darbības ikona"><br><span data-ttu-id="9f544-386">Pārvadātājs</span><span class="sxs-lookup"><span data-stu-id="9f544-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Pieļaujamā svara etiķetes darbības ikona"><br><span data-ttu-id="9f544-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="9f544-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Pieļaujamā svara etiķetes svara darbības ikona"><br><span data-ttu-id="9f544-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="9f544-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Kontrolcipara darbības ikona"><br><span data-ttu-id="9f544-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="9f544-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Ierakstīšanās vai izrakstīšanas ID darbības ikona"><br><span data-ttu-id="9f544-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="9f544-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Pakārtotās numura zīmes darbības ikona"><br><span data-ttu-id="9f544-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="9f544-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Klastera ID darbības ikona"><br><span data-ttu-id="9f544-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="9f544-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Klastera pozīcijas darbības ikona"><br><span data-ttu-id="9f544-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="9f544-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Konfigurācijas ID darbības ikona"><br><span data-ttu-id="9f544-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="9f544-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Konfigurētā lauka darbības ikona"><br><span data-ttu-id="9f544-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="9f544-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Con vai LP darbības ikona"><br><span data-ttu-id="9f544-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="9f544-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Konsolidēt no numura zīmes ID darbības ikona"><br><span data-ttu-id="9f544-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="9f544-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Konsolidēt uz numura zīmes ID darbības ikona"><br><span data-ttu-id="9f544-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="9f544-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Konteinera tipa darbības ikona"><br><span data-ttu-id="9f544-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="9f544-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Uzskaites darbības ikona"><br><span data-ttu-id="9f544-414">Inventarizācija</span><span class="sxs-lookup"><span data-stu-id="9f544-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Inventarizācijas iemesla koda darbības ikona"><br><span data-ttu-id="9f544-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="9f544-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Izcelsmes valsts koda darbības ikona"><br><span data-ttu-id="9f544-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="9f544-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Atgriešanas darbības ikona"><br><span data-ttu-id="9f544-420">Atgriešanas metode</span><span class="sxs-lookup"><span data-stu-id="9f544-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Pabeigtā darbības ikona"><br><span data-ttu-id="9f544-422">Pabeigts</span><span class="sxs-lookup"><span data-stu-id="9f544-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Transportlīdzekļa vadītāja reģistrēšanās apstiprinājuma darbības ikona"><br><span data-ttu-id="9f544-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Transportlīdzekļa vadītāja pierakstīšanās ID darbības ikona"><br><span data-ttu-id="9f544-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="9f544-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Transportlīdzekļa vadītāja izrakstīšanās ID darbības ikona"><br><span data-ttu-id="9f544-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="9f544-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Beigu datuma darbības ikona"><br><span data-ttu-id="9f544-430">ExpDate</span><span class="sxs-lookup"><span data-stu-id="9f544-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Lauka darbības ikona"><br><span data-ttu-id="9f544-432">Lauks</span><span class="sxs-lookup"><span data-stu-id="9f544-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="No partijas atgriešanas darbības ikona"><br><span data-ttu-id="9f544-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="9f544-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="No krājumu statusa darbības ikona"><br><span data-ttu-id="9f544-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="9f544-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="ID atribūta darbības ikona"><br><span data-ttu-id="9f544-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="9f544-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Krājumu partijas ID darbības ikona"><br><span data-ttu-id="9f544-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="9f544-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Krājumu krāsas ID darbības ikona"><br><span data-ttu-id="9f544-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="9f544-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Krājumu atrašanās vietas darbības ikona"><br><span data-ttu-id="9f544-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="9f544-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Krājumu sērijas ID darbības ikona"><br><span data-ttu-id="9f544-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="9f544-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Krājumu izmēra ID darbības ikona"><br><span data-ttu-id="9f544-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="9f544-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Krājumu statusa ID darbības ikona"><br><span data-ttu-id="9f544-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="9f544-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Krājumu stila ID darbības ikona"><br><span data-ttu-id="9f544-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="9f544-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Krājumu versijas ID darbības ikona"><br><span data-ttu-id="9f544-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="9f544-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Krājuma ID darbības ikona"><br><span data-ttu-id="9f544-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="9f544-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ITM konteinera ID darbības ikona"><br><span data-ttu-id="9f544-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="9f544-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ITM sūtījuma ID darbības ikona"><br><span data-ttu-id="9f544-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="9f544-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Kanban kartes ID darbības ikona"><br><span data-ttu-id="9f544-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="9f544-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Kanban vai kartes ID darbības ikona"><br><span data-ttu-id="9f544-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="9f544-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Numura zīmes ID darbības ikona"><br><span data-ttu-id="9f544-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="9f544-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Kravas ID darbības ikona"><br><span data-ttu-id="9f544-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="9f544-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Numura zīmes novietojuma pozīcijas darbības ikona"><br><span data-ttu-id="9f544-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="9f544-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Atrašanās vietas vai numura zīmes darbības ikona"><br><span data-ttu-id="9f544-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="9f544-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Atrašanās vietas vai numura zīmes pārbaudes darbības ikona"><br><span data-ttu-id="9f544-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="9f544-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Atrašanās vietas vai numura zīmes no darbības ikonas"><br><span data-ttu-id="9f544-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="9f544-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Atrašanās vieta vai numura zīme uz darbības ikona"><br><span data-ttu-id="9f544-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="9f544-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Ilgais process pabeigts darbības ikona"><br><span data-ttu-id="9f544-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="9f544-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="LP pārtraukuma pamata LP darbības ikona"><br><span data-ttu-id="9f544-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="9f544-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Apvienot konteinera ID darbības ikona"><br><span data-ttu-id="9f544-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="9f544-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Jauktas numura zīmes rindas numura darbības ikona"><br><span data-ttu-id="9f544-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="9f544-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Izejošā svara darbības ikona"><br><span data-ttu-id="9f544-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="9f544-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Īpašnieka darbības ikona"><br><span data-ttu-id="9f544-490">Īpašnieks</span><span class="sxs-lookup"><span data-stu-id="9f544-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Pamata numura zīmes darbības ikona"><br><span data-ttu-id="9f544-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="9f544-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Lūdzu, apstipriniet darbības ikona"><br><span data-ttu-id="9f544-494">PleaseConfirm</span><span class="sxs-lookup"><span data-stu-id="9f544-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Pirkšanas pasūtījuma rindas numura darbības ikona"><br><span data-ttu-id="9f544-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="9f544-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Pirkšanas pasūtījuma numura darbības ikona"><br><span data-ttu-id="9f544-498">PONum</span><span class="sxs-lookup"><span data-stu-id="9f544-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Pozīcija pilna darbības ikona"><br><span data-ttu-id="9f544-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="9f544-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Satura darbības ikona"><br><span data-ttu-id="9f544-502">Saturs</span><span class="sxs-lookup"><span data-stu-id="9f544-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Printera nosaukuma darbības ikona"><br><span data-ttu-id="9f544-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="9f544-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Preces ID darbības ikona"><br><span data-ttu-id="9f544-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="9f544-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Preces apstiprināšanas darbības ikona"><br><span data-ttu-id="9f544-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Izvietot darbības ikona"><br><span data-ttu-id="9f544-510">Izvietot</span><span class="sxs-lookup"><span data-stu-id="9f544-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Izvietošanas klastera ID darbības ikona"><br><span data-ttu-id="9f544-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="9f544-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Daudzuma darbības ikona"><br><span data-ttu-id="9f544-514">Daudz.</span><span class="sxs-lookup"><span data-stu-id="9f544-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Daudzuma pielāgošana izvietošanā darbības ikona"><br><span data-ttu-id="9f544-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="9f544-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Mazā daudzuma darbības ikona"><br><span data-ttu-id="9f544-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="9f544-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Daudzums, kas tiek patērēts darbības ikona"><br><span data-ttu-id="9f544-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="9f544-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Daudzums, kas tiek izvietots darbības ikona"><br><span data-ttu-id="9f544-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="9f544-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Daudzums, kas tiek izbrāķēts darbības ikona"><br><span data-ttu-id="9f544-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="9f544-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Daudzuma apstiprināšanas darbības ikona"><br><span data-ttu-id="9f544-526">QuantityConfirmation</span><span class="sxs-lookup"><span data-stu-id="9f544-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Ziņot, kad pabeigts gala darbs darbības ikona"><br><span data-ttu-id="9f544-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="9f544-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Saņemt novietojuma ID darbības ikona"><br><span data-ttu-id="9f544-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="9f544-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Noņemt konteinera ID darbības ikona"><br><span data-ttu-id="9f544-532">RemoveContainerID</span><span class="sxs-lookup"><span data-stu-id="9f544-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA numura darbības ikona"><br><span data-ttu-id="9f544-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="9f544-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Atlasīt pasūtījumu darbības ikona"><br><span data-ttu-id="9f544-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="9f544-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Saīsinātās izdošanas iemesla darbības ikona"><br><span data-ttu-id="9f544-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="9f544-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Kārtot pozīcijas ID darbības ikona"><br><span data-ttu-id="9f544-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="9f544-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Mērķa numura zīmes ID darbības ikona"><br><span data-ttu-id="9f544-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="9f544-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Uz rindas numuru darbības ikona"><br><span data-ttu-id="9f544-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="9f544-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Uz atrašanās vietu darbības ikona"><br><span data-ttu-id="9f544-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="9f544-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Uz numuru darbības ikona"><br><span data-ttu-id="9f544-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="9f544-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Uz noliktavu darbības ikona"><br><span data-ttu-id="9f544-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="9f544-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Transporta kravas ID darbības ikona"><br><span data-ttu-id="9f544-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="9f544-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Kreditora partijas ID darbības ikona"><br><span data-ttu-id="9f544-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="9f544-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Kopuma etiķetes ID darbības ikona"><br><span data-ttu-id="9f544-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="9f544-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Kopuma etiķetes daudzuma darbības ikona"><br><span data-ttu-id="9f544-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="9f544-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Svara darbības ikona"><br><span data-ttu-id="9f544-560">Lielums</span><span class="sxs-lookup"><span data-stu-id="9f544-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Svars, kas tiek patērēts darbības ikona"><br><span data-ttu-id="9f544-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="9f544-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="WHS korekcijas tipa darbības ikona"><br><span data-ttu-id="9f544-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="9f544-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="WHS saņemšanas izņēmuma darbības ikona"><br><span data-ttu-id="9f544-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="9f544-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="WMS atrašanās vietas ID darbības ikona"><br><span data-ttu-id="9f544-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="9f544-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Darba ID darbības ikona"><br><span data-ttu-id="9f544-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="9f544-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Darba ID, lai atceltu darbības ikona"><br><span data-ttu-id="9f544-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="9f544-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Darba numura zīmes ID darbības ikona"><br><span data-ttu-id="9f544-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="9f544-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Darba numura zīmes ID izdošanas klastera darbības ikona"><br><span data-ttu-id="9f544-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="9f544-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Darba kopuma ID darbības ikona"><br><span data-ttu-id="9f544-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="9f544-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Zonas ID darbības ikona"><br><span data-ttu-id="9f544-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="9f544-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="9f544-581">Piemērs: darbību ikonu un nosaukumu piešķiršana pielāgotajai plūsmai</span><span class="sxs-lookup"><span data-stu-id="9f544-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="9f544-582">Šajā piemērā skaidrots, kā iestatīt darbību ikonas un nosaukumus pielāgotai uzdevumu plūsmai.</span><span class="sxs-lookup"><span data-stu-id="9f544-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="9f544-583">Scenārijs ir veidots no pielāgotas uzdevumu plūsmas piemēra, kas ir uzrādīta un detalizētāk aprakstīta tālāk aprakstītajā ziņā: [Noliktavas mobilās programmas pielāgošana](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span><span class="sxs-lookup"><span data-stu-id="9f544-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="9f544-584">Uzdevumu plūsma darbojas šādi:</span><span class="sxs-lookup"><span data-stu-id="9f544-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="9f544-585">Programmā tiek parādīta lapa, kurā darbiniekam tiek parādīta uzvedne ar aicinājumu norādīt konteinera ID (piemēram, skenējot svītrkodu).</span><span class="sxs-lookup"><span data-stu-id="9f544-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="9f544-586">Ja konteinera ID ir derīgs, programma atver jaunu lapu, kurā tiek parādīta uzvedne ar aicinājumu darbiniekam ievadīt svaru.</span><span class="sxs-lookup"><span data-stu-id="9f544-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="9f544-587">(Ja konteinera ID nav derīgs, darbinieks tiek atgriezts pirmajā lapā.)</span><span class="sxs-lookup"><span data-stu-id="9f544-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="9f544-588">Kad darbinieks ievada derīgu svaru, sistēma saglabā svaru un atgriež darbinieku pirmajā lapā.</span><span class="sxs-lookup"><span data-stu-id="9f544-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="9f544-589">Šajā attēlā parādīta šī uzdevuma plūsma.</span><span class="sxs-lookup"><span data-stu-id="9f544-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="9f544-590">![Uzdevuma plūsmas diagramma](media/step-icons-example-task-flow.png "Uzdevuma plūsmas diagramma")</span><span class="sxs-lookup"><span data-stu-id="9f544-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="9f544-591">Izveidot darbības klasi konteinera ievades lapai</span><span class="sxs-lookup"><span data-stu-id="9f544-591">Create a step class for the container input page</span></span>

<span data-ttu-id="9f544-592">Konteinera ievades lapa ļauj darbiniekam skenēt vai ievadīt konteinera ID.</span><span class="sxs-lookup"><span data-stu-id="9f544-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="9f544-593">![Konteinera ievades lapa](media/step-icons-example-container-input.png "Konteinera ievades lapa")</span><span class="sxs-lookup"><span data-stu-id="9f544-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="9f544-594">Konteinera ievades lapā ir ievadītā lauka kontroles nosaukums `ContainerId`.</span><span class="sxs-lookup"><span data-stu-id="9f544-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="9f544-595">Tā kā šis vadīklas nosaukums nav norādīts [darbības ID sarakstā](#step-ids-classes), jūs neatradīsiet esošu darbību, kas ir balstīta uz to.</span><span class="sxs-lookup"><span data-stu-id="9f544-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="9f544-596">Tādēļ ir jāizveido darbības klase, kas pārstāv šo darbību.</span><span class="sxs-lookup"><span data-stu-id="9f544-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="9f544-597">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="9f544-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="9f544-598">Darbības ikonas identifikators tiek saglabāts `defaultStepIcon` klases dalībniekā, un darbības nosaukums tiek saglabāts `defaultStepTitle` klases dalībniekā.</span><span class="sxs-lookup"><span data-stu-id="9f544-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="9f544-599">Lai piešķirtu darbības ikonu, iestatiet `defaultStepIcon` uz vienu no ikonu ID, kas uzskaitīti sadaļā [Pieejamās darbības ikonas](#step-icons) iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="9f544-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="9f544-600">Izmantojiet standarta vai pielāgotu darbības ikonu un nosaukumu svara ievadei</span><span class="sxs-lookup"><span data-stu-id="9f544-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="9f544-601">Svara ievades lapa ļauj darbiniekam ievadīt svaru.</span><span class="sxs-lookup"><span data-stu-id="9f544-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="9f544-602">![Svara ievades lapa](media/step-icons-example-weight-input.png "Svara ievades lapa")</span><span class="sxs-lookup"><span data-stu-id="9f544-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="9f544-603">Svara ievades lapā ievades lauka kontroles nosaukums ir `Weight`, kas atrodas [darbības ID sarakstā](#step-ids-classes).</span><span class="sxs-lookup"><span data-stu-id="9f544-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="9f544-604">Tādēļ, ja definētā darbības ikona un nosaukums `WHSMobileAppStepWeight` klasē jums ir pieņemami, šai darbībai nekas nav jāmaina.</span><span class="sxs-lookup"><span data-stu-id="9f544-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="9f544-605">Tomēr, ja šai darbībai vēlaties lietot citu ikonu vai nosaukumu, varat ignorēt `stepId()` metodi vai `stepInfo()` metodi veidotāja klasē.</span><span class="sxs-lookup"><span data-stu-id="9f544-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="9f544-606">Katrai uzdevumu plūsmai ir savs darbību informācijas veidotājs.</span><span class="sxs-lookup"><span data-stu-id="9f544-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="9f544-607">Ignorēt stepId() metodi</span><span class="sxs-lookup"><span data-stu-id="9f544-607">Override the stepId() method</span></span>

<span data-ttu-id="9f544-608">Šajā piemērā parādīts viens veids, kā modificēt veidotāja klasi, ignorējot `stepId()` metodi.</span><span class="sxs-lookup"><span data-stu-id="9f544-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="9f544-609">Izveidojiet darbības klasi `NewWeight` darbībai.</span><span class="sxs-lookup"><span data-stu-id="9f544-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="9f544-610">Kodam ir jābūt līdzīgam kodam iepriekš parādītajā `ContainerId` piemērā.</span><span class="sxs-lookup"><span data-stu-id="9f544-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="9f544-611">Ignorēt stepInfo() metodi</span><span class="sxs-lookup"><span data-stu-id="9f544-611">Override the stepInfo() method</span></span>

<span data-ttu-id="9f544-612">Šajā piemērā parādīts viens veids, kā modificēt veidotāja klasi, ignorējot `stepInfo()` metodi.</span><span class="sxs-lookup"><span data-stu-id="9f544-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="9f544-613">Tad konstruējiet objektu `WHSMobileAppStepInfo` un tieši iestatiet ikonu un/vai nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="9f544-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9f544-614">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9f544-614">Additional resources</span></span>

- [<span data-ttu-id="9f544-615">Noliktavas pārvaldības mobilās programmas instalēšana un savienošana</span><span class="sxs-lookup"><span data-stu-id="9f544-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="9f544-616">Mobilās ierīces lietotāja iestatījumi</span><span class="sxs-lookup"><span data-stu-id="9f544-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
