---
title: Operācijas resursu izveide
description: Operācijas resurss izpilda projekta vai ražošanas procesa aktivitātes.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2e59b1e6a83d902df98a0b40ee6c572a6567f05
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212185"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="3bf62-103">Operācijas resursu izveide</span><span class="sxs-lookup"><span data-stu-id="3bf62-103">Create an operations resource</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3bf62-104">Operācijas resurss izpilda projekta vai ražošanas procesa aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="3bf62-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="3bf62-105">Šajā procedūrā ir parādīts, kā definēt operācijas resursu.</span><span class="sxs-lookup"><span data-stu-id="3bf62-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="3bf62-106">Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="3bf62-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="3bf62-107">Dodieties uz Resursi.</span><span class="sxs-lookup"><span data-stu-id="3bf62-107">Go to Resources.</span></span>
2. <span data-ttu-id="3bf62-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3bf62-108">Click New.</span></span>
3. <span data-ttu-id="3bf62-109">Laukā Resursi ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3bf62-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="3bf62-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3bf62-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="3bf62-111">Definēt noslodzes un patēriņa parametrus</span><span class="sxs-lookup"><span data-stu-id="3bf62-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="3bf62-112">Izvērsiet sadaļu Operācija.</span><span class="sxs-lookup"><span data-stu-id="3bf62-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="3bf62-113">Laukā Brāķis procentos ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="3bf62-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="3bf62-114">Laukā Iestatīšanas kategorija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3bf62-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="3bf62-115">Norādiet izmaksu kategoriju, kas nosaka, kā uzskaitīt iestatīšanas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="3bf62-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="3bf62-116">Laukā Izpildlaiks ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3bf62-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="3bf62-117">Norādiet izmaksu kategoriju, kas nosaka, kā uzskaitīt izpildes laika izmaksas.</span><span class="sxs-lookup"><span data-stu-id="3bf62-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="3bf62-118">Laukā Daudzuma kategorija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3bf62-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="3bf62-119">Norādiet izmaksu kategoriju, kas nosaka, kā uzskaitīt resursu izmaksas, pamatojoties uz izstrādes daudzumu.</span><span class="sxs-lookup"><span data-stu-id="3bf62-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="3bf62-120">Laukā Noslodzes vienība atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="3bf62-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="3bf62-121">Norādiet vienību, kādā izteikt operācijas resursa noslodzi.</span><span class="sxs-lookup"><span data-stu-id="3bf62-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="3bf62-122">Laukā Noslodze ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="3bf62-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="3bf62-123">Laukā Efektivitātes procenti ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="3bf62-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="3bf62-124">Norādiet efektivitāti, kādu sagaidāt no šī operācijas resursa.</span><span class="sxs-lookup"><span data-stu-id="3bf62-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="3bf62-125">Efektivitātes procentuālais daudzums pielāgo operācijas resursa caurlaidi un ietekmē resursam rezervēto laiku.</span><span class="sxs-lookup"><span data-stu-id="3bf62-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="3bf62-126">Laukā Operāciju plānošanas procenti ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="3bf62-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="3bf62-127">Norādiet maksimālo noslodzes procentuālo daudzumu tam operācijas resursam, kuru vēlaties izmantot operāciju plānošanā.</span><span class="sxs-lookup"><span data-stu-id="3bf62-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="3bf62-128">Laukā Ierobežota noslodze atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="3bf62-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="3bf62-129">Iestatiet šo opciju kā Jā, ja operācijas resurss ir jāplāno, pamatojoties uz faktiski pieejamo noslodzi, un ja ir jāņem vērā esošās noslodzes rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="3bf62-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="3bf62-130">Ja šī opcija ir iestatīta uz Nē, tad tiek pieņemts, ka operācijas resursam ir neierobežotā noslodze un resursam var tikt pārsniegta rezervācija.</span><span class="sxs-lookup"><span data-stu-id="3bf62-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="3bf62-131">Laukā Deficīta resurss atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="3bf62-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="3bf62-132">Definēt darba laikus</span><span class="sxs-lookup"><span data-stu-id="3bf62-132">Define working times</span></span>
1. <span data-ttu-id="3bf62-133">Izvērsiet sadaļu Kalendāri.</span><span class="sxs-lookup"><span data-stu-id="3bf62-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="3bf62-134">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="3bf62-134">Click Add.</span></span>
3. <span data-ttu-id="3bf62-135">Laukā Kalendārs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3bf62-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="3bf62-136">Norādiet darba laika kalendāru, kas nosaka resursa noslodzi (stundās).</span><span class="sxs-lookup"><span data-stu-id="3bf62-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="3bf62-137">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3bf62-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3bf62-138">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="3bf62-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="3bf62-139">Resursu iespēju definēšana</span><span class="sxs-lookup"><span data-stu-id="3bf62-139">Define resource capabilities</span></span>
1. <span data-ttu-id="3bf62-140">Izvērsiet sadaļu Iespējas.</span><span class="sxs-lookup"><span data-stu-id="3bf62-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="3bf62-141">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="3bf62-141">Click Add.</span></span>
    * <span data-ttu-id="3bf62-142">Iespēja ir operācijas resursu pieejamība konkrētas aktivitātes izpildīšanai.</span><span class="sxs-lookup"><span data-stu-id="3bf62-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="3bf62-143">Plānošanas programma resursus piešķir, katras aktivitātes resursu pieprasījumus saskaņojot ar pieejamo operāciju resursu iespējām.</span><span class="sxs-lookup"><span data-stu-id="3bf62-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="3bf62-144">Laukā Iespēja ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3bf62-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="3bf62-145">Laukā Līmenis ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="3bf62-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="3bf62-146">Norādiet prasmes līmeni, ar kādu šis resurss apstrādā iespēju.</span><span class="sxs-lookup"><span data-stu-id="3bf62-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="3bf62-147">Laukā Prioritāte ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="3bf62-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="3bf62-148">Norādiet operācijas resursa prioritāti attiecībā uz iespēju.</span><span class="sxs-lookup"><span data-stu-id="3bf62-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="3bf62-149">Kad plānojat pēc prioritātes, vispirms tiek atlasīti operācijas resursi ar augstāko prioritāti (zemāko skaitlisko vērtību).</span><span class="sxs-lookup"><span data-stu-id="3bf62-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="3bf62-150">Piešķirt resursu kādai resursu grupai</span><span class="sxs-lookup"><span data-stu-id="3bf62-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="3bf62-151">Izvērsiet sadaļu Resursu grupas.</span><span class="sxs-lookup"><span data-stu-id="3bf62-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="3bf62-152">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="3bf62-152">Click Add.</span></span>
    * <span data-ttu-id="3bf62-153">Resursu grupa operācijas resursiem nosaka vietu, ražošanas vienību un noliktavas kontekstu.</span><span class="sxs-lookup"><span data-stu-id="3bf62-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="3bf62-154">Operācijas resursu var plānot tikai tad, ja tas ir piešķirts kādai resursu grupai, un tikai tajā vietā, kur šī resursu grupa atrodas.</span><span class="sxs-lookup"><span data-stu-id="3bf62-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="3bf62-155">Laukā Resursu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3bf62-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="3bf62-156">Laukā Ievades novietojums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3bf62-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="3bf62-157">Norādiet noliktavas novietojumu, no kura operācijas resurss patērē materiālus.</span><span class="sxs-lookup"><span data-stu-id="3bf62-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  

