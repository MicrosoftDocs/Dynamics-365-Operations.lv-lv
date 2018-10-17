--- 
title: "Manuālas iepakošanas iestatīšana (2016. gada februāris un 2016. gada maijs)"
description: "Iepakošanas procesu ļauj jums pārbaudīt un iepakot preces konteineros."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: b90b4a71e2447e942dbb4a9645ef93064da630d3
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="a3cb7-103">Manuālas iepakošanas iestatīšana (2016. gada februāris un 2016. gada maijs)</span><span class="sxs-lookup"><span data-stu-id="a3cb7-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3cb7-104">Iepakošanas procesu ļauj jums pārbaudīt un iepakot preces konteineros.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="a3cb7-105">Šajā procesā, noliktavas darbinieki izdod preces no uzglabāšanas vietām un pārvieto tās uz iepakojuma staciju, kur tie pārbauda krājumu daudzumus un veidus, un piešķir tiem atbilstošus konteinerus.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="a3cb7-106">Kad konteiners ir pilns, to var aizvērt un pārvietot to uz nosūtīšanas doku, un preces ir gatavas nosūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="a3cb7-107">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="a3cb7-108">Šī procedūra ir paredzēta tikai 2016. gada februāra un 2016. gada maija Dynamics 365 for Operations versijām.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="a3cb7-109">Iestatīt novietojuma profilus</span><span class="sxs-lookup"><span data-stu-id="a3cb7-109">Set up location profiles</span></span>
1. <span data-ttu-id="a3cb7-110">Dodieties uz Noliktavas vadība > Iestatīšana > Noliktava > Novietojumu profili.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="a3cb7-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-111">Click New.</span></span>
    * <span data-ttu-id="a3cb7-112">Atrašanās vietas profils tiek izmantots iepakošanas stacijās, un satur informāciju un noteikumus par atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="a3cb7-113">Laukā Novietojuma profila ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="a3cb7-114">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a3cb7-115">Laukā Atrašanās vietas formāts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="a3cb7-116">Laukā Atrašanās vietas tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="a3cb7-117">Laukā Atļaut jauktus krājumus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="a3cb7-118">Laukā Atļaut jauktus krājumu statusus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="a3cb7-119">Atlasiet Jā, laukā Ignorēt partijas dienu kārtulas.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="a3cb7-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="a3cb7-121">Noliktavas vadības parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a3cb7-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="a3cb7-122">Doties uz Noliktavas vadība > Iestatīšana > Noliktavas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="a3cb7-123">Klikšķiniet cilni Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="a3cb7-124">Laukā Iepakošanas atrašanās vietas profila ID ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="a3cb7-125">Atlasiet atrašanās vietas profilu, kuru vēlaties izmantot iepakošanai.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="a3cb7-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="a3cb7-127">Konteinera veidu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a3cb7-127">Set up container types</span></span>
1. <span data-ttu-id="a3cb7-128">Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru veidi.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="a3cb7-129">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-129">Click New.</span></span>
    * <span data-ttu-id="a3cb7-130">Jūs varat noteikt konteineru tipus izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-130">You can define the types of containers to use.</span></span> <span data-ttu-id="a3cb7-131">Var norādīt konteinera fiziskās dimensijas, ieskaitot taras svaru, maksimālo svaru, maksimālo tilpumu, garumu, platumu un svaru.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="a3cb7-132">Atribūti ir pielāgoti lauki, kas ļauj jums pievienot papildu dimensijas konteinera tipam.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="a3cb7-133">Laukā Konteinera veida kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="a3cb7-134">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a3cb7-135">Laukā Taras svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="a3cb7-136">Ievadiet skaitli laukā Maksimālais svars.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="a3cb7-137">Laukā Tilpums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="a3cb7-138">Laukā Garums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="a3cb7-139">Ievadiet skaitli laukā Platums.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="a3cb7-140">Ievadiet skaitli laukā Augstums.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="a3cb7-141">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-141">Click Save.</span></span>
12. <span data-ttu-id="a3cb7-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="a3cb7-143">Iepakošanas profilu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a3cb7-143">Set up packing profiles</span></span>
1. <span data-ttu-id="a3cb7-144">Dodieties uz Noliktavas vadība > Iestatīšana > Iepakošana > Iepakošanas profili.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="a3cb7-145">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-145">Click New.</span></span>
3. <span data-ttu-id="a3cb7-146">Ievadiet vērtību laukā Iepakošanas profila ID.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="a3cb7-147">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a3cb7-148">Laukā Iepakošanas slēgšanas profila ID ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="a3cb7-149">Konteinera slēgšanas profila ID ir neobligāts, un ir noklusējuma konteinera slēgšanas profils šim iepakošanas profilam.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="a3cb7-150">Laukā Konteinera ID režīms atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="a3cb7-151">Šī opcija nosaka, vai konteinera ID tiks automātiski ģenerēts, kad tiek izveidots konteineris, vai arī konteinera ID tiks ģenerēts manuāli.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="a3cb7-152">Laukā Konteinera veids, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="a3cb7-153">Konteinera veids tiks izmantots pēc noklusējuma, veidojot jaunu konteineru.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="a3cb7-154">Konteinera slēgšanas izvēles rūtiņā, atlasiet Automātiski izveidot konteineru.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="a3cb7-155">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-155">Click Save.</span></span>
10. <span data-ttu-id="a3cb7-156">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="a3cb7-157">Konteinera slēgšanas profilu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a3cb7-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="a3cb7-158">Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru slēgšanas profili.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="a3cb7-159">Konteinera slēgšanas profili definē, kas notiek, ja konteiners tiek slēgts.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="a3cb7-160">Jūs varat iestatīt vairākus konteinera slēgšanas profilus.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="a3cb7-161">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-161">Click New.</span></span>
3. <span data-ttu-id="a3cb7-162">Laukā Iepakošanas slēgšanas profila ID ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="a3cb7-163">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a3cb7-164">Laukā Manifestācija, atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="a3cb7-165">Norādiet, vai manifestācija parādās, slēdzot konteinerus, vai apstiprinot sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="a3cb7-166">Ņemiet vērā, ka manifestācijai nepieciešama transportēšanas pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="a3cb7-167">Manifestācijai jābūt ieviestai transportēšanas programmās, lai tā strādātu.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="a3cb7-168">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="a3cb7-169">Laukā Noklusējuma galīgā sūtījuma atrašanās vieta, ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="a3cb7-170">Tas ir vieta, uz kuru preces tiks pārvietotas pēc konteineru slēgšanas.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="a3cb7-171">Šai vietai jābūt atrašanās vietas profilam, kas ir definēts Noliktavas parametros.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="a3cb7-172">Laukā Svara vienība, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="a3cb7-173">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a3cb7-173">Click Save.</span></span>


