---
title: Izveidot materiālu plānu līdzproduktiem
description: Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5915dca3af0650883ef5c90dbc50332af5be6cbd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209678"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="a36ec-103">Izveidot materiālu plānu līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="a36ec-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a36ec-104">Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti.</span><span class="sxs-lookup"><span data-stu-id="a36ec-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="a36ec-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USP2.</span><span class="sxs-lookup"><span data-stu-id="a36ec-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="a36ec-106">Vajadzības izveide līdzproduktam</span><span class="sxs-lookup"><span data-stu-id="a36ec-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="a36ec-107">Dodieties uz Noklusējuma informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="a36ec-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="a36ec-108">Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="a36ec-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="a36ec-109">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="a36ec-109">Click New.</span></span>
4. <span data-ttu-id="a36ec-110">Noklikšķiniet uz Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="a36ec-110">Click Sales order.</span></span>
5. <span data-ttu-id="a36ec-111">Laukā Debitora konts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a36ec-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="a36ec-112">Piemērs: US-001</span><span class="sxs-lookup"><span data-stu-id="a36ec-112">Example: US-001</span></span>  
6. <span data-ttu-id="a36ec-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a36ec-113">Click OK.</span></span>
7. <span data-ttu-id="a36ec-114">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a36ec-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a36ec-115">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="a36ec-115">Example: P6003</span></span>  
8. <span data-ttu-id="a36ec-116">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="a36ec-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a36ec-117">Piemērs: 50000</span><span class="sxs-lookup"><span data-stu-id="a36ec-117">Example: 50000</span></span>  
9. <span data-ttu-id="a36ec-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a36ec-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="a36ec-119">Materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="a36ec-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="a36ec-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a36ec-120">Close the page.</span></span>
2. <span data-ttu-id="a36ec-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a36ec-121">Close the page.</span></span>
3. <span data-ttu-id="a36ec-122">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="a36ec-122">Click Master planning.</span></span>
4. <span data-ttu-id="a36ec-123">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="a36ec-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a36ec-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a36ec-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a36ec-125">Piemērs: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="a36ec-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="a36ec-126">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="a36ec-126">Click Run.</span></span>
7. <span data-ttu-id="a36ec-127">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="a36ec-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="a36ec-128">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="a36ec-128">Click Filter.</span></span>
9. <span data-ttu-id="a36ec-129">Sarakstā atlasiet rindu Lauks = Krājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="a36ec-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="a36ec-130">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a36ec-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="a36ec-131">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="a36ec-131">Example: P6003</span></span>  
11. <span data-ttu-id="a36ec-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a36ec-132">Click OK.</span></span>
12. <span data-ttu-id="a36ec-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a36ec-133">Click OK.</span></span>
13. <span data-ttu-id="a36ec-134">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="a36ec-134">Click Planned orders.</span></span>
14. <span data-ttu-id="a36ec-135">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a36ec-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a36ec-136">Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".</span><span class="sxs-lookup"><span data-stu-id="a36ec-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="a36ec-137">Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a36ec-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="a36ec-138">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a36ec-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a36ec-139">Atlasiet jebkuru filtra atgriezto rindu.</span><span class="sxs-lookup"><span data-stu-id="a36ec-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="a36ec-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a36ec-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="a36ec-141">Izvērsiet vai sakļaujiet sadaļu Piesaiste.</span><span class="sxs-lookup"><span data-stu-id="a36ec-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="a36ec-142">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a36ec-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a36ec-143">Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="a36ec-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="a36ec-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a36ec-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="a36ec-145">Vajadzības izveide līdzproduktam</span><span class="sxs-lookup"><span data-stu-id="a36ec-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="a36ec-146">Dodieties uz Noklusējuma informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="a36ec-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="a36ec-147">Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="a36ec-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="a36ec-148">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="a36ec-148">Click New.</span></span>
4. <span data-ttu-id="a36ec-149">Noklikšķiniet uz Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="a36ec-149">Click Sales order.</span></span>
5. <span data-ttu-id="a36ec-150">Laukā Debitora konts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a36ec-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="a36ec-151">Piemērs: US-001</span><span class="sxs-lookup"><span data-stu-id="a36ec-151">Example: US-001</span></span>  
6. <span data-ttu-id="a36ec-152">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a36ec-152">Click OK.</span></span>
7. <span data-ttu-id="a36ec-153">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a36ec-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a36ec-154">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="a36ec-154">Example: P6003</span></span>  
8. <span data-ttu-id="a36ec-155">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="a36ec-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a36ec-156">Piemērs: 50000</span><span class="sxs-lookup"><span data-stu-id="a36ec-156">Example: 50000</span></span>  
9. <span data-ttu-id="a36ec-157">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a36ec-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="a36ec-158">Materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="a36ec-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="a36ec-159">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="a36ec-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="a36ec-160">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a36ec-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a36ec-161">Piemērs: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="a36ec-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="a36ec-162">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="a36ec-162">Click Run.</span></span>
4. <span data-ttu-id="a36ec-163">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="a36ec-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="a36ec-164">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="a36ec-164">Click Filter.</span></span>
6. <span data-ttu-id="a36ec-165">Sarakstā atlasiet rindu Lauks = Krājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="a36ec-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="a36ec-166">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a36ec-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="a36ec-167">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="a36ec-167">Example: P6003</span></span>  
8. <span data-ttu-id="a36ec-168">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a36ec-168">Click OK.</span></span>
9. <span data-ttu-id="a36ec-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a36ec-169">Click OK.</span></span>
10. <span data-ttu-id="a36ec-170">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="a36ec-170">Click Planned orders.</span></span>
11. <span data-ttu-id="a36ec-171">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a36ec-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a36ec-172">Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".</span><span class="sxs-lookup"><span data-stu-id="a36ec-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="a36ec-173">Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a36ec-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="a36ec-174">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a36ec-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a36ec-175">Atlasiet jebkuru filtra atgriezto rindu.</span><span class="sxs-lookup"><span data-stu-id="a36ec-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="a36ec-176">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a36ec-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="a36ec-177">Izvērsiet vai sakļaujiet sadaļu Piesaiste.</span><span class="sxs-lookup"><span data-stu-id="a36ec-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="a36ec-178">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a36ec-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a36ec-179">Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="a36ec-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="a36ec-180">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a36ec-180">Close the page.</span></span>
17. <span data-ttu-id="a36ec-181">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="a36ec-181">Click Master planning.</span></span>
18. <span data-ttu-id="a36ec-182">Doties uz Vispārējā plānošana > Iestatīšana > Vispārējas plānošanas parametri.</span><span class="sxs-lookup"><span data-stu-id="a36ec-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="a36ec-183">Laukā Atspējot visus plānošanas procesus atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="a36ec-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="a36ec-184">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a36ec-184">Close the page.</span></span>

