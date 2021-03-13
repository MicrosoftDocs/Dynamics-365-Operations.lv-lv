---
title: Kļūmju pārvaldība
description: Šajā tēmā ir izskaidrota kļūmju pārvaldība modulī Līdzekļu pārvaldība.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 176fbebcf88e7557bf2bafc56524cd2ec015220e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020968"
---
# <a name="fault-management"></a><span data-ttu-id="e0c2d-103">Kļūmju pārvaldība</span><span class="sxs-lookup"><span data-stu-id="e0c2d-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e0c2d-104">Modulī Līdzekļu pārvaldība varat izmantot kļūmju noformētāju, lai līdzekļu tipiem iestatītu kļūmju simptomus, kļūmju apgabalus un kļūmju tipus.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="e0c2d-105">Šādi varat pārvaldīt līdzekļos konstatētās kļūdas.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="e0c2d-106">Turklāt kļūmju iemeslus un ieteikumus to labošanai var reģistrēt darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="e0c2d-107">Kļūmju reģistrācijas un pārvaldības process ietver trīs darbības.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="e0c2d-108">Izveidojiet kļūmju simptomu, kļūmju apgabalu un kļūmju tipu sarakstu, kuri var parādīties jūsu līdzekļu tipos.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="e0c2d-109">Kļūmju noformētājā iestatiet simptomus, kļūmju apgabalus un kļūmju tipus.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="e0c2d-110">Tālāk ir sniegti daži piemēri, lai palīdzētu jums izprast atšķirību starp kļūmju simptomiem, kļūmju apgabaliem un kļūmju tipiem.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="e0c2d-111">**Kļūmju simptomi:**</span><span class="sxs-lookup"><span data-stu-id="e0c2d-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="e0c2d-112">Nesabalansēti spriegumi</span><span class="sxs-lookup"><span data-stu-id="e0c2d-112">Unbalanced voltages</span></span>
- <span data-ttu-id="e0c2d-113">Īsa shēma</span><span class="sxs-lookup"><span data-stu-id="e0c2d-113">Short circuit</span></span>
- <span data-ttu-id="e0c2d-114">Troksnis</span><span class="sxs-lookup"><span data-stu-id="e0c2d-114">Noise</span></span>
- <span data-ttu-id="e0c2d-115">Noplūde</span><span class="sxs-lookup"><span data-stu-id="e0c2d-115">Leak</span></span>
- <span data-ttu-id="e0c2d-116">Vibrācijas</span><span class="sxs-lookup"><span data-stu-id="e0c2d-116">Vibrations</span></span>

<span data-ttu-id="e0c2d-117">**Kļūmju apgabali:**</span><span class="sxs-lookup"><span data-stu-id="e0c2d-117">**Fault areas:**</span></span>

- <span data-ttu-id="e0c2d-118">Elektrības</span><span class="sxs-lookup"><span data-stu-id="e0c2d-118">Electrical</span></span>
- <span data-ttu-id="e0c2d-119">Mehānisks</span><span class="sxs-lookup"><span data-stu-id="e0c2d-119">Mechanical</span></span>
- <span data-ttu-id="e0c2d-120">Hidraulisks</span><span class="sxs-lookup"><span data-stu-id="e0c2d-120">Hydraulic</span></span>
- <span data-ttu-id="e0c2d-121">Pneimātisks</span><span class="sxs-lookup"><span data-stu-id="e0c2d-121">Pneumatic</span></span>

<span data-ttu-id="e0c2d-122">**Kļūmju tipi**</span><span class="sxs-lookup"><span data-stu-id="e0c2d-122">**Fault types:**</span></span>

- <span data-ttu-id="e0c2d-123">Bojāts galvenā statora tinums</span><span class="sxs-lookup"><span data-stu-id="e0c2d-123">Faulty main stator winding</span></span>
- <span data-ttu-id="e0c2d-124">Bojāta diode</span><span class="sxs-lookup"><span data-stu-id="e0c2d-124">Faulty diode</span></span>
- <span data-ttu-id="e0c2d-125">Netīri tinumi</span><span class="sxs-lookup"><span data-stu-id="e0c2d-125">Dirty windings</span></span>
- <span data-ttu-id="e0c2d-126">Defektīvs ģenerators</span><span class="sxs-lookup"><span data-stu-id="e0c2d-126">Defective generator</span></span>
- <span data-ttu-id="e0c2d-127">Defektīvs sensors</span><span class="sxs-lookup"><span data-stu-id="e0c2d-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="e0c2d-128">Kļūmju simptomu izveide</span><span class="sxs-lookup"><span data-stu-id="e0c2d-128">Create fault symptoms</span></span>

<span data-ttu-id="e0c2d-129">Izpildiet tālāk norādītās darbības kļūmju simptomu izveidei, kurus var izmantot kļūmju noformētājā.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="e0c2d-130">Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Kļūme** \> **Kļūmju simptomi**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="e0c2d-131">Atlasiet **Jauns**, lai izveidotu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="e0c2d-132">Laukā **Kļūmes simptoms** ievadiet kļūmes simptoma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="e0c2d-133">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="e0c2d-134">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="e0c2d-135">Kļūmju apgabalu izveide</span><span class="sxs-lookup"><span data-stu-id="e0c2d-135">Create fault areas</span></span>

<span data-ttu-id="e0c2d-136">Izpildiet tālāk norādītās darbības apgabalu vai atrašanās vietu saraksta izveidei, kurus var izmantot kļūmju noformētājā.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="e0c2d-137">Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Kļūme** \> **Kļūmju apgabali**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="e0c2d-138">Atlasiet **Jauns**, lai izveidotu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="e0c2d-139">Laukā **Kļūmes apgabals** ievadiet kļūmes apgabala nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="e0c2d-140">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="e0c2d-141">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="e0c2d-142">Kļūmju tipu izveide</span><span class="sxs-lookup"><span data-stu-id="e0c2d-142">Create fault types</span></span>

<span data-ttu-id="e0c2d-143">Izpildiet tālāk norādītās darbības kļūmju tipu saraksta izveidei, kurus var izmantot kļūmju noformētājā.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="e0c2d-144">Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Kļūme** \> **Kļūmju tipi**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="e0c2d-145">Atlasiet **Jauns**, lai izveidotu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="e0c2d-146">Laukā **Kļūmes tips** ievadiet kļūmes tipa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="e0c2d-147">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="e0c2d-148">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="e0c2d-149">Kļūmju noformētāja iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e0c2d-149">Set up the fault designer</span></span>

<span data-ttu-id="e0c2d-150">Kļūmju noformētājā līdzekļu tipiem iestatiet kļūmju datus.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="e0c2d-151">Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Kļūme** \> **Kļūmju noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="e0c2d-152">Kreisajā rūtī atlasiet līdzekļa tipu, kuram iestatīt kļūmes ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="e0c2d-153">Cilnē FastTab **Kļūmes simptoms** atlasiet **Pievienot rindu** un pēc tam laukā **Kļūmes simptoms** atlasiet kļūmes simptomu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="e0c2d-154">Cilnē FastTab **Kļūmes apgabals** atlasiet **Pievienot rindu** un pēc tam laukā **Kļūmes apgabals** atlasiet kļūmes apgabalu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="e0c2d-155">Cilnē FastTab **Kļūmes tips** atlasiet **Pievienot rindu** un pēc tam laukā **Kļūmes tips** atlasiet kļūmes tipu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="e0c2d-156">Lai ātri izveidotu kombināciju no visiem esošajiem kļūmju simptomiem, apgabaliem un tipiem atlasītajam līdzekļa tipam, atlasiet **Izveidot kļūmju kombinācijas**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="e0c2d-157">Šī funkcija ir noderīga, ja esat pievienojis daudz kļūmju simptomu, apgabalu un tipu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="e0c2d-158">Ir vieglāk dzēst rindas jebkādām kombinācijām, kas neatbilst līdzekļa tipam, nekā manuāli izveidot jaunas rindas.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0c2d-159">Lai kopētu kļūmju simptomu, apgabalu un tipu iestatīšanu no viena līdzekļa tipa uz atlasīto līdzekļa tipu, atlasiet **Kopēt no līdzekļa tipa**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="e0c2d-160">Atlasiet **Saglabāt**, lai saglabātu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-160">Select **Save** to save your changes.</span></span>

![Kļūmes veidotāja lapa](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="e0c2d-162">Kļūmju iemeslu izveide</span><span class="sxs-lookup"><span data-stu-id="e0c2d-162">Create fault causes</span></span>

<span data-ttu-id="e0c2d-163">Izpildiet tālāk norādītās darbības zināmo kļūmju iemeslu saraksta izveidei, kurus var pievienot darba pasūtījumam vai uzturēšanas pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="e0c2d-164">Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Kļūme** \> **Kļūmju iemesli**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="e0c2d-165">Atlasiet **Jauns**, lai izveidotu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="e0c2d-166">Laukā **Kļūmes iemesls** ievadiet kļūmes iemesla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="e0c2d-167">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="e0c2d-168">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="e0c2d-169">Kļūmju novēršanas izveide</span><span class="sxs-lookup"><span data-stu-id="e0c2d-169">Create fault remedies</span></span>

<span data-ttu-id="e0c2d-170">Izpildiet tālāk norādītās darbības, lai izveidotu ieteikumus kļūmju novēršanai un labošanai, kurus var pievienot darba pasūtījumam vai uzturēšanas pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="e0c2d-171">Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Kļūme** \> **Kļūmju novēršana**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="e0c2d-172">Atlasiet **Jauns**, lai izveidotu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="e0c2d-173">Laukā **Kļūmes novēršana** ievadiet kļūmes novēršanas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="e0c2d-174">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="e0c2d-175">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="e0c2d-176">Varat mainīt savu kļūmju simptomu, apgabalu, tipu, iemeslu un novēršanas nosaukumus pēc saviem ieskatiem.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="e0c2d-177">Nosaukuma izmaiņas automātiski tiek atspoguļoti atbilstošajās kļūmju reģistrācijās.</span><span class="sxs-lookup"><span data-stu-id="e0c2d-177">The name changes are automatically reflected in the related fault registrations.</span></span>
