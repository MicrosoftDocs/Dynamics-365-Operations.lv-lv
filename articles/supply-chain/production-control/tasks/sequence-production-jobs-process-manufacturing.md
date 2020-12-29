---
title: Secības ražošanas darbi procesa ražošanai
description: Šī procedūra izmanto krāsas produktus kā piemēru, lai parādītu kā izkārtot sērijā plānotos pasūtījumus atbilstoši krāsu un pakotnes lieluma prioritātei.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db2c881f60b6e5251e2bcdf198da9e1c9f39a0e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432736"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="e4780-103">Secības ražošanas darbi procesa ražošanai</span><span class="sxs-lookup"><span data-stu-id="e4780-103">Sequence production jobs for process manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4780-104">Šī procedūra izmanto krāsas produktus kā piemēru, lai parādītu kā izkārtot sērijā plānotos pasūtījumus atbilstoši krāsu un pakotnes lieluma prioritātei.</span><span class="sxs-lookup"><span data-stu-id="e4780-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="e4780-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USPI.</span><span class="sxs-lookup"><span data-stu-id="e4780-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="e4780-106">Šī procedūra ir paredzēta ražošanas plānotājam.</span><span class="sxs-lookup"><span data-stu-id="e4780-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="e4780-107">Palaist vispārējo USPI plānošanu</span><span class="sxs-lookup"><span data-stu-id="e4780-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="e4780-108">Doties uz Vispārējā plānošana > Vispārējā plānošana > Palaist > Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="e4780-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="e4780-109">Laukā Vispārējais plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="e4780-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e4780-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e4780-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e4780-111">Atlasiet Vispārējais plāns.</span><span class="sxs-lookup"><span data-stu-id="e4780-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="e4780-112">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e4780-112">Click OK.</span></span>
    * <span data-ttu-id="e4780-113">Tas aizsāks vispārējo plānošanu, ieskaitot sērijas procesu.</span><span class="sxs-lookup"><span data-stu-id="e4780-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="e4780-114">Šis process var aizņemt dažas minūtes.</span><span class="sxs-lookup"><span data-stu-id="e4780-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="e4780-115">Skatiet plānotos pasūtījumus krāsas precēm</span><span class="sxs-lookup"><span data-stu-id="e4780-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="e4780-116">Doties uz Vispārējā plānošana > Vispārējā plānošana > Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="e4780-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="e4780-117">Izvērsiet detalizētu Krājuma papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="e4780-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="e4780-118">Izvērsiet detalizētu Grafika papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="e4780-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="e4780-119">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="e4780-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e4780-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e4780-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e4780-121">Atlasiet Vispārējais plāns.</span><span class="sxs-lookup"><span data-stu-id="e4780-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="e4780-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e4780-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e4780-123">Izmantojiet ātro filtru, lai Krājuma numura laukā filtrētu pēc vērtības P300.</span><span class="sxs-lookup"><span data-stu-id="e4780-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="e4780-124">Atbloķējiet, lai ritinātu pa labi, lai varētu skatīt pasūtījuma un piegādes datumu.</span><span class="sxs-lookup"><span data-stu-id="e4780-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="e4780-125">Ņemiet vērā, ka šo krājumu pasūtījuma datums ir Šodiena, un plānoto pasūtījumu piegādes datumiem nav noteikta secība pēc krāsas un iepakojuma izmēra prioritātes, kā parādīts preces nosaukumā.</span><span class="sxs-lookup"><span data-stu-id="e4780-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="e4780-126">Jūs varat virzīt peli virs krājuma koda, lai skatītu preces nosaukumu un prioritāti.</span><span class="sxs-lookup"><span data-stu-id="e4780-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="e4780-127">Ierindot plānotos krāsas pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="e4780-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="e4780-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e4780-128">Close the page.</span></span>
2. <span data-ttu-id="e4780-129">Doties uz Vispārējā plānošana > Vispārējā plānošana > Ierindotie plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="e4780-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="e4780-130">Izvērsiet detalizētu Krājuma papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="e4780-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="e4780-131">Izvērsiet detalizētu Grafika papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="e4780-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="e4780-132">Piezīme: Šeit jūs redzat, ka sākuma datuma/laika secība plānotajiem pasūtījumiem tiek noteikta pēc krāsas un iepakojuma lieluma, ar 28 dienu laika intervālu.</span><span class="sxs-lookup"><span data-stu-id="e4780-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="e4780-133">Šie periodi tiek definēti ar skaitli laukā Kampaņa.</span><span class="sxs-lookup"><span data-stu-id="e4780-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="e4780-134">Ierindoto plānoto pasūtījumu forma darbojas tāpat kā parastas plānoto pasūtījumu formas, un ražošanas plānotājs var apstiprināt plānotos pasūtījumus šeit.</span><span class="sxs-lookup"><span data-stu-id="e4780-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="e4780-135">Atzīmēt visas rindas.</span><span class="sxs-lookup"><span data-stu-id="e4780-135">Mark all rows.</span></span>
6. <span data-ttu-id="e4780-136">Noklikšķiniet uz Akceptēt.</span><span class="sxs-lookup"><span data-stu-id="e4780-136">Click Accept.</span></span>
    * <span data-ttu-id="e4780-137">Tiks atjaunināti plānotie pasūtījumi ar atlasīto sērijas darbību - Atlikšana vai Turpināšana.</span><span class="sxs-lookup"><span data-stu-id="e4780-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="e4780-138">Pārbaudiet plānoto pasūtījumu secību</span><span class="sxs-lookup"><span data-stu-id="e4780-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="e4780-139">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e4780-139">Close the page.</span></span>
2. <span data-ttu-id="e4780-140">Doties uz Vispārējā plānošana > Vispārējā plānošana > Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="e4780-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="e4780-141">Izvērsiet detalizētu Krājuma papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="e4780-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="e4780-142">Izvērsiet detalizētu Grafika papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="e4780-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="e4780-143">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="e4780-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e4780-144">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e4780-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e4780-145">Atlasiet Vispārējais plāns.</span><span class="sxs-lookup"><span data-stu-id="e4780-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="e4780-146">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e4780-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e4780-147">Izmantojiet ātro filtru, lai Krājuma numura laukā filtrētu pēc vērtības P300.</span><span class="sxs-lookup"><span data-stu-id="e4780-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="e4780-148">Ņemiet vērā, ka pasūtījumiem tagad tiek noteikta secība atbilstoši krāsu un izmēru prioritātei, un plānoto pasūtījumu izpilde tiek sākta no pirmā pasūtījuma un piegādes datuma.</span><span class="sxs-lookup"><span data-stu-id="e4780-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="e4780-149">Pārbaudiet pasūtījuma datuma kolonna vai Sākuma datumu grafika papildinformācijas rūtī.</span><span class="sxs-lookup"><span data-stu-id="e4780-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  

