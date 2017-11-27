---
title: "Daļēja novietojuma cikla inventarizācija"
description: "Cikla inventarizācijas plāni vada faktiskās inventarizācijas operācijas. Varat pieprasīt, ka tiek uzskaitītas tikai noteiktas preces un preču varianti, nevis lai visi rīcībā esošie krājumi kādā novietojumā."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0e0f9d81f4d5943a89d8ac87776e05acb32cb8d9
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="b8999-104">Daļēja novietojuma cikla inventarizācija</span><span class="sxs-lookup"><span data-stu-id="b8999-104">Partial location cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b8999-105">Cikla inventarizācijas plāni vada faktiskās inventarizācijas operācijas.</span><span class="sxs-lookup"><span data-stu-id="b8999-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="b8999-106">Varat pieprasīt, ka tiek uzskaitītas tikai noteiktas preces un preču varianti, nevis lai visi rīcībā esošie krājumi kādā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="b8999-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="b8999-107">Izmantojot cikla inventarizācijas plānus, lai izveidotu inventarizācijas darbu, varat vadīt faktiskās inventarizācijas operācijas.</span><span class="sxs-lookup"><span data-stu-id="b8999-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="b8999-108">Varat pieprasīt, ka tiek uzskaitītas tikai noteiktas preces un preču varianti, nevis lai visi rīcībā esošie krājumi kādā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="b8999-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="b8999-109">Filtrējot pēc atsevišķām precēm, noliktavas pārvaldnieks var samazināt pārskatīšanas pieskaitāmo daudzumu, izvairīties no konsolidācijas kļūdām un ietaupīt laiku.</span><span class="sxs-lookup"><span data-stu-id="b8999-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="b8999-110">Kā konfigurēt daļēju novietojuma cikla inventarizāciju</span><span class="sxs-lookup"><span data-stu-id="b8999-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="b8999-111">Kad noliktavas darba procesu izmantojat inventarizācijas operācijām, katram novietojumam tiek izveidots darba virsraksts.</span><span class="sxs-lookup"><span data-stu-id="b8999-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="b8999-112">Kad definējat cikla inventarizācijas plānu, varat izmantot vaicājumu **Atlasīt novietojumus**, lai ierobežotu izveidoto cikla inventarizācijas darbu.</span><span class="sxs-lookup"><span data-stu-id="b8999-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="b8999-113">Kad atlasāt preces šim cikla inventarizācijas plānam, varat atlasīt gan preču, gan preču variantu vaicājumus, lai precizētu, kas tiek uzskaitīts.</span><span class="sxs-lookup"><span data-stu-id="b8999-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="b8999-114">Varat ar cikla inventarizācijas plānu saistīt kādu **darba veidni**, lai definētu veidu, kā ir jāveido cikla inventarizācijas darbs.</span><span class="sxs-lookup"><span data-stu-id="b8999-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="b8999-115">Uz darba veidni inventarizācijas operācijām ir tieša atsauce no cikla inventarizācijas plāna.</span><span class="sxs-lookup"><span data-stu-id="b8999-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="b8999-116">Kad definējat darba veidnes informāciju, varat izmantot opciju **Darba rindas pārtraukumi**, lai norādītu, vai inventarizācijas darba rindas ir jāgrupē pēc krājuma numura vai pēc preces varianta numura.</span><span class="sxs-lookup"><span data-stu-id="b8999-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="b8999-117">Šī iestatīšana ir nepieciešama, ja vēlaties uzskaitīt rīcībā esošos krājumus tikai konkrētām precēm kādā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="b8999-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="b8999-118">Izveidotajās cikla inventarizācijas darbu rindās būs jūsu šeit definētais informācijas līmenis, un vadītā inventarizācijas operācija tiks apstrādāta, pamatojoties uz šo līmeni.</span><span class="sxs-lookup"><span data-stu-id="b8999-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="b8999-119">Ja cikla inventarizācijas plānus saistāt ar darba veidnēm, izmantojot opciju **Darba rindu pārtraukumi**, tad izveidotajam cikla inventarizācijas darbam ir atlasīts lauks **Daļēja cikla inventarizācija**, un tiek izveidotas vairākas cikla inventarizācijas darba rindas, pamatojoties uz darba veidnes definīciju.</span><span class="sxs-lookup"><span data-stu-id="b8999-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="b8999-120">Lai varētu apstrādāt daļēja cikla inventarizācijas darbu, kā daļa no cikla inventarizācijas iestatīšanas jums mobilās ierīces izvēlnes vienumam ir jāatlasa vismaz vienums **Parādīt krājuma numuru**.</span><span class="sxs-lookup"><span data-stu-id="b8999-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="b8999-121">Noliktavas operatoram tiks lūgts ierakstīt tikai uzskaites informāciju, kas ir saistīta ar inventarizācijas rindām (krājumu kodus un preču dimensijas).</span><span class="sxs-lookup"><span data-stu-id="b8999-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="b8999-122">Visi citi rīcībā esošie krājumi šim inventarizācijas procesam tiks ignorēti.</span><span class="sxs-lookup"><span data-stu-id="b8999-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="b8999-123">Attiecībā uz daļēja cikla inventarizācijas procesu datums/laiks **Pēdējā cikla inventarizācija** novietojumam netiek atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="b8999-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="b8999-124">Piemērs</span><span class="sxs-lookup"><span data-stu-id="b8999-124">Example</span></span>
<span data-ttu-id="b8999-125">Šajā piemērā noliktavā 61 ir jāuzskaita tikai krājums numur A0001.</span><span class="sxs-lookup"><span data-stu-id="b8999-125">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="b8999-126">Tiek izveidota jauna darba veidne cikla inventarizācijai.</span><span class="sxs-lookup"><span data-stu-id="b8999-126">A new work template for cycle counting is created.</span></span> <span data-ttu-id="b8999-127">Lai inventarizācijas darbu rindas grupētu pēc krājuma koda, tiek izmantota opcija **Darba rindas pārtraukumi**.</span><span class="sxs-lookup"><span data-stu-id="b8999-127">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="b8999-128">Tādēļ izveidotajā cikla inventarizācijas darbā būs rindas katram krājuma kodam.</span><span class="sxs-lookup"><span data-stu-id="b8999-128">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="b8999-129">Rindas varat grupēt arī pēc preces varianta numura.</span><span class="sxs-lookup"><span data-stu-id="b8999-129">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="b8999-130">Tiek izveidots jauns cikla inventarizācijas plāns, kura ir atsauce uz jaunizveidoto darba veidni.</span><span class="sxs-lookup"><span data-stu-id="b8999-130">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="b8999-131">Šis cikla inventarizācijas plāns ietver visus novietojumus noliktavā 61 (vaicājums **Atlasīt novietojumus**), kuros atrodas krājums numuram A0001.</span><span class="sxs-lookup"><span data-stu-id="b8999-131">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="b8999-132">Konkrētu preču atlase tiek definēta sadaļā **Cikla inventarizācijas preču atlases**.</span><span class="sxs-lookup"><span data-stu-id="b8999-132">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="b8999-133">Varat atlasīt preces cikla inventarizācijas plāniem, iestatot lauka **Iztukšot atrašanās vietas** vērtību **Izslēgt tukšos**.</span><span class="sxs-lookup"><span data-stu-id="b8999-133">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="b8999-134">Apstrādājot cikla inventarizācijas plānu, tiek izveidots daļēja cikla inventarizācijas darbs krājumam Nr. A0001.</span><span class="sxs-lookup"><span data-stu-id="b8999-134">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="b8999-135">Faktisko uzskaites procesu var veikt, izmantojot mobilās ierīces izvēlnes vienumu vadītajai cikla inventarizācijai.</span><span class="sxs-lookup"><span data-stu-id="b8999-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="see-also"></a><span data-ttu-id="b8999-136">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="b8999-136">See also</span></span>
--------

[<span data-ttu-id="b8999-137">Cikla inventarizācija</span><span class="sxs-lookup"><span data-stu-id="b8999-137">Cycle counting</span></span>](cycle-counting.md)


