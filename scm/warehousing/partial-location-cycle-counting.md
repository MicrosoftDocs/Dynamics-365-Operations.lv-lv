---
title: "Daļēja novietojuma cikla inventarizācija"
description: "Cikla inventarizācijas plāni vada faktiskās inventarizācijas operācijas. Varat pieprasīt, ka tiek uzskaitītas tikai noteiktas preces un preču varianti, nevis lai visi rīcībā esošie krājumi kādā novietojumā."
author: perlynne
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2ee4de8eabc55271e272ca3026746787353f5fc3
ms.contentlocale: lv-lv
ms.lasthandoff: 07/18/2017

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="3942f-105">Daļēja novietojuma cikla inventarizācija</span><span class="sxs-lookup"><span data-stu-id="3942f-105">Partial location cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3942f-106">Cikla inventarizācijas plāni vada faktiskās inventarizācijas operācijas.</span><span class="sxs-lookup"><span data-stu-id="3942f-106">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="3942f-107">Varat pieprasīt, ka tiek uzskaitītas tikai noteiktas preces un preču varianti, nevis lai visi rīcībā esošie krājumi kādā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="3942f-107">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="3942f-108">Izmantojot cikla inventarizācijas plānus, lai izveidotu inventarizācijas darbu, varat vadīt faktiskās inventarizācijas operācijas.</span><span class="sxs-lookup"><span data-stu-id="3942f-108">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="3942f-109">Varat pieprasīt, ka tiek uzskaitītas tikai noteiktas preces un preču varianti, nevis lai visi rīcībā esošie krājumi kādā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="3942f-109">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="3942f-110">Filtrējot pēc atsevišķām precēm, noliktavas pārvaldnieks var samazināt pārskatīšanas pieskaitāmo daudzumu, izvairīties no konsolidācijas kļūdām un ietaupīt laiku.</span><span class="sxs-lookup"><span data-stu-id="3942f-110">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="3942f-111">Kā konfigurēt daļēju novietojuma cikla inventarizāciju</span><span class="sxs-lookup"><span data-stu-id="3942f-111">How to configure partial location cycle counting</span></span>
<span data-ttu-id="3942f-112">Kad noliktavas darba procesu izmantojat inventarizācijas operācijām, katram novietojumam tiek izveidots darba virsraksts.</span><span class="sxs-lookup"><span data-stu-id="3942f-112">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="3942f-113">Kad definējat cikla inventarizācijas plānu, varat izmantot vaicājumu **Atlasīt novietojumus**, lai ierobežotu izveidoto cikla inventarizācijas darbu.</span><span class="sxs-lookup"><span data-stu-id="3942f-113">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="3942f-114">Kad atlasāt preces šim cikla inventarizācijas plānam, varat atlasīt gan preču, gan preču variantu vaicājumus, lai precizētu, kas tiek uzskaitīts.</span><span class="sxs-lookup"><span data-stu-id="3942f-114">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="3942f-115">Varat ar cikla inventarizācijas plānu saistīt kādu **darba veidni**, lai definētu veidu, kā ir jāveido cikla inventarizācijas darbs.</span><span class="sxs-lookup"><span data-stu-id="3942f-115">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="3942f-116">Uz darba veidni inventarizācijas operācijām ir tieša atsauce no cikla inventarizācijas plāna.</span><span class="sxs-lookup"><span data-stu-id="3942f-116">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="3942f-117">Kad definējat darba veidnes informāciju, varat izmantot opciju **Darba rindas pārtraukumi**, lai norādītu, vai inventarizācijas darba rindas ir jāgrupē pēc krājuma numura vai pēc preces varianta numura.</span><span class="sxs-lookup"><span data-stu-id="3942f-117">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="3942f-118">Šī iestatīšana ir nepieciešama, ja vēlaties uzskaitīt rīcībā esošos krājumus tikai konkrētām precēm kādā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="3942f-118">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="3942f-119">Izveidotajās cikla inventarizācijas darbu rindās būs jūsu šeit definētais informācijas līmenis, un vadītā inventarizācijas operācija tiks apstrādāta, pamatojoties uz šo līmeni.</span><span class="sxs-lookup"><span data-stu-id="3942f-119">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="3942f-120">Ja cikla inventarizācijas plānus saistāt ar darba veidnēm, izmantojot opciju **Darba rindu pārtraukumi**, tad izveidotajam cikla inventarizācijas darbam ir atlasīts lauks **Daļēja cikla inventarizācija**, un tiek izveidotas vairākas cikla inventarizācijas darba rindas, pamatojoties uz darba veidnes definīciju.</span><span class="sxs-lookup"><span data-stu-id="3942f-120">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="3942f-121">Lai varētu apstrādāt daļēja cikla inventarizācijas darbu, kā daļa no cikla inventarizācijas iestatīšanas jums mobilās ierīces izvēlnes vienumam ir jāatlasa vismaz vienums **Parādīt krājuma numuru**.</span><span class="sxs-lookup"><span data-stu-id="3942f-121">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="3942f-122">Noliktavas operatoram tiks lūgts ierakstīt tikai uzskaites informāciju, kas ir saistīta ar inventarizācijas rindām (krājumu kodus un preču dimensijas).</span><span class="sxs-lookup"><span data-stu-id="3942f-122">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="3942f-123">Visi citi rīcībā esošie krājumi šim inventarizācijas procesam tiks ignorēti.</span><span class="sxs-lookup"><span data-stu-id="3942f-123">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="3942f-124">Attiecībā uz daļēja cikla inventarizācijas procesu datums/laiks **Pēdējā cikla inventarizācija** novietojumam netiek atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="3942f-124">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="3942f-125">Piemērs</span><span class="sxs-lookup"><span data-stu-id="3942f-125">Example</span></span>
<span data-ttu-id="3942f-126">Šajā piemērā noliktavā 61 ir jāuzskaita tikai krājums numur A0001.</span><span class="sxs-lookup"><span data-stu-id="3942f-126">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="3942f-127">Tiek izveidota jauna darba veidne cikla inventarizācijai.</span><span class="sxs-lookup"><span data-stu-id="3942f-127">A new work template for cycle counting is created.</span></span> <span data-ttu-id="3942f-128">Lai inventarizācijas darbu rindas grupētu pēc krājuma koda, tiek izmantota opcija **Darba rindas pārtraukumi**.</span><span class="sxs-lookup"><span data-stu-id="3942f-128">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="3942f-129">Tādēļ izveidotajā cikla inventarizācijas darbā būs rindas katram krājuma kodam.</span><span class="sxs-lookup"><span data-stu-id="3942f-129">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="3942f-130">Rindas varat grupēt arī pēc preces varianta numura.</span><span class="sxs-lookup"><span data-stu-id="3942f-130">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="3942f-131">Tiek izveidots jauns cikla inventarizācijas plāns, kura ir atsauce uz jaunizveidoto darba veidni.</span><span class="sxs-lookup"><span data-stu-id="3942f-131">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="3942f-132">Šis cikla inventarizācijas plāns ietver visus novietojumus noliktavā 61 (vaicājums **Atlasīt novietojumus**), kuros atrodas krājums numuram A0001.</span><span class="sxs-lookup"><span data-stu-id="3942f-132">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="3942f-133">Konkrētu preču atlase tiek definēta sadaļā **Cikla inventarizācijas preču atlases**.</span><span class="sxs-lookup"><span data-stu-id="3942f-133">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="3942f-134">Preces cikla inventarizācijas plāniem varat atlasīt, laukam **Tukšie novietojumi** iestatot vērtību **Izslēgt tukšos**. Kad šis cikla inventarizācijas plāns tiek apstrādāts, tiek izveidots daļēja cikla inventarizācijas darbs krājumam numur A0001.</span><span class="sxs-lookup"><span data-stu-id="3942f-134">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="3942f-135">Faktisko uzskaites procesu var veikt, izmantojot mobilās ierīces izvēlnes vienumu vadītajai cikla inventarizācijai.</span><span class="sxs-lookup"><span data-stu-id="3942f-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="see-also"></a><span data-ttu-id="3942f-136">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="3942f-136">See also</span></span>
--------

[<span data-ttu-id="3942f-137">Cikla inventarizācija</span><span class="sxs-lookup"><span data-stu-id="3942f-137">Cycle counting</span></span>](cycle-counting.md)


