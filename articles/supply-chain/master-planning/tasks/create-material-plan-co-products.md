---
title: Izveidot materiālu plānu līdzproduktiem
description: Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920733"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="e4c8a-103">Izveidot materiālu plānu līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="e4c8a-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4c8a-104">Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="e4c8a-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USP2.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="e4c8a-106">Vajadzības izveide līdzproduktam</span><span class="sxs-lookup"><span data-stu-id="e4c8a-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="e4c8a-107">Dodieties uz **Pārdošana un mārketings \> Darbvietas \> Pārdošanas pasūtījumu apstrāde un pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="e4c8a-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-108">Select **New**.</span></span>
1. <span data-ttu-id="e4c8a-109">Atlasiet vienumu **Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="e4c8a-110">Laukā **Debitora konts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="e4c8a-111">Piemērs: US-001</span><span class="sxs-lookup"><span data-stu-id="e4c8a-111">Example: US-001</span></span>  
1. <span data-ttu-id="e4c8a-112">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-112">Select **OK**.</span></span>
1. <span data-ttu-id="e4c8a-113">Laukā **Krājuma kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="e4c8a-114">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="e4c8a-114">Example: P6003</span></span>  
1. <span data-ttu-id="e4c8a-115">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="e4c8a-116">Piemērs: 50000</span><span class="sxs-lookup"><span data-stu-id="e4c8a-116">Example: 50000</span></span>  
1. <span data-ttu-id="e4c8a-117">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="e4c8a-118">Materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="e4c8a-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="e4c8a-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-119">Close the page.</span></span>
1. <span data-ttu-id="e4c8a-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-120">Close the page.</span></span>
1. <span data-ttu-id="e4c8a-121">Atlasiet **Vispārējā plānošana**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="e4c8a-122">Laukā **Plāns** atlasiet nolaižamo pogu uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="e4c8a-123">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="e4c8a-124">Piemērs: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="e4c8a-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="e4c8a-125">Atlasiet **Izpildīt**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-125">Select **Run**.</span></span>
1. <span data-ttu-id="e4c8a-126">Izvērsiet vai sakļaujiet sadaļu **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="e4c8a-127">Atlasiet **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-127">Select **Filter**.</span></span>
1. <span data-ttu-id="e4c8a-128">Sarakstā atlasiet rindu **Lauks** = *Krājuma numurs*.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="e4c8a-129">Laukā **Kritēriji** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="e4c8a-130">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="e4c8a-130">Example: P6003</span></span>  
1. <span data-ttu-id="e4c8a-131">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-131">Select **OK**.</span></span>
1. <span data-ttu-id="e4c8a-132">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-132">Select **OK**.</span></span>
1. <span data-ttu-id="e4c8a-133">Atlasiet **Plānotie pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="e4c8a-134">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e4c8a-135">Piemēram, filtrējiet pēc lauka **Krājuma numurs**, izmantojot vērtību "P6000".</span><span class="sxs-lookup"><span data-stu-id="e4c8a-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="e4c8a-136">Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="e4c8a-137">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e4c8a-138">Atlasiet jebkuru filtra atgriezto rindu.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="e4c8a-139">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="e4c8a-140">Izvērsiet sadaļu **Piesaiste**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="e4c8a-141">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="e4c8a-142">Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="e4c8a-143">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="e4c8a-144">Otras vajadzības izveide līdzproduktam</span><span class="sxs-lookup"><span data-stu-id="e4c8a-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="e4c8a-145">Dodieties uz **Pārdošana un mārketings \> Darbvietas \> Pārdošanas pasūtījumu apstrāde un pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="e4c8a-146">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-146">Select **New**.</span></span>
1. <span data-ttu-id="e4c8a-147">Atlasiet vienumu **Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="e4c8a-148">Laukā **Debitora konts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="e4c8a-149">Piemērs: US-001</span><span class="sxs-lookup"><span data-stu-id="e4c8a-149">Example: US-001</span></span>  
1. <span data-ttu-id="e4c8a-150">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-150">Select **OK**.</span></span>
1. <span data-ttu-id="e4c8a-151">Laukā **Krājuma kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="e4c8a-152">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="e4c8a-152">Example: P6003</span></span>  
1. <span data-ttu-id="e4c8a-153">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="e4c8a-154">Piemērs: 50000</span><span class="sxs-lookup"><span data-stu-id="e4c8a-154">Example: 50000</span></span>  
1. <span data-ttu-id="e4c8a-155">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="e4c8a-156">Otra materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="e4c8a-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="e4c8a-157">Laukā **Plāns** atlasiet nolaižamo pogu uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="e4c8a-158">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="e4c8a-159">Piemērs: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="e4c8a-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="e4c8a-160">Atlasiet **Izpildīt**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-160">Select **Run**.</span></span>
4. <span data-ttu-id="e4c8a-161">Izvērsiet vai sakļaujiet sadaļu **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="e4c8a-162">Atlasiet **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-162">Select **Filter**.</span></span>
6. <span data-ttu-id="e4c8a-163">Sarakstā atlasiet rindu **Lauks** = *Krājuma numurs*.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="e4c8a-164">Laukā *Kritēriji* ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="e4c8a-165">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="e4c8a-165">Example: P6003</span></span>  
8. <span data-ttu-id="e4c8a-166">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-166">Select **OK**.</span></span>
9. <span data-ttu-id="e4c8a-167">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-167">Select **OK**.</span></span>
10. <span data-ttu-id="e4c8a-168">Atlasiet **Plānotie pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="e4c8a-169">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e4c8a-170">Piemēram, filtrējiet pēc lauka **Krājuma numurs**, izmantojot vērtību "P6000".</span><span class="sxs-lookup"><span data-stu-id="e4c8a-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="e4c8a-171">Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="e4c8a-172">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e4c8a-173">Atlasiet jebkuru filtra atgriezto rindu.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="e4c8a-174">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="e4c8a-175">Izvērsiet vai sakļaujiet sadaļu **Piesaiste**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="e4c8a-176">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="e4c8a-177">Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="e4c8a-178">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-178">Close the page.</span></span>
17. <span data-ttu-id="e4c8a-179">Atlasiet **Vispārējā plānošana**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="e4c8a-180">Dodieties uz **Vispārējā plānošana \> Iestatīšana \> Vispārējas plānošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="e4c8a-181">Laukā **Atspējot visus plānošanas procesus** atlasiet *Nē*.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="e4c8a-182">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e4c8a-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]