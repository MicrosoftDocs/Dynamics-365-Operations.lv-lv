---
title: Tiešsaistes pārdošanas un maksājumu grāmatošana
description: Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu pārdošanas pasūtījumus un maksājumus tiešsaistes veikala transakcijām.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bac0cab764436a618fa570901c84ab720dbc86
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140788"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="4df54-103">Tiešsaistes pārdošanas un maksājumu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="4df54-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4df54-104">Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu pārdošanas pasūtījumus un maksājumus tiešsaistes veikala transakcijām.</span><span class="sxs-lookup"><span data-stu-id="4df54-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="4df54-105">Tiešsaistes pārdošanas un maksājumu grāmata ir process divos posmos.</span><span class="sxs-lookup"><span data-stu-id="4df54-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="4df54-106">Tiešsaistes komercijas darījumu datu vilkšana HQ.</span><span class="sxs-lookup"><span data-stu-id="4df54-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="4df54-107">Pasūtījumu sinhronizēšana, lai izveidotu pārdošanas pasūtījumus HQ.</span><span class="sxs-lookup"><span data-stu-id="4df54-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="4df54-108">Tiešsaistes darījumu datu vilkšanu var veikt vai nu manuāli palaižot P darbu vai izveidojot periodisku pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="4df54-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="4df54-109">P darba manuāla palaišana</span><span class="sxs-lookup"><span data-stu-id="4df54-109">Manually running the P-job</span></span>

1. <span data-ttu-id="4df54-110">Dodieties uz Visas darbvietas > Retail un Commerce IT.</span><span class="sxs-lookup"><span data-stu-id="4df54-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="4df54-111">Noklikšķiniet uz izplatīšanas grafika.</span><span class="sxs-lookup"><span data-stu-id="4df54-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="4df54-112">Atlasiet P-0001.</span><span class="sxs-lookup"><span data-stu-id="4df54-112">Select P-0001.</span></span>
4. <span data-ttu-id="4df54-113">Ja nepieciešams, pielāgojiet kanāla datu bāzu grupas.</span><span class="sxs-lookup"><span data-stu-id="4df54-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="4df54-114">Noklikšķiniet uz Izpildīt tūlīt.</span><span class="sxs-lookup"><span data-stu-id="4df54-114">Click Run now.</span></span>
6. <span data-ttu-id="4df54-115">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="4df54-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="4df54-116">Periodiskā P darba plānošana</span><span class="sxs-lookup"><span data-stu-id="4df54-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="4df54-117">Dodieties uz Visas darbvietas > Retail un Commerce IT.</span><span class="sxs-lookup"><span data-stu-id="4df54-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="4df54-118">Noklikšķiniet uz izplatīšanas grafika.</span><span class="sxs-lookup"><span data-stu-id="4df54-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="4df54-119">Atlasiet P-0001.</span><span class="sxs-lookup"><span data-stu-id="4df54-119">Select P-0001.</span></span>
4. <span data-ttu-id="4df54-120">Noklikšķiniet uz Izveidot pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="4df54-120">Click Create batch job.</span></span>
5. <span data-ttu-id="4df54-121">Noklikšķiniet uz Palaist fonā.</span><span class="sxs-lookup"><span data-stu-id="4df54-121">Click Run in the background.</span></span>
5. <span data-ttu-id="4df54-122">Iespējojiet pakešapstrādi.</span><span class="sxs-lookup"><span data-stu-id="4df54-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="4df54-123">Noklikšķiniet uz Periodiskums..</span><span class="sxs-lookup"><span data-stu-id="4df54-123">Click Recurrence..</span></span>
7. <span data-ttu-id="4df54-124">Atlasiet opciju Bez beigu datuma.</span><span class="sxs-lookup"><span data-stu-id="4df54-124">Select the No end date option.</span></span>
8. <span data-ttu-id="4df54-125">Laukā Skaits ievadiet intervālu starp izpildēm, izteiktu minūtēs.</span><span class="sxs-lookup"><span data-stu-id="4df54-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="4df54-126">Parasti tās būtu 5-10.</span><span class="sxs-lookup"><span data-stu-id="4df54-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="4df54-127">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="4df54-127">Click OK.</span></span>
10. <span data-ttu-id="4df54-128">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="4df54-128">Click OK.</span></span>

<span data-ttu-id="4df54-129">Pasūtījumus var sinhronizēt vai nu manuāli palaižot darbu "Sinhronizēt pasūtījumus" vai izveidojot periodisku pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="4df54-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="4df54-130">Pasūtījuma sinhronizācijas manuāla palaišana</span><span class="sxs-lookup"><span data-stu-id="4df54-130">Manually running order synchronization</span></span> 

<span data-ttu-id="4df54-131">Veiciet šīs darbības, lai vienreiz manuāli palaistu darbu "Sinhronizēt pasūtījumus".</span><span class="sxs-lookup"><span data-stu-id="4df54-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="4df54-132">Pārejiet uz sadaļu Visas darbvietas > Veikala finanses.</span><span class="sxs-lookup"><span data-stu-id="4df54-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="4df54-133">Noklikšķiniet uz Sinhronizēt pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="4df54-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="4df54-134">Laukā Organizācijas hierarhija atlasiet Veikali pēc reģiona.</span><span class="sxs-lookup"><span data-stu-id="4df54-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="4df54-135">Atlasiet konkrētu tiešsaistes veikalu vai zaru, lai izveidotu pakešuzdevumu veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="4df54-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="4df54-136">Noklikšķiniet uz bultiņas, lai pievienotu atlasi.</span><span class="sxs-lookup"><span data-stu-id="4df54-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="4df54-137">Noklikšķiniet uz cilnes Palaist fonā.</span><span class="sxs-lookup"><span data-stu-id="4df54-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="4df54-138">Atspējojiet pakešapstrādi.</span><span class="sxs-lookup"><span data-stu-id="4df54-138">Disable Batch processing</span></span>
6. <span data-ttu-id="4df54-139">Noklikšķiniet uz Periodiskums.</span><span class="sxs-lookup"><span data-stu-id="4df54-139">Click Recurrence.</span></span>
7. <span data-ttu-id="4df54-140">Atlasiet opciju Beidzas pēc</span><span class="sxs-lookup"><span data-stu-id="4df54-140">Select End After option</span></span>
8. <span data-ttu-id="4df54-141">Laukā Beidzas pēc, ievadiet 1.</span><span class="sxs-lookup"><span data-stu-id="4df54-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="4df54-142">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="4df54-142">Click OK.</span></span>
10. <span data-ttu-id="4df54-143">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="4df54-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="4df54-144">Periodiskas pasūtījuma sinhronizācijas plānošana</span><span class="sxs-lookup"><span data-stu-id="4df54-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="4df54-145">Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu pārdošanas pasūtījumus un maksājumus tiešsaistes veikala transakcijām.</span><span class="sxs-lookup"><span data-stu-id="4df54-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="4df54-146">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="4df54-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4df54-147">Pārejiet uz sadaļu Visas darbvietas > Veikala finanses.</span><span class="sxs-lookup"><span data-stu-id="4df54-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="4df54-148">Noklikšķiniet uz Sinhronizēt pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="4df54-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="4df54-149">Laukā Organizācijas hierarhija atlasiet Veikali pēc reģiona.</span><span class="sxs-lookup"><span data-stu-id="4df54-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="4df54-150">Atlasiet konkrētu tiešsaistes veikalu vai zaru, lai izveidotu pakešuzdevumu veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="4df54-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="4df54-151">Noklikšķiniet uz bultiņas, lai pievienotu atlasi.</span><span class="sxs-lookup"><span data-stu-id="4df54-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="4df54-152">Noklikšķiniet uz cilnes Palaist fonā.</span><span class="sxs-lookup"><span data-stu-id="4df54-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="4df54-153">Iespējojiet pakešapstrādi</span><span class="sxs-lookup"><span data-stu-id="4df54-153">Enable Batch processing</span></span>
6. <span data-ttu-id="4df54-154">Noklikšķiniet uz Periodiskums.</span><span class="sxs-lookup"><span data-stu-id="4df54-154">Click Recurrence.</span></span>
7. <span data-ttu-id="4df54-155">Atlasiet opciju Bez beigu datuma.</span><span class="sxs-lookup"><span data-stu-id="4df54-155">Select the No end date option.</span></span>
8. <span data-ttu-id="4df54-156">Laukā Skaits ievadiet intervālu starp izpildēm, izteiktu minūtēs.</span><span class="sxs-lookup"><span data-stu-id="4df54-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="4df54-157">Parasti tās būtu 2-20</span><span class="sxs-lookup"><span data-stu-id="4df54-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="4df54-158">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="4df54-158">Click OK.</span></span>
10. <span data-ttu-id="4df54-159">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="4df54-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="4df54-160">Procesā iesaistītie datu elementi</span><span class="sxs-lookup"><span data-stu-id="4df54-160">Data entities involved in the process</span></span>

- <span data-ttu-id="4df54-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="4df54-161">RetailTransactionTable</span></span>
- <span data-ttu-id="4df54-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="4df54-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="4df54-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="4df54-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="4df54-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="4df54-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="4df54-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="4df54-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="4df54-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="4df54-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="4df54-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="4df54-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="4df54-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="4df54-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="4df54-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="4df54-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="4df54-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="4df54-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="4df54-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="4df54-171">RetailTransactionAttributeTrans</span></span>
