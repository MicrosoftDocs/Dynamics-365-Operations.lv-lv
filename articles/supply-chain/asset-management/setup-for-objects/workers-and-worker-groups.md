---
title: Uzturēšanas speciālisti un speciālistu grupas
description: Šajā tēmā ir pakaidroti uzturēšanas speciālisti un speciālistu grupas Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6cf7e8e796032b348cff5a77c10b376dbbeef974
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214784"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="d4ce0-103">Uzturēšanas speciālisti un speciālistu grupas</span><span class="sxs-lookup"><span data-stu-id="d4ce0-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d4ce0-104">Šajā tēmā ir pakaidroti uzturēšanas speciālisti un speciālistu grupas Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="d4ce0-105">Pamatlīdzekļu pārvaldībā varat pievienot uzturēšanas speciālistus funkcionālajiem novietojumiem.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="d4ce0-106">(Papildinformāciju par funkcionālajiem novietojumiem skatiet nodaļā [Funkcionālo novietojumu izveide](../functional-locations/create-functional-locations.md).) Šī funkcionalitāte var būt noderīga, ja, piemēram, plānojat uzturēšanas darbu iekārtā, kas atrodas funkcionālajā novietojumā 01, un jūs vēlaties piešķirt uzturēšanas speciālistus no tās pašas atrašanās vietas darba izpildei.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="d4ce0-107">Varat arī izveidot uzturēšanas speciālistu grupas un saistīt uzturēšanas speciālistus ar tām.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="d4ce0-108">Šī funkcionalitāte noder, ja veicat vienkāršu darba pasūtījumu plānošanu un vēlaties ieplānot uzturēšanas speciālistu grupu darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="d4ce0-109">Varat izmantot uzturēšanas speciālistus un uzturēšanas speciālistu grupas, lai iestatītu vēlamos uzturēšanas speciālistus un atbildīgos uzturēšanas speciālistus.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="d4ce0-110">Izveidot nodarbinātos</span><span class="sxs-lookup"><span data-stu-id="d4ce0-110">Create workers</span></span>

1. <span data-ttu-id="d4ce0-111">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Nodarbinātie** \> **Nodarbinātie**.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="d4ce0-112">Atlasiet **Jauns**, lai pievienotu nodarbināto sarakstam.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="d4ce0-113">Laukā **Nodarbinātais** atlasiet nodarbināto.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="d4ce0-114">Iestatiet opciju **Aktīvs** uz **Jā**, lai nodarbinātajam ieplānotu darba pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="d4ce0-115">Kopsavilkuma cilnē **Vispārīgi** lauki **Resursi** un **Apraksts** tiek automātiski aizpildīti, ja nodarbinātajam ir atlasīts resurss.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="d4ce0-116">Lauks **Kalendārs** arī tiek aizpildīts automātiski, ja esat iestatījis nodarbināto kā resursu un piešķīris kalendāru šim resursam lapā **Resursi** (**Organizācijas administrēšana** \> **Resursi** \> **Resursi**).</span><span class="sxs-lookup"><span data-stu-id="d4ce0-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="d4ce0-117">Kopsavilkuma cilnē **Grupas** atlasiet **Pievienot** un pēc tam nodarbinātajam atlasiet uzturēšanas speciālistu grupu.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="d4ce0-118">Nodarbinātais var būt saistīts ar vairāk nekā vienu grupu.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="d4ce0-119">Standarta iestatījumā nodarbinātā piederība grupai ir spēkā no datuma, kad pievienojat grupu, un tā nekad nebeidzas.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="d4ce0-120">Šis datums tiek rādīts laukā **Ir spēkā**.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="d4ce0-121">Lai skatītu lauku **Ir spēkā**, atlasiet **Skatīt** \> **Visu**.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="d4ce0-122">Ja nodarbinātā piederība grupai jāierobežo līdz noteiktam periodam, tā definēšanai izmantojiet laukus **Ir spēkā** un **Beigu termiņš**.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="d4ce0-123">Kopsavilkuma cilnē **Funkcionālais novietojums** atlasiet **Pievienot** un pēc tam uzturēšanas speciālistam atlasiet funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="d4ce0-124">Norādiet arī, kura atrašanās vieta ir nodarbinātā primārais funkcionālais novietojums.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4ce0-125">Ja nodarbinātajam pievienojat funkcionālos novietojumus, visi aktīvie līdzekļi, kas ir saistīti ar šiem funkcionālajiem novietojumiem, tiek parādīti dažādos izvēlnes vienumos, piemēram **Mani aktīvie līdzekļi** un **Mani aktīvie funkcionālie novietojumi**.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="d4ce0-126">Tie ir redzami arī līdzekļa uzmeklēšanas sarakstos, kas tiek parādīti, veidojot jaunu līdzekli, uzturēšanas pieprasījumu vai darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="d4ce0-127">Kopsavilkuma cilnes **Detalizēta informācija** lauki rāda to uzturēšanas speciālistu grupu un funkcionālo novietojumu skaitu, ar kuriem ir saistīts atlasītais uzturēšanas speciālists.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="d4ce0-128">Nodarbināto grupu izveide</span><span class="sxs-lookup"><span data-stu-id="d4ce0-128">Create worker groups</span></span>

1. <span data-ttu-id="d4ce0-129">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Nodarbinātie** \> **Uzturēšanas speciālistu grupas**.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="d4ce0-130">Atlasiet **Jauns**, lai pievienotu nodarbināto grupu sarakstam.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="d4ce0-131">Laukā **Uzturēšanas speciālistu grupa** ievadiet grupas ID.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="d4ce0-132">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="d4ce0-133">Kopsavilkuma cilnē **Nodarbinātie** atlasiet **Pievienot** un pēc tam atlasiet uzturēšanas speciālistu nodarbināto grupai.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="d4ce0-134">Informāciju par laukiem **Ir spēkā** un **Beigu datums** skatiet iepriekšējās procedūras 6. darbībā.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="d4ce0-135">Ja resursu grupai ir jābūt saistītai ar atlasīto uzturēšanas speciālistu grupu, atlasiet **Kopēt no resursu grupas**.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="d4ce0-136">Laukā **Grupa** atlasiet resursu grupu, no kuras kopēt kalendāra iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="d4ce0-137">Pēc tam laukā **Nodarbināto grupa** atlasiet nodarbināto grupu, uz kuru kopēt resursu grupas kalendāra iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="d4ce0-138">Šī darbība ir būtiska tikai tad, ja vēlaties, lai uzturēšanas speciālisti darba pasūtījuma plānošanas laikā izmanto kalendāru, kas ir saistīts ar resursu (darba centru).</span><span class="sxs-lookup"><span data-stu-id="d4ce0-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="d4ce0-139">Kopsavilkuma cilne **Detalizēta informācija** rāda to uzturēšanas speciālistu skaitu, kuri ir iestatīti atlasītajā uzturēšanas speciālistu grupā.</span><span class="sxs-lookup"><span data-stu-id="d4ce0-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>
