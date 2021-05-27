---
title: Nosūtīšanas konteineri
description: Šajā tēmā ir aprakstīts, kā iestatīt nosūtīšanas konteinerus Kopējo izmaksu modulim.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 8f86f3603b64093214bb7cf7d165ba0fc2229ca3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021544"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="708c8-103">Nosūtīšanas konteinera iestatījumi</span><span class="sxs-lookup"><span data-stu-id="708c8-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="708c8-104">Šajā tēmā ir aprakstīts, kā iestatīt nosūtīšanas konteinerus **Kopējo izmaksu** modulim.</span><span class="sxs-lookup"><span data-stu-id="708c8-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="708c8-105">Konteinera veidu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="708c8-105">Set up shipping container types</span></span>

<span data-ttu-id="708c8-106">Nosūtīšanas konteinera veidi nosaka nosūtīšanas konteineru tipus, kuri ir pieejami izmantošanai nosūtīšanas un reisu laikā.</span><span class="sxs-lookup"><span data-stu-id="708c8-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="708c8-107">Lai strādātu ar nosūtīšanas konteineru tipiem, dodieties uz **Kopējās izmaksas \> Konteineru iestatījumi \> Nosūtīšanas konteineru veidi**.</span><span class="sxs-lookup"><span data-stu-id="708c8-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="708c8-108">Tur varat skatīt, pievienot un noņemt ierakstus saviem konteineru tipiem.</span><span class="sxs-lookup"><span data-stu-id="708c8-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="708c8-109">Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.</span><span class="sxs-lookup"><span data-stu-id="708c8-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="708c8-110">Lauks</span><span class="sxs-lookup"><span data-stu-id="708c8-110">Field</span></span> | <span data-ttu-id="708c8-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="708c8-111">Description</span></span> |
|---|---|
| <span data-ttu-id="708c8-112">Nosūtīšanas konteinera veids</span><span class="sxs-lookup"><span data-stu-id="708c8-112">Shipping container type</span></span> | <span data-ttu-id="708c8-113">Ievadiet nosūtīšanas konteinera tipam unikālu ID nosaukumu/numuru.</span><span class="sxs-lookup"><span data-stu-id="708c8-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="708c8-114">Apraksts</span><span class="sxs-lookup"><span data-stu-id="708c8-114">Description</span></span> | <span data-ttu-id="708c8-115">Ievadiet nosūtīšanas konteinera tipa aprakstu.</span><span class="sxs-lookup"><span data-stu-id="708c8-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="708c8-116">Tilpums</span><span class="sxs-lookup"><span data-stu-id="708c8-116">Volume</span></span> | <span data-ttu-id="708c8-117">Ievadiet maksimālo tilpumu, kas ir atļauts šī tipa nosūtīšanas konteineros.</span><span class="sxs-lookup"><span data-stu-id="708c8-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="708c8-118">Lielums</span><span class="sxs-lookup"><span data-stu-id="708c8-118">Weight</span></span> | <span data-ttu-id="708c8-119">Ievadiet maksimālo svaru, kas ir atļauts šī tipa nosūtīšanas konteineros.</span><span class="sxs-lookup"><span data-stu-id="708c8-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="708c8-120">Atgriežams</span><span class="sxs-lookup"><span data-stu-id="708c8-120">Returnable</span></span> | <span data-ttu-id="708c8-121">Norādiet, vai šāda veida sūtījuma konteinerus var atgriezt kreditoram pēc tam, kad tie ir izmantoti reisa laikā.</span><span class="sxs-lookup"><span data-stu-id="708c8-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="708c8-122">Ja šī opcija ir iestatīta kā *Jā*, šī tipa pārvadāšanas konteineru atgriešanai uz izcelsmes ostu var tikt piemērotas papildu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="708c8-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="708c8-123">Nosūtīšanas konteineru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="708c8-123">Set up shipping containers</span></span>

<span data-ttu-id="708c8-124">Jūs izmantojat nosūtīšanas konteinera ierakstus, lai identificētu katru konteineru, ko izmantojat reisu laikā.</span><span class="sxs-lookup"><span data-stu-id="708c8-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="708c8-125">Kad izveidojat reisu, varat tam atlasīt īpašu konteineru visu šeit definēto nosūtīšanas konteinera ierakstu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="708c8-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="708c8-126">Šī funkcija ir īpaši noderīga, ja jūsu uzņēmumam pieder savi nosūtīšanas konteineri.</span><span class="sxs-lookup"><span data-stu-id="708c8-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="708c8-127">Jums nav jāievada nosūtīšanas konteineru numuri nosūtīšanas konteineriem, kas tiks izmantoti tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="708c8-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="708c8-128">Tā vietā varat pievienot nosūtīšanas konteinera numuru, izveidojot reisu.</span><span class="sxs-lookup"><span data-stu-id="708c8-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="708c8-129">Nosūtīšanas konteinera ieraksti tiek izmantoti tikai sūtījuma izmaksām.</span><span class="sxs-lookup"><span data-stu-id="708c8-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="708c8-130">Tās nav pieejamas standarta **Transportēšanas pārvaldības** modulī (TMS).</span><span class="sxs-lookup"><span data-stu-id="708c8-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="708c8-131">Lai strādātu ar nosūtīšanas konteineru tipiem, dodieties uz **Kopējās izmaksas \> Konteineru iestatījumi \> Nosūtīšanas konteineri**.</span><span class="sxs-lookup"><span data-stu-id="708c8-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="708c8-132">Tur varat skatīt, pievienot un noņemt ierakstus saviem nosūtīšanas konteineriem.</span><span class="sxs-lookup"><span data-stu-id="708c8-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="708c8-133">Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.</span><span class="sxs-lookup"><span data-stu-id="708c8-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="708c8-134">Lauks</span><span class="sxs-lookup"><span data-stu-id="708c8-134">Field</span></span> | <span data-ttu-id="708c8-135">Apraksts</span><span class="sxs-lookup"><span data-stu-id="708c8-135">Description</span></span> |
|---|---|
| <span data-ttu-id="708c8-136">Nosūtīšanas konteiners</span><span class="sxs-lookup"><span data-stu-id="708c8-136">Shipping container</span></span> | <span data-ttu-id="708c8-137">Ievadiet nosūtīšanas konteinera tipam unikālu ID nosaukumu/numuru.</span><span class="sxs-lookup"><span data-stu-id="708c8-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="708c8-138">Nosūtīšanas konteinera veids</span><span class="sxs-lookup"><span data-stu-id="708c8-138">Shipping container type</span></span> | <span data-ttu-id="708c8-139">Atlasiet nosūtīšanas konteinera tipu.</span><span class="sxs-lookup"><span data-stu-id="708c8-139">Select the type of shipping container.</span></span> <span data-ttu-id="708c8-140">Papildinformāciju skatiet šīs tēmas iepriekšējā sadaļā [Nosūtīšanas konteineru tipu iestatīšana](#shipping-container-types).</span><span class="sxs-lookup"><span data-stu-id="708c8-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="708c8-141">Nosūtīšanas konteinera iestatīšana nav obligāta.</span><span class="sxs-lookup"><span data-stu-id="708c8-141">The shipping container setup is optional.</span></span> <span data-ttu-id="708c8-142">Parasti to izmantosiet tikai tad, ja jūsu uzņēmumam pieder savi nosūtīšanas konteineri vai arī tie paši nosūtīšanas konteineri bieži tiek atkārtoti izmantoti.</span><span class="sxs-lookup"><span data-stu-id="708c8-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="708c8-143">Nosūtīšanas konteineru numuriem netiek aprēķināts neviens kontrolskaitlis.</span><span class="sxs-lookup"><span data-stu-id="708c8-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="708c8-144">Vienību tipu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="708c8-144">Set up unit types</span></span>

<span data-ttu-id="708c8-145">Vienību tipi izveido papildu grupējumus un identifikācijas metodes nosūtīšanas konteineriem.</span><span class="sxs-lookup"><span data-stu-id="708c8-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="708c8-146">Vienības tips parasti tiek izmantots, lai identificētu konteinera tipu, kurā preces tiek iepakotas, piemēram, paletēs vai tvertnēs.</span><span class="sxs-lookup"><span data-stu-id="708c8-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="708c8-147">Vienības tipu var atlasīt, iestatot konteineru lapā **Visi pārvadāšanas konteineri**.</span><span class="sxs-lookup"><span data-stu-id="708c8-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="708c8-148">Vienību tipi tiek izmantoti tikai Kopējās izmaksās.</span><span class="sxs-lookup"><span data-stu-id="708c8-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="708c8-149">Tie nav pieejami TMS.</span><span class="sxs-lookup"><span data-stu-id="708c8-149">They aren't available in TMS.</span></span>

<span data-ttu-id="708c8-150">Lai strādātu ar nosūtīšanas konteineru tipiem, dodieties uz **Kopējās izmaksas \> Konteineru iestatījumi \> Vienību tipi**.</span><span class="sxs-lookup"><span data-stu-id="708c8-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="708c8-151">Tur varat skatīt, pievienot un noņemt ierakstus saviem vienību tipiem.</span><span class="sxs-lookup"><span data-stu-id="708c8-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="708c8-152">Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.</span><span class="sxs-lookup"><span data-stu-id="708c8-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="708c8-153">Lauks</span><span class="sxs-lookup"><span data-stu-id="708c8-153">Field</span></span> | <span data-ttu-id="708c8-154">Apraksts</span><span class="sxs-lookup"><span data-stu-id="708c8-154">Description</span></span> |
|---|---|
| <span data-ttu-id="708c8-155">Vienības veids</span><span class="sxs-lookup"><span data-stu-id="708c8-155">Unit type</span></span> | <span data-ttu-id="708c8-156">Ievadiet vienības tipa unikālo ID nosaukumu/numuru.</span><span class="sxs-lookup"><span data-stu-id="708c8-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="708c8-157">Apraksts</span><span class="sxs-lookup"><span data-stu-id="708c8-157">Description</span></span> | <span data-ttu-id="708c8-158">Ievadiet vienības tipa aprakstu.</span><span class="sxs-lookup"><span data-stu-id="708c8-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="708c8-159">Refrižeratora tipu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="708c8-159">Set up refrigeration types</span></span>

<span data-ttu-id="708c8-160">Refrižeratoru tipi veido papildu nosūtīšanas konteineru grupēšanas un identifikācijas līdzekļus, parasti tie ir refrižeratora konteineri.</span><span class="sxs-lookup"><span data-stu-id="708c8-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="708c8-161">Refrižeratora tipu var atlasīt, iestatot konteineru lapā **Visi nosūtīšanas konteineri**.</span><span class="sxs-lookup"><span data-stu-id="708c8-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="708c8-162">Lai strādātu ar nosūtīšanas konteineru tipiem, dodieties uz **Kopējās izmaksas \> Konteineru iestatījumi \> Refrižeratoru tipi**.</span><span class="sxs-lookup"><span data-stu-id="708c8-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="708c8-163">Tur varat skatīt, pievienot un noņemt ierakstus saviem refrižeratoru tipiem.</span><span class="sxs-lookup"><span data-stu-id="708c8-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="708c8-164">Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.</span><span class="sxs-lookup"><span data-stu-id="708c8-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="708c8-165">Lauks</span><span class="sxs-lookup"><span data-stu-id="708c8-165">Field</span></span> | <span data-ttu-id="708c8-166">Apraksts</span><span class="sxs-lookup"><span data-stu-id="708c8-166">Description</span></span> |
|---|---|
| <span data-ttu-id="708c8-167">Dzesēšanas veids</span><span class="sxs-lookup"><span data-stu-id="708c8-167">Refrigeration type</span></span> | <span data-ttu-id="708c8-168">Ievadiet refrižeratora tipa unikālo ID nosaukumu/numuru.</span><span class="sxs-lookup"><span data-stu-id="708c8-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="708c8-169">Apraksts</span><span class="sxs-lookup"><span data-stu-id="708c8-169">Description</span></span> | <span data-ttu-id="708c8-170">Ievadiet refrižeratora tipa aprakstu.</span><span class="sxs-lookup"><span data-stu-id="708c8-170">Enter a description of the refrigeration type.</span></span> |
