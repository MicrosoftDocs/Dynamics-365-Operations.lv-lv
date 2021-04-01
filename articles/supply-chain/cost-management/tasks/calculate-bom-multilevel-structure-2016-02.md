---
title: Aprēķināt MK, izmantojot vairāklīmeņu struktūru (2016. gada februāris)
description: Šajā procedūrā ir parādīts, kā aprēķināt pabeigtas preces izmaksas, izmantojot vairāklīmeņu izvēršanu, kura ir balstīta uz izmaksu aprēķināšanas lapu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bbbc1e3c7941fd12991f1f6eaec4e9daf35fde9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239513"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="7026e-103">Aprēķināt MK, izmantojot vairāklīmeņu struktūru (2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="7026e-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7026e-104">Šajā procedūrā ir parādīts, kā aprēķināt pabeigtas preces izmaksas, izmantojot vairāklīmeņu izvēršanu, kura ir balstīta uz izmaksu aprēķināšanas lapu.</span><span class="sxs-lookup"><span data-stu-id="7026e-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="7026e-105">Tas ir MK aprēķina sērijas septītais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="7026e-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="7026e-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="7026e-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="7026e-107">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="7026e-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="7026e-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7026e-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7026e-109">Atlasiet preci BOM_1.</span><span class="sxs-lookup"><span data-stu-id="7026e-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="7026e-110">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7026e-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="7026e-111">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="7026e-111">Click Item price.</span></span>
5. <span data-ttu-id="7026e-112">Noklikšķiniet uz Aprēķināt krājuma izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7026e-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="7026e-113">Lai augšējā izvēlnē redzētu šo opciju, iespējams, ir jānoklikšķina uz daudzpunktes (...).</span><span class="sxs-lookup"><span data-stu-id="7026e-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="7026e-114">Laukā Izmaksu aprēķināšanas versija ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="7026e-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="7026e-115">Atlasiet 20. izmaksu aprēķināšanas versiju, jo tās plānoto izmaksu tips un izvēršanas režīms ir Vairāklīmeņu.</span><span class="sxs-lookup"><span data-stu-id="7026e-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="7026e-116">Vairāklīmeņu izvēršanas režīms ir paredzēts plānotajām izmaksām un simulācijām.</span><span class="sxs-lookup"><span data-stu-id="7026e-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="7026e-117">Tas netiek izmantots standarta izmaksām.</span><span class="sxs-lookup"><span data-stu-id="7026e-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="7026e-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7026e-118">Click OK.</span></span>
8. <span data-ttu-id="7026e-119">Noklikšķiniet uz Skatīt detalizētu informāciju par aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="7026e-119">Click View calculation details.</span></span>
    * <span data-ttu-id="7026e-120">Lai augšējā izvēlnē redzētu šo opciju, iespējams, ir jānoklikšķina uz daudzpunktes (...).</span><span class="sxs-lookup"><span data-stu-id="7026e-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="7026e-121">Šajā gadījumā ievērojiet, kā BOM_2 tika aprēķināts, ņemot vērā izejmateriālu, procesu un pieskaitāmās izmaksas ar kopējo summu 29,40, nevis standarta izmaksu summu 10, kas tika aktivizēta šīs sērijas sākotnējā uzdevuma ceļvedī.</span><span class="sxs-lookup"><span data-stu-id="7026e-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="7026e-122">Noklikšķiniet uz cilnes Izmaksu aprēķināšanas lapa.</span><span class="sxs-lookup"><span data-stu-id="7026e-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="7026e-123">Pārejot uz cilni Izmaksu aprēķināšanas lapa, izmaksu grupu kopsummas atšķiras, salīdzinājumā ar iepriekšējā uzdevuma ceļvedī veiktajiem aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="7026e-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="7026e-124">Laukā Līmenis atlasiet “Multi”.</span><span class="sxs-lookup"><span data-stu-id="7026e-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="7026e-125">Atlasot vienumu Multi, izmaksas tiek klasificētas atbilstoši BOM_2 sastāvam, kur 10 tiek atvasināts no M1 izmaksu grupas (ITEM_C) un 15,60 tiek atvasināts no tās ražošanas, kur izmaksu grupa ir L2.</span><span class="sxs-lookup"><span data-stu-id="7026e-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="7026e-126">Arī netiešās izmaksas atšķiras.</span><span class="sxs-lookup"><span data-stu-id="7026e-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="7026e-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7026e-127">Close the page.</span></span>
12. <span data-ttu-id="7026e-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7026e-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]