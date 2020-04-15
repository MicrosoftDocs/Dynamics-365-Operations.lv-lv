---
title: Pārsūtīšanas dokumentu par preču kustību uzņēmumā iestatīšana
description: Šajā procedūrā ir aprakstīts, kā izveidot preču kustības uzņēmuma robežās pārsūtīšanas dokumentus.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e85bd359ce1053629ad4217cf623e57b2976463a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143486"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="3662a-103">Pārsūtīšanas dokumentu par preču kustību uzņēmumā iestatīšana</span><span class="sxs-lookup"><span data-stu-id="3662a-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3662a-104">Šajā procedūrā ir aprakstīts, kā izveidot preču kustības uzņēmuma robežās pārsūtīšanas dokumentus.</span><span class="sxs-lookup"><span data-stu-id="3662a-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="3662a-105">Šī procedūra ir pieejama tikai juridiskām personām, kuru primārā adrese ir Lietuvā.</span><span class="sxs-lookup"><span data-stu-id="3662a-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="3662a-106">Šī procedūra ir izveidota, izmantojot demonstrācijas datu uzņēmumu DEMF, kura primārā adrese ir Lietuvā.</span><span class="sxs-lookup"><span data-stu-id="3662a-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="3662a-107">Lai varētu pabeigt šo procedūru, ir jāizpilda procedūra "Iestatīt preču kustības uzņēmuma robežās pārsūtīšanas dokumentus".</span><span class="sxs-lookup"><span data-stu-id="3662a-107">Before you can complete this procedure, you must complete the "Set up transfer documents for goods movement inside a company" procedure.</span></span> <span data-ttu-id="3662a-108">Šī procedūra ir paredzēta krājumu grāmatvežiem.</span><span class="sxs-lookup"><span data-stu-id="3662a-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="3662a-109">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="3662a-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="3662a-110">Izveidot pārsūtīšanas pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="3662a-110">Create a transfer order</span></span>
1. <span data-ttu-id="3662a-111">Dodieties uz sadaļu Krājumu pārvaldība > Ienākošie pasūtījumi > Pārsūtīšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="3662a-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="3662a-112">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3662a-112">Click New.</span></span>
3. <span data-ttu-id="3662a-113">Laukā No noliktavas ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3662a-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="3662a-114">Laukā Uz noliktavu ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3662a-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="3662a-115">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="3662a-115">Click Add.</span></span>
6. <span data-ttu-id="3662a-116">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3662a-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="3662a-117">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3662a-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="3662a-118">Ievadīt pārsūtīšanas pasūtījuma transportēšanas datus</span><span class="sxs-lookup"><span data-stu-id="3662a-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="3662a-119">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3662a-119">Click Save.</span></span>
2. <span data-ttu-id="3662a-120">Darbību rūtī noklikšķiniet uz Sūtīt.</span><span class="sxs-lookup"><span data-stu-id="3662a-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="3662a-121">Noklikšķiniet uz Transportēšanas dati.</span><span class="sxs-lookup"><span data-stu-id="3662a-121">Click Transportation details.</span></span>
4. <span data-ttu-id="3662a-122">Laukā Drukāt transportēšanas datus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="3662a-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="3662a-123">Laukā Preces izsniedza ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3662a-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="3662a-124">Laukā Iepakojums ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3662a-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="3662a-125">Ievadiet vērtību laukā Noslodzes riska līmenis.</span><span class="sxs-lookup"><span data-stu-id="3662a-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="3662a-126">Ievadiet vai atlasiet vērtību laukā Pārvadātājs.</span><span class="sxs-lookup"><span data-stu-id="3662a-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="3662a-127">Ievadiet vai atlasiet vērtību laukā Modelis.</span><span class="sxs-lookup"><span data-stu-id="3662a-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="3662a-128">Laukā Reģistrācijas numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3662a-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="3662a-129">Ievadiet vērtību laukā Piekabes reģistrācijas numurs.</span><span class="sxs-lookup"><span data-stu-id="3662a-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="3662a-130">Ievadiet vai atlasiet vērtību laukā Transportlīdzekļa vadītājs.</span><span class="sxs-lookup"><span data-stu-id="3662a-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="3662a-131">Laukā Autovadītāja vārds ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3662a-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="3662a-132">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3662a-132">Click Save.</span></span>
15. <span data-ttu-id="3662a-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3662a-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="3662a-134">Skatīt negrāmatotā pārsūtīšanas pasūtījuma pavadzīmi</span><span class="sxs-lookup"><span data-stu-id="3662a-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="3662a-135">Noklikšķiniet uz Pavadzīme.</span><span class="sxs-lookup"><span data-stu-id="3662a-135">Click Packing slip.</span></span>
2. <span data-ttu-id="3662a-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="3662a-136">Click OK.</span></span>
3. <span data-ttu-id="3662a-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3662a-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="3662a-138">Skatīt grāmatotā pārsūtīšanas pasūtījuma pavadzīmi</span><span class="sxs-lookup"><span data-stu-id="3662a-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="3662a-139">Darbību rūtī noklikšķiniet uz Pārsūtīšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="3662a-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="3662a-140">Darbību rūtī noklikšķiniet uz Sūtīt.</span><span class="sxs-lookup"><span data-stu-id="3662a-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="3662a-141">Noklikšķiniet uz Nosūtīt pārsūtīšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="3662a-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="3662a-142">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="3662a-142">Click the General tab.</span></span>
5. <span data-ttu-id="3662a-143">Atlasiet opciju laukā Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="3662a-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="3662a-144">Noklikšķiniet uz cilnes Apskats.</span><span class="sxs-lookup"><span data-stu-id="3662a-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="3662a-145">Ierakstiet vērtību laukā Pavadzīme.</span><span class="sxs-lookup"><span data-stu-id="3662a-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="3662a-146">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="3662a-146">Click OK.</span></span>
9. <span data-ttu-id="3662a-147">Darbību rūtī noklikšķiniet uz Sūtīt.</span><span class="sxs-lookup"><span data-stu-id="3662a-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="3662a-148">Noklikšķiniet uz Pavadzīme.</span><span class="sxs-lookup"><span data-stu-id="3662a-148">Click Packing slip.</span></span>
11. <span data-ttu-id="3662a-149">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="3662a-149">Click OK.</span></span>

