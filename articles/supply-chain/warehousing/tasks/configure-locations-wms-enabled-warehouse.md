--- 
title: "Vietu konfigurēšana noliktavā ar iespējotu NPS"
description: "Šajā ceļvedī parādīts, kā konfigurēt novietojuma iestatīšanu jaunai noliktavai ar iespējotu NPS (noliktavai, kas izmanto papildu noliktavas pārvaldības procesus)."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1082c86361180db84bb2b5c0b8158816f76a219e
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="314ee-103">Vietu konfigurēšana noliktavā ar iespējotu NPS</span><span class="sxs-lookup"><span data-stu-id="314ee-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="314ee-104">Šajā ceļvedī parādīts, kā konfigurēt novietojuma iestatīšanu jaunai noliktavai ar iespējotu NPS (noliktavai, kas izmanto papildu noliktavas pārvaldības procesus).</span><span class="sxs-lookup"><span data-stu-id="314ee-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="314ee-105">Procesu parasti veic noliktavas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="314ee-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="314ee-106">Šo ceļvedi varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai savus datus.</span><span class="sxs-lookup"><span data-stu-id="314ee-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="314ee-107">Priekšnosacījums: jābūt konfigurētai vismaz vienai vietai.</span><span class="sxs-lookup"><span data-stu-id="314ee-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="314ee-108">Jaunas noliktavas izveide</span><span class="sxs-lookup"><span data-stu-id="314ee-108">Create a new warehouse</span></span>
1. <span data-ttu-id="314ee-109">Dodieties uz Noliktavas.</span><span class="sxs-lookup"><span data-stu-id="314ee-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="314ee-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="314ee-110">Click New.</span></span>
3. <span data-ttu-id="314ee-111">Laukā Noliktava ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="314ee-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="314ee-113">Laukā Vieta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="314ee-114">Izvērsiet vai sakļaujiet sadaļu Noliktava.</span><span class="sxs-lookup"><span data-stu-id="314ee-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="314ee-115">Iestatiet opciju Izmantot noliktavas vadības procesus uz Jā.</span><span class="sxs-lookup"><span data-stu-id="314ee-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="314ee-116">Šis iestatījums ļauj palaist papildu noliktavas procesus, izmantojot noliktavas darbu un mobilās ierīces.</span><span class="sxs-lookup"><span data-stu-id="314ee-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="314ee-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="314ee-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="314ee-118">Novietojuma formāta definēšana</span><span class="sxs-lookup"><span data-stu-id="314ee-118">Define a location format</span></span>
1. <span data-ttu-id="314ee-119">Dodieties uz Novietojuma formāti.</span><span class="sxs-lookup"><span data-stu-id="314ee-119">Go to Location formats.</span></span>
    * <span data-ttu-id="314ee-120">Novietojuma formāti ir nosaukumdošanas sistēma, kuru izmanto, lai izveidotu unikālus un saskanīgus nosaukumus dažādām novietojuma nodalījuma pozīcijām, kas izmantotas noliktavā.</span><span class="sxs-lookup"><span data-stu-id="314ee-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="314ee-121">Var būt noderīgi izmantot atdalītājus kā daļu no novietojuma formāta, lai būtu vieglāk noteikt sastāvdaļu novietojumu, piemēram, ailes numuru.</span><span class="sxs-lookup"><span data-stu-id="314ee-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="314ee-122">Šajā piemērā mēs izveidosim nosaukumu ar četriem komponentiem.</span><span class="sxs-lookup"><span data-stu-id="314ee-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="314ee-123">Piemēram, tie var būt aile, statīvs, plaukts un nodalījums.</span><span class="sxs-lookup"><span data-stu-id="314ee-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="314ee-124">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="314ee-124">Click New.</span></span>
3. <span data-ttu-id="314ee-125">Laukā Novietojuma formāts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="314ee-126">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="314ee-127">Laukā Segmenta apraksts ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="314ee-128">Te ir aprakstīts, uz ko attiecas novietojuma nosaukuma pirmais komponents.</span><span class="sxs-lookup"><span data-stu-id="314ee-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="314ee-129">Piemēram, tā varētu būt aile.</span><span class="sxs-lookup"><span data-stu-id="314ee-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="314ee-130">Laukā Garums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="314ee-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="314ee-131">Tas nosaka, cik rakstzīmes var būt šai novietojuma nosaukuma daļai.</span><span class="sxs-lookup"><span data-stu-id="314ee-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="314ee-132">Ņemiet vērā, ka visu komponentu nosaukumā, tostarp atdalītāju, skaits nedrīkst pārsniegt 10 rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="314ee-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="314ee-133">Laukā Atdalītājs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="314ee-134">Tas nosaka, kura rakstzīme vai simbols tiek izmantots starp pirmo un otro nosaukuma komponentu.</span><span class="sxs-lookup"><span data-stu-id="314ee-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="314ee-135">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="314ee-135">Click New.</span></span>
9. <span data-ttu-id="314ee-136">Laukā Segmenta apraksts ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="314ee-137">Laukā Garums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="314ee-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="314ee-138">Laukā Atdalītājs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="314ee-139">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="314ee-139">Click New.</span></span>
13. <span data-ttu-id="314ee-140">Laukā Segmenta apraksts ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="314ee-141">Laukā Garums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="314ee-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="314ee-142">Laukā Atdalītājs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="314ee-143">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="314ee-143">Click New.</span></span>
17. <span data-ttu-id="314ee-144">Laukā Segmenta apraksts ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="314ee-145">Laukā Garums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="314ee-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="314ee-146">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="314ee-146">Click Save.</span></span>
20. <span data-ttu-id="314ee-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="314ee-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="314ee-148">Novietojuma tipu definēšana</span><span class="sxs-lookup"><span data-stu-id="314ee-148">Define location types</span></span>
1. <span data-ttu-id="314ee-149">Dodieties uz Novietojuma tipi.</span><span class="sxs-lookup"><span data-stu-id="314ee-149">Go to Location types.</span></span>
    * <span data-ttu-id="314ee-150">Novietojuma tipus var izmantot kā filtrēšanas opcijas, lai kontrolētu dažādus noliktavas pārvaldības procesus.</span><span class="sxs-lookup"><span data-stu-id="314ee-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="314ee-151">Jums vismaz ir nepieciešams izveidot sagatavošanas un galīgos nosūtīšanas novietojuma tipus, lai noteiktu izejošo noliktavas pārvaldības procesu.</span><span class="sxs-lookup"><span data-stu-id="314ee-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="314ee-152">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="314ee-152">Click New.</span></span>
3. <span data-ttu-id="314ee-153">Laukā Novietojuma tips ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="314ee-154">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="314ee-155">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="314ee-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="314ee-156">Novietojuma profila definēšana</span><span class="sxs-lookup"><span data-stu-id="314ee-156">Define location profile</span></span>
1. <span data-ttu-id="314ee-157">Dodieties uz Novietojuma profili.</span><span class="sxs-lookup"><span data-stu-id="314ee-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="314ee-158">Ir ļoti svarīgi definēt novietojuma profilus.</span><span class="sxs-lookup"><span data-stu-id="314ee-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="314ee-159">Grupētu novietojumu noslodzes var kontrolēt šeit, kā arī politikas, saistībā ar kurām krājums tiek uzglabāts un kā tas tiek glabāts.</span><span class="sxs-lookup"><span data-stu-id="314ee-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="314ee-160">Novietojumu profilus var izmantot kā filtrēšanas opcijas, lai kontrolētu dažādus noliktavas pārvaldības procesus.</span><span class="sxs-lookup"><span data-stu-id="314ee-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="314ee-161">Lai iespējotu noliktavas pārvaldības procesus, ir jāizveido vismaz lietotāja novietojuma profils.</span><span class="sxs-lookup"><span data-stu-id="314ee-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="314ee-162">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="314ee-162">Click New.</span></span>
3. <span data-ttu-id="314ee-163">Laukā Novietojuma profila ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="314ee-164">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="314ee-165">Laukā Novietojuma formāts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="314ee-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="314ee-166">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="314ee-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="314ee-167">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="314ee-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="314ee-168">Laukā Novietojuma tips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="314ee-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="314ee-169">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="314ee-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="314ee-170">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="314ee-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="314ee-171">Atzīmējiet izvēles rūtiņu Atļaut jauktus krājumu statusus vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="314ee-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="314ee-172">Aktivizējiet šo opciju, ja vēlaties atļaut jauktas krājumu statusa vērtības novietojumos, kas jāgrupē pēc šī novietojuma profila.</span><span class="sxs-lookup"><span data-stu-id="314ee-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="314ee-173">Atzīmējiet izvēles rūtiņu Ignorēt partijas dienu kārtulas vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="314ee-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="314ee-174">Iespējojiet šo opciju, lai ignorētu nosacījumu, par cik dienām var atšķirties krājumu partijas derīguma termiņi, lai atļautu to krājumu partiju sajaukšanu, kas nav pakļautas šim nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="314ee-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="314ee-175">Atzīmējiet izvēles rūtiņu Atļaut cikla inventarizāciju vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="314ee-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="314ee-176">Aktivizējiet šo opciju, ja vēlaties atļaut cikla inventarizācijas apstrādi visos novietojumos, kas tiks grupēti pēc šī novietojuma profila.</span><span class="sxs-lookup"><span data-stu-id="314ee-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="314ee-177">Izvērsiet vai sakļaujiet sadaļu Dimensijas.</span><span class="sxs-lookup"><span data-stu-id="314ee-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="314ee-178">Cilne Dimensijas ļauj definēt parametrus un metodes, lai iespējotu precīzus noslodzes aprēķinus katrā no novietojumiem.</span><span class="sxs-lookup"><span data-stu-id="314ee-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="314ee-179">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="314ee-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="314ee-180">Noliktavas vadības parametru iespējošana</span><span class="sxs-lookup"><span data-stu-id="314ee-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="314ee-181">Dodieties uz Noliktavas vadības parametri.</span><span class="sxs-lookup"><span data-stu-id="314ee-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="314ee-182">Lai varētu apstrādāt noliktavas darbu, ir jāiestata parametri lietotāja novietojuma profilam kā sagatavošanas posma novietojuma tipam un galīgās nosūtīšanas novietojuma tipam. Tiklīdz izejošais process beidzas jūsu definētajā gala nosūtīšanas novietojuma tipā, saistītās izejošās transakcijas tiks atjauninātas uz "Izdots".</span><span class="sxs-lookup"><span data-stu-id="314ee-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="314ee-183">Izvērsiet vai sakļaujiet sadaļu Novietojuma profili.</span><span class="sxs-lookup"><span data-stu-id="314ee-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="314ee-184">Laukā Lietotāja novietojums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="314ee-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="314ee-185">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="314ee-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="314ee-186">Izvērsiet vai sakļaujiet sadaļu Novietojuma veidi.</span><span class="sxs-lookup"><span data-stu-id="314ee-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="314ee-187">Laukā Sagatavošanas posma novietojuma tips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="314ee-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="314ee-188">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="314ee-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="314ee-189">Laukā Galīgās nosūtīšanas novietojuma tips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="314ee-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="314ee-190">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="314ee-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="314ee-191">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="314ee-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="314ee-192">Noliktavas zonu grupu definēšana</span><span class="sxs-lookup"><span data-stu-id="314ee-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="314ee-193">Dodieties uz Noliktavas zonu grupas.</span><span class="sxs-lookup"><span data-stu-id="314ee-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="314ee-194">Noliktavas zonas var izmantot kā opciju filtrus, lai kontrolētu dažādus noliktavas pārvaldības procesus.</span><span class="sxs-lookup"><span data-stu-id="314ee-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="314ee-195">Pirms varēsiet definēt zonu, jums ir nepieciešams izveidot zonu grupu.</span><span class="sxs-lookup"><span data-stu-id="314ee-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="314ee-196">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="314ee-196">Click New.</span></span>
3. <span data-ttu-id="314ee-197">Laukā Zonu grupas ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="314ee-198">Laukā Zonu grupas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="314ee-199">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="314ee-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="314ee-200">Noliktavas zonu definēšana</span><span class="sxs-lookup"><span data-stu-id="314ee-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="314ee-201">Dodieties uz Zonas.</span><span class="sxs-lookup"><span data-stu-id="314ee-201">Go to Zones.</span></span>
2. <span data-ttu-id="314ee-202">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="314ee-202">Click New.</span></span>
3. <span data-ttu-id="314ee-203">Laukā Zonas ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="314ee-204">Laukā Zonas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="314ee-205">Laukā Zonu grupas ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="314ee-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="314ee-206">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="314ee-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="314ee-207">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="314ee-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="314ee-208">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="314ee-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="314ee-209">Novietojumu izveide, izmantojot Novietojuma iestatīšanas vedni</span><span class="sxs-lookup"><span data-stu-id="314ee-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="314ee-210">Dodieties uz Novietojuma iestatīšanas vednis.</span><span class="sxs-lookup"><span data-stu-id="314ee-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="314ee-211">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="314ee-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="314ee-212">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="314ee-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="314ee-213">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="314ee-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="314ee-214">Laukā Zonas ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="314ee-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="314ee-215">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="314ee-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="314ee-216">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="314ee-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="314ee-217">Laukā Novietojuma profila ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="314ee-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="314ee-218">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="314ee-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="314ee-219">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="314ee-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="314ee-220">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="314ee-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="314ee-221">Laukā No numura ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="314ee-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="314ee-222">Vērtība laukā No numura un Līdz numuram nosaka, cik daudz novietojumi tiks izveidoti.</span><span class="sxs-lookup"><span data-stu-id="314ee-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="314ee-223">Piemēram, ja visās četrās novietojuma formāta rindās laukā No numura tiek iestatīta vērtība 1 un laukā Līdz numuram — vērtība 3, tiek izveidots 81 novietojums (3x3x3x3).</span><span class="sxs-lookup"><span data-stu-id="314ee-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="314ee-224">Laukā Līdz numuram ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="314ee-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="314ee-225">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="314ee-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="314ee-226">Laukā No numura ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="314ee-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="314ee-227">Laukā Līdz numuram ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="314ee-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="314ee-228">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="314ee-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="314ee-229">Laukā No numura ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="314ee-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="314ee-230">Laukā Līdz numuram ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="314ee-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="314ee-231">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="314ee-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="314ee-232">Laukā No numura ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="314ee-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="314ee-233">Laukā Līdz numuram ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="314ee-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="314ee-234">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="314ee-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="314ee-235">Novietojumu manuālā izveide</span><span class="sxs-lookup"><span data-stu-id="314ee-235">Create locations manually</span></span>
1. <span data-ttu-id="314ee-236">Dodieties uz Novietojumi.</span><span class="sxs-lookup"><span data-stu-id="314ee-236">Go to Locations.</span></span>
    * <span data-ttu-id="314ee-237">Novietojumus noliktavā ir viegli veidot manuāli.</span><span class="sxs-lookup"><span data-stu-id="314ee-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="314ee-238">Novietojuma nosaukums un Novietojuma profila ID ir obligātas vērtības.</span><span class="sxs-lookup"><span data-stu-id="314ee-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="314ee-239">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="314ee-239">Click New.</span></span>
3. <span data-ttu-id="314ee-240">Laukā Noliktava ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="314ee-241">Ierakstiet vērtību laukā Vieta.</span><span class="sxs-lookup"><span data-stu-id="314ee-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="314ee-242">Ņemiet vērā, ka šeit jūs veidojat jaunu novietojumu, tāpēc ir nepieciešams ierakstīt jaunu unikālu nosaukumu nevis atlasīt esošo.</span><span class="sxs-lookup"><span data-stu-id="314ee-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="314ee-243">Laukā Novietojuma profila ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="314ee-244">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="314ee-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="314ee-245">Pakas lielumu kategoriju izveide</span><span class="sxs-lookup"><span data-stu-id="314ee-245">Define Pack size categories</span></span>
1. <span data-ttu-id="314ee-246">Dodieties uz Pakas lielumu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="314ee-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="314ee-247">Pakas lielumu kategorijas var izmantot, lai grupētu krājumus, kuriem ir līdzīgs fiziskā iepakojuma lielums.</span><span class="sxs-lookup"><span data-stu-id="314ee-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="314ee-248">Šajā piemērā pakas lieluma kategorija tiks izmantota, lai kontrolētu izdošanas vietu ietilpību noteiktā noliktavas zonā.</span><span class="sxs-lookup"><span data-stu-id="314ee-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="314ee-249">Lūdzu ņemiet vērā, ka pakas lieluma kategorijas ID ir jāpiešķir izlaisto preču elementam, lai to varētu izmantot kā daļu no dimensijas ierobežojumu apstrādes.</span><span class="sxs-lookup"><span data-stu-id="314ee-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="314ee-250">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="314ee-250">Click New.</span></span>
3. <span data-ttu-id="314ee-251">Laukā Pakas lieluma kategorijas ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="314ee-252">Laukā Pakas lieluma kategorijas nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="314ee-253">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="314ee-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="314ee-254">Novietojuma dimensijas ierobežojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="314ee-254">Define location stocking limits</span></span>
1. <span data-ttu-id="314ee-255">Dodieties uz Novietojuma dimensijas ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="314ee-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="314ee-256">Novietojuma dimensiju ierobežojumi palīdz pārliecināties, ka darbs netiek izveidots, lai pieprasītu krājuma ievietošanu vietā, kurā nav fiziski iespējams šo krājumu ievietot.</span><span class="sxs-lookup"><span data-stu-id="314ee-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="314ee-257">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="314ee-257">Click New.</span></span>
3. <span data-ttu-id="314ee-258">Laukā Noliktava ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="314ee-259">Laukā Novietojuma profila ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="314ee-260">Laukā Pakas lieluma kategorijas ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="314ee-261">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="314ee-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="314ee-262">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="314ee-262">Click Save.</span></span>
8. <span data-ttu-id="314ee-263">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="314ee-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="314ee-264">Fiksētu izdošanas vietu definēšana</span><span class="sxs-lookup"><span data-stu-id="314ee-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="314ee-265">Dodieties uz Fiksētie novietojumi.</span><span class="sxs-lookup"><span data-stu-id="314ee-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="314ee-266">Varat definēt novietojumus, kuri tiks izmantoti katrai precei vai katram preces variantam.</span><span class="sxs-lookup"><span data-stu-id="314ee-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="314ee-267">Ir iespējams izveidot vairākus fiksētos novietojumus vienai un tai pašai precei vienā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="314ee-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="314ee-268">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="314ee-268">Click New.</span></span>
3. <span data-ttu-id="314ee-269">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="314ee-270">Laukā Noliktava ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="314ee-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="314ee-271">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="314ee-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="314ee-272">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="314ee-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="314ee-273">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="314ee-273">Close the page.</span></span>


