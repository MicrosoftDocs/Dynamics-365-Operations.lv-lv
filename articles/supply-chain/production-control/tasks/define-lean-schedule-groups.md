--- 
title: "Racionālās plānošanas grupu definēšana"
description: "Racionālās plānošanas grupas tiek definētas, lai grupētu un izšķirtu preces Kanban plānošanā."
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: dcb8c82af7d3bcd95a13cef49c5606ea8781e459
ms.contentlocale: lv-lv
ms.lasthandoff: 09/11/2018

---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="bbcf5-103">Racionālās plānošanas grupu definēšana</span><span class="sxs-lookup"><span data-stu-id="bbcf5-103">Define lean schedule groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bbcf5-104">Racionālās plānošanas grupas tiek definētas, lai grupētu un izšķirtu preces Kanban plānošanā.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="bbcf5-105">Grupēšanu var veikt kā vispārīgu saistību pēc uzņēmuma vai noteiktai darba šūnai.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="bbcf5-106">Katrai grupai ir piešķirts krāsas kods vizuālai norādei Kanban plānošanas saraksta lapā.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-106">Each group has a color code assigned for visual indication in the kanban scheduling listpage.</span></span> <span data-ttu-id="bbcf5-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="bbcf5-108">Racionālās plānošanas grupas definēšana</span><span class="sxs-lookup"><span data-stu-id="bbcf5-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="bbcf5-109">Dodieties uz Preču informācijas pārvaldība > Lean manufacturing > Racionālās plānošanas grupas.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="bbcf5-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-110">Click New.</span></span>
3. <span data-ttu-id="bbcf5-111">Laukā Plānošanas grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="bbcf5-112">Plānošanas grupu var definēt kā globālo grupu vai noteiktai darba šūnai.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="bbcf5-113">Šajā vienkāršajā piemērā tiks definēta globāla grupa un darba šūna paliks tukša.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="bbcf5-114">Šīs grupas iestatījumi attiecas uz visām darba šūnām, kurām nav noteiktu plānošanas grupu.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="bbcf5-115">Atlasiet krāsu no krāsu atlases.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="bbcf5-116">Krāsas tiek lietotas, lai iezīmētu darbus Kanban grafiku saraksta lapā vai Kanban apstrādes ziņojumu dēlī.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="bbcf5-117">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="bbcf5-118">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="bbcf5-119">Preces piesaistīšana</span><span class="sxs-lookup"><span data-stu-id="bbcf5-119">Associate product</span></span>
1. <span data-ttu-id="bbcf5-120">Noteiktas preces piesaistīšana</span><span class="sxs-lookup"><span data-stu-id="bbcf5-120">Associate a specific product</span></span>
    * <span data-ttu-id="bbcf5-121">Ir divi veidi, kā saistīt preces ar racionālās plānošanas grupām kā noteiktu preci (Krājumu saistības tips = Krājums) vai kā daļu no krājumu sadalījuma principa (Krājumu saistības tips = Grupa).</span><span class="sxs-lookup"><span data-stu-id="bbcf5-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="bbcf5-122">Laukā Krājumu saistības tips atlasiet vienumu Krājums</span><span class="sxs-lookup"><span data-stu-id="bbcf5-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="bbcf5-123">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="bbcf5-124">Laukā Caurlaides koeficients ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="bbcf5-125">Noklusējuma caurlaides koeficients ir 1, kas nozīmē to, ka saistītās preces patērē tieši tādu noslodzi, kas norādīta ražošanas plūsmu procesa aktivitātēs.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activites of the production flows.</span></span> <span data-ttu-id="bbcf5-126">Caurlaides koeficients > 1 norāda lielāku resursu patēriņu, caurlaides koeficients < 1 norāda mazāku resursu patēriņu.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="bbcf5-127">Koeficients tiek izmantots izmaksu aprēķinā un Kanban darba patēriņa aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="bbcf5-128">Krājumu sadalījuma principa piesaistīšana</span><span class="sxs-lookup"><span data-stu-id="bbcf5-128">Associate item allocation key</span></span>
1. <span data-ttu-id="bbcf5-129">Krājumu sadalījuma principa piesaistīšana</span><span class="sxs-lookup"><span data-stu-id="bbcf5-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="bbcf5-130">Pievienojiet saistību ar krājumu sadalījuma principu, izmantojot krājumu saistības tipu Grupa.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="bbcf5-131">Ņemiet vērā, ka šim procesam ir nepieciešams datos definēt prognozi krājumu sadalījuma principam.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-131">Note that for this process, you need a forecast item alllocation key defined in your data.</span></span>  
2. <span data-ttu-id="bbcf5-132">Laukā Krājumu saistības tips atlasiet vienumu Grupa</span><span class="sxs-lookup"><span data-stu-id="bbcf5-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="bbcf5-133">Laukā Krājumu sadalījuma princips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bbcf5-134">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-134">In the list, click the link in the selected row.</span></span>


