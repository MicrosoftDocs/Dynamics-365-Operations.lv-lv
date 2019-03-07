---
title: Aprēķināt MK, izmantojot vairāklīmeņu struktūru (2016. gada februāris)
description: Šajā procedūrā ir parādīts, kā aprēķināt pabeigtas preces izmaksas, izmantojot vairāklīmeņu izvēršanu, kura ir balstīta uz izmaksu aprēķināšanas lapu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcc1248d64145c10f1c67bfac49c053e99dc1598
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "323368"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="82eea-103">Aprēķināt MK, izmantojot vairāklīmeņu struktūru (2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="82eea-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82eea-104">Šajā procedūrā ir parādīts, kā aprēķināt pabeigtas preces izmaksas, izmantojot vairāklīmeņu izvēršanu, kura ir balstīta uz izmaksu aprēķināšanas lapu.</span><span class="sxs-lookup"><span data-stu-id="82eea-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="82eea-105">Tas ir MK aprēķina sērijas septītais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="82eea-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="82eea-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="82eea-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="82eea-107">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="82eea-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="82eea-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="82eea-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="82eea-109">Atlasiet preci BOM_1.</span><span class="sxs-lookup"><span data-stu-id="82eea-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="82eea-110">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="82eea-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="82eea-111">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="82eea-111">Click Item price.</span></span>
5. <span data-ttu-id="82eea-112">Noklikšķiniet uz Aprēķināt krājuma izmaksas.</span><span class="sxs-lookup"><span data-stu-id="82eea-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="82eea-113">Lai augšējā izvēlnē redzētu šo opciju, iespējams, ir jānoklikšķina uz daudzpunktes (...).</span><span class="sxs-lookup"><span data-stu-id="82eea-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="82eea-114">Laukā Izmaksu aprēķināšanas versija ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="82eea-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="82eea-115">Atlasiet 20. izmaksu aprēķināšanas versiju, jo tās plānoto izmaksu tips un izvēršanas režīms ir Vairāklīmeņu.</span><span class="sxs-lookup"><span data-stu-id="82eea-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="82eea-116">Vairāklīmeņu izvēršanas režīms ir paredzēts plānotajām izmaksām un simulācijām.</span><span class="sxs-lookup"><span data-stu-id="82eea-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="82eea-117">Tas netiek izmantots standarta izmaksām.</span><span class="sxs-lookup"><span data-stu-id="82eea-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="82eea-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="82eea-118">Click OK.</span></span>
8. <span data-ttu-id="82eea-119">Noklikšķiniet uz Skatīt detalizētu informāciju par aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="82eea-119">Click View calculation details.</span></span>
    * <span data-ttu-id="82eea-120">Lai augšējā izvēlnē redzētu šo opciju, iespējams, ir jānoklikšķina uz daudzpunktes (...).</span><span class="sxs-lookup"><span data-stu-id="82eea-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="82eea-121">Šajā gadījumā ievērojiet, kā BOM_2 tika aprēķināts, ņemot vērā izejmateriālu, procesu un pieskaitāmās izmaksas ar kopējo summu 29,40, nevis standarta izmaksu summu 10, kas tika aktivizēta šīs sērijas sākotnējā uzdevuma ceļvedī.</span><span class="sxs-lookup"><span data-stu-id="82eea-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="82eea-122">Noklikšķiniet uz cilnes Izmaksu aprēķināšanas lapa.</span><span class="sxs-lookup"><span data-stu-id="82eea-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="82eea-123">Pārejot uz cilni Izmaksu aprēķināšanas lapa, izmaksu grupu kopsummas atšķiras, salīdzinājumā ar iepriekšējā uzdevuma ceļvedī veiktajiem aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="82eea-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="82eea-124">Laukā Līmenis atlasiet “Multi”.</span><span class="sxs-lookup"><span data-stu-id="82eea-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="82eea-125">Atlasot vienumu Multi, izmaksas tiek klasificētas atbilstoši BOM_2 sastāvam, kur 10 tiek atvasināts no M1 izmaksu grupas (ITEM_C) un 15,60 tiek atvasināts no tās ražošanas, kur izmaksu grupa ir L2.</span><span class="sxs-lookup"><span data-stu-id="82eea-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="82eea-126">Arī netiešās izmaksas atšķiras.</span><span class="sxs-lookup"><span data-stu-id="82eea-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="82eea-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="82eea-127">Close the page.</span></span>
12. <span data-ttu-id="82eea-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="82eea-128">Close the page.</span></span>

