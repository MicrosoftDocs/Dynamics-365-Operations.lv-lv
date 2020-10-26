---
title: Aprēķināt MK, izmantojot viena līmeņa struktūru (2016. gada februāris)
description: Šajā procedūrā ir parādīts, kā aprēķināt pabeigtas preces izmaksas, izmantojot viena līmeņa izvēršanu, kura ir balstīta uz izmaksu aprēķināšanas lapu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83a62966e343a9b1c073c2d6ec1c1b69b1daddbb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985917"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="830e6-103">Aprēķināt MK, izmantojot viena līmeņa struktūru (2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="830e6-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="830e6-104">Šajā procedūrā ir parādīts, kā aprēķināt pabeigtas preces izmaksas, izmantojot viena līmeņa izvēršanu, kura ir balstīta uz izmaksu aprēķināšanas lapu.</span><span class="sxs-lookup"><span data-stu-id="830e6-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="830e6-105">Tas ir MK aprēķina sērijas sestais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="830e6-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="830e6-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="830e6-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="830e6-107">Dodieties uz Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="830e6-107">Go to Released products.</span></span>
2. <span data-ttu-id="830e6-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="830e6-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="830e6-109">Atlasiet preci BOM_1.</span><span class="sxs-lookup"><span data-stu-id="830e6-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="830e6-110">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="830e6-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="830e6-111">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="830e6-111">Click Item price.</span></span>
5. <span data-ttu-id="830e6-112">Noklikšķiniet uz Aprēķināt krājuma izmaksas.</span><span class="sxs-lookup"><span data-stu-id="830e6-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="830e6-113">Lai augšējā izvēlnē redzētu šo opciju, iespējams, ir jānoklikšķina uz daudzpunktes (...).</span><span class="sxs-lookup"><span data-stu-id="830e6-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="830e6-114">Laukā Izmaksu aprēķināšanas versija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="830e6-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="830e6-115">Šajā demonstrācijā atlasiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="830e6-115">For this demo, select 10.</span></span> <span data-ttu-id="830e6-116">Tā ir tā pati izmaksu aprēķināšanas versija, kas tika izmantota izmaksu cenas pievienošanai komponentiem.</span><span class="sxs-lookup"><span data-stu-id="830e6-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="830e6-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="830e6-117">Click OK.</span></span>
8. <span data-ttu-id="830e6-118">Noklikšķiniet uz Skatīt detalizētu informāciju par aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="830e6-118">Click View calculation details.</span></span>
    * <span data-ttu-id="830e6-119">Lai augšējā izvēlnē redzētu šo opciju, iespējams, ir jānoklikšķina uz daudzpunktes (...).</span><span class="sxs-lookup"><span data-stu-id="830e6-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="830e6-120">Izmaksu sastāvs: \* 10 — atvasināts no ITEM_A, 10 — no ITEM_B, 10 — no BOM_2.</span><span class="sxs-lookup"><span data-stu-id="830e6-120">Here's the composition of the cost:  \*    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="830e6-121">Šajā gadījumā nav informācijas par BOM_2, jo tas tika ievadīts kā standarta izmaksas 10, bet nav iegūts, veicot aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="830e6-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="830e6-122">\* 7 tiek atvasināts no uzstādīšanas laika, kuram ir konstantas izmaksas, un papildu 7 tiek atvasināts no izpildlaika darbības (Process).</span><span class="sxs-lookup"><span data-stu-id="830e6-122">\*    7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="830e6-123">\* Pastāv arī citas summas, kas atbilst netiešajām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="830e6-123">\*    There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="830e6-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="830e6-124">@SysTaskRecorder:_RequestClose</span></span>

