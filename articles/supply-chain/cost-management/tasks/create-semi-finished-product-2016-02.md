---
title: Daļēji pabeigtas preces izveide (tikai 2016. gada februāris)
description: Šajā uzdevumā uzmanība ir vērsta uz daļēji pabeigtas preces izveidošanu.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76fcba3732879f85c9bf0faa6d2481b9c5313a17
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "358949"
---
# <a name="create-a-semi-finished-product-february-2016-only"></a><span data-ttu-id="13eac-103">Daļēji pabeigtas preces izveide (tikai 2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="13eac-103">Create a semi-finished product (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="13eac-104">Šajā uzdevumā uzmanība ir vērsta uz daļēji pabeigtas preces izveidošanu.</span><span class="sxs-lookup"><span data-stu-id="13eac-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="13eac-105">Tas ir MK aprēķina sērijas otrais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="13eac-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="13eac-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="13eac-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="13eac-107">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="13eac-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="13eac-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="13eac-108">Click New.</span></span>
3. <span data-ttu-id="13eac-109">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="13eac-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="13eac-110">Šajā piemērā ierakstiet vērtību BOM_2.</span><span class="sxs-lookup"><span data-stu-id="13eac-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="13eac-111">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="13eac-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="13eac-112">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="13eac-112">Select STD.</span></span> <span data-ttu-id="13eac-113">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="13eac-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="13eac-114">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="13eac-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="13eac-115">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="13eac-115">For example, select Audio.</span></span> <span data-ttu-id="13eac-116">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="13eac-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="13eac-117">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="13eac-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="13eac-118">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="13eac-118">Select SiteWH.</span></span> <span data-ttu-id="13eac-119">Šajā piemērā tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="13eac-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="13eac-120">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="13eac-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="13eac-121">Šajā piemērā izsekošanas dimensijas netiks lietotas, atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="13eac-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="13eac-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="13eac-122">Click OK.</span></span>
9. <span data-ttu-id="13eac-123">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="13eac-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="13eac-124">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="13eac-124">Click Default order settings.</span></span>
11. <span data-ttu-id="13eac-125">Laukā Noklusējuma pasūtījuma tips atlasiet vērtību “Ražošana”.</span><span class="sxs-lookup"><span data-stu-id="13eac-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="13eac-126">Tā kā šī ir daļēji pabeigta prece, kas tiks ražota, atlasiet Ražošana.</span><span class="sxs-lookup"><span data-stu-id="13eac-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="13eac-127">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="13eac-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="13eac-128">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="13eac-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="13eac-129">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="13eac-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="13eac-130">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="13eac-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="13eac-131">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="13eac-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="13eac-132">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="13eac-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="13eac-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="13eac-133">Close the page.</span></span>
16. <span data-ttu-id="13eac-134">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="13eac-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="13eac-135">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="13eac-135">Click Item price.</span></span>
18. <span data-ttu-id="13eac-136">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="13eac-136">Click New.</span></span>
19. <span data-ttu-id="13eac-137">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="13eac-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="13eac-138">Laukā Versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="13eac-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="13eac-139">Šajā piemērā atlasiet vērtību 10. versija.</span><span class="sxs-lookup"><span data-stu-id="13eac-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="13eac-140">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="13eac-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="13eac-141">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="13eac-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="13eac-142">Laukam Cena vērtību iestatiet uz “10”.</span><span class="sxs-lookup"><span data-stu-id="13eac-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="13eac-143">Šajā piemērā ierakstiet izmaksu cenu 10.</span><span class="sxs-lookup"><span data-stu-id="13eac-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="13eac-144">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="13eac-144">Click Save.</span></span>
24. <span data-ttu-id="13eac-145">Noklikšķiniet uz Aktivizēt gaidošās cenas.</span><span class="sxs-lookup"><span data-stu-id="13eac-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="13eac-146">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="13eac-146">Close the page.</span></span>
26. <span data-ttu-id="13eac-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="13eac-147">Close the page.</span></span>
27. <span data-ttu-id="13eac-148">Noklikšķiniet uz BOM_2, lai to atvērtu.</span><span class="sxs-lookup"><span data-stu-id="13eac-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="13eac-149">Izvērsiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="13eac-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="13eac-150">Laukā Izmaksu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="13eac-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="13eac-151">Šajā piemērā atlasiet vērtību Izmaksu grupa M1.</span><span class="sxs-lookup"><span data-stu-id="13eac-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="13eac-152">Lietojiet šo saīsni ieraksta saglabāšanai.</span><span class="sxs-lookup"><span data-stu-id="13eac-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="13eac-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="13eac-153">Close the page.</span></span>

