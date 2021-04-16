---
title: Likmju šablonu iestatīšana
description: Šajā procedūrā parādīts, kā iestatīt likmes šablonu.
author: ShylaThompson
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cb25726e05f11420c7355c39f7e262abca5da62
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808994"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="208d1-103">Likmju šablonu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="208d1-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="208d1-104">Šajā procedūrā parādīts, kā iestatīt likmes šablonu.</span><span class="sxs-lookup"><span data-stu-id="208d1-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="208d1-105">Loģistikas vadītājs parasti iestata likmes šablonus, atkarībā no ar pārvadātājiem parakstītajiem līgumiem.</span><span class="sxs-lookup"><span data-stu-id="208d1-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="208d1-106">Šajā scenārijā iestatīsit likmes šablonu gaisa pārvadātājam.</span><span class="sxs-lookup"><span data-stu-id="208d1-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="208d1-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="208d1-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="208d1-108">Pārtraukuma šablona iestatīšana</span><span class="sxs-lookup"><span data-stu-id="208d1-108">Set up break master</span></span>

1. <span data-ttu-id="208d1-109">Dodieties uz **Transportēšanas pārvaldība > Iestatīšana > Vērtējums > Pārtraukuma šablons**.</span><span class="sxs-lookup"><span data-stu-id="208d1-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="208d1-110">Pārtraukuma šabloni tiek izmantoti, lai noteiktu izcenojuma struktūru un tās pārtraukumpunktus.</span><span class="sxs-lookup"><span data-stu-id="208d1-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="208d1-111">Izcenojuma struktūra izmanto diferencētas cenas, kuru pamatā ir fiziskās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="208d1-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="208d1-112">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="208d1-112">Select **New**.</span></span>
1. <span data-ttu-id="208d1-113">Laukā **Pārtraukuma šablons** ievadiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="208d1-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="208d1-114">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="208d1-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="208d1-115">Laukā **Datu tips** atlasiet datu tipu.</span><span class="sxs-lookup"><span data-stu-id="208d1-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="208d1-116">Laukā **Salīdzinājums** ievadiet nepieciešamo salīdzinājuma veidu (izmantojot operatorus).</span><span class="sxs-lookup"><span data-stu-id="208d1-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="208d1-117">Laukā **Pārtraukuma vienība** ievadiet pārtraukuma vienības vērtības.</span><span class="sxs-lookup"><span data-stu-id="208d1-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="208d1-118">Sadaļā **Detalizēti** izveidojiet tik daudz pārtraukumu, cik nepieciešams cenu struktūrai.</span><span class="sxs-lookup"><span data-stu-id="208d1-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="208d1-119">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="208d1-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="208d1-120">Likmes šablona iestatīšana</span><span class="sxs-lookup"><span data-stu-id="208d1-120">Set up rate master</span></span>

1. <span data-ttu-id="208d1-121">Dodieties uz **Transportēšanas pārvaldība > Iestatīšana > Vērtējums > Likmes šablons**.</span><span class="sxs-lookup"><span data-stu-id="208d1-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="208d1-122">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="208d1-122">Select **New**.</span></span>
1. <span data-ttu-id="208d1-123">Laukā **Likmes šablons** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="208d1-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="208d1-124">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="208d1-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="208d1-125">Laukā **Vērtējuma metadatu ID** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="208d1-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="208d1-126">Vērtēšanas metadatu ID noteiks, kādi dati nepieciešami likmes šablonā, jo tas definē metadatus, kas nepieciešami šo likmes šablonu izmantojošajai pārvadājošajai pārvaldības programmai.</span><span class="sxs-lookup"><span data-stu-id="208d1-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="208d1-127">Šim piemēram atlasiet opciju P2P.</span><span class="sxs-lookup"><span data-stu-id="208d1-127">For this example, select the P2P option.</span></span> <span data-ttu-id="208d1-128">Tas jau ir definēts demonstrācijas datos.</span><span class="sxs-lookup"><span data-stu-id="208d1-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="208d1-129">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="208d1-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="208d1-130">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="208d1-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="208d1-131">Likmes bāzes tipa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="208d1-131">Set up rate base</span></span>

1. <span data-ttu-id="208d1-132">Atlasiet **Likmes bāze**.</span><span class="sxs-lookup"><span data-stu-id="208d1-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="208d1-133">Likmes bāze nosaka pārvadātāja kursu, un to var izmantot, lai iestatītu tarifu struktūru un likmes strukturētu atbilstoši pārtraukumpunktiem, kas definēti pārtraukumu šablonā.</span><span class="sxs-lookup"><span data-stu-id="208d1-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="208d1-134">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="208d1-134">Select **New**.</span></span>
3. <span data-ttu-id="208d1-135">Laukā **Likmes bāze** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="208d1-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="208d1-136">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="208d1-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="208d1-137">Laukā **Pārtraukuma šablons** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="208d1-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="208d1-138">Pārtraukuma šabloni tiek izmantoti, lai noteiktu izcenojuma struktūru un tās pārtraukumpunktus.</span><span class="sxs-lookup"><span data-stu-id="208d1-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="208d1-139">Izcenojuma struktūra izmanto diferencētas cenas, kuru pamatā ir fiziskās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="208d1-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="208d1-140">Šim piemēram izmantojiet svaru.</span><span class="sxs-lookup"><span data-stu-id="208d1-140">For this example, use weight.</span></span> <span data-ttu-id="208d1-141">Tas jau ir definēts demonstrācijas datos.</span><span class="sxs-lookup"><span data-stu-id="208d1-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="208d1-142">Sarakstā atlasiet saiti iezīmētajā rindā.</span><span class="sxs-lookup"><span data-stu-id="208d1-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="208d1-143">Izvērsiet sadaļu **Detalizēti**.</span><span class="sxs-lookup"><span data-stu-id="208d1-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="208d1-144">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="208d1-144">Select **New**.</span></span>
10. <span data-ttu-id="208d1-145">Laukā **Nodošanas pasta indekss no ierakstiet** ievadiet "30301".</span><span class="sxs-lookup"><span data-stu-id="208d1-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="208d1-146">Laukā **Nodošanas pasta indekss uz** ierakstiet "30318".</span><span class="sxs-lookup"><span data-stu-id="208d1-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="208d1-147">Laukā **Nodošanas valsts reģions** ierakstiet "ASV".</span><span class="sxs-lookup"><span data-stu-id="208d1-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="208d1-148">Laukā **<1,00 mārc.** ierakstiet “100”.</span><span class="sxs-lookup"><span data-stu-id="208d1-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="208d1-149">Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 1 mārciņu.</span><span class="sxs-lookup"><span data-stu-id="208d1-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="208d1-150">Laukā **<5,00 mārc.** ierakstiet “300”.</span><span class="sxs-lookup"><span data-stu-id="208d1-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="208d1-151">Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 5 mārciņām.</span><span class="sxs-lookup"><span data-stu-id="208d1-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="208d1-152">Laukā **<20,00 mārc.** ierakstiet “500”.</span><span class="sxs-lookup"><span data-stu-id="208d1-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="208d1-153">Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 20 mārciņām.</span><span class="sxs-lookup"><span data-stu-id="208d1-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="208d1-154">Laukā **<100,00 mārc.** ierakstiet “1000”.</span><span class="sxs-lookup"><span data-stu-id="208d1-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="208d1-155">Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 100 mārciņām.</span><span class="sxs-lookup"><span data-stu-id="208d1-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="208d1-156">Laukā **<1000,00 mārc.** ierakstiet “3000”.</span><span class="sxs-lookup"><span data-stu-id="208d1-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="208d1-157">Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 1000 mārciņām.</span><span class="sxs-lookup"><span data-stu-id="208d1-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="208d1-158">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="208d1-158">Select **Save**.</span></span>
19. <span data-ttu-id="208d1-159">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="208d1-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="208d1-160">Likmes bāzes piešķiršana</span><span class="sxs-lookup"><span data-stu-id="208d1-160">Assign rate base</span></span>

1. <span data-ttu-id="208d1-161">Izvērsiet sadaļu **Likmes bāzes piešķires**.</span><span class="sxs-lookup"><span data-stu-id="208d1-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="208d1-162">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="208d1-162">Select **New**.</span></span>
    * <span data-ttu-id="208d1-163">Katrā likmes šablonā var būt vairākas likmes bāzes piešķires.</span><span class="sxs-lookup"><span data-stu-id="208d1-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="208d1-164">Tas dod iespēju katram pārvadātājam izveidot vairākus dažādus cenu punktus atkarībā no galamērķiem, pakalpojumiem vai atšķirīgām pamatlikmēm.</span><span class="sxs-lookup"><span data-stu-id="208d1-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="208d1-165">Šajā procedūrā tiks izveidota tikai viena likmes bāzes piešķire.</span><span class="sxs-lookup"><span data-stu-id="208d1-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="208d1-166">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="208d1-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="208d1-167">Laukā **Likmes bāze** atlasiet nolaižamo saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="208d1-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="208d1-168">Sarakstā atlasiet saiti iezīmētajā rindā.</span><span class="sxs-lookup"><span data-stu-id="208d1-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="208d1-169">Laukā **Pakalpojums** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="208d1-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="208d1-170">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="208d1-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="208d1-171">Sarakstā atlasiet saiti iezīmētajā rindā.</span><span class="sxs-lookup"><span data-stu-id="208d1-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="208d1-172">Laukā **Saņemšanas pasta indekss** ierakstiet "98052".</span><span class="sxs-lookup"><span data-stu-id="208d1-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="208d1-173">Norādiet, no kura pasta koda ir spēkā šī likmes bāzes piešķire.</span><span class="sxs-lookup"><span data-stu-id="208d1-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="208d1-174">Laukā **Saņemšanas valsts reģions** ierakstiet "ASV".</span><span class="sxs-lookup"><span data-stu-id="208d1-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="208d1-175">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="208d1-175">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]