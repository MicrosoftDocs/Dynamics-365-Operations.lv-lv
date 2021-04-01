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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a87935f8f30d909f1a6a62ed7be00c83476a36a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214374"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="cbe5d-103">Izveidot materiālu plānu līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="cbe5d-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cbe5d-104">Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="cbe5d-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USP2.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="cbe5d-106">Vajadzības izveide līdzproduktam</span><span class="sxs-lookup"><span data-stu-id="cbe5d-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="cbe5d-107">Dodieties uz Noklusējuma informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="cbe5d-108">Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="cbe5d-109">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-109">Click New.</span></span>
4. <span data-ttu-id="cbe5d-110">Noklikšķiniet uz Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-110">Click Sales order.</span></span>
5. <span data-ttu-id="cbe5d-111">Laukā Debitora konts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="cbe5d-112">Piemērs: US-001</span><span class="sxs-lookup"><span data-stu-id="cbe5d-112">Example: US-001</span></span>  
6. <span data-ttu-id="cbe5d-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-113">Click OK.</span></span>
7. <span data-ttu-id="cbe5d-114">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="cbe5d-115">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="cbe5d-115">Example: P6003</span></span>  
8. <span data-ttu-id="cbe5d-116">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="cbe5d-117">Piemērs: 50000</span><span class="sxs-lookup"><span data-stu-id="cbe5d-117">Example: 50000</span></span>  
9. <span data-ttu-id="cbe5d-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="cbe5d-119">Materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="cbe5d-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="cbe5d-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-120">Close the page.</span></span>
2. <span data-ttu-id="cbe5d-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-121">Close the page.</span></span>
3. <span data-ttu-id="cbe5d-122">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-122">Click Master planning.</span></span>
4. <span data-ttu-id="cbe5d-123">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="cbe5d-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cbe5d-125">Piemērs: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="cbe5d-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="cbe5d-126">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-126">Click Run.</span></span>
7. <span data-ttu-id="cbe5d-127">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="cbe5d-128">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-128">Click Filter.</span></span>
9. <span data-ttu-id="cbe5d-129">Sarakstā atlasiet rindu Lauks = Krājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="cbe5d-130">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="cbe5d-131">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="cbe5d-131">Example: P6003</span></span>  
11. <span data-ttu-id="cbe5d-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-132">Click OK.</span></span>
12. <span data-ttu-id="cbe5d-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-133">Click OK.</span></span>
13. <span data-ttu-id="cbe5d-134">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-134">Click Planned orders.</span></span>
14. <span data-ttu-id="cbe5d-135">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="cbe5d-136">Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".</span><span class="sxs-lookup"><span data-stu-id="cbe5d-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="cbe5d-137">Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="cbe5d-138">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cbe5d-139">Atlasiet jebkuru filtra atgriezto rindu.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="cbe5d-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="cbe5d-141">Izvērsiet vai sakļaujiet sadaļu Piesaiste.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="cbe5d-142">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cbe5d-143">Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="cbe5d-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="cbe5d-145">Vajadzības izveide līdzproduktam</span><span class="sxs-lookup"><span data-stu-id="cbe5d-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="cbe5d-146">Dodieties uz Noklusējuma informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="cbe5d-147">Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="cbe5d-148">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-148">Click New.</span></span>
4. <span data-ttu-id="cbe5d-149">Noklikšķiniet uz Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-149">Click Sales order.</span></span>
5. <span data-ttu-id="cbe5d-150">Laukā Debitora konts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="cbe5d-151">Piemērs: US-001</span><span class="sxs-lookup"><span data-stu-id="cbe5d-151">Example: US-001</span></span>  
6. <span data-ttu-id="cbe5d-152">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-152">Click OK.</span></span>
7. <span data-ttu-id="cbe5d-153">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="cbe5d-154">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="cbe5d-154">Example: P6003</span></span>  
8. <span data-ttu-id="cbe5d-155">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="cbe5d-156">Piemērs: 50000</span><span class="sxs-lookup"><span data-stu-id="cbe5d-156">Example: 50000</span></span>  
9. <span data-ttu-id="cbe5d-157">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="cbe5d-158">Materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="cbe5d-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="cbe5d-159">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="cbe5d-160">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cbe5d-161">Piemērs: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="cbe5d-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="cbe5d-162">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-162">Click Run.</span></span>
4. <span data-ttu-id="cbe5d-163">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="cbe5d-164">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-164">Click Filter.</span></span>
6. <span data-ttu-id="cbe5d-165">Sarakstā atlasiet rindu Lauks = Krājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="cbe5d-166">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="cbe5d-167">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="cbe5d-167">Example: P6003</span></span>  
8. <span data-ttu-id="cbe5d-168">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-168">Click OK.</span></span>
9. <span data-ttu-id="cbe5d-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-169">Click OK.</span></span>
10. <span data-ttu-id="cbe5d-170">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-170">Click Planned orders.</span></span>
11. <span data-ttu-id="cbe5d-171">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="cbe5d-172">Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".</span><span class="sxs-lookup"><span data-stu-id="cbe5d-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="cbe5d-173">Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="cbe5d-174">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cbe5d-175">Atlasiet jebkuru filtra atgriezto rindu.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="cbe5d-176">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="cbe5d-177">Izvērsiet vai sakļaujiet sadaļu Piesaiste.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="cbe5d-178">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cbe5d-179">Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="cbe5d-180">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-180">Close the page.</span></span>
17. <span data-ttu-id="cbe5d-181">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-181">Click Master planning.</span></span>
18. <span data-ttu-id="cbe5d-182">Doties uz Vispārējā plānošana > Iestatīšana > Vispārējas plānošanas parametri.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="cbe5d-183">Laukā Atspējot visus plānošanas procesus atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="cbe5d-184">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cbe5d-184">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]