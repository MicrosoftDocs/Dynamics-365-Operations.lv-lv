--- 
title: "Kanāla tirdzniecības līgumu izveide"
description: "Šajā procedūrā parādīts, kā izveidot kanāla pārdošanas cenas tirdzniecības līgumus."
author: josaw1
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 4cc797d2e23f0c7b14564415de6153ac0894c727
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="create-channel-specific-trade-agreements"></a><span data-ttu-id="4430e-103">Kanāla tirdzniecības līgumu izveide</span><span class="sxs-lookup"><span data-stu-id="4430e-103">Create channel-specific trade agreements</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4430e-104">Šajā procedūrā parādīts, kā izveidot kanāla pārdošanas cenas tirdzniecības līgumus.</span><span class="sxs-lookup"><span data-stu-id="4430e-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="4430e-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="4430e-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="4430e-106">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Cenu noteikšana un atlaides > Cenu grupas > Visas cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="4430e-106">Go to Retail and commerce > Pricing and discounts > Price groups > All price groups.</span></span>
    * <span data-ttu-id="4430e-107">Cenu grupas ir veids, kā tirdzniecības līgumi tiek piešķirti noteiktiem kanāliem.</span><span class="sxs-lookup"><span data-stu-id="4430e-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="4430e-108">Izmantojot cenu grupas, lai tirdzniecības līgumus piešķirtu kanāliem, var cenas var noteikt konkrētam kanālam.</span><span class="sxs-lookup"><span data-stu-id="4430e-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="4430e-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4430e-109">Click New.</span></span>
3. <span data-ttu-id="4430e-110">Laukā Cenu grupas ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="4430e-110">In the Price groups field, type a value.</span></span>
4. <span data-ttu-id="4430e-111">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4430e-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="4430e-112">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="4430e-112">Click Save.</span></span>
6. <span data-ttu-id="4430e-113">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="4430e-113">Close the page.</span></span>
7. <span data-ttu-id="4430e-114">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Kanāli > Mazumtirdzniecības veikali > Visi mazumtirdzniecības veikali.</span><span class="sxs-lookup"><span data-stu-id="4430e-114">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
8. <span data-ttu-id="4430e-115">Sarakstā atlasiet Ņujorka.</span><span class="sxs-lookup"><span data-stu-id="4430e-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="4430e-116">Darbību rūtī noklikšķiniet uz Veikals.</span><span class="sxs-lookup"><span data-stu-id="4430e-116">On the Action Pane, click Store.</span></span>
10. <span data-ttu-id="4430e-117">Noklikšķiniet uz Cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="4430e-117">Click Price groups.</span></span>
11. <span data-ttu-id="4430e-118">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4430e-118">Click New.</span></span>
12. <span data-ttu-id="4430e-119">Laukā Cenu grupas noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="4430e-119">In the Price groups field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="4430e-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4430e-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="4430e-121">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="4430e-121">Click Save.</span></span>
15. <span data-ttu-id="4430e-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="4430e-122">Close the page.</span></span>
16. <span data-ttu-id="4430e-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="4430e-123">Close the page.</span></span>
17. <span data-ttu-id="4430e-124">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Preces un kategorijas > Izpildei nodotās preces pēc kategorijas.</span><span class="sxs-lookup"><span data-stu-id="4430e-124">Go to Retail and commerce > Products and categories > Released products by category.</span></span>
18. <span data-ttu-id="4430e-125">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="4430e-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="4430e-126">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="4430e-126">Click Edit.</span></span>
20. <span data-ttu-id="4430e-127">Pārslēdziet sadaļas Pārdošana paplašināšanas veidu.</span><span class="sxs-lookup"><span data-stu-id="4430e-127">Toggle the expansion of the Sell section.</span></span>
21. <span data-ttu-id="4430e-128">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="4430e-128">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="4430e-129">Šī cena tiek izmantota, ja netika atrasts neviens atbilstošs tirdzniecības līgums.</span><span class="sxs-lookup"><span data-stu-id="4430e-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="4430e-130">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="4430e-130">Click Save.</span></span>
23. <span data-ttu-id="4430e-131">Darbību rūtī noklikšķiniet uz Pārdot.</span><span class="sxs-lookup"><span data-stu-id="4430e-131">On the Action Pane, click Sell.</span></span>
24. <span data-ttu-id="4430e-132">Noklikšķiniet uz Izveidot tirdzniecības līgumus.</span><span class="sxs-lookup"><span data-stu-id="4430e-132">Click Create trade agreements.</span></span>
25. <span data-ttu-id="4430e-133">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="4430e-133">Click New.</span></span>
26. <span data-ttu-id="4430e-134">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="4430e-134">In the Name field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="4430e-135">Sarakstā atlasiet Mazumtirdzniecība.</span><span class="sxs-lookup"><span data-stu-id="4430e-135">In the list, select 'Retail'.</span></span>
    * <span data-ttu-id="4430e-136">Demonstrācijas datos žurnāla nosaukumam Mazumtirdzniecība ir noklusējuma relācija Cena (pārdošanas).</span><span class="sxs-lookup"><span data-stu-id="4430e-136">In the demo data, the 'Retail' journal name has the default relation of 'Price (sales)'.</span></span> <span data-ttu-id="4430e-137">Tas nozīmē, ka visām jaunajām rindām pēc noklusējuma tiks iestatīti pārdošanas cenas tirdzniecības līgumi.</span><span class="sxs-lookup"><span data-stu-id="4430e-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="4430e-138">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="4430e-138">Click Lines.</span></span>
29. <span data-ttu-id="4430e-139">Lauka Konta kods atlasiet Grupa.</span><span class="sxs-lookup"><span data-stu-id="4430e-139">In the Account code field, select 'Group'.</span></span>
30. <span data-ttu-id="4430e-140">Laukā Konta atlase noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="4430e-140">In the Account selection field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="4430e-141">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4430e-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4430e-142">Tādējādi tiks pabeigta piesaiste no kanāla uz cenu grupu uz tirdzniecības līgumu.</span><span class="sxs-lookup"><span data-stu-id="4430e-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="4430e-143">Laukā Krājumu saistība ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="4430e-143">In the Item relation field, type a value.</span></span>
33. <span data-ttu-id="4430e-144">Laukā Summa valūtā ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="4430e-144">In the Amount in currency field, enter a number.</span></span>
34. <span data-ttu-id="4430e-145">Atzīmējiet izvēles rūtiņu Meklēt nākamo vai noņemiet atzīmi no tās.</span><span class="sxs-lookup"><span data-stu-id="4430e-145">Check or uncheck the Find next checkbox.</span></span>
    * <span data-ttu-id="4430e-146">Ja opcijai Meklēt nākamo ir iestatīts Jā, cenu noteikšanas programma turpinās meklēt atbilstošos tirdzniecības līgumus ar zemāku pārdošanas cenu.</span><span class="sxs-lookup"><span data-stu-id="4430e-146">When Find next is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="4430e-147">Ja opcijai Meklēt nākamo ir iestatīts Nē, cenu noteikšanas programma pārtrauc meklēšanu un izmanto tirdzniecības līgumu.</span><span class="sxs-lookup"><span data-stu-id="4430e-147">When Find next is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="4430e-148">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="4430e-148">Click Post.</span></span>
36. <span data-ttu-id="4430e-149">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="4430e-149">Click OK.</span></span>
37. <span data-ttu-id="4430e-150">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="4430e-150">Close the page.</span></span>
38. <span data-ttu-id="4430e-151">Darbību rūtī noklikšķiniet uz Pārdot.</span><span class="sxs-lookup"><span data-stu-id="4430e-151">On the Action Pane, click Sell.</span></span>
39. <span data-ttu-id="4430e-152">Noklikšķiniet uz Pārdošanas cena.</span><span class="sxs-lookup"><span data-stu-id="4430e-152">Click Sales price.</span></span>


