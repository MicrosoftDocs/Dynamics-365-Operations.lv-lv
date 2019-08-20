---
title: Jauna noliktavas izkārtojuma izveide
description: Šajā procedūrā ir parādīts, kā iestatīt informāciju par novietojumiem noliktavā.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0a52c5d68816a81a94db019387b9ea3ec3efc5a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845526"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="78adf-103">Jauna noliktavas izkārtojuma izveide</span><span class="sxs-lookup"><span data-stu-id="78adf-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="78adf-104">Šajā procedūrā ir parādīts, kā iestatīt informāciju par novietojumiem noliktavā.</span><span class="sxs-lookup"><span data-stu-id="78adf-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="78adf-105">Tā attiecas tikai uz noliktavām, kas izveidotas, izmantojot “pamata noliktavu” krājumu vadības modulī, nevis uz noliktavām, kas izveidotas noliktavas vadības modulī.</span><span class="sxs-lookup"><span data-stu-id="78adf-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="78adf-106">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="78adf-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="78adf-107">Iestatīt noklusējuma novietojuma noslodzi</span><span class="sxs-lookup"><span data-stu-id="78adf-107">Set the default location capacity</span></span>
1. <span data-ttu-id="78adf-108">Pārejiet uz sadaļu Krājumu pārvaldība > Iestatījumi > Krājumu un noliktavas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="78adf-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="78adf-109">Noklikšķiniet uz cilnes Novietojumi.</span><span class="sxs-lookup"><span data-stu-id="78adf-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="78adf-110">Laukā Standarta platums ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="78adf-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="78adf-111">Laukā Standarta dziļums ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="78adf-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="78adf-112">Laukā Standarta augstums ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="78adf-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="78adf-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="78adf-113">Click Save.</span></span>
7. <span data-ttu-id="78adf-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="78adf-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="78adf-115">Definēt novietojuma nosaukuma formātu</span><span class="sxs-lookup"><span data-stu-id="78adf-115">Define the location name format</span></span>
1. <span data-ttu-id="78adf-116">Doties uz Krājumu vadība > Iestatījumi > Noliktavu sadalījums > Noliktavas.</span><span class="sxs-lookup"><span data-stu-id="78adf-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="78adf-117">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="78adf-117">Click New.</span></span>
3. <span data-ttu-id="78adf-118">Laukā Noliktava ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="78adf-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="78adf-119">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="78adf-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="78adf-120">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="78adf-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="78adf-121">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="78adf-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="78adf-122">Pārslēdziet sadaļas Novietojumu nosaukumi izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="78adf-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="78adf-123">Opcijas šajā sadaļā definē novietojumu nosaukumu noklusējuma formātu.</span><span class="sxs-lookup"><span data-stu-id="78adf-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="78adf-124">Mūsu piemērā būs ietverts ailes numurs, statīva numurs un plaukta numurs.</span><span class="sxs-lookup"><span data-stu-id="78adf-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="78adf-125">Opcijas Iekļaut aili vērtību iestatiet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="78adf-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="78adf-126">Opcijas Iekļaut statīvu vērtību iestatiet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="78adf-126">Set the Include rack option to Yes.</span></span> 
10. <span data-ttu-id="78adf-127">Statīva laukā Formāts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="78adf-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="78adf-128">Piemēram: -##</span><span class="sxs-lookup"><span data-stu-id="78adf-128">For example: -##</span></span>  
11. <span data-ttu-id="78adf-129">Opcijas Iekļaut plauktu vērtību iestatiet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="78adf-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="78adf-130">Plaukta laukā Formāts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="78adf-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="78adf-131">Piemēram: -##</span><span class="sxs-lookup"><span data-stu-id="78adf-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="78adf-132">Definēt noliktavas novietojumus</span><span class="sxs-lookup"><span data-stu-id="78adf-132">Define warehouse locations</span></span>
1. <span data-ttu-id="78adf-133">Darbību rūtī noklikšķiniet uz Noliktava.</span><span class="sxs-lookup"><span data-stu-id="78adf-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="78adf-134">Noklikšķiniet uz vienuma Novietojumu ceļvedis.</span><span class="sxs-lookup"><span data-stu-id="78adf-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="78adf-135">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="78adf-135">Click Next.</span></span>
4. <span data-ttu-id="78adf-136">Noņemiet atzīmi opcijai Nosūtīšanas doki</span><span class="sxs-lookup"><span data-stu-id="78adf-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="78adf-137">Notīriet atzīmi opcijai Uzkrāšanas vietas</span><span class="sxs-lookup"><span data-stu-id="78adf-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="78adf-138">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="78adf-138">Click Next.</span></span>
7. <span data-ttu-id="78adf-139">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="78adf-139">Click Next.</span></span>
8. <span data-ttu-id="78adf-140">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="78adf-140">Click Next.</span></span>
9. <span data-ttu-id="78adf-141">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="78adf-141">Click Next.</span></span>
10. <span data-ttu-id="78adf-142">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="78adf-142">Click Next.</span></span>
11. <span data-ttu-id="78adf-143">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="78adf-143">Click Next.</span></span>
12. <span data-ttu-id="78adf-144">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="78adf-144">Click Next.</span></span>
    * <span data-ttu-id="78adf-145">Ņemiet vērā, ka šajā lapā rādītie fiziskie izmēri ir tie paši, ko iestatāt šīs procedūras sākumā.</span><span class="sxs-lookup"><span data-stu-id="78adf-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="78adf-146">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="78adf-146">Click Next.</span></span>
14. <span data-ttu-id="78adf-147">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="78adf-147">Click Finish.</span></span>
15. <span data-ttu-id="78adf-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="78adf-148">Close the page.</span></span>
16. <span data-ttu-id="78adf-149">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="78adf-149">Refresh the page.</span></span>

