---
title: Jauna noliktavas izkārtojuma izveide
description: Šajā tēmā ir aprakstīts, kā iestatīt informāciju par vietām noliktavā.
author: perlynne
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09666e95cc90913f1bf8555b9ff2c48aa55369ed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433043"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="c124c-103">Jauna noliktavas izkārtojuma izveide</span><span class="sxs-lookup"><span data-stu-id="c124c-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c124c-104">Šajā tēmā ir aprakstīts, kā iestatīt informāciju par vietām noliktavā.</span><span class="sxs-lookup"><span data-stu-id="c124c-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="c124c-105">Tā attiecas tikai uz noliktavām, kas izveidotas, izmantojot “pamata noliktavu” krājumu vadības modulī, nevis uz noliktavām, kas izveidotas noliktavas vadības modulī.</span><span class="sxs-lookup"><span data-stu-id="c124c-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="c124c-106">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="c124c-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="c124c-107">Iestatīt noklusējuma novietojuma noslodzi</span><span class="sxs-lookup"><span data-stu-id="c124c-107">Set the default location capacity</span></span>
1. <span data-ttu-id="c124c-108">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Noliktavas vadība > Iestatīšana > Krājumu un noliktavas pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="c124c-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="c124c-109">Atlasiet cilni **Atrašanās vieta**.</span><span class="sxs-lookup"><span data-stu-id="c124c-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="c124c-110">Laukā **Standarta platums** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="c124c-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="c124c-111">Laukā **Standarta dziļums** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="c124c-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="c124c-112">Laukā **Standarta augstums** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="c124c-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="c124c-113">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c124c-113">Select **Save**.</span></span>
7. <span data-ttu-id="c124c-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c124c-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="c124c-115">Definēt novietojuma nosaukuma formātu</span><span class="sxs-lookup"><span data-stu-id="c124c-115">Define the location name format</span></span>
1. <span data-ttu-id="c124c-116">Navigācijas rūtī ejiet uz- **Moduļi > Krājumu pārvaldība > Iestatīšana > Krājumu sadalījums > Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="c124c-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="c124c-117">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c124c-117">Select **New**.</span></span>
3. <span data-ttu-id="c124c-118">Laukā **Noliktava** atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c124c-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="c124c-119">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c124c-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="c124c-120">Laukā **Vieta** uzmeklēšanā atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c124c-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="c124c-121">Pārslēdziet sadaļas **Atrašanās vietu nosaukumi** izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="c124c-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="c124c-122">Opcijas šajā sadaļā definē novietojumu nosaukumu noklusējuma formātu.</span><span class="sxs-lookup"><span data-stu-id="c124c-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="c124c-123">Mūsu piemērā būs ietverts ailes numurs, statīva numurs un plaukta numurs.</span><span class="sxs-lookup"><span data-stu-id="c124c-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="c124c-124">Opciju **Iekļaut aili** iestatiet kā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c124c-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="c124c-125">Opciju **Iekļaut statīvu** iestatiet kā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c124c-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="c124c-126">Laukam **Formāts** ierakstiet statīvam vērtību.</span><span class="sxs-lookup"><span data-stu-id="c124c-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="c124c-127">Opciju **Iekļaut plauktu** iestatiet kā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c124c-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="c124c-128">Laukam **Formāts** ierakstiet plauktam vērtību.</span><span class="sxs-lookup"><span data-stu-id="c124c-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="c124c-129">Definēt noliktavas novietojumus</span><span class="sxs-lookup"><span data-stu-id="c124c-129">Define warehouse locations</span></span>
1. <span data-ttu-id="c124c-130">Darbību rūtī atlasiet **Noliktava**.</span><span class="sxs-lookup"><span data-stu-id="c124c-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="c124c-131">Atlasiet **Atrašanās vietas vednis**.</span><span class="sxs-lookup"><span data-stu-id="c124c-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="c124c-132">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="c124c-132">Select **Next**.</span></span>
4. <span data-ttu-id="c124c-133">Noņemiet atzīmi opcijai **Izejošie doki**</span><span class="sxs-lookup"><span data-stu-id="c124c-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="c124c-134">Noņemiet atzīmi opcijai **Lielapjoma atrašanās vietas**</span><span class="sxs-lookup"><span data-stu-id="c124c-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="c124c-135">Atlasiet **Tālāk**, līdz aizejat uz opciju, kur var atlasīt **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="c124c-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="c124c-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c124c-136">Close the page.</span></span>
8. <span data-ttu-id="c124c-137">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="c124c-137">Refresh the page.</span></span>

