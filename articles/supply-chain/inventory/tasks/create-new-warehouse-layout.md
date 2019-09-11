---
title: Jauna noliktavas izkārtojuma izveide
description: Šajā tēmā ir aprakstīts, kā iestatīt informāciju par vietām noliktavā.
author: perlynne
manager: AnnBe
ms.date: 07/29/2019
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
ms.openlocfilehash: 302c028a93dfdb57972e4759abbbc4fdedabbd17
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867243"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="ae37d-103">Jauna noliktavas izkārtojuma izveide</span><span class="sxs-lookup"><span data-stu-id="ae37d-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ae37d-104">Šajā tēmā ir aprakstīts, kā iestatīt informāciju par vietām noliktavā.</span><span class="sxs-lookup"><span data-stu-id="ae37d-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="ae37d-105">Tā attiecas tikai uz noliktavām, kas izveidotas, izmantojot “pamata noliktavu” krājumu vadības modulī, nevis uz noliktavām, kas izveidotas noliktavas vadības modulī.</span><span class="sxs-lookup"><span data-stu-id="ae37d-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="ae37d-106">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="ae37d-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="ae37d-107">Iestatīt noklusējuma novietojuma noslodzi</span><span class="sxs-lookup"><span data-stu-id="ae37d-107">Set the default location capacity</span></span>
1. <span data-ttu-id="ae37d-108">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Noliktavas vadība > Iestatīšana > Krājumu un noliktavas pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="ae37d-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="ae37d-109">Atlasiet cilni **Atrašanās vieta**.</span><span class="sxs-lookup"><span data-stu-id="ae37d-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="ae37d-110">Laukā **Standarta platums** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="ae37d-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="ae37d-111">Laukā **Standarta dziļums** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="ae37d-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="ae37d-112">Laukā **Standarta augstums** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="ae37d-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="ae37d-113">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ae37d-113">Select **Save**.</span></span>
7. <span data-ttu-id="ae37d-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ae37d-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="ae37d-115">Definēt novietojuma nosaukuma formātu</span><span class="sxs-lookup"><span data-stu-id="ae37d-115">Define the location name format</span></span>
1. <span data-ttu-id="ae37d-116">Navigācijas rūtī ejiet uz- **Moduļi > Krājumu pārvaldība > Iestatīšana > Krājumu sadalījums > Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="ae37d-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="ae37d-117">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ae37d-117">Select **New**.</span></span>
3. <span data-ttu-id="ae37d-118">Laukā **Noliktava** atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ae37d-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="ae37d-119">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ae37d-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ae37d-120">Laukā **Vieta** uzmeklēšanā atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ae37d-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="ae37d-121">Pārslēdziet sadaļas **Atrašanās vietu nosaukumi** izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="ae37d-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="ae37d-122">Opcijas šajā sadaļā definē novietojumu nosaukumu noklusējuma formātu.</span><span class="sxs-lookup"><span data-stu-id="ae37d-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="ae37d-123">Mūsu piemērā būs ietverts ailes numurs, statīva numurs un plaukta numurs.</span><span class="sxs-lookup"><span data-stu-id="ae37d-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="ae37d-124">Opciju **Iekļaut aili** iestatiet kā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="ae37d-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="ae37d-125">Opciju **Iekļaut statīvu** iestatiet kā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="ae37d-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="ae37d-126">Laukam **Formāts** ierakstiet statīvam vērtību.</span><span class="sxs-lookup"><span data-stu-id="ae37d-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="ae37d-127">Opciju **Iekļaut plauktu** iestatiet kā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="ae37d-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="ae37d-128">Laukam **Formāts** ierakstiet plauktam vērtību.</span><span class="sxs-lookup"><span data-stu-id="ae37d-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="ae37d-129">Definēt noliktavas novietojumus</span><span class="sxs-lookup"><span data-stu-id="ae37d-129">Define warehouse locations</span></span>
1. <span data-ttu-id="ae37d-130">Darbību rūtī atlasiet **Noliktava**.</span><span class="sxs-lookup"><span data-stu-id="ae37d-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="ae37d-131">Atlasiet **Atrašanās vietas vednis**.</span><span class="sxs-lookup"><span data-stu-id="ae37d-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="ae37d-132">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="ae37d-132">Select **Next**.</span></span>
4. <span data-ttu-id="ae37d-133">Noņemiet atzīmi opcijai **Izejošie doki**</span><span class="sxs-lookup"><span data-stu-id="ae37d-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="ae37d-134">Noņemiet atzīmi opcijai **Lielapjoma atrašanās vietas**</span><span class="sxs-lookup"><span data-stu-id="ae37d-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="ae37d-135">Atlasiet **Tālāk**, līdz aizejat uz opciju, kur var atlasīt **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="ae37d-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="ae37d-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ae37d-136">Close the page.</span></span>
8. <span data-ttu-id="ae37d-137">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="ae37d-137">Refresh the page.</span></span>

