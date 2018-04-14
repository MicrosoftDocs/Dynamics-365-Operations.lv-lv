--- 
title: "Manuālas iepakošanas iestatīšana (tikai 2016. gada februāris un maijs)"
description: "Iepakošanas procesu ļauj jums pārbaudīt un iepakot preces konteineros."
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 31b689b6c31563f24892525eed5911af3a35bd51
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="cbcca-103">Manuālas iepakošanas iestatīšana (tikai 2016. gada februāris un maijs)</span><span class="sxs-lookup"><span data-stu-id="cbcca-103">Set up manual packing (February & May 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cbcca-104">Iepakošanas procesu ļauj jums pārbaudīt un iepakot preces konteineros.</span><span class="sxs-lookup"><span data-stu-id="cbcca-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="cbcca-105">Šajā procesā, noliktavas darbinieki izdod preces no uzglabāšanas vietām un pārvieto tās uz iepakojuma staciju, kur tie pārbauda krājumu daudzumus un veidus, un piešķir tiem atbilstošus konteinerus.</span><span class="sxs-lookup"><span data-stu-id="cbcca-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="cbcca-106">Kad konteiners ir pilns, to var aizvērt un pārvietot to uz nosūtīšanas doku, un preces ir gatavas nosūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="cbcca-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="cbcca-107">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="cbcca-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="cbcca-108">Iestatīt novietojuma profilus</span><span class="sxs-lookup"><span data-stu-id="cbcca-108">Set up location profiles</span></span>
1. <span data-ttu-id="cbcca-109">Dodieties uz Noliktavas vadība > Iestatīšana > Noliktava > Novietojumu profili.</span><span class="sxs-lookup"><span data-stu-id="cbcca-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="cbcca-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="cbcca-110">Click New.</span></span>
    * <span data-ttu-id="cbcca-111">Atrašanās vietas profils tiek izmantots iepakošanas stacijās, un satur informāciju un noteikumus par atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="cbcca-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="cbcca-112">Laukā Novietojuma profila ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="cbcca-113">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="cbcca-114">Laukā Atrašanās vietas formāts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="cbcca-115">Laukā Atrašanās vietas tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="cbcca-116">Laukā Atļaut jauktus krājumus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="cbcca-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="cbcca-117">Laukā Atļaut jauktus krājumu statusus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="cbcca-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="cbcca-118">Atlasiet Jā, laukā Ignorēt partijas dienu kārtulas.</span><span class="sxs-lookup"><span data-stu-id="cbcca-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="cbcca-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cbcca-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="cbcca-120">Noliktavas vadības parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cbcca-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="cbcca-121">Doties uz Noliktavas vadība > Iestatīšana > Noliktavas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="cbcca-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="cbcca-122">Klikšķiniet cilni Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="cbcca-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="cbcca-123">Laukā Iepakošanas atrašanās vietas profila ID ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="cbcca-124">Atlasiet atrašanās vietas profilu, kuru vēlaties izmantot iepakošanai.</span><span class="sxs-lookup"><span data-stu-id="cbcca-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="cbcca-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cbcca-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="cbcca-126">Konteinera veidu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cbcca-126">Set up container types</span></span>
1. <span data-ttu-id="cbcca-127">Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru veidi.</span><span class="sxs-lookup"><span data-stu-id="cbcca-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="cbcca-128">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="cbcca-128">Click New.</span></span>
    * <span data-ttu-id="cbcca-129">Jūs varat noteikt konteineru tipus izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="cbcca-129">You can define the types of containers to use.</span></span> <span data-ttu-id="cbcca-130">Var norādīt konteinera fiziskās dimensijas, ieskaitot taras svaru, maksimālo svaru, maksimālo tilpumu, garumu, platumu un svaru.</span><span class="sxs-lookup"><span data-stu-id="cbcca-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="cbcca-131">Atribūti ir pielāgoti lauki, kas ļauj jums pievienot papildu dimensijas konteinera tipam.</span><span class="sxs-lookup"><span data-stu-id="cbcca-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="cbcca-132">Laukā Konteinera veida kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="cbcca-133">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cbcca-134">Laukā Taras svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="cbcca-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="cbcca-135">Ievadiet skaitli laukā Maksimālais svars.</span><span class="sxs-lookup"><span data-stu-id="cbcca-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="cbcca-136">Laukā Tilpums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="cbcca-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="cbcca-137">Laukā Garums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="cbcca-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="cbcca-138">Ievadiet skaitli laukā Platums.</span><span class="sxs-lookup"><span data-stu-id="cbcca-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="cbcca-139">Ievadiet skaitli laukā Augstums.</span><span class="sxs-lookup"><span data-stu-id="cbcca-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="cbcca-140">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cbcca-140">Click Save.</span></span>
12. <span data-ttu-id="cbcca-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cbcca-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="cbcca-142">Iepakošanas profilu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cbcca-142">Set up packing profiles</span></span>
1. <span data-ttu-id="cbcca-143">Dodieties uz Noliktavas vadība > Iestatīšana > Iepakošana > Iepakošanas profili.</span><span class="sxs-lookup"><span data-stu-id="cbcca-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="cbcca-144">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="cbcca-144">Click New.</span></span>
3. <span data-ttu-id="cbcca-145">Ievadiet vērtību laukā Iepakošanas profila ID.</span><span class="sxs-lookup"><span data-stu-id="cbcca-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="cbcca-146">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cbcca-147">Laukā Iepakošanas slēgšanas profila ID ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="cbcca-148">Konteinera slēgšanas profila ID ir neobligāts, un ir noklusējuma konteinera slēgšanas profils šim iepakošanas profilam.</span><span class="sxs-lookup"><span data-stu-id="cbcca-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="cbcca-149">Laukā Konteinera ID režīms atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="cbcca-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="cbcca-150">Šī opcija nosaka, vai konteinera ID tiks automātiski ģenerēts, kad tiek izveidots konteineris, vai arī konteinera ID tiks ģenerēts manuāli.</span><span class="sxs-lookup"><span data-stu-id="cbcca-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="cbcca-151">Laukā Konteinera veids, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="cbcca-152">Konteinera veids tiks izmantots pēc noklusējuma, veidojot jaunu konteineru.</span><span class="sxs-lookup"><span data-stu-id="cbcca-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="cbcca-153">Konteinera slēgšanas izvēles rūtiņā, atlasiet Automātiski izveidot konteineru.</span><span class="sxs-lookup"><span data-stu-id="cbcca-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="cbcca-154">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cbcca-154">Click Save.</span></span>
10. <span data-ttu-id="cbcca-155">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cbcca-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="cbcca-156">Konteinera slēgšanas profilu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cbcca-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="cbcca-157">Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru slēgšanas profili.</span><span class="sxs-lookup"><span data-stu-id="cbcca-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="cbcca-158">Konteinera slēgšanas profili definē, kas notiek, ja konteiners tiek slēgts.</span><span class="sxs-lookup"><span data-stu-id="cbcca-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="cbcca-159">Jūs varat iestatīt vairākus konteinera slēgšanas profilus.</span><span class="sxs-lookup"><span data-stu-id="cbcca-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="cbcca-160">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="cbcca-160">Click New.</span></span>
3. <span data-ttu-id="cbcca-161">Laukā Iepakošanas slēgšanas profila ID ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="cbcca-162">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cbcca-163">Laukā Manifestācija, atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="cbcca-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="cbcca-164">Norādiet, vai manifestācija parādās, slēdzot konteinerus, vai apstiprinot sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="cbcca-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="cbcca-165">Ņemiet vērā, ka manifestācijai nepieciešama transportēšanas pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="cbcca-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="cbcca-166">Manifestācijai jābūt ieviestai transportēšanas programmās, lai tā strādātu.</span><span class="sxs-lookup"><span data-stu-id="cbcca-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="cbcca-167">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="cbcca-168">Laukā Noklusējuma galīgā sūtījuma atrašanās vieta, ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="cbcca-169">Tas ir vieta, uz kuru preces tiks pārvietotas pēc konteineru slēgšanas.</span><span class="sxs-lookup"><span data-stu-id="cbcca-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="cbcca-170">Šai vietai jābūt atrašanās vietas profilam, kas ir definēts Noliktavas parametros.</span><span class="sxs-lookup"><span data-stu-id="cbcca-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="cbcca-171">Laukā Svara vienība, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbcca-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="cbcca-172">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cbcca-172">Click Save.</span></span>


