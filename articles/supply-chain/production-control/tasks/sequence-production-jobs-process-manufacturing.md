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
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e22c767a3de8fd937d9032a5bf285dfb4ced3d55
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981065"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="10861-103">Secības ražošanas darbi procesa ražošanai</span><span class="sxs-lookup"><span data-stu-id="10861-103">Sequence production jobs for process manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="10861-104">Šī procedūra izmanto krāsas produktus kā piemēru, lai parādītu kā izkārtot sērijā plānotos pasūtījumus atbilstoši krāsu un pakotnes lieluma prioritātei.</span><span class="sxs-lookup"><span data-stu-id="10861-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="10861-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USPI.</span><span class="sxs-lookup"><span data-stu-id="10861-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="10861-106">Šī procedūra ir paredzēta ražošanas plānotājam.</span><span class="sxs-lookup"><span data-stu-id="10861-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="10861-107">Palaist vispārējo USPI plānošanu</span><span class="sxs-lookup"><span data-stu-id="10861-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="10861-108">Doties uz Vispārējā plānošana > Vispārējā plānošana > Palaist > Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="10861-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="10861-109">Laukā Vispārējais plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="10861-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="10861-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="10861-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="10861-111">Atlasiet Vispārējais plāns.</span><span class="sxs-lookup"><span data-stu-id="10861-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="10861-112">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="10861-112">Click OK.</span></span>
    * <span data-ttu-id="10861-113">Tas aizsāks vispārējo plānošanu, ieskaitot sērijas procesu.</span><span class="sxs-lookup"><span data-stu-id="10861-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="10861-114">Šis process var aizņemt dažas minūtes.</span><span class="sxs-lookup"><span data-stu-id="10861-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="10861-115">Skatiet plānotos pasūtījumus krāsas precēm</span><span class="sxs-lookup"><span data-stu-id="10861-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="10861-116">Doties uz Vispārējā plānošana > Vispārējā plānošana > Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="10861-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="10861-117">Izvērsiet detalizētu Krājuma papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="10861-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="10861-118">Izvērsiet detalizētu Grafika papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="10861-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="10861-119">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="10861-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="10861-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="10861-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="10861-121">Atlasiet Vispārējais plāns.</span><span class="sxs-lookup"><span data-stu-id="10861-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="10861-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="10861-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="10861-123">Izmantojiet ātro filtru, lai Krājuma numura laukā filtrētu pēc vērtības P300.</span><span class="sxs-lookup"><span data-stu-id="10861-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="10861-124">Atbloķējiet, lai ritinātu pa labi, lai varētu skatīt pasūtījuma un piegādes datumu.</span><span class="sxs-lookup"><span data-stu-id="10861-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="10861-125">Ņemiet vērā, ka šo krājumu pasūtījuma datums ir Šodiena, un plānoto pasūtījumu piegādes datumiem nav noteikta secība pēc krāsas un iepakojuma izmēra prioritātes, kā parādīts preces nosaukumā.</span><span class="sxs-lookup"><span data-stu-id="10861-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="10861-126">Jūs varat virzīt peli virs krājuma koda, lai skatītu preces nosaukumu un prioritāti.</span><span class="sxs-lookup"><span data-stu-id="10861-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="10861-127">Ierindot plānotos krāsas pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="10861-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="10861-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="10861-128">Close the page.</span></span>
2. <span data-ttu-id="10861-129">Doties uz Vispārējā plānošana > Vispārējā plānošana > Ierindotie plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="10861-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="10861-130">Izvērsiet detalizētu Krājuma papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="10861-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="10861-131">Izvērsiet detalizētu Grafika papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="10861-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="10861-132">Piezīme: Šeit jūs redzat, ka sākuma datuma/laika secība plānotajiem pasūtījumiem tiek noteikta pēc krāsas un iepakojuma lieluma, ar 28 dienu laika intervālu.</span><span class="sxs-lookup"><span data-stu-id="10861-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="10861-133">Šie periodi tiek definēti ar skaitli laukā Kampaņa.</span><span class="sxs-lookup"><span data-stu-id="10861-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="10861-134">Ierindoto plānoto pasūtījumu forma darbojas tāpat kā parastas plānoto pasūtījumu formas, un ražošanas plānotājs var apstiprināt plānotos pasūtījumus šeit.</span><span class="sxs-lookup"><span data-stu-id="10861-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="10861-135">Atzīmēt visas rindas.</span><span class="sxs-lookup"><span data-stu-id="10861-135">Mark all rows.</span></span>
6. <span data-ttu-id="10861-136">Noklikšķiniet uz Akceptēt.</span><span class="sxs-lookup"><span data-stu-id="10861-136">Click Accept.</span></span>
    * <span data-ttu-id="10861-137">Tiks atjaunināti plānotie pasūtījumi ar atlasīto sērijas darbību - Atlikšana vai Turpināšana.</span><span class="sxs-lookup"><span data-stu-id="10861-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="10861-138">Pārbaudiet plānoto pasūtījumu secību</span><span class="sxs-lookup"><span data-stu-id="10861-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="10861-139">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="10861-139">Close the page.</span></span>
2. <span data-ttu-id="10861-140">Doties uz Vispārējā plānošana > Vispārējā plānošana > Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="10861-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="10861-141">Izvērsiet detalizētu Krājuma papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="10861-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="10861-142">Izvērsiet detalizētu Grafika papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="10861-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="10861-143">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="10861-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="10861-144">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="10861-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="10861-145">Atlasiet Vispārējais plāns.</span><span class="sxs-lookup"><span data-stu-id="10861-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="10861-146">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="10861-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="10861-147">Izmantojiet ātro filtru, lai Krājuma numura laukā filtrētu pēc vērtības P300.</span><span class="sxs-lookup"><span data-stu-id="10861-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="10861-148">Ņemiet vērā, ka pasūtījumiem tagad tiek noteikta secība atbilstoši krāsu un izmēru prioritātei, un plānoto pasūtījumu izpilde tiek sākta no pirmā pasūtījuma un piegādes datuma.</span><span class="sxs-lookup"><span data-stu-id="10861-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="10861-149">Pārbaudiet pasūtījuma datuma kolonna vai Sākuma datumu grafika papildinformācijas rūtī.</span><span class="sxs-lookup"><span data-stu-id="10861-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  

