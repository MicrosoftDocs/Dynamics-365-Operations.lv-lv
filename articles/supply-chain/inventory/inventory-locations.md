---
title: Krājumu vietas
description: Krājumu atrašanās vietu dati tiek izmantoti kopā ar pamata noliktavu (WMS I), lai noteiktu, kur tiek glabāti krājumi un kur krājumi tiek izdoti no WMS I noliktavas.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 789272e1ee02c7f5dbab4e325cefe56425a3d1a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "350807"
---
# <a name="inventory-locations"></a><span data-ttu-id="b3b9c-103">Krājumu vietas</span><span class="sxs-lookup"><span data-stu-id="b3b9c-103">Inventory locations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3b9c-104">Krājumu atrašanās vietu dati tiek izmantoti kopā ar pamata noliktavu (WMS I), lai noteiktu, kur tiek glabāti krājumi un kur krājumi tiek izdoti no WMS I noliktavas.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="b3b9c-105">Šī tēma attiecas uz moduļa Krājumu vadība līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="b3b9c-106">Tā neattiecas uz moduļa Noliktavas pārvaldība līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="b3b9c-107">Termins novietojums attiecas uz vietu, kur tiek uzglabāti krājumi un no kurienes tie tiek ņemti.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="b3b9c-108">Katrai atrašanās vietai var tikt norādīta arī krājuma ievietošanas vieta.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="b3b9c-109">Pēc noklusējuma tās ir vienādas.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-109">By default, they are the same.</span></span> <span data-ttu-id="b3b9c-110">Krājumi parasti, bet ne vienmēr tiek ievietoti un ņemti no vienas un tās pašas atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="b3b9c-111">Piemēram, noliktavas statīvos uzglabāti krājumi tiek ņemti no vienas ailes un ievietoti citā.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="b3b9c-112">Galvenā ievade tiek noteikta pēc novietojuma nosaukuma, ko parasti nosaka tās koordinātas: noliktava, aile, statīvs, plaukts un nodalījums.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="b3b9c-113">Šo nosaukumu vai ID var ievadīt manuāli, vai tas var tikt ģenerēts no novietojuma koordinātām lapā Krājumu vietas, piemēram, 01-02-03-4 novietojumam 1. ailē, 2. statīvā, 3. plauktā, 4. nodalījumā.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="b3b9c-114">Atrašanās vietas rekvizīti</span><span class="sxs-lookup"><span data-stu-id="b3b9c-114">Location properties</span></span>

<span data-ttu-id="b3b9c-115">Atrašanās vietai ir šādi rekvizīti:</span><span class="sxs-lookup"><span data-stu-id="b3b9c-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="b3b9c-116">Izmērs (augstums, platums, dziļums un tilpums)</span><span class="sxs-lookup"><span data-stu-id="b3b9c-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="b3b9c-117">Noliktava un ailes, statīva, plaukta un nodalījuma pozīcija</span><span class="sxs-lookup"><span data-stu-id="b3b9c-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="b3b9c-118">Novietojuma tips (uzkrāšanas vieta, izdošanas vietu, saņemšanas doks, izdošanas doks, ražošanas ievades vieta, pārbaudes veikšanas vieta vai Kanban lielveikals)</span><span class="sxs-lookup"><span data-stu-id="b3b9c-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="b3b9c-119">Tiešsaistes sistēmās var lietot kontroltekstu, lai pārliecinātos, ka operators ir atlasījis pareizo noteikta krājuma novietojumu.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="b3b9c-120">Kontroltekstu var izveidot manuāli vai pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="b3b9c-121">Kārtošanas kodi</span><span class="sxs-lookup"><span data-stu-id="b3b9c-121">Sort codes</span></span>
<span data-ttu-id="b3b9c-122">Lietojiet kārtošanas kodus, lai optimizētu izdošanas rindu apstrādi, jo tie sniedz aprakstu par krājumu izdošanu, tostarp, par izdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="b3b9c-123">Kārtošanas kodi var tikt norādīti pēc ailes un citām koordinātēm vai arī tikt piešķirti novietojumam manuāli.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="b3b9c-124">Bloķētas atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="b3b9c-124">Blocked locations</span></span>
<span data-ttu-id="b3b9c-125">Dažreiz var būt vajadzīgs norādīt, ka novietojums ir aizturēts uz noteiktu laika periodu, piemēram, lai veiktu remontu.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="b3b9c-126">Šādā gadījumā ir ieteicams norādīt tikai ieejas vai izejas plūsmas aizturēšanu.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="b3b9c-127">Aplikācijas objektu koka struktūra</span><span class="sxs-lookup"><span data-stu-id="b3b9c-127">Tree structure</span></span>

<span data-ttu-id="b3b9c-128">Lapā Krājumu vietas varat definēta attēlojuma formātā skatīt noliktavas izkārtojuma koka struktūru, kuras pamatā ir krājumu vietu koordinātes.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="b3b9c-129">Krājumu vietu uzturēšana, izmantojot noliktavas veidlapu</span><span class="sxs-lookup"><span data-stu-id="b3b9c-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="b3b9c-130">Varat kopēt novietojumus no vienas noliktavas uz citu, kā arī izveidot novietojumus, izmantojot vedni.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="b3b9c-131">Pirms vedņa palaišanas pārliecinieties, ka esat definējis noklusējuma novietojumu nosaukumus lapā Noliktava.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="b3b9c-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b3b9c-132">Additional resources</span></span>
--------

[<span data-ttu-id="b3b9c-133">Jauna noliktavas izkārtojuma izveide (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="b3b9c-133">Create a new warehouse layout (Task guide)</span></span>](tasks/create-new-warehouse-layout.md)
