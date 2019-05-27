---
title: Ražošanas pasūtījuma sākšana
description: Šajā procedūrā parādīts, ka sākt ražošanas pasūtījumu ražotnē.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f83091a9f3e96a9176860bd16fa5969507488a25
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547472"
---
# <a name="start-a-production-order"></a><span data-ttu-id="12787-103">Ražošanas pasūtījuma sākšana</span><span class="sxs-lookup"><span data-stu-id="12787-103">Start a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12787-104">Šajā procedūrā parādīts, ka sākt ražošanas pasūtījumu ražotnē.</span><span class="sxs-lookup"><span data-stu-id="12787-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="12787-105">Šajā procesā tiek ziņots par laika un materiālu patēriņu.</span><span class="sxs-lookup"><span data-stu-id="12787-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="12787-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="12787-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="12787-107">Šī ir piektā procedūra no septiņām, kurā ir paskaidrots ražošanas pasūtījuma dzīves cikls.</span><span class="sxs-lookup"><span data-stu-id="12787-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="12787-108">Ražošanas pasūtījuma sākšana</span><span class="sxs-lookup"><span data-stu-id="12787-108">Start a production order</span></span>
1. <span data-ttu-id="12787-109">Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="12787-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="12787-110">Atlasiet ražošanas pasūtījumu, kura statuss ir Izlaists.</span><span class="sxs-lookup"><span data-stu-id="12787-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="12787-111">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="12787-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="12787-112">Noklikšķiniet uz Sākt.</span><span class="sxs-lookup"><span data-stu-id="12787-112">Click Start.</span></span>
    * <span data-ttu-id="12787-113">Šajā lapā var apstiprināt ražošanas pasūtījuma uzsākšanu.</span><span class="sxs-lookup"><span data-stu-id="12787-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="12787-114">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="12787-114">Click the General tab.</span></span>
5. <span data-ttu-id="12787-115">Laukā No operācijas Nr.</span><span class="sxs-lookup"><span data-stu-id="12787-115">In the From Oper.</span></span> <span data-ttu-id="12787-116">Nr.p.k.</span><span class="sxs-lookup"><span data-stu-id="12787-116">No.</span></span> <span data-ttu-id="12787-117">ievadiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="12787-117">field, enter '10'.</span></span>
6. <span data-ttu-id="12787-118">Laukā Automātisks maršruta patēriņš atlasiet "Vienmēr".</span><span class="sxs-lookup"><span data-stu-id="12787-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="12787-119">Noklikšķiniet uz izvēles rūtiņas Grāmatot maršruta karti tagad.</span><span class="sxs-lookup"><span data-stu-id="12787-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="12787-120">Laukā Automātisks MK patēriņš atlasiet "Vienmēr".</span><span class="sxs-lookup"><span data-stu-id="12787-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="12787-121">Noklikšķiniet uz izvēles rūtiņas Grāmatot izdošanas sarakstu tagad.</span><span class="sxs-lookup"><span data-stu-id="12787-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="12787-122">Noklikšķiniet uz izvēles rūtiņas Drukāt izdošanas sarakstu.</span><span class="sxs-lookup"><span data-stu-id="12787-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="12787-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="12787-123">Click OK.</span></span>
    * <span data-ttu-id="12787-124">Tas ir drukāts izdošanas saraksts, kurā norādīti materiāli, ko izmanto ražošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="12787-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="12787-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="12787-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="12787-126">Izdošanas saraksta apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="12787-126">Validate the picking list</span></span>
1. <span data-ttu-id="12787-127">Darbību rūtī noklikšķiniet uz Skatīt.</span><span class="sxs-lookup"><span data-stu-id="12787-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="12787-128">Noklikšķiniet uz Izdošanas saraksts.</span><span class="sxs-lookup"><span data-stu-id="12787-128">Click Picking list.</span></span>
3. <span data-ttu-id="12787-129">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="12787-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="12787-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="12787-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="12787-131">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="12787-131">Click Edit.</span></span>
6. <span data-ttu-id="12787-132">Laukā Patēriņš ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="12787-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="12787-133">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="12787-133">Click Post.</span></span>
8. <span data-ttu-id="12787-134">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="12787-134">Click OK.</span></span>
    * <span data-ttu-id="12787-135">Izdošanas saraksta žurnālā tiek grāmatoti ražošanas pasūtījumam patērētie materiāli.</span><span class="sxs-lookup"><span data-stu-id="12787-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="12787-136">Pirms žurnāla grāmatošanas var veikt korekcijas, ja pastāv starpība starp novērtēto daudzumu un faktisko patērēto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="12787-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="12787-137">Noklikšķiniet uz cilnes GridPanel.</span><span class="sxs-lookup"><span data-stu-id="12787-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="12787-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="12787-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="12787-139">Maršruta kartes žurnāla pārbaude</span><span class="sxs-lookup"><span data-stu-id="12787-139">Verify the route card journal</span></span>
1. <span data-ttu-id="12787-140">Darbību rūtī noklikšķiniet uz Skatīt.</span><span class="sxs-lookup"><span data-stu-id="12787-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="12787-141">Noklikšķiniet uz Maršruta karte.</span><span class="sxs-lookup"><span data-stu-id="12787-141">Click Route card.</span></span>
3. <span data-ttu-id="12787-142">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="12787-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="12787-143">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="12787-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="12787-144">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="12787-144">Click Edit.</span></span>
6. <span data-ttu-id="12787-145">Laukā Stundas ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="12787-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="12787-146">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="12787-146">Click Post.</span></span>
8. <span data-ttu-id="12787-147">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="12787-147">Click OK.</span></span>
    * <span data-ttu-id="12787-148">Maršruta karšu žurnālā tiek reģistrēts uz atsevišķām operācijām patērētais laiks.</span><span class="sxs-lookup"><span data-stu-id="12787-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="12787-149">Var ziņot arī par labu vai kļūdainu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="12787-149">Good and error quantity can also be reported.</span></span>  
