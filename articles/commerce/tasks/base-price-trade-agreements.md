---
title: " Bāzes cena un tirdzniecības līgumi"
description: Šajā procedūrā parādīts, kā izveidot kanāla pārdošanas cenas tirdzniecības līgumus.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7576c4218118724562ff739ff9805a06b7ba22d5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023296"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="44307-103"> Bāzes cena un tirdzniecības līgumi</span><span class="sxs-lookup"><span data-stu-id="44307-103">Base price and trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="44307-104">Šajā procedūrā parādīts, kā izveidot kanāla pārdošanas cenas tirdzniecības līgumus.</span><span class="sxs-lookup"><span data-stu-id="44307-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="44307-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="44307-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="44307-106">**Navigācijas rūtī** ejiet uz **Moduļi > Retail un Commerce > Cenošanas un atlaižu pārvaldība > Cenu grupas > Visas cenu grupas**.</span><span class="sxs-lookup"><span data-stu-id="44307-106">In the **Navigation pane**, go to **Modules > Retail and Commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="44307-107">Cenu grupas ir veids, kā tirdzniecības līgumi tiek piešķirti noteiktiem kanāliem.</span><span class="sxs-lookup"><span data-stu-id="44307-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="44307-108">Izmantojot cenu grupas, lai tirdzniecības līgumus piešķirtu kanāliem, var cenas var noteikt konkrētam kanālam.</span><span class="sxs-lookup"><span data-stu-id="44307-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="44307-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="44307-109">Click **New**.</span></span>
3. <span data-ttu-id="44307-110">Laukā **Cenu grupas** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="44307-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="44307-111">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="44307-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="44307-112">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="44307-112">Click **Save**.</span></span>
6. <span data-ttu-id="44307-113">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="44307-113">Close the page.</span></span>
7. <span data-ttu-id="44307-114">**Navigācijas rūtī** dodieties uz **Moduļi > Retail un Commerce > Kanāli > Veikali > Visi mazumtirdzniecības veikali**.</span><span class="sxs-lookup"><span data-stu-id="44307-114">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
8. <span data-ttu-id="44307-115">Sarakstā atlasiet Ņujorka.</span><span class="sxs-lookup"><span data-stu-id="44307-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="44307-116">Darbību rūtī noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="44307-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="44307-117">Noklikšķiniet uz **Cenu grupas**.</span><span class="sxs-lookup"><span data-stu-id="44307-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="44307-118">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="44307-118">Click **New**.</span></span>
12. <span data-ttu-id="44307-119">Laukā **Cenu grupas** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="44307-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="44307-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="44307-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="44307-121">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="44307-121">Click **Save**.</span></span>
15. <span data-ttu-id="44307-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="44307-122">Close the page.</span></span>
16. <span data-ttu-id="44307-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="44307-123">Close the page.</span></span>
17. <span data-ttu-id="44307-124">**Navigācijas rūtī** ejiet uz **Moduļi > Retail un Commerce > Produkti un kategorijas > Izlaistie produkti pēc kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="44307-124">In the **Navigation pane**, go to **Modules > Retail and Commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="44307-125">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="44307-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="44307-126">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="44307-126">Click **Edit**.</span></span>
20. <span data-ttu-id="44307-127">Izvērsiet kopsavilkuma cilni **Pārdot**.</span><span class="sxs-lookup"><span data-stu-id="44307-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="44307-128">Laukā **Cena** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="44307-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="44307-129">Šī cena tiek izmantota, ja netika atrasts neviens atbilstošs tirdzniecības līgums.</span><span class="sxs-lookup"><span data-stu-id="44307-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="44307-130">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="44307-130">Click **Save**.</span></span>
23. <span data-ttu-id="44307-131">**Darbību rūtī**noklikšķiniet uz **Pārdot**.</span><span class="sxs-lookup"><span data-stu-id="44307-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="44307-132">Klikšķiniet uz **Izveidot tirdzniecības līgumus**.</span><span class="sxs-lookup"><span data-stu-id="44307-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="44307-133">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="44307-133">Click **New**.</span></span>
26. <span data-ttu-id="44307-134">Laukā **Nosaukums** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu pārlūku.</span><span class="sxs-lookup"><span data-stu-id="44307-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="44307-135">Sarakstā atlasiet rindu **Tirdzniecība**.</span><span class="sxs-lookup"><span data-stu-id="44307-135">In the list, select **Commerce**.</span></span> <span data-ttu-id="44307-136">Demonstrācijas datos žurnāla nosaukumam **Commerce** ir noklusējuma relācija **Cena (pārdošanas)**.</span><span class="sxs-lookup"><span data-stu-id="44307-136">In the demo data, the **Commerce** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="44307-137">Tas nozīmē, ka visām jaunajām rindām pēc noklusējuma tiks iestatīti pārdošanas cenas tirdzniecības līgumi.</span><span class="sxs-lookup"><span data-stu-id="44307-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="44307-138">**Darbību rūtī** noklikšķiniet uz **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="44307-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="44307-139">Atlasiet „Grupa” laukā **Konta kods**.</span><span class="sxs-lookup"><span data-stu-id="44307-139">In the **Account code** field, select 'Group'.</span></span>
30. <span data-ttu-id="44307-140">Laukā **Konta atlase** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu pārlūku.</span><span class="sxs-lookup"><span data-stu-id="44307-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="44307-141">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="44307-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="44307-142">Tādējādi tiks pabeigta piesaiste no kanāla uz cenu grupu uz tirdzniecības līgumu.</span><span class="sxs-lookup"><span data-stu-id="44307-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="44307-143">Laukā **Vienuma attiecība** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="44307-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="44307-144">Laukā **Summa valūtā** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="44307-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="44307-145">Kopsavilkuma cilnē **Detaļas** atzīmējiet vai noņemiet atzīmi izvēles rūtiņai **Atrast nākamo**.</span><span class="sxs-lookup"><span data-stu-id="44307-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="44307-146">Kad iespēja **Atrast nākamo** iestatīta kā „Jā”, cenošanas programma turpinās meklēt piemērojamos tirdzniecības līgumus ar zemāku pārdošanas cenu.</span><span class="sxs-lookup"><span data-stu-id="44307-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="44307-147">Kad iespēja **Atrast nākamo** iestatīta kā „Nē”, cenošanas programma beidz meklēt un izmanto tirdzniecības līgumu.</span><span class="sxs-lookup"><span data-stu-id="44307-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="44307-148">Noklikšķiniet uz **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="44307-148">Click **Post**.</span></span>
36. <span data-ttu-id="44307-149">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="44307-149">Click **OK**.</span></span>
37. <span data-ttu-id="44307-150">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="44307-150">Close the page.</span></span>
38. <span data-ttu-id="44307-151">**Darbību rūtī** noklikšķiniet uz „Pārdot”</span><span class="sxs-lookup"><span data-stu-id="44307-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="44307-152">Noklikšķiniet uz **Pārdošanas cena**.</span><span class="sxs-lookup"><span data-stu-id="44307-152">Click **Sales price**.</span></span>

