---
title: "Noslodzes izmantošanas plānošana"
description: "Šajā tēmā ir paskaidrots, kā iestatīt un plānot noslodzi noliktavai."
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d52ad452c615a61739582431fcd100a7efa3d93a
ms.openlocfilehash: 350666cee8f2643c53e9eed8ee73299bbea1e757
ms.contentlocale: lv-lv
ms.lasthandoff: 04/26/2018

---

# <a name="schedule-load-utilization"></a><span data-ttu-id="26310-103">Noslodzes izmantošanas plānošana</span><span class="sxs-lookup"><span data-stu-id="26310-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="26310-104">Varat ieplānot noslodzes izmantošanu atlasītajiem novietojumu veidiem, kā arī varat projektēt pašreizējo un turpmāko noslodzes izmantošanu.</span><span class="sxs-lookup"><span data-stu-id="26310-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="26310-105">Varat projektēt noslodzi vienai vai vairākām vietām, (zonas vai noliktavas) noslodzes vienībām vai zonas un noliktavas kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="26310-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="26310-106">Noliktavas vai vietas noslodzes plānošana un skatīšana</span><span class="sxs-lookup"><span data-stu-id="26310-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="26310-107">Lai plānotu noslodzi vietās, noliktavās vai zonās, veidojiet telpas izmantošanas iestatījumus un saistiet tos ar vispārējo plānu.</span><span class="sxs-lookup"><span data-stu-id="26310-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="26310-108">Telpas izmantošanas iestatījumos tiek izmantoti novietojuma veidi, piemēram, **Uzkrāšanas vieta** un **Izdošanas vieta**, lai norādītu, kā ir jāprojektē telpas lietojums.</span><span class="sxs-lookup"><span data-stu-id="26310-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="26310-109">Jūs norādāt arī noliktavas noslodzes režīmu, piemēram, **Zona**.</span><span class="sxs-lookup"><span data-stu-id="26310-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="26310-110">Nākotnes telpas izmantošana tiek plānota, pamatojoties uz informāciju, kas tiek aprēķināta saistītajā vispārējā plānā.</span><span class="sxs-lookup"><span data-stu-id="26310-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="26310-111">Vispārējie plāni prognozē ienākošo un izejošo pasūtījumu resursu plānošanu attiecībā uz ražošanu un operācijām.</span><span class="sxs-lookup"><span data-stu-id="26310-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="26310-112">Pieejamās vietas projekcijas pamatā ir relācija starp telpas izmantošanas iestatījumiem un atlasīto vispārējo plānu.</span><span class="sxs-lookup"><span data-stu-id="26310-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="26310-113">Izmantojot noslodzes režīmu, kas ir atlasīts telpas izmantošanas iestatījumos, varat norādīt, vai noslodze ir jāprojektē katrai noliktavai vai zonai, vai arī projektēšanā ir jāietver informācija gan par noliktavām, gan par zonām.</span><span class="sxs-lookup"><span data-stu-id="26310-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="26310-114">Varat arī norādīt, vai bloķētie novietojumi ir jāizslēdz no noslodzes izmantošanas aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="26310-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="26310-115">Telpas izmantošanu varat projektēt, ģenerējot pārskatu **Noliktavas noslodzes izmantošana**.</span><span class="sxs-lookup"><span data-stu-id="26310-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="26310-116">Ģenerējot šo pārskatu, varat norādīt, vai noslodzes izmantošana ir jāprojektē katrai vietai, vairākām vietām vai atlasītajai noslodzes vienībai, piemēram, zonai vai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="26310-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="26310-117">Telpas izmantošanas iestatījumu izveidošana noliktavai</span><span class="sxs-lookup"><span data-stu-id="26310-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="26310-118">Atlasiet **Krājumu pārvaldība** \> **Iestatīšana** \> **Noliktavas uzraudzība** \> **Vietas izmantošana**.</span><span class="sxs-lookup"><span data-stu-id="26310-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="26310-119">Atlasiet **Jauns**, lai izveidotu telpas izmantošanas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="26310-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="26310-120">Norādiet jaunā iestatījuma ID un nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="26310-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="26310-121">Laukā **Noliktavas noslodzes režīms** atlasiet, vai telpas izmantošanas apskatā ir jārāda informācija pēc noliktavas, pēc zonas vai pēc noliktavas un zonas.</span><span class="sxs-lookup"><span data-stu-id="26310-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="26310-122">Lai no pieejamās vietas aprēķiniem izslēgtu bloķētos krājumu novietojumus, opciju **Izslēgt bloķētos novietojumus** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="26310-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="26310-123">Varat bloķēt krājumu novietojumu ieejas un izejas plūsmām, norādot novietojuma bloķēšanas iemeslu lapas **Krājumu novietojumi** kopsavilkuma cilnes **Citi** laukā **Saņemšana bloķēta** vai **Izdošana bloķēta**.</span><span class="sxs-lookup"><span data-stu-id="26310-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="26310-124">Kopsavilkuma cilnē **Novietojuma veids** atlasiet novietojumu veidus, kas jāiekļauj telpas izmantošanas aprēķinos.</span><span class="sxs-lookup"><span data-stu-id="26310-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="26310-125">Prognozēšanai ir jāatlasa vismaz viens atrašanās vietas veids.</span><span class="sxs-lookup"><span data-stu-id="26310-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="26310-126">Telpas izmantošanas iestatījumu saistīšana ar vispārēju plānu</span><span class="sxs-lookup"><span data-stu-id="26310-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="26310-127">Atlasiet **Krājumu pārvaldība** \> **Periodiskie uzdevumi** \> **Ieplānot noslodzes izmantošanu**.</span><span class="sxs-lookup"><span data-stu-id="26310-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="26310-128">Atlasiet vispārēju plānu laukā **Vispārējais plāns**.</span><span class="sxs-lookup"><span data-stu-id="26310-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="26310-129">Laukā **Dienu skaits** norādiet dienu skaitu, kas ir jāietver pašreizējo un turpmāko darba slodžu projektēšanā.</span><span class="sxs-lookup"><span data-stu-id="26310-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="26310-130">Laukā **Telpas izmantošana** atlasiet telpas izmantošanas iestatījumus, kurus izmantot pašreizējo un turpmāko darba slodžu projektēšanā.</span><span class="sxs-lookup"><span data-stu-id="26310-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="26310-131">Noslodzes izmantošanas projekcijas norādīšana un informācijas skatīšana</span><span class="sxs-lookup"><span data-stu-id="26310-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="26310-132">Atlasiet **Krājumu pārvaldība** \> **Pieprasījumi un pārskati** \> **Fizisko krājumu pārskati** \> **Noliktavas noslodzes izmantošana**.</span><span class="sxs-lookup"><span data-stu-id="26310-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="26310-133">Laukā **Rādīt pēc** atlasiet kādu no tālāk aprakstītajiem telpas izmantošanas projektēšanas līmeņiem.</span><span class="sxs-lookup"><span data-stu-id="26310-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="26310-134">**Vieta** — projektēt telpas izmantošanu katrai vietai.</span><span class="sxs-lookup"><span data-stu-id="26310-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="26310-135">Šāda prognoze ir noderīga, ja, piemēram, vēlaties skatīt visas vietai paredzētās noliktavas, lai varētu līdzsvarot telpas izmantošanu noliktavās.</span><span class="sxs-lookup"><span data-stu-id="26310-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="26310-136">**Noslodzes vienība** — projektēt telpas izmantošanu zonām vai noliktavām.</span><span class="sxs-lookup"><span data-stu-id="26310-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="26310-137">Pēc tam pieejamā telpa tiek projektēta atbilstoši vērtībai, kuru atlasījāt laukā **Noliktavas noslodzes režīms**, lapā **Telpas izmantošana**, kad izveidojāt telpu izmantošanas iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="26310-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="26310-138">Izpildiet vienu no tālāk aprakstītajām darbībām, ņemot vērā iepriekšējā darbībā atlasīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="26310-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="26310-139">Ja laukā **Rādīt pēc** atlasījāt vērtību **Vieta**, ir pieejams lauks **Vieta**.</span><span class="sxs-lookup"><span data-stu-id="26310-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="26310-140">Atlasiet vienu vai vairākas vietas, kas ir jāiekļauj projektēšanā.</span><span class="sxs-lookup"><span data-stu-id="26310-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="26310-141">Ja laukā **Rādīt pēc** atlasījāt vērtību **Noslodzes vienība**, ir pieejams lauks **Noslodzes vienība**.</span><span class="sxs-lookup"><span data-stu-id="26310-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="26310-142">Atlasiet noslodzes vienību.</span><span class="sxs-lookup"><span data-stu-id="26310-142">Select the load unit.</span></span>

4. <span data-ttu-id="26310-143">Laukā **Noslodzes veids** atlasiet **Tilpums** vai **Svars**, lai norādītu noliktavas pārvaldības struktūrvienību, kurai projektēt telpu.</span><span class="sxs-lookup"><span data-stu-id="26310-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="26310-144">Laukā **Telpu izmantošanas iestatījumi** atlasiet telpas izmantošanas iestatījumus, uz kā ir jābalsta projektēšana.</span><span class="sxs-lookup"><span data-stu-id="26310-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>

