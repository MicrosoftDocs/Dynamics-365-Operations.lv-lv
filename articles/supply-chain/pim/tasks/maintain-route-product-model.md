---
title: Preces modeļa maršruta uzturēšana
description: Šīs procedūras veikšanai ir nepieciešams, lai būtu preces konfigurācijas modelis.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e793466e021671501570aed06959d684d5e9c15
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "317158"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="9afbb-103">Preces modeļa maršruta uzturēšana</span><span class="sxs-lookup"><span data-stu-id="9afbb-103">Maintain route for a product model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9afbb-104">Šīs procedūras veikšanai ir nepieciešams, lai būtu preces konfigurācijas modelis.</span><span class="sxs-lookup"><span data-stu-id="9afbb-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="9afbb-105">Šai procedūrai tiek izmantots augstas kvalitātes skaļruņu modelis demonstrācijas uzņēmumā USMF, lai sniegtu jums informāciju par šo procesu.</span><span class="sxs-lookup"><span data-stu-id="9afbb-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="9afbb-106">Maršruta operācijas pievienošana</span><span class="sxs-lookup"><span data-stu-id="9afbb-106">Add a route operation</span></span>
1. <span data-ttu-id="9afbb-107">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="9afbb-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="9afbb-108">Noklikšķiniet uz Preču konfigurācijas modeļi.</span><span class="sxs-lookup"><span data-stu-id="9afbb-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="9afbb-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9afbb-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9afbb-110">Atlasiet augstas kvalitātes skaļruņa modeli šim uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="9afbb-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="9afbb-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9afbb-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9afbb-112">Izvērsiet sadaļu Maršruta operācijas.</span><span class="sxs-lookup"><span data-stu-id="9afbb-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="9afbb-113">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9afbb-113">Click Add.</span></span>
7. <span data-ttu-id="9afbb-114">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9afbb-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="9afbb-115">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9afbb-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="9afbb-116">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9afbb-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="9afbb-117">Detalizētas informācijas par maršruta operāciju ievadīšana</span><span class="sxs-lookup"><span data-stu-id="9afbb-117">Enter route operation details</span></span>
1. <span data-ttu-id="9afbb-118">Noklikšķiniet uz Detalizēta informācija par maršruta operāciju.</span><span class="sxs-lookup"><span data-stu-id="9afbb-118">Click Route operation details.</span></span>
2. <span data-ttu-id="9afbb-119">Laukā Operācija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9afbb-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="9afbb-120">Laukā Oper.</span><span class="sxs-lookup"><span data-stu-id="9afbb-120">In the Oper.</span></span> <span data-ttu-id="9afbb-121">Nr.p.k.</span><span class="sxs-lookup"><span data-stu-id="9afbb-121">No.</span></span> <span data-ttu-id="9afbb-122">ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="9afbb-122">field, enter a number.</span></span>
    * <span data-ttu-id="9afbb-123">Operāciju numuri nosaka maršruta secību.</span><span class="sxs-lookup"><span data-stu-id="9afbb-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="9afbb-124">Katram maršruta operācijas rekvizītam var tikt piešķirta statiska vērtība vai tas var tikt kartēts uz atribūtu.</span><span class="sxs-lookup"><span data-stu-id="9afbb-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="9afbb-125">Kartēšanas uz atribūtu rezultātā vērtība tiks iestatīta kā daļa no konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="9afbb-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="9afbb-126">Laukā Maršruta grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9afbb-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="9afbb-127">Maršruta grupa nosaka būtiskus aspektus izmaksu grāmatošanai, patēriņam un iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="9afbb-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="9afbb-128">Noklikšķiniet uz cilnes Iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="9afbb-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="9afbb-129">Noklikšķiniet uz cilnes Reizes.</span><span class="sxs-lookup"><span data-stu-id="9afbb-129">Click the Times tab.</span></span>
7. <span data-ttu-id="9afbb-130">Laukā Apstrādes daudz. ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="9afbb-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="9afbb-131">Nosakiet, cik daudzi tiks apstrādāti vienas operācijas ietvaros.</span><span class="sxs-lookup"><span data-stu-id="9afbb-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="9afbb-132">Laukā Stundas/laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9afbb-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="9afbb-133">Ievadiet laiku koeficientu.</span><span class="sxs-lookup"><span data-stu-id="9afbb-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="9afbb-134">Atzīmējiet izvēles rūtiņu Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="9afbb-134">Select the Set check box.</span></span>
10. <span data-ttu-id="9afbb-135">Laukā Izpildes laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9afbb-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="9afbb-136">Nosakiet apstrādes laiku jūsu norādītajam daudzumam.</span><span class="sxs-lookup"><span data-stu-id="9afbb-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="9afbb-137">Noklikšķiniet uz cilnes Resursu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="9afbb-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="9afbb-138">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9afbb-138">Click Add.</span></span>
13. <span data-ttu-id="9afbb-139">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9afbb-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="9afbb-140">Laukā Vajadzības veids atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="9afbb-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="9afbb-141">Izlemiet, vai vēlaties norādīt konkrētus resursus vai iespējas, kurām tiem jābūt.</span><span class="sxs-lookup"><span data-stu-id="9afbb-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="9afbb-142">Laukā Vajadzība ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9afbb-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="9afbb-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9afbb-143">Click OK.</span></span>

