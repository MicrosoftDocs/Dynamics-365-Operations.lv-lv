---
title: " Bāzes cena un tirdzniecības līgumi"
description: Šajā procedūrā parādīts, kā izveidot kanāla pārdošanas cenas tirdzniecības līgumus.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 4830ac553318cfbb3cb74395d1662e74dff75290
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "320424"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="2472c-103"> Bāzes cena un tirdzniecības līgumi</span><span class="sxs-lookup"><span data-stu-id="2472c-103">Base price and trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2472c-104">Šajā procedūrā parādīts, kā izveidot kanāla pārdošanas cenas tirdzniecības līgumus.</span><span class="sxs-lookup"><span data-stu-id="2472c-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="2472c-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="2472c-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="2472c-106">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Cenu noteikšana un atlaides > Cenu grupas > Visas cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="2472c-106">Go to Retail and commerce > Pricing and discounts > Price groups > All price groups.</span></span>
    * <span data-ttu-id="2472c-107">Cenu grupas ir veids, kā tirdzniecības līgumi tiek piešķirti noteiktiem kanāliem.</span><span class="sxs-lookup"><span data-stu-id="2472c-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="2472c-108">Izmantojot cenu grupas, lai tirdzniecības līgumus piešķirtu kanāliem, var cenas var noteikt konkrētam kanālam.</span><span class="sxs-lookup"><span data-stu-id="2472c-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="2472c-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2472c-109">Click New.</span></span>
3. <span data-ttu-id="2472c-110">Laukā Cenu grupas ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2472c-110">In the Price groups field, type a value.</span></span>
4. <span data-ttu-id="2472c-111">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2472c-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2472c-112">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2472c-112">Click Save.</span></span>
6. <span data-ttu-id="2472c-113">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2472c-113">Close the page.</span></span>
7. <span data-ttu-id="2472c-114">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Kanāli > Mazumtirdzniecības veikali > Visi mazumtirdzniecības veikali.</span><span class="sxs-lookup"><span data-stu-id="2472c-114">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
8. <span data-ttu-id="2472c-115">Sarakstā atlasiet Ņujorka.</span><span class="sxs-lookup"><span data-stu-id="2472c-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="2472c-116">Darbību rūtī noklikšķiniet uz Veikals.</span><span class="sxs-lookup"><span data-stu-id="2472c-116">On the Action Pane, click Store.</span></span>
10. <span data-ttu-id="2472c-117">Noklikšķiniet uz Cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="2472c-117">Click Price groups.</span></span>
11. <span data-ttu-id="2472c-118">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2472c-118">Click New.</span></span>
12. <span data-ttu-id="2472c-119">Laukā Cenu grupas noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="2472c-119">In the Price groups field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="2472c-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2472c-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="2472c-121">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2472c-121">Click Save.</span></span>
15. <span data-ttu-id="2472c-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2472c-122">Close the page.</span></span>
16. <span data-ttu-id="2472c-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2472c-123">Close the page.</span></span>
17. <span data-ttu-id="2472c-124">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Preces un kategorijas > Izpildei nodotās preces pēc kategorijas.</span><span class="sxs-lookup"><span data-stu-id="2472c-124">Go to Retail and commerce > Products and categories > Released products by category.</span></span>
18. <span data-ttu-id="2472c-125">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2472c-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="2472c-126">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="2472c-126">Click Edit.</span></span>
20. <span data-ttu-id="2472c-127">Pārslēdziet sadaļas Pārdošana paplašināšanas veidu.</span><span class="sxs-lookup"><span data-stu-id="2472c-127">Toggle the expansion of the Sell section.</span></span>
21. <span data-ttu-id="2472c-128">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="2472c-128">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="2472c-129">Šī cena tiek izmantota, ja netika atrasts neviens atbilstošs tirdzniecības līgums.</span><span class="sxs-lookup"><span data-stu-id="2472c-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="2472c-130">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2472c-130">Click Save.</span></span>
23. <span data-ttu-id="2472c-131">Darbību rūtī noklikšķiniet uz Pārdot.</span><span class="sxs-lookup"><span data-stu-id="2472c-131">On the Action Pane, click Sell.</span></span>
24. <span data-ttu-id="2472c-132">Noklikšķiniet uz Izveidot tirdzniecības līgumus.</span><span class="sxs-lookup"><span data-stu-id="2472c-132">Click Create trade agreements.</span></span>
25. <span data-ttu-id="2472c-133">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="2472c-133">Click New.</span></span>
26. <span data-ttu-id="2472c-134">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="2472c-134">In the Name field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="2472c-135">Sarakstā atlasiet Mazumtirdzniecība.</span><span class="sxs-lookup"><span data-stu-id="2472c-135">In the list, select 'Retail'.</span></span>
    * <span data-ttu-id="2472c-136">Demonstrācijas datos žurnāla nosaukumam Mazumtirdzniecība ir noklusējuma relācija Cena (pārdošanas).</span><span class="sxs-lookup"><span data-stu-id="2472c-136">In the demo data, the 'Retail' journal name has the default relation of 'Price (sales)'.</span></span> <span data-ttu-id="2472c-137">Tas nozīmē, ka visām jaunajām rindām pēc noklusējuma tiks iestatīti pārdošanas cenas tirdzniecības līgumi.</span><span class="sxs-lookup"><span data-stu-id="2472c-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="2472c-138">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="2472c-138">Click Lines.</span></span>
29. <span data-ttu-id="2472c-139">Lauka Konta kods atlasiet Grupa.</span><span class="sxs-lookup"><span data-stu-id="2472c-139">In the Account code field, select 'Group'.</span></span>
30. <span data-ttu-id="2472c-140">Laukā Konta atlase noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="2472c-140">In the Account selection field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="2472c-141">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2472c-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2472c-142">Tādējādi tiks pabeigta piesaiste no kanāla uz cenu grupu uz tirdzniecības līgumu.</span><span class="sxs-lookup"><span data-stu-id="2472c-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="2472c-143">Laukā Krājumu saistība ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2472c-143">In the Item relation field, type a value.</span></span>
33. <span data-ttu-id="2472c-144">Laukā Summa valūtā ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="2472c-144">In the Amount in currency field, enter a number.</span></span>
34. <span data-ttu-id="2472c-145">Atzīmējiet izvēles rūtiņu Meklēt nākamo vai noņemiet atzīmi no tās.</span><span class="sxs-lookup"><span data-stu-id="2472c-145">Check or uncheck the Find next checkbox.</span></span>
    * <span data-ttu-id="2472c-146">Ja opcijai Meklēt nākamo ir iestatīts Jā, cenu noteikšanas programma turpinās meklēt atbilstošos tirdzniecības līgumus ar zemāku pārdošanas cenu.</span><span class="sxs-lookup"><span data-stu-id="2472c-146">When Find next is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="2472c-147">Ja opcijai Meklēt nākamo ir iestatīts Nē, cenu noteikšanas programma pārtrauc meklēšanu un izmanto tirdzniecības līgumu.</span><span class="sxs-lookup"><span data-stu-id="2472c-147">When Find next is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="2472c-148">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="2472c-148">Click Post.</span></span>
36. <span data-ttu-id="2472c-149">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2472c-149">Click OK.</span></span>
37. <span data-ttu-id="2472c-150">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2472c-150">Close the page.</span></span>
38. <span data-ttu-id="2472c-151">Darbību rūtī noklikšķiniet uz Pārdot.</span><span class="sxs-lookup"><span data-stu-id="2472c-151">On the Action Pane, click Sell.</span></span>
39. <span data-ttu-id="2472c-152">Noklikšķiniet uz Pārdošanas cena.</span><span class="sxs-lookup"><span data-stu-id="2472c-152">Click Sales price.</span></span>

