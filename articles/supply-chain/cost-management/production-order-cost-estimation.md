---
title: Ražošanas pasūtījuma izmaksu novērtējums
description: Šajā rakstā ir sniegta informācija par ražošanas izmaksu novērtējumu. Ražošanas izmaksu novērtējums sniedz plānotajam ražošanas pasūtījuma daudzumam paredzētās krājuma ražošanas materiālu un veiktspējas patēriņa izmaksas.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93546fc170757ee2c39144842bae12d78400fd32
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2019
ms.locfileid: "350485"
---
# <a name="production-order-cost-estimation"></a><span data-ttu-id="42726-104">Ražošanas pasūtījuma izmaksu novērtējums</span><span class="sxs-lookup"><span data-stu-id="42726-104">Production order cost estimation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42726-105">Šajā rakstā ir sniegta informācija par ražošanas izmaksu novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="42726-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="42726-106">Ražošanas izmaksu novērtējums sniedz plānotajam ražošanas pasūtījuma daudzumam paredzētās krājuma ražošanas materiālu un veiktspējas patēriņa izmaksas.</span><span class="sxs-lookup"><span data-stu-id="42726-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="42726-107">Kad ir izveidots ražošanas pasūtījums, jums ir jānovērtē ražošanas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="42726-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="42726-108">Nolūks ir novērtēt krājumu un maršruta patēriņu attiecīgajam ražošanas procesam, jo šie novērtējumi tiek izmantoti turpmāko plānošanas un ražošanas procesu pamatā.</span><span class="sxs-lookup"><span data-stu-id="42726-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="42726-109">Ražošanas izmaksu novērtējums</span><span class="sxs-lookup"><span data-stu-id="42726-109">Production cost estimation</span></span>
<span data-ttu-id="42726-110">Ražošanas izmaksu novērtējumi ir balstīti uz tālāk uzskaitīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="42726-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="42726-111">Ražošanas pasūtījuma daudzums</span><span class="sxs-lookup"><span data-stu-id="42726-111">The quantity on the production order</span></span>
-   <span data-ttu-id="42726-112">Ražošanas materiālu komplektu (MK) komponenti</span><span class="sxs-lookup"><span data-stu-id="42726-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="42726-113">Ražošanas maršrutā iekļautās maršrutēšanas operācijas</span><span class="sxs-lookup"><span data-stu-id="42726-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="42726-114">Netiešās izmaksas, kas attiecas uz komponentiem un operācijām</span><span class="sxs-lookup"><span data-stu-id="42726-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="42726-115">Aktīvo izmaksu dati aprēķina datumā</span><span class="sxs-lookup"><span data-stu-id="42726-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="42726-116">Ja ražošanas materiālu komplektos (MK) pastāv fantoma rindas krājums, tad aprēķini atspoguļo fantoma komponentus un maršruta operācijas.</span><span class="sxs-lookup"><span data-stu-id="42726-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="42726-117">Novērtēšanas uzdevumu varat izmantot novērtēto izmaksu pārrēķināšanai, lai tās atspoguļotu atjaunināto informāciju.</span><span class="sxs-lookup"><span data-stu-id="42726-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="42726-118">Piemēram, atjauninātā informācija varētu būt izmaiņas ražošanas pasūtījuma daudzumā, ražošanas MK komponentos, maršrutēšanas operācijās ražošanas maršrutā, uz šiem komponentiem un operācijām attiecinātajās netiešajās izmaksās, vai aktīvajiem izmaksu datiem pārrēķina datumā.</span><span class="sxs-lookup"><span data-stu-id="42726-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="42726-119">Novērtēto izmaksu aprēķini var tikt izmantoti arī ražotā krājuma ieteicamās pārdošanas cenas noteikšanai, izmantojot metodi izmaksas-plus-uzcenojums.</span><span class="sxs-lookup"><span data-stu-id="42726-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="42726-120">Novērtēto izmaksu aprēķinus pēc izvēles var izmantot, lai atsauktos uz pasūtījumiem, kas atspoguļo citus ar šo ražošanas pasūtījumu saistītos ražošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="42726-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="42726-121">Skatīt novērtētās izmaksas</span><span class="sxs-lookup"><span data-stu-id="42726-121">View the estimated costs</span></span>
<span data-ttu-id="42726-122">Kad ir izpildīta novērtēšana, rezultātus varat skatīt lapā **Cenas aprēķins**.</span><span class="sxs-lookup"><span data-stu-id="42726-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="42726-123">Novērtēšanā tiek aprēķinātas tālāk uzskaitītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="42726-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="42726-124">**Ražošanas izmaksas** — ražošanas izmaksas ir novērtējuma augšējā rinda.</span><span class="sxs-lookup"><span data-stu-id="42726-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="42726-125">Tā parāda kopējās ražošanas pasūtījuma realizācijas izmaksas un kopējo ražojuma pārdošanas cenu.</span><span class="sxs-lookup"><span data-stu-id="42726-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="42726-126">Tā ir visu novērtējuma izmaksu rindu kopsumma.</span><span class="sxs-lookup"><span data-stu-id="42726-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="42726-127">**Maršruta vai resursu izmaksas** — maršruta vai resursu izmaksas ir izmaksas par ražošanas operācijām.</span><span class="sxs-lookup"><span data-stu-id="42726-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="42726-128">Tās ietver izmaksas par tādiem elementiem kā uzstādīšanas laiks, izpildlaiks un pieskaitāmās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="42726-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="42726-129">**Materiālu izmaksas** — materiālu izmaksas ir krājuma ražošanai nepieciešamā materiālu komplekta (MK) komponentu izmaksas un cenas.</span><span class="sxs-lookup"><span data-stu-id="42726-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="42726-130">Šīs izmaksas ir noteiktas un sistēmā ievadītas jau iepriekš.</span><span class="sxs-lookup"><span data-stu-id="42726-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="42726-131">Citi izmaksu novērtējuma lietojumi</span><span class="sxs-lookup"><span data-stu-id="42726-131">Other uses of cost estimation</span></span>
<span data-ttu-id="42726-132">Izmaksu novērtējums sniedz arī tālāk uzskaitīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="42726-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="42726-133">Jēgpilni cenu piedāvājumi</span><span class="sxs-lookup"><span data-stu-id="42726-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="42726-134">Pasūtījuma rentabilitātes novērtējumi</span><span class="sxs-lookup"><span data-stu-id="42726-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="42726-135">Izejmateriālu lietojuma novērtējumi</span><span class="sxs-lookup"><span data-stu-id="42726-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="42726-136">Cenu informācijas salīdzinājumu no iepriekšējās ražošanas</span><span class="sxs-lookup"><span data-stu-id="42726-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="42726-137">Budžeta un prognozēšanas informācija</span><span class="sxs-lookup"><span data-stu-id="42726-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="42726-138">Noteiktas cenas uzturēšanai nepieciešamo ražošanas apmēru novērtējumi</span><span class="sxs-lookup"><span data-stu-id="42726-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>




