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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c8cec376bcc8c50fb9a78bed039505608cd7782d
ms.contentlocale: lv-lv
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="d3753-103">Manuālas iepakošanas iestatīšana (tikai 2016. gada februāris un maijs)</span><span class="sxs-lookup"><span data-stu-id="d3753-103">Set up manual packing (February & May 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3753-104">Iepakošanas procesu ļauj jums pārbaudīt un iepakot preces konteineros.</span><span class="sxs-lookup"><span data-stu-id="d3753-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="d3753-105">Šajā procesā, noliktavas darbinieki izdod preces no uzglabāšanas vietām un pārvieto tās uz iepakojuma staciju, kur tie pārbauda krājumu daudzumus un veidus, un piešķir tiem atbilstošus konteinerus.</span><span class="sxs-lookup"><span data-stu-id="d3753-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="d3753-106">Kad konteiners ir pilns, to var aizvērt un pārvietot to uz nosūtīšanas doku, un preces ir gatavas nosūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="d3753-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="d3753-107">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="d3753-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="d3753-108">Šī procedūra ir paredzēta tikai 2016. gada februāra un 2016. gada maija Dynamics 365 for Operations versijām.</span><span class="sxs-lookup"><span data-stu-id="d3753-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="d3753-109">Iestatīt novietojuma profilus</span><span class="sxs-lookup"><span data-stu-id="d3753-109">Set up location profiles</span></span>
1. <span data-ttu-id="d3753-110">Dodieties uz Noliktavas vadība > Iestatīšana > Noliktava > Novietojumu profili.</span><span class="sxs-lookup"><span data-stu-id="d3753-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="d3753-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d3753-111">Click New.</span></span>
    * <span data-ttu-id="d3753-112">Atrašanās vietas profils tiek izmantots iepakošanas stacijās, un satur informāciju un noteikumus par atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="d3753-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="d3753-113">Laukā Novietojuma profila ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="d3753-114">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d3753-115">Laukā Atrašanās vietas formāts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="d3753-116">Laukā Atrašanās vietas tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="d3753-117">Laukā Atļaut jauktus krājumus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="d3753-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="d3753-118">Laukā Atļaut jauktus krājumu statusus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="d3753-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="d3753-119">Atlasiet Jā, laukā Ignorēt partijas dienu kārtulas.</span><span class="sxs-lookup"><span data-stu-id="d3753-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="d3753-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d3753-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="d3753-121">Noliktavas vadības parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d3753-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="d3753-122">Doties uz Noliktavas vadība > Iestatīšana > Noliktavas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="d3753-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="d3753-123">Klikšķiniet cilni Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="d3753-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="d3753-124">Laukā Iepakošanas atrašanās vietas profila ID ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="d3753-125">Atlasiet atrašanās vietas profilu, kuru vēlaties izmantot iepakošanai.</span><span class="sxs-lookup"><span data-stu-id="d3753-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="d3753-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d3753-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="d3753-127">Konteinera veidu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d3753-127">Set up container types</span></span>
1. <span data-ttu-id="d3753-128">Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru veidi.</span><span class="sxs-lookup"><span data-stu-id="d3753-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="d3753-129">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d3753-129">Click New.</span></span>
    * <span data-ttu-id="d3753-130">Jūs varat noteikt konteineru tipus izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="d3753-130">You can define the types of containers to use.</span></span> <span data-ttu-id="d3753-131">Var norādīt konteinera fiziskās dimensijas, ieskaitot taras svaru, maksimālo svaru, maksimālo tilpumu, garumu, platumu un svaru.</span><span class="sxs-lookup"><span data-stu-id="d3753-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="d3753-132">Atribūti ir pielāgoti lauki, kas ļauj jums pievienot papildu dimensijas konteinera tipam.</span><span class="sxs-lookup"><span data-stu-id="d3753-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="d3753-133">Laukā Konteinera veida kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="d3753-134">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d3753-135">Laukā Taras svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="d3753-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="d3753-136">Ievadiet skaitli laukā Maksimālais svars.</span><span class="sxs-lookup"><span data-stu-id="d3753-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="d3753-137">Laukā Tilpums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="d3753-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="d3753-138">Laukā Garums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="d3753-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="d3753-139">Ievadiet skaitli laukā Platums.</span><span class="sxs-lookup"><span data-stu-id="d3753-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="d3753-140">Ievadiet skaitli laukā Augstums.</span><span class="sxs-lookup"><span data-stu-id="d3753-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="d3753-141">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d3753-141">Click Save.</span></span>
12. <span data-ttu-id="d3753-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d3753-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="d3753-143">Iepakošanas profilu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d3753-143">Set up packing profiles</span></span>
1. <span data-ttu-id="d3753-144">Dodieties uz Noliktavas vadība > Iestatīšana > Iepakošana > Iepakošanas profili.</span><span class="sxs-lookup"><span data-stu-id="d3753-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="d3753-145">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d3753-145">Click New.</span></span>
3. <span data-ttu-id="d3753-146">Ievadiet vērtību laukā Iepakošanas profila ID.</span><span class="sxs-lookup"><span data-stu-id="d3753-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="d3753-147">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d3753-148">Laukā Iepakošanas slēgšanas profila ID ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="d3753-149">Konteinera slēgšanas profila ID ir neobligāts, un ir noklusējuma konteinera slēgšanas profils šim iepakošanas profilam.</span><span class="sxs-lookup"><span data-stu-id="d3753-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="d3753-150">Laukā Konteinera ID režīms atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="d3753-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="d3753-151">Šī opcija nosaka, vai konteinera ID tiks automātiski ģenerēts, kad tiek izveidots konteineris, vai arī konteinera ID tiks ģenerēts manuāli.</span><span class="sxs-lookup"><span data-stu-id="d3753-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="d3753-152">Laukā Konteinera veids, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="d3753-153">Konteinera veids tiks izmantots pēc noklusējuma, veidojot jaunu konteineru.</span><span class="sxs-lookup"><span data-stu-id="d3753-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="d3753-154">Konteinera slēgšanas izvēles rūtiņā, atlasiet Automātiski izveidot konteineru.</span><span class="sxs-lookup"><span data-stu-id="d3753-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="d3753-155">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d3753-155">Click Save.</span></span>
10. <span data-ttu-id="d3753-156">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d3753-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="d3753-157">Konteinera slēgšanas profilu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d3753-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="d3753-158">Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru slēgšanas profili.</span><span class="sxs-lookup"><span data-stu-id="d3753-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="d3753-159">Konteinera slēgšanas profili definē, kas notiek, ja konteiners tiek slēgts.</span><span class="sxs-lookup"><span data-stu-id="d3753-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="d3753-160">Jūs varat iestatīt vairākus konteinera slēgšanas profilus.</span><span class="sxs-lookup"><span data-stu-id="d3753-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="d3753-161">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d3753-161">Click New.</span></span>
3. <span data-ttu-id="d3753-162">Laukā Iepakošanas slēgšanas profila ID ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="d3753-163">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d3753-164">Laukā Manifestācija, atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="d3753-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="d3753-165">Norādiet, vai manifestācija parādās, slēdzot konteinerus, vai apstiprinot sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d3753-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="d3753-166">Ņemiet vērā, ka manifestācijai nepieciešama transportēšanas pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="d3753-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="d3753-167">Manifestācijai jābūt ieviestai transportēšanas programmās, lai tā strādātu.</span><span class="sxs-lookup"><span data-stu-id="d3753-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="d3753-168">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="d3753-169">Laukā Noklusējuma galīgā sūtījuma atrašanās vieta, ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="d3753-170">Tas ir vieta, uz kuru preces tiks pārvietotas pēc konteineru slēgšanas.</span><span class="sxs-lookup"><span data-stu-id="d3753-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="d3753-171">Šai vietai jābūt atrašanās vietas profilam, kas ir definēts Noliktavas parametros.</span><span class="sxs-lookup"><span data-stu-id="d3753-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="d3753-172">Laukā Svara vienība, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3753-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="d3753-173">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d3753-173">Click Save.</span></span>


