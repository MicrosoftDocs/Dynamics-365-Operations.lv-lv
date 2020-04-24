---
title: Likmju šablonu iestatīšana
description: Šajā procedūrā parādīts, kā iestatīt likmes šablonu.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91877c777c6f76bd4fcf1c786bd708051c2fcd47
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201460"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="0528c-103">Likmju šablonu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0528c-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0528c-104">Šajā procedūrā parādīts, kā iestatīt likmes šablonu.</span><span class="sxs-lookup"><span data-stu-id="0528c-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="0528c-105">Loģistikas vadītājs parasti iestata likmes šablonus, atkarībā no ar pārvadātājiem parakstītajiem līgumiem.</span><span class="sxs-lookup"><span data-stu-id="0528c-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="0528c-106">Šajā scenārijā iestatīsit likmes šablonu gaisa pārvadātājam.</span><span class="sxs-lookup"><span data-stu-id="0528c-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="0528c-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="0528c-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="0528c-108">Likmes šablona iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0528c-108">Set up rate master</span></span>
1. <span data-ttu-id="0528c-109">Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Vērtējums > Likmes šablons.</span><span class="sxs-lookup"><span data-stu-id="0528c-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="0528c-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0528c-110">Click New.</span></span>
3. <span data-ttu-id="0528c-111">Laukā Likmes šablons ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0528c-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="0528c-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0528c-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0528c-113">Laukā Vērtējuma metadatu ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0528c-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0528c-114">Vērtēšanas metadatu ID noteiks, kādi dati nepieciešami likmes šablonā, jo tas definē metadatus, kas nepieciešami šo likmes šablonu izmantojošajai TMS programmai.</span><span class="sxs-lookup"><span data-stu-id="0528c-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="0528c-115">Šim piemēram atlasiet opciju P2P</span><span class="sxs-lookup"><span data-stu-id="0528c-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="0528c-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0528c-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0528c-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0528c-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="0528c-118">Likmes bāzes tipa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0528c-118">Set up rate base</span></span>
1. <span data-ttu-id="0528c-119">Noklikšķiniet uz Likmes bāze.</span><span class="sxs-lookup"><span data-stu-id="0528c-119">Click Rate base.</span></span>
    * <span data-ttu-id="0528c-120">Likmes bāze nosaka pārvadātāja kursu, un to var izmantot, lai iestatītu tarifu struktūru un likmes strukturētu atbilstoši pārtraukumpunktiem, kas definēti pārtraukumu šablonā.</span><span class="sxs-lookup"><span data-stu-id="0528c-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="0528c-121">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0528c-121">Click New.</span></span>
3. <span data-ttu-id="0528c-122">Laukā Likmes bāze ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0528c-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="0528c-123">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0528c-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0528c-124">Laukā Pārtraukuma šablons noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0528c-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0528c-125">Pārtraukuma šabloni tiek izmantoti, lai noteiktu izcenojuma struktūru un tās pārtraukumpunktus.</span><span class="sxs-lookup"><span data-stu-id="0528c-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="0528c-126">Izcenojuma struktūra izmanto diferencētas cenas, kuru pamatā ir fiziskās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="0528c-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="0528c-127">Šim piemēram izmantojiet svaru</span><span class="sxs-lookup"><span data-stu-id="0528c-127">For this example, use weight</span></span>
7. <span data-ttu-id="0528c-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0528c-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0528c-129">Pārslēdziet sadaļas Detalizēti paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="0528c-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="0528c-130">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="0528c-130">Click New.</span></span>
10. <span data-ttu-id="0528c-131">Laukā Nodošanas pasta indekss no ierakstiet "30301".</span><span class="sxs-lookup"><span data-stu-id="0528c-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="0528c-132">Laukā Nodošanas pasta indekss uz ierakstiet "30318".</span><span class="sxs-lookup"><span data-stu-id="0528c-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="0528c-133">Laukā Nodošanas valsts reģions ierakstiet "ASV".</span><span class="sxs-lookup"><span data-stu-id="0528c-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="0528c-134">Laukā < 1,00 mārc. ierakstiet “100”.</span><span class="sxs-lookup"><span data-stu-id="0528c-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="0528c-135">Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 1 mārciņu.</span><span class="sxs-lookup"><span data-stu-id="0528c-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="0528c-136">Laukā <5,00 mārc. ierakstiet "300".</span><span class="sxs-lookup"><span data-stu-id="0528c-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="0528c-137">Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 5 mārciņām.</span><span class="sxs-lookup"><span data-stu-id="0528c-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="0528c-138">Laukā <20,00 mārc. ierakstiet "500".</span><span class="sxs-lookup"><span data-stu-id="0528c-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="0528c-139">Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 20 mārciņām.</span><span class="sxs-lookup"><span data-stu-id="0528c-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="0528c-140">Laukā <100,00 mārc. ierakstiet "1000".</span><span class="sxs-lookup"><span data-stu-id="0528c-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="0528c-141">Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 100 mārciņām.</span><span class="sxs-lookup"><span data-stu-id="0528c-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="0528c-142">Laukā <1000,00 mārc. ierakstiet "3000".</span><span class="sxs-lookup"><span data-stu-id="0528c-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="0528c-143">Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 1000 mārciņām.</span><span class="sxs-lookup"><span data-stu-id="0528c-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="0528c-144">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0528c-144">Click Save.</span></span>
19. <span data-ttu-id="0528c-145">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0528c-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="0528c-146">Likmes bāzes piešķiršana</span><span class="sxs-lookup"><span data-stu-id="0528c-146">Assign rate base</span></span>
1. <span data-ttu-id="0528c-147">Pārslēdziet sadaļas Likmes bāzes piešķires paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="0528c-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="0528c-148">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0528c-148">Click New.</span></span>
    * <span data-ttu-id="0528c-149">Katrā likmes šablonā var būt vairākas likmes bāzes piešķires.</span><span class="sxs-lookup"><span data-stu-id="0528c-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="0528c-150">Tas dod iespēju katram pārvadātājam izveidot vairākus dažādus cenu punktus atkarībā no galamērķiem, pakalpojumiem vai atšķirīgām pamatlikmēm.</span><span class="sxs-lookup"><span data-stu-id="0528c-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="0528c-151">Šajā procedūrā tiks izveidota tikai viena likmes bāzes piešķire.</span><span class="sxs-lookup"><span data-stu-id="0528c-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="0528c-152">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0528c-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0528c-153">Laukā Likmes bāze noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0528c-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0528c-154">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0528c-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0528c-155">Laukā Pakalpojums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0528c-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0528c-156">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0528c-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="0528c-157">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0528c-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0528c-158">Laukā Saņemšanas pasta indekss ierakstiet "98052".</span><span class="sxs-lookup"><span data-stu-id="0528c-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="0528c-159">Norādiet, no kura pasta koda ir spēkā šī likmes bāzes piešķire.</span><span class="sxs-lookup"><span data-stu-id="0528c-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="0528c-160">Laukā Saņemšanas valsts reģions ierakstiet "ASV".</span><span class="sxs-lookup"><span data-stu-id="0528c-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="0528c-161">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0528c-161">Click Save.</span></span>

