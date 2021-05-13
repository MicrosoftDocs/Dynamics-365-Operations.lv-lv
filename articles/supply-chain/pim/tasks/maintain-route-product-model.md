---
title: Preces modeļa maršruta uzturēšana
description: Šīs procedūras veikšanai ir nepieciešams, lai būtu preces konfigurācijas modelis.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921269"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="71c7f-103">Preces modeļa maršruta uzturēšana</span><span class="sxs-lookup"><span data-stu-id="71c7f-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71c7f-104">Šīs procedūras veikšanai ir nepieciešams, lai būtu preces konfigurācijas modelis.</span><span class="sxs-lookup"><span data-stu-id="71c7f-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="71c7f-105">Šai procedūrai tiek izmantots augstas kvalitātes skaļruņu modelis demonstrācijas uzņēmumā USMF, lai sniegtu jums informāciju par šo procesu.</span><span class="sxs-lookup"><span data-stu-id="71c7f-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="71c7f-106">Maršruta operācijas pievienošana</span><span class="sxs-lookup"><span data-stu-id="71c7f-106">Add a route operation</span></span>

1. <span data-ttu-id="71c7f-107">Dodieties uz **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="71c7f-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="71c7f-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="71c7f-109">Atlasiet augstas kvalitātes skaļruņa modeli šim uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="71c7f-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="71c7f-110">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="71c7f-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="71c7f-111">Izvērsiet sadaļu **Maršruta operācijas**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="71c7f-112">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-112">Select **Add**.</span></span>
1. <span data-ttu-id="71c7f-113">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="71c7f-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="71c7f-114">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="71c7f-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="71c7f-115">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="71c7f-116">Detalizētas informācijas par maršruta operāciju ievadīšana</span><span class="sxs-lookup"><span data-stu-id="71c7f-116">Enter route operation details</span></span>

1. <span data-ttu-id="71c7f-117">Atlasiet **Detalizēta informācija par maršruta operāciju**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="71c7f-118">Laukā **Operācija** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="71c7f-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="71c7f-119">Laukā **Operācijas Nr.**</span><span class="sxs-lookup"><span data-stu-id="71c7f-119">In the **Oper. No.**</span></span> <span data-ttu-id="71c7f-120">ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="71c7f-120">field, enter a number.</span></span>
    * <span data-ttu-id="71c7f-121">Operāciju numuri nosaka maršruta secību.</span><span class="sxs-lookup"><span data-stu-id="71c7f-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="71c7f-122">Katram maršruta operācijas rekvizītam var tikt piešķirta statiska vērtība vai tas var tikt kartēts uz atribūtu.</span><span class="sxs-lookup"><span data-stu-id="71c7f-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="71c7f-123">Kartēšanas uz atribūtu rezultātā vērtība tiks iestatīta kā daļa no konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="71c7f-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="71c7f-124">Laukā **Maršruta grupa** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="71c7f-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="71c7f-125">Maršruta grupa nosaka būtiskus aspektus izmaksu grāmatošanai, patēriņam un iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="71c7f-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="71c7f-126">Atlasiet cilni **Iestatījums**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="71c7f-127">Atlasiet cilni **Laiki**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="71c7f-128">Laukā **Apstrādes daudz.** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="71c7f-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="71c7f-129">Nosakiet, cik daudzi tiks apstrādāti vienas operācijas ietvaros.</span><span class="sxs-lookup"><span data-stu-id="71c7f-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="71c7f-130">Laukā **Stundas/laiks** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="71c7f-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="71c7f-131">Ievadiet laiku koeficientu.</span><span class="sxs-lookup"><span data-stu-id="71c7f-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="71c7f-132">Atzīmējiet izvēles rūtiņu **Iestatīt**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="71c7f-133">Laukā **Izpildes laiks** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="71c7f-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="71c7f-134">Nosakiet apstrādes laiku jūsu norādītajam daudzumam.</span><span class="sxs-lookup"><span data-stu-id="71c7f-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="71c7f-135">Atlasiet cilni **Resursu pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="71c7f-136">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-136">Select **Add**.</span></span>
1. <span data-ttu-id="71c7f-137">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="71c7f-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="71c7f-138">Laukā **Vajadzības veids** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="71c7f-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="71c7f-139">Izlemiet, vai vēlaties norādīt konkrētus resursus vai iespējas, kurām tiem jābūt.</span><span class="sxs-lookup"><span data-stu-id="71c7f-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="71c7f-140">Laukā **Vajadzība** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="71c7f-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="71c7f-141">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]